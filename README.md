# Soc-Triage-Simulations
SOC Tier-2 style incident triage simulations using Windows, SIEM-style logs, and cloud security events.
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

## 📁 Incident Simulations

### Incident 1: Multi-Host Lateral Movement (WS → WS → DC)
**Severity:** Critical  
**Techniques Observed:**  
- Initial access via credential reuse  
- PowerShell obfuscation  
- Service-based persistence  
- Credential dumping  
- Lateral movement via NTLM  
- Domain privilege escalation  

➡️ Full triage write-up below.

#### 📂 Incident Files

```text
/incident-01-lateral-movement
├── raw-logs.txt
├── analyst-triage.md
└── timeline.md
