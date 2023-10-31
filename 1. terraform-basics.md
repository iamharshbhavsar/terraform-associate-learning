## What is Infrastructure-as-Code(IaC)?
IaC is a blueprint of the infrastructre.
IaC allows to easily <b>share, version or inventory</b> the cloud infrstaruture.


## Popular IaC Tools

<br>

<table>
    <thead>
        <tr>
            <th>Declarartive</th>
            <th>Imperative</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Infrastructre will be created which is declared <i>Explicit</i></td>
            <td>You say that you want, rest is filled up <i>Implicit</i></td>
        </tr>
        <tr>
            <td>Scripting languages used: JSON, YAML, XML</td>
            <td>Programming languages used: Python, Ruby, Javascript</td>
        </tr>
        <tr>
            <td>Azure ARM Template</td>
            <td rowspan=2>AWS CDK (Cloud Development Kit)</td>
        </tr>
        <tr>
            <td>AWS Cloudformation</td>
        </tr>
        <tr>
            <td>Google Cloud Deployment Manager</td>
           <td rowspan=2>Pulumi supports AWS, Azure, GCP, Kubernetes</td>
        </tr>
        <tr>
            <td>Terraform</td>
        </tr>
    </tbody>
</table>

## Infrastructure Lifecycle
* **Reliabilty:** IaC makes changes idempotent, consistent, repeatable and predictable.
* **Idempotent:** No matter how many times you ran IaC, it will always end up with the same state as expected.
* **Manageability:** enable mutation via code, revised with minimal changes.

## Provising | Deplyment | Orchestration
**1. Provisioning:** To prepare server with systems, data and software and make it ready for network operation. Popular configuration tools like Puppet, Ansible, Chef, Bash scripts, PowerShell and Cloud-Init.
> When a VM is launched and configured is called "Provisioning"

**2. Deployment:** Deployment is act of delivering a version of your application to run a provisioned server. Deployment could be performed via AWS CodePipeline, Harness, Jenkins, GitHub Actions, CircleCI.
    
**3. Orchestration:** Orchestration is the act of coordinating multiple systems or services. It is a common term when working with microservices, containers and Kubernetes. Orchestration could be Kubernetes, Salt.

## Terraform Lifecycle

<img src="https://i.ibb.co/NVXC3r0/terraform-lifecycle.png" alt="terraform-lifecycle" border="3">


## Visualizing Terraform Execution Plan
You can **visualize execution plan** as a graph using terraform graph command, it will provide output a `GraphViz` file. For there you have to install GraphViz to view the graph. For more information check from [here.](https://developer.hashicorp.com/terraform/cli/commands/graph)

The output of terraform graph is in the DOT format, which can easily be converted to an image by making use of dot provided by GraphViz:

```hcl
$ terraform graph | dot -Tsvg > graph.svg
```


## Terraform Use-cases
* Iac for Exotic Providers: Terraform supports a variety of providers outside of GCP, AWS, Azure and sometimes is the only provider. Terraform is open-source an extendable so any API could be used to create laC tooling for any kind of cloud platform or technology. E.g. Heroku, Spotify Playlists.

* Multi-Tier Applications: Terraform by default makes it easy to divide large and complex applications into isolate configuration scripts (module). It has a complexity advantage over cloud-native laC tools for its flexibility while retaining simplicity over Imperative tools.

* Disposable Environments: Easily stand up an environment for a software demo or a temporary development environment

* Resource Schedulers: Terraform is not just defined to infrastructure of cloud resource but can be used to dynamic schedule Docker containers, Hadoop, Spark and other software tools. You can provision your own scheduling grid.

* Multi-Cloud Deployment: Terraform is cloud-agnostic and allows a single configuration to be used to manage multiple providers, and to even handle cross-cloud dependencies.

## Terraform Core & Terraform Plugins
1. Terraform Core
    * Uses remote procedure calls (RPC) to communicate with Terraform PLugins
2. Terraform Plugins
    * expose an implementation for a specific service, or provisioner.

<img src='https://developer.hashicorp.com/_next/image?url=https%3A%2F%2Fcontent.hashicorp.com%2Fapi%2Fassets%3Fproduct%3Dterraform-docs-common%26version%3Drefs%252Fheads%252Fmain%26asset%3Dwebsite%252Fimg%252Fdocs%252Fterraform-plugin-overview.png%26width%3D4096%26height%3D728&w=3840&q=75' border='3'>
