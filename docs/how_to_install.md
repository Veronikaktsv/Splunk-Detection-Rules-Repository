# How to install these rules in Splunk

1. Copy `savedsearches.conf` into `$SPLUNK_HOME/etc/apps/<your_app>/local/`.
2. Restart Splunk (or reload saved searches via Splunk web).
3. Import dashboard XML via Splunk > Dashboards > Create New > Source.
4. Verify alert actions and SMTP/webhook settings.
