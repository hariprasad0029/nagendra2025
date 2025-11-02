# Copilot Instructions for the Nagendra Project

Welcome to the Nagendra project! This document provides essential guidelines for AI coding agents to be productive and aligned with the project's structure, workflows, and conventions.

## Project Overview

The Nagendra project is a collection of machine learning notebooks and scripts organized into the following categories:

1. **Clustering**: Notebooks and datasets for clustering algorithms, including k-means, hierarchical clustering, and the elbow method.
2. **Regression**: A comprehensive set of notebooks covering regression techniques such as linear regression, ridge/lasso regularization, and decision trees.
3. **Classification**: Resources for classification algorithms, including logistic regression, decision trees, and performance metrics.
4. **Projects**: End-to-end machine learning projects, such as sales prediction and refinance value estimation.

Key directories include:
- `2_ML_Files/2_Clustering/`: Clustering-related notebooks and datasets.
- `2_ML_Files/3_Regression/`: Regression notebooks and datasets.
- `2_ML_Files/4_Classification/`: Classification notebooks and datasets.

## Developer Workflows

### Running Notebooks
- Use Jupyter Notebook or VS Code to run `.ipynb` files.
- Ensure the required Python environment is activated before running notebooks.

### Setting Up the Environment
- Install dependencies using `pip install -r requirements.txt` (if a `requirements.txt` file exists).
- For notebooks, install missing packages directly in the notebook using `!pip install <package>`.

### Debugging
- Use inline debugging tools in Jupyter or VS Code.
- For Python scripts, use `pdb` or VS Code's debugging interface.

## Project-Specific Conventions

1. **Notebook Structure**:
   - Start with a markdown cell describing the notebook's purpose.
   - Import libraries in the first code cell.
   - Use clear section headers for different stages (e.g., data loading, preprocessing, modeling).

2. **File Naming**:
   - Use descriptive names for notebooks and datasets (e.g., `Clustering_Iris_dataset.ipynb`).

3. **Data Handling**:
   - Store datasets in the appropriate subdirectory (e.g., `2_ML_Files/2_Clustering/iris_archive/`).
   - Use relative paths to load datasets.

## Integration Points

- **External Libraries**: Commonly used libraries include `pandas`, `numpy`, `matplotlib`, `seaborn`, and `scikit-learn`.
- **Data Sources**: Datasets are stored locally in the `2_ML_Files/` directory.

## Examples

### Loading a Dataset
```python
import pandas as pd

# Load the Iris dataset
iris = pd.read_csv("../2_ML_Files/2_Clustering/iris_archive/Iris.csv")
```

### Running a Clustering Algorithm
```python
from sklearn.cluster import KMeans

# Fit k-means clustering
kmeans = KMeans(n_clusters=3)
kmeans.fit(data)
```

## Notes for AI Agents

- Follow the existing structure and naming conventions.
- When adding new notebooks, ensure they are placed in the correct subdirectory.
- Document any new workflows or dependencies in this file.

---

If you have any questions or need clarification, feel free to ask!