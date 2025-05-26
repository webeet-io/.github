---
name: Data Science Task
about: Template for implementing data science algorithms such as recommendations, clustering, or analytics
title: "[Data Science] #placeholder model for #placeholder use case"
labels: data-science, modeling, pipeline
assignees: anastasia
---

### 1. Define the Goal
- [ ] Clearly state the objective of the task (e.g. recommendation, segmentation, scoring, etc.)
- [ ] Identify the target table or dataset from which the model will draw inputs.
- [ ] Specify the desired output (e.g. list of recommendations, cluster assignments, scores, etc.)

---

### 2. Data Preparation
- [ ] Explore and understand the available data relevant to the task.
- [ ] Clean and preprocess the data as needed.
- [ ] Document any assumptions or filters applied during data prep.

---

### 3. Modeling
- [ ] Select and justify the algorithm or approach (e.g. collaborative filtering, k-means, embeddings).
- [ ] Train and validate the model using appropriate metrics.
- [ ] Include code and artifacts (e.g. notebooks, scripts) under version control.

---

### 4. Review Plan with Senior
- [ ] Present the proposed approach, metrics, and initial results to **Anastasia** (or assigned reviewer).
- [ ] Incorporate feedback and finalize the modeling process.

---

### 5. Integration & Inference
- [ ] Build an inference pipeline to apply the model at scale (batch or real-time).
- [ ] Use **GitHub Actions** + Python/SQL as needed to operationalize the pipeline.

---

### 6. Insert Results into Database
- [ ] Define the schema for storing model outputs (e.g. recommendations, clusters).
- [ ] Insert results into the database, linking to existing entities (e.g. users, listings, neighborhoods).
- [ ] (Optional) Schedule recurring updates if model needs to run periodically.
