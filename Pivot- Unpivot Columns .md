<img width="754" height="274" alt="image" src="https://github.com/user-attachments/assets/8179c25e-42e7-4a75-8cec-66120886946d" />
🌀 1. Unpivot Columns – Jab data horizontal ho par usse vertical banana ho
📘 Example:
Name	Jan	Feb	Mar
Abhinay	100	120	130
Golu	80	110	125

🛠️ After Unpivot (Jan, Feb, Mar):

Name	Month	Sales
Abhinay	Jan	100
Abhinay	Feb	120
Abhinay	Mar	130
Golu	Jan	80
Golu	Feb	110
Golu	Mar	125

✅ Use When:
Har mahine ka column alag ho

Tu chahata hai ek vertical structure (Month & Value)

🔧 Steps to Unpivot:
Select columns like Jan, Feb, Mar

Right-click → Unpivot Columns

Columns banenge: Attribute, Value

Rename: Attribute to Month, Value to Sales (for clarity)

<img width="141" height="137" alt="image" src="https://github.com/user-attachments/assets/33880d49-5f25-4652-b325-656598247fdd" />

🏛️ 2. Pivot Columns – Jab same person ke multiple rows ho, unhe horizontal banana ho
📘 Example Before Pivot:
Name	Month	Sales
Abhinay	Jan	100
Abhinay	Feb	120
Abhinay	Mar	130
Golu	Jan	80
Golu	Feb	110
Golu	Mar	125

🔁 After Pivoting Month:

Name	Jan	Feb	Mar
Abhinay	100	120	130
Golu	80	110	125

✅ Use When:
Data vertical hai

Tu chahata hai columns me month-wise values aa jayein

🔧 Steps to Pivot:
Select Month column → Go to Transform → Click Pivot Column

Values Column = Sales

Power BI automatically generates columns: Jan, Feb, Mar

🧠 Pro Tip:
Unpivot = Flat structure = Best for charts

Pivot = Summary view = Useful for viewing at-a-glance data

📍 Real Life Analogy:
Unpivot = Jaise table ke sare kapde (columns) ek hanger pe daal do (vertical)

Pivot = Jaise sare kapde firse alag hangers pe (horizontal) rakh do person-wise
