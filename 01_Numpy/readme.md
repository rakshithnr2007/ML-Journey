# 01. NumPy Basics 🔢

This section covers my practice and notes on **NumPy**, the core library 
for numerical computing in Python and the foundation for most ML/data 
science workflows.

## ✅ Concepts Learnt
- Introduction to NumPy arrays (`ndarray`) and why they're faster than lists
- Creating arrays: `np.array()`, `np.zeros()`, `np.ones()`, `np.arange()`, `np.linspace()`
- Array attributes: `shape`, `ndim`, `size`, `dtype`
- 1D, 2D, and 3D array creation and understanding dimensions
- Indexing and slicing arrays
- Reshaping arrays with `reshape()`, `ravel()`, `flatten()`
- Basic arithmetic operations on arrays (element-wise +, -, *, /)
- Broadcasting rules
- Aggregate functions: `sum()`, `mean()`, `min()`, `max()`, `std()`, `var()`
- Sorting arrays with `np.sort()`
- Random number generation: `np.random.rand()`, `randint()`, `randn()`
- Stacking and splitting arrays: `hstack()`, `vstack()`, `split()`

## 🔜 Next Up
- Vectorization and why it replaces explicit loops for performance
- Fancy indexing and boolean masking for conditional data selection
- Linear algebra operations using `np.linalg` (dot product, matrix multiplication, determinant, inverse)
- Handling missing values with `np.nan`
- Structured/record arrays
- Memory views vs copies when slicing
- `np.where()` and conditional array operations
- Concatenation and array joining techniques
- Working with `np.unique()` and set-like operations
- Saving and loading arrays (`np.save()`, `np.load()`)

## Why It Matters
NumPy arrays are faster and more memory-efficient than regular Python 
lists, and almost every ML library (Pandas, Scikit-learn, TensorFlow) 
is built on top of NumPy — making it an essential first step.

