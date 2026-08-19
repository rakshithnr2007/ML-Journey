# Pandas Basics 🐼

Documentation of core **Pandas** concepts in Python, covering how to create, read, modify, and analyze tabular data using DataFrames and Series.

## What's inside

The notebook (`pandas_basics.ipynb`) covers:

- **Creating a DataFrame** – from a dictionary, and from a NumPy array
- **Reading & Saving Data** – `to_csv()`, `read_csv()`, `head()`, `tail()`, `describe()`
- **Series** – creating a Pandas Series from random NumPy values
- **DataFrame Basics** – `.index`, `.columns`, `.to_numpy()`, `.T` (transpose), `.sort_index()`
- **View vs Copy** – understanding shared memory between DataFrames, and using `.copy()` to avoid unwanted side effects
- **Dropping Rows & Columns** – using `.drop()` with `axis=0` / `axis=1`
- **Accessing Data** – difference between `.loc[]` (label-based) and `.iloc[]` (position-based), including conditional filtering
- **Saving Modifications Safely** – difference between a preview operation and reassigning/`inplace=True`, plus a common beginner bug around `inplace=True` returning `None`
- **Resetting the Index** – `.reset_index()`
- **Counting Values** – `.value_counts()`
- **Pivot Table** – reshaping data with `index`, `columns`, `values`, and `aggfunc`

---
⭐ If this helped you, consider starring the repo!
