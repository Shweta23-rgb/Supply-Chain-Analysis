# Supply-Chain-Analysis: 

Data analysis of USAID HIV shipment records to uncover cost inefficiencies and optimize supply chain strategy using Python.

Context: I worked on a supply chain shipment anlaytics project using real time  shipment data from USAID (usaid-data.gov). The dataset included over 10K records tracking global shipments of HIV and malaria related diagnostic tests, ARV treatments and Anti Malarial drugs. Almost 84% of the orders in the dataset were destined for African countries, making this project relevant to global public health efforts. 

**Why:**

We wanted to understand what was driving up costs and delays in delivering critical HIV and malaria-related health products. The goal was to use data to help optimize global health supply chains, especially in resource-constrained regions.

**Action:**
I started by loading the dataset into Python and using Pandas for initial exploration. The dataset had over 10,000 records with fields related to shipment mode, product group, vendor, cost, and delivery dates.

As part of data cleaning, I handled missing values in key operational fields and dropped irrelevant or low-quality columns such as internal IDs, dosage, and incomplete date entries. I also standardized datatypes across numeric and date columns.

For outlier handling, I applied Winsorization at the 5th and 95th percentiles to cap extreme values in freight cost and quantity without removing data points — preserving the dataset size while reducing distortion from outliers.

During preprocessing, I mapped coded fields like product group abbreviations (e.g., ARV → Anti-Retroviral Treatment) and expanded Incoterms (e.g., EXW, DDP) to their full forms to improve interpretability.

I then performed feature engineering, where I grouped countries into continents to enable regional analysis and created a new feature by calculating the difference between planned and actual delivery dates — which helped us assess delay patterns and their impact on cost.

In short: We cleaned the dataset by removing irrelevant columns, handling missing values, and standardizing types. We capped extreme values using Winsorization to reduce skew. Then we mapped product and shipping codes to full names, grouped countries by continent, and engineered a delay feature to analyze the impact of late deliveries on cost.

**Insigts:**

African countries had the highest freight costs ( total transportation costs including insurance,  — especially Cameroon, Kenya, and Nigeria.

Air shipping accounted for over 62% of total freight costs — much higher than trucking (17.8%) or ocean freight (5.6%). This suggested that shifting more shipments to sea or land routes could reduce costs where timelines allow.

HIV Rapid Diagnostic Tests (HRDTs) had the highest average freight cost per shipment, followed by ACTs and ARVs. Malaria RDTs (MRDTs) had the lowest average freight cost.

ARVs (Anti-Retroviral Treatments) alone made up 84.2% of total insurance costs, showing that the cost to insure different product types varies widely, and ARVs dominate the shipment value.

By proposing routing adjustments — like switching non-urgent air shipments to ocean — we estimated a potential cost reduction of 2% and delivery speed gains of 1.5%, especially in countries with repeat delay patterns.”






