# sarika020.github.io


My personal website and blog, built with Quarto. It includes a home page, an about me and a blog containing three posts-
one post about my first week in UBC and two computational posts(one in Python and one in R.)

## Install first

- [Quarto](https://quarto.org/docs/get-started/) (version 1.10.18)
- [uv](https://docs.astral.sh/uv/) (version 0.12.5)
- [R](https://cran.r-project.org/) (version 4.6.1)

uv installs Python 3.14 automatically, and renv installs itself.

## Build the site

Run these in a terminal:

```
git clone https://github.com/sarika020/sarika020.github.io.git
cd sarika020.github.io
uv sync
Rscript -e "renv::restore()"
uv run quarto render
```

Always run `quarto render` from the top folder of the repository.

## View the site

The built site is in `docs/`. Open `docs/index.html` in a browser.

## Data

Both posts use the [Palmer Penguins](https://allisonhorst.github.io/palmerpenguins/)
dataset, which comes with the `palmerpenguins` package in Python and R.
It installs with the packages, so the build doesn't download any extra data.

The data comes with the `palmerpenguins` package, so rendering needs no
network access. Installing the packages with `uv sync` and
`renv::restore()` does need internet.