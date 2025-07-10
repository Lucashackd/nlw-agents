# NLW Agents - Server

Este é o backend do projeto **NLW Agents**, desenvolvido durante a edição NLW Agents da [Rocketseat](https://rocketseat.com.br). A aplicação consiste em um servidor Node.js que gerencia salas e utiliza inteligência artificial para interações.

## ✨ Tecnologias Utilizadas

O projeto foi construído com um conjunto de tecnologias modernas para garantir performance, escalabilidade e qualidade de código.

- **[Node.js](https://nodejs.org/)**: Ambiente de execução JavaScript no servidor.
- **[TypeScript](https://www.typescriptlang.org/)**: Superset do JavaScript que adiciona tipagem estática.
- **[Fastify](https://www.fastify.io/)**: Framework web focado em performance e baixo overhead.
- **[PostgreSQL](https://www.postgresql.org/)**: Banco de dados relacional robusto e de código aberto.
- **[pgvector](https://github.com/pgvector/pgvector)**: Extensão para PostgreSQL que permite o armazenamento e busca de vetores, essencial para aplicações de IA.
- **[Drizzle ORM](https://orm.drizzle.team/)**: ORM TypeScript-first que oferece segurança de tipos e uma experiência de desenvolvimento superior.
- **[Biome](https://biomejs.dev/)**: Ferramenta integrada para formatação e linting de código, garantindo consistência e qualidade.
- **[Docker](https://www.docker.com/)**: Plataforma para desenvolvimento, deploy e execução de aplicações em contêineres.

## 🚀 Setup e Configuração

Siga os passos abaixo para configurar e executar o projeto em seu ambiente de desenvolvimento.

### Pré-requisitos

- **Node.js** (versão 20.x ou superior)
- **Docker** e **Docker Compose**

### Passos

1.  **Clone o repositório:**

    ```bash
    git clone https://github.com/Lucashackd/nlw-agents.git
    cd nlw-agents/server
    ```

2.  **Instale as dependências:**

    ```bash
    npm install
    ```

3.  **Configure as variáveis de ambiente:**

    - Copie o arquivo de exemplo `.env.example` para um novo arquivo chamado `.env`.
      ```bash
      cp .env.example .env
      ```
    - As variáveis padrão já estão configuradas para o ambiente Docker local, mas você pode alterá-las se necessário.

4.  **Inicie o banco de dados:**

    - Utilize o Docker Compose para iniciar o contêiner do PostgreSQL com a extensão `pgvector`.
      ```bash
      docker-compose up -d
      ```

5.  **Execute as migrações do banco de dados:**

    - O Drizzle Kit gerencia as migrações. Para aplicar o schema ao banco, execute:
      ```bash
      npx drizzle-kit migrate
      ```

6.  **Inicie o servidor:**
    - Para iniciar o servidor em modo de desenvolvimento, execute:
      ```bash
      npm run dev
      ```
    - O servidor estará disponível em `http://localhost:3333` por padrão.

## 📝 API

O projeto inclui um arquivo `client.http` que pode ser usado para testar os endpoints da API. Você pode utilizar a extensão REST Client para o VS Code para fazer requisições diretamente do seu editor.

### Endpoints Disponíveis:

- `GET /health`: Verifica o status da aplicação.
- `GET /rooms`: Lista as salas disponíveis.

---

Desenvolvido com ❤️ durante o NLW Agents.
