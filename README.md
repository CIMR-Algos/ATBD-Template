# ATBD Template
A JupyterBook template for CIMR DEVALGO ATBDs. This repository holds a template for Algorithm Theoretical Basis Documents (ATBDs) for the ESA-funded DEVALGO project.

**DISCLAIMER: This repository is used for testing and developing jupyterbooks, it does not contain any valuable science.**

## Fetch and read the book
If you just want to download the repo and read the book (not building it):
```
cd </path/to/where/you/want/the/repo> # call it /PATH/
git clone <repo>
```
In your web browser load `file:///PATH/book/_build/html/intro.html` in the url field.

## Creating a new repo from the template
The `ATBD-Template` repo is a _template repository_. It can be used to create a new repo for your L2 book as a copy of the `ATBD-Template` repo,
directly with the right structure and with initial file content. You can then work on your L2 book repo, this will not change the
`ATBD-Template` repository.

Follow these instructions to create a new repo from the template repo: [link](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-repository-from-a-template).

## Structure of the repo
* Each L2 variable has its own GitHub repository, referenced from the [CIMR-Algos](https://github.com/CIMR-Algos) organization.
* In the repo we have (at least) 3 directories: `book/` (for the book itself), `algorithm` (for the software), `data` (for static data).
* Convention: the main branch is called `main` (not `master`). `git config --global init.defaultBranch main`. Here is [why](https://github.com/github/renaming).

## Instructions for building the book

### If needed, install miniconda
See https://docs.conda.io/en/latest/miniconda.html

### Create a conda environment and install the jupyter-book tools
```
conda create -c conda-forge --name JB python=3.8
conda activate JB
conda env list # check that JB is the current env
pip install --upgrade pip #(if needed several times)
pip install jupyter-book
```

### install packages needed for the book (this list might grow as we develop the books)
```
conda install -c conda-forge matplotlib numpy
```

### build the book
```
cd /path/to/local/repo/with/atbd/ # the root of the repo, with book/ algorithm/ data/ ...
jupyter-book build book/
jupyter-book build --all book/ #(force rebuild everything)
```

### develop the book and commit to GitHub
Edit the `.md` files of the book
Build the book (see above)
```
git add / commit #possibly in two commits, first the changes to the `.md` files, then the modified `_html` files
git push
```

## Instructions for publishing the book (with GitHub pages)

**This requires that the repository is public.**

We follow the instructions on the jupyterbook.org website: https://jupyterbook.org/en/stable/start/publish.html#

Install `ghp-import`:
```
conda install -c conda-forge ghp-import
```

Move to the `book/` subdirectory in your local directory.

Make sure the book HTML is freshly built
```
make
```

Remember to commit and push your edits to the `.md` and the `_build/` files (this pushes to `main` branch).

Run ghp-import
```
ghp-import -n -p -f _build/html
```

This will create a `gh-pages` branch (1st time) and push the new HTML pages to that branch (not `main`).

First time, visit "Settings / Pages" and check that it points at the `gh-pages` branch.

Your book is hosted at https://cimr-algos.github.io/ATBD-Template/

## Other Resources:
* [Setting up repos on GitHub](https://kbroman.org/github_tutorial/pages/init.html)
* [Put your JupyterBook on Github with online webpage (requires Public repo)](https://jupyterbook.org/en/stable/start/publish.html#)
