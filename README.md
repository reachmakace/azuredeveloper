# azuredeveloper
This repo contains the key points related to the Azure certification AZ-204

*Examine Azure App Service*
Azure App Service is an HTTP-based service for hosting web applications, REST APIs, and mobile back ends. The ability to scale up/down or scale out/in is baked into the Azure App Service.

**Built-in auto scale support** --> Scale In/Out or Scale Up/Down

**Container support** --> With Azure App Service, you can deploy and run containerized web apps on Windows and Linux. You can pull container images from a private Azure Container Registry or Docker Hub

**Continuous integration/deployment support** --> Source code can be from Azure DevOps Services, GitHub, Bitbucket, FTP, or a local Git repository on your development machine.

**Deployment slot:** When deploying a web app you can use a separate deployment slot instead of the default production slot when you're running in the Standard App Service Plan tier or better

**App Service on Linux**: App Service can also host web apps natively on Linux for supported application stacks. It can also run custom Linux containers (also known as Web App for Containers).  The languages, and their supported versions, are updated regularly. You can retrieve the current list by using the following command in the Cloud Shell (az webapp list-runtimes --os-type linux).

  **Limitations:**
    App Service on Linux isn't supported on Shared pricing tier.
    The Azure portal shows only features that currently work for Linux apps. As features are enabled, they're activated on the portal.
    When deployed to built-in images, it uses Content volumes supported by Azure storage. More latency
    When deployed using custom container image, it uses Container filesystem.

**Examine Azure App Service plans**
In App Service, an app always runs in an App Service plan. An App Service plan defines a set of compute resources for a web app to run. One or more apps can be configured to run on the same computing resources (or in the same App Service plan).

Each App Service plan defines:
 Operating System (Windows, Linux) 
 Region (West US, East US, etc.) 
 Number of VM instances 
 Size of VM instances (Small, Medium, Large) 
 Pricing tier (Free, Shared, Basic, Standard, Premium, PremiumV2, PremiumV3, Isolated, IsolatedV2) 

The pricing tier of an App Service plan determines what App Service features you get and how much you pay for the plan. There are a few categories of pricing tiers:

**Shared compute: ** Free and Shared, the two base tiers, runs an app on the same Azure VM as other App Service apps, including apps of other customers. These tiers allocate CPU quotas to each app that runs on the shared resources, and the resources can't scale out.
**Dedicated compute:** The Basic, Standard, Premium, PremiumV2, and PremiumV3 tiers run apps on dedicated Azure VMs. Only apps in the same App Service plan share the same compute resources. The higher the tier, the more VM instances are available to you for scale-out.
**Isolated:** The Isolated and IsolatedV2 tiers run dedicated Azure VMs on dedicated Azure Virtual Networks. It provides network isolation on top of compute isolation to your apps. It provides the maximum scale-out capabilities.

The App Service plan is the scale unit of the App Service apps. If the plan is configured to run five VM instances, then all apps in the plan run on all five instances. If the plan is configured for autoscaling, then all apps in the plan are scaled out together based on the autoscale settings.
