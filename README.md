# Kaggle-Spaceship-Titanic
# Spaceship Titanic Prediction Project

This repository contains code and notebooks for the Kaggle competition [Spaceship Titanic](https://www.kaggle.com/competitions/spaceship-titanic) aimed at predicting passenger transportation status. The goal is to preprocess the data, build and tune a classification model, and generate a submission file for ranking.

## Project Structure

```
├── data
│   ├── raw             # Original train/test CSV files
│   ├── processed       # Cleaned data and final submission.csv
├── notebooks
│   ├── SpaceshipTitanic_ModellingNotebook.ipynb  # Main exploratory and modelling notebook
├── env                # Virtual environment configuration (optional)
├── requirements.txt   # Python dependencies
├── README.md          # This file
```

## Setup and Installation

1. **Clone the repository**:

   ```bash
   git clone <repo_url>
   cd spaceship-titanic
   ```

2. **Create and activate a virtual environment** (recommended):

   ```bash
   python3 -m venv env
   source env/bin/activate    # On Windows: env\\Scripts\\activate
   ```

3. **Install dependencies**:

   ```bash
   pip install -r requirements.txt
   ```

## Running the Notebook

1. Launch Jupyter Lab or Notebook:

   ```bash
   jupyter lab
   ```

2. Open `notebooks/SpaceshipTitanic_ModellingNotebook.ipynb`.

3. Run cells in order. The notebook covers:

   * Data loading and exploration
   * Feature engineering (e.g., spending totals, group size, cabin splits)
   * Pipeline creation with `ColumnTransformer` and classifiers
   * Hyperparameter tuning (RandomizedSearchCV, GridSearchCV)
   * Validation and final model selection
   * Generating `submission.csv`

## Usage

After fitting the final model in the notebook, the submission file is saved to:

```
data/processed/submission.csv
```

Upload this file to Kaggle to view your score.

## Hyperparameter Tuning

* **RandomizedSearchCV** for broad parameter exploration
* **GridSearchCV** for fine-tuning around best values
* Metrics tracked: Accuracy, F1 Score, ROC AUC

## Notes

* Ensure your `data/raw` folder contains `train.csv` and `test.csv` from Kaggle.
* The `.gitignore` is configured to ignore raw data and keep only processed results and code.

## Contact

For questions or issues, please open an issue in this repository or contact the maintainer.
