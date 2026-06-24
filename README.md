# Docker API IFF

API simples em Node.js com Express para demonstração de Docker.

## Executar localmente

```bash
npm install
npm start
```

Acessar: http://localhost:3000

## Docker

### Construir a imagem

```bash
docker build -t minha-api .
```

### Executar o container

```bash
docker run -d -p 3000:3000 --name api-node minha-api
```

### Parar e remover o container

```bash
docker stop api-node
docker rm api-node
```

### Testar

Abra no navegador: http://localhost:3000

A resposta deve ser: **API Node.js rodando no Docker!**
