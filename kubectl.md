# List usinnovation pods with tags

Input:

```bash
kubectl get pods -o json | jq '[.items[].spec.containers[].image | select(contains("innovation")) | .[25:]] | unique'
```
Output:

```
[
  "analytics-ui:1.2.45",
  "auditlog-service:1.1.4",
  "autoscaling-service:1.1.22",
  "bundle-service:1.1.61",
  "client-service:1.1.38",
  "convert-service:1.1.7",
  "corptax:0.3.56",
  "datarequest-service:1.1.77",
  "engagement-service:1.1.47",
  "excel-csv-converter-service:0.2.11",
  "extraction-ui:1.1.60",
  "informatica-service:1.1.32",
  "notification-service:1.1.41",
  "prep-orchestrator-service:12310",
  "preparation-service:1.1.8",
  "sap-service:1.2.6",
  "scheduler-service:1.1.12",
  "security-service:1.1.19",
  "sftp-service:1.1.6",
  "spark-ssh:0.1.5",
  "staging-service:1.1.67",
  "tableau-api:1.1.26",
  "workpaper-service:1.1.33"
]
```
