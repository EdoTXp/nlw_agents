# NLW Agents

Projeto desenvolvido durante a Next Level Week (NLW) Agents, um evento online e gratuito promovido pela [Rocketseat](https://www.rocketseat.com.br/).

## ✨ Tecnologias

Este projeto foi desenvolvido utilizando as seguintes tecnologias e bibliotecas:

- **React 19.1** - Biblioteca para interfaces de usuário
- **TypeScript 5.8** - Superset JavaScript com tipagem estática
- **Vite 7.0** - Build tool e servidor de desenvolvimento
- **TailwindCSS 4.1** - Framework CSS utility-first
- **React Router Dom 7.6** - Biblioteca de roteamento
- **TanStack React Query 5.8** - Gerenciamento de estado servidor e cache
- **Radix UI** - Componentes primitivos acessíveis
- **Shadcn/ui** - Sistema de componentes
- **Lucide React** - Biblioteca de ícones

## 📂 Padrões de Projeto

- **Component-based Architecture** - Arquitetura baseada em componentes React
- **File-based Routing** - Roteamento baseado em arquivos com React Router
- **Server State Management** - Gerenciamento de estado servidor com React Query
- **Variant-based Components** - Componentes com variantes usando CVA
- **Composition Pattern** - Padrão de composição com Radix Slot
- **Path Aliasing** - Alias de caminhos (`@/` aponta para `src/`)

## ⚙️ Setup e Configuração

Para executar este projeto localmente, siga os passos abaixo:

### Pré-requisitos

- [Node.js](https://nodejs.org/en/) (versão 20.x ou superior)
- [npm](https://www.npmjs.com/) ou [yarn](https://yarnpkg.com/)

### Instalação

1.  Clone o repositório para a sua máquina local:

    ```bash
    git clone <URL_DO_REPOSITORIO>
    cd <NOME_DA_PASTA_DO_PROJETO>
    ```

2.  Instale as dependências do projeto:
    ```bash
    npm install
    ```

### Executando a Aplicação

1.  Execute o servidor de desenvolvimento:
    ```bash
    npm run dev
    ```
2.  Acesse a aplicação em `http://localhost:5173`

### Backend

O projeto consome uma API que deve estar rodando na porta `3333`. Certifique-se de que o backend esteja configurado e executando antes de iniciar o frontend.

## 🛠️ Scripts Disponíveis

- `npm run dev` - Inicia o servidor de desenvolvimento
- `npm run build` - Gera build de produção
- `npm run preview` - Preview do build de produção

## 📁 Estrutura do Projeto

```
src/
├── components/ui/    # Componentes de interface (Shadcn/ui)
├── pages/           # Páginas da aplicação (Roteamento)
├── lib/             # Utilitários, configs e helpers (ex: axios, react-query)
└── app.tsx          # Componente raiz da aplicação
```
