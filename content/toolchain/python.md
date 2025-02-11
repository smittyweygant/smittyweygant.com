---
title: 'Python Setup'
date: 2025-02-06T15:35:00+07:00
draft: false
description: 'My approach to managing Python environments'
menus:
  toolchain:
---
There are many ways to approach Python environment and version management. Ultimately, the ideal solution allows for any project to run a different version of Python and package a unique set of dependent libraries. 

This article from the team at [Daytona](www.daytona.io) provides a great overview and comparison of the various environment management tools. 

[The Ultimate Guide to Managing Python Environments](https://www.daytona.io/dotfiles/the-ultimate-guide-to-managing-python-environments)

<!--more-->
I have chosen to use ```pipenv``` but have some older projects that use ```pyenv```.  

```python {.line-numbers}
    # Install pipenv
    pip install pipenv

    # Create environment and install dependencies
    pipenv install

    # Activate environment
    pipenv shell

    # Install specific package
    pipenv install requests

    # Install development dependencies
    pipenv install pytest --dev

    # Generate requirements.txt
    pipenv lock -r > requirements.txt

    # Deactivate environment
    exit
```

I have a few projects where I've used ```pyenv``` 

```python {.line-numbers}
    # Install pyenv (macOS/Linux)
    brew install pyenv

    # Install pyenv-virtualenv plugin
    git clone https://github.com/pyenv/pyenv-virtualenv.git \ 
    $(pyenv root)/plugins/pyenv-virtualenv

    # Install Python version
    pyenv install 3.8.0

    # Create environment
    pyenv virtualenv 3.8.0 myenv

    # Activate environment
    pyenv activate myenv

    # Install packages
    pip install package_name

    # Deactivate environment
    pyenv deactivate
```


