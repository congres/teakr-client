# Teaker

## Installation

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
  pip install -U pip
  ```
- On Windows:
  ```bash
  python -m pip install -U pip
  ```

#### Install and setup Virtualenv
To install globally with pip:
```bash
pip install virtualenv
```
Virtualenv has one basic command to setup the virtual environnment:
```bash
virtualenv env
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
