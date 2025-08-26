# 📊 Bank of America: Key Analytical Insights

<img width="275" height="183" alt="image" src="https://github.com/user-attachments/assets/036203a0-58e1-449c-a203-e7c068713674" />



## 📌 Introduction  

In today’s digital economy, financial institutions generate vast amounts of transactional data daily. For a bank like **Bank of America**, understanding this data is critical to improving operational efficiency, strengthening customer relationships, and staying competitive in a rapidly evolving financial landscape.  

This project leverages transactional records to provide a **comprehensive analysis of customers, agents, and merchants**. The dataset contains details on transaction value, channels used, commissions, customer demographics, and merchant activity — enabling a holistic view of how the bank’s ecosystem operates.  

The primary motivation behind this analysis was to answer key business questions, such as:  
- Who are the top-performing agents, merchants, and customers?  
- What channels do customers and merchants prefer for transactions?  
- How do transaction values and volumes trend over time?  
- Which customer segments contribute the most to overall performance?  
- How can commissions, agent performance, and merchant activities be optimized?  

By building an **interactive Power BI dashboard**, this project transforms raw data into actionable insights. The dashboard not only highlights high-value customers and merchants but also uncovers hidden trends in agent performance, seasonal transaction patterns, and customer behavior.  

Ultimately, this work provides decision-makers with the tools to:  
- Identify and reward top performers.  
- Optimize transaction channels and commission strategies.  
- Strengthen customer engagement and retention.  
- Develop data-driven strategies for growth and profitability.  

This introduction sets the stage for exploring the detailed **visualizations, insights, and recommendations** presented in the following sections.  
  

## 🗂 Dataset  
The dataset contains transaction records with attributes such as:  
- **Transaction Details** (value, volume, type, channel, location)  
- **Customer Information** (age category, location)  
- **Agent Information** (commission, performance, activity)  
- **Merchant Information** (location, transaction activity, channels used)  
- **Calendar** (date hierarchy for time-based analysis)  

The **Transactions table** serves as the fact table, linked to dimension tables for customers, agents, merchants, and calendar.  

## 🎯 Objectives  
1. Analyze customer behavior and engagement across years.  
2. Track agent activity, commissions, and performance.  
3. Measure merchant activity and identify top contributors.  
4. Discover seasonal and channel-based transaction patterns.  
5. Provide executives with a clear, actionable visualization dashboard.


  ## 🏗 Data Modelling  

  <img width="1234" height="533" alt="image" src="https://github.com/user-attachments/assets/8ec75631-a532-45f7-ad3b-c8b370566fc4" />


To ensure efficient analysis and reporting, a **relational star-schema model** was designed in Power BI. This model connects **transactions**, **customers**, **agents**, **merchants**, and a **calendar table**, creating a unified structure for business intelligence.  

### 📊 Model Overview  

The schema consists of:  

1. **Fact Table**  
   - **Transactions** (`opay_transactions_medium`)  
     - Holds all transaction records including amount, channel, customer, agent, merchant, and transaction status.  
     - Measures such as **Total Amount**, **Transaction Count**, and **Failure Rate** are derived here.  

2. **Dimension Tables**  
   - **Customers** (`opay_customers_medium`)  
     - Attributes: Customer ID, Name, Location, Age, Age Category, Customer Type, Registration details.  
     - Enables segmentation of transaction activity by demographics.  

   - **Agents** (`opay_agents_medium`)  
     - Attributes: Agent ID, Name, Location, Join Date, Commission Rate, Status.  
     - Supports analysis of agent performance and commission trends.  

   - **Merchants** (`opay_merchants_medium`)  
     - Attributes: Merchant ID, Name, Category, Location.  
     - Provides insights into merchant performance and activity.  

   - **Calendar** (`Calendar`)  
     - Attributes: Date, Month, Quarter, Year.  
     - Serves as the time intelligence backbone for trend analysis.  

### 🔗 Relationships  

- **Transactions ↔ Customers**: Linked by `customer_id`.  
- **Transactions ↔ Agents**: Linked by `agent_id`.  
- **Transactions ↔ Merchants**: Linked by `merchant_id`.  
- **Transactions ↔ Calendar**: Linked by `Transaction Date`.  
- **Agents ↔ Calendar**: Linked via `join_date` for tenure and performance analysis.  

This structure follows a **star schema**, placing the **Transactions table** at the center as the fact table, with Customers, Agents, Merchants, and Calendar serving as dimensions.  

### ✅ Benefits of This Model  

- Ensures **scalability** and efficient queries.  
- Enables **time-series analysis** using the Calendar table.  
- Allows for **segmentation** by customer, agent, and merchant.  
- Provides a strong foundation for **KPI measurement** and **dashboard visualization** in Power BI.  
  

## 📊 Visualizations  

<img width="941" height="533" alt="image" src="https://github.com/user-attachments/assets/e2c57cf5-444a-436e-9677-0ab0ff322b1e" />

<img width="935" height="530" alt="image" src="https://github.com/user-attachments/assets/24def598-fc25-4602-b694-c604cc059fcb" />

<img width="933" height="524" alt="image" src="https://github.com/user-attachments/assets/79490c92-aec7-44d3-9ee4-8df0e7d98828" />

<img width="941" height="532" alt="image" src="https://github.com/user-attachments/assets/447eacb4-78b9-469b-8cde-d9ba3b7d4e57" />





Here are the visuals created across the dashboard:  

1. **Merchant Transactions by Location**  
2. **Transaction Value by Month Number**  
3. **Transaction Value by Channel**  
4. **Top 5 Transaction Values by Agents**  
5. **KPI Cards** → Total Commission Amount, Average Transaction Volume, Transaction Volume ($), Customers per Agent, Transactions of the Top 14 Agents  
6. **Commission Gauge** → Actual Commission Earned vs Target  
7. **Transactions by Top 5 Agents via Channels**  
8. **Agent Commission Value by Date**  
9. **Transaction Value by Customer Location**  
10. **Top 14 Customers and Their Transaction Value**  
11. **Transactions by Age Category and Type**  
12. **Transaction Value by Merchant Location**  
13. **Top 27 Merchants and Their Transactions**  
14. **Top 3 Highest Transaction Value Merchants**  
15. **Top 5 Merchant Transactions by Channel**  

## 🔍 Key Insights from the Dataset  

The Bank of America transaction dataset provided valuable insights into customer behavior, agent performance, merchant activities, and transaction channels. Below are the major findings from the analysis and visualizations:  

1. **Merchant Transactions by Location**  
   - Certain regions host the **highest concentration of merchants**, leading to higher transaction volumes.  
   - Merchant activity is uneven, with some locations driving significantly more value.  

2. **Transaction Trends Over Time**  
   - Transactions **increase progressively across months**, with noticeable peaks in specific months.  
   - This suggests **seasonality in customer spending behavior**.  

3. **Preferred Transaction Channels**  
   - The **mobile channel dominates** in terms of transaction value, followed by POS and web channels.  
   - Customers show a clear preference for **convenience-driven digital channels**.  

4. **Top 5 Agents by Transaction Value**  
   - A small group of **top-performing agents** contributes a disproportionately high share of transactions.  
   - These agents are critical to sustaining transaction volume.  

5. **Commission and Agent Performance**  
   - High-performing agents also receive the **largest commission payouts**, highlighting strong alignment between performance and incentives.  
   - Average transaction volume and customer-to-agent ratios reveal efficiency gaps among agents.  

6. **Transactions by Age Category**  
   - **Younger and middle-aged customers** account for the largest share of transactions.  
   - Elderly customers contribute minimally, suggesting opportunities for **financial inclusion strategies**.  

7. **Customer Concentration**  
   - The **top 14 customers** account for a significant share of total transaction value, showing **high-value customer dependency**.  
   - Targeted engagement with these customers can further strengthen revenue.  

8. **Merchant Performance**  
   - A few merchants consistently rank at the top, with the **top 27 merchants** responsible for a major share of total transactions.  
   - The **top 3 merchants alone** contribute heavily to overall transaction value.  

9. **Channel Utilization by Agents**  
   - Top agents leverage **multiple channels** to process transactions, showing adaptability and stronger customer engagement.  

10. **Geographic Insights**  
   - Both **merchant location** and **customer location** strongly influence transaction activity.  
   - Some locations show high customer demand but lower merchant presence, suggesting **opportunities for expansion**.  

---

### 🧾 Summary  
The dataset highlights that **transactions are heavily concentrated among top-performing agents, merchants, and customers**, while digital channels are the **most preferred medium**. Growth opportunities lie in expanding merchant coverage in underserved regions, diversifying channel offerings, and improving engagement with underrepresented customer groups.  
 

## ✅ Conclusion  
The Bank of America dashboard provides a **comprehensive view of customers, agents, and merchants**.  
With its insights, stakeholders can:  
- Identify top customers and merchants.  
- Reward high-performing agents.  
- Plan for seasonal transaction spikes.  
- Optimize transaction channels to improve efficiency.  

## 💡 Recommendations  
Based on the analysis, the following actions are recommended:  

1. **Customer Engagement**  
   - Launch loyalty programs for consistent customers to increase retention.  
   - Focus marketing campaigns on the small percentage of inactive customers to reactivate them.  

2. **Agent Performance**  
   - Provide incentives for top-performing agents to sustain motivation.  
   - Offer training programs to underperforming agents to balance productivity.  

3. **Merchant Optimization**  
   - Strengthen partnerships with high-performing merchants driving most of the transaction value.  
   - Encourage merchants to adopt underutilized channels for broader reach.  

4. **Strategic Planning**  
   - Use monthly transaction insights for seasonal planning and resource allocation.  
   - Align commission structures with transaction performance for greater efficiency.  

5. **Future Improvements**  
   - Integrate predictive analytics to forecast transaction volumes and customer behavior.  
   - Develop a churn detection model to retain at-risk customers.  
   - Segment merchants and customers for more personalized strategies.  

---


![image](https://github.com/user-attachments/assets/56f6722a-2ca2-4415-b79a-b8fdd6f99635)


For any collaborative work or gigs, reach out to me at:

📧 Email: Bosschuks97@gmail.com  📞: 07064106675
