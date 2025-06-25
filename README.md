# task2_internship
 Objective: Identify phishing characteristics in a suspicious email sample.
 Tools:  Email client or saved email file (text), free online header analyzer.
 Deliverables: A report listing phishing indicators found.

 So, i obtained a online phishing mail sample as it was from online source it doesn't include header the i first analyzed the online source sample then for header analyses and sharpening the knowledge i used mail from spam folder.
 ------------
 Sample 1 outcome.
 ## 📌 Email Summary

- **Subject:** Content Infringement on @Contoso Corp
- **Sender Name:** X Admin
- **Sender Address:** x@webnotifications[.]net
- **Recipient:** john.jdoe@mybusiness[.]com

---

## 🔍 Analysis Report

### 1. **Spoofed Sender**
- **Domain:** `webnotifications[.]net` is not affiliated with **X/Twitter**.
- **Expected Domain:** `@x.com`, `@twitter.com`, etc.
- ✅ **Phishing Indicator:** Yes

### 2. **Email Header Analysis**
- **Header not available** for this phishing sample.
- No SPF/DKIM/DMARC analysis could be done.
- ⚠️ **Phishing still highly likely** due to other strong indicators.

### 3. **Suspicious Link**
- Prominent **“Review Details”** button with no clear destination.
- Likely leads to a credential harvesting site.
- ✅ **Phishing Indicator:** Yes

### 4. **Urgent Language**
- “Your page may be suspended within 48 hours.”
- Creates pressure to act quickly.
- ✅ **Phishing Indicator:** Yes

### 5. **Generic Message**
- No specific mention of what content was removed or who filed the complaint.
- Example of vague text: “content posted X”.
- ✅ **Phishing Indicator:** Yes

### 6. **Brand Impersonation**
- Uses **X logo** and falsely claims to be from @Contoso Corp.
- ✅ **Phishing Indicator:** Yes

---

## 🧠 Conclusion

This email contains several phishing signs:

- Spoofed sender
- Unverifiable, generic complaint
- Fake urgency
- Suspicious CTA button
- False brand impersonation

📛 **This email is a phishing attempt**.  
🗑️ Delete immediately and report it as phishing to your provider.

---

## 📎 Evidence Screenshots

Screenshots are stored in the `screenshots/` folder:
-------------------
 The three main principles of email authentication are:

SPF (Sender Policy Framework):
Verifies if the sender’s IP is authorized to send mail for the domain.

DKIM (DomainKeys Identified Mail):
Uses a digital signature to check if the email content was altered in transit.

DMARC (Domain-based Message Authentication, Reporting, and Conformance):
Uses SPF and DKIM results to decide whether to deliver, reject, or quarantine the email.
--------------------
Phishing Email Analysis – Sample 2 (Spam-marked Marketing Email)

## 📄 Email Details

- **Subject:** 🌟 Three Things Hurting Your Social Posts  
- **From:** Vic from Visme <updates@visme.co>  
- **Date:** Tue, Jun 17, 2025, 2:57 AM  
- **Status:** Automatically flagged as spam by Gmail  
- **Source:** Found in Gmail Spam Folder  

---

## 📥 How Header Was Collected

The full email header was obtained by:
1. Clicking the three-dot menu in Gmail (next to "Reply").
2. Selecting **"Show original"** to reveal the full raw email header.
3. Copied the header and pasted into **MXToolbox** for analysis.

---

## 🔧 Tools Used

| Tool | Purpose |
|------|---------|
| **Gmail (Show Original)** | To extract the raw email header |
| **MXToolbox - Email Header Analyzer** | To test SPF, DKIM, and DMARC results |
| **MXToolbox - Deliverability Tool** | To verify DKIM validity when it failed in the analyzer |
| **Gmail Spam Explanation** | To understand Gmail’s reason for marking as spam |

---

## 🔐 Email Authentication Results

| Protocol | Result |
|----------|--------|
| **SPF**  | ✅ Pass (IP 54.240.11.36 allowed to send for visme.co) |
| **DKIM** | ✅ Pass (Verified domain `visme.co`) via Gmail header |
| **DMARC**| ✅ Pass (Policy aligned and enforced) |

*Note:* While MXToolbox showed **"DKIM Authenticated ❌"**, Gmail showed **DKIM 'PASS'** — this is a known issue due to DKIM validation incompatibility with copied headers.

---

## 🚩 Spam Indicators (Non-Phishing)

| Indicator               | Status      | Explanation |
|------------------------|-------------|-------------|
| Sender Authentication  | ✅ Legit     | Authenticated by SPF, DKIM, DMARC |
| Sender Domain           | ✅ Trusted   | Matches known email marketing service |
| Urgency or Threats      | ❌ None      | Tone is professional and educational |
| Attachments or Links    | ✅ Clean     | All links go to `visme.co` |
| Spam Reason (Gmail)     | ⚠️ Similar   | Similar to previous flagged marketing emails |

---

## ✅ Conclusion

- **Not a phishing attempt**.
- Marked as spam **due to Gmail heuristics**, not due to malicious behavior.
- Legitimate newsletter from Visme, authenticated and professionally written.
