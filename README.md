# obsidian-workflow-template-docs

This is the documentation for my [obsidian-workflow-template](https://github.com/mathisgauthey/obsidian-workflow-template) project.

## Technology used

I'm using [MkDocs](https://www.mkdocs.org/) with the [Material theme](https://squidfunk.github.io/mkdocs-material/).

It has a wonderful documentation and is very customizable.

## Requirements

```bash
pip install mkdocs
pip install mkdocs-material
```

Don't forget the `sudo` before on linux, otherwise you might run into possible errors related to `command not found`.

## Usage

MkDocs includes a live preview server, so you can preview your changes as you write your documentation. The server will automatically rebuild the site upon saving. Start it with:

```bash
mkdocs serve
```

When you're finished editing, you can build a static site from your Markdown files with:

```bash
mkdocs build
```
