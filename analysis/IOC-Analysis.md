# IOC Analysis

## Objective

The purpose of this phase is to identify, extract, and enrich all Indicators of Compromise (IOCs) observed during the investigation.

---

# Extracted Indicators

| IOC Type | Indicator | Status |
|----------|-----------|--------|
| Domain | micros0ft-billing.com | Suspicious |
| URL | hxxps://micros0ft-billing[.]com/invoice | Suspicious |
| IP Address | 185.225.69.55 | Suspicious |
| Email Address | accounts@micros0ft-billing.com | Suspicious |
| Reply-To | support@micros0ft-billing.com | Suspicious |
| Attachment | Invoice_10482.docm | High Risk |

---

# IOC Enrichment

The following public threat intelligence sources were used during the investigation:

- VirusTotal
- Cisco Talos Intelligence
- AbuseIPDB
- WHOIS
- URLScan.io

---

## IOC Findings

| IOC | Finding |
|------|----------|
| Domain | Typosquatted Microsoft domain |
| URL | Invoice payment page impersonating Microsoft |
| IP Address | External infrastructure not associated with Microsoft |
| Attachment | Macro-enabled Microsoft Word document |
| Overall Assessment | High-confidence phishing infrastructure |

---

## Analyst Assessment

Multiple indicators collectively support the conclusion that the email is part of a phishing campaign. The use of a typosquatted domain, failed authentication, suspicious infrastructure, and a macro-enabled attachment significantly increase confidence that the sender intended to deceive the recipient.
