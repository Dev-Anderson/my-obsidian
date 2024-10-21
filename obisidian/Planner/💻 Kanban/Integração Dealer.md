# Descrição 
Reunião para tratar dos testes dos endponits e como que será os testes; 
Sobre o cancelamento: 
Individual 
	 vamos fazer o cancelamento apenas se não tiver pago
Consolidado 
	vamos fazer o cancelamento apenas se não tiver faturado

## Verificar 
- v<span style="color:rgb(255, 192, 0)">erificar sobre o ID Paccar parts quando tem mais de uma empresa exemplo matriz e filial como que vamos fazer para consultar o crédito</span>; 
	- Alterar o endpoint de criar OS porque não tem como consultar o crédito do cliente; 
	- verificar o cadastro de filial dentro do cadastro do cliente; 
- <span style="color:rgb(255, 192, 0)">é possível fazer o faturamento de várias tipos os de uma única vez ?</span>
	- isso vai impactar o upload de nota fiscal
- <span style="color:rgb(255, 192, 0)">como que vamos fazer com o cancelamento de nota fiscal ? </span>
	- verificar como que faz dentro do Dealer
- <span style="color:rgb(255, 192, 0)">como que vamos fazer com a alteração de nota fiscal ? </span>
	- boleto que foi pago não mexe
	- agendar uma reunião com o financeiro e também os envolvidos
- <span style="color:rgb(255, 192, 0)">não tem o endpoint de consulta de venda balcão; </span>
- o que vamos fazer com os clientes que não tem veículo cadastrado; 
	- vamos ter que criar um novo endpoint para consultar a placa do veiculo 
- <span style="color:rgb(255, 192, 0)">como que vamos fazer com as vendas balcão que não precisa de placa ? </span>
	- placa coringa sempre deve mandar isso
- <span style="color:rgb(255, 192, 0)">Como que vamos fazer para mostrar os títulos para o Dealer ? </span>
	- título nós vamos ver

5631 - endpoint de upload de nota
5640 - Remover obrigação da placa (3 dias)
# Comentários
## 17-10-2024
### 14:13
precisa montar um roadmap para o pessoal da DAF até dia 18/10/2024
## 16-10-2024
### 14:09
Dealer entrou em contato, avisando sobre a placa do veiculo, na venda balcão isso não deve ser obrigatório, pedi para o Christian alterar isso, o Raul vai abrir uma tarefa e também pedi uma estimativa para o Dev, aguardando a resposta
## 15-10-2024
### 15:44
enviado o e-mail sobre o cancelamento e também o collection
### 14:20
Cobrado o Joel para subir as alterações o quanto antes. 
montando o collection para envio para o pessoal do Dealer fazer os testes. 

### 10:59
concluido o endpoint de cancelamento de OS
concluido o endpoint de consulta de OS venda balcão
Avisar o pessoal do Dealer que vamos ter uma opção de fazer o cadastro de condição de pagamento por concessionaria, porém ela vai exibir apenas para a concessionária que ele tem acesso. 
## 10-10-2024
### 08:44
Duvida sobre o faturamento da nota fiscal, é possível faturar várias tipos de OS no mesmo tempo ?
Verificando isso com o Emmanuel
## 09-10-2024
### 13:59
- Novo campo de periodicidade 
foi solicitado para ver se esse novo campo vai impactar na integração, em conversa com o pessoal isso não vai impactar em nada. 
Exemplos: 
Se na hora do envio dos dados para o Dealer ele passar uma condição mensal, porém no envio das parcelas estiver quinzenal como que vamos fazer ? 
nós vamos ter validações ? 

Raul vai atualizar o manual, antes ele precisa verificar o retorno; 
## 08-10-2024
### 14:21
Dentro do manual de consulta pagamentos, deixei algumas observações para o Raul
- Realizado reunião com o pessoal do Dealer
- enviado e-mail para o pessoal do Dealer para atualizar os novos manuais
- Avisado sobre o endpoint de consulta venda balcão está tudo certo 

### 13:59
reunião com o pessoal do Dealer vamos repassar o prazo 
### 12:17
falei com o Joel pra ele verificar junto com o Dev se o prazo ainda está de pé e se vamos conseguir entregar isso. 
### 11:41
O prazo do cancelamento ainda é dia 19/10
## 01-10-2024
### 14:28
realizado reunião com o time Dealer + DAF 
COISAS QUE VAMOS AJUSTAR
- endpoints de cancelamento 
	- tipo de faturamento individual 
	- tipo de faturamento consolidado
- authorization está com problemas, no criar venda balcão; 
- 
## 30-09-2024
### 13:54
hoje concluimos a troca do ID Paccar parts para o CNPJ mandei e-mail para o pessoal do Dealer; 
## 24-09-2024
### 15:17
Agendado uma reunião com o time de negócio para tratar alguns assuntos de como que vamos exibir os tipos de faturamentos para o Dealer. 
Raul ficou responsável para montar isso no manual e também como que vamos exibir isso para o pessoal do Dealer
### 14:22
- placa coringa se vier null nós vamos atribuir a placa coringa nossa; 
- dentro da venda balcão "criar-os" o authorization precisa verificar; 
- mudar o ID paccar parts para CNPJ na validação de preço; 
- agendar reunião com o pessoal do financeiro e também o pessoal do T.I; 
### 11:37
Call com o Alex sobre os pontos levantados
- cancelamento da OS 
- ID Paccar parts com matriz e filial 
## 23-09-2024
### 10:36
montado as perguntas que eu vou precisar responder para continuar com a integração
### 08:03
precisa agendar uma reunião para verificar os seguintes pontos
- Como que vamos fazer com o cancelamento ? 
- Como que vamos fazer com a placa do veiculo ? 
- Como que vamos fazer com os tipos de faturamentos que nós temos ? 
## 20-09-2024
### 10:17
conversado com o Raul para abrir as tarefas dos endpoints que vamos precisar ajustar eles são: 
-<span style="color:rgb(255, 0, 0)"> **venda balcão**</span>
	- Cancelar nota fiscal
	- Alterar nota fiscal
<span style="color:rgb(255, 0, 0)">- **Venda oficina**</span>
	- upload nota fiscal
	- cancelar nota fiscal
	- alterar nota fiscal
## 2024-09-19


### 15:54
enviado mensagem no grupo para avisar sobre o projeto; 
montando o e-mail para o pessoal do Dealer; 
### 13:16
número para teste
os_numero = 88181
Tipo sigla id = 1135

Dentro do upload-nota 
precisa verificar se dentro do Dealer é possível fazer o faturamento de vários "tipos_os" de uma única vez; 
Verificar depois; 

Ednpoit "Excluir item"
OK

Endpoint "criar-os" venda balcão 
- o campo placa está null no retorno; 
- Como que vamos fazer com a placa nesse endpoint porque sempre precisar ter uma placa; 

### 10:15
Christian mandou mensagem pedindo para alterar o horário da reunião porque ficou de subir algumas coisas no ambiente de homologação antes da reunião. 
## 2024-09-17
### Todos os Endpoints
### Condição de pagamento
[ x ] - Consulta condição de pagamento por cliente especifico; 
### Venda balção
[ ] - Validação de preço
[ ] - Criar ordem de serviço
[ ] - Consulta todas ordem de serviço
[ ] - Consulta um ordem de serviço
### Venda oficina 
[ x ] - Criar a OS
[ ] - Alterar "os_tipos"
[ ] - 


Endpoint 
Consulta condição de pagamento = falha 

### Consulta condição de pagamento 
OK 

### Venda balcão 
#### Validação de preço e crédito
##### Ajustes
* Trocar o parâmetro da URL em vez de CNPJ informar o código frotista
* não está validando o preço corretamente
	* Exemplo: código do produto = 1626237
### Venda Balcão - Criar OS 
### Ajustes 
* campo a mais = "pedido_valor_total" : "1223,370";
* O motorista deve pegar do parâmetro "Motorista DAF Padrão";
* Falha no valor total ao criar a OS;
* Anexo do XML precisa alterar para aceitar apenas o XML da NF-e; 
### Observações
OS criada 

ID da OS = 1133
#### Alterar "os_tipos"
### Ajustes 
*  Falha no campo descricao": "Serviço desconto inválido."

### Alterar "produto_os"
#### Ajustes 
- Dentro do campo "manutencao_ordem_servico_produtos" não retornar a chave manutencao_ordem_servico_tipo_deeler_id; 
- o endpoint não está aceitando inserir mais de um produto; 
- O ID para consulta precisa alterar para "os_numero";
### Consulta OS 
#### Ajustes 
- O ID para consulta precisa alterar para "os_numero";
- O campo "servico_termino_real" não deve retornar "null" no caso de campos numericos retornar o valor zero, nas strings retornar vazio; 
- No retorno no campo "manutencao_ordem_servico_tipos_deeler" trocar para "os_tipos" igual o envio; 
- No retorno dentro chave "manutencao_ordem_servico_tipos_deeler" nos campos manutencao_ordem_servico_tipo_deeler_id e manutencao_ordem_servico_deeler_id trocar para "os_truckpag; 
- - Não precisa retornar isso "manutencao_ordem_servico_tipo_deeler_id" dentro da chave "manutencao_ordem_servico_produtos"; 

### Consulta todas as OSs 
#### Ajustes

#### Observação
- Endpoint OK 

## 2024-09-18 
### 11:51
ainda precisa falar com o Joel e também o Christian para saber como que está as alterações; 
Foi agendado reunião para dia 19/09 as 10:30 para fazer os testes; 