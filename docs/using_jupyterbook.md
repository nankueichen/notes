# using jupyterbook
`2023-11-17`

I followed this [tutorial](https://jupyterbook.org/en/stable/start/overview.html) to set up my jupyterbook. The highlights are:

1. Everthing is located here: __Dropbox/jupyterbook__
2. Using virtual environment:
	* `python3 -m venv venv`
	* `source venv/bin/activate`
3. Installing python modules:
	* `python -m pip install jupyter-book`
4. Pin the dependence
	* `python -m pip freeze > requirements.txt`
1. Create a new folder __lipidMRI__ and organize the files there
	* `jupyter-book create lipidMRI`
	* I then edited the automatically produced _book configuration_ file _config.yml
	* I then edited the automatically produced _Table of Contents_ file _toc.yml . This is a YAML file with a collection of pages, each one linking to a file in the book.
	* Book content: A collection of text files make up your book’s content. These can be one of several types of files, such as markdown (`.md`) and Jupyter Notebooks (`.ipynb`), and MyST markdown (`.md`) that is discussed [here](https://myst-nb.readthedocs.io/en/v0.9.1/use/markdown.html#:~:text=MyST%20Markdown%20Notebooks%20allow%20you,use%20with%20text%2Dbased%20tools.). For example, `:::{note}` is a directive in MyST Markdown.
1. Now it’s time to build outputs for the book, using the `jupyter-book build` command line tool for this.
	* `jupyter-book build lipidMRI`
1. To back up files and publish the book in github, following [this](https://jupyterbook.org/en/stable/start/publish.html)
	* `git init`
	* `git remote add origin https://github.com/nankueichen/lipidMRI.git`
	* `git add .`
	* `git commit -m "Add documentation"`
	* `git push -u origin main` or using github Desktop to push
1. To host the book in _readthedocs_, I followed this [link](https://jbtest.readthedocs.io/en/latest/intro.html) and added a __.readthedocs.yml__ file.
