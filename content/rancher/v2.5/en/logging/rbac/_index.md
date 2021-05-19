---
shortTitle: Role-based Access Control
title: Role-based Access Control for Logging
weight: 3
---

Rancher logging has two roles, `logging-admin` and `logging-view`.

- `logging-admin` gives users full access to namespaced flows and outputs
- `logging-view` allows users to *view* namespaced flows and outputs, and cluster flows and outputs

> **Why choose one role over the other?** Edit access to cluster flow and cluster output resources is powerful. Any user with it has edit access for all logs in the cluster.

In Rancher, the cluster administrator role is the only role with full access to all `rancher-logging` resources. Cluster members are not able to edit or read any logging resources. Project owners and members have the following privileges:

Project Owners | Project Members
--- | ---
able to create namespaced flows and outputs in their projects' namespaces | only able to view the flows and outputs in projects' namespaces
can collect logs from anything in their projects' namespaces | cannot collect any logs in their projects' namespaces

Both project owners and project members require at least *one* namespace in their project to use logging. If they do not, then they may not see the logging button in the top nav dropdown.