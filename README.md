

---

# 📊 Netflix Data Analysis

This project provides an exploratory data analysis (EDA) of a Netflix dataset using Python and Pandas. It focuses on gaining insights into Netflix's content library, such as distribution by genre, content type, release year, and more.

---

## 📁 Dataset

The dataset contains metadata about Netflix titles, including:

* Title
* Genre(s)
* Type (Movie or TV Show)
* Release Year
* Duration
* Country
* Rating
* Cast & Crew

> Note: The `'Genre'` column often contains multiple genres per title, separated by commas.

---

## 🔍 Key Features of the Analysis

* **Data Cleaning**: Handling missing values and inconsistent formats.
* **Genre Processing**:

  * Splitting multiple genres into lists
  * Exploding the `'Genre'` column to analyze each genre independently
* **Content Breakdown**:

  * Distribution of content by type (Movie/TV Show)
  * Year-wise release trends
  * Most frequent genres
* **Visualizations** (optional depending on your code):

  * Bar plots
  * Pie charts
  * Histograms

---

## 🛠 Technologies Used

* Python 🐍
* Pandas 📊
* Jupyter Notebook 📒
* Matplotlib / Seaborn (optional for visualizations)

---

## 🚀 How to Use

1. Clone the repository:

   ```bash
   git clone https://github.com/yourusername/netflix-data-analysis.git
   cd netflix-data-analysis
   ```

2. Open the notebook:

   ```bash
   jupyter notebook "NETFLIX DATA ANALYSIS.ipynb"
   ```

3. Run the cells to follow the analysis.

---

## 📝 Genre Column Exploding – Highlight

To enable granular analysis by genre, the following transformation was done:

```python
df['Genre'] = df['Genre'].str.split(', ')
df = df.explode('Genre').reset_index(drop=True)
```

This allows each row to represent a single genre per title, enabling better filtering and aggregation.

---

## 📈 Possible Extensions

* Add visualizations for genre distribution.
* Perform sentiment analysis on descriptions.
* Build a recommendation system based on genres or content type.

---

## 📚 License

This project is open-source and available under the [MIT License](LICENSE).

---


