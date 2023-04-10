# Docker com Google Cloud 

Passos

Baixar o .zip https://github.com/marcelompmatos/Docker.git
Crie o arquivo Dockerfile👋
```bash
    FROM python:3

    COPY ./requirements.txt /app/requirements.txt

    WORKDIR /app

    RUN pip install --no-cache-dir -r requirements.txt

    COPY . /app

    ENTRYPOINT [ "python" ]

    CMD [ "app.py" ]
```

Zip e Upload app.zip para o Cloud Shell 👋
Unzip app.zip 👋
Crie (Build) a Docker image 👋

⚡ MultiCloud com DevOps 
## 🛠 Provisionar Bucket no S3 AWS - Executando o arquivo main.tf


```bash
  terraform init
  terraform plan
  terraform apply
```


