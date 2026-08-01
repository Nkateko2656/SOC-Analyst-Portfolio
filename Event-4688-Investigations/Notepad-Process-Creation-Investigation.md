# Alert: Event ID 4688 - Process creation

## Investigation

Reviewed process creation event. Event ID 4688 was launched by Notepad.exe under the SYSTEM account.

## Findings

The activity is legitimate with consistent behaviour.

## Justification

Notepad.exe is a legitimate FIRSTBLACKGUYON$ maintenance process used to optimize indexes which are expected to run under the SYSTEM account as part of normal operation account.

## Disposition

Benign - No further action is required. A new process was created as part of FIRSTBLACKGUYON$ normal operations.
