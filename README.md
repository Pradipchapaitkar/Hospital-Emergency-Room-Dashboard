# 🏥 Hospital Emergency Room Dashboard

## 📌 Project Overview
This project focuses on analyzing emergency room patient data to enhance hospital efficiency and patient experience.
Using **Excel**, we visualize key healthcare metrics, including wait times, patient admissions, and department referrals.
The dashboard enables **hospital administrators and decision-makers** to quickly assess performance and take necessary actions for improvement.

## 📊 Key Features
- **📌 Patient Admission Tracking** – Categorizes admitted vs. non-admitted patients.
- **📌 Age Distribution Analysis** – Groups patients into specific age ranges.
- **📌 Wait Time Insights** – Tracks average patient wait time.
- **📌 Gender Breakdown** – Displays the number of male vs. female patients.
- **📌 Department Referrals** – Analyzes where patients are referred within the hospital.
- **📌 Interactive Filters** – Allows users to filter data by month and year.

## 📁 Repository Structure
```plaintext
📂 hospital-emergency-dashboard
├── 📊 Hospital Emergency Room Dashboard Project.xlsx  # Dataset
├── 🖼️ Hospital Dashboard Final.jpg                  # Dashboard visualization
├── 📄 README.md                                     # Project documentation
├── 📂 Power BI Files (Coming Soon)                 # Power BI dashboard files
└── 📄 END TO END DASHBOARD PROJECT IN EXCEL.pptx    # Project presentation
```

## 📊 Data Processing & Formulas
### **📅 Calendar Table Creation**
```DAX
= List.Dates(#date(2023,01,01),731,#duration(1,0,0,0))
```
### **👥 Age Group Classification**
```DAX
=IF([Patient Age]>=70,"70-79",
IF([Patient Age]>=60,"60-69",
IF([Patient Age]>=45,"45-59",
IF([Patient Age]>=30,"30-44",
IF([Patient Age]>=15,"15-29",
IF([Patient Age]>=5,"05-14","0-4"))))))
```
### **⏳ Patient Attended Within Time**
```DAX
= IF ([Patient  Waittime ]<30, "Within Time" , "Delayed" )
```
### **📈 Patient Satisfaction Score Calculation**
```DAX
= AVERAGE([Satisfaction Score])
```

## 🛠 Technology Stack
- **📊 Excel** – Data cleaning, storage, and pivot tables.
- **📈 Power BI** – Interactive data visualization.
- **🖩 DAX (Data Analysis Expressions)** – Advanced data modeling.
- **📂 CSV/XLSX** – Standardized data formats.

## 🤝 Contribution Guidelines
1. **Fork the Repository** – Click the **Fork** button to copy the repo.
2. **Clone the Repository** – Run the command:
   ```bash
   git clone https://github.com/your-username/hospital-emergency-dashboard.git
   ```
3. **Make Improvements** – Enhance charts, optimize formulas, or add new visuals.
4. **Submit a Pull Request** – Push your changes and open a PR for review.

## 🎯 Future Enhancements
- ✅ Integration with **real-time hospital data**.
- ✅ Addition of **more detailed patient insights**.
- ✅ Development of a **Power BI web dashboard**.
- ✅ Implementation of **predictive analytics for hospital efficiency**.

## 📢 Join Us!
Let’s collaborate to create a **data-driven solution for healthcare analytics!** 🚀

#️⃣ **Tags:** `#DataAnalytics` `#Excel` `#PowerBI` `#DAX` `#Healthcare` `#Visualization` `#Dashboard`

