# Write-up Template

### Analyze, choose, and justify the appropriate resource option for deploying the app.

*For **both** a VM or App Service solution for the CMS app:*
- ***Analyze costs, scalability, availability, and workflow***
 
  **VM Cost Analysis;**
     1. **Pay for:** VM size (CPU, RAM), OS Disk, Networking (Load balancer, outbound traffic), **Always on cost** unless explicitly stopped, even when the app is idle, VM continues to accrue compute charges.
     2. **Cost implications:** Predictable but often higher baseline cost, hidden costs like patching effort, monitoring setup, backup configuration, security hardening.
     3. **Cost effective:** When you have ong running stable workloads, specialized compute needs and legacy apps that would be expensive to refactor.
  
  **App Service Cost Analysis:**
    1. **Pay for:** Shared compute (App service plan), Number od instances, Chosen SKU (Basic, Standard, Premium)
    2. **Cost implications:** Lower operational cost, better cost-to-value ratio for web/api workloads, easier to right size and downgrade
    3. **Cost effective when:** Web or API apps, variable or unpredictable traffic, teams want minimal ops cost
  
  **VM Scalability Analysis;**
    1. Powerful but complex, slower reaction to sudden traffic spikes, risk of over provisioning
  
  **App Service Scalability Analysis;**
    1. Fast automatic scaling, handles traffic spikes gracefully, zero infrastructure tuning

  **VM Availability Analysis;**
    1. Single VM (low availability), availability sets, availability zones, load balancer and scale sets.
    2. High availability is **achievable** but **entirely customer designed**.
  
  **App Service Availability Analysis;**
    1. Built-in redundancy within the App Service Plan, SLA baked into the platform, automatic instance replacement, zero downtime patching
       
   **VM Workflow Analysis;**
    1. This mirrors the **traditional on-prem workflow** and slows delivery cycles.
  
  **App Service Workflow Analysis;**
    1. App service is optimized for **modern DevOps and rapid iteration**
  
- *Choose the appropriate solution (VM or App Service) for deploying the app*
   1. I chose App service as never have setup a VM and not very familiar with CLI and how to use it. So it was easier for me to do the app service.
  
- ***Justify your choice***
  1. App service generally wins on **total cost of ownership** unless VM level control is required
  2. App service is superior for elasticity and operational simplicity
  3. App service delivers higher default availability with less effort
     
### Assess app changes that would change your decision.

*Detail how the app and any other needs would have to change for you to change your decision in the last section.* 
- If there is requirement for security or the app becomes a long running stable worklaod then I would think about moving to a VM.
