# python-package-recipe
Recipe for new Python packages using Pyscaffold

Assumptions:
- using [conda](https://docs.conda.io) for Python environment and package management
- using [pytest](https://docs.pytest.org) for testing
- other tools in use: [sphinx](https://www.sphinx-doc.org/), [tox](https://tox.wiki), [pre-commit](https://pre-commit.com)

1. pick a spot for your new package folder and copy `environment.yml` there; modify `environment.yml`
- change environment name (probably just use the package name)
- add any known dependencies
2. create the conda environment

```shell
$ conda env create -f environment.yml
```

3. create the package

```shell
$ putup -i new-project-name
```

4. move `environment.yml` into `new-project-name` folder

```shell
$ mv environment.yml new-project-name
```
