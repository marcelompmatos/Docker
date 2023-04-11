# Docker

## :computer: Exemplo de Docker com Google Cloud 

Passos

1. Baixar o .zip https://github.com/marcelompmatos/Docker.git
2. Crie o arquivo Dockerfile👋
```bash
    FROM python:3

    COPY ./requirements.txt /app/requirements.txt

    WORKDIR /app

    RUN pip install --no-cache-dir -r requirements.txt

    COPY . /app

    ENTRYPOINT [ "python" ]

    CMD [ "app.py" ]
```

3. Zip e Upload app.zip para o Cloud Shell 👋
4. Unzip app.zip 👋
5. Crie (Build) a Docker image 👋

```bash
    docker build -t app:1.0 .
    docker image ls
```

5. Teste a imagem localmente no Cloud Shell👋

```bash
    docker container run --name app -p 5000:5000 app:1.0
    docker container ls 
    docker container ls --all
    docker container start app
    docker container stop app
```

6. Adicione tag a imagem👋

```bash
    docker tag app:1.0 us.gcr.io/<ID_PROJETO>/app
```

7. Suba (Push) a imagem para Container Registry na Google Cloud👋

```bash
    docker push us.gcr.io/<ID_PROJETO>/app
```

## 🛠 8. Faça o deploy da aplicação em container no Google Cloud Run usando a imagem criada👋
