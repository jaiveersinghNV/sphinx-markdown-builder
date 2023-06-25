# sphinx-markdown-builder

[![Coverage Status](https://coveralls.io/repos/github/liran-funaro/sphinx-markdown-builder/badge.svg?branch=main)](https://coveralls.io/github/liran-funaro/sphinx-markdown-builder?branch=main)

Sphinx builder that generates markdown files from reStructuredText.

## Install

```sh
pip3 install sphinx-markdown-builder==0.5.5
```


## Usage

Add the extension to your `conf.py` file:
```python
extensions = [
    ...,
    "sphinx_markdown_builder",
    ...,
]
```

Build markdown files with `sphinx-build` command
```sh
sphinx-build -M markdown ./docs ./build
```

## Configurations

You can add the following configurations to your `conf.py` file:

* `markdown_http_base`: If set, all references will link to this prefix address
* `markdown_uri_doc_suffix`: If set, all references will link to documents with this suffix.
* `markdown_anchor_sections`/`markdown_anchor_signatures`: If set to `True`, then anchors will be added before each section/function/class signature. 
 This allows references to a specific anchor in the document.

For example, if your `conf.py` file have the following configuration:
```python
markdown_http_base = "https://your-domain.com/docs"
markdown_uri_doc_suffix = ".html"
```

Then a reference to `your-doc-name#your-header` will be substituted with `https://your-domain.com/docs/your-doc-name.html#your-header`. 

## Credits
This project forked from [
sphinx-markdown-builder](https://github.com/clayrisser/sphinx-markdown-builder), which was developed by [Clay Risser](https://github.com/clayrisser) under the [MIT](https://github.com/clayrisser/sphinx-markdown-builder/blob/master/LICENSE) license.

The original implementation was based on [doctree2md](https://github.com/matthew-brett/nb2plots/blob/master/nb2plots/doctree2md.py) by [Matthew Brett](https://github.com/matthew-brett) under the [BSD-2](https://github.com/matthew-brett/nb2plots/blob/main/LICENSE) license.

## License

[MIT](LICENSE)
