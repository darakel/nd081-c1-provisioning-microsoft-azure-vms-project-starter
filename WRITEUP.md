# Write-up Template

### Analyze, choose, and justify the appropriate resource option for deploying the app.

*For **both** a VM or App Service solution for the CMS app:*

- *Analyze costs, scalability, availability, and workflow*
- *Choose the appropriate solution (VM or App Service) for deploying the app*
- *Justify your choice*

### Assess app changes that would change your decision.

*Detail how the app and any other needs would have to change for you to change your decision in the last section.*



When you consider the cost, scalability, availability, and workflow of the app, you come to the conclusion that App Service is the better choice. To explain this decision in detail, we need to take a closer look at the individual points and the dependencies.

Scalability: Both App Service and VM can be scaled automatically. Therefore, this point is irrelevant if you look at it alone.
Availability: If we look at availability alone, VMs with an SLA of 99.99% are better than an APP service, which guarantees an SLA of 99.95%.
Workflow: Since both App Service and VMs provide the functions required for this app, this point is also irrelevant in itself.
Costs: If you look purely at the Azure costs, we would be in a productive scenario (50 GB storage and up to 10 instances) with the app service ~ 0.085 € / h (standard). A VM costs € 0.0043 / h alone (general Av2). However, to have a failure safety, you need at least 2 VMs. There are also costs for the data transfer.
If you also look at the maintenance and servicing of the various systems, it quickly becomes clear that App Service is the more cost-effective choice.

**When would the choice be different?**
As soon as the circumstances of the request for the app change significantly. Or a planned change requires certain services that are not supported out of the box by App Services. It would be a reason to reconsider the choice.
External influences such as security concerns on the part of the customer or possibly other requirements (e.g. GDPR) would affect the choice.
