# Incident 01 – Analyst Triage Report

## Summary
Multi-host lateral movement originating from WS-21, spreading to WS-22 and DC-01.

## Severity
Critical

## Scope / Impact
- Affected hosts: WS-21, WS-22, DC-01
- Affected accounts: a.chen, helpdesk.admin

## Initial Detection
Alert triggered by suspicious PowerShell execution and NTLM authentication anomalies.

## Analysis
- Initial access via credential reuse (NTLM)
- Obfuscated PowerShell used to stage payload
- Service-based persistence established
- Credential dumping via LSA access
- Lateral movement WS → WS → DC
- Domain-level privilege escalation observed

## Evidence
- Event ID 4624 (NTLM logon)
- Event ID 4104 (PowerShell script block)
- Event ID 7045 (service creation)
- Event ID 4672 (privileged token)
- Kerberos service ticket activity on DC

## Conclusion
Confirmed compromise with credential theft and domain escalation.

## Recommended Actions
- Isolate affected hosts
- Disable compromised accounts
- Reset domain credentials
- Block C2 infrastructure
- Escalate to IR
