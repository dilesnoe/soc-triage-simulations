# Incident 02 – Timeline

**T0 – Initial Authentication**
- Interactive logon on WS-18 using account `temp.admin`

**T1 – Failed Network Authentication**
- NTLM network authentication attempts from WS-18 to WS-25 failed

**T2 – Administrative Share Access Attempt**
- Attempted access to `\\WS-25\ADMIN$`
- Access denied

**T3 – Execution Attempt**
- `net.exe` executed on WS-25, consistent with share or credential validation activity

**T4 – Additional Credential Testing**
- Failed NTLM authentication attempt using `administrator` account

**T5 – Outcome**
- No successful authentication
- No persistence established
- No lateral movement achieved
- Incident classified as attempted but blocked

