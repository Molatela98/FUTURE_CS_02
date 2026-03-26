# Phishing Email Detection & Awareness System

**Task 2:** FUTURE_CS_02  
---

## Project Overview

This project focuses on identifying and analyzing phishing email threats. Three email samples were examined to detect common phishing indicators such as spoofed sender domains, malicious links, urgency tactics, and business email compromise (BEC) techniques. Each email was classified based on risk level, and actionable prevention guidelines were developed for both individuals and organizations.

---

## Email Analysis Findings

### Sample 1: PayPal Account Scam

**Classification:** Phishing (High Risk)

**Sender Domain:** `security@paypal-verify.com` – This is fraudulent. The legitimate domain is `@paypal.com`.

**Link Destination:** `http://paypal-security-verify.com/account/restore/verify-identity` – Leads to a fake PayPal login page designed to steal credentials.

**Urgency Tactic:** Claims the account will be "permanently suspended" within 24 hours unless immediate action is taken.

**Red Flags:** 
- Spoofed domain using "paypal-verify.com" instead of official "paypal.com"
- Generic greeting "Dear Valued Customer" instead of using the recipient's name
- Threat of permanent account closure creates panic
- Link uses HTTP instead of HTTPS, indicating an insecure site
- Poor grammar and formatting inconsistencies

**Why It's Dangerous:** This email creates panic by threatening immediate loss of account access. Users who click the link are directed to a fake login page designed to capture their PayPal username and password. Once credentials are stolen, attackers can drain bank accounts, make unauthorized purchases, and lock the victim out of their own account.

---

### Sample 2: CEO Fraud / Wire Transfer Scam

**Classification:** Phishing (High Risk)

**Sender Domain:** `james.carter@company-domain-support.com` – Impersonates a company executive using a fake domain.

**Urgency Tactic:** Claims a wire transfer of $48,500 must be processed within 2 hours to "secure a contract."

**Red Flags:**
- Sender domain does not match the legitimate company domain
- Executive claims to be "unreachable by phone" – a common tactic to prevent verification
- Requests urgent wire transfer to an external account
- Directs reply to the same suspicious email address
- No official purchase order or contract attached
- High-pressure language demanding immediate action

**Why It's Dangerous:** This is a classic Business Email Compromise (BEC) attack. The attacker impersonates a high-level executive to trick employees into authorizing fraudulent wire transfers. Since the request appears to come from leadership, employees may bypass normal approval processes. Funds sent to these accounts are often quickly moved overseas and become unrecoverable.

---

### Sample 3: Invoice Scam

**Classification:** 🟡 Suspicious (Medium Risk)

**Sender Domain:** `invoices@global-suppliers-network.org` – Claims to be from a vendor but uses a suspicious domain.

**Link Destination:** `http://global-suppliers-network.org/invoices/INV-38492-2026/view` – Leads to a fake invoice portal.

**Red Flags:**
- Sender domain `global-suppliers-network.org` does not match any known vendor
- Threat of "late fees" to pressure immediate payment
- Link leads to a fake website designed to steal credentials or deliver malware
- Generic greeting "Dear Accounts Payable" instead of addressing a specific person
- No previous communication or established vendor relationship
- Invoice details provided but cannot be verified independently

**Why It's Concerning:** This email targets accounts payable departments by impersonating a vendor with a past-due invoice. The goal is to trick staff into clicking the malicious link, which may lead to credential theft or malware installation. If the link is clicked, attackers could gain access to financial systems or corporate networks. Even if the link isn't clicked, replying to the email could confirm the email address is active for future attacks.

---

## Key Phishing Indicators Identified

**Spoofed Domains**  
Check for misspellings like `paypal-verify.com` instead of `paypal.com`. Attackers register domains that look similar to legitimate ones. Always verify the exact domain before trusting an email.

**Urgency and Threats**  
Words like "URGENT," "immediately," "24 hours," "permanent suspension," or "late fees" are designed to make you act without thinking. Attackers rely on panic to bypass logical decision-making.

**Generic Greetings**  
"Dear Customer," "Dear User," or "Dear Accounts Payable" instead of your actual name is a major red flag. Legitimate companies use your name and reference specific account details.

**Suspicious Links**  
Hover over every link to reveal the actual URL. Fake domains often use hyphens, extra words, or free hosting services. Legitimate companies use secure HTTPS connections, not HTTP.

**Requests for Money or Information**  
Legitimate companies never ask for passwords, credit card details, wire transfers, or login credentials via email. Any request for sensitive information should be verified through official channels.

**Executive Impersonation**  
Emails claiming to be from CEOs, CFOs, or other executives demanding urgent action should always be verified. Attackers exploit the authority of leadership to bypass security procedures.

**Poor Grammar and Formatting**  
Odd sentence structure, spelling errors, inconsistent formatting, and unprofessional design are common in phishing emails. Legitimate companies maintain professional communication standards.

---

## Prevention & Awareness Guidelines

### For Users

**Verify the Sender**  
Always click or hover over the sender name to reveal the actual email address. Legitimate companies use official domains like `@amazon.com` or `@paypal.com`, not `@paypal-verify.com` or `@company-domain-support.com`. Watch for typos like `paypa1.com` or `rnicrosoft.com`.

**Pause Before Acting**  
Attackers create urgency to make you act without thinking. If an email demands immediate action, stop and verify through official channels first. Call the company using a phone number from their official website, not from the email.

**Inspect Links Before Clicking**  
Hover over every link to see where it actually goes. Red flags include mismatched domains, HTTP instead of HTTPS, and shortened URLs like `bit.ly`. When in doubt, type the website address directly into your browser.

**Verify Financial Requests**  
Any request for wire transfers, invoice payments, or changes to banking details should be verified through a separate communication channel. Call the requester using a known phone number, not the one listed in the email.

**Treat Attachments with Caution**  
Never open unexpected attachments, especially `.exe`, `.zip`, `.docm`, or `.xlsm` files. Fake invoices and delivery notices are common ways to deliver malware and ransomware.

**Report Suspicious Emails**  
Don't just delete—use the "Report Phishing" button in your email client. Forward suspicious emails to your IT or security team to help protect others. Reporting helps security teams identify and block emerging threats.

---

### For Organizations

**Email Authentication**  
Implement SPF, DKIM, and DMARC protocols to prevent attackers from spoofing your company domain. These protocols help email providers verify that messages actually come from your legitimate servers.

**Email Filtering**  
Deploy security solutions that automatically block malicious domains, suspicious attachments, and known phishing links. Advanced solutions can sandbox links and attachments for analysis before delivery.

**User Training**  
Conduct regular phishing simulations to test and educate employees. Track click rates and provide targeted training for those who fall for test emails. Focus on real-world scenarios like CEO fraud and invoice scams.

**Reporting Channel**  
Create a simple way for staff to report suspicious emails, such as a dedicated email address like `reportphishing@company.com`. Make reporting easy and encourage employees to report anything suspicious.

**Incident Response**  
Establish a clear process to quickly block malicious domains, reset compromised credentials, and notify all users when a phishing threat is identified. Speed is critical in containing phishing attacks.

**Wire Transfer Verification**  
Implement a mandatory dual-approval process for all wire transfers, especially those initiated by email. Require verbal confirmation with a known contact before processing any urgent payment requests.

---

## Tools Used

**Email Header Analysis** – Used to inspect sender domain, routing information, and authentication results to identify spoofed emails.

**Browser DevTools** – Helped examine and verify suspicious links safely without clicking them, revealing actual destinations.

**Google Docs / Word** – Used to format and structure the final report professionally with clear organization and readability.

---

## Key Takeaways

**Phishing targets psychology, not technology.**  
Attackers rely on fear, urgency, trust, and authority to bypass logical thinking. The most sophisticated technical controls can be defeated by a single user acting in panic.

**Domain inspection is critical.**  
Small variations like `paypal-verify.com` instead of `paypal.com` or `company-domain-support.com` instead of a legitimate company domain reveal the scam immediately when checked.

**CEO fraud is highly effective.**  
Impersonating executives to request urgent wire transfers works because employees are conditioned to follow leadership instructions without question. Always verify through a second channel.

**Invoice scams target finance teams.**  
Accounts payable departments are prime targets because they handle money transfers daily. Fake invoices with malicious links or fraudulent payment instructions can cause significant financial loss.

**Awareness is the best defense.**  
Technical controls help filter many threats, but educated users who know what to look for are the strongest protection against phishing. Regular training and simulations build a security-conscious culture.
