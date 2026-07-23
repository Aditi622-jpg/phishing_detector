Phisheild AI Detector
A full‑stack web application built with Flask that detects phishing emails using rule‑based checks, machine learning models, and email header analysis. It provides both a web interface and a REST API for flexible integration.

🚀 Features
User Authentication

Secure login with Gmail validation

OTP verification for added security

Session expiry and login attempt limits

Phishing Detection

Rule‑based analysis: keyword checks, suspicious links, sender validation

Machine learning analysis: trained model + vectorizer for adaptive detection

Risk scoring: confidence levels and risk classification (High/Low)

Email Header Analysis

Upload raw .eml files for forensic inspection

Extracts From, To, Subject, Return‑Path, Message‑ID, Received hops

Flags suspicious patterns (Return‑Path mismatch, too many hops, invalid sender format)

Blacklist System

Automatically blocks repeat offenders

Prevents duplicate analysis

Manage blacklist entries via dashboard

Dashboard & Reports

View statistics for rule‑based and ML detections

Recent email analysis history

Export phishing detection reports as PDF

REST API

/api/analyze endpoint for programmatic access

Accepts JSON input (email_text, sender, links, attachments)

Returns JSON verdicts (verdict_rule, verdict_ml, confidence, risk_score)

🖥️ User Interface
Upload Page

Two analysis options:

Paste email text → Content analysis

Upload .eml file → Header analysis

Results Pages

result.html: verdicts, confidence, gauges, risk score

results_headers.html: header breakdown + suspicious findings

Dashboard

Stats, recent emails, blacklist management

Reports

Generate PDF summaries of detection activity

⚙️ Tech Stack
Backend: Flask, SQLite, Joblib (ML model + vectorizer)

Frontend: HTML, CSS, Bootstrap, Chart.js

Security: OTP verification, session expiry, login attempt limits

Reporting: ReportLab for PDF generation
