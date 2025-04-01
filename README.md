# Yelp Recommendation System Project

This repository contains a collection of Jupyter Notebooks that implement various recommendation system approaches on the Yelp dataset. The project is organized into different notebooks to streamline data processing and avoid repetitive code.

---

## Repository Structure

- **Yelp_00_dataload&cleaning.ipynb**  
  - **Purpose:** Loads, cleans, and samples the Yelp dataset.
  - **Contents:**  
    - Data ingestion from `review.json`, `business.json`, `user.json`, `checkin.json`, and `tip.json`.
    - Data cleaning and preprocessing.
    - Sampling techniques to create manageable subsets.
  - **Usage:** Run this notebook first to prepare the data for subsequent recommendation models.
 
- **Yelp_01_EDA.ipynb**
    - **Purpose:** Exploratory analysis of the Yelp Dataset. 
    - **Usage:** Use the pre-processed data from Yelp_01. Run this notebook to explore the dataset.
      
- **Yelp_02_non_personalized.ipynb**  
  - **Purpose:** Implements non-personalized recommendation methods (e.g., random, popular, demographic filtering).
  - **Usage:** Use the pre-processed data from Yelp_01. This notebook provides previews with output included.

- **Yelp_03_collaborative_filtering.ipynb**  
  - **Purpose:** Implements collaborative filtering approaches (memory-based, model-based, SVD, etc.).
  - **Usage:** Ensure you run the data load and cleaning notebook (Yelp_01) before running this file.

- **Yelp_04_content_based.ipynb**  
  - **Purpose:** Implements content-based recommendation techniques.
  - **Usage:** Reuse the data prepared in Yelp_01 for this analysis.

- **Yelp_04.1_BERT.ipynb**  
  - **Purpose:** Implements content-based recommendation technique: BERT.
  - **Usage:** Reuse the data prepared in Yelp_01 for this analysis.
 
- **Yelp_05_hybrid_context_based.ipynb**  
  - **Purpose:** Implements context-aware recommenders that consider additional contextual signals.
  - **Usage:** Again, the cleaned and sampled data from Yelp_01 is required.

> **Note:** Each notebook is organized to include both code and output previews. If you wish to re-run any recommender notebook (e.g., collaborative filtering), make sure to execute the code from **Yelp_01_dataload&cleaning.ipynb** first to initialize and load the necessary datasets.

---

## Required Libraries

Make sure you have the following Python libraries installed:

- **pandas** – Data manipulation and analysis  
  `pip install pandas`
- **numpy** – Numerical computing  
  `pip install numpy`
- **matplotlib** and **seaborn** – Data visualization  
  `pip install matplotlib seaborn`
- **scikit-learn** – Machine learning tools (for similarity metrics, etc.)  
  `pip install scikit-learn`
- **surprise** – Collaborative filtering algorithms (SVD, etc.)  
  `pip install scikit-surprise`
- (Optional) **pyarrow** or **fastparquet** – For efficient Parquet file handling if you choose to save data in Parquet format  
  `pip install pyarrow`

You can install all required packages using pip and a requirements file if desired.

---

## Running the Notebooks

1. **Start with Yelp_01_dataload&cleaning.ipynb:**  
   - This notebook handles all data loading, cleaning, and sampling tasks.  
   - Run this notebook to generate the processed DataFrames needed by all subsequent notebooks.

2. **Proceed to the Recommender Notebooks:**  
   - Depending on which recommendation system you want to explore (non-personalized, collaborative filtering, content-based, or context-based), open the corresponding notebook.
   - Before running any recommender code, ensure that the outputs (cleaned DataFrames) from Yelp_01 are loaded into the notebook environment.
   - Each recommender notebook is designed to use the pre-processed data, avoiding redundant code and ensuring consistency.

---

## Project Goals and Value Proposition

- **Enhanced User Experience:**  
  The models aim to provide personalized restaurant recommendations, reducing search time and increasing user engagement.

- **Business Impact:**  
  Improved recommendation accuracy translates into higher conversion rates and increased customer satisfaction.

- **Scalable Architecture:**  
  The modular design of the repository allows for easy updates and integration of additional recommendation techniques (e.g., hybrid models, metadata integration).

---
