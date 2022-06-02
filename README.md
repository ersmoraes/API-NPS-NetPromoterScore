# API-NPS-NetPromoterScore

API de envio de pesquisa de satisfação via e-mail, desenvolvida totalmente no backend.

![App Screenshot](src/views/NPS_API.png)

Utilizado das seguintes tecnologias:

- Express
- Handlesbars
- Nodemailer
- SQlite3
- typeORM
- uuid
- yup
- teste de integração em Jest
- supertest

Após realizar o download do repositorio basta abrir o seu editor de texto, instalar as dependencias do projeto
utilizando "npm installl" ou "yarn add".

Depois de instalar as dependencias, basta executar os comando:
yarn dev ou npm run dev, para iniciar o servidor.
yarn test ou npm run test, para executar os testes de integrações.

Após iniciar o servidor, abra o Insominia para fazer os teste de cominicação e execução da API

- Para cadastrar um usuário utilize o metodo POST na rota "http://localhost:3333/users"
{
	"name": "Informe um nome",
	"email": "Informe o e-mail"
}

- Para cadastrar a pesquisa que deseja enviar utilize o metodo POST na rota "http://localhost:3333/surveys"
{
	"title": "Informe o titulo",
	"description": "Informe a descrição"
}

- Depois de realizar essas duas etapas abra o arquivo database.sqlite, recomendo abrir no "Beekkeper"
copie o "id" da coluna "id" na tabela "surveys".

- Acesse o Insominia novamente, acesse a rota "http://localhost:3333/sendMail" utilizando o metodo GET
{
	"email": "informe o email do usuário já cadastrado",
	"survey_id": "cole o ID que você copiou na tabela 'surveys'"
}

- Após da um "Send" no seu terminal do editor de Texto Irá gerar um link simulando a entrega desse e-mail em uma caixa de entrada.

