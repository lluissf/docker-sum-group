# Documentação do Projeto.
## Utilizando o Docker 🦈
**⚠️ É muito importante você lembrar que precisa listar todas as bibliotecas utilizadas no Projeto, e também lembrar de criar e ativar o ambiente virtual.**
```md
# Criando o ambiente virtual 
python -m venv .venv
# Ativando o ambiente virtual
source .venv/bin/activate # Linux
.\.venv\Scripts\Activate # Windows 
# Listando os pacotes instalados.
pip freeze > requirements.txt 
```

**Executando a build**.
```md
# Build da imagem Single Stage
docker build -t <nome-do-usuario-docker>/soma-api:single -f Dockerfile.single .
# Build da imagem Multi Stage (Otimizada)
docker build -t <nome-do-usuario-docker>/soma-api:multi -f Dockerfile .
# Verificando se as imagens foram criadas
docker images | grep soma-api # Linux
docker images | findstr soma-api # Windows
```
**Criando e iniciando o container**.
```md
# Criando no modo single stage
docker run -d -p 8000:8000 --name api-teste <nome-do-usuario-docker>/soma-api:single
# Criando no modo multi stage
docker run -d -p 8000:8000 --name api-teste <nome-do-usuario-docker>/soma-api:multi
```

