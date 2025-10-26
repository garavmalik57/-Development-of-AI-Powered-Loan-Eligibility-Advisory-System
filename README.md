### LoanAdvisor

An end-to-end Flask web app that helps users assess basic loan eligibility, upload documents, verify Aadhaar details via OCR, and download a summary PDF report. Includes a chatbot-style data collection flow and a separate ML training script for a loan-status classifier.

---

### Features
- **Web UI**: Pages for home, login, signup, dashboard, result, and a chatbot interface.
- **Chatbot flow**: Collects user inputs such as employment, income, Aadhaar/PAN, loan type, amount, and tenure (`/chatbot`).
- **Document uploads**: Accepts Aadhaar, salary slips, and bank statements (`/upload`).
- **Aadhaar OCR**: Extracts and validates a 12-digit Aadhaar number from the uploaded Aadhaar image.
- **Eligibility summary**: Generates a basic rule-based eligibility assessment and recommendations.
- **PDF export**: Creates a summary report PDF for download (`/generate_pdf`).
- **ML training script**: `train_model.py` builds an XGBoost classifier on a provided dataset and saves a model artifact.

---

### Tech Stack
- Python 3.7+
- Flask
- OCR: Tesseract via `pytesseract` and `Pillow`
- ML: Scikit-learn, XGBoost (training script)
- PDF: reportlab (used via `reportlab.pdfgen.canvas` in code)

---

### Project Structure
```
loan-advisor/
  app.py                  # Flask app entrypoint
  chatbot_route.py        # (If used) extra routing logic for chatbot (not required to run app.py)
  train_model.py          # ML training pipeline
  models/
    loan_model.pkl        # Example pre-trained model (not used directly by app.py)
  utils/
    ocr_utils.py          # OCR helpers (Aadhaar extraction)
    pdf_generator.py      # (If used) PDF helper utilities
  templates/              # Flask Jinja templates
    home.html
    login.html
    signup.html
    dashboard.html
    chatbot.html
    result.html
  static/                 # Static assets (CSS/JS/images)
    style.css
    chatbot.js
    logo.png
  uploads/                # Runtime uploads (created if missing)
    aadhar/
    salary_slips/
    bank/
  requirements.txt
  README.md
```

---
Demo & Live Website

🎥 Demo Video: https://drive.google.com/file/d/1HUjIm4oGDf9BhR7Thco1qSdC4UAkxo6U/view?usp=drive_link

🌐 Hosted Website: https://ai-credit-underwriting-system.onrender.com
