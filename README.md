## ADS Microservice Template Instructions

Template for an ADS microservice project. 

### Usage
1. From the main template repository page, click the "Use This Template" button located above the file list. From the dropdown menu, select "Create a new repository". 
2. Name the new repository and add a description. Change the new repository owner and/or permissions as necessary.

    *Naming convention*: The repository name should end with `_service`, e.g. `reference_service`, `metrics_service`.
    
3. Update this README file: remove this instructions section and update the contents:
    
    * Replace instances of `<repo_name>` and `<package_name>`, including within the CI status badge
    * Update stub text (e.g. microservice name, description, maintainers, etc.)
    
4. Rename the directory `package_name`.

    *Naming convention*: The package name should be a shortened form of the repository name.

5. Edit the `pyproject.toml` file:

    * Replace `<repo_name>` and `<package_name>` 
    * In the `[project]` section, replace fields as indicated (i.e. name, description, author info)
    * Dependencies go here, instead of in `requirements.txt` and `dev-requirements.txt` files
    
6. Microservice code goes into the `package_name` directory. There's a `tests` sub-directory in there for your unittests.


### Features

The new project will have these:

- Uses `pyproject.toml` for dependencies (note: older ADS microservices may still use `requirements.txt` and `dev-requirements.txt` for dependencies)
- Provides `setup.py`
- Testing with Pytest (locally and using Github actions)
- Follows the [black] style guide with [flake8] and [isort]
- Style guide enforced on CI

[black]: https://github.com/psf/black
[flake8]: https://pypi.org/project/flake8/
[isort]: https://pypi.org/project/isort/
[pre-commit]: https://pre-commit.com/
[gh-secrets]: https://help.github.com/en/actions/configuring-and-managing-workflows/creating-and-storing-encrypted-secrets
[codecov]: https://codecov.io/
[pypi]: https://pypi.org/
[create-pat]: https://github.com/settings/tokens/new?scopes=repo

__________

# Microservice Name

<p align="center">

![CI Status](https://github.com/adsabs/<repo_name>/actions/workflows/ci.yml/badge.svg)

  <a href="https://codecov.io/gh/adsabs/<repo_name>">
    <img src="https://img.shields.io/codecov/c/github/adsabs/<repo_name>.svg?logo=codecov&logoColor=fff&style=flat-square" alt="Test coverage percentage">
  </a>
</p>

Add a description of the project here.

## Installation

Install this via pip (or your favourite package manager):

```bash
pip install package_name
```

## Development

Install locally into virtualenv.

```bash
virtualenv .venv
source .venv/bin/activate
pip install .[dev]
pip install .
pre-commit install
pre-commit install --hook-type commit-msg
```

## Maintainers

Dev 1, dev 2