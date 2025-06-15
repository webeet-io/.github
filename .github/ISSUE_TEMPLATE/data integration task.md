---
name: Data Integration Task
about: Template for integrating new data sources into the database and building data layers
title: "[Data Integration] #placeholder topic in #placeholder city"
labels: data, pipeline, modeling
assignees: anastasia
---


This issue outlines the process for integrating a new  data layer on topic **#placeholder** in **#placeholder** into the database. The work should be completed in **3 PRs**, one for each major step.

---

## 🧪 Step 1: Research & Data Modelling

**PR Branch Name:** `layer-data-modelling`
*(e.g. `public-transport-data-modelling`)*

### 1.1 Data Source Discovery

* [ ] Conduct research on the topic **#placeholder** in **#placeholder** city.
* [ ] Identify all relevant data sources that can enrich listings and neighborhood datasets.
* [ ] Provide detailed documentation for each data source:

  * [ ] Source and origin (e.g. public datasets, APIs, scrapers)
  * [ ] Update frequency (e.g. hourly, daily, monthly)
  * [ ] Data type: **static** (one-time import) or **dynamic** (ongoing via API/scraper)

### 1.2 Modelling & Planning

* [ ] Select and document key parameters/columns from raw data relevant to the use case.
* [ ] Define how this data connects to existing tables (`coordinates`, `neighborhoods`, etc.)
* [ ] Draft and document the planned schema for the new table.
* [ ] List known data issues or inconsistencies.
* [ ] Outline the transformation plan (cleaning, normalization, structure, etc.)

### 1.3 Prepare the `sources` Directory

* [ ] Add raw data files or links to external data into the `/sources` folder.
* [ ] In `/sources/README.md`, describe:
  * [ ] The data sources used.
  * [ ] The steps planned for transformation.

### 1.4 Review
* [ ] Submit the first PR.

---

## 🛠 Step 2: Data Transformation

**PR Branch Name:** `layer-data-transformation`

* [ ] Write transformation logic using Python/SQL.
* [ ] Ensure data is clean, normalized, and matches the model defined in Step 1.
* [ ] Do **not** insert into the DB yet — this step is focused purely on transformation.
* [ ] Place scripts in the `/scripts` folder.
* [ ] Test transformation outputs locally.
* [ ] Submit the second PR.

---

## 🧩 Step 3: Populate Database

**PR Branch Name:** `layer-populating-db`

* [ ] Use the approved script to insert transformed data into the database.
* [ ] Create new tables or update existing ones based on schema.
* [ ] Establish keys, references, and relationships between the new table and `listings`/`neighborhoods`.
* [ ] Verify data is inserted and properly linked.
* [ ] (Optional) Set up scheduled GitHub Actions workflows for ongoing updates (for dynamic layers).
* [ ] Submit the third and final PR.


