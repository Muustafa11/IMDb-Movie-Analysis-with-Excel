![image alt](https://github.com/Muustafa11/IMDb-Movie-Analysis-with-Excel/blob/main/c8373447-3cfd-4181-aef6-31e26f9a3414-731323186.jpg)




# IMDb-Movie-Analysis-with-Excel
In this project, I aim to derive insights from movie data, aiding cinema industry professionals in identifying the best countries, languages, actors, directors, and actor-director duos. Additionally, I will analyze if IMDb scores correlate with gross income, offering a comprehensive view of factors driving movie success.

## Dataset description

This dataset contains 3523 rows , 14 original rows and I add 8 new rows to help in the insigt extraction
#Original Columns :
1-director_name: The name of the director of the movie.
2-num_critic_for_reviews: The number of reviews the movie has received from critics.
3-gross: The total gross revenue the movie generated.
4-genres: The genres the movie belongs to (e.g., Drama, Comedy).
5-actor_1_name: The name of the lead actor/actress in the movie.
6-movie_title: The title of the movie.
7-num_voted_users: The number of users who have voted/rated the movie.
8-plot_keywords: Keywords describing the main plot points of the movie.
9-num_user_for_reviews: The number of reviews the movie has received from users.
10-language: The primary language in which the movie was released.
11-country: The country where the movie was produced.
12-budget: The production budget of the movie.
13-title_year: The year the movie was released.
14-imdb_score: The IMDb rating score for the movie.
#Added Columns: will be described next

## Data Preprocessing Steps 
### Overview:
The following steps outline the data preprocessing procedures undertaken to prepare the IMDb dataset for analysis. This includes data cleaning, the addition of new columns, and the transformation of existing data to ensure consistency and comparability.

#### Data Cleaning Steps:
Remove Special Characters:
Removed special characters from the following columns: director_name, actor_1_name, and movie_title.
Highlight and Fill Null Values in Plot Keywords:
Used conditional formatting to highlight null values in the plot_keywords column.
Filled the blanks using ChatGPT to generate appropriate keywords based on movie context.
Fill Blanks in Language Column:
Filled blanks in the language column based on the country column. For example, if the movie is from the USA, the language was filled as English.
Verified and corrected the filled entries using ChatGPT for accuracy.

### Added Columns and Their Transformations:
Main Genre: Extracted from the genres column by taking the first genre listed.
Actor & Director Duo: Concatenated actor_1_name and director_name.
Conversion: Applied a lookup function to reference a table of exchange rates based on the country.
Adjusted Gross: Calculated by multiplying the gross by the Conversion rate.
Adjusted Budget: Calculated by multiplying the budget by the Conversion rate.
Profit: Subtracted the Adjusted Budget from the Adjusted Gross.
ROI (Return on Investment): Calculated using the formula: (Profit / Adjusted Budget) * 100.
Score Group: Created groups based on the imdb_score using conditional statements.

## Data Visualization and Analysis

### Visualizations:
Rating vs Average of Gross:
Description: This pie chart illustrates the distribution of average gross income across different IMDb ratings. It helps to understand how the gross income varies with the rating categories.
![image alt](https://github.com/Muustafa11/IMDb-Movie-Analysis-with-Excel/blob/main/Screenshot%202024-07-25%20192627.png)

Top 15 Countries Budget Analysis:
Description: This bar chart shows the budget distribution for the top 15 countries. It helps to compare how different countries allocate their movie budgets.
![image alt](https://github.com/Muustafa11/IMDb-Movie-Analysis-with-Excel/blob/main/Screenshot%202024-07-25%20192216.png)

Annual Gross Income Analysis:
Description: This line graph illustrates the trend of annual gross income over time, providing insights into how movie revenue has changed year by year.
![image alt](https://github.com/Muustafa11/IMDb-Movie-Analysis-with-Excel/blob/main/Screenshot%202024-07-25%20184359.png)

### Pivot tables

Top 10 Actors with Highest ROI:
Description: Shows the top 10 actors ranked by their return on investment (ROI), highlighting those who generate the highest returns relative to their investments.

![image alt](https://github.com/Muustafa11/IMDb-Movie-Analysis-with-Excel/blob/main/Top%2010%20Actors%20with%20Highest%20ROI.png)

Top 10 Directors with Highest ROI:
Description: Lists the top 10 directors based on their ROI, identifying directors who achieve the highest financial returns.

![image alt](https://github.com/Muustafa11/IMDb-Movie-Analysis-with-Excel/blob/main/Top%2010%20Directors%20with%20Highest%20ROI.png)


Top 10 Actor & Director Duo with Highest ROI:
Description: Displays the top 10 actor-director duos ranked by their ROI, showcasing the most profitable collaborations.

![image alt](https://github.com/Muustafa11/IMDb-Movie-Analysis-with-Excel/blob/main/Top%2010%20Actor%20%26%20Director%20Duo%20with%20Highest%20ROI.png)


Top 10 Movies with Highest Profit:
Description: This pivot table showcases the top 10 movies ranked by their total profit. It highlights the most financially successful films, offering valuable insights for those looking to replicate these achievements in the film industry.

![image alt](https://github.com/Muustafa11/IMDb-Movie-Analysis-with-Excel/blob/main/Top%2010%20Movies%20with%20Highest%20Profit%20.png)


Top 10 Countries Based on the ROI and Their Profit Average:
Description: This pivot table ranks the top 10 countries by their return on investment (ROI) and provides the average profit for each country. It offers insights into which countries achieve the highest profitability relative to their investments.

![image alt](https://github.com/Muustafa11/IMDb-Movie-Analysis-with-Excel/blob/main/Top%2010%20Countries%20with%20Highest%20ROI.png)

# Conclusion
In this project, we successfully preprocessed and analyzed the IMDb dataset to gain meaningful insights for the cinema industry. The visualizations and pivot tables created offer a comprehensive overview of the factors contributing to movie profitability, including top-performing countries, languages, actors, directors, and actor-director duos. By understanding these trends, industry professionals can make more informed decisions and strategies for future projects. Additionally, the correlation analysis between IMDb scores and gross income provides valuable information on the impact of movie ratings on financial success.
