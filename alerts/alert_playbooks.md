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

## Excessive Failed Logons - Playbook
1. Triage: Review user account and source IP for suspicious patterns.
2. Containment: Temporarily lock the account if threshold exceeded.
3. Investigation: Check for brute-force tools or unusual login times.
4. Remediation: Reset credentials, enable MFA, and notify the user.

## Unusual Process Execution from Temp Directory - Playbook
1. Triage: Identify the process name, user, and parent process.
2. Containment: Isolate host if malicious indicators found.
3. Investigation: Analyze the script or executable for malicious behavior.
4. Remediation: Remove files, block hash/signature, update endpoint protection.

## Multiple Malware Alerts on Same Host - Playbook
1. Triage: Correlate alerts to confirm true positive.
2. Containment: Quarantine affected host.
3. Investigation: Review malware types, infection vectors, and lateral movement.
4. Remediation: Run full antivirus/malware scans, patch vulnerabilities, and restore clean backups.

## High Volume Data Transfer to External IP - Playbook
1. Triage: Identify destination IP, data volume, and affected host.
2. Containment: Block suspicious external IP at firewall or network level.
3. Investigation: Analyze transferred data type and user activity.
4. Remediation: Review and tighten data access policies, notify data owners, and escalate incident response.

