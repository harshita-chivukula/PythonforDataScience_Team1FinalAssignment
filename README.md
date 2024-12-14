# Python for Data Science Team 1: Analyzing the Fast Food Market 
# (Enric B, Harshita, Henning, Iman, Pien)

## **Brief Description of the Project**  
The *PDS Final Project - Analyzing the Fast Food Market* explores the stock market performance of 10 leading fast-food companies through a comprehensive data-driven approach. The project focuses on comparative financial analysis, identifying industry trends, and analyzing performance drivers such as volatility, trading volume, and price spreads. By leveraging financial metrics like closing prices, trading volumes, and average spreads, the project benchmarks companies, identifies seasonal trends, and uncovers factors influencing market behavior.  

### **Key Deliverables**  
1. **Data Analysis**: In-depth exploration of stock performance, trends, and volatility across 10 fast-food companies.  
2. **Visualizations**: Informative plots showcasing monthly averages, yearly trends, price-volume relationships, and other key metrics.  
3. **Presentation**: A final presentation summarizing findings and insights into stock market trends and company performance.  

## Team Collaboration  

This project was a collaborative effort by **Team 1**, consisting of Enric B., Harshita, Henning, Iman, and Pien. We all collaborated on the code for every exercise and focused on gaining a deep understanding of the code and insights for two exercises each. The exercises each team member was responsible for are reflected in their respective branches, labeled under their names in the repository.  

---
## **Exercises Description**

### **Preprocessing**  
Before starting the analysis, we conducted preprocessing to inspect and clean the datasets. This step involved verifying column types, handling missing values, and ensuring consistency in date formats and structures across all datasets.

---

### **Exercise 1: Dataset Overview**  
**What is the exercise asking us to do?**  
The exercise asks us to analyze the datasets for the 10 companies to determine the number of rows and columns in each dataset and display the column names and their data types.  

**How did we do it?**  
Using a loop, we calculated the number of rows and columns for each dataset and listed the column names with their data types. We also determined each company’s earliest trading date by finding the minimum value in the Date column, sorted the companies by these dates, and displayed the results.  

**What insight did we gain?**  
The datasets were consistent in structure and data types, but their sizes varied, reflecting differences in the companies’ trading histories. Older companies like McDonald’s and Berkshire Hathaway had earlier market entry dates, while newer entrants such as DNUT and LKNCY had shorter records, indicating their more recent IPOs. These observations highlight the diverse market history of the companies.  

---

### **Exercise 2: 2023 Close Price Trends**  
**What is the exercise asking us to do?**  
The exercise requires us to perform a trend analysis of the close prices for the year 2023 and determine how many rows (entries) exist for each company and in total for that year.  

**How did we do it?**  
First, we used a loop to calculate the number of rows per company and the total number of rows for 2023. Then, we analyzed the close price trends for each company by plotting their data over the year. To address the large price disparity between BRK-A and other companies, we used two separate subplots: one for BRK-A and another for the remaining companies. This separation ensured better visibility and interpretability of trends.  

**What insight did we gain?**  
All companies participated in the stock market during 2023, with 250 trading days recorded for that year. BRK-A displayed a significantly higher price range, with its peak close price reaching approximately $560,000, while the next highest price among the other companies was around $440. The market exhibited general stability, but two companies—Domino’s Pizza (DPZ) and BRK-A—showed significant price increases over the year.  

---

### **Exercise 3: Peak Closing Prices**  
**What is the exercise asking us to do?**  
This exercise aims to identify the day with the highest closing price for each company and display the price alongside the corresponding date. The goal is to analyze the peak performance periods of each company and gain insights into their historical stock trends.  

**How did we do it?**  
We used a loop to iterate through the datasets of each company. For each dataset, we calculated the maximum closing price using the max() function and determined the index of this maximum value using the idxmax() function. We then retrieved the date corresponding to the peak price and formatted it for clear presentation. Finally, the peak price and its associated date were printed for each company to summarize their respective highest-performing days.  

**What insight did we gain?**  
Most companies, such as McDonald’s and Domino’s, achieved their highest prices in 2024, reflecting a strong recovery and increased investor confidence in the post-pandemic era. BRK-A stood out with a record-breaking peak price of $641,435, underscoring its dominance as a high-value stock. Wendy’s, on the other hand, reached its peak price of $30.50 in 1993, making it an outlier as this value has not been surpassed in decades. This peak was tied to a remarkable 68% stock return that year, showcasing a brief period of exceptional performance. The disparity in peak prices highlights the varied growth stages of the companies, with Starbucks, Luckin, and Krispy Kreme remaining below $150. Global events, particularly the COVID-19 pandemic, played a significant role in driving peak performances for many companies in recent years.

---

### **Exercise 4: Monthly Averages**  
**What is the exercise asking us to do?**  
The exercise requires us to group the data for the closing prices (Close) of each company by month across all years. Following this, we need to calculate the average closing price for each month and each company. To gather meaningful insights, we must select three companies, plot their monthly averages on a chart, and compare their performance. Finally, we are required to justify the choice of chart used for this comparison.  

**How did we do it?**  
To complete the task, we created a dictionary to store the monthly averages. We iterated through the datasets for all 10 companies using a loop. For each dataset, we grouped the data by month using the Date column and calculated the average closing price for each month with the groupby function. We then converted the numeric month indices into their corresponding month names (e.g., “January,” “February”) to improve readability. The monthly averages for each company were stored in a dictionary for organized access. Next, we selected three companies that provide different types of foods—pizza, fries/burgers, and coffee—and plotted their monthly averages on a line chart.  

**What insight did we gain?**  
LKNCY experienced a decline in stock prices from March to May, followed by a recovery toward the end and beginning of the year. The dip in May is likely attributed to reduced demand during post-spring break and exam periods, while peaks were driven by increased demand for coffee in the winter months. MCD and QSR demonstrated consistent trends throughout the year, with notable peaks in August and dips in March and October. The August peak was likely driven by higher consumer demand during vacations and the tourism season. McDonald’s, in particular, consistently maintained higher stock prices, reflecting its long history and strong market dominance compared to QSR.

---
### **Exercise 5: Yearly Averages**  
**What is the exercise asking us to do?**  
We are asked to compute the yearly average of the Close price and plot a comparison for all companies on a chart. Additionally, we are required to justify the choice of visualization.  

**How did we do it?**  
We looped through each company and its dataset. For each company, we grouped the data by year and computed the average close price. These averages were stored in a dictionary for each company. Finally, we plotted a line chart with multiple lines, one for each company, ensuring comparability and clear insights.  

**What insight did we gain?**  
The entire market is growing, with notable faster growth for BRK-A, DPZ, and MCD. A dip in average close prices was observed around 2008, likely due to the global financial crisis. LKNCY exhibited fluctuations and unstable pricing, but the overall market has been resilient and stable over time.  

---

### **Exercise 6: Price Ranges**  
**What is the exercise asking us to do?**  
The exercise requires us to create a plot showing the range of prices for each month, and we must justify the choice of visualization.  

**How did we do it?**  
We grouped the data for each company by month and extracted the Close price. Using these values, we created a boxplot for each company, visualizing the monthly price ranges. Each company's data was displayed in a subplot for better clarity and comparison.  

**What insight did we gain?**  
DNUT and QSR exhibited stable price ranges, indicating less fluctuation in their stock performance. In contrast, BRK-A showed numerous outliers above the box, reflecting inconsistent price spikes. Both QSR and LKNCY displayed outliers below the box, which can be attributed to rapid growth and market instability. Overall, the market demonstrated consistent medians, underscoring stability in valuation across the companies.

---

### **Exercise 7: Volume vs. Price**  
**What is the exercise asking us to do?**  
The exercise requires us to analyze the relationship between trading volume and closing price for a selected company by creating a plot. Additionally, we must derive insights from the observed patterns and justify the chosen chart type.  

**How did we do it?**  
We selected McDonald’s (MCD) due to its historical significance and stable market presence. Using its dataset, we plotted a scatter plot to visualize the relationship between trading volume and close price. The chart was styled with transparency for overlapping points and axis labels for clarity.  

**What insight did we gain?**  
Most trading days exhibited low trading volumes, with closing prices primarily concentrated between $50 and $250. There was no strong direct correlation observed between trading volume and closing price, reflecting McDonald’s stable stock performance. Outliers with unusually high trading volumes were likely associated with significant events, such as financial reports or major announcements.

---

### **Exercise 8: Peak Trading Volumes**  
**What is the exercise asking us to do?**  
This exercise involves identifying the month with the highest total trading volume for each company and presenting these results in a structured summary table.  

**How did we do it?**  
We grouped the data by month and calculated the total trading volume for each company. For each company, we identified the month with the highest trading volume and stored the results in a summary table for clear presentation.  

**What insight did we gain?**  
Companies such as Starbucks (SBUX) and Luckin Coffee (LKNCY) demonstrated exceptionally high trading volumes during periods of growth, highlighting heightened investor interest. In contrast, BRK-A, despite its massive share price, recorded the lowest peak trading volume, reflecting its characteristic high-value, low-trade stock behavior. The year 2020 witnessed peak trading volumes for several companies, likely influenced by the COVID-19 pandemic’s impact on market volatility and an increase in speculative trading.

---

### **Exercise 9: Merging Yearly Data**  
**What is the exercise asking us to do?**  
The task is to create a dataset for each year and then merge them into a single dataset to analyze trading trends over time.  

**How did we do it?**  
We combined the individual datasets for all companies into a single merged dataset. Additional columns, `Company` and `Year`, were added to indicate the source dataset and year, respectively. The merged dataset was then split by year into separate datasets for further analysis.  

**What insight did we gain?**  
The increase in the number of rows over the years reflected the market's expansion and the entry of new companies. The merged dataset facilitated a more comprehensive analysis of overall market trends.  

---

### **Exercise 10: Price Spread Analysis**  
**What is the exercise asking us to do?**  
The exercise requires us to calculate the daily price spread (difference between the high and low prices) for each company, compute their average spread, and visualize these results. Additionally, we need to justify the chosen visualization type and interpret the companies’ behavior based on their price spreads.  

**How did we do it?**  
We added a new column, `Spread`, to each dataset, calculated as the difference between the high and low prices for each trading day. Using this column, we computed the mean spread for each company and visualized the results using a strip plot. A logarithmic scale was applied to the y-axis to handle the wide range of spreads, particularly for BRK-A.  

**What insight did we gain?**  
BRK-A demonstrated the highest average spread, driven by its exceptionally high stock price, where even small percentage changes translated into significant absolute differences. McDonald’s exhibited moderate spread variability with lower averages, reflecting its market maturity and stability. In contrast, newer companies like LKNCY showed higher spreads, influenced by market speculation and instability. The strip plot effectively captured the variability in spreads, providing insights into both central tendencies and outliers for each company.  

---

## How to Install and Run  

To set up the environment and install the required dependencies, follow these steps:  

1. **Clone the Repository**  
   Clone the repository to your local machine using the following command:  
   git clone https://github.com/harshita-chivukula/PythonforDataScience_Team1FinalAssignment.git
2. **cd your-repo-folder (Create the Repo)**
3. **Create your own environment, you can use: python -m venv myenv (Create an env)**
   Source myenv/bin/activate (Activate the env)
4. Install the requirements.txt using:
   pip install -r requirements.txt (Install the requirements)

   

  

