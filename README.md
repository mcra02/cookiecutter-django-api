<p align="center">
    <img src="https://dashboard.snapcraft.io/site_media/appmedia/2020/04/cookiecutter-logo-square-512.png" width="120" alt="Cookiecutter" />
    <img src="https://cdn.iconscout.com/icon/free/png-512/django-2-282855.png" width="120" alt="Django" />
    </p>


<h1 align="center">
  Django Api Cookiecutter
</h1>

Powered by [Maicol](https://github.com/mcra02) with the goal of optimize our development processes, we are happy to introduce our Django projects boilerplate packed and ready to use with the following features:

- **Python** 3.8
- **Django** 3.0.6
- **Django REST Framework** 3.11.0
- [**12 Factor**](https://12factor.net/) based settings
- **PostgreSQL** as database engine
- **Docker** as container engine
- Run tests with unittest or pytest
- **django-allauth** 0.41.0

## Installation

1. First, get [Cookiecutter](https://github.com/audreyr/cookiecutter). Trust me, it's awesome:

    ```bash
    $ pip install cookiecutter
    ```

2. Run against this repo

    ```bash
    $ cookiecutter https://github.com/mcra02/cookiecutter-django-api.git
    ```

    You'll be prompted for some values. Provide them, then a Django project will be created for you.

3. Enter the project and take a look around:

    ```bash
    $ cd project/
    $ ls
    ``` 

## Development

1. Migration generated
    ```bash
    $ python manage.py makemigrations
    ```

2. Migration database
    ```bash
    $ python manage.py migrate
    ```

2. Run development
    ```bash
    $ python manage.py runserver 0.0.0.0:8000
    ```

## Production

1. Build dockerfile
    ```bash
    $ docker build -t "project_name" .
    ```

2. Migration database
    ```bash
    $ docker run -itd --name backend-osffni -p 3000:8000 project_name
    ```


## Contributing

Please fill free to submit pull requests as well as open issues.
