# Apache Vulnerable Server Lab  
**Vulnerability Identification + Exploitation + Remediation (Nessus Essentials + Apache2 on Ubuntu VM)**  
_A hands-on cybersecurity lab demonstrating vulnerability creation, scanning, exploitation validation, and remediation._

---

## 📌 Overview

This project simulates a **real-world vulnerability management workflow**:

1. Install and configure an Apache2 web server on Ubuntu.
2. **Intentionally introduce a known vulnerability** (Apache Directory Listing).
3. Run a full vulnerability scan using **Nessus Essentials**.
4. Analyze findings.
5. **Fix the vulnerability**.
6. Re-run a scan to confirm successful remediation.
7. Document everything, including screenshots, commands, and lessons learned.


---
## 📚 Lessons Learned

Working through this Apache Vulnerable Server Lab taught me several key concepts relevant to real-world cybersecurity operations:

### 🔐 1. Misconfigurations Are a Major Attack Vector  
The simple addition of `Indexes` to the Apache `Options` directive instantly created a security weakness.  
This reinforced that **small configuration mistakes can lead to high-impact vulnerabilities**, and why configuration audits are a crucial part of system hardening.

### 🕵️ 2. Vulnerability Scanning Is Only the Beginning  
Nessus Essentials provided detailed findings, but understanding the root cause, severity, and exploitability required human analysis.  
This highlighted the difference between:
- **Automated detection**  
- **Manual validation**  
- **Informed remediation**  

A tool can identify issues, but the analyst must interpret and act on them.

### 🛠️ 3. Apache Configuration Management  
I learned how Apache uses a layered configuration structure:
- `/etc/apache2/apache2.conf`
- `/etc/apache2/sites-enabled/`
- `/var/www/html/`

And how directives like `Options`, `FollowSymLinks`, and `AllowOverride` impact web server behavior.

This deepened my comfort with Linux-based web server administration.

### 🔄 4. Importance of the Vulnerability Management Lifecycle  
This project required following the full VM workflow:
1. **Identify** vulnerabilities  
2. **Analyze** severity and impact  
3. **Exploit/Validate** (Directory Listing in this case)  
4. **Remediate** the root cause  
5. **Rescan** to ensure the fix worked  

This mirrors what real SOC, blue team, and vulnerability management teams do every day.

### ⚙️ 5. Logs and Errors Provide Valuable Insight  
Interacting with Apache responses like `403 Forbidden` and reviewing Nessus plugin output taught me how to:
- Confirm vulnerability presence  
- Validate that a fix actually took effect  
- Troubleshoot unexpected behavior  

Understanding **HTTP status codes**, request behavior, and server responses is foundational for any analyst.

### 🖥️ 6. Using VMs and Tools in a Controlled Lab Environment  
Running Ubuntu and Apache inside a Parallels VM provided a safe playground to:
- Experiment with configurations  
- Break things intentionally  
- Fix issues without impacting production systems  

This reinforced the value of **hands-on, isolated labs** for skill development.



Helped me practice professional documentation standards expected in:
- SOC analyst reports  
- Security team knowledge bases  
- Compliance evidence packages  

### 🏁 Final Takeaway  
This lab proved that even a simple web server can present multiple entry points for attackers if misconfigured.  
More importantly, it demonstrated the mindset and process required to:
- Identify risk  
- Understand impact  
- Apply a fix  
- Validate security posture  




