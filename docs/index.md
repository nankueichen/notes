# using mkdocs
`2023-11-15`

I followed this [real python webpage](https://realpython.com/python-project-documentation-with-mkdocs/) to set up my mkdocs. The highlights are:

1. Everthing is located here: __Dropbox/mkdocs__
2. Using virtual environment:
	* `python3 -m venv venv`
	* `source venv/bin/activate`
3. Installing python modules:
	* `python -m pip install mkdocs`
	* `python -m pip install "mkdocstrings[python]"`
	* `python -m pip install mkdocs-material`
1. Pin the dependence
	* `python -m pip freeze > requirements.txt` (see [here](https://realpython.com/python-virtual-environments-a-primer/#pin-your-dependencies))
1. Create a new mkdocs folder __notes__ and organize the files there
	* `mkdocs new notes`
	* I then edited the automatically produced file __mkdocs.yml__
	* In the future I could add more *md files to the __docs__ folder and update the __index.md__
1. Start the live-reloading docs server
	* `mkdocs serve`
1. Optionally Build the documentation site
	* `mkdocs build` 
1. more information in [mkdocs.org](https://www.mkdocs.org). Also Print help message and exit
	* `mkdocs -h`
1. To back up files in github: 
	* `git init`
	* `git remote add origin https://github.com/<user name>/notes.git`
	* `git add .`
	* `git commit -m "Add documentation"`
	* `git branch -M main`
	* `git push -u origin main` or using github Desktop to push
	* Following these [instructions](https://squidfunk.github.io/mkdocs-material/publishing-your-site/) I could add a github workflow. Afterward, in __setting__ / __Pages__ of the github folder, I change the Branch to __main__ and location to __/doc__ ; Afterward the github site is up and running.
	* I then add __.readthedocs.yaml__ and __requirements.txt__ so that the document can be built in _readthedocs.io_ website.

Try the math here $\alpha$, $\gamma$
