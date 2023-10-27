### Day 0 (22/10)

* Start preparation for the associate examination.

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
