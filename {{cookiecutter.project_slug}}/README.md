<p align="center">
    <img src="https://cdn.iconscout.com/icon/free/png-512/django-2-282855.png" width="120" alt="Django" />
    </p>


<h1 align="center">
  {{cookiecutter.project_name}}
</h1>

## Description

<p ALIGN="justify">
{{cookiecutter.description}}
</p>

This project has using the following features:

- **Python** 3.8
- **Django** 3.0.6
- **Django REST Framework** 3.11.0
- [**12 Factor**](https://12factor.net/) based settings
- **PostgreSQL** as database engine
- **Docker** as container engine
- Run tests with unittest or pytest
- **django-allauth** 0.41.0

## Installation

### Development

1. Clone Repository

   ```bash
   $ git clone {{cookiecutter.git_repository}}
   ```

2. Check the .env/.postgres file and change the credentials of the connection url to postgresql if necessary (**postgresql://USER:PASSWORD@HOST:PORT/DATABASE**).

   You should create a database named **{{cookiecutter.db_name}}**.

3. Install dependencies

   ```bash
   $ virtualenv -p python3 venv
   ```

4. Install dependencies

   ```bash
   $ pip install -r requeriments/local.txt
   ```

5. Run save migrations

   ```bash
   $ python manage.py makemigrations
   ```

6. Run up migrations

   ```bash
   $ python manage.py migrate
   ```

7. Run service (dev)

   ```bash
   $ python manage.py runserver 0.0.0.0:8000
   ```

8. Open http://localhost:8000/

### Production

1. Clone Repository

   ```bash
   $ git clone {{cookiecutter.git_repository}}
   ```

2. Check the .env/.postgres file and change the credentials of the connection url to postgresql if necessary (**postgresql://USER:PASSWORD@HOST:PORT/DATABASE**).

   You should create a database named **{{cookiecutter.db_name}}**.

3. Build Dockerfile

   ```bash
   $ docker build -t "{{cookiecutter.project_slug}}" .
   ```

3. Start project

   ```bash
   $ docker run -itd --name {{cookiecutter.project_slug}} -p 3000:8000 {{cookiecutter.project_slug}}
   ```
4. Open http://localhost:3000/

# Authors

#### {{cookiecutter.author_name}}
