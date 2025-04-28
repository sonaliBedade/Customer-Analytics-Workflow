# Customer-Analytics-Workflow using DBT and BigQuery

This project showcases an end-to-end customer data transformation and analytics workflow using **dbt (Data Build Tool)** and **Google BigQuery**.  
It focuses on structuring raw customer data into clean, trusted datasets ready for analysis — and extracting valuable business insights like customer loyalty, churn behavior, and overall activity trends.

---

## Project Overview

In real-world business environments, raw customer data is often messy, inconsistent, and hard to use directly for decision-making.  
This project simulates a modern data workflow where raw data is:

- Transformed and modeled into clean structures
- Tested for quality
- Documented for transparency
- Analyzed to generate meaningful insights

By following best practices in data engineering and analytics, this project builds a robust foundation for trustworthy business intelligence.

---

## Tools & Technologies

- dbt (Data Build Tool): For data transformation, testing, and documentation.
- Google BigQuery: As the cloud data warehouse to store and query the data.
- SQL: For all transformation logic and insights extraction.

---

## Key Steps

1. Data Transformation:
   - Built dbt models to clean and organize raw customer data.
   - Structured fields like customer IDs, names, first/most recent orders, and number of orders.

2. Data Testing:
   - Implemented dbt tests to ensure data integrity (e.g., primary key uniqueness, no nulls in critical fields).

3. Data Documentation:
   - Generated dbt documentation to provide model descriptions, column details, and lineage graphs.

4. Data Analysis:
   - Queried BigQuery to extract insights such as:
     - Top 10 loyal customers
     - Average number of orders per customer
     - Churned customers (inactive > 80 days)
     - New vs Returning customer breakdown
     - Customer active lifespan analysis

5. Visualization:
   - Created basic charts directly in BigQuery to visualize key metrics like loyalty distribution and churn rates.

---

## Business Impact

By implementing this workflow:
- Data becomes structured, consistent, and reliable for analysis.
- Businesses can quickly identify high-value customers and churn risks.
- Data quality is monitored automatically using dbt testing.
- Teams gain clear documentation and data lineage visibility, reducing onboarding time for new members.

---

## Analysis:

Query 1 - finding top 10 loyal customers

![Loyals](https://github.com/user-attachments/assets/886921ba-a05b-4c73-84f3-8c8129196cc7)

![image](https://github.com/user-attachments/assets/33af9051-c046-4743-8bff-7b0f719228aa)

Query 2 - average number of orders per customer

![image](https://github.com/user-attachments/assets/5cdc46ba-5062-44b4-8dd3-90efa5b59a86)

Query 3 - churn analysis (customers inactive for 2+ months)

![image](https://github.com/user-attachments/assets/3367a903-945b-467a-811b-29fbebe44e06)

Query 4 - new vs returning customer

![returning_vs_new](https://github.com/user-attachments/assets/0a05c619-7832-4248-8139-8057861da0f9)

![image](https://github.com/user-attachments/assets/7d756504-3b1c-46a8-ae0b-1870dfb4aeda)

Query 5 - customer activity time span

![image](https://github.com/user-attachments/assets/8ea09d70-bfd8-4da4-a267-7770b21c5a79)

## Insights:

- Most customers place only a single order.
This indicates low customer retention across the user base.
Business Focus: Introduce loyalty programs, reactivation offers, and retention campaigns to encourage repeat orders.

- A small group of loyal customers contributes to repeat business.
Top customers placed 8 to 10 orders each. These high-value users represent an opportunity for VIP loyalty programs, exclusive offers, and personalized marketing.
Business Focus: Nurture loyal customers and increase their lifetime value.

- Customer churn is a potential risk.
Several customers have been inactive for over 80 days.
Early signs of churn highlight the need for customer re-engagement strategies.
Business Focus: Send reactivation campaigns targeting churned customers to win them back.

- Returning customer rate is strong, but new customer acquisition is lower.
67% of customers are returning; only 33% are new. This suggests the business is retaining customers well, but may need to increase new customer acquisition efforts.
Business Focus: Enhance marketing campaigns to attract new customers, while maintaining strong loyalty efforts for existing users.

- Most customers have short activity spans.
The longest customer activity period recorded is only 76 days (~2.5 months).
This indicates that customers typically stop engaging within 2-3 months of their first order.
Business Focus: Launch re-engagement campaigns around the 60-day mark to prevent churn.

## Conclusion

This project demonstrates the power of combining dbt, BigQuery, and SQL for building scalable, tested, and insightful data workflows.  
It highlights how structured data pipelines can translate directly into business value by enabling faster, more confident decision-making.





