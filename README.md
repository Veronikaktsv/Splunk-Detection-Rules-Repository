# Splunk-Detection-Rules-Repository

# Splunk Detection Rules Repository

A curated repository of Splunk detection rules, ready to import into Splunk Enterprise or Splunk Cloud. This repo is intended for SOC teams and security engineers to detect common adversary behaviors, map to MITRE ATT&CK, and provide documentation for tuning and alerting.

## Contents
- `rules/` — savedsearches.conf and individual query files
- `dashboards/` — Simple XML dashboards to visualize detections
- `alerts/` — playbooks and example alert actions
- `docs/` — installation and tuning guidance

## Quickstart
1. Review rules in `rules/rules_catalog.md` and tune thresholds to your environment.
2. Import `rules/savedsearches.conf` into Splunk's `etc/apps/your_app/local/` folder or add saved searches via the UI.
3. Import dashboards (`dashboards/*.xml`) via Splunk UI: Dashboards > Create New Dashboard > Source and paste XML.
4. Configure alert actions (email, webhook, notable) in Splunk for critical searches.

## Contributing
- Add new searches to `rules/queries/` and update `rules/rules_catalog.md` with use case & tuning notes.
- Test queries on historical logs and include example events in `sample_events/` (optional).

## License
This project is licensed under the [MIT License](LICENSE).
