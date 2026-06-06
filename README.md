# Robotic Review Notes

A structured, expandable robotics knowledge base that combines:

- Concept-focused pages for reading and reference
- Runnable Python notebook demos for interactive understanding
- Curated external resources with context

## Project Goals

- Keep topics organized and easy to navigate locally in a browser
- Support both narrative explanations and executable examples
- Make publishing to GitHub straightforward

## Core Stack

- Quarto: site container and navigation
- Jupyter + Python: executable demos and experiments

## Requirements

### 1) Quarto CLI

Install Quarto from the official docs:

- https://quarto.org/docs/get-started/

Verify installation:

```bash
quarto --version
```

### 2) Python

Recommended:

- Python 3.10 or newer

Verify:

```bash
python3 --version
```

### 3) Virtual Environment

From repository root:

```bash
python3 -m venv .venv
source .venv/bin/activate
python -m pip install --upgrade pip
pip install -r requirements.txt
```

### 4) Jupyter Kernel (optional but recommended)

```bash
python -m ipykernel install --user --name robotic-review --display-name "Python (robotic-review)"
```

## Run Locally

After Quarto and Python dependencies are installed:

```bash
quarto preview
```

This starts a local web server and opens a browser view with navigation.

Some pages include runtime widget controls (for example, map selector and connectivity toggles).
Those controls require `ipywidgets`, which is already listed in `requirements.txt`.

For fully editable, run-any-cell notebook workflow, use Jupyter Lab:

```bash
jupyter lab --no-browser --port 8888
```

Then open notebook URLs like:

- http://localhost:8888/lab/tree/notebooks/path-planning/<topic>/<demo>.ipynb

Important: rendered `.html` pages are static outputs and are not notebook editors.

## Build Static Site

```bash
quarto render
```

Generated site output is placed in the default Quarto output directory.

## Notes on Content Style

- Keep concept pages concise and cross-linked
- Keep demos small, runnable, and focused on one idea each
- For external references, include a short note on why each resource is useful
