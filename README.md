## plann.er
### NLW Journey (RocketSeat)
- O projeto Journey tem como objetivo ajudar o usuário a organizar viagens à trabalho ou lazer. O usuário pode criar uma viagem com nome, data de início e fim. Dentro da viagem o usuário pode planejar sua viagem adicionando atividades para realizar em cada dia.
- Utilizando IntelliJ e Visual Studio Code
- Insomnia para testes

#### Json para testes
{
    "destionation": "Florianópolis, SC",
    "starts_at": "2024-06-25T21:51:54.7342",
    "ends_at": "2024-06-25T21:51:54.7342",
    "emails_to_invite": ["convidado@rocketseat.com"],
    "owner_name": "Fernanda",
    "owner_email": "fernanda@rocketseat.com"
}

------------------------------------------------------------------------------------------
## Requisitos

#### Requisitos funcionais

1. O usuário cadastra uma viagem informando o local de destino, data de início, data de término, e-mails dos convidados e também seu nome completo e endereço de e-mail;
2. O criador da viagem recebe um e-mail para confirmar a nova viagem através de um link. Ao clicar no link, a viagem é confirmada, os convidados recebem e-mails de confirmação de presença e o criador é redirecionado para a página da viagem;
3. Os convidados, ao clicarem no link de confirmação de presença, são redirecionados para a aplicação onde devem inserir seu nome (além do e-mail que já estará preenchido) e então estarão confirmados na viagem;
4. Na página do evento, os participantes da viagem podem adicionar links importantes da viagem como reserva do AirBnB, locais para serem visitados, etc...
5. Ainda na página do evento, o criador e os convidados podem adicionar atividades que irão ocorrer durante a viagem com título, data e horário;
6. Novos participantes podem ser convidados dentro da página do evento através do e-mail e assim devem passar pelo fluxo de confirmação como qualquer outro convidado

#### Criando o projeto
- [X] Criar projeto usando [Spring Initializr](https://start.spring.io/)
    - Spring Web
    - Flyway
    - Dev Tools
    - Lombok
    - JPA
    - H2 Database
- [X] Configurar banco de dados na aplicação
- [X] Criar migration para criação da tabela `trips`
   - Arquivos de Migration representam mudanças na estrutura do nosso banco de dados
   - criar uma tabela
   - alterar tabela, removendo campo, adicionando um campo
   - instalacao de driver
   - inserção em massa, de dados default
   - Arquivos de migration ⇒ scripts SQL, rodar comandos no banco
- [X] Criar entidades que irá representar uma `Trip`
- [X] Criar repository da entidade viagem
- [X] Criar endpoint de cadastro de viagem **`POST**/trips`
- [X] Criar endpoint de consulta de viagem **`GET**/trips/{tripId}`
- [X] Criar endpoint de atualização de viagem **`PUT**/trips/{tripId}`
- [X] Criar endpoint confirmação de viagem **`GET**/trips/{tripId}/confirm`
- [X] Criar tabela de `Participant`
- [X] Criar entidade que irá representar um`Participant`
- [X] Criar repository da entidade participante
- [X] Criar endpoint confirmação de participante **`POST**/participants/{participantId}/confirm`
- [X] Criar endpoint para convidar participante **`POST**/trips/{tripId}/invites`
- [X] Criar endpoint para consultar participantes **`GET**/trips/{tripId}/participants`
- [X] Criar tabela de `Activities`
- [X] Criar entidade que irá representar uma `Activity`
- [X] Criar repository da entidade atividade
- [X] Criar endpoint para cadastro de atividade **`POST**/trips/{tripId}/activities`
- [X] Criar endpoint para consultar atividades de uma viagem **`GET**/trips/{tripId}/invites`
- [X] Criar tabela de `Links`
- [X] Criar entidade que irá representar um `Link`
- [X] Criar repository da entidade links
- [X] Criar endpoint para criação de link **`POST**/trips/{tripId}/links`
- [X] Criar endpoint para consultar links de uma viagem **`GET**/trips/{tripId}/links`

#### Features extras

- [X] Adicionar uma validação nos campos de data
- [X] A data de começo da viagem, é inferior a data de término viagem
- [X] A data de uma atividade está entre as datas da viagem    
Exemplo: viagem entre os dias 20 á 25 de julho no Rio de Janeiro
  ⇒ Atividade 19 de julho
  ⇒ Atividade 21 de julho
- [X] Extração do core das trips pra dentro de uma classe Service
- [X] Mapeamento das exceções da nossa aplicação
- [X] Com tratativas de erro personalizadas

------------------------------------------------------------------------------------------
