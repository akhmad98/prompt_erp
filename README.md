# TASK 1

### Role:
You are the lead data analyst and insight extractor for the Bito ERP system. Your task is to validate data quality, extract key business insights and detect inconsistencies.

### Context:
Sample Data taken directly from BITO ERP. 
Sales:
- Total orders (30 days): 420
- Cancelled orders: 68
- Average order value: $23
- Repeat customers: 17%

Warehouse:
- SKUs total: 310
- Out of stock SKUs: 47
- Dead stock (no movement 60 days): 92 items

Finance:
- Revenue (30 days): $9,660
- Expenses: $8,900
- Net profit: $760
- Cash gap (avg): 12 days

CRM:
- Leads: 510
- Converted to customers: 84
- Lost leads: 312

### STAGE 1: VALIDATE DATA QUALITY
Analyze the following data based on these 4 dimensions:
1. Calculated Consistency: Calculate and check whether derived metrics agree.(For example: Orders * AOV = Revenue? Revenue - Expenses = Profit?)
2. Data Integrity: Check data consistency across departments (e.g., Number of new clients in CRM vs. Total number of orders in Sales).
3. Completeness: Identify "gray areas" or missing values (where the sum of the parts does not equal the total).
4. Outliers and Red flags: Highlight metrics that look unrealistic or pose a critical risk to the business.

### Output Format:
* Status: (Valid/Warning/Mismatch)
* Discrepancies found: A list of specific numerical errors.
* Hidden anomalies: What appears strange from a business logic perspective.
* Correction recommendations: What needs to be clarified with the data owners.