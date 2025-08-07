# estimation_stats

Estimate and visualize effect sizes using DABEST in Python.

## Overview
This mini-tool provides a simple workflow for estimation statistics using the DABEST package. It loads data from Excel, computes effect sizes (mean difference, Hedges' g), and visualizes results with customizable plots.

## Features
- Load two-group data from Excel
- Calculate mean difference and Hedges' g
- Visualize results with DABEST's plotting functions

## Requirements
See `requirements.txt` for dependencies (numpy, pandas, dabest).

## Usage
1. Place your data in an Excel file (e.g., `Group 1.xlsx`) with columns for each group.
2. Open and run `est_stats.ipynb` in Jupyter or VS Code.
3. Adjust group names and plot settings as needed.

## Example
```python
import pandas as pd
import dabest
df = pd.read_excel('Group 1.xlsx')
two_groups = dabest.load(df, idx=("Untreated", "Treated"))
print(two_groups.mean_diff)
two_groups.mean_diff.plot()
```
