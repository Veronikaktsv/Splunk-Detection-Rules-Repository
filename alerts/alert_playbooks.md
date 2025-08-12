# Alert Playbooks

## PowerShell Encoded Command - Playbook
1. Triage: Identify source host, user, and parent process.
2. Containment: Isolate host if multiple detections or high confidence.
3. Investigation: Pull process tree, command line, network connections, and scheduled tasks.
4. Remediation: Remove malicious scripts, disable persistence, reset credentials if necessary.

## LSASS Access - Playbook
1. Triage: Confirm lsass access events and correlate with process command line.
2. Capture memory image (forensic) if permitted.
3. Identify lateral movement indicators.
4. Reset privileged credentials and rotate keys if compromise confirmed.
