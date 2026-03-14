# Example KQL Queries

## Failed Login Attempts
SecurityEvent
| where EventID == 4625
| summarize count() by Account, IPAddress


## Unusual Login Times


SecurityEvent
| where EventID == 4624
| where TimeGenerated between (datetime(2024-01-01 00:00) .. datetime(2024-01-01 05:00))
