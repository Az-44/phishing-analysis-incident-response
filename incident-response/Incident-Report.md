# Incident Report

## Executive Summary

A Finance employee reported a suspicious invoice email claiming to originate from Microsoft Billing. The message requested immediate payment, contained a macro-enabled Microsoft Word attachment, and included a hyperlink to a typosquatted domain.

The investigation identified multiple indicators consistent with a phishing campaign, including sender impersonation, failed email authentication (SPF and DMARC), a missing DKIM signature, and social engineering techniques designed to pressure the recipient into opening the attachment or visiting the embedded link.

No evidence indicates that the recipient opened the attachment or clicked the embedded link. Based on the available evidence, the incident was classified as a **high-confidence phishing attempt** with no confirmed endpoint compromise.

---

# Incident Details

| Field | Value |
|--------|-------|
| Incident ID | INC-2026-0087 |
| Category | Phishing |
| Severity | High |
| Status | Closed |
| Reported By | Sarah Johnson |
| Department | Finance |
| Date Reported | 2026-08-04 |
| Analyst | Az E. |

---

# Investigation Timeline

| Time | Activity |
|------|----------|
| 09:17 UTC | User reported a suspicious invoice email. |
| 09:20 UTC | Initial triage performed. |
| 09:28 UTC | Email headers analyzed. |
| 09:37 UTC | IOC extraction completed. |
| 09:48 UTC | Threat intelligence enrichment performed. |
| 10:02 UTC | MITRE ATT&CK mapping completed. |
| 10:10 UTC | Incident report finalized and closed. |

---

# Investigation Summary

The investigation focused on validating the legitimacy of the reported email and determining whether the organization had experienced a successful phishing compromise.

Analysis identified several high-confidence phishing indicators:

- Typosquatted sender domain
- Failed SPF authentication
- Failed DMARC authentication
- Missing DKIM signature
- Macro-enabled Microsoft Word attachment
- Urgent payment request
- Microsoft brand impersonation
- Suspicious embedded hyperlink

Threat intelligence enrichment provided limited public reputation for the observed infrastructure. However, the absence of public detections did not reduce confidence in the phishing assessment because the email itself contained sufficient technical and behavioral indicators to classify it as malicious.

---

# Root Cause Analysis

The phishing attempt relied primarily on social engineering rather than technical exploitation.

The attacker attempted to exploit user trust by:

- Impersonating Microsoft Billing
- Creating urgency through an outstanding invoice
- Targeting a Finance employee
- Encouraging interaction with a macro-enabled attachment
- Providing a deceptive payment link

No evidence suggests that the recipient interacted with the attachment or hyperlink.

---

# Business Impact Assessment

### Confirmed Impact

- No confirmed malware execution
- No confirmed credential compromise
- No confirmed unauthorized access
- No confirmed financial loss

### Potential Impact

If the recipient had interacted with the email, potential consequences could have included:

- Credential theft
- Malware infection
- Initial network access
- Financial fraud
- Business Email Compromise (BEC)

---

# Final Verdict

The investigated email is assessed as a **high-confidence phishing attempt**.

Although public threat intelligence sources did not identify the observed infrastructure as malicious, the investigation identified multiple independent indicators supporting the phishing classification.

The evidence does not indicate that the attachment was executed or that the embedded hyperlink was accessed. Therefore, the investigation found **no evidence of endpoint compromise** at the time of analysis.

---

# Recommendations

- Block the typosquatted domain at the email gateway.
- Block the associated IP address where appropriate.
- Remove the email from all affected mailboxes.
- Educate users on recognizing phishing indicators.
- Disable Office macros where business requirements allow.
- Continue monitoring for similar phishing attempts.
- Review email authentication policies (SPF, DKIM, and DMARC).

---

# Lessons for Security Operations

This investigation demonstrates the importance of combining technical analysis with contextual evidence.

Public threat intelligence can support an investigation but should not be the sole basis for determining whether an email is malicious.

Indicators such as failed email authentication, sender impersonation, suspicious attachments, and social engineering techniques provided sufficient evidence to classify the message as a phishing attempt even in the absence of significant public reputation.
