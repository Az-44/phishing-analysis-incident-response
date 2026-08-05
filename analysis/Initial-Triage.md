
# Initial Triage

## Incident Overview

| Field | Value |
|--------|-------|
| Incident ID | INC-2026-0087 |
| Reported By | Sarah Johnson |
| Department | Finance |
| Reported Time | 2026-08-04 09:17 UTC |
| Category | Phishing |
| Initial Severity | High |
| Status | Under Investigation |

---

## Summary

A finance employee reported receiving an unsolicited invoice email requesting urgent payment. The email impersonates Microsoft Billing and includes a macro-enabled Microsoft Word attachment (`.docm`) along with a suspicious URL. Initial review identified multiple indicators consistent with a phishing attempt.

---

## Initial Observations

- Sender uses a typosquatted domain (`micros0ft-billing.com`).
- The email creates a sense of urgency by requesting immediate payment.
- The attachment is a macro-enabled Microsoft Word document (`.docm`).
- Email authentication checks failed (SPF and DMARC), and no DKIM signature is present.
- The email targets a Finance employee, a common target for invoice fraud.
- The embedded URL points to the same suspicious domain.

---

## Risk Assessment

| Category | Assessment |
|----------|------------|
| Credential Theft | Possible |
| Malware Delivery | Highly Likely |
| Business Email Compromise | Possible |
| Financial Fraud | Possible |

---

## Initial Analyst Assessment

Based on the initial review, the email exhibits several characteristics commonly associated with phishing campaigns, including brand impersonation, social engineering, failed email authentication, and the use of a macro-enabled attachment. The message is assessed as a high-confidence phishing attempt and requires further investigation.

---

## Immediate Actions

- Advise the user not to open the attachment or click any links.
- Isolate the email for investigation.
- Preserve the email headers and attachment metadata as evidence.
- Begin IOC extraction and enrichment.
- Determine whether similar emails were delivered to other users.
