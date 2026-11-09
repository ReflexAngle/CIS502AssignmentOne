# CIS502AssignmentOne

A group data-analysis project exploring the classic Iris flower dataset. Working as junior data analysts for a botanical research center, our team cleaned the dataset, wrote Python programs demonstrating core language features, analyzed the measurements with pandas, and visualized the patterns that separate the three Iris species.

## Team

| Member | Primary Contribution
| --- | --- |
| Bradley Petersen | Control structures, functions, data cleaning, visualizations, written analysis |
| Tensae Gonfa | Variables, data inspection (pandas), species counting, flower categorization |
| Timur Zhomartov | Loops, CSV file I/O & summary file, descriptive statistics |

## Dataset

The project uses the **Iris dataset** from the [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/53/iris).
 
- **150 flowers** (50 of each species) across **3 species**: *Iris setosa*, *Iris versicolor*, and *Iris virginica*.
- **4 numeric measurements** per flower (in centimeters): sepal length, sepal width, petal length, petal width.
- **1 categorical label**: species.
The raw file ships without a header row, so column names are assigned on import.


## Repository Structure

```
.
├── DataSet/
│   ├── iris.data            # Raw dataset from UCI (no header)
│   ├── clean_iris.csv       # Cleaned dataset (duplicates/nulls removed)
│   └── iris_classes.csv     # Cleaned data + petal_category column
├── PythonFiles/
│   ├── Iris_Project_Phases_1_2_3_4.ipynb   # Main analysis notebook
│   └── summary.txt          # Auto-generated dataset summary (Phase 3)
├── REFLECTION.md            # Group reflection (Phase 5)
├── gitignore
└── README.md
```

## Steps Performed

The project was completed in five phases.

## Phase 1 — Setup & GitHub Basics

Created the shared GitHub repository and starter notebook; each member committed a "Hello Iris" cell to confirm their environment and Git workflow.

## Phase 2 — Python Fundamentals

Demonstrated core Python features with commented examples:
- **Variables** — stored dataset metadata (`n_rows = 150`, `n_columns = 5`, `n_species = 3`).
- **Control structures** — an `if/else` that labels a petal "Large" or "Small" against a 1.5 cm threshold.
- **Loops** — iterated over the list of species and printed each.
- **Functions** — `classify_flower(sepal_length, petal_length)` returns a size label (`Small` / `Medium` / `Large`).


## Phase 3 — File Handling & Data Cleaning

- Read the raw CSV with Python's built-in `csv` module and wrote **`summary.txt`** (row count, min/max, and average petal length).
- Loaded the data with **pandas**, then checked column names, data types, and missing values.
- Removed duplicate rows and any nulls, then saved the result as **`clean_iris.csv`**.
- Cleaning removed **3 duplicate rows**, reducing the dataset from 150 to **147 rows**.

## Phase 4 — Analysis & Visualization

- Counted flowers per species with a `for` loop (setosa 48, versicolor 50, virginica 49 after cleaning).
- Categorized every flower by petal length into **Short** (< 2 cm), **Medium** (2–5 cm), and **Long** (> 5 cm) buckets.
- Computed mean, median, min, and max of sepal and petal lengths, and grouped averages by species.
- Built a histogram, bar chart, boxplot, and scatter plot (see below).
- Exported the categorized data to **`iris_classes.csv`**.

## Phase 5 — Presentation & Reflection

Polished the notebook with Markdown explanations and thorough comments, wrote this README, prepared a 10-minute group presentation, and documented the group reflection in REFLECTION.md.

## Key Findings
- Petal length clearly separates the species. Average petal length jumps from 1.46 cm (setosa) to 4.26 cm (versicolor) to 5.56 cm (virginica). Setosa stands apart completely, while versicolor and virginica overlap slightly.

- Sepal length and sepal width are not strongly correlated across the full dataset — the scatter forms a loose cloud rather than a straight line. A positive trend does appear within each species, but it is masked when the three species are pooled together because each occupies a different region of the plot.

- Petal measurements are the most useful features for separating species; sepal width is the least useful, since all three species overlap heavily on that dimension.

## Example Graphs

Petal length distribution by species

Average sepal length by species

Petal length range by species

Sepal length vs sepal width by species

## How to Run
1. Clone the repository:
```bash
git clone https://github.com/ReflexAngle/CIS502AssignmentOne.git
cd CIS502AssignmentOne
```
2. Install the dependencies:
``` python
pip install pandas matplotlib jupyter 
```
3. Launch the notebook and run all cells top to bottom:
```python
jupyter notebook notebook/Iris_Project_Phases_1_2_3_4.ipynb
```

## Running the notebook regenerates summary.txt, clean_iris.csv, and iris_classes.csv.

### Requirements
Python 3.9+
pandas
matplotlib
Jupyter Notebook
