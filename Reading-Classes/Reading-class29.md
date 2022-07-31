## AbstractUser vs AbstractBaseUser

There are two modern ways to create a custom user model in Django: AbstractUser and AbstractBaseUser. In both cases we
can subclass them to extend existing functionality however AbstractBaseUser requires much, much more work. Seriously,
don't mess with it unless you really know what you're doing. And if you did, you wouldn't be reading this tutorial,
would you?

So we'll use AbstractUser which actually subclasses AbstractBaseUser but provides more default configuration.

## Custom User Model

Creating our initial custom user model requires four steps:

- update django_project/settings.py
- create a new CustomUser model
- create new UserCreation and UserChangeForm
- update the admin

In settings.py we'll add the accounts app and use the AUTH_USER_MODEL config to tell Django to use our new custom user
model in place of the built-in User model. We'll call our custom user model CustomUser.

Within INSTALLED_APPS add accounts at the bottom. Then at the bottom of the entire file, add the AUTH_USER_MODEL config.

        # django_project/settings.py
        INSTALLED_APPS = [
            "django.contrib.admin",
            "django.contrib.auth",
            "django.contrib.contenttypes",
            "django.contrib.sessions",
            "django.contrib.messages",
            "django.contrib.staticfiles",
            "accounts",  # new
        ]

        ...
        AUTH_USER_MODEL = "accounts.CustomUser"  # new

Now update accounts/models.py with a new User model which we'll call CustomUser.

    # accounts/models.py
    from django.contrib.auth.models import AbstractUser
    from django.db import models
    
    class CustomUser(AbstractUser):
        pass
        # add additional fields in here

    def __str__(self):
        return self.username

We need new versions of two form methods that receive heavy use working with users. Stop the local server with Control+c
and create a new file in the accounts app called forms.py.

        (accounts) $ touch accounts/forms.py

We'll update it with the following code to largely subclass the existing forms.

        # accounts/forms.py
        from django import forms
        from django.contrib.auth.forms import UserCreationForm, UserChangeForm
        
        from .models import CustomUser
        
        class CustomUserCreationForm(UserCreationForm):
        
            class Meta:
                model = CustomUser
                fields = ("username", "email")
        
        class CustomUserChangeForm(UserChangeForm):
        
            class Meta:
                model = CustomUser
                fields = ("username", "email")

Finally we update admin.py since the Admin is highly coupled to the default User model.

        # accounts/admin.py
        from django.contrib import admin
        from django.contrib.auth.admin import UserAdmin
        
        from .forms import CustomUserCreationForm, CustomUserChangeForm
        from .models import CustomUser
        
        class CustomUserAdmin(UserAdmin):
            add_form = CustomUserCreationForm
            form = CustomUserChangeForm
            model = CustomUser
            list_display = ["email", "username",]

        admin.site.register(CustomUser, CustomUserAdmin)

And we're done! We can now run makemigrations and migrate for the first time to create a new database that uses the
custom user model.

        (.venv) > python manage.py makemigrations accounts
        (.venv) > python manage.py migrate

## Superuser

It's helpful to create a superuser that we can use to log in to the admin and test out log in/log out. On the command
line type the following command and go through the prompts.

        (.venv) > python manage.py createsuperuser

