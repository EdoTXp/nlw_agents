# NLW Agents

Projeto desenvolvido durante o evento **Next Level Week (NLW)** da Rocketseat.

## 🚀 Tecnologias e Padrões

Este projeto foi construído com uma stack moderna, focada em performance, escalabilidade e boas práticas de desenvolvimento.

- **Node.js**: Ambiente de execução JavaScript no servidor.
  - **Strip Types (Experimental)**: Utiliza o recurso nativo do Node.js para remover anotações de tipo do TypeScript em tempo de execução, otimizando a performance.
- **Fastify**: Framework web de alta performance e baixo overhead, escolhido por sua velocidade e ecossistema de plugins.
- **PostgreSQL** com **pgvector**: Banco de dados relacional robusto, utilizando a extensão `pgvector` para operações eficientes com vetores.
- **Drizzle ORM**: ORM type-safe que garante a segurança de tipos nas operações com o banco de dados.
- **Zod**: Biblioteca para declaração e validação de schemas, utilizada tanto para os dados de entrada das rotas quanto para as variáveis de ambiente.
- **Docker**: Utilizado para criar um ambiente de desenvolvimento padronizado e isolado para o banco de dados.
- **Biome**: Ferramenta unificada de alta performance para linting e formatação de código.

A arquitetura do projeto segue princípios de **separação de responsabilidades**, com uma estrutura modular que divide a aplicação em rotas, schemas e lógica de banco de dados.

## ⚙️ Setup e Configuração

Siga os passos abaixo para configurar e executar o projeto em seu ambiente local.

### Pré-requisitos

- Node.js (versão 20 ou superior, com suporte a `--experimental-strip-types`)
- Docker e Docker Compose

### Instalação

1.  **Clone o repositório**

    ```bash
    git clone <url-do-repositorio>
    cd server
    ```

2.  **Configure as Variáveis de Ambiente**
    Crie um arquivo `.env` na raiz do diretório `server` e adicione as seguintes variáveis:

    ```env
    PORT=3333
    DATABASE_URL=postgresql://docker:docker@localhost:5432/agents
    ```

3.  **Inicie o Banco de Dados**
    Use o Docker Compose para iniciar o container do PostgreSQL:

    ```bash
    docker-compose up -d
    ```

4.  **Instale as Dependências**

    ```bash
    npm install
    ```

5.  **Execute as Migrações**
    Aplique as migrações do Drizzle para criar a estrutura do banco de dados:
    ```bash
    npx drizzle-kit migrate
    ```

## ▶️ Executando o Projeto

Com o ambiente configurado, você pode executar o servidor de diferentes formas:

- **Modo de Desenvolvimento** (com hot-reload):

  ```bash
  npm run dev
  ```

- **Modo de Produção**:

  ```bash
  npm start
  ```

- **(Opcional) Popular o Banco de Dados**:
  Para popular o banco com dados de exemplo, execute:
  ```bash
  npm run db:seed
  ```

A API estará disponível em `http://localhost:3333`.

## ✨ Qualidade de Código

Utilizamos o **Biome** para manter a consistência e a qualidade do código. Para formatar e verificar seu código, execute os seguintes comandos na raiz do projeto:

```bash
# Formatar todos os arquivos
npx @biomejs/biome format --write .

# Executar o linter e aplicar correções seguras
npx @biomejs/biome lint --apply .
```

Desenvolvido com ❤️ durante o NLW da Rocketseat
