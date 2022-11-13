# SaaS Cookbook

## Security

See [CONTRIBUTING](CONTRIBUTING.md#security-issue-notifications) for more information.

## License

This library is licensed under the MIT-0 License. See the LICENSE file.

## Writing recipes

To write recipes we're using [MkDocs][mkdocs] with the [Material][mkdocs-material]
theme. MkDocs is a static site generator, converting the Markdown files you
edit to static HTML pages which are then served as via GitHub pages

### Local preview

In order to locally preview the recipes site you need to have MkDocs installed:

* Make sure to upgrade pip installer
```
pip3 install --upgrade pip
pip --version
```

* Install mkdocs
```
pip install mkdocs
```

* Validate mkdocs setup
```
pip check mkdocs
pip show mkdocs
```

* Depending on python version and OS configuration, execute mkdocs by running one of the following commands
```
$ python -m mkdocs [OPTIONS] COMMAND [ARGS]...
```
```
$ mkdocs [OPTIONS] COMMAND [ARGS]...
```

Further, we depend on the Material theme and some plugins you can install as follows:

```
pip install mkdocs-material mkdocs-awesome-pages-plugin mkdocs-macros-plugin
```

To generate a local preview do:

```
$ mkdocs serve
INFO     -  Building documentation...
INFO     -  Cleaning site directory
...
```

Now head over to `http://127.0.0.1:8000/aws-saas-factory.github.io/` where you should
find the local preview of the  site.

If you are looking for formatting tips, check out the [Material theme
reference][material-formatting].

**IMPORTANT** Before you send in a PR, make sure that the local preview with
`mkdocs serve` renders OK, that is, all images are shown and the rest of the
formatting, such as code, displays as you would expect.

### Publishing

Once you PR the repo, we will review and test the recipes and the merge of
your PR kicks of a [GitHub action][publishing-ghaction] that publishes your 
recipe automatically.

[mkdocs]: https://www.mkdocs.org/
[mkdocs-material]: https://squidfunk.github.io/mkdocs-material/
[material-formatting]: https://squidfunk.github.io/mkdocs-material/reference/formatting/