⚽ API – Sistema de Gestão de Futebol Amador

🎓 Contexto Acadêmico

Curso: Desenvolvimento de Software – Back-End

Projeto desenvolvido como parte da formação prática em construção de APIs REST.

📑 Sumário
Visão Geral
Tecnologias Utilizadas
Estrutura do Projeto
Funcionalidades e Modelos de Dados
Documentação da API
Configuração do Ambiente
Licença
📌 Visão Geral

O Sistema de Gestão de Futebol Amador é uma API backend desenvolvida para auxiliar organizadores na criação e gerenciamento de peladas e campeonatos.

O sistema permite o cadastro e controle de jogadores com níveis de habilidade, servindo como base para funcionalidades futuras como sorteio de times balanceados, gerenciamento de partidas e estatísticas.

A aplicação foi construída utilizando Node.js com Express, banco de dados relacional (PostgreSQL) e o ORM Prisma, seguindo boas práticas de organização, segurança e escalabilidade.

🛠️ Tecnologias Utilizadas
Tecnologia	Versão Recomendada	Descrição
Node.js	>= 18	Ambiente de execução JavaScript.
Express.js	^4.x	Framework para criação de APIs REST.
Prisma ORM	latest	ORM moderno para manipulação de banco de dados.
PostgreSQL	>= 14	Banco de dados relacional.
bcrypt	latest	Hash de senhas.
jsonwebtoken	latest	Autenticação via JWT.
dotenv	latest	Variáveis de ambiente.
cors	latest	Controle de acesso entre origens.

📌 Consulte o package.json para versões exatas.

📁 Estrutura do Projeto

O projeto segue uma arquitetura baseada em separação de responsabilidades:

backend/
 ├── src/
 │   ├── controllers/         # Lógica de requisição/resposta
 │   ├── routes/              # Definição das rotas
 │   ├── middlewares/         # Autenticação e validações
 │   ├── services/            # Regras de negócio
 │   ├── prisma/              # Schema e configuração do banco
 │   └── app.js               # Configuração do Express
 ├── server.js                # Inicialização do servidor
 ├── .env                     # Variáveis de ambiente
 ├── package.json
 └── README.md
⚙️ Funcionalidades e Modelos de Dados
🔐 Autenticação de Organizadores
Cadastro de organizador
Login com JWT
Proteção de rotas
Edição de perfil
👥 Gestão de Jogadores
Cadastro de jogadores
Edição de dados
Desativação (soft delete)
Listagem por organizador
📊 Modelos de Dados
Entidade	Descrição
Organizador	Usuário do sistema com acesso às funcionalidades.
Jogador	Jogador cadastrado com nível de habilidade e status ativo/inativo.
📡 Documentação da API

A API segue o padrão REST, utilizando JSON.

🔐 Autenticação
Endpoints
Método	Endpoint	Descrição
POST	/auth/register	Cadastro de organizador
POST	/auth/login	Login e geração de token
GET	/auth/me	Dados do usuário autenticado
🔒 Autorização

A API utiliza JWT (JSON Web Token).

As rotas protegidas exigem:

Authorization: Bearer <token>
👥 Endpoints de Jogadores
Método	Endpoint	Descrição
GET	/jogadores	Lista jogadores do organizador
POST	/jogadores	Cria um jogador
PUT	/jogadores/:id	Atualiza jogador
DELETE	/jogadores/:id	Desativa jogador
📌 Regras de Negócio
Cada organizador acessa apenas seus próprios dados
Jogadores não são excluídos, apenas desativados
Nível de habilidade varia de 0.5 a 5.0
Rotas protegidas por autenticação JWT
⚙️ Configuração do Ambiente
📌 Pré-requisitos
Node.js (>= 18)
PostgreSQL (ou SQLite para desenvolvimento)
🚀 Instalação
git clone https://github.com/Gabriel0879/Sistema-de-Gest-o-de-Futebol-Amador.git
cd Sistema-de-Gest-o-de-Futebol-Amador
npm install
🔧 Variáveis de ambiente

Crie um .env:

PORT=3000
DATABASE_URL="sua_url_do_banco"
JWT_SECRET="sua_chave_secreta"
🗄️ Banco de dados
npx prisma migrate dev
▶️ Rodar o projeto
npm run dev
📊 Status do Projeto

🚧 Em desenvolvimento – Sprint 3 concluída

Próximas funcionalidades:
Criação de peladas
Lista de inscritos
Sorteio de times
Jogo ao vivo
👨‍💻 Autor

Gabriel Santos

📄 Licença

Este projeto está sob a licença MIT.
