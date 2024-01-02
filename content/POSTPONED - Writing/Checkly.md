---
aliases:
  - Checkly
  - monitoring platform
tags:
  - technology
  - computer-science/software-engineering
file-created: 2023-03-15
file-modified: 2023-09-02
note-type:
  - general
description: 
linter-yaml-title-alias: Checkly
---

# Checkly

#status/postponed

## Checkly

### Overview of checkly

> Checkly is the API & E2E monitoring platform for the modern JavaScript stack. It seamlessly integrates into your Vercel deployment pipeline to guarantee that **you'll never deploy broken apps again** - free and zero-config!
>
> #### Features
>
> -   Run reliability checks against all your deployments.
>     -   Run fast Playwright-powered Browser checks to ensure essential user flows are working.
>     -   Monitor and test your APIs to guarantee they’re up and running.
> -   Add performance checks to avoid regressions for your Web Vitals.
> -   Automatically block deploys when a reliability or performance check fails.
> -   Analyze your automated checks with detailed error logs and network waterfalls.
> -   Define fine-grained alerting to know about regressions before your users report them.
> ^[https://vercel.com/integrations/checkly]

### Key features of checkly

> [!ai] AI
>
> As an AI language model, I cannot provide personal opinion based answers. However, I can list out the key functions and features of Checkly.
> Checkly is a monitoring platform that allows developers to implement monitoring as code. The key functions and features of Checkly include:
>
> 1. Automated End-to-End Testing: Checkly allows developers to create automated end-to-end tests for web applications.
> 2. Real-time Monitoring: Checkly monitors web applications in real-time and alerts developers when there are issues.
> 3. API Monitoring: Checkly monitors APIs and alerts developers when there are issues.
> 4. Synthetic Monitoring: Checkly offers synthetic monitoring capabilities, which means it simulates user behavior to ensure that web applications are functioning correctly.
> 5. Customizable Alerting: Checkly allows developers to customize alerting rules based on their specific needs.
> 6. Integrations: Checkly integrates with various tools such as Slack, PagerDuty, and Datadog.
> 7. Collaborative Environment: Developers can collaborate with their team members by sharing test results and monitoring data.
> 8. Infrastructure Monitoring: With infrastructure monitoring capabilities, Checkly provides insights into the performance of servers, databases, and other components of the application stack.
> 9. Code-based Configuration: With code-based configuration, developers can configure monitoring settings using code instead of a graphical user interface (GUI).
> 10. Custom Metrics Collection: Developers can configure custom metrics collection to monitor specific aspects of their applications that are not covered by default metrics collection options provided by Checkly

### Key steps in configuring checkly

Here are the key steps to configure Checkly:

1.  Create a new check: Start by creating a new check in the Checkly dashboard. Choose the appropriate check type, such as a browser check, API check, or load check, and provide the necessary details for the check, such as the URL or API endpoint to be monitored.
2.  Customize the check: Configure the check to include any additional parameters or settings that are needed, such as headers, request body, or query parameters. You can also set the frequency of the check, and configure any notifications or integrations that are needed.
3.  Choose the location: Choose the location where the check will be run from. Checkly has a global network of test locations, so you can choose a location that is closest to your users or target audience.
4.  Configure integrations: Checkly integrates with various third-party tools such as Slack, PagerDuty, or Datadog. Configure these integrations to receive notifications or alerts when the check fails or encounters errors.
5.  Set up Assertions: You can set up Assertions to validate specific responses to API calls or checks. This ensures that the response meets certain criteria and avoids false positives.
6.  Review and save: Review the check configuration and save the check. Checkly will now run the check at the specified frequency and provide reports on the check results.

Overall, configuring Checkly involves creating a new check, customizing it to include any necessary parameters, choosing the location for the check to run from, configuring integrations, setting up Assertions, and reviewing and saving the configuration. Checkly provides a simple, yet powerful, way to configure website and API monitoring, making it easier to ensure that your application is functioning correctly and providing a positive [[User experience design|user experience]].

#status/wip

Related to [[Continuous Integration and Deployment]]

---
