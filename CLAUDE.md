# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Purpose

A collection of Jupyter notebooks demonstrating idiomatic Python 3: concise, efficient, "Pythonic" patterns inspired by the [Zen of Python](https://en.wikipedia.org/wiki/Zen_of_Python). This is a learning and reference resource, not a library or application.

## Setup & Running

```bash
python -m venv .venv
source .venv/bin/activate
pip install jupyterlab
jupyter lab
```

## Notebook Structure

Notebooks are numbered sequentially by topic:

| Notebook | Topic | Status |
|---|---|---|
| 01 - Python Standard Library | Conditionals, strings, math, bit ops | Complete |
| 02 - Python Lists | Creating, accessing, modifying, sorting, comprehensions | Complete |
| 03 - Python Dictionaries | Creating, comprehensions, merging, get/setdefault, iterating, nested dicts, dispatch tables | Complete |
| 04 - Generators and Itertools | yield, generator expressions, infinite iterators, chain, combinatorics, groupby, accumulate | Complete |
| 05 - Context Managers | with mechanics, __enter__/__exit__, contextlib.contextmanager, suppress, ExitStack | Complete |
| 06 - Object-Oriented Python | Classes, inheritance, decorators, properties, dunder methods, dataclasses, enums, ABCs | Complete |
| 07 - Type Hints | Variable/function annotations, generics, Optional, Callable, TypeVar, Protocol | Complete |
| 08 - Concurrency | ThreadPoolExecutor, asyncio (async/await, gather), ProcessPoolExecutor, choosing the right model | Complete |
| 09 - Web Requests and Scraping | HTTP with requests, HTML parsing with BeautifulSoup, live scraping patterns | Complete |
| 10 - Data Analysis with pandas | DataFrames, filtering, groupby, merging, missing data | Complete |
| 11 - Numerical Computing with NumPy | Arrays, broadcasting, ufuncs, aggregation, reshaping, linear algebra | Complete |
| 12 - Visualization with Matplotlib | Line/scatter/bar/histogram, subplots, styling, annotations, saving, NumPy/pandas integration | Complete |
| 13 - Scientific Computing with SciPy | Stats, optimisation, curve fitting, numerical integration, ODEs, interpolation, linalg | Complete |
| 14 - Machine Learning with scikit-learn | Classification, regression, clustering, preprocessing, pipelines, model selection | Complete |

## Content Conventions

- Each notebook is organized into numbered sections covering related features
- Sections contain short, standalone code cells demonstrating one concept at a time
- Markdown cells provide section headers and brief context; code cells do the teaching
- Every notebook begins with an intro markdown cell: title, what's covered, why it's interesting, and "Learn more" links
- Notebooks with external dependencies include a `## Setup` section immediately after the intro, containing a single `%pip install` code cell

## Dependencies

Notebooks 01–08 use only the Python standard library. Notebooks with external dependencies:

| Notebook | pip install |
|---|---|
| 09 - Web Requests and Scraping | `requests beautifulsoup4` |
| 10 - Data Analysis with pandas | `pandas` |
| 11 - Numerical Computing with NumPy | `numpy` |
| 12 - Visualization with Matplotlib | `matplotlib numpy pandas` |
| 13 - Scientific Computing with SciPy | `scipy numpy` |
| 14 - Machine Learning with scikit-learn | `scikit-learn numpy pandas` |
