# Rules catalog

## Suspicious PowerShell Encoded Command
- **MITRE**: T1059.001 (PowerShell)
- **Description**: Detects PowerShell executions containing encoded commands or suspicious flags that commonly indicate obfuscation or download-execute patterns.
- **Use case**: Detects fileless payloads, initial access via malicious scripts, and attacker post-exploitation activities.
- **False positives**: Legitimate automation scripts; tune by whitelisting known hosts/users and excluding enterprise management tools.
- **Tuning**: Increase threshold, add filters for trusted PVAs, or match to ParentImage.

## Unusual Parent-Child Process Relationship
- **MITRE**: T1059.003 (cmd.exe)
- **Description**: Alerts when cmd.exe is launched by an unusual parent process (e.g., Word, Excel) — common for macro-based attacks.
- **Use case**: Detect macro-based execution or lateral movement using shell.
- **False positives**: Admin scripts executed by orchestration tools; whitelist accordingly.

## LSASS Access
- **MITRE**: T1003 (Credential dumping)
- **Description**: Monitors for ProcessAccess events targeting lsass.exe indicating attempts to access LSASS memory.
- **Use case**: Detect credential dumping tools (Mimikatz) and suspicious memory access.
- **Tuning**: Correlate with process command lines, source host reputation, or volume of access.
