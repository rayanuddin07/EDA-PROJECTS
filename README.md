# 🎬 Netflix Movies & TV Shows — Exploratory Data Analysis

An end-to-end exploratory data analysis (EDA) of the Netflix titles dataset, covering data cleaning, feature engineering, and visualization to uncover trends in content type, country of production, genres, ratings, and release patterns.

## 📌 Overview

This project analyzes the Netflix catalog (movies and TV shows) to answer questions such as:
- How does the balance between Movies and TV Shows look?
- Which countries produce the most Netflix content?
- What are the most popular genres?
- How has content been added to Netflix over the years?
- How long are movies typically, and how are ratings distributed?

The analysis is done entirely in a Jupyter Notebook using Python's data science stack.

## 🗂️ Repository Contents

| File | Description |
|------|--------------|
| `netflix.ipynb` | Jupyter Notebook containing the full data cleaning, EDA, and visualization workflow |
| `netflix_file_is_cleaned.csv` | Final cleaned dataset exported after preprocessing |

## 🧹 Data Cleaning & Preprocessing

- Removed duplicate records
- Converted `date_added` to a proper datetime format
- Extracted `year_added` and `month_added` from `date_added`
- Filled missing values in `director`, `cast`, `country`, `rating`, and `duration`
- Parsed `duration` into a numeric field (`duration_num`) and a type label (`duration_type`: Minutes/Seasons)
- Extracted a primary `genre` from the `listed_in` column

## 📊 Exploratory Analysis

The notebook includes visualizations for:
- **Content type distribution** — Movies vs. TV Shows
- **Titles added by year** — growth of Netflix's catalog over time
- **Top 10 countries** producing Netflix content
- **Top 10 genres** on the platform
- **Movie duration distribution**
- **Content by release year** (Movies vs. TV Shows trend)
- **Ratings distribution**
- **Correlation heatmap** of numerical features
- A combined dashboard-style summary figure

## 🔍 Key Insights

- **Dataset size:** 8,807 titles across 12 original columns
- **Most common content type:** Movies (6,131) outnumber TV Shows (2,676)
- **Top content-producing country:** United States (3,649 titles), followed by India (972) and the UK (419)
- **Most common genre:** Dramas (1,600 titles)
- **Peak release year:** 2018
- **Average movie duration:** ~99.5 minutes

## 🛠️ Tech Stack

- Python 3
- pandas, numpy — data manipulation
- matplotlib, seaborn — data visualization
- Jupyter Notebook

## 🚀 Getting Started

1. Clone the repository:
   ```bash
   git clone https://github.com/<your-username>/<your-repo-name>.git
   cd <your-repo-name>
   ```

2. Install the required dependencies:
   ```bash
   pip install pandas numpy matplotlib seaborn jupyter
   ```

3. Launch the notebook:
   ```bash
   jupyter notebook netflix.ipynb
   ```

## 📁 Dataset

The dataset used is the popular [Netflix Movies and TV Shows dataset](https://www.kaggle.com/datasets/shivamb/netflix-shows), containing information on titles available on Netflix as of 2021, including cast, director, country, release year, rating, duration, and genre.

## 📄 License

This project is open source and available for learning and portfolio purposes.

---

⭐ If you found this project useful, consider giving it a star!
