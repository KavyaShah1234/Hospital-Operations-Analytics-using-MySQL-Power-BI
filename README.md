# Healthcare-mysql-analytics
This project analyzes hospital operational data to identify utilization trends, readmission patterns, and procedure insights.
## 🛠️ Tech Stack

- **Database:** MySQL  
- **Query Tool:** PopSQL  
- **Language:** SQL  
- **Data Processing:** Relational database operations  

---

## 📂 Dataset Description

The dataset consists of multiple relational healthcare tables used for analysis:

- `encounters` → Patient visit records  
- `patients` → Patient demographic information  
- `procedures` → Medical procedures performed  
- `payers` → Insurance / coverage information  
- `organizations` → Hospital / healthcare providers

---

## Business Recommendations

Based on the analysis, the following recommendations were identified:

### 1. Expand Mental Health Capacity
Mental health–related procedures were among the most frequently performed, indicating sustained demand. The hospital should evaluate therapist availability, appointment wait times, and patient load to determine whether additional behavioral health professionals are required.

### 2. Investigate Annual Spikes in Encounters
Encounter volume increased significantly during specific years. Further investigation into seasonal trends, disease outbreaks, policy changes, or operational factors could help explain these fluctuations and improve future capacity planning.

### 3. Improve Financial Assistance for Uninsured Patients
Nearly half of all encounters had zero payer coverage, exposing the hospital to potential revenue loss. Establishing financial counseling services and assisting eligible patients with insurance or government subsidy enrollment could improve reimbursement rates.

### 4. Monitor Patients with Frequent Readmissions
Several patients experienced repeat encounters within 30 days. Identifying the underlying causes of these readmissions and implementing targeted follow-up programs may improve patient outcomes while reducing unnecessary hospital utilization.

### 5. Optimize Resource Allocation
Ambulatory encounters accounted for the majority of hospital visits. Resource planning should reflect this demand while ensuring sufficient capacity is maintained for emergency and inpatient care.
---

## 🧠 Key SQL Concepts Used

### 1. Aggregations
Used to summarize large datasets into meaningful business metrics such as:
- Total encounters per year  
- Average cost per payer  
- Procedure frequency distribution  

---

### 2. Joins
Used to combine data across related tables and enable multi-entity analysis such as:
- Linking patients with their encounters  
- Mapping procedures to specific encounters  
- Connecting payer information with billing data  

---

### 3. Common Table Expressions (CTEs)
Used to break complex queries into structured and readable steps.

Applied in:
- Readmission analysis  
- Multi-step filtering logic  
- Intermediate result computation for patient behavior analysis  

---

### 4. Window Functions
Used for advanced analytical queries on sequential data.

Example use case:
- `LAG()` function to compare consecutive encounters for the same patient  
- Identification of readmissions within a defined time window  

---

### 5. Date & Time Functions
Used for time-based analysis:
- `YEAR()` → yearly trends  
- `QUARTER()` → quarterly patient distribution  
- `DATEDIFF()` → readmission and duration calculations

## Dashboard Preview

![Healthcare Dashboard Preview](Hospital_Dashboard.png)
