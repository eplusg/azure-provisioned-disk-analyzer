# Azure Provisioned Disk Usage Analyzer Workbook

This Azure workbook helps you identify and analyze unused disk space across your subscriptions. It highlights the provisioned disk size versus the actual tier size being billed, enabling you to optimize costs by identifying disks with significant unused capacity. 

### Key Features:
- **Subscription Filtering**: View disk usage across selected subscriptions.
- **Unused Disk Analysis**: Identify disks with unused capacity above a certain threshold.
- **Cost Optimization Insights**: Pinpoint opportunities to reduce costs by resizing or decommissioning unused disk space.

### Note:
Disks with names containing -ASRReplica are ignored. These are typically associated with Azure Site Recovery (ASR) replication and are not included in the analysis.
The query also filters out disks where the size difference between the provisioned size and the tier size is less than or equal to 1 GiB (or 2 GiB in some parts of the query). Only disks with a larger size difference are included.

![Screenshot 2024-12-05 at 13 00 21@2x](https://github.com/user-attachments/assets/8d54eab4-8155-484d-8073-f8e35a837924)
