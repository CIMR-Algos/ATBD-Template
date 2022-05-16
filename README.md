# ATBD-Template
A JupyterBook template for CIMR DEVALGO ATBDs

## Structure of the repo
* Each L2 variable has its own GitHub repository, referenced from the [CIMR-Algos](https://github.com/CIMR-Algos) organization.
* In the repo we have (at least) 3 directories: `book/` (for the book itself), `algorithm` (for the software), `data` (for static data).

## Instructions for building the book

### If needed, install miniconda
https://docs.conda.io/en/latest/miniconda.html

### Create a conda environment and install the jupyter-book tools
conda create -c conda-forge --name JB python=3.8
conda activate JB
conda env list # check that JB is the current env
pip install --upgrade pip #(if needed several times)
pip install jupyter-book

### install packages needed for the book (this list might grow as we develop the books)
conda install -c conda-forge matplotlib numpy

### build the book
cd /path/to/local/repo/with/atbd/ # the root of the repo, with book/ algorithm/ data/ ...
jupyter-book build book/
jupyter-book build --all book/ #(force rebuild everything)

### develop the book and commit to GitHub
Edit the `.md` files of the book
Build the book (see above)
git commit (possibly in two commits, first the changes to the `.md` files, then the modified `_html` files)
git push

## Other Resources:
* [Setting up repos on GitHub](https://kbroman.org/github_tutorial/pages/init.html)
* [Put your JupyterBook on Github with online webpage (requires Public repo)](https://github.com/pabloinsente/jupyter-book-tutorial)
