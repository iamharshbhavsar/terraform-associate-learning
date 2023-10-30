
# Terraform Provisioners
* Terraform Provisioners will install software, edit files and provision machines created with Terraform. It will allow different methods:
<br>
1. Cloud-Init:
    * Cloud-Init is an industry standard for cross-platform cloud instance initializations. When a VM is launch on a Cloud Service Provider (CSP), you will provide a YAML or bash script. 
<br>
2. Packer:
    * Packer is an automated image-builder service. You provide a configuration file to create and provision the machine image and the image is the delivered to a repository for use.
<br>
3. Local-Exec:
    * Local-exec allows you to execute local commands after a resource is provisioned.
    For ex: Local-Machine, Build Server (GCP Cloud Build, AWS CodeBuild, Jenkins), Terraform Cloud Run Environment.
<br>
4. Remote-Exec:
    * Remote-exec allows you to execute commands on a target resource after resource is provisioned. It is useful for provisioning a Virtual Machine with a simple set of commands.
<br>
5. File:
    * **File-Provisioner** is used to copy files or dictories from our local machine to the newly created resource.
<br>
6. Connection:
    * A **Connection** tells a provisioner or resource how to establish a connection.
<br>
7. Null Resources:
    * **null_resources** is a placeholder for resources that have no specific association to a provider resources. Triggers is a map of values which should cause this set of provisioners to re-run.
<br>
8. Terraform-Data:
    * Similar to `null_resources` but does not require or the configuration of a provider.

## Terraform Providers
* Providers are Terraform Plugins that allow you to interactive with:
    * Cloud Service Providers (CSP), eg: AWS, Azure, GCP
    * Software-as-a-Service (SaaS), eg: GitHub, Angoliam Stripe.
    * Other APIs eg: Kubernetes, Postgres.
* Providers are  distrubted sperately from Terraform and the plugins must be downloaded before use. `terraform init` will download the necessary provider plugins listed in Terraform configuration file.

## Terraform Registry
* [Terraform Registry](https://registry.terraform.io) is a website portal to browse, download or publish available Providers or Modules.

    * Provider: A Provider is a plugin that is mapping to a Cloud Service Provider (CSP) APIs.
    * Module: Module is a group of configuration files that provide common configuration functionality.

## Terraform Cloud - Private Registry
* **Terraform Cloud** allows you to publish private modules for your organization with the Terraform Cloud Private Registry.
* When creating module you need to connect to a Version Control System (VCS) and choose a Repository.

## Terraform Modules
* A Terrform Module is a group of configuration files that provide common configuration functionality.
    * Enforces best practices
    * Reduce the amount of code
    * Reduce time to develop scripts
