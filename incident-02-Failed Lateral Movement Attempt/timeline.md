# Incident 02 – Timeline

## Timeline of Events

**T0 – Initial Authentication**
- WS-18 authenticated with an interactive logon (Logon Type 2)
- Account: `temp.admin`

**T1 – Failed Network Authentication**
- NTLM network logon attempt from WS-18 to WS-25 failed
- Account: `temp.admin` (Event ID 4625)

**T2 – Administrative Share Access Attempt**
- Attempted access to administrative share `\\WS-25\ADMIN$`
- Access denied (Event ID 5145)

**T3 – Execution Attempt**
- `net.exe` executed on WS-25 under `temp.admin`
- Activity consistent with share or credential validation attempt

**T4 – Additional Failed Authentication**
- Failed NTLM network logon attempt using account `administrator`
- No authenticated session established

**T5 – Outcome**
- No successful authentication
- No persistence established
- No lateral movement achieved
- Incident classified as attempted but unsuccessful lateral movement
