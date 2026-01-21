# Incident 01 – Analyst Triage Report

## Summary
Investigation identified a confirmed multi-host intrusion originating on WS-21, followed by credential access, lateral movement, and domain-level privilege escalation impacting WS-22 and DC-01.

---

## Severity Assessment
**Critical**

**Rationale:** Successful credential dumping, lateral movement across multiple systems, and confirmed domain controller authentication significantly expanded the blast radius and required immediate incident response.

---

## Scope & Impact
- **Affected hosts:** WS-21, WS-22, DC-01
- **Affected accounts:** a.chen, helpdesk.admin
- **Impact:** Loss of domain trust boundary; potential full Active Directory compromise

---

## Detection Context
Activity was identified during manual review of authentication, process execution, and service creation telemetry. Observed behavior deviated from normal administrative patterns and aligned with known post-exploitation techniques.

---

## Analyst Findings

### Initial Access & Execution
- NTLM authentication using user credentials inconsistent with baseline activity
- Obfuscated PowerShell execution used to retrieve external script content

**Assessment:** Strong indication of initial access through compromised credentials rather than legitimate administration.

---

### Persistence
- Unauthorized service creation configured for auto-start under SYSTEM context

**Assessment:** Persistence mechanism established to maintain access across system reboots.

---

### Credential Access
- LSA access attempts by non-standard binary
- Privileged token usage observed

**Assessment:** Successful credential harvesting enabled further lateral movement.

---

### Lateral Movement & Escalation
- NTLM authentication as privileged account across multiple hosts
- Administrative share access and service deployment on secondary host
- Domain controller authentication followed by elevated privilege confirmation

**Assessment:** Attacker successfully escalated privileges and expanded control to the domain level.

---

## Evidence Highlights
- Authentication events (4624 / NTLM) supporting credential reuse
- PowerShell script block logging (4104) indicating obfuscated execution
- Service creation events (7045) establishing persistence
- Privilege assignment events (4672)
- Kerberos ticket activity on domain controller

---

## Conclusion
This activity represents a confirmed intrusion with credential theft, lateral movement, and domain-level compromise. The incident exceeds monitoring thresholds and requires coordinated incident response.

---

## Recommended Actions
- Isolate affected systems immediately
- Disable compromised accounts and reset credentials
- Remove malicious services and binaries
- Revoke domain-level credentials and review AD integrity
- Block identified command-and-control infrastructure
- Escalate to Incident Response for containment and recovery

