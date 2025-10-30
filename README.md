🚀 Project Overview

Manual data handling in supply chain processes often leads to delays and inconsistencies.
This project automates that workflow by:

Extracting CSV files from Gmail using n8n
Inserting structured records into a Supabase database
Analyzing and visualizing the data in Quadratic
Fetching exchange rates via the Open Exchange Rates API for cost normalization

🧩 Tools & Technologies
Tools Used 
n8n- Workflow automation (Gmail → Supabase data pipeline)
Supabase- Cloud database for storing and querying records
Quadratic- Interactive spreadsheet-like tool for data analytics
Open Exchange Rates API- Historical exchange rate data (for currency conversion)
Python- Used for fetching and transforming external data (optional scripts)

⚙️ Workflow Overview

Step 1: Gmail → n8n
n8n connects to Gmail via OAuth2.
It automatically fetches new supply chain CSV attachments.

Step 2: n8n → Supabase
The files are parsed and inserted into Supabase tables.
Table includes columns like Order_ID, Product, Quantity, Date, and Cost.

Step 3: Supabase → Quadratic
Quadratic connects to Supabase via connection URL.
Data is analyzed for trends, performance, and bottlenecks.

Step 4: Exchange Rate Integration (optional)
The Python script fetches daily INR/USD rates
These rates are stored in the exchange_rate table for financial analysis.


