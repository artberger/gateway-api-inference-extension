# Contributing to the docs

## mkdocs

This doc site is built using MkDocs.

Before you begin, make sure that you have a recent version of `python` and `pip`. You also might want to set up a Python virtual environment for the `gateway-api-inference-extension` project.

To install and use `mkdocs`, refer to the [MkDocs User Guide](https://www.mkdocs.org/user-guide/).

### Set up mkdocs

```sh
# Install mkdocs
pip install mkdocs

# Install the Material theme that this project uses
pip install mkdocs-material

# Install the plugins that this project uses
pip install mkdocs-awesome-pages-plugin
pip install mkdocs-macros-plugin
pip install mkdocs-mermaid2-plugin

```

### Preview local changes

1. Make your changes to the docs. If you add a new page, make sure to update the `nav` section in the `mkdocs.yml` file.

2. Serve the docs locally.

    `mkdocs serve`

3. Open the local address that the docs are served from in your browser: [http://127.0.0.1:8000/](http://127.0.0.1:8000/)

## Publish the docs

The project uses Netlify to host the docs. 

You can locally build the files that become the doc site. For example, you might want to check the HTML output of changes that you make to the site.

```sh
make build-docs-netlify
```

The Gateway API Inference Extension team will publish the docs based on the latest changes in the `main` branch.