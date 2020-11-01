# Django-Blog
[![](https://img.shields.io/pypi/pyversions/Django.svg)](https://python.org/downloads/)
[![](https://img.shields.io/badge/django-2.0%20%7C%202.1%20%7C%202.2-success.svg)](https://djangoproject.com/)


Full-Featured Blog with Django web framework. 

Screenshots
=
![HomePage](https://user-images.githubusercontent.com/69810375/97808602-ebfb1800-1c8d-11eb-86c0-c0eb7cd676af.PNG)
![HomePage2](https://user-images.githubusercontent.com/69810375/97808635-15b43f00-1c8e-11eb-9b30-7968bbc04b84.PNG)
![EditPost](https://user-images.githubusercontent.com/69810375/97808671-3e3c3900-1c8e-11eb-976e-35ddc4cdad8d.PNG)
![AddPost](https://user-images.githubusercontent.com/69810375/97808692-51e79f80-1c8e-11eb-84c4-5718f4d714a9.PNG)
![EditProfile](https://user-images.githubusercontent.com/69810375/97808724-7b083000-1c8e-11eb-8361-f965affc98ad.PNG)
![SignUp](https://user-images.githubusercontent.com/69810375/97808742-96733b00-1c8e-11eb-9b19-c67a54c49aa2.PNG)
![LoginPage](https://user-images.githubusercontent.com/69810375/97808747-a12dd000-1c8e-11eb-97f4-f75c79cc3abe.PNG)
![PasswordReset](https://user-images.githubusercontent.com/69810375/97808759-adb22880-1c8e-11eb-8e49-ede89590dc48.PNG)

Features 
=
- User Registration
- User Login & Logout
- User Profile
- Create, Update, Edit & Delete Posts
- Search
- User Change Password
- Password Reset
- Customized admin panel

How To Use
=
## Clone project & Install Requirements
> Make sure you have already installed python3 and git.
```
$ git clone https://github.com/amanasati11/Django-Blog.git && cd django-blog
$ pip install -r requirements.txt
```
## Migrate & Collect Static
```
$ cd src && python manage.py migrate
$ python manage.py collectstatic
```
## Create Admin User
```
$ python manage.py createsuperuser
```
## Run Server
```
$ python manage.py runserver
```
> Enter your browser http://localhost:8000/. You can login via admin in http://localhost:8000/admin/.

## Add Some Fake Posts
> First add one another user from blog register page or admin panel.
```
$ python manage.py shell
>>> from blog.models import Post
>>> import json
>>> with open('posts.json') as f:
...     json_posts = json.load(f)
...
>>> for post in json_posts:
...     Post(title=post['title'], content=post['content'], author_id=post['user_id']).save()
...
>>> exit()
```
> You can edit posts via admin panel or from corrent user added post.
## Project Structure

C:.
├───.idea
│   ├───dictionaries
│   └───inspectionProfiles
├───blog
│   ├───migrations
│   │   └───__pycache__
│   ├───static
│   │   └───blog
│   ├───templates
│   │   └───blog
│   └───__pycache__
├───django_blog
│   └───__pycache__
├───media
│   └───profile_pics
└───users
    ├───migrations
    │   └───__pycache__
    ├───templates
    │   └───users
    └───__pycache__
