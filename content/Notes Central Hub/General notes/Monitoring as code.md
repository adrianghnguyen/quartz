---
dg-publish: true
aliases: Monitoring as code, Checkly, monitoring as code, MaC
file-created: 2023-03-15
file-modified: 2023-05-05
tags: [computer-science/programming, engineering/infrastructure, computer-science/software-engineering]
linter-yaml-title-alias: Monitoring as code
---

# Monitoring as code

#status/done

---

## What is Monitoring as Code?

It's similar to [[infrastructure as code]].

> [!ai] AI
>
> Monitoring as code is an approach to monitoring in which the monitoring configurations and rules are written as code instead of being manually configured through a graphical user interface or command line interface. This code can be version-controlled, tested, and deployed alongside application code, making it easier to manage and maintain monitoring across multiple environments. It also promotes collaboration between development and operations teams, as they can work together on defining the monitoring requirements and configurations. Overall, monitoring as code helps organizations improve their observability and quickly identify issues in their applications or infrastructure.

### Why Do We Use Monitoring as Code?

> [!ai] AI
>
> There are several reasons why we use monitoring as code:
>
> 1. Automation: Monitoring as code allows us to automate the monitoring process, which saves time and reduces the risk of human error.
> 2. Consistency: With monitoring as code, we can ensure that monitoring is consistent across all environments and applications.
> 3. Collaboration: By defining monitoring as code, we can collaborate more effectively with other teams such as development, operations, and security.>
> 4. Version control: Monitoring as code allows us to version control our monitoring configurations and changes over time, making it easier to track changes and roll back if necessary.
> 5. Scalability: As our systems grow in complexity and scale, monitoring as code allows us to manage and scale our monitoring infrastructure more efficiently.

## Monitoring the IaC way

It takes the declarative principles of infrastructure as code and applies it to monitoring or making sure that the website works correctly.

> Setting up monitoring can present some of the same issues as provisioning infrastructure. This becomes apparent when we move past the initial rollout or proof-of-concept and onboard multiple products and/or teams, and see our monitoring setup rapidly grow in scope - along with its maintenance needs, that is.
>
> Monitoring-as-Code learns from IaC and brings your **monitoring config closer to your application and your development workflows**. How? By having it also declared as code, much like you would do with any kind of IT infrastructure.^[https://www.checklyhq.com/guides/monitoring-as-code/]

## How Am I Using [[Monitoring as code|MaC]] with Checkly

For my project on [[Implementing CI-CD on my digital garden|implementing CI/CD in my digital garden]]], I'm planning on using [[Checkly|Checkly]] as it integrates into [[Vercel]].
