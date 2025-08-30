# Income-Prediction

This project predicts income levels using the UCI Adult dataset, focusing on bias identification and mitigation in machine learning models.

## Project Structure

```
data/
  raw/         # Original data files
  processed/   # Cleaned and transformed data
docs/          # Documentation and GitHub Pages site (results, figures)
models/        # Trained models and results per cluster
notebooks/     # Jupyter notebooks (EDA, classification, clustering, clustered models)
requirements.txt
README.md
```

## How to Reproduce

1. **Install dependencies**
   ```sh
   pip install -r requirements.txt
   ```

2. **Download the UCI Adult dataset**
   - Place the raw files in `data/raw/` as expected by the notebooks.

3. **Run the notebooks in order:**

   1. **Exploratory Data Analysis (EDA)**
      - Cleans and preprocesses the data.
      - Output: `data/processed/adult.data`
      - Notebook: [`notebooks/EDA.ipynb`](notebooks/EDA.ipynb)

   2. **Initial Classification**
      - Trains and evaluates a baseline classifier (e.g., XGBoost).
      - Notebook: [`notebooks/initial_classification.ipynb`](notebooks/initial_classification.ipynb)

   3. **Clustering**
      - Segments the data using K-Prototypes and analyzes clusters.
      - Assigns cluster labels and exports processed data with clusters.
      - Notebook: [`notebooks/clustering.ipynb`](notebooks/clustering.ipynb)

   4. **Clustered Models**
      - Trains and evaluates a model for each cluster.
      - Notebook: [`notebooks/clustered_models.ipynb`](notebooks/clustered_models.ipynb)

> **Tip:** Run the notebooks in order for reproducibility. All results and processed files will be saved in the corresponding folders.

## Key Results

- **EDA:** Outliers and missing values handled, categorical variables grouped for robustness.
- **Initial Classification:** Baseline model performance and bias metrics.
- **Clustering:** Data segmented into 6 clusters; cluster profiles analyzed and exported.
- **Clustered Models:** Models trained per cluster; results compared to global model.
- **Modeling and bias analysis:** See [docs/index.html](docs/index.html) for results, tables, and visualizations.

## Authors

- Diego Lemus
- José Kiesling
- Francisco Castillo
- Sharis Barrios
- Sebastián Silva
