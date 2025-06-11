MathJax for Django
==================

This package provides a copy of MathJax, a JavaScript library for
displaying mathematics on the web, packaged for use with the Django
web framework.

## Installation and usage

To use MathJax with Django:

1. Install this package.

For instance, if you use Poetry, add this line in the `[tool.poetry.dependencies]` section of your pyproject.toml:

    django-static-mathjax = {git = "https://github.com/MIT-LCP/django-static-mathjax", branch="master"}

2. Add `'mathjax'` to your list of `INSTALLED_APPS`.

3. Add a script tag to your page templates, such as:

```
<script src="{% static 'mathjax/es5/tex-mml-chtml.js' %}"></script>
```

For more information about MathJax, refer to https://www.mathjax.org/.

For more information about Django, refer to https://www.djangoproject.com/.

## Contributing

1. [Install npm](https://docs.npmjs.com/downloading-and-installing-node-js-and-npm) if not already installed, for instance:

```
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.3/install.sh | bash
nvm install node
```

2. Clone this project with the mathjax submodule:

```
git clone --recurse-submodules https://github.com/MIT-LCP/django-static-mathjax
```

3. Create and source your Python virtual environment:

```
cd django-static-mathjax
python -m venv .venv
source .venv/bin/activate
```

4. Ensure pip and setuptool are up-to-date:

```
pip install --upgrade pip
pip install --upgrade setuptools
```

5. Install django-static-mathjax module:

```
pip install .
```

6. Eventually update the dependencies in the pyproject.toml of your projects using django-static-mathjax in order to look at the local folder, for instance:

```
django-static-mathjax = {path = "../django-static-mathjax", develop = true}
```
