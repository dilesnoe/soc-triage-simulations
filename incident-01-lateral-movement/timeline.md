# Incident 01 – Timeline

## Timeline of Events

**T0 – Initial Access**
- WS-21 authenticated using reused NTLM credentials (user: a.chen)

**T1 – Execution**
- Obfuscated PowerShell executed
- External script downloaded (a.ps1)

**T2 – Persistence**
- Malicious service AgentUpdate installed on WS-21

**T3 – Credential Access**
- agent.exe accessed LSA on WS-21 (Event IDs 4656 / 4663)
- LSA accessed, credentials dumped

**T4 – Lateral Movement**
- NTLM authentication as helpdesk.admin to WS-22
- Administrative share (C$) accessed with write permissions

**T5 – Domain Compromise**
- NTLM authentication to DC-01
- Kerberos service ticket (krbtgt) observed
- Domain-level privileges assigned

**T6 – Command and Control**
- Outbound connections to multiple external IPs
