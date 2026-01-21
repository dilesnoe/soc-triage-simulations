# Incident 01 – Timeline

**T0 – Initial Access**
- Interactive logon to WS-21 using compromised credentials (`a.chen`)

**T1 – Execution**
- PowerShell executed with obfuscation
- External script downloaded and executed

**T2 – Persistence**
- Malicious service `AgentUpdate` installed and configured for auto-start

**T3 – Credential Access**
- LSA memory accessed
- Credentials harvested from WS-21

**T4 – Lateral Movement**
- NTLM authentication as `helpdesk.admin` to WS-22
- Administrative share accessed and remote service installed

**T5 – Domain Compromise**
- NTLM authentication to DC-01
- Kerberos service ticket activity observed
- Domain-level privileges confirmed

**T6 – Command and Control**
- Sustained outbound connections to external IPs
- Activity consistent with active C2 beaconing

