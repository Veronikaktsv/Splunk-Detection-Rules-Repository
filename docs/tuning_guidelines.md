# Tuning guidelines

- Start with low frequency (daily/hourly) and tighten thresholds gradually.
- Whitelist legitimate management tools (PSExec, SCCM, Intune) where necessary.
- Add context enrichment (asset tags, criticality, owner) to prioritize alerts.
- Test searches against a representative historical dataset before enabling real-time alerts.
