## Wazuh Investigation
<img width="1366" height="768" alt="608892111-a7529a12-0bf7-40bd-8f73-4d8d3174a0a9" src="https://github.com/user-attachments/assets/537c5c55-a072-405d-a860-9dbc785aec57" />
<img width="1366" height="768" alt="608892077-ca32de22-2a64-4cc6-96ef-292503969c4f" src="https://github.com/user-attachments/assets/003867ef-8a73-460c-a914-fa4980358500" />
<img width="1366" height="768" alt="608892035-6cccdbaa-fd25-4346-825b-b1b4ea0a256d" src="https://github.com/user-attachments/assets/cd0ea6ca-24fd-488b-9597-cd8f5627ec56" />

# Windows Event ID 4625 - Failed Logon Investigation

## Objective

Investigate a Windows Event and determine whether this was a failed logon attempt or a false positive.

## Alert Details 

- Event ID: 4625
- IP: 192.168.0.231
- TargeT Account: Fakeuser
- Failure Reason: Unknown username or password

## Investigation 

Multiple authentication attempts were detected from IP 192.168.0.231 targeting account Fakeuser. A total of 10 failed logon attempts
occurred within the timeframe of 35 seconds.
No successful logon was observed from this IP.

An analysis of security event ID 4625 indicates failed logon attempts with status 0xc000006d and subStatus 0xc0000064,
which signifies that the specified user account does not exist. The overall risk is considered low at this time.

The attempts originate from the localhost::1, this suggests that the authentication requests were locally generated rather than
remote external source.

Futher investigation is recommended to determine whether these events were caused by user error,
misconfigured software, scheduled tasks or unauthorized account enumeration activity.

