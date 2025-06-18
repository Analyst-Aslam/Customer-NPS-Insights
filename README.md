#  Net Promoter Score (NPS) Analysis in Excel

##  Project Overview

This project analyzes **Net Promoter Score (NPS)** survey data using **Microsoft Excel**. NPS measures customer satisfaction and loyalty by asking how likely a customer is to recommend a service to others.


The project includes data cleaning, NPS classification, and the creation of an **interactive dashboard** with slicers, charts, and a timeline.

---

### What is Net Promoter Score (NPS)?
Net Promoter Score (NPS) is a simple and powerful metric for measuring customer loyalty and satisfaction.
Customers are asked: 


"How likely are you to recommend our product/service to a friend or colleague?"

They respond with a score from 0 to 10, which categorizes them as: Promoters, Passives and Detractors based on the score.

##  Dataset Overview

| Column Name     | Description                                                                 |
|-----------------|-----------------------------------------------------------------------------|
| `ID`            | Unique identifier for each customer                                          |
| `Market`        | Country where the customer is based                                          |
| `Survey date`   | Date when the customer completed the survey                                  |
| `Customer Name` | Name of the customer                                                         |
| `Month`         | Month when the survey was completed (converted to "mmm" format, e.g., Jan)  |
| `Quarter`       | Quarter in which the survey was completed                                    |
| `NPS`           | Score from 0 to 10 on likelihood to recommend the service                    |

---

##  Data Cleaning & Transformation

All steps were done in **Excel**:

1. **Survey Date Fix**  
   - Some `Survey date` entries were in text format.
   - Used **Text to Columns** to separate day, month, year.
   - Combined using:  
     ```excel
     =DATE(year, month, day)
     ```

2. **Month Conversion**  
   - Converted numeric months to `"mmm"` format:  
     ```excel
     =TEXT(DATE(2021, [Month], 1), "mmm")
     ```

3. **NPS Type Classification**  
   - Created a new column to label customers as:
     - **Promoter** (score 9–10)
     - **Passive** (score 7–8)
     - **Detractor** (score 0–6)

   - Formula used:  
     ```excel
     =IF([@NPS]>=9, "Promoter", IF([@NPS]>=7, "Passive", "Detractor"))
     ```

---

##  Dashboard Components

Built an interactive Excel dashboard with:

-  **Pie Chart** showing the distribution of NPS Types (Promoters, Passives, Detractors)
-  **Column Chart** showing NPS Types by Market
-  **Slicers** to filter by:
  - Market
  - Quarter
-  **Timeline** to filter records by `Survey date`

These visuals help explore how customer satisfaction varies across regions and over time.

---

##  About NPS

**Net Promoter Score (NPS)** is calculated as:

```text
NPS = %Promoters − %Detractors
```

---

##  Applications of NPS

NPS is more than just a score — it drives strategic customer decisions. It is used to:

###  1. Track Customer Loyalty  
Monitor how satisfaction changes over time or after product/service updates.

###  2. Identify Pain Points  
Understand reasons behind low scores through detractor feedback.

###  3. Segment Customers  
Prioritize high-value promoters and develop strategies to retain passives.

###  4. Benchmark Performance  
Compare customer loyalty across regions, products, or industry peers.

###  5. Encourage Customer-Centric Culture  
Promote continuous improvement and responsiveness to customer needs.

###  6. Forecast Business Growth  
High NPS often correlates with long-term customer retention and word-of-mouth referrals.

---

## 🙌 Let's Connect!

If you found this project helpful or have feedback, feel free to connect with me on [LinkedIn](https://www.linkedin.com/in/aslamayub/) or check out my other data analytics projects!

Happy Analyzing! 📈

