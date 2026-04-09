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
| 09 - Functional Programming | map, filter, sorted key=, functools (partial, reduce, lru_cache, wraps, total_ordering), operator | Complete |
| 10 - Regular Expressions | search, match, findall, finditer, sub, groups, named groups, lookahead, flags, re.VERBOSE | Complete |
| 11 - Structural Pattern Matching | match/case literals, sequences, mappings, classes, guards, nested patterns, OR pattern | Complete |
| 12 - pathlib and File IO | pathlib.Path, read_text/write_text, glob, JSON, CSV, pickle, tempfile, shutil | Complete |
| 13 - Logging and Debugging | logging levels, named loggers, handlers, formatters, exc_info, breakpoint(), pdb, traceback | Complete |
| 14 - Testing with pytest | test functions, pytest.raises, fixtures, parametrize, unittest.mock (patch, MagicMock), tmp_path | Complete |
| 15 - Building CLI Tools | sys.argv, argparse (positional, options, flags, subcommands), click (commands, groups, styling) | Complete |
| 16 - Database Access | sqlite3 (connect, execute, row_factory), SQLAlchemy Core, SQLAlchemy ORM (declarative models) | Complete |
| 17 - Web Requests and Scraping | HTTP with requests, HTML parsing with BeautifulSoup, live scraping patterns | Complete |
| 18 - Data Analysis with pandas | DataFrames, filtering, groupby, merging, missing data | Complete |
| 19 - Numerical Computing with NumPy | Arrays, broadcasting, ufuncs, aggregation, reshaping, linear algebra | Complete |
| 20 - Visualization with Matplotlib | Line/scatter/bar/histogram, subplots, styling, annotations, saving, NumPy/pandas integration | Complete |
| 21 - Scientific Computing with SciPy | Stats, optimisation, curve fitting, numerical integration, ODEs, interpolation, linalg | Complete |
| 22 - Machine Learning with scikit-learn | Classification, regression, clustering, preprocessing, pipelines, model selection | Complete |

## Content Conventions

- Each notebook is organized into numbered sections covering related features
- Sections contain short, standalone code cells demonstrating one concept at a time
- Markdown cells provide section headers and brief context; code cells do the teaching
- Every notebook begins with an intro markdown cell: title, what's covered, why it's interesting, and "Learn more" links
- Notebooks with external dependencies include a `## Setup` section immediately after the intro, containing a single `%pip install` code cell

## Dependencies

Notebooks 01–13 use only the Python standard library. Notebooks with external dependencies:

| Notebook | pip install |
|---|---|
| 14 - Testing with pytest | `pytest pytest-asyncio` |
| 15 - Building CLI Tools | `click` |
| 16 - Database Access | `sqlalchemy` |
| 17 - Web Requests and Scraping | `requests beautifulsoup4` |
| 18 - Data Analysis with pandas | `pandas` |
| 19 - Numerical Computing with NumPy | `numpy` |
| 20 - Visualization with Matplotlib | `matplotlib numpy pandas` |
| 21 - Scientific Computing with SciPy | `scipy numpy` |
| 22 - Machine Learning with scikit-learn | `scikit-learn numpy pandas` |
