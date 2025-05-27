# Job Market Salary Prediction using PySpark

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/)
[![PySpark](https://img.shields.io/badge/PySpark-3.0%2B-orange.svg)](https://spark.apache.org/docs/latest/api/python/)

## Abstract

In the era of big data, accurate job market analysis is essential for understanding employment trends, forecasting salaries, and aiding job seekers and organizations in informed decision-making. This project builds a predictive model to estimate job salaries based on job titles and locations using various machine learning algorithms implemented in **PySpark**.

## Table of Contents

- [Objective](#objective)
- [Proposed System](#proposed-system)
- [Benchmarking Results](#benchmarking-results)
- [Technologies Used](#technologies-used)
- [Setup & Usage](#setup--usage)
- [Project Structure](#project-structure)
- [Future Enhancements](#future-enhancements)
- [Contributors](#contributors)
- [License](#license)

## Objective

- Analyze the job market focusing on salary prediction based on job title and location.
- Benchmark multiple machine learning models to determine the most efficient and accurate one.
- Evaluate models using training time, prediction time, and RMSE.
- Identify the best model for deployment.
- Fully implement the system in **PySpark** for scalability.
- Predict salaries for unseen job titles and locations, offering insights for job seekers, HR professionals, and policymakers.

## Proposed System

1. **Data Scraping**  
   - Scraped job listings from platforms like Glassdoor and Indeed.
   - Extracted fields: job title, job location, salary estimates, company name, and job description.
   - Used Python tools like **BeautifulSoup** and **Selenium**.

2. **Data Preprocessing**  
   - Cleaned and structured the data using **PySpark**.
   - Handled missing values, duplicates, and irrelevant data.
   - Encoded categorical features and split the dataset into training and testing sets.

3. **Model Benchmarking**  
   - Implemented and evaluated:  
     - Linear Regression (LR)
     - Random Forest (RF)
     - Decision Tree (DT)
     - Gradient Boosted Trees (GBT)
     - Support Vector Machine (SVM)
     - XGBoost
     - K-Nearest Neighbors (KNN)
     - Multi-layer Perceptron (MLP)
   - Evaluation Metrics:  
     - **Training Time**
     - **Prediction Time**
     - **Root Mean Square Error (RMSE)**

4. **Model Selection and Deployment**  
   - **XGBoost** was selected based on the best RMSE and computational efficiency.
   - Deployed the XGBoost model for predicting unseen salary data.

5. **Implementation Platform**  
   - Complete implementation using **PySpark** to leverage distributed computing for handling large-scale datasets.

## Benchmarking Results

| Model              | RMSE      | Training Time (s) | Prediction Time (s) |
|--------------------|-----------|-------------------|---------------------|
| XGBoost            | 24,586.38 | 0.084             | 0.0018              |
| Linear Regression  | ...       | ...               | ...                 |
| Random Forest      | ...       | ...               | ...                 |
| Decision Tree      | ...       | ...               | ...                 |
| GBT                | ...       | ...               | ...                 |
| SVM                | ...       | ...               | ...                 |
| KNN                | ...       | ...               | ...                 |
| MLP                | ...       | ...               | ...                 |

> **Note:** XGBoost achieved the lowest RMSE and fastest training/prediction times.

## Technologies Used

- PySpark
- Python (BeautifulSoup, Selenium)
- Machine Learning Algorithms (XGBoost, RF, DT, etc.)
- Big Data Handling

## Setup & Usage

1. **Clone the repository**
   ```sh
   git clone https://github.com/Abishek7952/Job-Market-Analysis-using-Bigdata-Tools.git
   cd Job-Market-Analysis-using-Bigdata-Tools
   ```

2. **Install dependencies**
   ```sh
   pip install -r requirements.txt
   ```

3. **Run the notebook**
   - Open `Job Market Analysis.ipynb` in Jupyter or Colab.

4. **Dataset**
   - Place your dataset as `indeed_scraped_dataset.csv` in the project root.

## Project Structure

```
.
├── Job Market Analysis.ipynb
├── indeed_scraped_dataset.csv
├── README.md
├── LICENSE
├── requirements.txt
└── ...
```

## Future Enhancements

- Deploy model predictions as RESTful APIs for easy integration.
- Use real-time job market data feeds.
- Extend prediction features (e.g., based on required skills, company reputation).

## Contributors

- [Abishek R](https://github.com/Abishek7952/Job-Market-Analysis-using-Bigdata-Tools) - Developer

Open to collaborations and improvements. Feel free to contribute!

## License

This project is licensed under the [MIT License](LICENSE).
