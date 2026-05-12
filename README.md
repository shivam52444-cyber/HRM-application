

<h1>HireIQ — Agentic AI-Powered HRM System</h1>

<p>
HireIQ is an end-to-end intelligent hiring platform that automates resume screening,
candidate evaluation, and hiring workflows using LLMs, rule-based systems, and human-in-the-loop decisions.
</p>

<hr>

<h2>Problem Statement</h2>

<ul>
<li>Manual hiring process</li>
<li>Bias in screening</li>
<li>Time-consuming workflows</li>
<li>Difficult to scale</li>
</ul>

<p><strong>Solution:</strong></p>
<p>Resume → AI Evaluation → Human Decision → Feedback Loop</p>

<hr>

<h2>System Overview</h2>

<p>
Candidate Upload → Resume Parsing → AI Scoring → HR Dashboard → Manager Review → Final Decision
</p>

<hr>

<h2>Core Features</h2>

<h3>1. Resume Pipeline</h3>
<ul>
<li>Upload multiple resumes (PDF)</li>
<li>Extract text using PyMuPDF</li>
<li>Extract contact details (email, phone)</li>
<li>Rule-based name extraction</li>
</ul>

<h3>2. AI Resume Scoring Engine</h3>
<ul>
<li>Uses LLM (ChatGroq)</li>
<li>Evaluates skill match, experience, project alignment</li>
</ul>

<pre>
{
  "overall_score": 85,
  "strengths": [...],
  "gaps": [...],
  "recommendation": "shortlist"
}
</pre>

<h3>3. Intelligent Parsing Layer</h3>
<ul>
<li>Handles messy LLM outputs</li>
<li>Ensures valid JSON parsing</li>
<li>Prevents silent failures</li>
</ul>

<h3>4. HR Dashboard</h3>
<ul>
<li>Candidate ranking by score</li>
<li>Shortlist / Reject actions</li>
<li>Status tracking</li>
</ul>

<h3>5. Manager Review Layer</h3>
<ul>
<li>Final approval or rejection</li>
<li>Decision tracking</li>
</ul>

<h3>6. Email Automation System</h3>
<p>Built using SendGrid</p>
<ul>
<li>Application received email</li>
<li>Shortlist notification</li>
<li>Rejection notification</li>
<li>Manager decision updates</li>
</ul>

<hr>

<h2>Tech Stack</h2>

<table>
<tr><th>Layer</th><th>Technology</th></tr>
<tr><td>Frontend</td><td>Streamlit</td></tr>
<tr><td>Backend</td><td>Python</td></tr>
<tr><td>Database</td><td>SQLite</td></tr>
<tr><td>AI Engine</td><td>LangChain + LLM</td></tr>
<tr><td>PDF Parsing</td><td>PyMuPDF</td></tr>
<tr><td>Email</td><td>SendGrid</td></tr>
</table>

<hr>

<h2>System Design Philosophy</h2>

<p>Deterministic Logic + LLM Reasoning + Human Decisions</p>

<hr>

<h2>Strengths</h2>

<ul>
<li>Agentic multi-stage hiring workflow</li>
<li>Robust LLM integration</li>
<li>Reliable data pipeline</li>
<li>Automated communication system</li>
<li>Debuggable architecture</li>
</ul>

<hr>

<h2>Limitations</h2>

<ul>
<li>SQLite is not scalable</li>
<li>Streamlit is not production frontend</li>
<li>LLM-only scoring (no ML model)</li>
<li>No async processing</li>
<li>No event-driven system</li>
</ul>

<hr>

<h2>Future Improvements</h2>

<ul>
<li>PostgreSQL database</li>
<li>FastAPI backend</li>
<li>React frontend</li>
<li>Hybrid ML + embedding scoring</li>
<li>Feedback learning system</li>
<li>Personalized test links</li>
<li>Real-time integrity monitoring</li>
<li>Event-driven architecture</li>
<li>Full agentic orchestration</li>
</ul>

<hr>

<h2>How to Run,before running set a llm and sendgridapi key</h2>

<pre>
pip install -r requirements.txt
python initdb.py
streamlit run main_app.py
</pre>

<hr>

<h2>Key Learning Outcomes</h2>

<ul>
<li>End-to-end system design</li>
<li>Production-level LLM integration</li>
<li>Data pipeline debugging</li>
<li>Human-AI collaboration</li>
<li>Real-world hiring workflow</li>
</ul>

<hr>

<h2>Project Vision</h2>

<p>
Build a foundation for autonomous AI-driven hiring systems.
</p>

<hr>

<h2>Author</h2>

<p>
Shivam<br>
Data Scientist and AI System Builder
</p>

<hr>

<h2>Final Note</h2>

<p>Thinking beyond models — building systems.</p>
