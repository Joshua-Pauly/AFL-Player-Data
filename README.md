# AFL Player Data Web Scraping

## Introduction
While there is no possibility of the Buffalo Bills making the Super Bowl, it is time for me to look forward to the start of the season for my second favorite sport, Australian Football.

## Data Identification and Review
This project demonstrates how I scraped data from [AFL.com.au](https://www.afl.com.au) to pull player data from the 2024 season. Since there is no `robots.txt` file restricting access, I retrieved data directly from the AFL's API, which provides structured data to the public.

## Data Description
- **Website:** [AFL Stats - AFL.com.au](https://www.afl.com.au/stats/leaders?category=Scoring&seasonId=62&roundId=-1&roundNumber=0&sortColumn=goals&sortDirection=descending&positions=All&teams=All&benchmarking=false&dataType=totals&playerOneId=null&playerTwoId=null)
- **Objective:** Extract relevant player data from the previous season for further analysis.
- **Use Case:** Conduct data analytics to determine *points above replacement*, a common statistic used to rank player performance compared to the average player.

### Data Catalogue
- **Update Frequency:** Player data is refreshed after each AFL game.
- **Last Update:** The final game of the 2024 AFL season was on September 28, 2024. No new data has been generated since that date.
- **Format:** Data was initially in JSON format but converted into a CSV file.

## Legal and Ethical Considerations
- Since the data was not stored in an HTML table, I used **Postman** to extract the JSON file from the API.
- The API is intended for public use, so there are no legal concerns.

## Data Collection Procedure
1. **Identifying the Data Source:**
   - I wanted to pull stats leaders from the 2024 AFL season, but the table was not directly in an HTML format.
   - By inspecting the website and reviewing the network activity, I found a JSON file with the largest file size, which contained player data.
![image](https://github.com/user-attachments/assets/e69a2d40-43bc-4694-b0b6-5d167364c0e1)



2. **Extracting Data Using Postman:**
   - Right-clicked the JSON request and copied it as a `cURL (Windows)` command.
   - Imported it into Postman, which generated the required headers for Python requests.

![image](https://github.com/user-attachments/assets/b01c9fb7-517e-44a3-944a-40a7e91ca4bc)


3. **Fetching Data with Python:**
   - Copied Postman’s generated code and modified it for efficiency.
   - Imported `json` and created a variable `player_data`.
   - ![image](https://github.com/user-attachments/assets/aadfae86-954c-40f5-96d6-f14fb5f6fe80)
   - Extracted key statistics, displaying the total number of players and details of the first player.
   - ![image](https://github.com/user-attachments/assets/bcf5bc43-0d7f-4bb1-bd9f-675f22c02669)



4. **Processing Data in Pandas:**
   - Converted the JSON response into a DataFrame.
   - Printed the first few rows to validate the data.
   - ![image](https://github.com/user-attachments/assets/e24b002e-a26f-4729-bb6a-be36965bb80a)


5. **Exporting Data:**
   - Saved the cleaned DataFrame as a CSV file.
   - **Result:** 807 players and 149 columns of statistics available for analysis.
   - ![image](https://github.com/user-attachments/assets/caed47e7-d5b9-44de-8dbd-3ca7ddfbc3f7)


## Results
- Successfully scraped and stored AFL player statistics.
- The dataset allows for in-depth player performance analysis, including *points above replacement* calculations.
- ![image](https://github.com/user-attachments/assets/cfc87890-4202-4a3e-9f6a-f336bbd1e739)


## Sources
- **AFL Stats:** [AFL.com.au Stats Leaders](https://www.afl.com.au/stats/leaders?category=Scoring&seasonId=62&roundId=-1&roundNumber=0&sortColumn=goals&sortDirection=descending&positions=All&teams=All&benchmarking=false&dataType=totals&playerOneId=null&playerTwoId=null)
- **YouTube Guide:**
  - Rooney, J. W. (2020). *How to scrape sports stats websites with Python* [Video]. YouTube.  
    [https://www.youtube.com/watch?v=SEQjNEawceo](https://www.youtube.com/watch?v=SEQjNEawceo)

## Credits
- All data collection and processing were based on the techniques demonstrated in the referenced YouTube tutorial.
- This project was inspired by my passion for Australian Football and sports analytics.

---

### *Future Work*
With this dataset, additional insights can be generated, including:
- Player rankings based on performance metrics.
- Predictive analytics for future seasons.
- Advanced visualization of player statistics.

Feel free to use or expand upon this project for further analysis!
