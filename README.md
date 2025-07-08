# NLW Agents

Projeto full-stack desenvolvido durante a **Next Level Week (NLW) Agents**, um evento online e gratuito promovido pela [Rocketseat](https://www.rocketseat.com.br/).

## 📖 Sobre o Projeto

O NLW Agents é uma aplicação completa que consiste em um backend robusto e um frontend web moderno. O projeto foi estruturado como um monorepo, contendo duas pastas principais: `server` e `web`.

- **Backend (`/server`)**: Uma API de alta performance construída com Node.js e Fastify. Utiliza PostgreSQL com a extensão `pgvector` para operações eficientes com vetores, Drizzle ORM para segurança de tipos no acesso ao banco de dados, e Zod para validação de schemas. O ambiente de desenvolvimento é padronizado com Docker.

- **Frontend (`/web`)**: Uma interface de usuário reativa construída com React e Vite. Para o design, utiliza TailwindCSS e um sistema de componentes baseado em Shadcn/ui e Radix UI. O gerenciamento de estado do servidor é feito com TanStack React Query, e o roteamento é baseado em arquivos com React Router.

## ✨ Tecnologias Utilizadas

### Backend (server/)

- **Node.js** com `strip-types` experimental
- **Fastify**
- **PostgreSQL** com **pgvector**
- **Drizzle ORM**
- **Zod**
- **Docker**
- **Biome** (Linter e Formatador)

### Frontend (web/)

- **React**
- **TypeScript**
- **Vite**
- **TailwindCSS**
- **React Router Dom**
- **TanStack React Query**
- **Radix UI** & **Shadcn/ui**
- **Lucide React** (Ícones)

## 🚀 Como Executar o Projeto

Para executar este projeto, você precisará ter Node.js (versão 20.x ou superior) e Docker instalados.

1.  Clone o repositório:

    ```bash
    git clone <URL_DO_REPOSITORIO>
    cd <NOME_DA_PASTA_DO_PROJETO>
    ```

2.  Configure e execute o **Backend**:

    ```bash
    # Navegue para a pasta do servidor
    cd server

    # Crie o arquivo .env e preencha as variáveis de ambiente
    # (você pode copiar o conteúdo de server/README.md)

    # Inicie o container do banco de dados com Docker
    docker-compose up -d

    # Instale as dependências
    npm install

    # Execute as migrações do banco de dados
    npx drizzle-kit migrate

    # Inicie o servidor de desenvolvimento
    npm run dev
    ```

    O backend estará disponível em `http://localhost:3333`.

3.  Configure e execute o **Frontend**:
    Em um **novo terminal**, a partir da raiz do projeto:

    ```bash
    # Navegue para a pasta da web
    cd web

    # Instale as dependências
    npm install

    # Inicie o servidor de desenvolvimento
    npm run dev
    ```

    A aplicação web estará disponível em `http://localhost:5173`.
