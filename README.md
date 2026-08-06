<p align="center">
  <img src="evidence/screenshots/phishing-analysis-incident-response_banner" alt="Phishing Analysis & Incident Response Banner">
</p>

# Phishing Analysis & Incident Response

> A SOC-style phishing investigation demonstrating email triage, header analysis, IOC enrichment, MITRE ATT&CK mapping, incident response, and technical reporting.

---

## Project Overview

This project simulates the investigation of a phishing email from the perspective of a Security Operations Center (SOC) analyst.

The objective was to determine whether the reported email represented a legitimate security threat by analyzing the email content, authentication headers, embedded indicators, and social engineering techniques before documenting the investigation and recommended response.

The investigation follows a structured incident response workflow commonly used by SOC analysts:

- Initial Triage
- Email Header Analysis
- Email Body Analysis
- IOC Extraction & Enrichment
- MITRE ATT&CK Mapping
- Incident Reporting
- Containment & Remediation
- Lessons Learned

---

## Investigation Summary

| Category | Result |
|----------|--------|
| Incident Type | Phishing |
| Severity | High |
| Status | Closed |
| Verdict | High-Confidence Phishing Attempt |
| User Interaction | No Evidence Observed |
| Endpoint Compromise | Not Observed |

---

## Investigation Workflow

```text
User Reports Suspicious Email
            │
            ▼
      Initial Triage
            │
            ▼
   Header & Body Analysis
            │
            ▼
 IOC Extraction & Enrichment
            │
            ▼
 MITRE ATT&CK Mapping
            │
            ▼
 Incident Report
            │
            ▼
 Containment & Remediation
```

---

## Investigation Artifacts

| Investigation Phase | Documentation |
|---------------------|---------------|
| Initial Triage | [View](analysis/Initial-Triage.md) |
| Header Analysis | [View](analysis/Header-Analysis.md) |
| Email Body Analysis | [View](analysis/Email-Body-Analysis.md) |
| IOC Analysis | [View](analysis/IOC-Analysis.md) |
| MITRE ATT&CK Mapping | [View](analysis/MITRE-ATTACK-Mapping.md) |
| Incident Report | [View](incident-response/Incident-Report.md) |
| Containment & Remediation | [View](incident-response/Containment-and-Remediation.md) |
| Lessons Learned | [View](incident-response/Lessons-Learned.md) |

---

## Indicators of Compromise (IOCs)

| Type | Indicator |
|------|-----------|
| Domain | `micros0ft-billing.com` |
| URL | `hxxps://micros0ft-billing[.]com/invoice` |
| Sender Email | `accounts@micros0ft-billing.com` |
| Reply-To | `support@micros0ft-billing.com` |
| IP Address | `185.225.69.55` |
| Attachment | `Invoice_10482.docm` |

---

## MITRE ATT&CK Techniques

| Tactic | Technique | ID |
|--------|-----------|----|
| Initial Access | Phishing | T1566 |
| Initial Access | Spearphishing Attachment | T1566.001 |
| Initial Access | Spearphishing Link | T1566.002 |

---

## Tools & Resources

### Analysis

- Manual Email Review
- Email Header Analysis
- IOC Extraction

### Threat Intelligence

- VirusTotal
- AbuseIPDB
- WHOIS

### Frameworks

- MITRE ATT&CK

---

## Repository Structure

```text
phishing-analysis-incident-response/

├── analysis/
├── evidence/
├── incident-response/
├── tools/
├── LICENSE
└── README.md
```

---

## Key Skills Demonstrated

- Phishing Investigation
- Email Header Analysis
- IOC Extraction
- Threat Intelligence Enrichment
- MITRE ATT&CK Mapping
- Incident Response
- Technical Documentation
- Security Analysis
- Risk Assessment

---

## Key Takeaways

- Investigated a phishing email using a structured SOC workflow.
- Extracted and analyzed Indicators of Compromise (IOCs).
- Performed email authentication analysis (SPF, DKIM, and DMARC).
- Applied MITRE ATT&CK techniques based on observed evidence.
- Produced professional incident response documentation and remediation recommendations.

---

## Disclaimer

This repository is intended for educational purposes and demonstrates a structured phishing investigation workflow from the perspective of a Security Operations Center (SOC) analyst.

The phishing email, organization, and investigation scenario are fictional and were created to simulate a realistic incident response process. Public threat intelligence resources were used to demonstrate IOC enrichment where appropriate.

No production systems, organizational data, or unauthorized targets were accessed during this project.

---

## Credits

This project was built using publicly available cybersecurity resources and industry frameworks.

### Threat Intelligence

- VirusTotal
- AbuseIPDB
- WHOIS

### Security Frameworks

- MITRE ATT&CK®

### References

- Microsoft documentation (SPF, DKIM, and DMARC)
- Public phishing awareness guidance
- Industry-standard incident response practices

All third-party tools, trademarks, and frameworks remain the property of their respective owners.

---

## License

The original documentation and investigation content contained in this repository are licensed under the **MIT License**. See the [LICENSE](LICENSE) file for details.
