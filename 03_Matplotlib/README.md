# Matplotlib Notes 📊

Documentation of **Matplotlib** (and a bit of Pandas' built-in plotting) concepts in Python, practiced using IPL cricket datasets (Kohli vs Rohit runs, batsman stats, ball-by-ball data, etc.).

## What's inside

The notebook (`Matplotlib.ipynb`) covers:

- **2D Line Plots** – basic plots, multiple lines, colors, line styles, markers, legends, axis limits, grid
- **Scatter Plots** – simple scatter, plotting from a DataFrame, changing point size
- **Bar Graphs** – simple bar chart, horizontal bars, multiple/grouped bars, stacked bar chart
- **Histograms** – frequency plots, bins, log scale
- **Pie Charts** – basic pie chart, percentage labels, explode & shadow effect
- **Changing Styles** – using built-in matplotlib styles (like `dark_background`)
- **Subplots** – different ways to plot multiple graphs together (`plt.subplots()`, `fig.add_subplot()`)
- **Annotations** – adding text labels, horizontal/vertical reference lines
- **Saving Figures** – exporting plots as image files
- **3D Plots** – 3D scatter, 3D line plot, 3D surface plot, contour plots
- **Heatmaps** – using `imshow()`
- **Pandas `.plot()`** – quick plotting directly from Series/DataFrame (line, bar, hist, pie, stacked, subplots)

---
⭐ If this helped you, consider starring the repo!


# Matplotlib Cheat Sheet 📊

Quick reference for the key functions and parameters used across the Matplotlib notebook.

---

## Line Plots

| Function/Param | Purpose |
|---|---|
| `plt.plot(x, y)` | Draw a line plot |
| `color='red'` / `color='#369FEB'` | Line color (name or hex) |
| `linestyle='dashdot'/'dashed'/'solid'` | Line style |
| `linewidth=` | Line thickness |
| `marker='o'/'D'/'s'/'^'/'*'/'+'/'x'` | Point marker shape |
| `markersize=` | Marker size |
| `label=` | Name for legend |
| `plt.legend(loc='best')` | Show legend |
| `plt.title()`, `plt.xlabel()`, `plt.ylabel()` | Labels |
| `plt.xlim()`, `plt.ylim()` | Limit axis range |
| `plt.grid()` | Show grid |
| `plt.show()` | Render the plot |

## Scatter Plots

| Function/Param | Purpose |
|---|---|
| `plt.scatter(x, y)` | Draw scatter plot |
| `s=` | Point size (can map to a column, for bubble charts) |
| `c=` / `color=` | Point color |
| `marker='+'` | Marker style |

## Bar Charts

| Function/Param | Purpose |
|---|---|
| `plt.bar(x, height)` | Vertical bar chart |
| `plt.barh(x, height)` | Horizontal bar chart |
| `width=` | Bar width (used with offsets for grouped bars) |
| `bottom=` | Stack bars on top of another (stacked bar chart) |
| `plt.xticks(rotation='vertical')` | Rotate category labels |

## Histogram

| Function/Param | Purpose |
|---|---|
| `plt.hist(data, bins=[...])` | Draw histogram |
| `bins=` | Bin edges/count |
| `log=True` | Log scale (fixes skewed distributions) |

## Pie Chart

| Function/Param | Purpose |
|---|---|
| `plt.pie(values, labels=)` | Draw pie chart |
| `autopct='%0.1f%%'` | Show percentage on slices |
| `colors=[...]` | Custom slice colors |
| `explode=[...]` | Pull out a slice |
| `shadow=True` | Add shadow effect |

## Styles & Subplots

| Function/Param | Purpose |
|---|---|
| `plt.style.available` | List built-in styles |
| `plt.style.use('dark_background'/'default')` | Apply a style |
| `plt.figure(figsize=(w,h))` | Set figure size |
| `plt.subplots(nrows=, ncols=, sharex=, figsize=)` | Create figure + axis grid |
| `ax[i].scatter()`, `ax[i].set_title()`, `ax[i].set_xlabel()` etc. | Plot/label on a specific subplot |
| `fig.add_subplot(rows, cols, position)` | Manually add a subplot |

## Annotations

| Function/Param | Purpose |
|---|---|
| `plt.text(x, y, "label", fontdict={})` | Place text at coordinates |
| `plt.axhline(y, color=)` | Horizontal reference line |
| `plt.axvline(x, color=)` | Vertical reference line |

## Saving

| Function/Param | Purpose |
|---|---|
| `plt.savefig('name.png')` | Export current figure as an image |

## 3D Plots

| Function/Param | Purpose |
|---|---|
| `plt.subplot(projection='3d')` | Create a 3D axis |
| `ax.scatter3D(x, y, z)` | 3D scatter |
| `ax.plot3D(x, y, z, color=)` | 3D line |
| `ax.plot_surface(xx, yy, z, cmap=)` | 3D surface plot |
| `np.meshgrid(x, y)` | Build coordinate grid for surface/contour plots |
| `ax.contour()` / `ax.contourf()` | 2D top-down view of a 3D surface (unfilled/filled) |
| `fig.colorbar(g)` | Add color scale legend |
| `ax.set_xlabel()/set_ylabel()/set_zlabel()` | Axis labels in 3D |

## Heatmaps

| Function/Param | Purpose |
|---|---|
| `plt.imshow(grid)` | Draw heatmap from a 2D array/pivot table |
| `plt.colorbar()` | Show color scale |
| `plt.yticks(ticks, labels)` | Custom y-axis tick labels |

## Pandas `.plot()`

| Function/Param | Purpose |
|---|---|
| `df.plot(kind='line'/'bar'/'hist'/'pie'/'scatter')` | Plot directly from a Series/DataFrame |
| `x=`, `y=` | Columns to use as axes |
| `stacked=True` | Stack bar segments |
| `subplots=True` | Split each column into its own panel |
| `figsize=` | Figure size |
| `cmap=` | Colormap (used with `c=` for color-coded scatter) |

---
⭐ If this helped you, consider starring the repo!
