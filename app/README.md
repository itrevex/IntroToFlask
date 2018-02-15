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
