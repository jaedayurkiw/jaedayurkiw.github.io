# jaedayurkiw.github.io

My personal website and blog for DSCI 521. It includes a Python post and an R post with numbers and figures that were produced by code that ran at render time.

## What to install first 

These are the versions I used:

- [Quarto](https://quarto.org/docs/get-started/) 1.10.18
- [uv](https://docs.astral.sh/uv/getting-started/installation/) 0.12.7
  (uv installs Python 3.14 for you)
- [R](https://cran.r-project.org/) 4.6.1
- git

You do not need to install renv; it bootstraps itself.

## Building the site 

### 1. Clone the repository (in the terminal)

```bash
git clone https://github.com/jaedayurkiw/jaedayurkiw.github.io.git
cd jaedayurkiw.github.io
```

### 2. Install Python packages (in the terminal, in the repository folder)

```bash
uv sync
```

### 3. Install the R packages (in R, started from the repositroy folder)

Start R from the repository folder:

```bash
R
```

renv starts automatically. Then run:

```r
renv::restore()
```

Type `y` when asked to proceed. When it finishes, quit R:

```r
q()
```

Type `n` when asked to save the workspace.

### 4. Render the site (in the terminal, in the repository folder)

```bash
uv run quarto render
```

## Vieweing the site

The built site is saved in the `docs/` folder. To open it locally, run this
in the terminal from the repository folder (`jaedayurkiw.github.io`):

```bash
open docs/index.html
```

On Windows, open `docs/index.html` in a browser instead. The live site is at
https://jaedayurkiw.github.io.

## Data 

- **Python post** (`posts/penguins-python/`): the
  [Palmer Penguins](https://allisonhorst.github.io/palmerpenguins/) data (CC0),
  loaded from the `palmerpenguins` Python package, installed by `uv sync`.
- **R post** (`posts/gapminder-r/`): the
  [gapminder](https://cran.r-project.org/package=gapminder) data (CC0), loaded
  from the `gapminder` R package, installed by `renv::restore()`.

## Use of AI

I used Claude (Anthropic's AI assistant) to help me understand the assignment requirements, set up the `uv` and `renv` environments, 
fix errors in my code and Git workflow, and help with the the pandas, dplyr, and ggplot2 syntax. It also helped guide me through making 
the README template and citing the penguins and gapminder data sets.

