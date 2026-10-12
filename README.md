# SmartCart: Customer Segmentation Using Machine Learning

## Overview

SmartCart is a customer-segmentation project that explores customer
demographics, spending patterns, and shopping behaviour using
unsupervised machine learning. The goal is to group customers with
similar characteristics so businesses can better understand their
audience and plan more relevant marketing strategies.

## Objectives

-   Clean and prepare customer data for analysis.
-   Explore relationships between income, age, spending, and shopping
    behaviour.
-   Engineer useful features, including age, total spending, number of
    children, and customer tenure.
-   Encode categorical variables and standardize features.
-   Use Principal Component Analysis (PCA) to reduce dimensionality.
-   Explore the number of clusters with the Elbow Method and Silhouette
    Score.
-   Compare K-Means and Agglomerative Clustering.
-   Summarize customer characteristics by cluster.

## Dataset

The project uses `smartcart_customers.csv`, containing **2,240 customer
records and 22 columns**.

The data includes fields such as:

-   Customer demographics: year of birth, education, marital status,
    income, and household children.
-   Spending: wine, fruit, meat, fish, sweets, and gold products.
-   Purchasing behaviour: web, catalog, and store purchases, deal
    purchases, and monthly web visits.
-   Customer information: joining date, recency, complaints, and
    campaign response.

**Data note:** The dataset contains 24 missing values in `Income`. The
notebook fills these values with the median income. Make sure you have
permission to redistribute the dataset before uploading it publicly, and
include its original source and licence in this section.

## Tools and Libraries

-   Python
-   Pandas
-   Seaborn
-   Matplotlib
-   scikit-learn
-   kneed

## Workflow

1.  **Load and inspect data** --- review columns and missing values.
2.  **Handle missing income values** --- replace missing values with the
    median.
3.  **Feature engineering** --- derive age, total product spending,
    total children, and customer tenure.
4.  **Feature preparation** --- group education and living-status
    categories, remove selected original columns, and one-hot encode
    categorical features.
5.  **Outlier filtering** --- exclude records with age of 90 or above
    and income of 600,000 or above.
6.  **Exploratory data analysis** --- use pair plots and a correlation
    heatmap.
7.  **Scaling and dimensionality reduction** --- standardize features
    and use PCA for visualization and clustering.
8.  **Cluster selection** --- inspect the Elbow Method and Silhouette
    Score plots.
9.  **Clustering** --- fit K-Means and Agglomerative Clustering with
    four clusters.
10. **Cluster interpretation** --- visualize cluster sizes and income
    versus spending, then calculate cluster-level averages.

## Installation

Use Python 3.10 or later if possible. From the project folder, install
the required libraries:

``` bash
python -m pip install pandas seaborn matplotlib scikit-learn kneed jupyter
```

## Run the Project

1.  Clone or download this repository.
2.  Place `smartcart_customers.csv` in the same folder as the notebook.
3.  Install the libraries listed above.
4.  Open Jupyter Notebook or JupyterLab and run the notebook cells in
    order.

``` bash
jupyter notebook
```

> **Important:** Ensure `Smart cart.ipynb` is saved as a valid Jupyter
> Notebook file before publishing. If it currently contains plain Python
> script text, create a new notebook and copy the code into cells, or
> save the code as a `.py` file and update these instructions
> accordingly.

## Outputs

The analysis generates:

-   Pair plots for selected customer features.
-   A correlation heatmap.
-   2D and 3D PCA visualizations.
-   Elbow Method and Silhouette Score plots.
-   3D cluster visualizations for K-Means and Agglomerative Clustering.
-   A cluster-count plot.
-   An income-versus-spending scatter plot.
-   A table of average feature values by cluster.

## Current Approach and Notes

-   The notebook currently uses **four clusters** for both K-Means and
    Agglomerative Clustering.
-   It calculates the Elbow Method and Silhouette Score to help assess
    the number of clusters, but the final choice should be justified
    using the actual plots and scores.
-   Cluster labels such as `0`, `1`, `2`, and `3` are arbitrary
    identifiers; interpret them using the cluster summary rather than
    treating the numbers as rankings.
-   PCA is used for visualization and clustering in the current
    workflow. Consider comparing results with clustering on the full
    standardized feature set, since dimensionality reduction can affect
    cluster structure.
-   For reproducibility, set `random_state` where applicable and record
    your Python/library versions.

## Key Findings

Add your verified findings here after running the notebook. For example,
describe which clusters have relatively high or low average spending,
income, or purchase activity. Do not label a cluster as "high-value" or
"at-risk" until the cluster summary supports that interpretation.

## Future Improvements

-   Add a clear comparison of clustering quality using silhouette
    scores.
-   Create a concise profile for each cluster using interpretable
    averages and charts.
-   Validate the selected number of clusters instead of relying only on
    a fixed value.
-   Improve plot titles, axis labels, legends, and saved output
    filenames.
-   Add a `requirements.txt` file and record the dataset source and
    licence.

## Repository Structure

``` text
SmartCart/
├── README.md
├── requirements.txt
├── Smart cart.ipynb
└── smartcart_customers.csv
```

## Disclaimer

This project is for learning and demonstration purposes. Customer
segments are exploratory patterns in the supplied dataset and should be
validated before being used for business decisions.

## Author

**Pesarakayala Ashwith Reddy**
