What can we really build using only an Azure Free Subscription?
Starting a small series based on hands-on labs I’ve been building recently.

Part 1 — Observability & Monitoring Lab

Built an end-to-end Azure observability setup integrating:

- Azure Monitor
- Log Analytics Workspace
- Azure Monitor Agent (AMA)
- Azure Alerts + Action Groups
- Activity Log ingestion
- KQL-based operational analytics
- Azure Workbooks
- VNet Flow Logs
- Traffic Analytics
- RBAC audit tracking

Lab resources included:

- law-shiva-monitoring
- hub-vnet
- spoke1-vnet
- spoke2-vnet
- shiva-vnet-WestEurope
- vm-web
- shiva-vm-web1

A few things I specifically wanted to validate:

✔ Centralized telemetry collection
✔ Subscription Activity Log ingestion into LAW
✔ KQL queries for operational/security visibility
✔ Memory alerting with Action Groups
✔ Workbook-based dashboards
✔ East-West traffic visibility using Traffic Analytics
✔ RBAC audit trail correlation

The interesting part was seeing how quickly operational visibility improves once logs from compute, subscription activity, and network layers start converging into a single workspace.

Also validated practical troubleshooting scenarios:

- storage key regeneration audit tracking
- role assignment visibility
- failed operations analysis
- network flow validation between VNets/VMs

Coming from a traditional infrastructure/storage operations background, it’s been interesting mapping enterprise operational thinking into cloud-native observability workflows.


***********************  Part 2 — Azure Site Recovery (ASR) & DR Failover Validation *****************************

This week I focused on building and testing a practical Disaster Recovery workflow using Azure Site Recovery (ASR).
The objective was not just enabling replication — but validating whether an actual failover scenario could be operationally recovered and troubleshooted end-to-end.
Lab activities included:
Azure Site Recovery configuration
Cross-region VM replication
Recovery Services Vault integration
Test Failover execution
Boot Diagnostics validation
Serial Console troubleshooting
NSG verification during DR testing
Recovery VM validation after failover
One of the most useful parts of the lab was understanding how DR testing quickly moves beyond “replication succeeded” into operational troubleshooting territory.
A few practical validations performed during failover testing:
✔ VM replication health monitoring
✔ Test Failover to DR region
✔ Boot diagnostics log analysis
✔ Serial console access validation
✔ Network/NSG verification during recovery
✔ Post-failover VM accessibility testing
✔ Recovery cleanup operations
Interesting observation:
Even in cloud-native DR workflows, the fundamentals remain the same as traditional datacenter operations:
recovery validation
dependency checks
network accessibility
boot troubleshooting
operational readiness
The tooling changes. The operational thinking does not.
Coming from enterprise infrastructure and BCDR operations background, this lab was a good bridge between traditional DR concepts and Azure-native recovery workflows.
