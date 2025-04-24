# heroku-buildpack-uv

A Heroku Buildpack for [uv](https://github.com/astral-sh/uv).

Generates `requirements.txt` and `.python-version` files from your `uv.lock` file.

This buildpack is essentially a pre-processor for the [`heroku/python`](https://github.com/heroku/heroku-buildpack-python) buildpack, so it should be added *before* `heroku/python`.

For example:

```
heroku buildpacks:clear
heroku buildpacks:add https://github.com/muchbetteradventures/heroku-buildpack-uv.git
heroku buildpacks:add heroku/python
```

Originally developed for use with [Plain](https://plainframework.com/), but can be used with any Python project using uv.
