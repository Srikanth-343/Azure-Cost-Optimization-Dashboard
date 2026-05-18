# Azure Cloud Cost Optimization Dashboard

An interactive analytics dashboard built in Databricks AI/BI that analyzes Azure cloud spending patterns and identifies cost optimization opportunities across services.

---

## 📊 Data Source

- **Table:** `db_cloud_cost_project.default.azure_cost_data`
- **Scope:** 10 Azure services (monthly tracking)
- **Time Period:** May 2023 – Apr 2024
- **Total Spend:** ~$4,197 USD

---

<img width="1920" height="1080" alt="Screenshot (111)" src="https://github.com/user-attachments/assets/cfd00be8-697f-4539-96ee-2bef7922bff7" />


## 📈 Dashboard Components

### KPIs
- Total spend
- Average cost per record
- Cost spike ratio

### Service Breakdown
- Bar chart: cost ranking by service
- Pie chart: cost distribution across services

### Trends
- Line chart: monthly cost evolution per service

### Volatility Analysis
- Spike ratio (max vs average cost) to detect unstable usage

### Optimization Actions
- Recommendations table with estimated savings per service

### Data View
- Detailed table: total cost, average cost, max cost, record count

---

## 🔍 Key Findings

- Storage and Bandwidth account for ~78% of total spend
- Virtual Machines show highest volatility (2.8x spike ratio), suggesting opportunity for auto-shutdown or reserved instances
- Backup costs increased sharply from $0.23 to $77/month — indicates policy or configuration change
- VM Licensing costs are stable and can be reduced using Azure Hybrid Benefit (40–55% savings)
- Estimated total savings potential: **$80–$150/month (20–40% reduction)**

---

## 💡 Cost Optimization Insights

### 1. Storage (~$142/month)
- Steady growth trend
- Recommendation: implement lifecycle policies (Hot → Cool → Archive)
- Estimated savings: 20–40%

### 2. Bandwidth (~$129/month)
- Stable but high cost
- Recommendation: enable CDN and compression
- Estimated savings: 15–30%

### 3. Backup (~$45/month avg, sharp spike)
- Sudden cost increase detected
- Recommendation: review retention and backup policies
- Estimated savings: 20–35%

### 4. Virtual Machines (~$15/month avg)
- Highly volatile usage
- Recommendation: auto-shutdown or reserved instances
- Estimated savings: 30–60%

### 5. VM Licenses (~$26/month avg)
- Stable recurring cost
- Recommendation: apply Azure Hybrid Benefit
- Estimated savings: 40–55%

---

## ⚙️ Features

- Global service filter for interactive analysis
- KPI-based dataset model using reusable metrics
- Time-series cost trend analysis
- Volatility detection via spike ratio
- Azure-themed responsive dashboard layout

---

## 🧠 Summary

Total monthly spend is approximately **$380/month**.

Key optimization opportunities:
- Backup policy correction
- VM right-sizing / scheduling
- Storage lifecycle management
- Licensing optimization

**Overall potential savings:** $80–$150/month (20–40%)

---

## 🛠️ Technologies

- Databricks AI/BI Dashboards
- SQL / Delta Lake
- Azure Data Platform
- Azure Cloud Billing Dataset
- Data Modeling & KPI Design
