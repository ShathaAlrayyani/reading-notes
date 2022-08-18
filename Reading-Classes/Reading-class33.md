## Making Database Changes Without SQL

Without migrations, you would have to connect to your database and type in a bunch of SQL commands or use a graphical
tool like PHPMyAdmin to modify the database schema every time you wanted to change your model definition.

In Django, migrations are primarily written in Python, so you don’t have to know any SQL unless you have really advanced
use cases.

## Setting Up a Django Project

Throughout this tutorial, you are going to work on a simple Bitcoin tracker app as an example project.

The first step is to install Django. Here is how you do that on Linux or mac OS X using a virtual environment:

    $ python3 -m venv env
    $ source env/bin/activate
    (env) $ pip install "Django==2.1.*"
    ...
    Successfully installed Django-2.1.3

With Django installed, you can create the project using the following commands:

    $ django-admin.py startproject bitcoin_tracker
    $ cd bitcoin_tracker
    $ python manage.py startapp historical_data

to create a model, add this class in historical_data/models.py:

    class PriceHistory(models.Model):
        date = models.DateTimeField(auto_now_add=True)
        price = models.DecimalField(max_digits=7, decimal_places=2)
        volume = models.PositiveIntegerField()

add the newly created app to settings.INSTALLED_APPS. Open bitcoin_tracker/settings.py and append historical_data to the
list INSTALLED_APPS, like this:

    INSTALLED_APPS = [
        'django.contrib.admin',
        'django.contrib.auth',
        'django.contrib.contenttypes',
        'django.contrib.sessions',
        'django.contrib.messages',
        'django.contrib.staticfiles',
        'historical_data',
    ]

