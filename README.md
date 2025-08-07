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

## Setup for New Python Users
1. Open a terminal in this project folder.
2. Create a virtual environment (recommended):
	 - On Windows:
		 ```sh
		 python -m venv venv
		 .\venv\Scripts\activate
		 ```
	 - On Mac/Linux:
		 ```sh
		 python3 -m venv venv
		 source venv/bin/activate
		 ```
3. Install the required packages:
	 ```sh
	 pip install -r requirements.txt
	 ```
4. Launch Jupyter or VS Code and open the notebook.

## Example
```python
import pandas as pd
import dabest
df = pd.read_excel('Group 1.xlsx')
two_groups = dabest.load(df, idx=("Untreated", "Treated"))
print(two_groups.mean_diff)
two_groups.mean_diff.plot()
```
