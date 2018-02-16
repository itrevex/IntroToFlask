# INTRODUCTION TO FLASK

## SETTING ENVIRONMENT

### 1. Instal Python and Virtual Environment

* Download and install [python](https://www.python.org/downloads/) distribution
* Download and install pip
* Download [get-pip.py](https://bootstrap.pypa.io/get-pip.py) to a folder on your computer. Open a command prompt window and navigate to the folder containing get-pip.py. Then run `python get-pip.py`. This will install pip.
* Now you install **_distribute_** and _**virtualenv**_ using pip as follows:

  * `pip install virtualenv`

#### NOTE: If you run into installation error, try the following

* `pip install -U setuptools` to update setuptools and package resources

### 2. Install Flask in Virtual Environment

* create app folder `app`
* `cd app` to enter `app` folder where we shall install the virtualenv
* run `virtualenv --version` to check if virtual environment was installed succesfully
* `$ virtualenv env` creates a folder _env/_, and sets a clean copy of Python inside
* `env/. bin/activate` or `env/scripts/activate` to activate environment and begin working with it
* `pip install Flask` safely install flask in new virtual environment

## MAKING THE FLASK APP

* create app folder with a static and templates folder, create a routes.py file and a README.md file
* Follow through the files to see how this simple example has been done

## ADDING PROJECT TO GITHUB

* Create new repository on github
* Initial git on in your local project `git init`
* Create a `.gitignore` file and ignore files inside `env` folder, which our virtual env folder
* Add and commit files inside your local repository `git add . && -am"First Commit"`
* Add remote repository to your local repository `git remote add origin remote_repository_url.gi`
* `git remote -v` to verify new remote url
* `git pull origin` to get changes on the origin synced with those you have locally.
* if you find there some staged files from remote that you want to reset, do a `git resest filename` and you can remove the changes and commit what you exactly want.
* Push local changes to remote `git push origin master`

## DEPLOYING APP ON HEROKU

* First of all create a requirements file `pip freeze > requirements.txt`
* Update requirements file every time you add a new depedancy by running command above
* Then install gunicorn `pip install gunicorn`
* Create a `Procfile`, and this the server to `web: gunicorn app:app`, see _*setting up Procfile below*_
* create app on heroku site, or in command line interface `heroku create app_name`, _app_name_ is not mandatory, if you left it out, heroku would generate one for you.
* `heroku git:remote -a intro-to-flask` to link heroku to remote
* `git push heroku master` to push changes to heroku
* ensure that at least one instance of the app is running before opening `heroku ps:scale=1`
* `heroku open` to open app

### Setting Up the Procfile

*`web: gunicorn routes: app`* This means that use heroku's `web` process to run the `gunicorn` server and look for a file named ``routes.py` and run the `app` method in that file. Voula, your done setting up the `Procfile`.