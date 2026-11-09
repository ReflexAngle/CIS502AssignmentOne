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

## Steps Performed

## Phase 1 — Setup & GitHub Basics

## Phase 2 — Python Fundamentals

## Phase 3 — File Handling & Data Cleaning

## Phase 4 — Analysis & Visualization

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
pip install pandas matplotlib jupyter </pre>
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

(The csv and os modules used in Phase 3 are part of the Python standard library.)
