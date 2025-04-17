# Parents and Baby Book


## How to Contribute

This repository contains mostly markdown files. To make sure we have the same conventions, we have added markdownlint tools to pre-commit. So please install [pre-commit](https://pre-commit.com/) then run the following command the first time you cloned the repository.

```bash
pre-commit install
```

### Preview Requires Python

Install the requirements using

```
poetry install
```

Preview the docs:

```python
poetry run mkdocs serve -s
```

### Developing Notebooks

We use jupytext to sync the `.py` files to `.ipynb` files. `.ipynb` files are ignore in git.
Please pair the `.py` file with the `.ipynb` using jupytext in jupyterlab first.

### Optional Requirements

> The pdf generation is done by the [mkdocs-with-pdf](https://github.com/orzih/mkdocs-with-pdf) plugin.

To generate PDF locally, please install [cairo, Pango and GDK-PixBuf ](https://doc.courtbouillon.org/weasyprint/latest/first_steps.html#macos).


#### Install pango on Mac

When installing pango on Mac using homebrew, the path for `DYLD_LIBRARY_PATH` are not automatically updated. So we need to add the correct path for pango, harfbuzz, and fontconfig. For example,

```
export DYLD_LIBRARY_PATH=$DYLD_LIBRARY_PATH:/Users/itsme/homebrew/Cellar/pango/1.48.8/lib:/Users/itsme/homebrew/Cellar/harfbuzz/2.8.2/lib:/Users/itsme/homebrew/Cellar/fontconfig/2.13.1/lib
```
