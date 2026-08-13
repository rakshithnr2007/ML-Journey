# 02. Pandas Basics 🐼

This section covers my practice and notes on **Pandas**, the go-to library 
for data manipulation and analysis in Python — built on top of NumPy and 
essential for handling real-world, tabular datasets.

## ✅ Concepts Learnt
- Importing NumPy and Pandas together
- Creating a DataFrame from a dictionary
- Reading & saving data: `pd.read_csv()`, `df.to_csv()`
- Quick data inspection: `df.head()`, `df.tail()`, `df["col"].describe()`
- Setting a custom index (`df.index = [...]`)
- Creating a `pd.Series()` from a random NumPy array
- Creating a DataFrame directly from a NumPy array
- Core DataFrame attributes/methods: `.head()`, `.describe()`, `.index`, `.columns`
- Converting a DataFrame back to a NumPy array with `.to_numpy()`
- Transposing a DataFrame with `.T`
- Sorting by index using `.sort_index()`
- **View vs Copy** — understanding that plain assignment (`newdf2 = newdf`) creates a view sharing memory (editing one affects the other), while `df.copy()` creates a fully independent object
- Dropping rows and columns using `drop()`, and the difference between `axis=0` (rows) and `axis=1` (columns)
- **Accessing data with `loc` vs `iloc`** — `loc` is label/condition-based indexing (`loc[[rows],[cols]]`, conditional filtering), while `iloc` is purely position-based indexing
- **Saving modifications safely** — understanding that `drop()` alone doesn't change the original DataFrame unless you reassign it (`newdf = newdf.drop(...)`) or use `inplace=True`
- Resetting index using `reset_index(drop=True, inplace=True)`
- Modifying a specific column safely using `.loc`
- Counting unique values with `df["col"].value_counts()`

