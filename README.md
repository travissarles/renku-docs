# Renku Project Documentation

This repository contains the base documentation of the Renku Project and
aggregates pieces of documentation from various components of Renku.

## Prerequisites

* `pyenv` with the `virtualenv` plugin
* `make`

## Building

To build the documentation, you must initialize the submodules, install
the dependencies, and use `make`:

```
git submodule sync
git submodule update --init --force renku-python renku

pyenv virtualenv 3.9.0 renku-docs
pyenv activate renku-docs
pip install -r requirements.txt

make html
```

The docs will now be available in `_build/html`.
