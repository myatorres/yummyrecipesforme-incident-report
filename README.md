# YummyRecipesForMe.com - Security Incident Report

This repository documents a cybersecurity incident investigation I performed as part of the [Google Cybersecurity Certificate](https://www.coursera.org/professional-certificates/google-cybersecurity) on Coursera.

## Scenario

A former employee compromised the web server for `yummyrecipesforme.com` via a brute force attack on the admin account. After gaining access, the attacker modified the source code of the website to distribute malware, redirecting users to a malicious website. The project documents the investigation, analysis of tcpdump network logs, and recommendations for improving security.

[See the full scenario](scenario/scenario_description.md)

---

## Provided Supporting Materials

- **[Incident Report](incident_report.md)**  
  A detailed account of the incident, analysis of network protocols involved, and recommendations for remediation.

- **[tcpdump Logs](data/tcpdump_log.pdf)**  
  The packet captures showing DNS and HTTP traffic during the incident.

- **[How to Read tcpdump Logs](data/how_to_read_tcpdump.pdf)**  
  A reference guide provided as part of the course.

- **[Security Incident Report Template](templates/security_incident_report_template.pdf)**  
  The original blank template used to structure this report.

---

## Project Structure

| File/Folder | Description |
|-------------|-------------|
| `incident_report.md` | The finalized incident report |
| `data/` | Contains tcpdump logs and supporting materials |
| `scenario/` | Contains the scenario text |
| `templates/` | Contains the blank report template |
| `LICENSE` | The license governing this repository |

---

## How to Use

If you'd like to follow along or practice:
1. Review the scenario in `scenario/scenario_description.md`.
2. Examine the `tcpdump_log.txt` in `data/` to analyze the captured traffic.
3. Reference `how_to_read_tcpdump.pdf` to help interpret the packet capture.
4. Read the completed `incident_report.md` to see documentation and recommendations.

---

*This project is for educational purposes only as part of a course lab activity.*

