# Airbnb-Data-analysis-EDA-Project

## Objective
The objective of this project is to conduct a comprehensive **Exploratory Data Analysis (EDA)** on the Airbnb dataset to uncover key patterns, pricing behaviors, and listing trends.  

Using Python libraries such as **Pandas**, **NumPy**, **Matplotlib**, and **Seaborn**, this project focuses on:

- **Data Cleaning**: Handling missing values, correcting inconsistencies, and preparing the dataset for analysis.  
- **Feature Understanding**: Examining individual features to understand their distributions and relationships.  
- **Visual Exploration**: Creating insightful visualizations to identify trends and patterns in the Airbnb rental market.  

The ultimate goal is to derive meaningful insights that can help both **guests** and **hosts** make informed decisions.  

## Dataset

The dataset contains **20,765 entries** and **22 features**, providing detailed information about Airbnb listings. Key features include:

- **id**: Unique identifier for each listing  
- **name**: Title of the Airbnb listing  
- **host_name**: Name of the host  
- **neighborhood_group**: Borough where the listing is located  
- **latitude / longitude**: Geolocation coordinates of the listing  
- **price**: Nightly rental price  
- **room_type**: Type of accommodation (e.g., entire home, private room)  
- **reviews_per_month**: Average number of reviews per month for the listing  
- **availability_365**: Number of days the listing is available in a year  

> Note: The dataset contains additional features not listed here, which are used in the exploratory analysis.

## Steps and Workflow

The project followed a structured workflow to perform a thorough Exploratory Data Analysis (EDA) on the Airbnb dataset:

### 1. Initial Data Exploration
- Checked column names, data types, and overall structure using `.info()` and `.describe()`.  
- Identified missing values, incorrect types (e.g., bedrooms, rating), and potential outliers.  

### 2. Data Cleaning
- Converted object columns to numeric where required (e.g., bedrooms, rating).  
- Handled missing values through conversion, dropping, or coercing invalid entries.  
- Removed inconsistencies and prepared clean numerical columns for correlation analysis.  
- Filtered data using conditions like `data['price'] > 1500` to create subsets.  

### 3. Univariate Analysis
- Used **histograms** (`sns.histplot`) with KDE curves to study distributions of price, minimum nights, availability, etc.  
- Performed **boxplots** to detect outliers and understand data spread.  

### 4. Bivariate Analysis
- **Scatterplots** to explore numeric–numeric relationships (e.g., price vs reviews, price vs latitude/longitude, price vs availability).  
- **Barplots and boxplots** for category–numeric relationships:
  - room_type vs price  
  - neighbourhood_group vs price  
  - bedrooms vs price  
- **Countplots** to analyze the distribution of room types across neighbourhood groups.  
- **Pairplots** to visualize interactions between major numeric variables: `price`, `minimum_nights`, `number_of_reviews`, `reviews_per_month`, `availability_365`.  

### 5. Multivariate & Correlation Analysis
- Created a **correlation heatmap** of all numeric columns.  
- Identified relationships between price and other numerical factors.  
- Analyzed top neighbourhoods and compared price patterns using filtered subsets.  

### 6. Feature Engineering & Useful Calculations
- Added new analytical calculations to enhance insights:
  - **Price per bedroom**: `price / bedrooms`  
  - **Review rate**: `number_of_reviews / minimum_nights`  
  - **Occupancy rate**: `1 - availability_365 / 365`  
  - **Estimated revenue**: `price * (occupancy_rate * 365)`  
   

These features added depth and professionalism to the project analysis.  

### 7. Final Visualization & Interpretation
- Interpreted all plots and numerical results to form meaningful insights about:
  - Pricing patterns  
  - Influence of neighbourhoods  
  - Availability trends  
  - Customer behavior

  ##  Key Findings and Insights

Based on the visualizations, filters, and calculations performed during the EDA, the following insights were derived:

- **Price Variations Across Neighbourhoods**
  - Some boroughs consistently show higher pricing due to popularity or demand.
  - Less popular areas generally have lower prices, offering more affordable options.

- **Influence of Room Type on Price**
  - Entire homes are the most expensive listings.  
  - Private rooms are moderately priced, while shared rooms are the cheapest.  

- **Relationship Between Reviews and Price**
  - Listings with more reviews generally have lower prices.  
  - Affordable stays tend to attract more bookings and accumulate more reviews.  

- **Availability Patterns**
  - Cheaper listings are booked more frequently.  
  - High-priced listings often remain available for more days in the year.  

- **Bedrooms vs. Price**
  - Positive correlation: listings with more bedrooms usually have higher prices.  
  - Extreme outliers suggest either luxury properties or data entry inconsistencies.  

- **Correlation Analysis**
  - Weak-to-moderate correlations between numeric variables and price.  
  - No single numeric factor fully determines listing price.  

- **Insights from Feature Engineering**
  - Calculated features like **estimated revenue** and **occupancy rate** provide operational insights.  
  - These metrics highlight which listings could potentially earn more annually.  

- **Geolocation Analysis**
  - Scatter plots of latitude and longitude show clusters of higher-priced listings.  
  - Certain coordinates correspond to premium areas, reflecting location-based price differences.

## Recommendations

### For Guests
- Prioritize listings with consistently high ratings to ensure a reliable stay.  
- Explore neighborhoods slightly outside busy areas for better value while staying accessible.  

### For Hosts
- Encourage guests to leave detailed reviews to build trust and attract more bookings.  
- Use dynamic pricing based on seasonality and neighborhood trends to remain competitive.  

## Author
- Name: Febina  
- Email: febinasaleemr@gmail.com
- linkedin: [linkedin](https://www.linkedin.com/in/febina-s-083436347/)




