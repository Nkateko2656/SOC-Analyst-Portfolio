# Event 4688
<img width="1366" height="768" alt="Screenshot (22)" src="https://github.com/user-attachments/assets/9801f56e-c005-4533-a5a8-e58c4d756388" />

##Alert: 

Event ID 4688 - Process creation

##Investigation: 
Reviewed process creation event. Event ID 4688 was launched by splunk-optimize.exe under the NT SERVICE\Splunkd acccount.

## Findings 

Activity is legitimate with consistent behaviour.

## Justification

splunk-optimize.exe is a legitimate splunk maintenance process used to optimize indexes
which are expected to run under the NT SERVICE\Splunkd account.

## Disposition

Benign - No further action required. A new process has been created as part of splunks normal operations.

