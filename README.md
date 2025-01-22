# Named Entity Recognition (NER) System for Financial Reports

This project builds a Named Entity Recognition (NER) system to extract key financial entities from company reports. Starting with Apple Inc.’s 10-Q and 10-K reports, the system is designed to scale for reports from other electronics companies.

---

## Features
- Extracts entities like:
  - **Organizations** (e.g., Apple Inc.)
  - **Monetary Values** (e.g., $123 billion)
  - **Dates** (e.g., Fiscal Year 2023)
  - **Financial Events** (e.g., Stock Splits, IPOs)
- Preprocesses financial text by:
  - Cleaning and tokenizing the data.
  - Replacing abbreviations with full forms.
- Deploys an interactive web app using **Streamlit** for real-time entity extraction.

---

## Workflow
1. **Data Collection**:
   - Reports were sourced in **HTML format** and converted to **PDF** for easier text extraction.
   - Combined 10-Q and 10-K reports for Apple Inc. as the initial dataset.

2. **Preprocessing**:
   - Text was cleaned by removing punctuation and replacing abbreviations (e.g., "$" → "USD").
   - Stopwords were removed for better focus on meaningful entities.

3. **Model Development**:
   - Used SpaCy’s pre-trained `en_core_web_sm` model.
   - Fine-tuned the model with domain-specific financial text for better accuracy.

4. **Deployment**:
   - Built a **Streamlit app** to highlight extracted entities in user-provided text.

---

## Requirements
- Python 3.8+
- SpaCy
- Streamlit
- PyPDF2

Install dependencies:
```bash
pip install spacy streamlit PyPDF2
