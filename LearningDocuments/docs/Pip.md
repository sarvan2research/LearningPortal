# Pip Install Instructions

Python's official documentation says:

"A virtual environment is a Python environment such that the Python interpreter, libraries and scripts installed into it are isolated from those installed in other virtual environments, and (by default) any libraries installed in a “system” Python, i.e., one which is installed as part of your operating system"

To break this down, when you activate a virtual environment for your project, your project becomes its own self contained application, independent of the system installed Python and its modules. 

## Below Command to setup venv, use and deactivate

```
python<version> -m venv <virtual-environment-name>

ex:
python -m venv venv

//Activate
source venv/bin/activate

//Deactivate
deactivate

```

## Export venv library to txt
```
pip freeze > requirements.txt

Add requirement file part of code base


```

## Install venv required file
```
Install it on new systems

 pip install -r requirements.txt
```
