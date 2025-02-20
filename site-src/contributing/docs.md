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
pip install mkdocs-spellcheck

```

### Preview local changes

1. Make your changes to the docs. If you add a new page, make sure to update the `nav` section in the `mkdocs.yml` file.

2. Serve the docs locally.
   
    `mkdocs serve`

3. Open the local address that the docs are served from in your browser: [http://127.0.0.1:8000/](http://127.0.0.1:8000/)

## Spellcheck

The project uses [MkDocs SpellCheck](https://pawamoy.github.io/mkdocs-spellcheck/).

1. Install the spellcheck with the backends. The ticks are added for shells that otherwise interpret the `[]` as a command.

    `pip install 'mkdocs-spellcheck[codespell]' && pip install 'mkdocs-spellcheck[symspellpy]'`

2. Build the docs to trigger the spellcheck.

    `mkdocs build`

3. Review the output for `mkdocs_spellcheck` warnings, such as the following example. Notice that the output includes the file name, mispelled word, and suggestions.

    `WARNING -  mkdocs_spellcheck: (symspellpy) index.md: Misspelled 'dont', did you mean 'done'...?`

4. If the word is correct, you can update the [`site-src/known_words.txt` file](../known_words.txt).    

## Publish the docs

The project uses Netlify to host the docs. 

You can locally build the files that become the doc site. For example, you might want to check the HTML output of changes that you make to the site.

```sh
make build-docs-netlify
```

The Gateway API Inference Extension team will publish the docs based on the latest changes in the `main` branch.
