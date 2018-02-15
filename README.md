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

* `virtualenv --version` check if virtual environment was installed succesfully
* `$ virtualenv flaskapp` creates a folder _flaskapp/_, and sets a clean copy of Python inside
* `cd flaskapp` to enter new developement environment
* `. bin/activate` or `scripts/activate.bat` activate environment to begin working in it
* `pip install Flask` safely install flask in new environment

## MAKING THE FLASK APP

* create app folder with a static and templates folder, create a routes.py file and a README.md file
* Follow through the files to see how this simple example has been done

## ADDING PROJECT TO GITHUB

* Create new repository on github
* Initial git on in your local project `git init`
* Add and commit files inside your local repository `git add -am"First Commit"`
* Add remote repository to your local repository `git remote add origin remote_repository_url.gi`
* `git remote -v` to verify new remote url
* Push local changes to remote `git push origin master`

## DEPLOYING APP ON HEROKU

* First of all create a requirements file `pip freeze > requirements.txt`
* Update requirements file every time you add a new depedancy by running command above
* Then install gunicorn `pip install gunicorn`
* Create a `Procfile`, and this the server to `web: gunicorn app:app`
* create app on heroku site, or in command line interface `heroku create`
* `heroku git:remote -a intro-to-flask` to link heroku to remote
* `git push heroku master` to push changes to heroku
* ensure that atleast one instance of the app is running before opening `heroku ps:scale=1`
* `heroku open` to open app