# Book-Recommender-System

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white)
![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626.svg?style=for-the-badge&logo=Jupyter&logoColor=white)

## Overview

This project is a user-based collaborative filtering recommender system designed to suggest books to users. It analyzes a user's past ratings and finds other users with similar tastes to recommend new books. The core of the system is built using Python, pandas for data manipulation, and scikit-learn for machine learning.

The dataset contains over 1 million ratings for hundreds of thousands of books from the Book-Crossings dataset.

## Features

* **Data Preprocessing:** Cleans and transforms raw CSV data into a memory-efficient sparse matrix suitable for machine learning.
* **Collaborative Filtering:** Implements a k-Nearest Neighbors (KNN) model to find similar users based on their book ratings.
* **Recommendation Generation:** Provides a ranked list of top-N book recommendations for users, excluding books they have already rated.
* **Model Persistence:** Saves the trained KNN model using `joblib` to avoid time-consuming retraining.

## Project Structure

The project is organized into a clean and reproducible structure:

```
book_recommender/
├── data/
│   ├── raw/                 # Original datasets (Books, Users, Ratings)
│   └── processed/           # Processed data (e.g., user-item matrix)
├── models/                  # Saved model artifacts (knn_recommender.pkl)
├── notebooks/
│   ├── 01-data-exploration.ipynb
│   ├── 02-data-preprocessing.ipynb
│   └── 03-model-training-and-recommendation.ipynb
├── output/                  # Generated recommendations CSV
└── README.md
```

## Tech Stack

* **Languages:** Python
* **Libraries:**
    * pandas: Data manipulation and analysis
    * NumPy: Numerical operations
    * scikit-learn: Machine learning (KNN, sparse matrix tools)
    * Joblib: Model serialization
    * Jupyter Notebook: Prototyping and analysis

## Setup and Installation

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/your-username/book_recommender.git](https://github.com/your-username/book_recommender.git)
    cd book_recommender
    ```

2.  **Create a virtual environment (recommended):**
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
    ```

3.  **Install the required dependencies:**
    ```bash
    pip install pandas numpy scikit-learn jupyterlab
    ```

## Usage

To reproduce the project results, run the Jupyter notebooks in the following order:

1.  **`notebooks/01-data-exploration.ipynb`**: An initial look at the raw datasets.
2.  **`notebooks/02-data-preprocessing.ipynb`**: This will process the raw data and create the `user_item_rating_matrix.libsvm` file in the `data/processed/` directory.
3.  **`notebooks/03-model-training-and-recommendation.ipynb`**: This will train the KNN model, save it to the `models/` directory, and generate the final `recommendations_output.csv` in the `output/` directory.

---
