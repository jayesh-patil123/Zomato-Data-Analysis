# Zomato-Data-Analysis

Project Overview:
    In this project, you're working with a Zomato restaurant dataset containing information about restaurants in Bangalore. The goal is to clean the data, preprocess it, perform various exploratory data analysis (EDA) tasks, and generate useful insights. The dataset includes details about restaurant ratings, costs, locations, cuisines, and more. Throughout the project, you perform data cleaning, transformation, and visualization to better understand the data and its patterns.

Steps Taken in the Project:
    1. Import Libraries:
    You start by importing the necessary libraries:
    
    Pandas (pd) for data manipulation.
    Numpy (np) for numerical operations.
    Seaborn (sns) and Matplotlib (plt) for creating static visualizations.
    Plotly and Cufflinks for interactive visualizations.
    2. Reading the Data:
    You read the Zomato dataset using pd.read_csv(r"zomato.csv") and load it into a Pandas DataFrame df.
    3. Exploring the Data:
    You perform basic exploration:
    
    Shape and Info: Checking the shape of the dataset (df.shape), and understanding data types and missing values using df.info().
    Missing Data: Identifying the missing values in the dataset and visualizing them using a heatmap (sns.heatmap()).
    Initial Insights: You look at the first few rows of the data with df.head() to get an overview of the content.
    4. Data Cleaning & Preprocessing:
    Here’s where significant cleaning and preprocessing happens:
    
    Removing Unnecessary Columns:
    You delete columns that are not useful for analysis (url, address, phone).
    Removing Duplicates:
    You remove any duplicate rows using df.drop_duplicates().
    Handling Missing Values:
    You remove rows with any missing values using df.dropna().
    You also drop the dish_liked column due to its many missing values.
    A heatmap is used again to check the missing values after cleaning.
    Renaming Columns:
    You rename some columns to make them more meaningful and easier to work with, e.g., approx_cost(for two people) to cost, listed_in(type) to type, and listed_in(city) to city.
    5. Data Transformation:
    Cleaning the cost Column:
    The cost column is initially a string type. You remove commas (',') from the values, then convert it to a float for easier numerical analysis.
    Cleaning the rate Column:
    The rate column contains values like "NEW" and "-". You clean it by removing those rows and then stripping off the /5 to retain only the numeric part of the rating. The column is then converted to float type.
    6. Exploratory Data Analysis (EDA):
    With the cleaned data, you proceed with several analyses and visualizations:
    
    Pie Charts:
    
    You plot pie charts for online_order and book_table to see the distribution of these features in the dataset.
    Count Plots:
    
    You create count plots for categorical columns (online_order, book_table, type, and city) to understand the distribution of restaurant features across different categories.
    Popular Restaurants:
    
    You identify the most popular restaurant names and types using bar charts.
    Boxplots for Numeric Columns:
    
    You create boxplots for numeric columns like cost, rate, and votes to visualize the distribution and detect outliers.
    Expensive Restaurants:
    
    You filter and display expensive restaurants (cost > 3000) and investigate their characteristics, such as whether they take online orders, whether table booking is available, and their ratings.
    You also identify where most of these expensive restaurants are located and what type of restaurants they are (e.g., Fine Dining).
    Top-rated Restaurants:
    
    You sort restaurants by votes to find the top 10 restaurants with the highest number of votes.
    Restaurants by Location:
    
    You plot the number of restaurants per location, and you explore the locations of popular and expensive restaurants.
    Cuisines:
    
    You identify the most popular cuisines in Bangalore by plotting a bar chart of the cuisines column.
    7. Advanced Analysis:
    Average Cost by Location:
    
    You group restaurants by their location and calculate the mean cost for each location. The results are plotted as a bar chart to see which locations have higher or lower average costs.
    Best Economical Restaurants:
    
    You filter out restaurants that have a cost of 100 or less and a rating of 4 or higher to identify the best inexpensive restaurants.
    Best Restaurants by Cost & Location:
    
    You create a function top_rest(res_cost, res_loc) where the user inputs a maximum cost and location, and the function returns the best restaurants based on the conditions of cost being less than or equal to the entered value and rating being 4 or higher.
    The filtered results are sorted by rating.
    8. Visualization of Final Results:
    Scatter Plots:
    A scatter plot is created to show the relationship between the rating and the cost of restaurants, with colors indicating whether they allow online ordering and markers showing whether table booking is available.

      Code Explanation (Step-by-step):
    Imports and Data Loading: Libraries are imported, and the dataset is read.
    Data Exploration: Basic exploration is done using df.head() and df.info(), and missing values are checked using df.isnull().
    Data Cleaning:
    Dropping unnecessary columns, removing duplicates, and handling missing values.
    Data Transformation:
    Conversion of columns (cost and rate) to appropriate types.
    Exploratory Data Analysis (EDA):
    Various plots (pie, count, box) are used to analyze the data and discover trends.
    Advanced Analysis: Deeper insights into expensive restaurants, popular cuisines, and the best economical restaurants are explored.
    Custom Filtering Function: The top_rest function allows users to input criteria (cost, location) to find the best restaurants in their area.

Brief Description for Presentation:
      In this project, I analyzed the Zomato Bangalore restaurant dataset. The goal was to clean the data, preprocess it, and gain meaningful insights into restaurant trends in Bangalore. 
      The steps included:

    Data Cleaning: Removing unnecessary columns, handling missing data, and transforming specific columns like cost and rate.
    Exploratory Data Analysis: Visualizing key patterns using various plots (pie charts, count plots, box plots) and identifying relationships between features like restaurant cost, ratings, and location.
    Insights & Recommendations: Identified expensive restaurants and locations where most of these restaurants are concentrated.
    Analyzed the distribution of cuisines and ratings across different types of restaurants.
    Created an interactive filtering function to help users find the best restaurants based on their budget and location.
