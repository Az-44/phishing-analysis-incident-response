# Lessons Learned

## Project Overview

This project simulated the investigation of a phishing email from the perspective of a SOC analyst. The objective was not only to identify phishing indicators but also to follow a structured incident response process, document findings, and communicate the results clearly.

---

# Key Technical Takeaways

## Phishing Detection Goes Beyond Reputation

One of the biggest lessons from this project was that public threat intelligence should support an investigation—not drive it.

Although VirusTotal and other public intelligence sources provided little or no reputation for the investigated domain, the email itself contained sufficient evidence to classify it as a high-confidence phishing attempt.

Indicators such as:

- Failed SPF authentication
- Failed DMARC authentication
- Missing DKIM signature
- Brand impersonation
- Typosquatted domain
- Macro-enabled attachment
- Urgent payment request

provided stronger evidence than reputation alone.

---

## Email Headers Contain Valuable Evidence

This project reinforced the importance of email header analysis.

Authentication results such as SPF, DKIM, and DMARC can quickly identify sender impersonation attempts and should always be reviewed during phishing investigations.

---

## Documentation Is Part of Incident Response

Investigating an incident is only part of a SOC analyst's responsibility.

Equally important is documenting findings in a clear and structured manner so that other analysts, incident responders, or management can understand what occurred and what actions were taken.

---

## MITRE ATT&CK Should Be Evidence-Based

Rather than mapping every possible ATT&CK technique, this project only mapped techniques directly supported by the available evidence.

This approach produces more accurate and defensible documentation.

---

# Challenges Encountered

During the IOC enrichment phase, most public threat intelligence sources returned little or no reputation for the investigated domain.

Initially, this seemed like a limitation.

However, it highlighted an important lesson:

The absence of public detections does **not** indicate that an email is legitimate.

Security analysts must evaluate the complete context of an investigation instead of relying solely on external reputation services.

---

# What I Would Improve

If this investigation were expanded in the future, I would:

- Analyze a real-world phishing sample using sanitized indicators.
- Investigate attachment metadata and file hashes.
- Perform deeper email header analysis using additional tools.
- Include SIEM detection logic for identifying similar phishing emails at scale.
- Automate IOC extraction using Python.

---

# Skills Strengthened

This project strengthened my understanding of:

- Phishing investigation
- Email header analysis
- IOC extraction
- Threat intelligence enrichment
- MITRE ATT&CK mapping
- Incident response documentation
- Technical report writing

---

# Final Reflection

This project demonstrated the complete workflow of a phishing investigation, from initial triage through incident reporting and remediation.

More importantly, it reinforced that effective security analysis depends on evaluating evidence, communicating findings clearly, and making decisions based on the overall context of an investigation rather than a single indicator.

---

## Personal Reflection

This project improved both my technical investigation skills and my ability to document security incidents in a structured and professional manner.

It also reinforced the importance of making evidence-based decisions and communicating technical findings in a way that can be understood by both technical teams and management.
