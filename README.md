# INSAAF

**An AI-based Interactive Chatbot for the Department of Justice’s Website**

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Problem Statement](#problem-statement)
- [Solution Approach](#solution-approach)
  - [Architecture](#architecture)
  - [Technology Stack](#technology-stack)
- [Installation & Setup](#installation--setup)
- [Usage](#usage)
- [Security & Compliance](#security--compliance)
- [Challenges & Mitigations](#challenges--mitigations)
- [Impact & Benefits](#impact--benefits)
- [Future Work](#future-work)
- [References](#references)

## Overview

INSAAF is an AI-powered chatbot platform designed to simplify interaction with judicial services on the Department of Justice’s website. By providing a conversational interface, INSAAF enables users to:

- Check case status
- File e‑petition and documents
- Access live streaming of court proceedings
- Retrieve legal information and statutes
- And more interactive judicial services

## Features

- **Natural Language Interaction**: Understand and respond to user queries in conversational English.
- **Case Status Tracker**: Real-time updates on pending and closed cases.
- **eFiling Integration**: Submit petitions and related documents through the chatbot.
- **Live Streaming Access**: Seamlessly link to court proceeding streams.
- **Legal Knowledge Base**: "Know Your Law" module powered by NLP to fetch relevant statutes and precedents.
- **Multi-Channel Support**: Accessible via web chat interface, mobile browsers, and potentially messaging apps.

## Problem Statement

The Department of Justice’s website hosts a wide range of services that can be difficult to navigate for non‑technical or first‑time users. INSAAF addresses:

- **Complex Navigation**: Simplifies multi‑step processes into conversational flows.
- **Manual Bottlenecks**: Automates repetitive queries and form filling.
- **Accessibility Gaps**: Provides a unified, user-friendly interface for underserved communities.

## Solution Approach

### Architecture

```
User Browser ↔️ Frontend (HTML/CSS/JS + Streamlit) ↔️ Flask Backend ↔️ LLaMA API
                                          ↳ TensorFlow & spaCy NLP
                                          ↳ Middleware for Legacy API Integration
                                          ↳ AES Encryption & SSL/TLS
```

### Technology Stack

- **Frontend**: HTML5, CSS3, JavaScript, Streamlit
- **Backend**: Python, Flask
- **AI / NLP**: LLaMA model (via API), TensorFlow, spaCy
- **Security**: AES Encryption, SSL/TLS, Multi-Factor Authentication
- **Hosting**: HostGator India Hatchling Plan
- **Middleware**: Custom connectors for legacy court APIs

## Installation & Setup

1. **Clone repository**
   ```bash
   git clone https://github.com/your-org/insAAF.git
   cd insAAF
   ```
2. **Backend Setup**
   ```bash
   cd backend
   python3 -m venv venv
   source venv/bin/activate
   pip install -r requirements.txt
   ```
3. **Frontend Setup**
   ```bash
   cd ../frontend
   pip install -r requirements.txt  # Streamlit-based UI
   ```
4. **Environment Variables**
   ```bash
   export FLASK_APP=app.py
   export LLaMA_API_KEY=<your_api_key>
   export SECRET_KEY=<your_secret>
   ```
5. **Run Services**
   ```bash
   # Start Flask API
   flask run --host=0.0.0.0 --port=5000

   # Start Streamlit UI
   streamlit run ui.py --server.port 8501
   ```

## Usage

- Open your browser and navigate to `http://localhost:8501` for the chatbot UI.
- Type your legal query (e.g., "What is the status of Case No. 12345?").
- Follow prompts to upload documents or stream live court sessions.

## Demo Video

A project walkthrough is available in the demo video. You can watch it here:

[▶️ Watch the Demo Video](https://youtu.be/8IjmfIf2Vc8)

## Security & Compliance

- **Data Encryption**: All communication is secured with AES-256 encryption and SSL/TLS.
- **Authentication**: Multi-Factor Authentication (MFA) protects sensitive actions.
- **Privacy**: Complies with GDPR and national data protection guidelines.

## Challenges & Mitigations

- **Legacy System Integration**: Used middleware adapters to connect with older court APIs.
- **Data Security**: Implemented AES and SSL/TLS; regularly audited logs.
- **Scalability**: Deployed on scalable cloud hosting; auto-scaling enabled.

## Impact & Benefits

- **Social**: Improves access to justice for remote and underserved users.
- **Economic**: Reduces manual workload for court staff, cutting operational costs.
- **Environmental**: Minimizes paper usage via digital document handling.

## Future Work

- Expand language support beyond English.
- Integrate voice interface for accessibility.
- Develop mobile app wrappers for Android and iOS.
- Add deeper analytics on user interactions for service improvement.

## References

- Department of Justice: [https://doj.gov.in](https://doj.gov.in)
- Ministry of Law and Justice: [https://lawmin.gov.in](https://lawmin.gov.in)
- eCourts Services: [https://ecourts.gov.in](https://ecourts.gov.in)

