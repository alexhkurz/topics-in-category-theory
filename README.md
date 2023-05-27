# README

Created from [this template](https://github.com/alexhkurz/template-for-jupyter-book).

To make the book locally and open it in my browser, I run (the `open` command may be specific to a mac)

```
jb build . ; open _build/html/index.html
```

To publish the book, install `ghp-import` with `pip install ghp-import`. Then run 

```
ghp-import -n -p -f _build/html
```

This makes the [book available online](https://alexhkurz.github.io/topics-in-category-theory). It also keeps the source files in the `main`-branch separate from the files in `_build` in the `gh-pages` branch (Github knows that it should use the `gh-pages` branch to show the book as a webpage).

If the table of contents in the left-hand pane behaves in a strange way, clean out `_build` by running `jb clean .`

