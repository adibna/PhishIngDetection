<div align="center">
![Image](https://github.com/user-attachments/assets/1cbd1c99-ce13-4e32-88bb-c7da40c3a003)
  
<h1>PhishIngDetection</h1>
<p><strong>A Proactive Threat Hunting Web Application</strong></p>

<blockquote>
An intelligent web application designed to proactively discover and assess the risk of phishing, typosquatting, and brand impersonation domains.
</blockquote>

<p>
<img src="https://img.shields.io/badge/Python-3.12+-blue.svg?style=for-the-badge&logo=python" alt="Python">
<img src="https://img.shields.io/badge/Flask-3.0+-black.svg?style=for-the-badge&logo=flask" alt="Flask">
<img src="https://img.shields.io/badge/Bootstrap-5.3-purple.svg?style=for-the-badge&logo=bootstrap" alt="Bootstrap">
<img src="https://img.shields.io/badge/Status-In%20Development-yellow.svg?style=for-the-badge" alt="Status">
</p>
</div>

✨ Key Features
🔐 Secure User Authentication: Full registration and login system with email confirmation and optional Two-Factor Authentication (2FA).

⚙️ Dynamic Domain Permutation Engine: Generates dozens of phishing variations from a target domain using common attack techniques.

📊 Multi-Layered Threat Analysis: Performs automated checks for IP reputation, MX record configuration, and live page content.

🖥️ Live Page Content Analysis: Securely fetches active suspect domains to detect password forms and brand impersonation in page titles.

💯 Dynamic Risk Scoring System: A unique algorithm calculates a risk score (0-100) by weighing multiple threat vectors for an at-a-glance threat assessment.

🎨 Interactive Web Interface: A clean, responsive frontend built with Bootstrap, featuring a custom theme, dynamic results table, and user-friendly components.

⚙️ How It Works
The application follows a two-phase analysis pipeline to deliver fast and comprehensive results:

➡️ Input & Generation: A user enters a target domain (e.g., company.com). The backend engine immediately generates a list of potential phishing variations (companny.com, company-login.com, etc.).

filtering Phase 1: Rapid DNS Filtering: The tool performs a high-speed DNS lookup on all variations to quickly filter out unregistered domains, identifying only those that are live on the internet.

🔬 Phase 2: In-Depth Analysis: For each live domain, the tool launches a series of detailed background checks:

IP Reputation: Queries the AbuseIPDB API to check the server's IP address against a database of known bad actors.

Email Configuration (MX Scan): Checks for DNS MX records to determine if the domain is configured to handle email, a strong indicator of intent for BEC attacks.

Live Page Analysis: Securely fetches the website's HTML to analyze its content for the presence of password forms (<input type="password">) and brand impersonation in the page title.

📈 Scoring & Display: The collected data is fed into the Risk Score algorithm. The final results are sorted by the highest risk and displayed in a clear, color-coded table.

💯 The Risk Score Explained
The Risk Score is the core differentiator of the PhishIngDetection tool. It is a heuristic score from 0 to 100, calculated by combining multiple weighted factors to provide a more intelligent and actionable assessment.

The score is calculated as a sum of the following points:

🌐 IP Reputation (Up to 50 points): Half of the IP's abuse percentage from AbuseIPDB is added to the score. (Example: An IP with a 90% abuse score adds 45 points.)

🔑 Live Password Form Detected (+40 points): This is a critical indicator and is weighted heavily, as it's direct evidence of a credential harvesting trap.

👑 Brand Impersonation in Title (+25 points): Shows a clear intent to deceive users by using the original brand's name in the page title.

📧 Email (MX) Records Configured (+20 points): Indicates the domain is prepared for email-based fraud.

🔡 Suspicious Keywords in Domain (+10 points): Words like login, secure, or verify in the domain name increase the risk.

## Risk Score Categorization:

🟢 0-39 (Low Risk): Unlikely to be a direct threat. May be a parked or unrelated domain.

🟡 40-69 (Medium Risk): Exhibits several suspicious characteristics. Caution is strongly advised.

🔴 70-100 (High Risk): Shows multiple, strong indicators of being a phishing or malicious site. Avoid this domain.

<img width="1885" height="944" alt="Image" src="https://github.com/user-attachments/assets/6beb58b3-e922-45e9-badb-d3d6dbddc2c8" />
