# Teaker

## Installation

alias python='/usr/bin/python3.x'

#### Install pip if needed:
To install pip, download get-pip.py.
```bash
curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py
```
Then run the following:
```bash
python get-pip.py
```

#### Upgrading pip
- On Linux or macOS:
  ```bash
  python -m pip install -U pip
  ```
- On Windows:
  ```bash
  python -m pip install -U pip
  ```

#### Install and setup Virtualenv
To install globally with pip:
```bash
python -m pip install virtualenv --user
```
Virtualenv has one basic command to setup the virtual environnment:
```bash
path/to/packages/virtualenv env
```
In a newly created virtualenv there will also be a activate shell script.
- On Posix systems,
  ```bash
  source env/bin/activate
  ```
- For Windows systems, activation scripts are provided for the Command Prompt and Powershell:
  ```bash
  > \path\to\env\Scripts\activate
  ```

#### Install Django
After you’ve created and activated a virtual environment, enter the command:
```bash
pip install Django
```

### Verifying
To verify that Django can be seen by Python, type `python` from your shell. Then at the Python prompt, try to import Django:
```python3
>>> import django
>>> print(django.get_version())
2.0
```


## The development server
Let’s verify your Django project works. Change into the outer mysite directory, if you haven’t already, and run the following commands:
```bash
python manage.py runserver 0.0.0.0:8000
```

## Local to global access: Port Forwarding
- add IP in `ALLOWED_HOSTS` in `settings.py`
- enable portfowarding in your personnal router

## IP to FQDN: Dynamic DNS
- Duckdns inscription
- ./duck.sh

## Prod Deployment
### How to use Django with uWSGI
uWSGI is a fast, self-healing and developer/sysadmin-friendly application container server coded in pure C.

```bash
pip install uwsgi
uwsgi --http :8000 --module teaker.wsgi
```

## Basic nginx
```bash
sudo apt-get install nginx
sudo /etc/init.d/nginx start    # start nginx
```

You will need the uwsgi_params file, which is available in the nginx directory of the uWSGI distribution, or from https://github.com/nginx/nginx/blob/master/conf/uwsgi_params
