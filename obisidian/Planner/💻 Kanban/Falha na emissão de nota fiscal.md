#001
001=03.00
002=11
#002
001=000000000
002=unknown ISC error 0
[AddInfo]
SQL: UPDATE NFE_TBITEMSPENDENTES 
SET INMONITOR = -1,
STATUS = ?STATUS,
MOTIVO = ?MOTIVO,
TRYCOUNT = NULL
WHERE GID = ?GID
RETURNING GID, VERSAOREGISTRO
M‚todo: ExecQuery
003=
004=
005=
006=41241076062488000739550060001024701147967635
007=
#003
001=CHAVE=01110247010165413

# Comentários 
## 18-10-2024
enviado mensagem par ao Evandro para saber o que pode estar acontecendo essa falha. 
## 17-10-2024
verificar o porque está dando a falha na emissão de nota fiscal, ao reenviar o arquivo de texto ele é aprovado. 