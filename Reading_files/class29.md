## Django Custom User

- Django ships with a built-in User model for authentication and if you'd like a basic tutorial on how to implement log in, log out, sign up and so on see the Django Login and Logout tutorial for more.

However, for a real-world project, the official Django documentation highly recommends using a custom user model instead. This provides far more flexibility down the line so, as a general rule, always use a custom user model for all new Django projects.

- There are two modern ways to create a custom user model in Django: AbstractUser and AbstractBaseUser. In both cases we can subclass them to extend existing functionality however AbstractBaseUser requires much, much more work. Seriously, don't mess with it unless you really know what you're doing. 

- Creating our initial custom user model requires four steps:

    - update config/settings.py
    - create a new CustomUser model
    - create new UserCreation and UserChangeForm
    - update the admin

- In settings.py we'll add the accounts app and use the AUTH_USER_MODEL config to tell Django to use our new custom user model in place of the built-in User model. We'll call our custom user model CustomUser.

- Within INSTALLED_APPS add accounts at the bottom. Then at the bottom of the entire file, add the AUTH_USER_MODEL config.

- It's helpful to create a superuser that we can use to log in to the admin and test out log in/log out. On the command line type the following command and go through the prompts.

- Now that our custom user model is configured you can easily and at any time add additional fields to it. See the Django docs for further instructions.

- You can also check out DjangoX, which is an open-source Django starter framework that includes a custom user model, email/password by default instead of username/email/password, social authentication, and more.






[<===BACK](../README.md)
