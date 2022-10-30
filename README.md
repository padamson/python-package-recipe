# python-package-recipe
Recipe for a new Python package using Pyscaffold

Assumptions:
- using [conda](https://docs.conda.io) for Python environment and package management
- using [pytest](https://docs.pytest.org) for testing
- other tools in use: [sphinx](https://www.sphinx-doc.org/), [tox](https://tox.wiki), [pre-commit](https://pre-commit.com)

1. pick a spot for your new package folder and copy `environment.yml` there; modify `environment.yml`
- replace new-package-name with an environment name (probably just the package name, perhaps with -dev appended)
- add any known dependencies

2. create and activate the conda environment

```shell
$ conda env create -f environment.yml
$ conda activate new-package-name
```

3. create the package

```shell
$ putup -i new-package-name
```

4. move `environment.yml` into `new-package-name` folder

```shell
$ mv environment.yml new-package-name
```

5. if using `pre-commit`, update hooks

```shell
$ cd new-package-name
$ pre-commmit autoupdate
```
