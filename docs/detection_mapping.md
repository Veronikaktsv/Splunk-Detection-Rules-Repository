# Detection Rules to MITRE & Playbook Mapping

This table maps each Splunk detection rule in this repository to its MITRE ATT&CK technique, the related dashboard panels, and the corresponding alert playbook.

| Rule Name                                      | MITRE ATT&CK ID | Dashboard Panel(s)                | Playbook File                                   |
|------------------------------------------------|-----------------|------------------------------------|-------------------------------------------------|
| Suspicious PowerShell Encoded Command          | **T1059.001**   | `Top Detections`                   | [PowerShell Encoded Command](../alerts/alert_playbooks.md#powershell-encoded-command---playbook) |
| LSASS Access Detection                         | **T1003**       | `Top Detections`                   | [LSASS Access](../alerts/alert_playbooks.md#lsass-access---playbook) |
| Excessive Failed Logons                        | **T1110**       | `Authentication Failures`          | *Playbook not yet defined — recommend adding*   |
| Unusual Process Execution from Temp Directory  | **T1204**       | `Unusual Process Activity`          | *Playbook not yet defined — recommend adding*   |
| Multiple Malware Alerts on Same Host           | **T1059 / T1204** | `Malware Summary`                  | *Playbook not yet defined — recommend adding*   |
| High Volume Data Transfer to External IP       | **T1048**       | `Data Exfiltration`                 | *Playbook not yet defined — recommend adding*   |

---

## Notes
- **Playbooks**: All defined playbooks are located in the [`alerts/alert_playbooks.md`](../alerts/alert_playbooks.md) file.
- **MITRE IDs**: These are based on the [MITRE ATT&CK](https://attack.mitre.org/) framework for consistent SOC mapping.
- **Dashboards**: The panels listed correspond to those in the `dashboards/` folder.
- **Next Steps**: Add missing playbooks for rules without documented responses.
