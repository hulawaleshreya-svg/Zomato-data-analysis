# Zomato Restaurant Ratings: Data Analysis

Exploratory data analysis of Zomato restaurant listings using Python. The project cleans a dataset of about 123,000 rows, summarizes dining and delivery ratings, and compares average dining ratings across cities.

**Tools:** Python, Pandas, NumPy, Matplotlib, Seaborn, Jupyter Notebook

## Dataset

- File: `Zomato.csv` (a Zomato restaurant listings dataset; the CSV is not included in this repository, but all outputs and charts are saved in the notebook)
- Size: 123,657 rows × 12 columns
- Columns: Restaurant_Name, Dining_Rating, Delivery_Rating, Dining Votes, Delivery_Votes, Cuisine, Place_Name, City, Item_Name, Best_Seller, Votes, Prices
- Source: *add the link or name of where you got the dataset*

## Workflow

1. **Data collection:** loaded the CSV with Pandas.
2. **Data cleaning**
   - Found missing values: Dining_Rating (32,236), Delivery_Rating (1,280), Best_Seller (95,715).
   - Converted ratings to numeric and filled missing ratings with the column mean.
   - Converted `Prices` to integer and `Votes` to float.
   - Removed duplicate rows, leaving 101,530 rows.
3. **EDA:** summary statistics with `describe()` on dining rating, delivery rating, and dining votes.
4. **Visualization:** bar charts of average dining rating by city and a histogram of dining ratings, built with Matplotlib and Seaborn, with titles, labels, and a clean theme.
5. **Insights:** interpretation of each chart (below).

## Key numbers

| Metric | Value |
| --- | --- |
| Rows after removing duplicates | 101,530 |
| Mean dining rating | 3.82 |
| Mean delivery rating | 3.96 |
| Dining rating range | 2.5 to 4.8 |

## Charts

![Average dining rating by city](images/avg_dining_rating_by_city_final.png)

![Distribution of dining ratings](images/dining_rating_distribution.png)

## Insights

- Average dining ratings are close across locations, mostly between 3.5 and 4.0, so restaurant quality looks consistent. Magrath Road is the lowest and Malleshwaram the highest.
- Most dining ratings fall between 3.5 and 4.3. Very few restaurants are below 3.0 or above 4.5.
- Delivery ratings (mean 3.96) are slightly higher than dining ratings (mean 3.82).

## Limitations

- About 26% of dining ratings were missing and were filled with the mean (3.82). This creates the tall spike at about 3.8 in the histogram, so the distribution is not truly bell-shaped. A future version could drop those rows or analyze them separately.
- The bar chart's y-axis starts at 0, which makes the cities look more alike than they are. Zooming the axis to 3.0–4.5 would show the differences.
- Some entries in the `City` column are neighborhoods (for example Malleshwaram and Magrath Road), not cities, so the City column needs cleanup before a fair city comparison.

## How to run

1. Clone this repository:
   ```
   git clone https://github.com/hulawaleshreya-svg/zomato-data-analysis.git
   cd zomato-data-analysis
   ```
2. Install the requirements:
   ```
   pip install -r requirements.txt
   ```
3. Add a Zomato restaurant dataset with the same columns, saved as `Zomato.csv`, in the same folder as the notebook.
4. Open `Zomato_Analysis.ipynb` in Jupyter Notebook and run all cells.

To read the results without running anything, open the notebook on GitHub: every output and chart is already saved in it.

## Author

Shreya Hulawale | [LinkedIn](https://linkedin.com/in/shreya-hulawale-928259382) | [GitHub](https://github.com/hulawaleshreya-svg)
