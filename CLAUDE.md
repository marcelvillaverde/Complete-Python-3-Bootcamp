# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Purpose

This is the **Complete Python 3 Bootcamp** course repository by Pierian Data, containing curriculum materials for a Udemy course. It is purely educational — there is no application to build or deploy, no package to install, and no CI pipeline.

## Running Notebooks

All learning content lives in Jupyter notebooks (`.ipynb`). To work interactively:

```bash
jupyter notebook
```

Individual notebooks can also be executed non-interactively:

```bash
jupyter nbconvert --to notebook --execute "00-Python Object and Data Structure Basics/01-Numbers.ipynb"
```

## Running Tests

The only test file in the repo is a unit testing demonstration in section 07:

```bash
# From the repo root
python -m pytest "07-Errors and Exception Handling/test_cap.py"

# Or with unittest directly
python -m unittest "07-Errors and Exception Handling/test_cap.py"
```

`test_cap.py` imports `cap.py` from the same directory — both must be present for the tests to pass.

## Repository Structure

Content is organized into 20 numbered sections that follow a progressive curriculum arc:

| Range | Topics |
|-------|--------|
| 00–03 | Core language: data types, operators, control flow, functions |
| 04 | Milestone Project 1 (capstone exercises) |
| 05–06 | OOP, modules and packages |
| 07 | Errors, exceptions, and unit testing |
| 08 | Milestone Project 2 |
| 09–11 | Built-ins, decorators, generators |
| 12 | Advanced standard library modules (collections, regex, datetime, etc.) |
| 13–16 | External integrations: web scraping, images, PDFs/CSVs, email |
| 17 | Advanced data structures |
| 18 | Milestone Project 3 |
| 19 | Bonus: Jupyter widgets / GUIs |

Each section typically contains three notebook types:
- **Lecture notebooks** — instructional content with embedded output
- **Exercise notebooks** — blank or partially filled problems for students
- **Solution notebooks** — completed answers (usually suffixed with `-Solutions`)

## Key Conventions

- **No external dependencies are tracked.** Students install packages as needed per section (e.g., `Pillow` for section 14, `requests`/`BeautifulSoup4` for section 13). There is no `requirements.txt`.
- **`.ipynb_checkpoints/`** directories are Jupyter auto-saves — ignore them when searching for content.
- **Python `.py` files** in the repo are teaching examples (demonstrating module imports, package structure, or unit testing), not application code.
- **Section 06** contains a deliberately constructed package (`MyMainPackage/`) used to teach `__init__.py` and relative imports — edits there should preserve that didactic structure.
- Notebook cell outputs are intentionally committed so students can preview results without running code.
