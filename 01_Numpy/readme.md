# 🔢 NumPy Learning Notes

A collection of hands-on NumPy notebooks built while learning the essentials needed for Data Science and Machine Learning.
They go from creating your first array, through indexing, broadcasting and math/statistics, to practical tricks and small ML helpers (sigmoid, MSE).
Every function listed below was actually practiced in a notebook, so this README doubles as a quick reference.
Learning path: **NumPy → Pandas → Data Analysis → Machine Learning**.

---

## 📑 What's Inside

1. [numpy_Basics.ipynb](#1-numpy_basicsipynb): covers the basic topics: creating arrays, attributes, indexing, axis, reshaping, simple matrix operations and memory usage.
2. [Numpy_Depth.ipynb](#2-numpy_depthipynb): covers the important core topics in depth: math and statistics functions, slicing, fancy and Boolean indexing, stacking, broadcasting, missing values, and ML formulas (sigmoid, MSE).
3. [Numpy_tricks.ipynb](#3-numpy_tricksipynb): covers handy extras: sorting, searching, cumulative operations, percentiles, correlation, set operations and other useful one-liners.
4. [Array Attributes & Methods (reference)](#4-array-attributes--methods-reference): a lookup sheet of every `ndarray` attribute and method.

<br>

<sub><sup>Small tag at the end of a row = cell number(s) where it appears (1-based position in the notebook, counting markdown cells too).</sup></sub>

---

## 1. `numpy_Basics.ipynb`

Core concepts: creating arrays, indexing, axis, reshaping, and basic matrix operations.

### Array Creation & Attributes
| Function / Attribute | Description |
|---|---|
| `np.array()` | Creates an array from a Python list (1D, 2D or 3D). <sub><sup>cells 4, 15, 19, 33, 39, 47, 48, 63</sup></sub> |
| `.dtype` | Data type of the elements. <sub><sup>cells 6, 67</sup></sub> |
| `.shape` | Tuple of the size of each dimension. <sub><sup>cells 7, 21</sup></sub> |
| `.size` | Total number of elements. <sub><sup>cells 8, 20, 66</sup></sub> |
| `.ndim` | Number of dimensions. <sub><sup>cells 9, 22, 42</sup></sub> |

### Indexing & Slicing
| Concept | Description |
|---|---|
| `arr[0]` | Access an element by index. <sub><sup>cell 5</sup></sub> |
| `arr[1:]` | Slice from an index to the end. <sub><sup>cell 11</sup></sub> |
| `arr[-1]` | Negative indexing: last element. <sub><sup>cell 12</sup></sub> |
| `arr[::-1]` | Reverse the array. <sub><sup>cell 13</sup></sub> |

### NumPy Axis
| Function | Description |
|---|---|
| `sum(axis=0)` | Sums down the columns. <sub><sup>cell 16</sup></sub> |
| `sum(axis=1)` | Sums across the rows. <sub><sup>cell 17</sup></sub> |

### Intrinsic Array Creation Functions
| Function | Description |
|---|---|
| `np.zeros()` | Array filled with zeros (with a chosen dtype, e.g. `np.int8`). <sub><sup>cell 24</sup></sub> |
| `np.arange()` | Evenly spaced values within a range (like `range`). <sub><sup>cells 25, 30</sup></sub> |
| `np.linspace()` | Fixed number of equally spaced values between two points. <sub><sup>cell 26</sup></sub> |
| `np.empty()` | Array with uninitialized (garbage) values; fastest to create. <sub><sup>cell 27</sup></sub> |
| `np.identity()` | Square identity matrix. <sub><sup>cell 28</sup></sub> |

### Reshaping & Flattening
| Function | Description |
|---|---|
| `reshape()` | Gives an array a new shape without changing its data. <sub><sup>cells 31, 44</sup></sub> |
| `ravel()` | Flattens an array back to 1D. <sub><sup>cells 32, 43</sup></sub> |

### Combining Arrays
| Function | Description |
|---|---|
| `np.concatenate()` | Joins arrays along an existing axis. <sub><sup>cell 33</sup></sub> |
| `np.vstack()` | Stacks arrays vertically (as rows). <sub><sup>cell 34</sup></sub> |
| `np.hstack()` | Stacks arrays horizontally (side by side). <sub><sup>cell 35</sup></sub> |

### Random Arrays
| Function | Description |
|---|---|
| `np.random.rand()` | Random floats in [0, 1) in a given shape. <sub><sup>cell 37</sup></sub> |

### Miscellaneous Functions
| Function | Description |
|---|---|
| `argmin()` | Index of the smallest element. <sub><sup>cell 40</sup></sub> |
| `argmax(axis=0)` | Index of the largest element along an axis. <sub><sup>cell 41</sup></sub> |
| `min()`, `max()`, `mean()` | Smallest value, largest value, and average. <sub><sup>cell 45</sup></sub> |

### Matrix Operations
| Operation / Function | Description |
|---|---|
| `a + b`, `a - b`, `a / b`, `a % b` | Element-wise arithmetic between arrays. <sub><sup>cells 49, 50, 52, 54</sup></sub> |
| `a * b` | Element-wise multiplication (not matrix multiplication). <sub><sup>cell 51</sup></sub> |
| `np.sqrt()` | Square root of every element. <sub><sup>cell 55</sup></sub> |
| `np.where(condition)` | Returns indices where the condition is True. <sub><sup>cells 56, 57</sup></sub> |
| `np.count_nonzero()` | Counts non-zero elements. <sub><sup>cell 58</sup></sub> |
| `a.T` | Transpose of the matrix. <sub><sup>cell 59</sup></sub> |
| `a @ b` | True matrix multiplication. <sub><sup>cell 60</sup></sub> |

### Memory & System Info
| Function / Attribute | Description |
|---|---|
| `sys.getsizeof()` | Memory used by a Python object (used to compare with lists). <sub><sup>cell 65</sup></sub> |
| `.itemsize` | Bytes used by one array element. <sub><sup>cell 66</sup></sub> |
| `itemsize * size` | Total memory used by a NumPy array. <sub><sup>cell 66</sup></sub> |

### Meshgrid
| Function | Description |
|---|---|
| `np.meshgrid()` | Turns two 1D arrays into 2D coordinate grids of all x-y combinations. <sub><sup>cell 69</sup></sub> |

---

## 2. `Numpy_Depth.ipynb`

A deeper look: attributes, operations, math/statistics, slicing, stacking, broadcasting and ML formulas.

### Creating Arrays
| Function | Description |
|---|---|
| `np.array()` | Builds 1D, 2D and 3D arrays; accepts `dtype=`. <sub><sup>cells 4, 5, 6, 7, 94</sup></sub> |
| `np.arange(start, stop, step)` | Range of values with a step (combine with `reshape`). <sub><sup>cells 8, 9, 16, 25, 38, 42, 65, 69, 74, 82 …</sup></sub> |
| `np.ones()` | Array filled with ones. <sub><sup>cell 10</sup></sub> |
| `np.zeros()` | Array filled with zeros. <sub><sup>cell 11</sup></sub> |
| `np.random.random()` | Random floats in [0, 1) in a given shape. <sub><sup>cells 12, 33, 40</sup></sub> |
| `np.linspace()` | Equally spaced values between two numbers. <sub><sup>cells 13, 98</sup></sub> |
| `np.identity()` | Identity matrix. <sub><sup>cell 14</sup></sub> |

### Array Attributes
| Attribute | Description |
|---|---|
| `ndim` | Number of dimensions. <sub><sup>cell 17</sup></sub> |
| `shape` | Rows, columns, etc. of the array. <sub><sup>cell 18</sup></sub> |
| `size` | Number of items. <sub><sup>cell 19</sup></sub> |
| `itemsize` | Memory of one item (e.g. 8 bytes for float64). <sub><sup>cell 20</sup></sub> |
| `dtype` | Data type of the items. <sub><sup>cell 21</sup></sub> |

### Changing Data Type
| Function | Description |
|---|---|
| `astype()` | Returns a copy converted to another dtype (e.g. `np.int32`). <sub><sup>cell 23</sup></sub> |

### Array Operations
| Concept | Description |
|---|---|
| Scalar operations | `+ - * /` with a single number applies to every element. <sub><sup>cell 27</sup></sub> |
| Relational operators | `a2 > 7` gives a Boolean array. <sub><sup>cell 29</sup></sub> |
| Vector operations | Same-shaped arrays operate element by element. <sub><sup>cell 31</sup></sub> |

### Array Functions (Math & Statistics)
| Function | Description |
|---|---|
| `np.round()` | Rounds to the nearest integer / given decimals. <sub><sup>cells 33, 40</sup></sub> |
| `np.max()`, `np.min()` | Maximum and minimum (optionally along an axis). <sub><sup>cells 34, 35</sup></sub> |
| `np.sum()`, `np.prod()` | Sum and product of elements. <sub><sup>cell 34</sup></sub> |
| `np.mean()`, `np.median()` | Average and middle value. <sub><sup>cells 36, 92</sup></sub> |
| `np.std()`, `np.var()` | Standard deviation and variance. <sub><sup>cell 36</sup></sub> |
| `np.sin()` | Trigonometric sine of each element. <sub><sup>cells 37, 86, 100</sup></sub> |
| `np.dot()` | Dot product / matrix multiplication of two arrays. <sub><sup>cell 38</sup></sub> |
| `np.log()`, `np.exp()` | Natural logarithm and exponential. <sub><sup>cell 39</sup></sub> |
| `np.floor()` | Rounds down to the previous whole number. <sub><sup>cell 40</sup></sub> |
| `np.ceil()` | Rounds up to the next whole number. <sub><sup>cell 40</sup></sub> |

> `axis=0` works down columns, `axis=1` works across rows.

### Indexing & Slicing
| Concept | Description |
|---|---|
| `a[-1]` | Last item. <sub><sup>cell 43</sup></sub> |
| `a2[1, 2]` / `a2[1][2]` | Element by row and column (2D). <sub><sup>cell 45</sup></sub> |
| `a3[1, 0, 1]` | Element by block, row, column (3D). <sub><sup>cell 47</sup></sub> |
| `a1[2:7:2]` | Slice with start, stop and step. <sub><sup>cell 48</sup></sub> |
| `a2[0, :]`, `a2[:, 2]` | A full row / a full column. <sub><sup>cells 49, 50</sup></sub> |
| `a2[1:3, 1:3]`, `a2[::2, 1::2]` | Sub-matrix slicing with steps. <sub><sup>cells 51, 52</sup></sub> |
| `a3[1:2, 0:2, 0:1]` | 3D slicing `[array, row, column]`. <sub><sup>cell 55</sup></sub> |

### Iterating
| Function | Description |
|---|---|
| `for i in arr` | Loops over elements (1D) or rows (2D) or sub-arrays (3D). <sub><sup>cells 57, 58, 60</sup></sub> |
| `np.nditer()` | Iterates over every single element of any-dimension array. <sub><sup>cells 59, 61</sup></sub> |

### Reshaping
| Function | Description |
|---|---|
| `np.transpose()` | Swaps rows and columns (a view, no data copy). <sub><sup>cell 62</sup></sub> |
| `ravel()` | Flattens to 1D. <sub><sup>cell 63</sup></sub> |

### Stacking & Splitting
| Function | Description |
|---|---|
| `np.hstack()` | Joins arrays side by side (3×4 + 3×4 → 3×8). <sub><sup>cell 66</sup></sub> |
| `np.vstack()` | Joins arrays top to bottom (3×4 + 3×4 → 6×4). <sub><sup>cell 67</sup></sub> |
| `np.hsplit()` | Splits an array into equal column groups. <sub><sup>cell 70</sup></sub> |
| `np.vsplit()` | Splits an array into equal row groups. <sub><sup>cell 71</sup></sub> |

### Advanced Indexing
| Technique | Description |
|---|---|
| Fancy indexing | `a[[0, 2, 5]]` / `a[:, [0, 2]]` selects specific rows / columns. <sub><sup>cells 76, 77</sup></sub> |
| Boolean indexing | `a[a > 40]` filters elements by a condition. <sub><sup>cell 79</sup></sub> |
| Combined conditions | `a[(a > 50) & (a % 2 == 0)]` uses `&` for multiple conditions. <sub><sup>cell 80</sup></sub> |
| `np.random.randint()` | Random integers in a range (used to create test data). <sub><sup>cells 78, 90, 101</sup></sub> |
| `reshape(-1, 3)` | Lets NumPy work out one dimension automatically. <sub><sup>cell 79</sup></sub> |

### Broadcasting
| Concept | Description |
|---|---|
| Same shape | Arrays of identical shape are added element-wise. <sub><sup>cell 82</sup></sub> |
| Different shape | NumPy stretches the smaller array to match the larger one. <sub><sup>cell 83</sup></sub> |
| Rules | (1) Pad shape with 1s to equal dimensions, (2) sizes must match or be 1, (3) stretch and compute. <sub><sup>cell 84</sup></sub> |

### Mathematical Formulas in NumPy
| Item | Description |
|---|---|
| `np.sin()` on arrays | Applies a formula to every element at once (vectorized). <sub><sup>cells 37, 86, 100</sup></sub> |
| Sigmoid | `1 / (1 + np.exp(-x))`: squashes values between 0 and 1 (used in ML). <sub><sup>cell 88</sup></sub> |
| Mean Squared Error | `np.mean((actual - predict) ** 2)`: loss function for linear regression. <sub><sup>cell 92</sup></sub> |

### Missing Values
| Function | Description |
|---|---|
| `np.nan` | Represents a missing value. <sub><sup>cell 94</sup></sub> |
| `np.isnan()` | Boolean mask showing which values are NaN. <sub><sup>cells 95, 96</sup></sub> |
| `a[~np.isnan(a)]` | Removes NaN values using the inverted mask. <sub><sup>cell 96</sup></sub> |

### Plotting Graphs
| Function | Description |
|---|---|
| `plt.plot()` | Plots lines such as `y = x`, `y = x²` and `y = sin(x)` using `np.linspace` data. <sub><sup>cells 98, 99, 100, 101</sup></sub> |

---

## 3. `Numpy_tricks.ipynb`

Handy functions for sorting, editing, searching and analyzing arrays.

### Sorting & Editing
| Function | Description |
|---|---|
| `np.sort()` | Returns a sorted copy (row-wise by default, or by `axis`). <sub><sup>cells 5, 6, 7</sup></sub> |
| `np.append()` | Adds values at the end; use `axis=1` to add a column. <sub><sup>cells 9, 10</sup></sub> |
| `np.concatenate()` / `np.concat()` | Joins arrays along a chosen axis (`np.concat` needs NumPy 2.0+). <sub><sup>cells 13, 14</sup></sub> |
| `np.unique()` | Returns the sorted unique values. <sub><sup>cell 17</sup></sub> |
| `np.expand_dims()` | Adds a new axis (row vector ↔ column vector). <sub><sup>cells 19, 20, 21, 22</sup></sub> |
| `np.flip()` | Reverses the order of elements (all or along an axis). <sub><sup>cells 53, 55, 56</sup></sub> |
| `np.put()` | Replaces elements at given indices with new values. <sub><sup>cell 59</sup></sub> |
| `np.delete()` | Removes elements at given indices. <sub><sup>cells 62, 63</sup></sub> |
| `np.clip()` | Limits values to a min and max range. <sub><sup>cell 70</sup></sub> |

### Searching
| Function | Description |
|---|---|
| `np.where(cond)` | Returns indices where the condition is True. <sub><sup>cell 24</sup></sub> |
| `np.where(cond, x, y)` | Replaces values: `x` where True, otherwise `y`. <sub><sup>cells 25, 26</sup></sub> |
| `np.argmax()` | Index of the maximum value (optionally by axis). <sub><sup>cells 28, 29</sup></sub> |
| `np.argmin()` | Index of the minimum value. <sub><sup>cell 31</sup></sub> |
| `np.isin()` | Boolean mask of elements that exist in another list. <sub><sup>cells 49, 50</sup></sub> |

### Cumulative Operations
| Function | Description |
|---|---|
| `np.cumsum()` | Running (cumulative) sum. <sub><sup>cells 34, 35</sup></sub> |
| `np.cumprod()` | Running (cumulative) product. <sub><sup>cell 37</sup></sub> |

### Statistics
| Function | Description |
|---|---|
| `np.percentile()` | Value below which a given percent of data falls (0 = min, 50 = middle, 100 = max). <sub><sup>cells 39, 40, 41</sup></sub> |
| `np.histogram()` | Counts values falling into given bins. <sub><sup>cell 43</sup></sub> |
| `np.corrcoef()` | Correlation matrix between variables (e.g. salary vs experience). <sub><sup>cell 45</sup></sub> |

### Set Functions
| Function | Description |
|---|---|
| `np.union1d()` | All unique values from both arrays. <sub><sup>cell 66</sup></sub> |
| `np.intersect1d()` | Values common to both arrays. <sub><sup>cell 67</sup></sub> |
| `np.setdiff1d()` | Values in the first array but not in the second. <sub><sup>cell 68</sup></sub> |
| `np.setxor1d()` | Values in either array but not in both. <sub><sup>cell 69</sup></sub> |

### Miscellaneous
| Function | Description |
|---|---|
| `np.swapaxes()` | Interchanges two axes of an array. <sub><sup>cell 76</sup></sub> |
| `np.random.uniform()` | Random floats between a low and high value. <sub><sup>cell 77</sup></sub> |
| `np.count_nonzero()` | Counts non-zero elements. <sub><sup>cell 79</sup></sub> |
| `np.repeat()` | Repeats each element a given number of times. <sub><sup>cell 80</sup></sub> |

---

## 4. Array Attributes & Methods (reference)

`array_attributes_and_methods.png` is the NumPy `ndarray` documentation page listing every attribute (`T`, `dtype`, `shape`, `size`, `itemsize`, `nbytes`, `ndim`, `strides`, ...) and method (`all`, `any`, `argsort`, `astype`, `clip`, `cumsum`, `dot`, `flatten`, `reshape`, `sort`, `transpose`, ...). Use it as a lookup when you need something beyond these notebooks.

![ndarray attributes and methods](array_attributes_and_methods.png)

---

## 📂 Repository Structure

| File | Description |
|---|---|
| `numpy_Basics.ipynb` | Core NumPy concepts and operations |
| `Numpy_Depth.ipynb` | Deeper NumPy concepts and array operations |
| `Numpy_tricks.ipynb` | Useful NumPy tricks and practical techniques |
| `array_attributes_and_methods.png` | ndarray attributes/methods reference |

## ✅ Status

**NumPy: essential concepts completed.** I'll revisit it when a future Data Science or Machine Learning project needs more.

---

## 🚀 Uses of NumPy

* **Data Science:** fast numerical computing and cleaning of large datasets; the base that Pandas is built on.
* **Machine Learning:** arrays hold features, weights and predictions; used for loss functions (MSE) and activations (sigmoid).
* **Statistics & Analysis:** mean, median, standard deviation, percentiles, correlation and histograms.
* **Linear Algebra:** matrix multiplication, transpose and dot products.
* **Image Processing:** images are stored as 2D/3D arrays of pixel values.
* **Scientific Computing:** simulations, signal processing and math on large arrays.
* **Data Visualization:** generates the data behind Matplotlib plots (`linspace`, `sin`, `random`).
* **Performance:** vectorized operations are much faster and more memory-efficient than Python loops and lists.
