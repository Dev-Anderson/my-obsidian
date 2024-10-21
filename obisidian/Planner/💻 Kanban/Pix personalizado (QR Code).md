#truckpag #gestaofrotas 
# Descrição
Pix personalizado
1. Acessar a tela "Gestão QRCode PIX"
2. Gerar um QR code para a empresa
3. Depois o cliente consegue mandar um valor para a truckpag 
Depois que entra o dinheiro, ela vai utilizar esse dinheiro para abater as faturas em aberto
-------------

- verificar a baixa está correta; 
 Na fase de teste; 
Falha 
- Quando realizado PIX é o valor total do titulo porém sobra um valor, neste caso não rodou a tarefa de baixa, a Maieza e o Djonathan fizeram uma correção, agora a vai rodar a cada 2 horas; 
- Melhorias 
	- Travar apenas abastecimento e também manutenção básica
	- mostrar o limite no cadastro do cliente
As tarefas de melhorias já estão em andamento; 
5595 - mostrar saldo do PIX (prazo 21/10/2024); 
- back end = OK 
- Está na fila do front-end, já falei com o Fernando pra agilizar a tarefa
5618 - correções no PIX; 
em desenvolvimento
# Comentários
## 18-10-2024
### 11:04
Foi aberto aberto uma tarefa para ajustar a data de pagamento segundo o Ronaldo a data de pagamento precisa ser a data de pagamento que ele recebeu o PIX. 
Pensando melhor, se você trazer isso para a conta normal, a data de pagamento sempre vai ser a data que você fez a compra, exemplo: 
Se você tem um saldo de R$ 10,00 e esse R$ 10,00 foi recebido dia 10/10 por exemplo e fizer uma compra no dia 20/10 a data do pagamento vai ser 20/10 e não dia 10/10, o PIX da truckpag vai funcionar da mesma forma 
## 17-10-2024
### 14:17
Ronaldo passou que será concluído o teste amanhã assim que gerar, amanhã precisa entrar em contato com ele novamente para ver como que foi os testes; 
## 16-10-2024
### 08:16
enviei mensagem para o Misa para verificar as tarefas que estão em CR porque estão em atraso; 
## 15-10-2024
### 11:50
Ronaldo entrou em contato falando que deu falha na baixa do titulo da 3sat valor de R$ 200,00 precisa ver isso; 
### 09:24
Em conversa com o Misa o Dev vai terminar hoje; 
## 14-10-2024
### 15:27
enviado mensagem para o Misa, para saber o porque a tarefa ainda não foi concluida.
### 08:03
A tarefa 5618 ainda está em desenvolvimento, precisa verificar uma estimativa para a tarefa; 
## 11-10-2024
### 10:16
em call junto com os responsaveis, fizemos alguns levantamentos
- tarefa agendada a cada 2 horas 
## 10-10-2024
### 15:26
teste realizado junto com o Ronaldo + Felipe
Teste 01 
Fazer um pix de R$ 200,00 verificar se vai entrar no titulo em aberto = OK 
Teste 02 
Fazer um pix de R$ 100,00 verificar se ele vai abater no titulo em abert e depois ele não fica duplicado = OK 
Teste 03 
Fazer um pix no valor maior que o titulo e depois verificar se vai abater o tiulo em aberto e depois ficar um saldo de crédito => Em fase de teste vai concluir amanhã de manhã quanto tiver outro titulo; 

## 07-10-2024
### 11:52
enviado mensagem para a Maieza para saber se será possível cumprir com o prazo enviado; 

### 10:22
em conversa com os Devs será publicado uma correção até amanhã com as alterações. 
eu vou falar com o Ronaldo para fazer o teste amanhã a tarde. 
## 26-09-2024
### 09:14
reunião com o pessoal do financeiro. 