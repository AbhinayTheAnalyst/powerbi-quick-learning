<img width="1211" height="395" alt="image" src="https://github.com/user-attachments/assets/26ab748b-76e0-4ff1-8352-9aa30e582a00" />
🔍 Power BI: Calculated Column vs Measure (Explained Simply)
When learning Power BI and DAX, one of the most confusing parts is understanding the difference between a Calculated Column and a Measure. Here's a clear breakdown with examples and best practices.

✅ What is a Calculated Column?
A calculated column is created row-by-row in your table.

It behaves like a new column added to your dataset.

The calculation is performed when the data is loaded or refreshed.

It takes space in the data model.

Example 1 – Pass/Fail logic using IF:

DAX
Copy
Edit
Result = IF(Sheet1[Marks] >= 33, "Pass", "Fail")
Example 2 – Grading system:

DAX
Copy
Edit
Grade = 
IF(Sheet1[Marks] >= 90, "A",
    IF(Sheet1[Marks] >= 75, "B",
        IF(Sheet1[Marks] >= 50, "C", "F")
    )
)
🟢 Use Calculated Columns when:

You need to filter, slice, or group data using the new values.

The value is static per row (like category, flag, tag, label etc.).

✅ What is a Measure?
A measure performs aggregated calculations on data.

It is calculated on the fly during interaction with visuals.

It does not take storage in your dataset — more efficient.

It only works when used in visuals (like Cards, Charts, Tables, etc.)

Example – Total Revenue:

DAX
Copy
Edit
Total Revenue = SUM(Sheet1[Revenue])
Important Note:
If you try to write SUM(Sheet1[Revenue]) inside a calculated column, it will return same total value in every row. That’s why aggregations should be done using measures.

🟢 Use Measures when:

You want to calculate totals, averages, max, min, count etc.

You are building KPIs, dashboards, or summaries.

⚠ Common Mistake:
❌ Trying to use SUM() inside a calculated column:

DAX
Copy
Edit
WrongColumn = SUM(Sheet1[Revenue])  -- This gives same value in every row!
Instead:

✅ Use it as a measure:

DAX
Copy
Edit
Total Revenue = SUM(Sheet1[Revenue])  -- Use this in visuals
🧠 Summary:
Feature	Calculated      Column	Measure
Works per	Row	Entire    dataset (aggregated)
Storage in model?	Yes    	No

When calculated?	Data refresh/load time	At runtime (on visual interaction)
Where to use?	As part of table columns	In charts, cards, KPIs
Example	IF(Marks > 33, "Pass", "Fail")	SUM(Revenue)
