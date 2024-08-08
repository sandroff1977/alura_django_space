### CTR+L limpa o terminal

### CTR+SHIFT+P abre a pesquisa no topo do vs code
## escrever
python select interpreter
## verificar para utilizar o versao python da venv

#### 01

### Estabeleça um ambiente virtual dentro do diretório do projeto
## Linux/MacOS:
virtualenv -p python3 venv
## Windows:
python -m virtualenv venv

### Ative o ambiente virtual
## Linux/MacOS:
source venv/bin/activate
## Windows:
venv/Scripts/activate

### Desativar a venv
deactivate

### Instale o Django
pip install django

### Visualizar todas as dependencias do projeto
pip freeze

### Criar arquivo com as dependencias do prejeto
pip freeze > requirements.txt

### Visualizar os comandos inseridos no Django
django-admin help


### Crie o projeto Django
django-admin startproject setup .

### Rode o servidor pela primeira vez
python manage.py runserver

#### 02

### Idioma e timezone
## Alterar idioma e time zone
# Setup > settings.py

# Internationalization
# https://docs.djangoproject.com/en/5.1/topics/i18n/

# LANGUAGE_CODE = 'en-us'
LANGUAGE_CODE = 'pt-br'

TIME_ZONE = 'America/Sao_Paulo'

USE_I18N = True

USE_TZ = True



### Variáveis de ambiente
## 

### 1) Crie um novo arquivo chamado .env no diretório raiz da aplicação para armazenar a SECRET_KEY
## Conteúdo do arquivo .env:
SECRET_KEY=<chave aleatória>

### 2) Instale o pacote python-dotenv
pip install python-dotenv

### 3) Importe os pacotes python-dotenv e os no arquivo settings.py
from pathlib import os
from dotenv import load_dotenv


### 4) Importe a SECRET_KEY do arquivo .env e coloque dentro da variável SECRET_KEY no arquivo settings.py
load_dotenv()
SECRET_KEY = str(os.getenv('SECRET_KEY'))


### 5) Gere um arquivo .gitignore no diretório raiz do projeto e inclua o arquivo .env como conteúdo
## Conteúdo do .gitignore:
## pesquisar arquivos comuns para incluir no gitignore "https://www.toptal.com/developers/gitignore"
# copiar e colar a relação de arquivos
# no prompt iniciar repositorio local: 
git init
# copiar os arquivos do projeto
git add .