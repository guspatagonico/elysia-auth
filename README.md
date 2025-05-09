# Elysia with Bun runtime

ElysiaJS JWT Authentication with Refresh Token Rotation and Reuse Detection.

Inspirations:

- [Dicoding's "Belajar Fundamental Aplikasi Back-End"](https://github.com/dicodingacademy/a271-backend-menengah-labs) (files, folders, and code structure)
- [Dave Gray's "Node JS Tutorial Series - Refresh Token Rotation and Reuse Detection"](https://github.com/gitdagray/refresh_token_rotation) (refresh token rotation and reuse detection mechanism)
- [cholasimmons's 'Modular Elysia JS app | Authentication template (Bun runtime)'](https://github.com/cholasimmons/bun-elysia-modular_auth) (cron usage for cleaning expired tokens)

## Prerequisites

- [Git](https://git-scm.com/downloads)
- [Bun](https://bun.sh/)
- [Docker (optional)](https://www.docker.com/products/docker-desktop/)

## Getting Started

### Non-Docker

Clone the repository:

```bash
git clone https://github.com/guspatagonico/elysia-auth.git
```

Navigate to the project directory:

```bash
cd elysia-auth
```

Create a `.env` file and configure it:

```bash
cp .env.example .env
```

Install the dependencies:

```bash
bun install
```

I added `bun compile` to package.json to create the binary version (not cross-platform, compile must be run on Linux or MacOS independently).

With the binary you can also use pm2 as process manager, for example with:

```bash
pm2 start elysia-auth-server --watch /your_path/elysia-auth/elysia-auth-server
```

### Docker

Clone the repository:

```bash
git clone https://github.com/guspatagonico/elysia-auth.git
```

Navigate to the project directory:

```bash
cd elysia-auth
```

Start the docker compose:

```bash
docker compose up -d
```

## Development

To start the development server run (not needed with Docker):

```bash
bun run dev
```

Open http://localhost:3210/docs with your browser to see the available APIs (thanks to **swagger**).
