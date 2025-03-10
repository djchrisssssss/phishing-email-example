# Phishing Email Sample

This repository contains a **phishing email** I personally received on **February 15, 2025**, claiming to be from “Wintermute Trading.” The email targeted my organization. I am sharing it here for **educational and security research purposes** only—please do not use it for any illegal activities.

---

## 1. Overview

- **Alleged Sender:** Wintermute Trading `<partnerships@wintermute.com>`
- **Actual Sending Domain:** Different from the header (e.g., `srv1862.main-hosting.eu` or `wintermute.business`)
- **Subject:** **Wintermute & Scallop.io**
- **Aim/Purpose:** To deceive recipients into thinking this is a legitimate market-maker invitation, enticing them to click suspicious links or join a phishing Telegram group.

The email employs a spoofed sender address, professional formatting, and references to legitimate company names to lower the recipient’s defenses.

---

## 2. Original File

- [Wintermute & Scallop.io.eml](./Wintermute & Scallop.io.eml)

You can open this `.eml` file with any mail client or text editor to inspect the **full headers** and **HTML content**.  
Some personal or sensitive information may be redacted for privacy.

---

## 3. Key Indicators of Phishing

1. **Suspicious Email Headers**  
   - **DMARC Failure:** The header domain (`wintermute.com`) doesn’t match the actual sending domain.  
   - **SPF Pass but DMARC Fail:** Attackers can use relays or Google Groups to bypass some spam filters.

2. **Brand Spoofing**  
   - The email leverages a genuine company’s logo and name, making it appear more credible and professional.

3. **Malicious Links**  
   - The message contains a Telegram invite link (`https://t.me/+xxxxxx`), potentially used for fraud or data harvesting.

4. **Mismatch Between Displayed and Actual Domains**  
   - Although it appears to be from `@wintermute.com`, the actual routing (envelope sender or relay info) points to other domains (e.g., `main-hosting.eu`).

---

## 4. Analysis and Identification

1. **Check the Original Headers**  
   - In Gmail or other mail clients, use “Show Original” (or similar) to compare:  
     - **“From”** vs **“Envelope-From”**  
     - **SPF, DKIM, DMARC** results  
   - If there’s a mismatch or DMARC failure, be highly cautious.

2. **Verify Domain Authenticity**  
   - If the “From” domain differs from the actual sending server, that’s a major red flag.

3. **Be Careful with Links**  
   - Never click a Telegram invite or unknown URL without verifying through official channels or the company’s main website.

4. **Watch Out for Impersonation**  
   - Attackers often copy official branding to appear more authentic. When in doubt, confirm via the organization’s legitimate contact information.

---

## 5. Further Reading

- [Google Support: How to Handle Phishing Emails](https://support.google.com/mail/answer/8253)
- [Phishing.org: Phishing Basics](http://www.phishing.org/)
- [DMARC Official Site](https://dmarc.org/) – Learn how to prevent domain spoofing

---

## 6. Disclaimer

This repository and the included email sample are provided strictly for educational and security research purposes. **Do not** use any of the content or techniques here for illegal or unethical activities. Always follow best practices and your organization’s policies when handling suspicious emails.
