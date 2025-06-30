# VulnShop
🛒 Project Name: VulnShop (Vulnerable Online Shop)
🎯 Purpose
A visually modern e-commerce platform intentionally built with security flaws (especially SQL Injection, XSS, weak authentication) to allow learners and professionals to:

Practice attack simulations

Conduct defacement exercises

Analyze poor security practices

Understand and implement remediation techniques

🧱 Core Features & Technologies
💻 Frontend
Framework: React (for a modern UI)

Design: TailwindCSS + Heroicons

Pages: Home, Product List, Product Details, Cart, Login, Checkout

⚙️ Backend
Framework: Node.js + Express

Database: MySQL (intentionally misconfigured)

Security Weaknesses:

No input validation

SQL queries directly interpolate user input

Session tokens stored in predictable cookies

Weak password hashing (e.g., MD5)

📦 Functionality
Browse and search products (prone to SQLi)

Add to cart & checkout (unsecured transactions)

Admin login panel (susceptible to brute-force and SQLi)

Simulated payment page (exploitable via XSS)

Site theme easy to deface via database or direct HTML manipulation

🔓 Intentional Vulnerabilities
Area	Vulnerability	Simulation Purpose
Auth	SQLi in login form	Bypass login, escalate privileges
Product URL	SQL Injection	Dump database contents
Cart	CSRF + IDOR	Manipulate cart of other users
Admin Panel	XSS + SQLi	Stored XSS defacement + admin takeover
Checkout	Insecure direct object references (IDOR)	View/modify order IDs
Sessions	Weak session management	Session hijacking demonstration

🛠️ Deployment Options
Docker container for isolated testing

Kali Linux VM with Apache/MySQL preconfigured

AWS/GCP with reverse proxy + logging for training scenarios

🧪 Tools for Exploitation
You can test this platform using:

sqlmap for SQL injection

Burp Suite for intercepting/modifying requests

OWASP ZAP for automated vulnerability scanning

BeEF for XSS exploitation

Metasploit to simulate payload delivery

🧯 Logging & Recovery
Webhook/Discord alert simulation for defacement detection

Reset scripts (reset_db.sh) to reinitialize the platform for repeat labs


