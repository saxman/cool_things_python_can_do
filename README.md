# Cool Things Python Can Do

Python is one of the most expressive languages in existence; the same logic that takes ten lines in other languages often fits in one in Python, and it actually reads like English when you're done. This collection of notebooks is a hands-on tour of what makes Python worth knowing.

Each notebook focuses on a topic and shows you the elegant, idiomatic way to do things, not just *how* it works, but *why* it's better. The goal is to make you think "I didn't know Python could do that."

## What's Inside

### 01 - Python Standard Library
The features built into Python that most people underuse. Conditionals as expressions (`x if condition else y`), f-strings that call methods and format numbers inline, `math` and `statistics` functions that avoid common floating-point traps, and bit manipulation that makes flag operations clean and fast. These are the patterns that separate Python code that *works* from Python code that *reads well*.

### 02 - Python Lists
Lists are Python's workhorse, but most people only scratch the surface. List comprehensions replace verbose loops with single readable expressions. Slicing lets you reverse, sample, and step through sequences without writing a single index. `sorted` with a key function outperforms manual comparison in one argument. This notebook shows the full range of what lists can do when you know all the tools.

### 03 - Python Dictionaries
Dicts are O(1) lookup structures that can also replace `if/elif` chains, accumulate grouped data, and merge configurations with a single `|` operator (Python 3.9+). This notebook covers the full dict toolkit: comprehensions, safe access with `get` and `setdefault`, iteration over keys/values/items, sorting by value, nested dicts, and using a dict of functions as a dispatch table.

### 04 - Generators and Itertools
One of Python's most elegant features. A generator function produces values one at a time with `yield`; it computes a 100,000-element sequence in 200 bytes of memory instead of 800KB. `itertools` extends this with composable building blocks: infinite sequences, combinatorics (all combinations, permutations, or cartesian products in one call), running totals with `accumulate`, and grouped data with `groupby`. Things that take pages of code in other languages fit in a single expression here.

### 05 - Context Managers
The `with` statement guarantees cleanup (file closes, lock releases, DB rollbacks) even when exceptions occur, without a single `try/finally`. Writing a custom context manager with `contextlib.contextmanager` takes five lines and works for anything: timing blocks, temporary directory changes, patching attributes, capturing stdout. This notebook shows how to package any setup/teardown pattern into a reusable, clean interface.

### 06 - Object-Oriented Python
Python's OOP features go well beyond basic classes. Decorators transform functions without changing their code, and you'll learn how to write your own. `@property` makes attribute access run logic transparently. Dunder methods (`__repr__`, `__len__`, `__add__`) let your objects work with Python's built-in operators. `@dataclass` generates boilerplate-free data containers. Enums replace magic strings with safe, comparable constants. Abstract base classes enforce interfaces at definition time.

### 07 - Type Hints
Type hints don't change what Python does at runtime; they change what your tools can tell you before you run it. This notebook covers the full annotation system: function signatures, generics (`list[int]`, `dict[str, float]`), `Optional` and `Union` for values that might be absent, `Callable` for functions as arguments, `TypeVar` for generic functions, and `Protocol` for structural typing (duck typing with documentation). The payoff is code that self-documents and catches bugs before execution.

### 08 - Concurrency
Python has three distinct concurrency models, each suited to a different problem. `ThreadPoolExecutor` parallelises I/O-bound work (network calls, file reads) with minimal code. `asyncio` does the same with a single thread and cooperative scheduling; thousands of concurrent tasks, near-zero overhead. `ProcessPoolExecutor` breaks through the GIL for CPU-heavy work by running real parallel processes. This notebook shows all three and explains when to reach for each.

### 09 - Web Requests and Scraping
The web is the world's largest dataset. `requests` handles HTTP in one line: GET, POST, headers, authentication, sessions. BeautifulSoup turns raw HTML into a searchable tree: find elements by tag, class, or CSS selector; extract text, links, and attributes. Together they let you pull data from any page that a browser can see. The notebook works through real-world patterns including pagination and scraping a live site.

### 10 - Data Analysis with pandas
pandas is the reason Python became the language of data science. A DataFrame is a spreadsheet that you can filter, transform, group, and merge with code instead of clicks, and it scales to millions of rows without breaking a sweat. This notebook covers the full workflow: loading and inspecting data, boolean filtering, `groupby` aggregation, joining DataFrames, and handling missing values. Every operation is one method call.

### 11 - Numerical Computing with NumPy
NumPy arrays are 50–100× faster than Python lists for numerical work because operations run in compiled C, not interpreted Python. Broadcasting lets you add a 1D array to a 2D array without writing a loop. Universal functions (`ufunc`) apply math operations element-wise across entire arrays instantly. This notebook also covers aggregation along axes, reshaping, stacking, and linear algebra: the building blocks behind every scientific Python library.

### 12 - Visualization with Matplotlib
Numbers become insight when you can see them. Matplotlib turns NumPy arrays and pandas DataFrames into publication-quality charts with fine-grained control over every element. This notebook covers the chart types you'll use most (line, scatter, bar, histogram), multi-panel layouts with `subplots`, styling with colors and markers, annotating points of interest with arrows and text, and saving figures to disk, all using the object-oriented API that scales from quick plots to polished visuals.

### 13 - Scientific Computing with SciPy
SciPy picks up where NumPy leaves off. Statistical distributions and hypothesis tests in one function call. Numerical optimisation that finds the minimum of any function without calculus. Curve fitting that finds the parameters that best match your data. Numerical integration and ODE solvers for continuous systems. Interpolation for filling in gaps between measurements. This notebook shows Python doing the work of tools like MATLAB and R, built on the same NumPy arrays you already know.

### 14 - Machine Learning with scikit-learn
scikit-learn makes machine learning remarkably approachable: every algorithm (from logistic regression to random forests to k-means clustering) follows the same `fit`/`predict` interface. This notebook covers the full ML workflow: preprocessing features, building pipelines that prevent data leakage, cross-validation for honest accuracy estimates, and hyperparameter tuning with grid search. The goal is to demystify ML and show that the hard part is understanding your data, not the code.

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
