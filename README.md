LoanAdvisor

An end-to-end Flask web app that helps users assess basic loan eligibility, upload documents, verify Aadhaar details via OCR, and download a summary PDF report.

Features

Web UI: Home, login, signup, dashboard, result, and chatbot interface.

Chatbot: Collects user details like employment, income, Aadhaar/PAN, loan type, amount, and tenure.

Document Upload: Supports Aadhaar, salary slips, and bank statements.

Aadhaar OCR: Extracts and validates Aadhaar number from the uploaded image.

Eligibility Summary: Rule-based loan eligibility assessment.

PDF Export: Generates a downloadable summary PDF report.

ML Training: XGBoost classifier model for loan status prediction (training script provided).

Tech Stack

Python 3.7+

Flask

Tesseract OCR (via pytesseract)

ML: Scikit-learn, XGBoost

PDF: reportlab
