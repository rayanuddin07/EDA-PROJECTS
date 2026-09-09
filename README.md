# 📊 Data Analysis Portfolio

A collection of exploratory data analysis (EDA) projects built with Python. Each project covers data cleaning, feature engineering, and visualization on a different real-world dataset — from streaming content to healthcare, housing, retail, and historical survival data.

## 🗂️ Projects

| Project | Dataset | Notebook | Cleaned Data |
|---|---|---|---|
| 🎬 [Netflix](#-netflix-movies--tv-shows) | Netflix Titles | `netflix.ipynb` | `netflix_file_is_cleaned.csv` |
| 🏠 [Airbnb NYC](#-airbnb-nyc-listings) | AB_NYC_2019 | `airbnb.ipynb` | `airbnb.csv` |
| 🏥 [Medical Appointments](#-medical-appointment-no-shows) | KaggleV2-May-2016 | `medical.ipynb` | `medical.csv` |
| 🛒 [Superstore Sales](#-superstore-sales) | Superstore Train | `superstore.ipynb` | `superstore_cleaned.csv` |
| 🚢 [Titanic](#-titanic-survival-analysis) | Titanic-Dataset | `titanic.ipynb` | `titanic_is_cleaned.csv` |

---

## 🎬 Netflix Movies & TV Shows

Analysis of Netflix's content catalog to explore content type, countries, genres, and release trends.

**Cleaning steps:** removed duplicates, parsed `date_added` into datetime, extracted `year_added`/`month_added`, filled missing `director`/`cast`/`country`/`rating`/`duration`, split `duration` into numeric + type, extracted primary `genre`.

**Key insights:**
- Dataset: 8,807 titles, 12 original columns
- Movies (6,131) far outnumber TV Shows (2,676)
- Top country: United States (3,649), followed by India (972) and the UK (419)
- Most common genre: Dramas (1,600 titles)
- Peak release year: 2018
- Average movie duration: ~99.5 minutes

---

## 🏠 Airbnb NYC Listings

Analysis of NYC Airbnb listings to explore pricing patterns across boroughs and room types.

**Cleaning steps:** filled missing `name` values, parsed `last_review` into datetime, removed duplicates, applied log transform to `price` (`price_log`), engineered `price_category` and `review_rate` features.

**Key insights:**
- Dataset: 48,895 listings, 16 original columns
- Manhattan has the highest average price (~$197/night), followed by Brooklyn (~$124)
- Staten Island, Queens, and the Bronx are notably cheaper
- Price distribution is heavily right-skewed, hence the log transformation

---

## 🏥 Medical Appointment No-Shows

Analysis of Brazilian medical appointment records to understand what drives patients to miss scheduled appointments.

**Cleaning steps:** renamed inconsistent columns (`Hipertension` → `Hypertension`, `No-show` → `No_show`), parsed `ScheduledDay`/`AppointmentDay` into datetime, clipped invalid ages, engineered `WaitingTimeDays`, `AgeGroup`, and `WaitingTimeCategory`.

**Key insights:**
- Dataset: 110,527 appointments, 14 original columns
- Overall no-show rate: **20.19%**
- Teens (26.1%) and young adults (23.8%) no-show more than seniors (15.2%)
- Patients who received an SMS reminder had a *higher* no-show rate (27.6% vs 16.7%) — likely reflects reminder timing/targeting rather than reminders causing no-shows
- No-shows have a notably longer average waiting time (14.8 days) vs shows (7.75 days)

---

## 🛒 Superstore Sales

Analysis of retail order data to uncover sales trends across categories, sub-categories, and time.

**Cleaning steps:** parsed `Order Date`/`Ship Date` into datetime, engineered `Order_Year`, `Order_Month`, `Order_Quarter`, `Shipping_Days`, and `Sales_Category`, ran data quality and outlier checks.

**Key insights:**
- Dataset: 9,800 orders, spanning 2015-01-03 to 2018-12-30
- Total sales: **$2,261,536.78** | Average sales per order: $230.77
- Average shipping time: 3.96 days
- Technology leads in average sale value ($456.40/order); Office Supplies leads in order volume (5,909 orders)
- Phones and Chairs are the top-selling sub-categories by revenue

---

## 🚢 Titanic Survival Analysis

Classic analysis of Titanic passenger data to identify factors associated with survival.

**Cleaning steps:** filled missing `Age` with median, engineered `HasCabin`, `AgeGroup`, `FamilySize`, `IsAlone`, and `FareCategory` bins.

**Key insights:**
- Dataset: 891 passengers, 12 original columns
- Overall survival rate: **38.38%**
- Women survived at far higher rates than men (74.2% vs 18.9%)
- 1st class passengers had the highest survival rate (63.0%) vs 3rd class (24.2%)
- Children had the highest survival rate by age group (57.4%), seniors the lowest (26.9%)

---

## 🛠️ Tech Stack

- **Python 3**
- **pandas, numpy** — data manipulation & feature engineering
- **matplotlib, seaborn** — data visualization
- **Jupyter Notebook**

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

3. Launch any notebook:
   ```bash
   jupyter notebook netflix.ipynb
   ```

## 📁 Datasets

- **Netflix** — [Netflix Movies and TV Shows](https://www.kaggle.com/datasets/shivamb/netflix-shows) (Kaggle)
- **Airbnb** — [New York City Airbnb Open Data (AB_NYC_2019)](https://www.kaggle.com/datasets/dgomonov/new-york-city-airbnb-open-data) (Kaggle)
- **Medical** — [Medical Appointment No Shows](https://www.kaggle.com/datasets/joniarroba/noshowappointments) (Kaggle)
- **Superstore** — [Sample Superstore Sales](https://www.kaggle.com/datasets/vivek468/superstore-dataset-final) (Kaggle)
- **Titanic** — [Titanic - Machine Learning from Disaster](https://www.kaggle.com/c/titanic) (Kaggle)

## 📄 License

This project is open source and available for learning and portfolio purposes.

---

⭐ If you found this portfolio useful, consider giving it a star!
