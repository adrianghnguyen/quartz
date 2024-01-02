---
dg-publish: true
aliases: Continuous integration and deployment, CI pipeline, continous deployment, continuous integration, CI/CD, continuous integration, continous deployment
file-created: 2023-03-01
file-modified: 2023-05-05
tags: [computer-science/programming, computer-science, computer-science/software-engineering, computer-science/software-engineering]
note-type: general
linter-yaml-title-alias: Continuous integration and deployment
---

# Continuous integration and deployment

#status/wip

---

## What is continuous integration and continuous deployment?

> [!info] Also known as CI/CD

> [!ai] AI
>
> Continuous integration (CI) and continuous deployment (CD) are two related software development practices that aim to streamline the process of building, testing, and deploying software.
>
> Continuous integration is the practice of regularly merging code changes from multiple developers into a shared repository. This allows for early detection of bugs or conflicts between different code changes, which can then be resolved before they cause larger problems.
>
> Continuous deployment takes this process one step further by automating the deployment of new code changes to production environments as soon as they pass all tests and checks. This means that new features or bug fixes can be rolled out to users quickly and efficiently.
>
> Overall, CI/CD helps teams to work more collaboratively, catch errors earlier in the development cycle, and deliver software more quickly and reliably.

- See also [[Difference between CI and CD]]
- See also [[Continuous integration aka CI]]
- See also [[Monitoring as code]]
- See also [[Continuous Deployment aka CD]]
- See also [[Development Operations]]

## Example of a ci/cd pipeline in practice

1.  A developer makes changes to the codebase and pushes the changes to the [[Github|version control system]].
2.  The [[Continuous integration aka CI|CI system]] automatically builds the code changes, runs automated tests, and generates reports on any issues or errors.
3.  If the tests pass, the [[CD system]] automatically deploys the changes to a staging environment, where they can be further tested and validated.
4.  Once the changes have been validated in the staging environment, the CD system automatically deploys the changes to the production environment, where they are made available to end-users.
5.  The CD system continues to monitor the production environment, using automated testing and monitoring tools to identify any issues or errors and automatically roll back changes if necessary.

---

## Related

See also [[Context on My Vercel Publishing Issue]] to hear why I started implemented CI/CD best practices on my toy project/website.
