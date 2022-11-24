# Write-up Template

### Analyze, choose, and justify the appropriate resource option for deploying the app.

*For **both** a VM or App Service solution for the CMS app:*
- *Analyze costs, scalability, availability, and workflow*
- *Choose the appropriate solution (VM or App Service) for deploying the app*
- *Justify your choice*

### Costs
- Virtual Machines are more expensive.
- App Service is less expensive although you are charged even if the application or services aren't running
- App Service supports different tiers/costs bases on the development,test, production and isolated workloads.

### Scalability
- Virtual Machines can be horizontally scaled by using either load balancers or virtual machine scale sets.
- Azure App service provides auto scaling support both for Horizontal and Vertical Scaling although there are hardware limitations that allows you use only 4 VCPU's and 15 GB of RAM in a single app service instance.

### Availability
- Azure App Service is highly available with an SLA of 99.95%.
- Availablilty in virtual machines can be achieved by deploying more than 1 of them.

### Workflow
- Deploying an app to virtual machine involves creating a new virtual machine in Azure, configuring it with the underlying operating system, installing a web server like nginx, configuring firewall rules, installing the necessary dependencies and finally running the application.
- Deploying an app to App Service is comparatively easy because azure abstracts away most of the underlying infrastructure work from the developer. 
- It provides Continuous deployment model using GitHub, Azure DevOps, or any Git repo.

I choose to deploy the Article CMS Application to Azure App Service and the following are my reasons behind it:
- They are less expensive compared to Virtual Machines.
- It is relatively easy to deploy the application to an App Service.
- Current application scaling requirements fit well with in the App Service Plans.
- High availability with a service-level agreement (SLA)-backed uptime of 99.95 percent.

### Assess app changes that would change your decision.

*Detail how the app and any other needs would have to change for you to change your decision in the last section.* 

I would change my decision if any of the following conditions are met:
- If we hit the hardware limitations of the app service and the application becomes no longer scalable.
- If the application is migrated and rewritten in a different programming language which is not yet supported by the App Service.
- Regulatory and compliance requirements mandating to have access to the underlying operating system.

