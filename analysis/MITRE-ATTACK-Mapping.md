# MITRE ATT&CK Mapping

## Objective

This document maps the observed phishing activity to the MITRE ATT&CK framework based on evidence collected during the investigation.

Only techniques directly supported by the available evidence have been included.

---

# ATT&CK Mapping

| Tactic | Technique | ID | Evidence |
|--------|-----------|----|----------|
| Initial Access | Phishing | T1566 | Email used social engineering to deliver a malicious attachment and link. |
| Initial Access | Spearphishing Attachment | T1566.001 | Email included a macro-enabled Microsoft Word document (`Invoice_10482.docm`). |
| Initial Access | Spearphishing Link | T1566.002 | Email contained a link directing the user to a suspicious typosquatted domain. |

---

# Technique Analysis

## T1566 — Phishing

The attacker attempted to obtain user interaction by sending a fraudulent email impersonating Microsoft Billing.

Evidence supporting this technique:

- Brand impersonation
- Financial-themed phishing email
- Urgency ("complete payment today")
- Suspicious attachment
- Suspicious embedded link

---

## T1566.001 — Spearphishing Attachment

The email included a Microsoft Word macro-enabled attachment (`Invoice_10482.docm`).

Macro-enabled Office documents are commonly used to deliver malware after convincing a victim to enable macros.

Observed evidence:

- `.docm` attachment
- Invoice-themed lure
- Finance department targeted

---

## T1566.002 — Spearphishing Link

The email contained a hyperlink directing the recipient to a typosquatted domain.

Such links are commonly used for:

- Credential harvesting
- Malware delivery
- Redirecting victims to phishing pages

Observed evidence:

- `hxxps://micros0ft-billing[.]com/invoice`
- Brand impersonation
- Suspicious domain

---

# ATT&CK Navigator Summary

| Technique ID | Name |
|--------------|------|
| T1566 | Phishing |
| T1566.001 | Spearphishing Attachment |
| T1566.002 | Spearphishing Link |

---

# Analyst Assessment

The observed activity aligns with MITRE ATT&CK Initial Access techniques involving phishing.

Although there is no evidence that the attachment was executed or the embedded link was accessed, the email demonstrates multiple phishing delivery mechanisms designed to persuade the recipient to interact with malicious content.

The investigation therefore maps only the techniques directly observed during the delivery stage and does not infer post-compromise activity.

---

## ATT&CK Tactics Covered

| Initial Access |
|----------------|
| ✅ T1566 |
| ✅ T1566.001 |
| ✅ T1566.002 |
