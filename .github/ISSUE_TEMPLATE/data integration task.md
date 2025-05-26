---
name: Data Integration Task
about: Template for integrating new data sources into the database and building data layers
title: "[Data Integration] #placeholder topic in #placeholder city"
labels: data, pipeline, modeling
assignees: anastasia
---

### 1. Find and List Data Sources
- [ ] Conduct research on the topic **#placeholder** in **#placeholder** city. Identify all relevant data sources that can enrich the listing and neighborhood datasets.
- [ ] Provide detailed documentation for each data source:
  - Origin and source (e.g. public datasets, APIs, scrapers)
  - Update frequency (e.g. hourly, daily, monthly)
  - Data type: **static** (one-time import) or **dynamic** (ongoing integration via API/scraper)

---

### 2. Modeling
- [ ] Select and document the key parameters from the raw data that are relevant for the use case.
- [ ] Define how the data will be modeled, including relationships with the existing `listings` and `neighborhoods` tables.
- [ ] Draft the final schema for the new table.

---

### 3. Review Plan with Senior
- [ ] Review the selected parameters and proposed schema with **Anastasia** for feedback and approval.

---

### 4. Transform
- [ ] Implement transformation logic using **GitHub Actions**, along with Python scripts and SQL as needed.
- [ ] Ensure all transformations result in clean, normalized, and database-ready data.

---

### 5. Insert
- [ ] Set up the data pipeline to insert transformed data into the database.
- [ ] (Optional) Automate daily data updates using scheduled GitHub Actions workflows.
