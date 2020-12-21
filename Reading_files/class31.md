# Django REST Framework & Docker

## Docker

- With Docker we now longer have to mess around with virtual environments. We can faithfully reproduce a production environment locally. And Docker can be shared among team members so everyone is working on the same setup. Wins all around. The downside is complexity. Docker is a complex beast under the hood.

- Docker is really just Linux containers which are a type of virtualization. Virtualization has its roots at the beginning of computer science when large, expensive mainframe computers were the norm. How could multiple programmers use the same single machine? The answer was virtualization and specifically virtual machines which are complete copies of a computer system from the operating system on up.

- If you rent space on a cloud provider like AWS they are typically not providing you with a dedicated piece of hardware. Instead you are probably sharing a physical server with hundreds or even thousands of other clients. What’s the downside to a virtual machine? Size and speed. A typical guest operating system can easily take up 700MB of size. So if one physical server supports three virtual machines, that’s at least 2.1GB of disk space taken up along with separate needs for CPU and memory resources.

- Most computers rely on the same Linux operating system, so what if we virtualized from that level up instead? Wouldn’t that provide a lightweight, faster way to duplicate much of the same functionality? The answer is yes. And in recent years Linux containers, also known as “containerization,” has become increasingly popular. For most applications, a virtual machine provides far more resources than are needed and a container is more than sufficient. This, fundamentally, is what Docker is. A way to implement Linux containers!

- Virtual environments are used to isolate Python software packages locally. We can create an isolated box for individual projects so one can use Python 2.7 and Django 1.5 while another can use Python 3.5 and Django 2.1 on the same computer. Virtual environments are great. But…virtual environments can only isolate Python packages. They still rely on a global, system-level installation of Python albeit they can refer to the proper version. So when we use Python 2.7 in a project, we’re pointing to an installation of Python 2.7 on the computer itself, not actually within the virtual environment. Also we can’t run a production database or other services within virtual environments so compared to Docker containers they are far more limited.

- Docker is a way to run Linux containers
    1. Containers are a lightweight alternative to Virtual Machines
    2. Dockerfile is a list of instructions for creating an image
    3. Images are made up of one or more layers
    4. Containers are a running instance of an image
    5. docker-compose.yml controls how to run the container
    6. Containers are stateless and ephemeral in nature. We can link the local filesystem via volumes but things become more complex with databases (which we didn’t cover here).


## Django REST API

- Django REST Framework works alongside the Django web framework to create web APIs. We cannot build a web API with only Django Rest Framework; it always must be added to a project after Django itself has been installed and configured.

- First we need a dedicated directory on our computer to store the code. This can live anywhere but for convenience, if you are on a Mac, we can place it in the Desktop folder. The location really does not matter; it just needs to be easily accessible.

- Now we are within the code folder which will be the location for all the code in this book. The next step is to create a dedicated directory for our library site, install Django via Pipenv, and then enter the virtual environment using the shell command. You should always use a dedicated virtual environment for every new Python project.

- Pipenv creates a Pipfile and a Pipfile.lock within our current directory. The (library) in parentheses before the command line shows that our virtual environment is active. A traditional Django website consists of a single project and one (or more) apps representing discrete functionality. Let’s create a new project with the startproject command. Don’t forget to include the period . at the end which installs the code in our current directory. If you do not include the period, Django will create an additional directory by default.

- This is a basic Django model where we import models from Django on the top line and then create a Book class that extends it. There are four fields: title, subtitle, author, and isbn. We also include a __str__ method so that the title of a book will display in the admin later on.

- The way Django works, now when a user goes to the homepage of our website they will first hit the config/urls.py file, then be redirected to books/urls.py which specifies using the BookListView. In this view file, the Book model is used along with ListView to list out all books.

- The final step is to create our template file that controls the layout on the actual web page. We have already specified its name as book_list.html in our view. There are two options for its location: by default the Django template loader will look for templates within our books app in the following location: books/templates/books/book_list.html. We could also create a separate, project-level templates directory instead and update our settings.py file to point there.

- Django REST Framework is added just like any other third-party app. Make sure to quit the local server Control + c if it is still running. Then on the command line type the below.

- There are multiple ways we can organize these files however my preferred approach is to create a dedicated api app. That way even if we add more apps in the future, each app can contain the models, views, templates, and urls needed for dedicated webpages, but all API-specific files for the entire project will live in a dedicated api app.


[<===BACK](../README.md)
