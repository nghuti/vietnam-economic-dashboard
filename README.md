# Vietnam Economic Dashboard After Provincial Merger Dashboard

An interactive Power BI dashboard analyzing the socio-economic landscape of Vietnam's 34 provinces following the administrative merger, covering GDP, population, income, and geographic distribution.

---

## 📊 Dashboard Preview

<img width="1112" height="610" alt="Dashboard" src="https://github.com/user-attachments/assets/30c85f95-bb97-4592-aa8e-caea61e16af7" />

## 📁 Project Structure

vietnam-economic-dashboard/
│
├── Dashboard_Kinh_te_VN_sau_sap_nhap.pbix   # Power BI dashboard file
├── Danh_sach_34_tinh_thanh_theo_Map.xlsx     # Province mapping data
├── Dashboard.png                              # Dashboard screenshot
└── README.md
```


## 🎯 Objective

Following Vietnam's provincial merger reducing the number of provinces to 34, this project aims to:
- Visualize the new economic landscape by region and province
- Compare GDP, income per capita, population density across regions
- Provide an interactive map-based view of the restructured administrative units


## 🛠️ Tools Used

| Tool | Purpose |
|------|---------|
| Power BI | Data modeling, DAX measures, dashboard |
| Power Query | Data cleaning and transformation |
| Excel | Province mapping reference data |
| Web Scraping (Power BI) | Imported data directly from websites |


## 🔄 Workflow

### 1. Get Data
- Connected to web sources directly via Power BI's **Get Data → Web** feature
- Selected and filtered relevant tables from source pages

### 2. Power Query — Data Cleaning & Transformation
- **Filled down** null values in merged cells from web tables
- **Merged queries** to compare province names across two data sources, identified mismatches and standardized values
- **Removed duplicate rows**
- **Split cell values** into multiple rows using delimiter (line feed) to normalize data
- **Created custom column** using `Text.BetweenDelimiters` to extract values from parentheses

### 3. Data Modeling & DAX
- Built relationships between tables
- Created key measures:
  - `GDP` — Total GDP by province/region
  - `GDP per capita` — GDP / Population
  - `Population Density` — Population / Area (km²)
  - `Average Income per person`

### 4. Dashboard Design
- KPI cards for top-level metrics
- Donut chart for GDP by region (Miền Bắc / Nam / Trung)
- Treemap for GDP by vùng miền
- Map visual for geographic distribution
- Bar chart for GDP by province (Top provinces)
- Detail tables for region and province breakdown


## 📈 Key Metrics

| Metric | Value |
|--------|-------|
| Total GDP | $450.58 Tỷ |
| Total Population | 113.57 triệu người |
| Total Area | 331.33K km² |
| Avg Income per person | $3,967.38 |
| Population Density | 343 ng/km² |


## 💡 Key Findings

- **Đông Nam Bộ** leads with the highest GDP ($140.55 Tỷ) and income per capita ($6,462.58/người)
- **Hồ Chí Minh** is the top province by GDP ($104.94 Tỷ), nearly double Hà Nội ($55.08 Tỷ)
- **Miền Nam** contributes the most to national GDP (42.66%), followed by Miền Bắc (38.08%)
- **Tây Bắc Bộ** has the lowest income per capita ($2,345.42), highlighting regional economic disparity
- **Bắc Ninh** stands out with high income ($4,694.91/người) despite smaller population — driven by FDI manufacturing


## 🧠 Skills Demonstrated

- Web data extraction using Power BI native connector
- Advanced Power Query transformations (fill down, merge, split by delimiter, custom columns)
- DAX measure creation
- Data modeling with table relationships
- Dashboard design and layout in Power BI


## 📝 Notes

> Data sourced from publicly available Vietnamese government and statistical websites. This project was independently built to practice Power BI skills in the context of Vietnam's 2025 provincial restructuring.




