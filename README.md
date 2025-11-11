# API REST de Usuarios

API REST completa para gerenciamento de usuarios, desenvolvida com Node.js, Express e MongoDB.

## Caracteristicas

- Autenticacao com JWT
- Gerenciamento completo de usuarios (CRUD)
- Validacao de entrada com Joi
- Hash seguro de senhas com bcrypt
- Tratamento de erros robusto
- Modulos bem estruturados
- Documentacao com Swagger

## Stack Tecnologico

- **Node.js** - Runtime JavaScript
- **Express** - Framework web
- **MongoDB** - Banco de dados NoSQL
- **Mongoose** - ODM para MongoDB
- **JWT** - Autenticacao
- **bcrypt** - Hashing de senhas
- **Joi** - Validacao de schema

## Como Rodar Localmente

### Pre-requisitos

- Node.js (v14+)
- npm ou yarn
- MongoDB

### Passos

1. Clone o repositorio:
```bash
git clone https://github.com/nilotj/api-usuarios-nodejs.git
cd api-usuarios-nodejs
```

2. Instale as dependencias:
```bash
npm install
```

3. Configure as variaveis de ambiente:
```bash
cp .env.example .env
```

4. Inicie a API:
```bash
npm start
# ou em modo desenvolvimento
npm run dev
```

## Endpoints Disponiveis

### Autenticacao

```
POST /api/auth/register       - Registrar novo usuario
POST /api/auth/login          - Login de usuario
```

### Usuarios

```
GET    /api/users             - Listar todos os usuarios
GET    /api/users/:id         - Obter usuario por ID
POST   /api/users             - Criar novo usuario
PUT    /api/users/:id         - Atualizar usuario
DELETE /api/users/:id         - Deletar usuario
```

## Estrutura do Projeto

```
api-usuarios-nodejs/
├── src/
│   ├── models/
│   │   └── User.js           # Schema do Mongoose
│   ├── routes/
│   │   ├── auth.js           # Rotas de autenticacao
│   │   └── users.js          # Rotas de usuarios
│   ├── controllers/
│   │   ├── authController.js
│   │   └── userController.js
│   ├── middleware/
│   │   ├── auth.js           # Middleware de autenticacao
│   │   └── errorHandler.js   # Tratamento de erros
│   └── app.js                # Configuracao da aplicacao
├── .env.example              # Variaveis de ambiente
├── package.json              # Dependencias
└── README.md                 # Este arquivo
```

## Variaveis de Ambiente

```
PORT=3000
MONGODB_URI=mongodb://localhost:27017/usuarios
JWT_SECRET=sua_chave_secreta_super_segura
NODE_ENV=development
```

## Licenca

Este projeto eh de codigo aberto sob a licenca MIT.

## Contribuindo

Contribuicoes sao bem-vindas! Por favor:

1. Fork o projeto
2. Crie uma branch para sua feature
3. Commit suas mudancas
4. Push para a branch
5. Abra um Pull Request

---

**Se este projeto foi util, considere dar uma star!**
