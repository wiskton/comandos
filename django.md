# Django

Meu helper de comandos do django

## Principais comandos

### Criar um projeto django

1. Instalar o Django
```python
pip install django
```

2. Criar um novo projeto
```python
django startproject <nome-projeto>
```

Gerar o banco do projeto
```python
python manage.py syncdb
```

Rodar o projeto
```python
python manage.py runserver
```

### Criar um novo app no seu projeto

1. Criar um novo app
```python
python manage.py startapp <nome-app>
```

2. Lembrar de adicionar ao **INSTALLED_APPS**
```python
INSTALLED_APPS = (....
  '<nome_app>',
)
```

Gerar arquivos estáticos [imgs,js,css]
```python
python manage.py collectionstatic
```

Testar sql no terminal
```python
python manage.py dbshell
```

## Instalar um pacote

Instalar um pacote com pip exemplo django e uma versão específica
```python
pip install django=1.3.1
```

Lembrar de adicionar ao **INSTALLED_APPS**
```python
INSTALLED_APPS = (....
  '<nome_app>',
)
```

## Banco de dados

Criar um usuário admin no django
```python
python manage.py createsuperuser
```

Criar uma nova migração de dados do banco em um app específico
```python
python manage.py makemigrations <nome_app>
```

Criar a migração e executa no banco de dados para um app específico

```python
python manage.py makemigrations <nome_app>
python manage.py migrate <nome_app>
```

Criar todas as tabelas e modificações nas migrações do django

```python
python manage.py migrate
```
Criar um fixture de um app específico

```python
python manage.py dumpdata nome-app > nome_app/fixtures/initial_data.json
```

Listar todas as dependências instaladas do projeto

```python
pip freeze
```

Criar um requirements a partir das libs da env

```python
pip freeze > requirements.txt
```
