# Soc-Triage-Simulations

SOC Tier-2 style incident triage simulations using Windows, SIEM-style logs, and cloud security events.  
Each incident includes raw logs, analyst triage, and a reconstructed attack timeline.

> All incidents were manually analyzed without pre-labeled alerts to simulate real SOC conditions.

---

# SOC Analyst Incident Triage Portfolio

This repository demonstrates my ability to perform real-world SOC triage,  
incident analysis, and attack-chain reconstruction using Windows, Active Directory,  
SIEM-style logs, and cloud-style security events.

This work is based on:
- A self-built virtual lab (VirtualBox)
- Windows Server (AD / DC)
- Windows endpoints
- Security Onion / SIEM-style telemetry
- Manual triage without automated hints

---

## 🔐 Skills Demonstrated

- Authentication analysis (NTLM, Kerberos, logon types)
- PowerShell abuse detection
- Malware staging and persistence identification
- Credential dumping indicators (LSA / SAM)
- Lateral movement (WS → WS → DC)
- Privilege escalation detection
- Command-and-Control (C2) vs Exfiltration
- Cloud and on-prem log correlation
- Incident severity classification
- SOC Tier-2 style escalation

---





## 📖 How to Review
Start with `raw-logs.txt`, then review `analyst-triage.md`, and finally `timeline.md` to see how raw telemetry was converted into a confirmed incident assessment.
This mirrors a Tier-2 SOC workflow: alert review → investigation → escalation-ready documentation.

## 🧠 Analyst Notes

All findings represent defensive analysis only.  
Indicators, accounts, IPs, and payloads are simulated.  
Focus is on reasoning, triage methodology, and documentation quality.


