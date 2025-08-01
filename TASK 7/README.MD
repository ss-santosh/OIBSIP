🔒 Vulnerability Scanning with Nikto

📝 Task Overview
This task involves performing a vulnerability scan using **Nikto**, a widely used open-source web server scanner. The objective is to identify known security issues and misconfigurations on a target web server.

---

🛠️ Tool Used
"Nikto"
- Nikto is a command-line-based web vulnerability scanner that checks for:
  - Dangerous files/CGIs
  - Outdated server software
  - Insecure server configurations
  - Missing security headers
- Website: [https://cirt.net/Nikto2](https://cirt.net/Nikto2)

---

🎯 Target Information
- **Target URL**: `http://testphp.vulnweb.com`
- **Target IP**: `44.228.249.3`
- **Port Scanned**: 80 (HTTP)

---

🚀 Command Used
nikto -h http://testphp.vulnweb.com -o nikto_scan_results.txt

🔍 Command Explanation
Option	Description
-h	Specifies the host to scan
-o	Outputs the scan results to a file (nikto_scan_results.txt)

📄 Scan Results Summary
Nikto found 6 potential security issues. Here are the highlights:




1. ⚠️ PHP Version Disclosure
Details: X-Powered-By: PHP/5.6.40...

Risk: Reveals backend technology version.

Impact: Attackers can search for known vulnerabilities in that version.

Mitigation: Disable X-Powered-By header via server configuration.

2. ❌ Missing Security Headers
Header	Issue	Risk	Mitigation
X-Frame-Options	Not set	Clickjacking	Add header to prevent iframe embedding
X-Content-Type-Options	Not set	MIME sniffing	Add header with nosniff value

3. 🧩 Policy Files Detected
Files:

/clientaccesspolicy.xml

/crossdomain.xml

Risk: If misconfigured, these files allow unsafe cross-domain access.

Reference:

Crossdomain.xml Security Risk

⚠️ Error Message
vbnet
Copy
Edit
ERROR: Error limit (20) reached for host, skipping remaining tests.
Reason: Nikto stops scanning after too many failed requests or timeouts.

Impact: Not all vulnerabilities may have been detected.

✅ Recommendations
Issue	Fix
PHP version disclosure	Hide version info in HTTP headers
Missing security headers	Add X-Frame-Options, X-Content-Type-Options, Content-Security-Policy
Policy files	Restrict access in crossdomain.xml and clientaccesspolicy.xml
Unpatched server	Keep server software updated and monitor for CVEs

📌 Conclusion
Nikto revealed multiple areas where the target server could be improved:

Avoid disclosing server details.

Apply recommended HTTP security headers.

Configure access policy files securely.

These basic security measures help protect against a wide range of automated and manual attacks.

📁 Deliverables
nikto_scan_results.txt – Raw scan output

README.md – This documentation

✍️ Author
Santosh
Cybersecurity Intern | 2025
