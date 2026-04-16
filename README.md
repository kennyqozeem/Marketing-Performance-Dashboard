# 📊 Marketing Performance Dashboard

A Power BI report that tracks and analyzes key marketing metrics across ad campaigns, course performance, locations, and platforms — enabling data-driven decisions for marketing teams.

---

## 📁 File

| File | Description |
|------|-------------|
| `Marketing_Performance.pbix` | Power BI Desktop report file |

---

## 📌 Overview

This dashboard provides a single-page overview of marketing performance for an online course business. It surfaces key engagement, reach, and conversion metrics segmented by course, location, ad campaign platform, and time.

The report is built using the **"New Executive"** theme and is optimized for a **1280 × 720** canvas.

---

## 📐 Report Structure

### Pages

| Page | Display Name |
|------|--------------|
| Page 1 | Marketing Performance |

---

## 📊 Visuals Inventory

### KPI Cards (Top Row)

A row of KPI cards spans the top of the dashboard, giving at-a-glance metrics:

| Metric | Description |
|--------|-------------|
| **Landing Page Views** | Total views on the landing page |
| **Avg Conversion Rate** | Average rate at which ad views convert to sign-ups |
| **Average Ads** | Average number of ads per period |
| **Average Impression** | Average ad impressions |
| **Average Sign Ups** | Average sign-ups per period |
| **Average Clicks** | Average number of ad clicks |

### KPI Cards (Left Sidebar)

A vertical sidebar on the left side of the dashboard displays cumulative totals:

| Metric | Description |
|--------|-------------|
| **Total Ads** | Total number of ads run |
| **Total Course** | Total number of courses tracked |
| **Total Clicks** | Total ad clicks |
| **Total Sign Ups** | Total course sign-ups |
| **Total Impression** | Total ad impressions |

---

### Charts & Visuals

#### 1. Course Performance Table
- **Type:** Table
- **Columns:** Course Title, Avg Conversion Rate, Total Ads
- **Sorting:** Ascending by Course Title
- **Conditional Formatting:** `Avg Conversion Rate` values are color-coded using a red-to-green gradient (low → high)

#### 2. Ads by Ad Campaign Platform (Donut Chart)
- **Type:** Donut Chart
- **Category:** Ad Campaign Platform
- **Measure:** Total Ads
- **Title:** *Ads by Ad Campaign Platform*

#### 3. Sign Ups by Location (Clustered Column Chart)
- **Type:** Clustered Column Chart
- **X-Axis:** Location
- **Y-Axis:** Average Sign Ups
- **Title:** *Sign Ups by Location*

#### 4. Ads by Course (Clustered Column Chart)
- **Type:** Clustered Column Chart
- **X-Axis:** Course Title
- **Y-Axis:** Average Ads
- **Sorting:** Descending by Average Ads
- **Title:** *Ads by Course*

#### 5. Conversion Rate by Ad Campaign Platform (Donut Chart)
- **Type:** Donut Chart
- **Category:** Ad Campaign Platform
- **Measure:** Avg Conversion Rate
- **Title:** *Conversion Rate by Ad Campaign Platform*

#### 6. Ads by Date (Area Chart)
- **Type:** Area Chart
- **X-Axis:** Date Hierarchy (Year → Quarter → Month → Day)
- **Y-Axis:** Average Ads
- **Title:** *Ads by Date*

#### 7. Location Performance Table
- **Type:** Table
- **Columns:** Location, Total Ads, Total Impression, Total Sign Ups, Total Clicks, Avg Conversion Rate
- **Conditional Formatting:** `Avg Conversion Rate` is color-coded red-to-green

---

## 🗄️ Data Model

### Table: `course_marketing_performance_da`

The primary fact table containing marketing and course data.

| Column | Type | Description |
|--------|------|-------------|
| `Course Title` | Text | Name of the course |
| `Ad Campaign Platform` | Text | Platform used for the ad campaign (e.g., Facebook, Google) |
| `Location` | Text | Geographic location of the target audience |
| `Date` | Date | Date of the marketing activity, with a built-in date hierarchy (Year / Quarter / Month / Day) |

### Table: `Key Measures`

A dedicated measures table containing all DAX calculations.

| Measure | Description |
|---------|-------------|
| `Total Ads` | Total count of ads |
| `Average Ads` | Average number of ads |
| `Total Impression` | Total ad impressions |
| `Average Impression` | Average impressions |
| `Total Clicks` | Total ad clicks |
| `Average Clicks` | Average clicks |
| `Total Sign Ups` | Total user sign-ups |
| `Average Sign Ups` | Average sign-ups |
| `Total Course` | Total number of courses |
| `Avg Conversion Rate` | Average conversion rate (sign-ups relative to impressions/clicks) |
| `Landing Page Views` | Total landing page views |

---

## 🎨 Theme & Styling

| Setting | Value |
|---------|-------|
| Base Theme | CY26SU02 |
| Custom Theme | New Executive |
| Canvas Size | 1280 × 720 |
| Display Option | Fit to Page |
| Font (Tables) | wf_standard-font, Helvetica, Arial, sans-serif |
| Font (Charts) | Tahoma |
| Conditional Format (Conversion Rate) | Red (#EE0707 / #FA0F0F) → Green (#0B5A30 / #095425) |

---

## ⚙️ Report Settings

| Setting | Value |
|---------|-------|
| Export Data Mode | Allow Summarized |
| Default Drill Filter Other Visuals | Enabled |
| Allow Change Filter Types | Enabled |
| Enhanced Tooltips | Enabled |
| Stylable Visual Container Header | Enabled |
| Cross-Visual Drill Filtering | Enabled on all visuals |

---

## 🚀 Getting Started

### Prerequisites

- [Power BI Desktop](https://powerbi.microsoft.com/desktop/) (latest version recommended)

### Opening the Report

1. Clone or download this repository.
2. Open `Marketing_Performance.pbix` in Power BI Desktop.
3. If prompted, update the data source connection to point to your dataset.
4. Refresh the data using **Home → Refresh**.

### Connecting Your Data

The report expects a data source named `course_marketing_performance_da` with at minimum the following columns:

- `Course Title`
- `Ad Campaign Platform`
- `Location`
- `Date`

Replace the existing data source under **Home → Transform Data → Data Source Settings** with your own database, CSV, or API connection.

---

## 📬 Contributing

1. Fork this repository.
2. Create a feature branch: `git checkout -b feature/your-feature-name`
3. Commit your changes: `git commit -m "Add your message"`
4. Push to the branch: `git push origin feature/your-feature-name`
5. Open a Pull Request.

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).
