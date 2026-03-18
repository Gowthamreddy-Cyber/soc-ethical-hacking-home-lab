# Splunk Detection

## Failed Login Detection
index=security EventCode=4625
| stats count by src_ip
| where count > 5

## Suspicious Activity
index=security
| stats count by user, src_ip
