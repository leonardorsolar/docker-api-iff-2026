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
# Docker Build

O comando abaixo é usado para criar uma imagem Docker a partir de um **Dockerfile**:

```bash
docker build -t minha-api .
```

## Explicação dos parâmetros

- **`docker`**: chama o Docker.
- **`build`**: informa ao Docker que ele deve construir (**build**) uma imagem.
- **`-t`**: significa **tag**, ou seja, define o nome da imagem.
- **`minha-api`**: é o nome que será dado à imagem criada.
- **`.` (ponto)**: representa o **contexto da construção**.

O ponto (`.`) significa:

> **"Utilize a pasta atual como contexto e procure nela o arquivo `Dockerfile`."**

### Executar o container

```bash
docker run -d -p 3000:3000 --name api-node minha-api
```

> A opção `-d` significa **detached**, ou seja, executa os contêineres em segundo plano.
Se você não usar a opção -d, os contêineres serão executados em primeiro plano (foreground). Isso significa que o terminal ficará exibindo os logs em tempo real e permanecerá ocupado enquanto os contêineres estiverem em execução.

### Parar e remover o container

```bash
docker stop api-node
docker rm api-node
```

### Testar

Abra no navegador: http://localhost:3000

A resposta deve ser: **API Node.js rodando no Docker!**
