Plan 9 Documentation Project
=============================
This documentation repository is for community collaboration to create documentation for future revisions and additions to the Plan 9 wiki. This repository builds automatically on every changes pushed in. This repository build a [collaboration site](https://plan9-documentation.readthedocs.io).

It uses Sphinx, myst-parser, [readthedocs.io](https://readthedocs.io) hook to produce documentation from the Markdown source files in this repository.



## Local development server 

Choose a platform to use as a development server. In this example, FreeBSD is depicted.

Use a local development server that regenerates the output whenever the input changes:

```
git clone git@github.com:tip9ug/plan9-documentation.git
sudo pkg install -y py38-pip py38-sphinx py38-myst-parser py38-sphinx_rtd_theme gmake
pip install docutils==0.16
sudo pip install sphinx-autobuild
cd plan9-documentation
sphinx-autobuild source build/html
```

Now open http://127.0.0.1:8000/index.html in a web browser. It will be regenerated and refreshed whenever one of the files changes get saved.

## Generating documentation

One can also generate documentation in various output formats locally:

```
gmake html
gmake epub

```
