YardFlow - Gestão Inteligente de Pátio de Motos 🏍️
>>> ORGANIZE | LOCALIZE | FLUA <<<

O YardFlow é uma API desenvolvida em .NET 8 para controle de entrada, saída, localização, locação de motos e gerenciamento de usuários em pátios. Ideal para realizar gerenciamentos práticos e eficientes.

📌 Índice

🚀 Funcionalidades

💻 Tecnologias

📋 Pré-requisitos

🔧 Instalação

🏃 Execução

📘 Documentação da API

🗂 Estrutura

🚧 Status da Aplicação

👥 Autores

🚀 Funcionalidades

Gerenciamento de Motos:

Registro de entrada e saída de motos no pátio

Consultar status da moto (disponível, alugada, etc.)

Localização:

Consultar a localização da moto dentro do pátio

Gerenciamento de Usuários:

Cadastro de usuários do sistema

Atualização de dados de usuários

Autenticação básica via e-mail e senha

Definição de função (ex.: administrador, funcionário)

💻 Tecnologias

.NET 8

ASP.NET Core

Entity Framework Core

Oracle Database

Swagger (OpenAPI)

IDE: Visual Studio ou VS Code

📋 Pré-requisitos

.NET 8 SDK

Banco de Dados Oracle configurado

Visual Studio, VS Code ou outro editor

🔧 Instalação
git clone https://github.com/lerri05/ChallengeYardFlow.git
cd ChallengeYardFlow

Configure o arquivo appsettings.json com sua string de conexão Oracle:
"ConnectionStrings": {
  "DefaultConnection": "User Id=seu_usuario;Password=sua_senha;Data Source=seu_servidor"
}

Aplique as migrações:
dotnet ef database update

🏃 Execução

Execute o projeto localmente:

dotnet run

📘 Documentação da API

A API conta com uma interface interativa via Swagger, permitindo testar os endpoints diretamente pelo navegador.

Acesse:

https://localhost:5050/swagger  

🔗 Endpoints da API
🏍️ Motos /api/moto
Método	Endpoint	Descrição
GET	/api/moto	Lista todas as motos cadastradas
GET	/api/moto/{id}	Retorna os dados de uma moto específica
POST	/api/moto	Cadastra uma nova moto
PUT	/api/moto/{id}	Atualiza os dados de uma moto existente
DELETE	/api/moto/{id}	Remove uma moto do sistema
📅 Locações /api/locacoes
Método	Endpoint	Descrição
POST	/api/locacoes/calcular	Calcula o valor da locação de uma moto com base nas datas informadas
👤 Usuários /api/usuarios
Método	Endpoint	Descrição
GET	/api/usuarios	Lista todos os usuários cadastrados
GET	/api/usuarios/{id}	Retorna os dados de um usuário específico
POST	/api/usuarios	Cadastra um novo usuário
PUT	/api/usuarios/{id}	Atualiza os dados de um usuário existente
DELETE	/api/usuarios/{id}	Remove um usuário do sistema
🗂 Estrutura
ChallengeYardFlow
├── Controllers
│   ├── LocacoesController.cs
│   ├── MotoController.cs
│   └── UsuariosController.cs
├── Data
│   └── LocadoraContext.cs
├── Migrations
│   ├── 20250519011323_Inicial.cs
│   ├── 20250918223050_Usuario.cs
│   └── LocadoraContextModelSnapshot.cs
├── Modelo
│   ├── Locacao.cs
│   ├── Moto.cs
│   └── Usuario.cs
├── appsettings.json
├── CP2-LocadoraDeCarros.http
├── Program.cs
└── README.md

🚧 Status da Aplicação

✅ Aplicação em desenvolvimento

🚧 Cronograma de execução:

60% concluído até 01/10/2025 ( 3ª sprint)

100% previsto para conclusão na 4ª sprint

👥 Autores
Nome	RM	GitHub
Fernanda Budniak de Seda	558274	@Febudniak

Lucas Lerri de Almeida	554635	@lerri05

Karen Marques dos Santos	554556	@KarenMarquesS
