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

### STAGE 2: DETECT INCONSISTENCIES OR RED FLAGS
1. Outliers and Red flags: Highlight metrics that look unrealistic or pose a critical risk to the business.

### STAGE 3: EXTRACT KEY BUSINESS INSIGHTS
1. Risk Detection: Highlight unrealistic metrics or those posing critical business risks.
2. Anomaly Detection: Flag anything that contradicts standard business logic.


### Output Format:
* Status: (Valid/Warning/Mismatch)
* Discrepancies found: A list of specific numerical errors.
* Hidden anomalies: What appears strange from a business logic perspective.
* Correction recommendations: What needs to be clarified with the data owners.


# TASK 2


### Role:
You are the lead business analyst or COO. Your task is to explain WHY a problem exists and WHAT to do.

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

### Analysis Focus:
1. The WHY:
Using figures provided several "holes" identified throug which money is wasted.
* why is the conversion rate so low with 510 leads
* why 16% of orders canceled
* how does out-of-stock affect cancelled orders
* why 61% of leads lost
* why net profit is 7.8% and cash gap is 12 days
* why dead stock is 30%

2. Impact/Effort:
Present the solution as a table sorted by priority.
    1. Action: Specific operational step (no generalities).
    2. Rationale: What report number will this change?
    3. Difficulty: (Low/Medium/High).
    4. Impact on profit: (1-10).

3. Identify one "Quick Win" action that needs to be implemented immediately to close the cash gap or salvage net profit.

### Output format:
A bulleted list of specific numerical errors and logical gaps with priority actions.



# Task 3

### Role:
You are ERP Process Consultant for Bito ERP. Your task is to recommend specific changes inside Bito ERP to improve process.

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

### Task: 
Formulate the technical specifications for changing the settings within Bito ERP.

### Requirements based on modules:
1. Inventory & Purchasing:
Describe how to set up automatic reorder rules. Specify the Min/Max parameters for 47 out-of-stock SKUs to eliminate 68 cancellations.
2. Sales & Pricing:
How can I programmatically implement a sale of 92 Dead Stock items? Describe how to create a new "Price List" with the "Valid for Category: DeadStock" condition and apply it to the lost leads segment.
3. Workflow & Approvals:
What Validation Rules should be added to the Sales Order confirmation process to prevent items with zero inventory from being sold?
4. Finance Reporting:
What custom dashboards do you recommend setting up to monitor Cash Gap in real time so that net profit increases from the current $760?

### Output Format:
A list of specific actions inside Quotation Marks (" ") in the ERP interface in format of bullet list. Only hardcore system settings.
Example:
* "Enable low-stock alerts when SKU < X”
* “Block purchasing for dead stock categories”