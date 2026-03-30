# Documentação do Projeto.
## Utilizando o Docker 🦈

**Executando a build**.
```md
# Build da imagem Single Stage
docker build -t <nome-do-usuario-docker>/soma-api:single -f Dockerfile.single .
# Build da imagem Multi Stage (Otimizada)
docker build -t <nome-do-usuario-docker>/soma-api:multi -f Dockerfile .
# Verificando se as imagens foram criadas
docker images | grep soma-api
```
**Criando e iniciando o container**.
```md
# Criando no modo single stage
docker run -d -p 8000:8000 --name api-teste <nome-do-usuario-docker>/soma-api:single
# Criando no modo multi stage
docker run -d -p 8000:8000 --name api-teste <nome-do-usuario-docker>/soma-api:multi
```

