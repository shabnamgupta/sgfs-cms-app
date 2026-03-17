# Write-up Template

### Analyze, choose, and justify the appropriate resource option for deploying the app.

*For **both** a VM or App Service solution for the CMS app:*
- *Analyze costs, scalability, availability, and workflow*
-   VM Cost Analysis -
-     Pay for: VM size (CPU, RAM), OS Disk, Networking (Load balancer, outbound traffic), **Always on cost** unless explicitly stopped, even when the app is idle, VM continues to accrue compute charges
-     Cost implications: Predictable but often higher baseline cost, hidden costs like patching effort, monitoring setup, backup configuration, security hardening
-     Cost effective: When you have ong running stable workloads, specialized compute needs and legacy apps that would be expensive to refactor
-   App Service -
-     Pay for: Shared compute (App service plan), Number od instances, Chosen SKU (Basic, Standard, Premium)
-     Cost implications: Lower operational cost, better cost-to-value ratio for web/api workloads, easier to right size and downgrade
-     Cost effective when: Web or API apps, variable or unpredictable traffic, teams want minimal ops cost
- *Choose the appropriate solution (VM or App Service) for deploying the app*
- *Justify your choice*

### Assess app changes that would change your decision.

*Detail how the app and any other needs would have to change for you to change your decision in the last section.* 
