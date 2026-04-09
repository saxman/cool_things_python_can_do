# Cool Things Python Can Do

Most programmers learn Python. Far fewer learn to *use* it. The same logic that takes ten lines in other languages often fits in one in Python, and when done right, it reads like English. This collection of notebooks is a hands-on tour of what Python looks like when you actually know it.

Each notebook picks a topic and shows you the elegant, idiomatic way, not just *how* it works, but *why* it's better. The goal is to make you think "I didn't know Python could do that."

## What's Inside

### 01 - Python Standard Library
Most Python developers use maybe 20% of what's already installed. Before you reach for a library, the standard library probably already does what you need, often better. Conditionals as expressions, f-strings that call methods and format numbers inline, `math` and `statistics` functions that sidestep floating-point traps, and bit manipulation that makes flag operations clean and instant. These are the patterns that separate Python that *works* from Python that *reads well*.

### 02 - Python Lists
Lists are Python's workhorse, but most people only scratch the surface. A single list comprehension replaces five lines of `append` logic. Slicing reverses, samples, and steps through sequences without a single explicit index. `sorted` with a key function outperforms manual comparison in one argument. Once you've seen the full toolkit, you'll wonder how you wrote list code any other way.

### 03 - Python Dictionaries
Dicts are O(1) lookup structures, but that's just the start. They can replace entire `if/elif` chains, accumulate grouped data in one pass, and merge configurations with a single `|` operator (Python 3.9+). This notebook covers the full toolkit: comprehensions, safe access with `get` and `setdefault`, sorting by value, nested dicts, and using a dict of functions as a dispatch table that scales better than any switch statement.

### 04 - Generators and Itertools
Here's a trick: a generator that produces 100,000 numbers uses 200 bytes of memory. The equivalent list uses 800KB. Generators compute values on demand: no waiting, no waste. `itertools` extends this with composable building blocks: infinite sequences, all combinations or permutations in a single call, running totals with `accumulate`, grouped data with `groupby`. Things that take pages of code in other languages fit in a single expression here.

### 05 - Context Managers
The `with` statement guarantees cleanup (file closes, lock releases, database rollbacks) even when exceptions blow up mid-function, without a single `try/finally`. A custom context manager takes five lines with `contextlib.contextmanager` and works for anything: timing blocks, temporary directory changes, patching attributes, capturing stdout. If you're still writing setup/teardown by hand, this notebook will change that permanently.

### 06 - Object-Oriented Python
Python's OOP goes well beyond basic classes, and the interesting parts are what most tutorials skip. Decorators transform functions without touching their code, and you'll learn to write your own. `@property` makes attribute access run logic transparently. Dunder methods (`__repr__`, `__len__`, `__add__`) let your objects work with Python's built-in operators as if they were native types. `@dataclass` kills boilerplate. Enums replace magic strings. Abstract base classes enforce contracts at definition time.

### 07 - Type Hints
Type hints don't change what Python does at runtime. They change what your tools can tell you *before* you run it. Catch a `None` dereference before it happens. Document what a function accepts without writing prose. This notebook covers the full system: function signatures, generics (`list[int]`, `dict[str, float]`), `Optional` and `Union`, `Callable` for functions-as-arguments, `TypeVar` for generic functions, and `Protocol` for structural typing (duck typing with documentation). Your future self will thank you.

### 08 - Concurrency
Three concurrency models. Most developers only know one. `ThreadPoolExecutor` parallelises I/O-bound work (network calls, file reads) with minimal code changes. `asyncio` handles thousands of concurrent tasks on a single thread with near-zero overhead. `ProcessPoolExecutor` breaks through the GIL for genuinely CPU-heavy work with real parallel processes. This notebook shows all three, when each one shines, and what happens when you pick the wrong one.

### 09 - Functional Programming
Python treats functions as first-class objects: pass them, return them, compose them. `functools` builds on this with tools that make the pattern shine. `partial` freezes some arguments so you can reuse a function across contexts. `lru_cache` turns any pure function into a memoised lookup in one decorator: recursive Fibonacci becomes instant. `wraps` preserves the metadata your decorators would otherwise destroy. `total_ordering` derives all six comparison methods from just two. Pair these with `map`, `filter`, and `sorted`'s `key=` argument and you get expressive, composable code with no loops in sight.

### 10 - Regular Expressions
The `re` module gives Python a full regular-expression engine. A single pattern can validate an email address, extract all phone numbers from a document, or reformat every date in a file, faster and more precisely than any string method chain. This notebook covers the full toolkit: `search`, `match`, `findall`, `finditer`, capture groups, named groups, `sub` with a replacement function, lookahead and lookbehind assertions, flags (`re.IGNORECASE`, `re.MULTILINE`, `re.DOTALL`), compiled patterns, and `re.VERBOSE` for patterns readable enough to maintain.

### 11 - Structural Pattern Matching
Added in Python 3.10, `match`/`case` is not a switch statement. It matches the *structure* of data: sequences by length and position, mappings by key, class instances by attribute, and literals by value. Guards let you add `if` conditions inline. Nested patterns handle deeply structured data (JSON responses, AST nodes, protocol messages) in a single readable block that would otherwise be an `isinstance` chain wrapped in loops. If you work with heterogeneous data, this changes how you write dispatch logic.

### 12 - pathlib and File IO
`pathlib.Path` replaces `os.path` with an object-oriented interface that composes naturally. Build paths with `/`, navigate with `.parent`, glob with `.glob('**/*.py')`, and read or write with a single method call. This notebook pairs `pathlib` with the full standard-library I/O toolkit: `json` for structured data, `csv.DictReader`/`DictWriter` for tabular data, `pickle` for arbitrary Python objects, `tempfile` for safe temporary files, and `shutil` for copying, moving, and deleting entire directory trees. Every pattern you need to read and write files without touching `open` by hand.

### 13 - Logging and Debugging
`print` statements are not a logging strategy. The `logging` module gives you severity levels, named loggers, multiple simultaneous destinations, and hierarchical namespaces, so library code and application code each control their own output without interfering. This notebook covers the idiomatic setup (`logger = logging.getLogger(__name__)`), handlers and formatters, routing warnings to file and errors to console simultaneously, and logging exceptions with full tracebacks. Then `breakpoint()` for interactive debugging, and the `traceback` module for programmatic introspection of exceptions.

### 14 - Testing with pytest
Untested code is code that only works by accident. pytest is Python's most popular testing framework: write plain functions that start with `test_`, use plain `assert`, and pytest finds and runs them all. No subclassing `TestCase`, no `self.assertEqual`. Fixtures handle setup and teardown with a dependency-injection model that keeps tests independent. `parametrize` runs the same test against a table of inputs in one decorator. `unittest.mock` patches out network calls, filesystems, and external services so your tests are fast and deterministic even without the real thing.

### 15 - Building CLI Tools
Python is an excellent scripting language, and `argparse` makes it easy to turn a script into a proper CLI with named options, type validation, subcommands, and auto-generated `--help`. For more user-friendly interfaces, `click` replaces the parser setup with decorators: `@click.command()`, `@click.option()`, `@click.argument()`. Commands compose into groups, output styling is built in, and testing is straightforward. This notebook covers both, so you can pick the right tool for the job.

### 16 - Database Access
Python's `sqlite3` module ships a fully relational database with no installation required: connect, create tables, insert rows, and query, all from the stdlib. For production databases (PostgreSQL, MySQL, or still SQLite), SQLAlchemy adds a unified API, a composable SQL expression language, and a full ORM with declarative models, sessions, and relationships. Write your model once and SQLAlchemy handles the SQL. This notebook covers both layers, from raw cursor operations to a complete ORM workflow.

### 17 - Web Requests and Scraping
The web is the world's largest dataset, and most of it is freely accessible if you know how to ask. `requests` handles HTTP in one line: GET, POST, headers, authentication, sessions. BeautifulSoup turns raw HTML into a searchable tree: find elements by tag, class, or CSS selector; extract text, links, and attributes. Together they let you pull data from any page a browser can see. The notebook works through real-world patterns including pagination and a live scrape.

### 18 - Data Analysis with pandas
pandas is a big reason Python became the language of data science. A DataFrame is a spreadsheet you control entirely with code: filter rows with a boolean expression, group and aggregate in one call, join two tables like SQL, handle missing values without a plugin. It scales to millions of rows without breaking a sweat. This notebook covers the full workflow: loading, inspecting, filtering, transforming, groupby, merging, and missing data. Every step is one method call.

### 19 - Numerical Computing with NumPy
NumPy arrays are 50–100× faster than Python lists for numerical work because operations run in compiled C, not interpreted Python. And you never write a loop. Broadcasting lets you add a 1D array to a 2D array and Python figures out the shape. Universal functions apply math operations element-wise across entire arrays instantly. This notebook covers aggregation along axes, reshaping, stacking, and linear algebra, the building blocks that every scientific Python library is built on.

### 20 - Visualization with Matplotlib
Numbers become insight when you can see them. Matplotlib turns NumPy arrays and pandas DataFrames into publication-quality charts with fine-grained control over every element. Line plots, scatter plots, bar charts, histograms, multi-panel layouts, all built with the object-oriented API that scales from a quick exploratory plot to a polished visual ready for a paper or presentation. Including annotations, custom styles, and saving to disk.

### 21 - Scientific Computing with SciPy
SciPy is where Python stops being a scripting language and starts being a scientific computing platform. Statistical distributions and hypothesis tests in one function call. Numerical optimisation that finds the minimum of any function without calculus. Curve fitting that extracts parameters from noisy data. Numerical integration and ODE solvers for continuous systems. Interpolation for filling gaps between measurements. This notebook shows Python doing the work of MATLAB and R, built on NumPy arrays you already know.

### 22 - Machine Learning with scikit-learn
Every algorithm in scikit-learn (logistic regression, random forests, k-means, SVMs) shares the same three-method interface: `fit`, `predict`, `score`. Swap one model for another in a single line. This notebook covers the full ML workflow: preprocessing features, building pipelines that physically prevent data leakage, cross-validation for honest accuracy estimates, and grid search for hyperparameter tuning. The hard part of ML is understanding your data. The code part doesn't have to be.

---

## Getting Started

You'll need Python 3 and pip installed. Then:

```bash
# Clone the repo and enter the project directory
python -m venv .venv
source .venv/bin/activate
pip install jupyterlab
jupyter lab
```

Jupyter Lab will open in your browser. Click any notebook to start exploring.
