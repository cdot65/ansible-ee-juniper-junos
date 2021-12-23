# Ansible Execution Environment: Juniper JunOS
[![N|Solid](https://upload.wikimedia.org/wikipedia/commons/thumb/3/31/Juniper_Networks_logo.svg/315px-Juniper_Networks_logo.svg.png)](https://www.ansible.com/products/execution-environments)

## Overview

This project aims to bring our needed Python packages into Ansible AWX through the construct of an Execution Environment.

You can read more about Execution Environments at this link: https://www.ansible.com/products/execution-environments, but let's call it even by saying that Ansible Execution Environments are a method to build a custom execution environment for Ansible AWX.

### Declare your dependencies

Visit the `requirements.txt` and `requirements.yml` files to update Python packages and Ansible Collection dependencies, respectively.

### 🐍 Prep your Python environment

I have included a Poetry file for anyone saavy enough to take advantage. For the uninitiated, Poetry helps replicate Python environments between users with a single file. 

You'll need to have Poetry installed on your machine, please visit the docs for the one-liner

> Poetry: https://python-poetry.org/docs/

1. install Python dependencies

```bash
poetry install
```

2. activate environment

```bash
poetry shell
```

## Executing the build

build the container image with

```bash
ansible-builder build --tag (please insert the name of your container image here)
```

## Upload container image

Your last step will be to upload your resulting Docker container image to a centralized repository that Ansible AWX can access.

## 📝 Dependencies

Refer to the Poetry Lock file located at [poetry.lock](poetry.lock) for detailed descriptions on each package installed.
