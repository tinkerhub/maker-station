## Why learn Django ❓

- Django is designed to create web applications quickly and easily, ranging from small websites to large-scale enterprise applications.
- Learning Django can enable you to build a variety of web applications, including blogs, e-commerce sites, social networks, content management systems, and more.
---
## 🎓 Take Away Skills

After completing this learning path you will be knowledgeable in:

- django-admin cli
- handle HTTP request and response
- Rendering Templates using Django templates
- ORM (Object Relation Mapper)
- Form handling
- Authentication
- APIs using Django Rest Framework


---
## 🛠️ Prerequisites
## 🧑🏻‍💻 Programming Knowledge 

Before learning django, there are a few prerequisites that you should have a basic understanding of:

  - **Python** : You need to have a good grasp of python which include, data types, variables, functions, lists, control structures, classes and objects.

  - **HTML, CSS and JS** : To build a web application with django, you need to have basic understanding of HTML, CSS and Javascript.

## 📲 Installation and Setup

You need to install a code editor, browser and a python interpreter to follow along this path. You can choose editor and browser of your choice, the preferred ones are listed below

 - **VS Code**
 
    Light-weight code editor by Microsoft with a large ecosystem of plugins to help your workflow

    [Install VS Code](https://code.visualstudio.com/)

 
 - **Google Chrome**

    A browser based on V8 JavaScript engine with developer tools.
    
    [Install Google Chrome](https://chrome.google.com)

 - **Python**

    The Python interpreter that executes Python code. It is available for download from the official Python website,
    make sure to check the option to add to path during installation.

    [Install Python](https://python.org)


*Get started by installing Django using pip*

```bash
pip install django
```

*Choose a project directory and run the following command to create a django project.*

```bash
django-admin startproject myproject
```

*Now move into the newly created project folder and open vscode to start editing*

```bash
cd myproject
code .
```

*To make sure everything is done correctly run the following command to run the development server*

```
python manage.py runserver
```

---

## 💡 Learning Session

### 🎓 Topics to Learn

- **django CLI**
    - Create project and apps
    - Database migration

- **urls**
    - url patterns
    

- **Creating views**
    - Templates
        - if..else
        - for loop
        - blocks
        - include
        - extends
    - Static files

- **ORM (Object relation mapper)**
    - Database models
    - Field options
    - Database CRUD operation
    - Table relationships
    - Aggregation
- **Forms**
    - CSRF Tokens
    - Form fields
    - Rendering forms in templates
- **Authentication**
    - Creating Login and sign up forms
    - Session handling

- **Extensions**
    - [Crispy Forms](https://django-crispy-forms.readthedocs.io/en/latest/)
    
    - [Django Storages](https://django-storages.readthedocs.io/en/latest/)

    - [Django Channels](https://channels.readthedocs.io/en/stable/)

    - [Django-allauth](https://www.intenct.nl/projects/django-allauth/)

- **Hosting**
    - Gunicorn
    - NGINX
    - PostgreSQL
    - Docker


### 🎓 Learn from

#### 📽️ Videos

- [Django tutorial for beginers (Telusko)](https://youtube.com/playlist?list=PLsyeobzWxl7r2ukVgTqIQcl-1T0C2mzau)

- [Django  Web development tutorial (Tech with Tim)](https://youtube.com/playlist?list=PLzMcBGfZo4-kQkZp-j9PNyKq7Yw5VYjq9)

#### 📄 Articles/Blogs

- [Django Templates](https://www.w3schools.com/django/django_template_variables.php)

- [Django Models](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Django/Models)

- [CSRF token in Django](https://www.tutorialspoint.com/what-is-csrf-token-in-django#:~:text=CSRF%20stands%20for%20Cross%20Site,putting%20the%20data%20at%20risk.)

### 🛠️ Get into action

Small and Easy projects to test what you have learned so far

- Create a simple todo-list. Use django models to store to the database. 

- Create a owner-pet model to understand database relationship (Use the admin interface to add and delete data)

- Use a css framework like [bootstrap](https://getbootstrap.com/) to create a base template, Extend the view and generate dynamic contents using data from the database

---
## 🔖 Resource Pool

### 📄 Articles/Blogs

- [Django Web Framework](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Django/Introduction)

- [Django REST framework (Javapoint)](https://www.javatpoint.com/create-rest-api-using-django-rest-framework)

### 📽️ Videos
- [The basocs of Django Models](https://youtu.be/r9kT-jm136Q)
- [Django authentication Basics](https://youtu.be/dBctY3-Z5hY)
- [Django REST Framework Course](https://youtu.be/tujhGdn1EMI)
- [Sending Emails in Django](https://youtu.be/X7DWErkNVJs)
- [Django Stripe payment integration](https://youtu.be/JwhEjEqG43M)

### 🫂 Communities

- [Django Forum](https://forum.djangoproject.com/)
---
## 🚀 Project Pool


A few projects you can build to implement the concepts you have learned above:


- Create a microblog using all the features we learned. ie, templates, models, authentication, database models. Try to add features like comments, likes etc.

- Create an E-Commerce application. Get familiar with integrating payment gateway checkout [Razorpay](https://razorpay.com/) and [stripe](https://stripe.com/)