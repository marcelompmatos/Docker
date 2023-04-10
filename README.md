# Docker com Google Cloud 

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

⚡ MultiCloud com DevOps 
## 🛠 Provisionar Bucket no S3 AWS - Executando o arquivo main.tf


```bash
  terraform init
  terraform plan
  terraform apply
```


