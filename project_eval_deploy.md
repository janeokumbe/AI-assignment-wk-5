# ✅ Member 3: Evaluation, Deployment & Monitoring (20 Points)

---

## 🔹 Part 1: Short Answer (8 points)

### 4. Evaluation & Deployment

**a. Select 2 evaluation metrics and explain why they're relevant:**

1. **Recall** – In hospital readmission prediction, it's important to identify as many true positive cases (patients likely to be readmitted) as possible. Missing these could mean a patient is discharged without proper follow-up, increasing health risks.

2. **F1-Score** – Balances precision and recall. In healthcare, both false positives (unnecessary concern/resources) and false negatives (missed readmission risk) are costly, so a balanced metric like F1-score is suitable.

---

**b. Define concept drift and describe monitoring post-deployment:**

- **Concept Drift** refers to a change in the statistical patterns of the target variable over time. In our case, patient behavior or treatment protocols might change, making the model less accurate.

- **Monitoring** should involve:
  - Tracking model performance metrics regularly (e.g., weekly F1-score, recall)
  - Setting up alerts for significant drops
  - Retraining the model periodically with fresh data

---

**c. Describe 1 technical challenge (e.g., scalability):**

- **Scalability**: As hospital data grows (from new patient records, more departments, etc.), the model must scale to handle increased load. This includes managing real-time prediction requests and retraining pipelines, which may strain computational resources.

---

## 🔹 Part 2: Case Study (10 points)

### Deployment

**a. Outline integration into the hospital’s system:**

1. The model will be deployed as a **REST API** using Flask or FastAPI.
2. It will integrate with the **hospital’s EHR system** via secure APIs.
3. Predictions will be triggered automatically after discharge data is recorded.
4. A **dashboard** will display predicted readmission risk to clinicians.
5. The system will log predictions for auditing and retraining.

---

**b. Ensure compliance with healthcare regulations (e.g., HIPAA):**

- Use **encrypted data transmission (HTTPS)** to protect PHI.
- Ensure data storage is on **HIPAA-compliant servers** (e.g., AWS HealthLake, Google Cloud for Healthcare).
- Apply **role-based access controls (RBAC)** to restrict data access.
- Log and audit every access to patient data to maintain compliance and traceability.

---

## 🔹 Part 4: Support (2 points)

- Support the **workflow diagram** by helping define how model monitoring connects to feedback loops.
- Highlight the **monitoring stage** as continuous, with options for alerting, retraining, and reporting to the data science and clinical teams.
