# Security Assessment – itsecgames.com (bWAPP)

## 📌 Overview
This repository contains my submission for the **Security Officer Trainee Assignment** at **AccuKnox**.  
The target assessed was `http://www.itsecgames.com/`, a deliberately vulnerable web application (bWAPP).  

The assessment was **non-exploitative** and focused on reconnaissance, scanning, and configuration checks.

---

## 📂 Repository Contents
- **report/**  
  - `Security_Assessment_Report.pdf` → Final compiled report  
  - `raw_outputs/` → Nmap, Nikto, Gobuster logs, ZAP report, screenshots  

- **slides/**  
  - `Assessment_Presentation.pdf` → Slide deck used for demo video  

- **video/**  
  - `demo_link.txt` → Link to recorded demonstration video  

- **docs/**  
  - `methodology.md` → Commands and workflow notes  

---

## 🛠️ Methodology (Brief)
1. **Passive Reconnaissance** – Whois, Dig, WhatWeb, curl headers, robots/sitemap.  
2. **Active Recon (Nmap)** – Service/version detection, OS fingerprinting, vuln scripts.  
3. **Automated Scanning** – Nikto + OWASP ZAP.  
4. **Directory Discovery** – Gobuster, manual checks, robots.txt.  
5. **Manual Validation** – SSH banner, SSL cert check, input reflection.  
6. **Prioritization** – Risks categorized High/Medium/Low with recommendations.

---

## 🚩 Key Findings
- **High:** Outdated OpenSSH banner (6.7p1), exposed backup reference.  
- **Medium:** Missing security headers, reflected input.  
- **Low:** ETag information disclosure.  
- **Info:** Demo application visible (bWAPP).  

---

## ✅ Recommendations
- Upgrade and harden SSH.  
- Remove backup/archive files from webroot.  
- Add missing security headers (XFO, CSP, etc.).  
- Sanitize input/output.  
- Hide server tokens and disable ETag.  
- Keep bWAPP isolated for lab use only.  

---

## 🎥 Demo Video
The demonstration video is available here:  
👉 [Google Drive / YouTube link](https://your-video-link.com)

---

## 📌 Note
This assessment was performed strictly within the scope provided for the assignment.  
No exploitative actions were taken. Outputs are provided for **educational and assignment purposes only**.
