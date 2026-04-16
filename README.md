⚽ Sistema de Gestão de Futebol Amador

Sistema web desenvolvido para auxiliar na organização e gestão de futebol amador, permitindo o controle de jogadores, peladas e campeonatos de forma simples e eficiente.

🎯 Objetivo

O objetivo do projeto é digitalizar e organizar a gestão de jogos e competições amadoras, substituindo controles manuais e desorganizados por uma solução estruturada e automatizada — algo que é uma dor comum nesse tipo de cenário .

🚀 Funcionalidades (até a Sprint atual)

🔐 Autenticação de Organizadores
Cadastro de organizador
Login com autenticação JWT
Recuperação de senha (simulada)
Edição de perfil

👥 Gestão de Jogadores
Cadastro de jogadores
Definição de nível de habilidade (0.5 a 5 estrelas)
Edição de dados
Desativação de jogadores (soft delete)
Listagem de jogadores por organizador

🛠️ Tecnologias Utilizadas
Backend
Node.js
Express
Prisma ORM
PostgreSQL / SQLite
JWT (autenticação)
Bcrypt (hash de senha)
Ferramentas
Git e GitHub
Postman / Insomnia

📁 Estrutura do Projeto
src/
 ├── controllers/
 ├── routes/
 ├── middlewares/
 ├── services/
 ├── prisma/
 └── app.js
 
⚙️ Como rodar o projeto
1. Clonar o repositório
git clone https://github.com/Gabriel0879/Sistema-de-Gest-o-de-Futebol-Amador.git
2. Entrar na pasta
cd Sistema-de-Gest-o-de-Futebol-Amador
3. Instalar dependências
npm install
4. Configurar variáveis de ambiente

Crie um arquivo .env:

DATABASE_URL="sua_url_do_banco"
JWT_SECRET="sua_chave_secreta"
5. Rodar o banco (Prisma)
npx prisma migrate dev
6. Iniciar o servidor
npm run dev

🔐 Rotas da API

Auth
POST /auth/register → Cadastro
POST /auth/login → Login
GET /auth/me → Dados do usuário logado
Jogadores
GET /jogadores → Listar jogadores
POST /jogadores → Criar jogador
PUT /jogadores/:id → Editar jogador
DELETE /jogadores/:id → Desativar jogador

📌 Regras de Negócio

Cada organizador só pode acessar seus próprios dados
Jogadores não são deletados, apenas desativados
Nível de habilidade varia de 0.5 a 5.0
Rotas protegidas por autenticação JWT
📊 Status do Projeto

🚧 Em desenvolvimento — Sprint 3 concluída

Próximas etapas:

Criação de peladas
Lista de inscritos
Sorteio de times
👨‍💻 Autor

Desenvolvido por Gabriel Santos

💡 Dica importante

Se quiser deixar ainda mais profissional, você pode depois adicionar:

📸 Prints do sistema (quando tiver frontend)
📄 Licença (MIT, por exemplo)
✅ Checklist de sprints
