## Wazuh Investigation
<img width="1366" height="768" alt="2026-06-18T23-06-57 849Z" src="https://github.com/user-attachments/assets/d76ba090-1816-4265-a44c-ee7353f7d1c9" />
<img width="1366" height="768" alt="2026-06-18T23-07-55 154Z" src="https://github.com/user-attachments/assets/16cc94c8-4b6e-4e1e-abdb-4f448048a079" />
<img width="1366" height="768" alt="Screenshot 2026-06-19 130726" src="https://github.com/user-attachments/assets/cd604927-ad10-4230-bae5-dac085640e21" />

# Windows Event ID 4625 - Failed Logon Investigation (Valid Account, Wrong Password)

## Objective

Investigate failed logons from a valid account but wrong or incorrect passwords.

## Alert Details

- Event ID: 4625 
- IP: Localhost::1
- Target Account: TestUser
- Failure Reason: Incorrect Password or Bad Password
- Total Attempts: 10
- Timeframe: 39 Seconds

## Investigation 

Multiple authentication attempts were detected from a localhost IP targeting account TestUser. A total of 10 failed logon attempts occurred within the timeframe of 39 seconds.
No successful logon was observed from this IP.

This pattern suggests possible brute force activity. This may also be behavior of password spraying.

This activity is not high risk because it comes from a local host.
The account should be reviewed for further successful attempts because of the volume of logons within the timeframe.

Recommend monitering the IP for further attempts.
Recommend looking up previos successful logons from this IP.


