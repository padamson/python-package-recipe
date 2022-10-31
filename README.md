# python-package-recipe
Recipe for a new Python package using Pyscaffold

Assumptions:
- using [conda](https://docs.conda.io) for Python environment and package management
- using [pytest](https://docs.pytest.org) for testing
- other tools in use: [sphinx](https://www.sphinx-doc.org/), [tox](https://tox.wiki), [pre-commit](https://pre-commit.com)

1. pick a spot for your new package folder and copy `environment.yml` there; modify `environment.yml`
- replace new-package with an environment name (probably just the package name, perhaps with -dev appended)
- add any known dependencies

2. create and activate the conda environment

```shell
$ conda env create -f environment.yml
$ conda activate new-package
```

3. create the package

```shell
$ putup -i new-package
```

4. move `environment.yml` into `new-package` folder and add the package to your conda environment

```shell
$ mv environment.yml new-package
$ cd new-package
$ pip install -e .
```

5. if using `pre-commit`, update hooks

```shell
$ pre-commmit autoupdate
```

6. replace content in new-package `README.rst` after the package description with content in `README.rst` from this repo and update it appropriately

7. update CONTRIBUTING.rst

8. copy over and update RELEASE_WORKFLOW.md

9. copy over the logos included at the end of `README.rst`

10.  get to work!