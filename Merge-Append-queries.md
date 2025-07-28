MERGE

Like we use join in sql we use merge in Powerbi
To merge column from two ....
<img width="924" height="847" alt="image" src="https://github.com/user-attachments/assets/b86797ef-a0c9-47e9-ad1a-d251a9939713" />
If i want to add city and country just after emoployee name then we use merege;
<img width="861" height="797" alt="image" src="https://github.com/user-attachments/assets/ff8c78a9-a8eb-48cd-9981-9d51b4ccdea0" />
we select only city and country: 
<img width="892" height="699" alt="image" src="https://github.com/user-attachments/assets/568975bf-1453-4406-bd87-1a215dae8673" />
Finally done
<img width="677" height="796" alt="image" src="https://github.com/user-attachments/assets/40d0a93f-7786-4108-913f-5aa8c0185f31" />



now to APPENDING data
<img width="301" height="126" alt="image" src="https://github.com/user-attachments/assets/e33dc92a-39a0-49c3-95e8-85da7ee3a71d" />

🔹 Append Queries (जैसे Excel में नीचे जोड़ना)
Append is used when you want to combine rows from two or more tables with same column structure.

📌 Use case: Combine data from different months or files (e.g., Jan.csv + Feb.csv).

Example:
You have two tables:

Sales_Jan

Sales_Feb
👉 Append will combine rows into one table: Sales_All

text
Copy
Edit
Sales_Jan       Sales_Feb        →        Append →       Sales_All
Date | Sales     Date | Sales              Date | Sales
1/1  | 100        1/2  | 200               1/1  | 100  
                                       +   1/2  | 200
📍 In Power BI:

Go to Home > Append Queries

Choose either Two Tables or Three or more tables

🔹 Merge Queries (जैसे SQL JOINs)
Merge is used to combine columns from two tables based on a common key column (like VLOOKUP or SQL JOIN).

📌 Use case: Add customer details to a sales table using CustomerID.

Example:
You have:

Orders table (has CustomerID)

Customers table (has CustomerID, Name)

👉 Merge on CustomerID to bring Name into Orders.

text
Copy
Edit
Orders             Customers            →     Merge →     Orders with Customer Name
OrderID | CustID   CustID | Name                       OrderID | CustID | Name
101     | C001     C001   | Alex                        101     | C001   | Alex
📍 In Power BI:

Go to Home > Merge Queries

Select primary and related table

Choose matching columns (like CustomerID)

Select Join Type (Default: Left Outer)

Join Types in Merge:

Join Type	Description
Left Outer	All from first table, matching from second
Right Outer	All from second, matching from first
Inner	Only matching rows from both
Full Outer	All rows from both tables
Anti Joins	Rows that don’t match

✅ Summary Table
Feature	Append Queries	Merge Queries
Use	Combine rows	Combine columns
Like	Excel stack / UNION	VLOOKUP / SQL JOIN
Input	Same structure tables	Key column needed
Output	Single large table	Table with extra columns
