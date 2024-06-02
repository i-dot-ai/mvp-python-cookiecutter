# Minimal Python Cookiecutter

This is a very basic Python Cookiecutter repo.


## How to use this

- Ensure Cookiecutter is installed: https://cookiecutter.readthedocs.io/en/stable/README.html.
- Clone this repo.
- Run `cookiecutter mvp-python-cookiecutter`.
- You will be prompted for the project name. This will be slugified for the repo name and the package name within the repo.
- You should now have a new repo!

Within the new repo:
- Run `git init` to initialise it as a Git repo.
- Run `poetry install` to install packages.
- Update the `README.md` with project details including how to run your code.
- Add to the `PULL_REQUEST_TEMPLATE.md` as needed.
- You will likely need to tweak settings for `ruff`, `mypy` and `poetry` in the `pyproject.toml` file, and the settings for `pre-commit` in `.pre-commit-config.yaml`.
- GitHub Actions can be amended in `.github`.
- Amend `.gitignore` (and potentially `pre-commit`) to make sure sensitive data is not committed.


## What is included

This uses:
- [Poetry](https://python-poetry.org/) for Python package and dependency management.
- [Ruff](https://docs.astral.sh/ruff/) for linting and formatting (controversially with a 100 char line length limit).
- [Mypy](https://mypy.readthedocs.io/en/stable/#) for checking type hints.
- [Pre-commit](https://pre-commit.com/) to avoid committing sensitive data
- [Pytest](https://docs.pytest.org/) for running tests.
- [EditorConfig](https://editorconfig.org/) for formatting non-Python files
- [GitHub Actions](https://github.com/features/actions) for CI (basic code checks and running tests)
- [Dependabot](https://docs.github.com/en/code-security/dependabot) config file
- `.env.example` file for environment variables (take a copy `.env` not to be committed into the repo).
- `.gitignore` file with common files to be excluded from Git.

There is a `Makefile` with some basic shortcuts.

This does **not** include:
- Anything Django-specific.
- Non-Python settings (apart from EditorConfig).
- Docker-related files.
- Anything to do with infrastructure or deployment.