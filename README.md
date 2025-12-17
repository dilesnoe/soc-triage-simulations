# SOC Triage Simulations

**SOC Tier-2 style incident triage simulations** using Windows, SIEM-style telemetry,  
and cloud-inspired security events.

Each incident includes:
- Raw security logs
- Analyst triage notes
- A reconstructed attack timeline

> All incidents were manually analyzed **without pre-labeled alerts** to simulate real SOC conditions.

---

## 🧭 SOC Analyst Incident Triage Portfolio

This repository demonstrates my ability to perform **real-world SOC triage**,  
incident analysis, and **attack-chain reconstruction** across Windows and Active Directory environments.

The work reflects how incidents are handled in a production SOC:  
from raw telemetry → investigation → documented escalation.

### Lab Environment
- Self-built virtual lab (VirtualBox)
- Windows Server (Active Directory / Domain Controller)
- Windows workstation endpoints
- Security Onion / SIEM-style telemetry
- Manual analysis (no automated hints or detections)

---

## 🔐 Skills Demonstrated

- Authentication analysis (NTLM, Kerberos, logon types)
- PowerShell abuse detection
- Malware staging and persistence identification
- Credential dumping indicators (LSA / SAM)
- Lateral movement analysis (WS → WS → DC)
- Privilege escalation detection
- Command-and-Control (C2) vs data exfiltration
- Cloud and on-prem log correlation
- Incident severity classification
- SOC Tier-2 style escalation documentation

---

## 📁 Incident Simulations

### 🔴 Incident 1: Multi-Host Lateral Movement (WS → WS → DC)
**Severity:** Critical

**Techniques Observed:**
- Initial access via credential reuse
- PowerShell obfuscation
- Service-based persistence
- Credential dumping activity
- Lateral movement via NTLM authentication
- Domain-level privilege escalation

➡️ Full triage write-up available in the incident folder.

 
### 🟠 Incident 2: Failed Lateral Movement Attempt (WS-18 → WS-25)
**Severity:** Medium

**Techniques Observed:**
- Failed NTLM authentication attempts
- Attempted ADMIN$ share access
- Cross-host authentication using multiple accounts
- Process execution via net.exe
- Blocked lateral movement attempt


➡️ Full triage write-up available in the incident folder.

#### 📂 Incident Files
```text
/incident-01-lateral-movement
├── raw-logs.txt
├── analyst-triage.md
└── timeline.md

/incident-02-failed-lateral-movement
├── raw-logs.txt
├── analyst-triage.md
└── timeline.md
```


## 📖 How to Review
Start with `raw-logs.txt`, then review `analyst-triage.md`, and finally `timeline.md` to see how raw telemetry was converted into a confirmed incident assessment.
This mirrors a Tier-2 SOC workflow: alert review → investigation → escalation-ready documentation.

## 🧠 Analyst Notes

All findings represent defensive analysis only.  
Indicators, accounts, IPs, and payloads are simulated.  
Focus is on reasoning, triage methodology, and documentation quality.


