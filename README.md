# Phishing Email Example

This repository contains a phishing email sample I personally received, shared here for learning and reference.  
Please do not use it for any illegal activities.

---

## 1. Overview

- **Purported Sender:** Wintermute Trading `<partnerships@wintermute.com>`  
- **Subject:** Wintermute & Scallop.io  
- **Date:** February 15, 2025  
- **Purpose:** Phishing attempt seeking to lure recipients into clicking suspicious links or joining a fake Telegram group.

The email poses as a professional market-maker invitation, but is in fact crafted to deceive the recipient.

---

## 2. Original File

- [phishing_email_sample.eml](./phishing_email_sample.eml) (or .txt)

You can open this file to see the full email headers and contents.  
(Some personal info or sensitive data may be redacted.)

---

## 3. Key Indicators

1. **Suspicious Headers**  
   - Traces show the actual sending source is not `wintermute.com` but a different domain (e.g., `main-hosting.eu`).  
   - DMARC fails, but SPF might appear to pass due to relay or Google Groups usage.

2. **Malicious or Suspicious Link**  
   - The email includes a Telegram invite link (e.g., `https://t.me/+xxxxxx`) that could be used for fraud.

3. **Spoofed Branding**  
   - The content is styled with a professional layout and a brand logo to reduce suspicion.

---

## 4. Analysis Steps

1. **Inspect Original Headers**  
   - Use “Show Original” (in Gmail or any mail client) to compare the “From” vs. “Envelope-From,” along with SPF, DKIM, and DMARC results.

2. **Watch Out for Fake Domains**  
   - Notice the mismatch between `@wintermute.com` and the actual sending domain or server.

3. **Be Cautious with Links**  
   - Always verify official partnerships or brand invitations through known channels, rather than clicking unsolicited links.

---

## 5. References

- [Google Support: How to Handle Phishing Emails](https://support.google.com/mail/answer/8253)
- [Phishing.org: Phishing Basics](http://www.phishing.org/)

---

## 6. Disclaimer

This repository is provided for educational and security research purposes only. Do not use the content for illegal or unethical activities.
