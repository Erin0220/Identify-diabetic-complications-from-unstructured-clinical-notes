# Identifying Patients with Diabetic Complications

👉 **Rendered Project Report (HTML):**  
https://erin0220.github.io/Identify-diabetic-complications-from-unstructured-clinical-notes/

---

## 📌 Project Overview
This project applies clinical text processing and natural language processing (NLP) techniques to identify diabetic complications from unstructured clinical notes.

Using a corpus of notes from patients with diabetes, the goal is to determine:
1. Whether a clinical note documents the presence of diabetic complications, and  
2. Which type of complication is described.

The project focuses on three common diabetic complications:
- **Neuropathy**
- **Nephropathy**
- **Retinopathy**

A keyword window–based approach is used to capture local clinical context, while exclusion rules are applied to remove negated mentions and references to family history.

---

## 🧠 Data
- **Dataset:** `mimic3_demo`
- **Tables used:**
  - `course4_data.diabetes_notes`
  - `course4_data.diabetes_goldstandard`

These tables contain de-identified clinical notes and a gold-standard annotation of diabetic complications.

---

## ⚙️ Methods
- Keyword window technique (±10 words around diabetes-related terms)
- Regular expression matching for complication identification
- Rule-based exclusion of:
  - Negated mentions
  - Family history references
- Note-level aggregation of predictions
- Performance evaluation using confusion matrices

---

## 📊 Evaluation
Predictions were evaluated against the gold-standard dataset at the note level.

Performance summary:
- **Accuracy:** 0.9362  
- **Sensitivity:** 0.8148  
- **Specificity:** 0.9649  

The results demonstrate a good balance between sensitivity and specificity, with high overall accuracy.

---

## 🛠 Tools & Technologies
- R
- R Markdown
- tidyverse
- caret
- BigQuery
- Regular expressions (regex)

---

## 📚 Course Context
This project was completed as part of a clinical data science / health informatics course focused on:
- Computational phenotyping
- Clinical NLP
- Feature engineering using unstructured text
- Model evaluation and interpretation

---

## 📝 Notes
The emphasis of this assignment is on methodological reasoning and transparency rather than advanced modeling techniques.  
Future work could explore section-based parsing or machine learning–based approaches to improve robustness.

---
