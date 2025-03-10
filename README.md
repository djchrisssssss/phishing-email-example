# Phishing Email Sample

This repository contains a **phishing email** I personally received on **February 15, 2025**, purporting to be from “Wintermute Trading” and targeting my organization. I am sharing it here for **educational and security research purposes**—please do not use it for any illegal activities.

---

## 1. Overview

- **Sender Claimed:** Wintermute Trading `<partnerships@wintermute.com>`
- **Actual Source:** A different domain (e.g., `srv1862.main-hosting.eu` or `wintermute.business`)
- **Subject:** **Wintermute & Scallop.io**
- **Intended Purpose:** To deceive recipients into believing it’s a professional market-maker invitation and lure them into joining a suspicious Telegram group or clicking malicious links.

This email leverages a spoofed sender address, a professional-looking layout, and references to legitimate companies to lower the recipient’s guard.

---

## 2. Original File

- [phishing_email_sample.eml](./phishing_email_sample.eml)

Open this `.eml` file in any mail client or text editor to inspect the **full headers** and **HTML content**.  
Some personal or confidential information may be redacted to protect privacy.

---

## 3. Key Indicators of Phishing

1. **Suspicious Email Headers**  
   - **DMARC Failure:** Shows the header domain (`wintermute.com`) does not match the actual sending domain.
   - **SPF Pass but DMARC Fail:** Attackers exploit relay or Google Groups to bypass certain spam filters.

2. **Brand Spoofing**  
   - The email uses a real company’s logo and name, giving it a deceptive, professional appearance.

3. **Malicious Links**  
   - The message invites you to a Telegram group (`https://t.me/+xxxxxx`), which could be used to harvest information or facilitate fraud.

4. **Mismatch Between Visible and Actual Domains**  
   - The “From” line displays `@wintermute.com` while the envelope sender or mail path references different domains (e.g. `main-hosting.eu`).

---

## 4. How to Analyze/Identify

1. **Check the Original Headers**  
   - In Gmail or other mail clients, use “Show Original” (or equivalent) to compare:
     - **“From”** vs **“Envelope-From”**
     - **SPF, DKIM, DMARC** results  
   - Look for any sign of mismatch or DMARC failure.

2. **Verify Domain Authenticity**  
   - If the domain in the “From” field differs from the actual sending server, that’s a major red flag.

3. **Scrutinize Links**  
   - Never trust Telegram invites or unknown URLs at face value. Go through verified channels or contact the real company via their official website.

4. **Stay Alert for Impersonation**  
   - Attackers often copy official branding to appear legitimate. Always double-check with the real organization when in doubt.

---

## 5. References & Further Reading

- [Google Support: How to Handle Phishing Emails](https://support.google.com/mail/answer/8253)
- [Phishing.org: Phishing Basics](http://www.phishing.org/)
- [DMARC Official Site](https://dmarc.org/) — For more on preventing spoofed emails

---

## 6. Disclaimer

This repository and the sample email are provided strictly for educational purposes to help others recognize and analyze phishing attempts. **Do not** use any of the content or techniques here for illegal or unethical activities. Always follow best practices and organizational policies when handling suspicious messages.
