# Package Name

<p align="center">

![CI Status](https://github.com/adsabs/<repo_name>/actions/workflows/ci.yml/badge.svg)

  <a href="https://codecov.io/gh/adsabs/<repo_name>">
    <img src="https://img.shields.io/codecov/c/github/adsabs/<repo_name>.svg?logo=codecov&logoColor=fff&style=flat-square" alt="Test coverage percentage">
  </a>
</p>

Template for an ADS microservice project. 

## Usage
From the main repository page, click the "Use This Template" button located above the file list. From the dropdown menu, select "Create a new repository". 

**Naming Conventions**

We generally follow these naming conventions in ADS microservices:
* The repository name should end with `_service`, e.g. `reference_service`, `metrics_service`.
* The package name should be a shortened form of the repository name.

**Things to edit**

Once the template is copied into a new repository, there are a few things that need to be edited:
* The name of the directory `package_name` should be changed (see Naming Conventions section above). Code files go here.
* The CI and coverage badges within this README need to be edited to include the new repository name, as indicated by `<repo_name>`.
* `pyproject.toml` needs to be edited:
    * Replace `<repo_name>` and `<package_name>` 
    * In the `[project]` section, replace fields as indicated (i.e. name, description, author info)
    * Dependencies go here, instead of in `requirements.txt` and `dev-requirements.txt` files

## Features

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

