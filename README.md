# HRM-application
A end to end hrm application , that can be useful  from jd upload to candidate shortlisting and sending automatic email with hr tracking and feedback loop


HireIQ — Agentic AI-Powered HRM System
An end-to-end intelligent hiring platform that automates resume screening, candidate evaluation, and hiring workflows using LLMs, rule-based systems, and human-in-the-loop decisions.

Problem Statement
Modern hiring is:


Manual


Biased


Time-consuming


Hard to scale


HireIQ addresses this by building an agentic hiring system:
Resume → AI Evaluation → Human Decision → Feedback Loop

System Overview
Candidate Upload → Resume Parsing → AI Scoring → HR Dashboard → Manager Review → Final Decision

Core Features
1. Resume Pipeline


Upload multiple resumes (PDF)


Extract structured text using PyMuPDF


Extract contact details (email, phone)


Rule-based name extraction to avoid hallucination



2. AI Resume Scoring Engine


Uses LLM (ChatGroq)


Evaluates:


Skill match


Experience relevance


Project alignment




Example output:
{  "overall_score": 85,  "strengths": [...],  "gaps": [...],  "recommendation": "shortlist"}

3. Intelligent Parsing Layer


Robust JSON extraction from LLM output


Handles malformed responses


Prevents silent failures



4. HR Dashboard


Displays candidates sorted by score


Categorization:


Strong Match


Moderate Match


Weak Match




Actions:


Shortlist


Reject (with reason)





5. Manager Review Layer


Reviews shortlisted candidates


Final approval or rejection


Triggers candidate communication



6. Leader Dashboard


Hiring analytics


Shortlist vs reject trends


Quality insights



7. Email Automation System
Uses SendGrid for email delivery.
Emails sent:


Application received (immediately after upload)


Shortlisted notification


Rejection notification


Manager decision updates



Tech Stack
LayerTechnologyFrontendStreamlitBackendPythonDatabaseSQLiteAI EngineLangChain + LLMPDF ParsingPyMuPDFEmailSendGrid

System Design Philosophy
The system follows a hybrid approach:
Deterministic Logic + LLM Reasoning + Human Decisions

Strengths
1. Agentic Workflow Design


Multi-stage hiring pipeline


Reflects real-world enterprise hiring process



2. Robust LLM Integration


Handles JSON parsing issues


Reduces hallucination risks


Enforces structured output



3. Reliable Data Pipeline


Prevents stale records


Updates existing candidates correctly


Deterministic name extraction



4. Product-Oriented Design


Automated candidate communication


Role-based dashboards


Human-in-the-loop decisions



5. Debuggable System


Logging at every stage


Transparent processing pipeline


Easy error tracing



Limitations


Uses SQLite (not suitable for scale)


Streamlit UI is not production-grade


LLM-only scoring (no ML calibration yet)


No asynchronous processing


No event-driven architecture



Future Improvements
1. Database Upgrade


Replace SQLite with PostgreSQL


Add indexing and scalability



2. Backend API Layer


Build FastAPI services


Separate frontend and backend


Enable microservices architecture



3. Frontend Upgrade


Replace Streamlit with React


Improve performance and UX


Enable real-time updates



4. Advanced Scoring System
Move from LLM-based scoring to:
Hybrid = Embeddings + Machine Learning Model + LLM Explanation

5. Feedback Learning System


Use HR decisions as training labels


Build predictive hiring model:
P(shortlist | resume)



6. Personalized Candidate Test Links


Generate secure links for assessments


Track candidate attempts


Enable structured evaluation



7. Real-Time Integrity Monitoring


Detect tab switching


Track typing behavior


Monitor idle time


Future model:
P(cheating | behavioral signals)

8. Event-Driven Architecture


Introduce message queues (Kafka or Redis)


Enable asynchronous agent workflows



9. Full Agentic System


Manager agent for planning


Worker agent for scoring


Evaluation agent for feedback loop



How to Run
pip install -r requirements.txtpython initdb.pystreamlit run main_app.py

Key Learning Outcomes


End-to-end system design


Production-level LLM integration


Data pipeline debugging


Human-AI collaboration systems


Real-world hiring workflow implementation



Project Vision
This project serves as a foundation for building autonomous AI-driven hiring systems.

Author
Shivam
Data Scientist and AI System Builder

Final Note
Thinking beyond models — building systems.
