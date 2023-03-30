Housing Rental Analysis for San Francisco
In this challenge, your job is to use your data visualization skills, including aggregation, interactive visualizations, and geospatial analysis, to find properties in the San Francisco market that are viable investment opportunities.

Instructions
Use the san_francisco_housing.ipynb notebook to visualize and analyze the real-estate data.

Note that this assignment requires you to create a visualization by using hvPlot and GeoViews. Additionally, you need to read the sfo_neighborhoods_census_data.csv file from the Resources folder into the notebook and create the DataFrame that you’ll use in the analysis.

The main task in this Challenge is to visualize and analyze the real-estate data in your Jupyter notebook. Use the san_francisco_housing.ipynb notebook to complete the following tasks:

Calculate and plot the housing units per year.

Calculate and plot the average prices per square foot.

Compare the average prices by neighborhood.

Build an interactive neighborhood map.

Compose your data story.

Calculate and Plot the Housing Units per Year
For this part of the assignment, use numerical and visual aggregation to calculate the number of housing units per year, and then visualize the results as a bar chart. To do so, complete the following steps:

Use the groupby function to group the data by year. Aggregate the results by the mean of the groups.

Use the hvplot function to plot the housing_units_by_year DataFrame as a bar chart. Make the x-axis represent the year and the y-axis represent the housing_units.

Style and format the line plot to ensure a professionally styled visualization.

Note that your resulting plot should appear similar to the following image:

A screenshot depicts an example of the resulting bar chart.

Answer the following question:

What’s the overall trend in housing units over the period that you’re analyzing?
Calculate and Plot the Average Sale Prices per Square Foot
For this part of the assignment, use numerical and visual aggregation to calculate the average prices per square foot, and then visualize the results as a bar chart. To do so, complete the following steps:

Group the data by year, and then average the results. What’s the lowest gross rent that’s reported for the years that the DataFrame includes?

Create a new DataFrame named prices_square_foot_by_year by filtering out the “housing_units” column. The new DataFrame should include the averages per year for only the sale price per square foot and the gross rent.

Use hvPlot to plot the prices_square_foot_by_year DataFrame as a line plot.

Hint This single plot will include lines for both sale_price_sqr_foot and gross_rent.

Style and format the line plot to ensure a professionally styled visualization.

Note that your resulting plot should appear similar to the following image:

A screenshot depicts an example of the resulting plot.

Use both the prices_square_foot_by_year DataFrame and interactive plots to answer the following questions:

Did any year experience a drop in the average sale price per square foot compared to the previous year?

If so, did the gross rent increase or decrease during that year?

Compare the Average Sale Prices by Neighborhood
For this part of the assignment, use interactive visualizations and widgets to explore the average sale price per square foot by neighborhood. To do so, complete the following steps:

Create a new DataFrame that groups the original DataFrame by year and neighborhood. Aggregate the results by the mean of the groups.

Filter out the “housing_units” column to create a DataFrame that includes only the sale_price_sqr_foot and gross_rent averages per year.

Create an interactive line plot with hvPlot that visualizes both sale_price_sqr_foot and gross_rent. Set the x-axis parameter to the year (x="year"). Use the groupby parameter to create an interactive widget for neighborhood.

Style and format the line plot to ensure a professionally styled visualization.

Note that your resulting plot should appear similar to the following image:

A screenshot depicts an example of the resulting plot.

Use the interactive visualization to answer the following question:

For the Anza Vista neighborhood, is the average sale price per square foot for 2016 more or less than the price that’s listed for 2012?
Build an Interactive Neighborhood Map
For this part of the assignment, explore the geospatial relationships in the data by using interactive visualizations with hvPlot and GeoViews. To build your map, use the sfo_data_df DataFrame (created during the initial import), which includes the neighborhood location data with the average prices. To do all this, complete the following steps:

Read the neighborhood_coordinates.csv file from the Resources folder into the notebook, and create a DataFrame named neighborhood_locations_df. Be sure to set the index_col of the DataFrame as “Neighborhood”.

Using the original sfo_data_df Dataframe, create a DataFrame named all_neighborhood_info_df that groups the data by neighborhood. Aggregate the results by the mean of the group.

Review the two code cells that concatenate the neighborhood_locations_df DataFrame with the all_neighborhood_info_df DataFrame. Note that the first cell uses the Pandas concat function to create a DataFrame named all_neighborhoods_df. The second cell cleans the data and sets the “Neighborhood” column. Be sure to run these cells to create the all_neighborhoods_df DataFrame, which you’ll need to create the geospatial visualization.

Using hvPlot with GeoViews enabled, create a points plot for the all_neighborhoods_df DataFrame. Be sure to do the following:

Set the geo parameter to True.
Set the size parameter to “sale_price_sqr_foot”.
Set the color parameter to “gross_rent”.
Set the frame_width parameter to 700.
Set the frame_height parameter to 500.
Include a descriptive title.
Note that your resulting plot should appear similar to the following image:

A screenshot depicts an example of a scatter plot created with hvPlot and GeoViews.

Use the interactive map to answer the following question:

Which neighborhood has the highest gross rent, and which has the highest sale price per square foot?
Compose Your Data Story
Based on the visualizations that you created, answer the following questions:

How does the trend in rental income growth compare to the trend in sales prices? Does this same trend hold true for all the neighborhoods across San Francisco?

What insights can you share with your company about the potential one-click, buy-and-rent strategy that they're pursuing? Do neighborhoods exist that you would suggest for investment, and why?

# Import the required libraries and dependencies
# Using the read_csv function and Path module, create a DataFrame 
# by importing the sfo_neighborhoods_census_data.csv file from the Resources folder
# Review the first and last five rows of the DataFrame
For this part of the assignment, use numerical and visual aggregation to calculate the number of housing units per year, and then visualize the results as a bar chart. To do so, complete the following steps:

Use the groupby function to group the data by year. Aggregate the results by the mean of the groups.

Use the hvplot function to plot the housing_units_by_year DataFrame as a bar chart. Make the x-axis represent the year and the y-axis represent the housing_units.

Style and format the line plot to ensure a professionally styled visualization.

Note that your resulting plot should appear similar to the following image:

A screenshot depicts an example of the resulting bar chart.

Answer the following question:

What’s the overall trend in housing units over the period that you’re analyzing?
# pandas data filtering
# specific neighborhood? specific year?
# 3 steps for filtering dataframes
# 1. pick a col
# 2. create the true false condition that you want, create the filer
# this creates a series of true and false values?
# doesnt help because its not the full dataframe?
# 3.df[filter]
 #if you true or false values into the rows of the df. return True only
 # 1 step
Step 1: Use the groupby function to group the data by year. Aggregate the results by the mean of the groups.
.groupby('year')
# Create a numerical aggregation that groups the data by the year and then averages the results.
# to select with loc or ilov
# Review the DataFrame
Step 2: Use the hvplot function to plot the housing_units_by_year DataFrame as a bar chart. Make the x-axis represent the year and the y-axis represent the housing_units.
Step 3: Style and format the line plot to ensure a professionally styled visualization.
# Create a visual aggregation explore the housing units by year
Step 5: Answer the following question:
Question: What is the overall trend in housing_units over the period being analyzed?

Answer: it has a increasing trend.

Calculate and Plot the Average Sale Prices per Square Foot
For this part of the assignment, use numerical and visual aggregation to calculate the average prices per square foot, and then visualize the results as a bar chart. To do so, complete the following steps:

Group the data by year, and then average the results. What’s the lowest gross rent that’s reported for the years that the DataFrame includes?

Create a new DataFrame named prices_square_foot_by_year by filtering out the “housing_units” column. The new DataFrame should include the averages per year for only the sale price per square foot and the gross rent.

Use hvPlot to plot the prices_square_foot_by_year DataFrame as a line plot.

Hint This single plot will include lines for both sale_price_sqr_foot and gross_rent.

Style and format the line plot to ensure a professionally styled visualization.

Note that your resulting plot should appear similar to the following image:

A screenshot depicts an example of the resulting plot.

Use both the prices_square_foot_by_year DataFrame and interactive plots to answer the following questions:

Did any year experience a drop in the average sale price per square foot compared to the previous year?

If so, did the gross rent increase or decrease during that year?

Step 1: Group the data by year, and then average the results.
gross_rent
# Create a numerical aggregation by grouping the data by year and averaging the results
# Review the resulting DataFrame
Question: What is the lowest gross rent reported for the years included in the DataFrame?

Answer: lowest gross rent reported is in 2010, 1239.00

Step 2: Create a new DataFrame named prices_square_foot_by_year by filtering out the “housing_units” column. The new DataFrame should include the averages per year for only the sale price per square foot and the gross rent.
# Filter out the housing_units column, creating a new DataFrame 
# Keep only sale_price_sqr_foot and gross_rent averages per year
# Review the DataFrame
gross_rent_by_year
Step 3: Use hvPlot to plot the prices_square_foot_by_year DataFrame as a line plot.
Hint This single plot will include lines for both sale_price_sqr_foot and gross_rent

Step 4: Style and format the line plot to ensure a professionally styled visualization.
# Plot prices_square_foot_by_year. 
# Inclued labels for the x- and y-axes, and a title.
prices_square_foot_by_year * gross_rent_by_year
Step 6: Use both the prices_square_foot_by_year DataFrame and interactive plots to answer the following questions:
Question: Did any year experience a drop in the average sale price per square foot compared to the previous year?

**Answer:**yes in 2011 average sales price droped

Question: If so, did the gross rent increase or decrease during that year?

Answer: yes average rent also droped in 2011

Compare the Average Sale Prices by Neighborhood
For this part of the assignment, use interactive visualizations and widgets to explore the average sale price per square foot by neighborhood. To do so, complete the following steps:

Create a new DataFrame that groups the original DataFrame by year and neighborhood. Aggregate the results by the mean of the groups.

Filter out the “housing_units” column to create a DataFrame that includes only the sale_price_sqr_foot and gross_rent averages per year.

Create an interactive line plot with hvPlot that visualizes both sale_price_sqr_foot and gross_rent. Set the x-axis parameter to the year (x="year"). Use the groupby parameter to create an interactive widget for neighborhood.

Style and format the line plot to ensure a professionally styled visualization.

Note that your resulting plot should appear similar to the following image:

A screenshot depicts an example of the resulting plot.

Use the interactive visualization to answer the following question:

For the Anza Vista neighborhood, is the average sale price per square foot for 2016 more or less than the price that’s listed for 2012?
Step 1: Create a new DataFrame that groups the original DataFrame by year and neighborhood. Aggregate the results by the mean of the groups.
# Group by year and neighborhood and then create a new dataframe of the mean values
# Review the DataFrame
Step 2: Filter out the “housing_units” column to create a DataFrame that includes only the sale_price_sqr_foot and gross_rent averages per year.
# Filter out the housing_units
# Review the first and last five rows of the DataFrame
Step 3: Create an interactive line plot with hvPlot that visualizes both sale_price_sqr_foot and gross_rent. Set the x-axis parameter to the year (x="year"). Use the groupby parameter to create an interactive widget for neighborhood.
Step 4: Style and format the line plot to ensure a professionally styled visualization.
# Use hvplot to create an interactive line plot of the average price per square foot
# The plot should have a dropdown selector for the neighborhood
Step 6: Use the interactive visualization to answer the following question:
Question: For the Anza Vista neighborhood, is the average sale price per square foot for 2016 more or less than the price that’s listed for 2012?

Answer: yes it is lower in 2016 than 2012

Build an Interactive Neighborhood Map
For this part of the assignment, explore the geospatial relationships in the data by using interactive visualizations with hvPlot and GeoViews. To build your map, use the sfo_data_df DataFrame (created during the initial import), which includes the neighborhood location data with the average prices. To do all this, complete the following steps:

Read the neighborhood_coordinates.csv file from the Resources folder into the notebook, and create a DataFrame named neighborhood_locations_df. Be sure to set the index_col of the DataFrame as “Neighborhood”.

Using the original sfo_data_df Dataframe, create a DataFrame named all_neighborhood_info_df that groups the data by neighborhood. Aggregate the results by the mean of the group.

Review the two code cells that concatenate the neighborhood_locations_df DataFrame with the all_neighborhood_info_df DataFrame. Note that the first cell uses the Pandas concat function to create a DataFrame named all_neighborhoods_df. The second cell cleans the data and sets the “Neighborhood” column. Be sure to run these cells to create the all_neighborhoods_df DataFrame, which you’ll need to create the geospatial visualization.

Using hvPlot with GeoViews enabled, create a points plot for the all_neighborhoods_df DataFrame. Be sure to do the following:

Set the size parameter to “sale_price_sqr_foot”.

Set the color parameter to “gross_rent”.

Set the size_max parameter to “25”.

Set the zoom parameter to “11”.

Note that your resulting plot should appear similar to the following image:

A screenshot depicts an example of a scatter plot created with hvPlot and GeoViews.

Use the interactive map to answer the following question:

Which neighborhood has the highest gross rent, and which has the highest sale price per square foot?
Step 1: Read the neighborhood_coordinates.csv file from the Resources folder into the notebook, and create a DataFrame named neighborhood_locations_df. Be sure to set the index_col of the DataFrame as “Neighborhood”.
Step 2: Using the original sfo_data_df Dataframe, create a DataFrame named all_neighborhood_info_df that groups the data by neighborhood. Aggregate the results by the mean of the group.
"
# Load neighborhoods coordinates data
# Review the DataFrame
# Calculate the mean values for each neighborhood
# Review the resulting DataFrame
Step 3: Review the two code cells that concatenate the neighborhood_locations_df DataFrame with the all_neighborhood_info_df DataFrame.
Note that the first cell uses the Pandas concat function to create a DataFrame named all_neighborhoods_df.

The second cell cleans the data and sets the “Neighborhood” column.

Be sure to run these cells to create the all_neighborhoods_df DataFrame, which you’ll need to create the geospatial visualization.

# Using the Pandas `concat` function, join the 
# neighborhood_locations_df and the all_neighborhood_info_df DataFrame
# The axis of the concatenation is "columns".
# The concat function will automatially combine columns with
# identical information, while keeping the additional columns.
# Review the resulting DataFrame
# Call the dropna function to remove any neighborhoods that do not have data
# Rename the "index" column as "Neighborhood" for use in the Visualization
# Review the resulting DataFrame
Step 4: Using hvPlot with GeoViews enabled, create a points plot for the all_neighborhoods_df DataFrame. Be sure to do the following:
Set the geo parameter to True.
Set the size parameter to “sale_price_sqr_foot”.
Set the color parameter to “gross_rent”.
Set the frame_width parameter to 700.
Set the frame_height parameter to 500.
Include a descriptive title.
# Create a plot to analyze neighborhood info
Step 5: Use the interactive map to answer the following question:
Question: Which neighborhood has the highest gross rent, and which has the highest sale price per square foot?
Compose Your Data Story
Based on the visualizations that you have created, compose a data story that synthesizes your analysis by answering the following questions:

Question: How does the trend in rental income growth compare to the trend in sales prices? Does this same trend hold true for all the neighborhoods across San Francisco?

Question: What insights can you share with your company about the potential one-click, buy-and-rent strategy that they're pursuing? Do neighborhoods exist that you would suggest for investment, and why?
