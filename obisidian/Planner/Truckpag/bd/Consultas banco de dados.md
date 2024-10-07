#truckpag #sql #bancodedados 
# Consulta de clientes
`select * from SNC_COMPANY c`
# Consulta de parâmetros 
`select * from empresa_parametros_vinculados epv`

# Consulta de todos os serviços
`select * from SERVICE s`

# Buscar parâmetros cadastrados dentro da empresa
`select * from empresa_parametros_vinculados epv where epv.empresa_id = :id`

## Buscando título por cliente Gestão de manutenção
```
SELECT DISTINCT mos.manutencao_ordem_servico_id AS 'Ordem Serviço',

cli.COM_NM_FANCY AS 'Cliente',

cli.COM_NR_CNPJ AS 'CNPJ Cliente',

est.COM_NM_FANCY AS 'Estabelecimento',

est.COM_NR_CNPJ AS 'CNPJ Estabelecimento',

tl.cd_titulo AS 'Título',

tl.dt_vencimento AS 'Título Vencimento',

dnf.nfe_numero AS 'Número NFe',

dnf.nfse_numero AS 'Número NFSe',

CONVERT(MONEY, mos.valor) AS 'Valor Ordem Serviço',

(SELECT SUM(manutencao_item_valor)

FROM manutencao_ordem_servico_item mosi

WHERE mosi.manutencao_ordem_servico_id = mos.manutencao_ordem_servico_id) AS 'Valor Produtos',

(SELECT SUM(manutencao_servico_valor)

FROM manutencao_ordem_servico_item mosi

WHERE mosi.manutencao_ordem_servico_id = mos.manutencao_ordem_servico_id) AS 'Valor Serviços',

mos.quantidade_parcelas AS 'Quantidade Parcelas',

mos.valor_parcela AS 'Valor Parcela',

CONCAT(

ROW_NUMBER() OVER (

PARTITION BY mos.manutencao_ordem_servico_id

ORDER BY t.TRC_DT_RECEIVE

),

'/',

mos.quantidade_parcelas

) AS "Número Parcela"

FROM manutencao_ordem_servico mos

join MANUALTRANSACTION m on mos.manutencao_ordem_servico_id = m.manutencao_ordem_servico_id

join daf_notas_fiscais dnf on mos.manutencao_ordem_servico_id = dnf.manutencao_ordem_servico_id

join SNC_COMPANY est on est.COM_ID = mos.estabelecimento_id

join SNC_COMPANY cli on cli.COM_ID = mos.cliente_id

join transacoes_cobrancas tc on m.MTR_ID = tc.transacao_id

join TRANSACTIONCHARGE t on tc.cobranca_id = t.TRC_ID

join titulo tl on tl.cd_nf_reembolso = t.cd_nf_reembolso

WHERE tl.cd_cliente in (17481)

AND tl.deleted_at is null

AND t.COM_ID = mos.cliente_id

AND tl.dt_pagamento is null

ORDER BY tl.dt_vencimento;
```