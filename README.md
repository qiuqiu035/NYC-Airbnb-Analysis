# NYC-Airbnb-Analysis
NYC Airbnb Data Analysis Report
# NYC Airbnb Data Analysis Report

## Dataset
The dataset used in this analysis comes from [Kaggle: NYC Airbnb Open Data](https://www.kaggle.com/dgomonov/new-york-city-airbnb-open-data).  

- **Source**: Kaggle  
- **File Name**: `AB_NYC_2019.csv`  
- **Description**: This dataset contains Airbnb listings in New York City, including price, location, room type, and other details.  
- **Download Instructions**:
  1. Go to the [Kaggle dataset page](https://www.kaggle.com/dgomonov/new-york-city-airbnb-open-data).
  2. Click "Download".
  3. Place the `AB_NYC_2019.csv` file in the `data/` directory before running the analysis.

**Make sure to download the dataset before running the code!**


## 1. Data Cleaning
In the data cleaning phase, I first examined **missing values** and **duplicate records** in the dataset.

- **Handling Missing Values**
  - I found missing values in **`name`**, **`host_name`**, **`last_review`**, and **`reviews_per_month`**:
    - **`name` and `host_name`** had only a few missing values, so I **removed these rows**.
    - **`last_review` and `reviews_per_month`** had a significant number of missing values, so I handled them as follows:
      - Replaced missing values in **`last_review`** with **"No Review"**.
      - Replaced missing values in **`reviews_per_month`** with **0**.

- **Handling Duplicate Records**
  - After checking the dataset, I found **no duplicate records**, so no further action was needed.

## 2. SQL Data Queries

In the SQL analysis phase, I performed several queries to analyze **average prices, the number of listings in different areas, and the highest-priced listings**.

- **Average Price by Neighborhood**  
  - **Manhattan** had the highest average price of **$196.90**.  
  - **Bronx** had the lowest average price of **$87.47**.  

- **Number of Listings by Neighborhood**  
  - **Manhattan** had the highest number of listings, with **21,643 properties**.  
  - **Staten Island** had the fewest listings, with only **373 properties**.  

- **Most Expensive Listings**  
  - The **highest-priced listings in Queens, Manhattan, and Brooklyn** were all **$10,000**.  
  - **Bronx** had the **lowest highest-priced listing**, at **$2,500**.  

All SQL query results were **sorted in descending order** to facilitate comparison between neighborhoods.
hborhoods.

## 3. Key Insights

### **Key Statistics**
To better understand the Airbnb market, I first calculated key statistics:
- **Overall average price:** **$152.72**
- **Overall median price:** **$106.00**
- **Average price by neighborhood:**
  - **Manhattan** had the highest average price.
  - **Bronx** had the lowest average price.

These findings indicate that **Manhattan is significantly more expensive**, while **Bronx offers the most budget-friendly options**.


### **Price Distribution Analysis**
I plotted the **Airbnb price distribution** to observe pricing trends:
- **For listings priced between $0 and $110**, the number of listings steadily increased, with a **peak around $100 (approximately 5,500 listings)**.
- **Above $110, the number of listings dropped sharply**, reaching the lowest point at **$500**.

This suggests that **most Airbnb listings are within the affordable range**, while luxury listings above **$110** are relatively rare.


### **Price Comparison by Room Type**
I created a **bar chart comparing the average prices of different room types**, and found:
- **Entire home/apartment** had the highest average price at **$210**.
- **Private rooms** were more affordable, averaging around **$90**.
- **Shared rooms** were the cheapest, with an average price of **$70**.

These findings indicate that **renting an entire apartment is significantly more expensive**, while private and shared rooms offer more affordable options.


### **Geographic Distribution Analysis**
A **scatter plot of Airbnb listings in NYC** reveals clear regional differences:
- **Brooklyn has the highest density of listings**, particularly in **the eastern and southern areas**.
- **Manhattan listings are densely clustered**, especially near **Central Park**.
- **Queens has a broader but less dense distribution of listings**.
- **Staten Island has the fewest Airbnb listings**.
- **Bronx listings are relatively sparse but evenly distributed**.

These insights show that **Brooklyn and Manhattan are the hotspots for Airbnb listings**, while **Staten Island has the least activity**.


## 4. Conclusion

Through this Airbnb data analysis, we identified key insights regarding **pricing, listing density, and room type variations**:

**Manhattan is the most expensive neighborhood, while Bronx is the cheapest**
   - **Manhattan has the highest average price ($196.90)**, likely due to high demand for luxury accommodations.
   - **Bronx has the lowest average price ($87.47)**, making it the most budget-friendly option.

**Most Airbnb listings are priced around $100, with fewer listings above $110**
   - The **price distribution graph shows that most listings are concentrated at $100**, with around **5,500 properties** at this price point.
   - **Listings priced above $110 decrease sharply**, suggesting that **luxury rentals are less common**.

**Significant price differences between room types**
   - **Entire home/apartments are the most expensive (avg. $210)**, catering to travelers seeking privacy.
   - **Private rooms (avg. $90) offer a balance between affordability and comfort**.
   - **Shared rooms (avg. $70) are the most economical choice**.

**Brooklyn and Manhattan have the highest density of listings, while Staten Island has the fewest**
   - **Brooklyn and Manhattan dominate the Airbnb market**, with a significantly higher number of listings than other boroughs.
   - **Staten Island has the least Airbnb activity**, likely due to its remote location.


### **Business Implications**
**For Airbnb Hosts: How to Price Listings?**
- **If renting in Manhattan, hosts can set higher prices** due to strong market demand.
- **If renting in Bronx, competitive pricing is key** to attract budget-conscious guests.

**For Travelers: How to Choose a Listing?**
- **Budget travelers should consider staying in Bronx or shared rooms** for lower costs.
- **Long-term travelers or families may prefer entire apartments** for privacy, despite the higher cost.

This data analysis provides **valuable insights for both Airbnb hosts and travelers**, offering a data-driven approach to pricing and accommodation selection.