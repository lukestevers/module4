# Luke Stevers - Exploratory Data Analysis

[![Python 3.14](https://img.shields.io/badge/python-3.14%2B-blue?logo=python)](./pyproject.toml)
[![uv managed](https://img.shields.io/badge/uv-managed-DE5FE9)](https://docs.astral.sh/uv/)
[![Ruff](https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/astral-sh/ruff/main/assets/badge/v2.json)](https://docs.astral.sh/ruff/)
[![Jupyter](https://img.shields.io/badge/Jupyter-notebook-F37626?logo=jupyter&logoColor=white)](https://jupyter.org/)
[![Zensical](https://img.shields.io/badge/Zensical-docs-purple)](https://zensical.org/)
[![MIT](https://img.shields.io/badge/license-MIT-yellow.svg)](./LICENSE)

## Project Overview

This project demonstrates **Exploratory Data Analysis (EDA)** using Python, pandas, Seaborn, Matplotlib, and Jupyter notebooks.

The project includes two related analyses:

1. A technical modification to the provided Palmer Penguins analysis comparing body mass between male and female penguins.
2. A custom EDA investigation using the Seaborn `mpg` dataset to explore factors associated with vehicle fuel efficiency.

The goal of the project is to demonstrate a repeatable EDA workflow: inspect a dataset, evaluate data quality, summarize variables, visualize distributions, investigate relationships, and communicate findings clearly.

---

## Phase 4: Penguin Analysis

As part of the technical modification, I extended the original penguin analysis to compare **body mass between female and male penguins**.

The analysis removes records with missing values for sex or body mass and then uses a Matplotlib box plot to compare the two groups.

![Penguin Body Mass by Sex](docs/images/body-mass-by-sex.png)

### Observation

The box plot shows a noticeable difference in the distribution of body mass between female and male penguins. Male penguins generally have higher body mass values, although there is variation within both groups.

This analysis demonstrates how grouping data by a categorical variable can reveal differences that are not obvious from an overall summary.

---

## Phase 5: Custom EDA - Automobile Fuel Efficiency

For my custom EDA project, I used the **Seaborn `mpg` dataset**.

### Project Question

> **What vehicle characteristics are associated with differences in fuel efficiency?**

The dataset contains automobile measurements and characteristics including:

- Miles per gallon (`mpg`)
- Number of cylinders
- Engine displacement
- Horsepower
- Vehicle weight
- Acceleration
- Model year
- Country of origin
- Vehicle name

The analysis is contained in:

**[`notebooks/eda_lukestevers.ipynb`](notebooks/eda_lukestevers.ipynb)**

---

## Data Inspection and Quality

The dataset contains:

- **398 rows**
- **9 variables**
- **6 missing horsepower values**
- **0 duplicate rows**

The analysis uses pandas to inspect the structure and quality of the dataset before examining relationships between variables.

The missing horsepower values were identified during the data-quality stage. Rather than treating missing values as a problem to hide, the EDA documents them as part of understanding the dataset.

---

## Key Findings

### Vehicle Weight and Fuel Efficiency

The strongest relationship investigated was between vehicle weight and fuel efficiency.

The correlation between weight and MPG was approximately:

**r = -0.832**

This indicates a strong negative linear association in this dataset: as vehicle weight increases, MPG generally decreases.

The scatter plot also shows this pattern visually.

### Cylinders and Fuel Efficiency

Fuel efficiency also differs by number of cylinders.

The box plot shows that:

- 4-cylinder vehicles generally have higher MPG values.
- 6-cylinder vehicles tend to fall between the 4-cylinder and 8-cylinder groups.
- 8-cylinder vehicles generally have lower MPG values.
- The 3-cylinder group contains relatively few observations.

This suggests that engine configuration is associated with differences in fuel efficiency.

### Vehicle Origin and Fuel Efficiency

The analysis also compared MPG by vehicle origin.

The distributions suggest differences among vehicles from the United States, Japan, and Europe. Japanese vehicles generally show higher MPG values in this dataset, while U.S. vehicles generally show lower MPG values.

There is still substantial overlap between the groups, so origin alone does not explain fuel efficiency.

---

## EDA Workflow

The custom notebook follows a structured exploratory process:

1. **Load the data**
2. **Inspect the dataset**
3. **Check data quality**
4. **Describe numerical variables**
5. **Visualize distributions**
6. **Explore relationships**
7. **Compare MPG by number of cylinders**
8. **Compare MPG by vehicle origin**
9. **Summarize findings and identify possible next steps**

This workflow provides a repeatable approach for becoming familiar with an unfamiliar dataset.

---

## Skills Demonstrated

This project demonstrates experience with:

- Python
- pandas
- Seaborn
- Matplotlib
- Jupyter notebooks
- Exploratory Data Analysis
- Data-quality checks
- Descriptive statistics
- Missing-value analysis
- Grouping and filtering
- Correlation analysis
- Data visualization
- Interpreting distributions
- Comparing categorical groups
- Writing analytical observations
- Git and GitHub
- UV Python project management
- Zensical documentation

---

## Project Structure

```text
datafun-04-eda/
│
├── docs/
│   └── images/
│       └── body-mass-by-sex.png
│
├── notebooks/
│   └── eda_lukestevers.ipynb
│
├── src/
│   └── datafun/
│       └── app.py
│
├── project.log
├── pyproject.toml
├── README.md
└── zensical.toml
