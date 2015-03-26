# project_sketch

A nerd's boilerplate for your Python project.


## Usage

```bash
$ cp project_sketch <your_projects_name>
$ cd <your_projects_name>
$ mv project_sketch <your_projects_name>
```

And change every `project_sketch` word into `<your_projects_name>`.


## Hierarchy

```
project_sketch
├── project_sketch
│   ├── _module
│   │   └── __init__.py
│   └── __init__.py
├── .gitignore
├── setup.py
├── Makefile
├── manage.py
├── requirements.txt
├── dev-requirements.txt
└── README.md
```

## Explanation

- **project_sketch/**

  The Python package of this project, mostly has the same name with root folder

- **project_sketch/__init__.py**

  Essential file to claim a package, contains `__version__` variable.

- **project_sketch/_module/**

  A submodule of the project, there's also a necessary `__init__.py` under it.

  you can `cp _module what-you-like` to create a new submodule.

- **.gitignore**

  Simple, effective gitignore, much less verbose than
  [this windbag](https://github.com/github/gitignore/blob/master/Python.gitignore)

- **setup.py**

  You may hate it, but you can't ignore it. This `setup.py` do just what you want,
  and it automatically involves `requirements.txt` and `README.md`.

  If you rock, go and dig [this](https://pinboard.in/u:reorx/t:python/t:packaging).

- **Makefile**

  We love Makefile, not Rakefile or Gruntfile or whatever requires extra program.
  This awesome Makefile contains three commands at your service:

  * `make build`

    Build Python package with `setup.py`.

  * `make clean`

    Clean files & folders generated by `build`.

  * `make test`

    Run tests (if you have any) with nose.

- **manage.py**

  Try `pip install click` & `./manage.py ping` to see how it works.

  If you are writing something needs to run in a complicated way,
  and you realize that this sort of code should not be put in the package,
  this is what you need. `manage.py` is a entrance script which you can customize
  your own command in it. By default, it uses [click](http://click.pocoo.org/3/)
  to define commands & options, you can replace it by other things like
  [docopt](http://docopt.org/), or [fabric](http://www.fabfile.org/)
  (the file should be named `fabfile.py` then), if you prefer.

  If you are writing a pure import-only package, feel free to remove it.

- **requirements.txt**

  Includes a `click` by default, this is what your package depends on.

- **dev-requirements.txt**

  Includes a `nose` by default, this is what you need in developing environment,
  but not necessary in production.

- **README.md**

  A cute, well formatted `README.md` makes people happy.  
  True heros love `README.rst`.
