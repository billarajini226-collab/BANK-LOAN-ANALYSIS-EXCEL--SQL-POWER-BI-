# END-TO-END LOAN DEFAULT ANALYSIS AND RISK SEGMENTATION 

This project performs a comprehensive analysis of a bank's loan portfolio using a multi-tool analytics pipeline. It answers critical business questions around:

- *Who is borrowing?* (income, geography, loan purpose)
- *How are loans performing?* (fully paid vs. charged off vs. current)
- *Where is the risk?* (default rate, DTI, high-risk segments)
- *How is the bank trending?* (year-over-year growth, interest rate shifts)

The result is a fully interactive Power BI dashboard that enables data-driven lending decisions.

---

## 🛠 Tech Stack

| Tool | Purpose |
|---|---|
| *Microsoft Excel* | Data cleaning, pivot analysis, initial exploration |
| *SQL Server (SSMS)* | Data querying, KPI extraction, aggregation |
| *Power BI* | Interactive dashboard, visual storytelling |

---

## 📊 Key Metrics Tracked

| # | Metric | Description |
|---|---|---|
| 1 | Total Loan Applications | Count of all loan requests received |
| 2 | Total Loan Amount Issued | Total disbursed principal across all loans |
| 3 | Total Amount Received | Cumulative repayments collected from borrowers |
| 4 | Loan Status Distribution | Breakdown: Fully Paid / Current / Charged Off |
| 5 | Default Rate (%) | Charged-off loans as a % of total issued |
| 6 | Average Interest Rate | Mean interest rate across the portfolio |
| 7 | Average Annual Income | Borrower income used to assess creditworthiness |
| 8 | Debt-to-Income (DTI) Ratio | Borrower repayment capacity indicator |
| 9 | Loan Distribution by Term | 36-month vs. 60-month performance split |
| 10 | Loan Distribution by State | Geographic risk and volume heatmap |
| 11 | Year-wise Loan Growth | Disbursement volume trends over time |
| 12 | Risk Segmentation | Low / Medium / High risk classification |

---

## 🎯 Business Objectives

1. Evaluate overall loan portfolio health and distribution.
2. Identify the volume and trend of charged-off (defaulted) loans.
3. Segment customers by risk level using income, loan amount, and DTI.
4. Analyze loan disbursement trends year over year.
5. Understand geographic and product-level performance.
6. Measure year-over-year bank performance improvement.
7. Deliver actionable insights via SQL and Power BI for decision-makers.

---

## 💡 Key Insights

### 🔹 Loan Term Preference
- *59.16%* of loans are 36-month (short-term); only 40.84% are 60-month.
- *Insight:* Borrowers strongly prefer shorter commitments, indicating lower risk appetite and cautious borrowing behavior.

### 🔹 Loan Purpose — Debt Consolidation Dominates
- Debt consolidation accounts for *40.68%* of all loan purposes.
- Combined with credit card refinancing, *62.71%* of borrowers are managing existing liabilities.
- *Insight:* The bank's primary customer base consists of debt-restructuring borrowers, not new capital seekers.
In 60 months there is 40.84% and in 36 months 59.16%.
So majority customers prefer shorter term loans.

### 🔹 Loan Status & Portfolio Stability
- Current payables carry the highest outstanding loan amounts, while fully paid loans remain relatively low in count.
- *Insight:* The portfolio is active and growing, but repayment velocity needs monitoring.

### 🔹 Charged-Off Trend
- Charged-off cases spiked by *+123.31%* at peak, then declined by *84.41%* — a net reduction of *38.1%*.
- The effective impact on portfolio health is a *18.19%* improvement in default control.

### 🔹 High-Risk Segment
- *35,200 loans* are classified as high-risk, with loan amounts ranging *$30K–$60K*, spread across multiple states.
- *Insight:* High-risk accounts are geographically distributed, requiring state-level risk policies.

### 🔹 Payment Completion
- Only *50% of the total payment obligation* (270.3K of 540.6K) has been fulfilled.
- *Insight:* A significant repayment backlog exists — collections strategy review is recommended.

### 🔹 Default Rate by Year
- Default rate peaked in *2015* at *18.9%* (funded amount: $63.9M), then declined steadily through 2018 before recovering to $85.2M in disbursement with a stable default ratio.
- *Insight:* Portfolio quality improved significantly post-2015 despite higher volumes.

### 🔹 Term vs. Default Rate
- The *60-month term* carries a disproportionately higher default rate than 36-month loans.
- *Insight:* Longer loan durations correlate with increased borrower default risk.

### 🔹 Interest Rate Trend
- Interest rates peaked in *2015*, then gradually declined and stabilized — indicating improved risk-adjusted pricing over time.

  # 🗄 SQL Queries Preview

The following SQL analyses were performed in *Microsoft SQL Server Management Studio (SSMS)*:

- Total loan applications and disbursement by year
- Default rate calculation (charged-off / total)
- Average interest rate by loan term and status
- High-risk loan segmentation by income band and geography
- Month-over-month and year-over-year growth queries
- DTI ratio aggregation by loan purpose
- Payment plan completion analysis

 📸 See SQL screenshots below (scroll down to the Screenshots section)


<img width="968" height="555" alt="SQLQuery2 sql - BILLA RAJINI bank_data (DESKTOP-B9RQCTF_LENOVO (58)) - SQLQuery2 sql - BILLA RAJINI bank_data (DESKTOP-B9RQCTF_LENOVO (58)) - Microsoft SQL Server Management Studio 26-02-2026 23_31_22" src="https://github.com/user-attachments/assets/8367f842-4daa-4cc2-9b66-fe6922c020b1" />
<img width="928" height="535" alt="SQLQuery2 sql - BILLA RAJINI bank_data (DESKTOP-B9RQCTF_LENOVO (58)) - SQLQuery2 sql - BILLA RAJINI bank_data (DESKTOP-B9RQCTF_LENOVO (58)) - Microsoft SQL Server Management Studio 26-02-2026 23_31_50" src="https://github.com/user-attachments/assets/6190b22a-636f-421a-a7c9-94ceff0ca93e" />
<img width="952" height="538" alt="SQLQuery2 sql - BILLA RAJINI bank_data (DESKTOP-B9RQCTF_LENOVO (58)) - SQLQuery2 sql - BILLA RAJINI bank_data (DESKTOP-B9RQCTF_LENOVO (58)) - Microsoft SQL Server Management Studio 26-02-2026 23_32_13" src="https://github.com/user-attachments/assets/67e8a4aa-a4f5-464b-9879-75d27dc1802d" />
<img width="970" height="557" alt="SQLQuery2 sql - BILLA RAJINI bank_data (DESKTOP-B9RQCTF_LENOVO (58)) - SQLQuery2 sql - BILLA RAJINI bank_data (DESKTOP-B9RQCTF_LENOVO (58)) - Microsoft SQL Server Management Studio 26-02-2026 23_32_24" src="https://github.com/user-attachments/assets/5f2f1b85-1fa5-4da4-b710-3d4bdf8101e3" />
<img width="980" height="565" alt="SQLQuery2 sql - BILLA RAJINI bank_data (DESKTOP-B9RQCTF_LENOVO (58)) - SQLQuery2 sql - BILLA RAJINI bank_data (DESKTOP-B9RQCTF_LENOVO (58)) - Microsoft SQL Server Management Studio 26-02-2026 23_32_43" src="https://github.com/user-attachments/assets/12ea8819-97aa-4b1c-9c9e-b25fa09a8ba2" />
<img width="908" height="542" alt="SQLQuery2 sql - BILLA RAJINI bank_data (DESKTOP-B9RQCTF_LENOVO (58)) - SQLQuery2 sql - BILLA RAJINI bank_data (DESKTOP-B9RQCTF_LENOVO (58)) - Microsoft SQL Server Management Studio 26-02-2026 23_32_55" src="https://github.com/user-attachments/assets/a15218c5-bbba-46b5-b312-6a48e049f872" />
<img width="950" height="555" alt="SQLQuery2 sql - BILLA RAJINI bank_data (DESKTOP-B9RQCTF_LENOVO (58)) - SQLQuery2 sql - BILLA RAJINI bank_data (DESKTOP-B9RQCTF_LENOVO (58)) - Microsoft SQL Server Management Studio 26-02-2026 23_33_08" src="https://github.com/user-attachments/assets/b6f6ed85-8021-4fdf-ae06-16a4d67a03e2" />
<img width="966" height="510" alt="SQLQuery2 sql - BILLA RAJINI bank_data (DESKTOP-B9RQCTF_LENOVO (58)) - SQLQuery2 sql - BILLA RAJINI bank_data (DESKTOP-B9RQCTF_LENOVO (58)) - Microsoft SQL Server Management Studio 26-02-2026 23_33_26" src="https://github.com/user-attachments/assets/d997918f-4159-409f-91a9-b442492a8039" />
<img width="990" height="548" alt="SQLQuery2 sql - BILLA RAJINI bank_data (DESKTOP-B9RQCTF_LENOVO (58)) - SQLQuery2 sql - BILLA RAJINI bank_data (DESKTOP-B9RQCTF_LENOVO (58)) - Microsoft SQL Server Management Studio 26-02-2026 23_33_37" src="https://github.com/user-attachments/assets/bf1a250b-5cbc-4ed1-840b-fefde0b8ac77" />
<img width="956" height="563" alt="SQLQuery2 sql - BILLA RAJINI bank_data (DESKTOP-B9RQCTF_LENOVO (58)) - SQLQuery2 sql - BILLA RAJINI bank_data (DESKTOP-B9RQCTF_LENOVO (58)) - Microsoft SQL Server Management Studio 26-02-2026 23_33_47" src="https://github.com/user-attachments/assets/9be2fa8f-a042-4638-860b-1c24114b580d" />
<img width="965" height="572" alt="SQLQuery2 sql - BILLA RAJINI bank_data (DESKTOP-B9RQCTF_LENOVO (58)) - SQLQuery2 sql - BILLA RAJINI bank_data (DESKTOP-B9RQCTF_LENOVO (58)) - Microsoft SQL Server Management Studio 26-02-2026 23_33_57" src="https://github.com/user-attachments/assets/00886f2c-ff67-4695-8eb1-a7489b4ef2a8" />


                                                DASH BOARD  

# 📈 Power BI Dashboard

The dashboard provides:
- KPI cards for all 12 key metrics
- Loan status donut / bar charts
- State-level geographic heatmap
- Year-wise loan growth line chart
- Risk segmentation treemap / bar
- Term vs. default rate comparison
- Interactive slicers for year, state, purpose, and risk level

---
## 📋 KPI Summary

| KPI | Value |
|---|---|
| Total Loan Applications | 270,000 |
| Total Loan Amount | $4 Billion |
| Avg. Loan Amount | $15,410 |
| Default Rate | 6.60% |
| Charged-Off Count | 18,000 |
| High-Risk Loan Count | 19,000 |
| Payment Completion | ~50% |
                        
                                                
<img width="1217" height="502" alt="image" src="https://github.com/user-attachments/assets/707d7b66-2da2-47ee-80f8-f83f9105da62" />

## OVER ALL REVIEW ##
"The bank demonstrated significant performance growth in 2015, driven by increased loan disbursement and improved repayment rates. Post-2015, a consistent reduction in default ratio was observed even as portfolio volume expanded — indicating stronger underwriting standards and risk controls. The data supports a stable, growing lending operation with targeted opportunities for improvement in long-term loan default management and collections efficiency."
