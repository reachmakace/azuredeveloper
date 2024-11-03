# azuredeveloper
This repo contains the key points related to the Azure certification AZ-204

*Examine Azure App Service*
Azure App Service is an HTTP-based service for hosting web applications, REST APIs, and mobile back ends. The ability to scale up/down or scale out/in is baked into the Azure App Service.
**Built-in auto scale support** --> Scale In/Out or Scale Up/Down
**Container support** --> With Azure App Service, you can deploy and run containerized web apps on Windows and Linux. You can pull container images from a private Azure Container Registry or Docker Hub
**Continuous integration/deployment support** --> Source code can be from Azure DevOps Services, GitHub, Bitbucket, FTP, or a local Git repository on your development machine.
**Deployment slot:** When deploying a web app you can use a separate deployment slot instead of the default production slot when you're running in the Standard App Service Plan tier or better
**App Service on Linux**: App Service can also host web apps natively on Linux for supported application stacks. It can also run custom Linux containers (also known as Web App for Containers).  The languages, and their supported versions, are updated regularly. You can retrieve the current list by using the following command in the Cloud Shell (az webapp list-runtimes --os-type linux)
  Limitations:
    App Service on Linux isn't supported on Shared pricing tier.
    The Azure portal shows only features that currently work for Linux apps. As features are enabled, they're activated on the portal.
    When deployed to built-in images, it uses Content volumes supported by Azure storage. More latency
    When deployed using custom container image, it uses Container filesystem.
