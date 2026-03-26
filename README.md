# Phishing Email Detection & Awareness System

**Task:** FUTURE_CS_02  
**Track:** Cyber Security  
**Date:** March 2026

---

## Project Overview

This project focuses on identifying and analyzing phishing email threats. Three email samples were examined to detect common phishing indicators such as spoofed sender domains, malicious links, urgency tactics, and grammatical inconsistencies. Each email was classified based on risk level, and actionable prevention guidelines were developed for both individuals and organizations.

---

## Email Analysis Findings

### Sample 1: PayPal Account Alert
| Attribute | Finding |
|-----------|---------|
| **Classification** | 🔴 Phishing (High Risk) |
| **Sender Domain** | `paypal-verify.com` (fraudulent - legitimate is `paypal.com`) |
| **Link Destination** | `http://paypal-security-verify.com` (fake login page) |
| **Urgency Tactic** | "24 hours," "permanent suspension" |
| **Red Flags** | Generic greeting, poor grammar, threat of account closure |

**Why It's Dangerous:** The email creates panic by threatening immediate account closure. Users who click the link are directed to a fake PayPal login page designed to steal credentials.

---

### Sample 2: Amazon Order Issue
| Attribute | Finding |
|-----------|---------|
| **Classification** | 🟡 Suspicious (Medium Risk) |
| **Sender Domain** | `amazon-customer-service.net` (not official - legitimate is `amazon.com`) |
| **Link Destination** | `https://amazon-payment-verify.com` (impersonation domain) |
| **Urgency Tactic** | "order cannot be processed" |
| **Red Flags** | Domain mismatch, request for billing information |

**Why It's Concerning:** The email mimics Amazon's branding but uses a fake domain. It creates urgency about a fake order issue to trick users into entering payment details.

---

### Sample 3: Genuine Amazon Confirmation
| Attribute | Finding |
|-----------|---------|
| **Classification** | 🟢 Safe (Low Risk) |
| **Sender Domain** | `noreply@amazon.com` (legitimate) |
| **Link Destination** | `amazon.com/orders/...` (official domain) |
| **Personalization** | Includes recipient name and actual order details |
| **Red Flags** | None identified |

**Why It's Safe:** The email comes from an official domain, includes personal details only the real company would know, and doesn't request sensitive information.

---

## Key Phishing Indicators Identified

| Indicator | How to Spot It |
|-----------|----------------|
| **Spoofed Domains** | Check for misspellings like `paypal-verify.com` instead of `paypal.com` |
| **Urgency Language** | Words like "URGENT," "immediately," "24 hours," "account suspended" |
| **Generic Greetings** | "Dear Customer" or "Dear User" instead of your actual name |
| **Suspicious Links** | Hover to reveal the actual URL; fake domains often use hyphens or extra words |
| **Requests for Info** | Legitimate companies never ask for passwords or payment details via email |
| **Poor Grammar** | Odd sentence structure, spelling errors, inconsistent formatting |

---

## Prevention & Awareness Guidelines

### For Users

**🔍 Verify the Sender**
- Always click or hover over the sender name to reveal the actual email address
- Legitimate companies use official domains like `@amazon.com`, not `@amazon-security.net`
- Watch for typos like `paypa1.com` or `rnicrosoft.com`

**⏸️ Pause Before Acting**
- Attackers create urgency to make you act without thinking
- If an email demands immediate action, stop and verify through official channels first

**🖱️ Inspect Links Before Clicking**
- Hover over every link to see where it actually goes
- Red flags: mismatched domains, HTTP (not HTTPS), shortened URLs like `bit.ly`
- When in doubt, type the website address directly into your browser

**📎 Treat Attachments with Caution**
- Never open unexpected attachments, especially `.exe`, `.zip`, `.docm`, or `.xlsm`
- Fake invoices are a common way to deliver malware

**📢 Report Suspicious Emails**
- Don't just delete—use the "Report Phishing" button in your email client
- Forward suspicious emails to your IT or security team to help protect others

---

### For Organizations

| Control | Action |
|---------|--------|
| **Email Authentication** | Implement SPF, DKIM, and DMARC to prevent domain spoofing |
| **Email Filtering** | Deploy solutions that block malicious domains and attachments |
| **User Training** | Conduct regular phishing simulations to test and educate employees |
| **Reporting Channel** | Create a simple way for staff to report suspicious emails (e.g., `reportphishing@company.com`) |
| **Incident Response** | Have a process to quickly block malicious domains and notify all users |

---

## Tools Used

| Tool | Purpose |
|------|---------|
| Email Header Analysis | Inspect sender domain and routing information |
| Browser DevTools | Examine and verify suspicious links safely |
| Google Docs | Format and structure the final report |

---

## Repository Contents

| File | Description |
|------|-------------|
| `README.md` | Project overview and documentation |
| `email-samples.md` | Raw email samples analyzed |
| `phishing-detection-report.pdf` | Complete professional report with findings |
| `prevention-guidelines.md` | Detailed security guidelines |

---

## Key Takeaways

1. **Phishing targets psychology, not technology** – Attackers rely on fear, urgency, and trust to bypass logical thinking
2. **Domain inspection is critical** – Small variations like `paypal-verify.com` are easy to miss but reveal the scam
3. **Personalization indicates legitimacy** – Real companies use your name; generic greetings are a red flag
4. **Awareness is the best defense** – Technical controls help, but educated users are the strongest protection

---

## Connect

- **GitHub:** [Your GitHub Profile Link]
- **LinkedIn:** [Your LinkedIn Profile Link]

---

*This project was completed as part of the Future Interns Cyber Security Internship Program.*

*Last Updated: March 2026*
