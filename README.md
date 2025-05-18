# SpauldingRidgeCaseStudy

# Employee Compensation Forecasting Tool  
**A C# application to analyze compensation data and simulate salary adjustments**  

---

##  Tools Used  
- **C#/.NET**: Windows Forms application  
- **SQLite**: Database storage (`employees`, `ratings`, `industry_compensation` tables)  
- **MySQL Workbench**: Initial database design  
- **Visual Studio**: IDE for C# development  
- **Excel**: Data cleaning (fixed typos, outliers, inconsistencies)  
- **HTML/JS**: Prototype web interface (optional)  

---

##  Data Cleaning  
### Issues Fixed:  
1. **Typos**:  
   - `"Senir Associate"` → `"Senior Associate"`  
   - `"Banglore"` → `"Bangalore"`  
2. **Outliers**:  
   - 5 records with compensation ±40% from market average  
3. **Inactive Employees**:  
   - Fixed 7 records with conflicting `is_active` status  

### SQL Cleaning Example:  
```sql  
UPDATE employees  
SET role = 'Senior Associate'  
WHERE role LIKE 'Senir%';

Key Features
1. Filter Employees: By role/location

2. Forecast Raises: Adjust global or role-specific %

3. Visualize Data: Bar/pie charts in C# app

4. Export Reports: CSV files for HR

5. Risk Alerts: Low-rated + underpaid employees

Note for GitHub Users
This is my first GitHub repository!

1. May lack standard conventions (folder structure, .gitignore)

2. Basic commit history ("fixed errors", "updated code")

3. Open to feedback on improving repository quality!

Setup Instructions
1. Database Setup:
Download compensation.db

Open in DB Browser for SQLite

2. Run C# Application:
Open CompensationTool.sln in Visual Studio

Build solution (Ctrl + Shift + B)

Run (F5)

3. Web Interface (Optional):
cd web-interface  
python -m http.server 8000

Key Findings
1. Pune: Highest turnover (13.3%)

2. Associates: Paid 8.2% below market avg

3. 32 Employees: High turnover risk (low ratings + pay gap)

How to Contribute
1. Report issues in GitHub Issues

2. Suggest code improvements

3. Share visualization ideas

+ Working Features: Filtering, Forecasting, CSV Export  
- Needs Work: Error Handling, Role-Specific Adjustments


License
MIT License
