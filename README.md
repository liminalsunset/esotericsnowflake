1. Create a blank repo on Github

From the terminal:

2. Make a directory for project
3. CD into directory
4. python3 -m venv env_name
5. source env_name/bin/activate

after you've created and activated your venv:

6. python3 -m pip install Django

It might be suggested you update pip here, if you'd like to you can:

python3 -m pip install --upgradepip

7. django-admin startproject project_name

cd into your project

8. python3 manage.py runserver

9. maybe check out http://localhost:8000/
also:

** You have 80,000 unapplied migrations

10. python3 manage.py migrate

11. Find a .gitignore

12. code .

13. In VS Code terminal once you open your project:

    - start the venv here by cd .. up to the root directory (where the venv is located) and type source env_name/bin/activate and then cd back into your project folder.

    - it should change to (env_name) -> project_name in the terminal

14. add the .gitignore at the same directory level as manage.py <=== !

    (I will probably add a link to a .gitignore)

    read the documentation on .gitignore
    https://git-scm.com/docs/gitignore

IMPORTANT!!:

Set up an ENV:

15. make sure your .gitignore ignores .env

16. make a .env file (at the same directory level as manage.py and your .gitignore)

17. Cut your secret key from settings.py (in project directory) and paste it in your .env 

18. Where your security key was in settings.py, replace that with (this is case sensitive, you're probably already aware but just in case):

from decouple import config

SECRET_KEY = config(“SECRET_KEY”)

19. Then in your terminal run:

pip install python-decouple
pip freeze > requirements.txt (I would google this further, but basically it seems to just keep track of your dependencies)

(here is a great site about this/python decouple: https://simpleisbetterthancomplex.com/2015/11/26/package-of-the-week-python-decouple.html)


**7/10 test -- works until this point so far**

20. git init
21. git add .
22. git commit -m "first commit"
23. git branch -M main
24. git remote add origin .. (past your git remote origin address)

start app

In root directory:

25. python3 manage.py startapp myapp

In settings.py:

26. update INSTALLED_APPS --
    add 'myapp.apps.MyappConfig'

    * the django projects folder holds manage.py and the other module that includes settings.py
    * adding it to the settings.py under INSTALLED_APPS tells your project of its existence

--
    python3 manage.py startapp myapp


unreviewed continuation:

--
27. urls.py









--
    possibly useful:
    git config --global credential.helper osxkeychain
    git remote set-url origin [updated link url https://........git]
__

aside: Django MTV architecture: https://towardsdatascience.com/working-structure-of-django-mtv-architecture-a741c8c64082

