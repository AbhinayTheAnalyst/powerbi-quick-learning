# Change Type Using Locale in Power BI
<img width="837" height="614" alt="image" src="https://github.com/user-attachments/assets/88142bb8-a257-4b55-b5ba-b448ac054f90" />


`Change Type using Locale` in Power Query is used when your data comes from different regional formats (e.g., French decimal comma `1,23` or European date format `dd/mm/yyyy`).

## 🛠️ When to Use

Use this feature when:
- Numbers have `,` instead of `.`
- Dates follow non-US formats
- You face conversion errors during type change

## 🔄 Steps
1. Open Power Query Editor
2. Right-click on the column → Select `Change Type` → `Using Locale...`
3. Choose:
   - **Data Type** (e.g., Date, Decimal Number)
   - **Locale** (e.g., French (France), English (India))
4. Click OK

## ✅ Example

French value: `1,23` → Convert to Decimal using `French (France)` locale.

## 🔚 Summary

This ensures accurate type conversion for international datasets and avoids formatting issues.

