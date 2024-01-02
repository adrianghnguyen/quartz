---
dg-publish: true
aliases:
  - Application performance monitoring
  - APM
  - infrastructure
  - IT infrastructure
  - system uptime
file-created: 2023-03-20
file-modified: 2023-05-05
tags:
  - engineering/infrastructure
  - technology
  - computer-science/data/data-engineering
  - computer-science/software-engineering
  - computer-science/software-engineering
linter-yaml-title-alias: Application performance monitoring
---

# Application performance monitoring

#status/done

---

## Application performance management

This is the greater concept under which application performance monitoring falls."Application performance **monitoring** falls under the more general, related term _application performance management_. While application performance monitoring only focuses on _tracking_ the performance of an application, application performance management focuses on the broader concept of _controlling_ an app's performance levels. In other words, monitoring is a part of management."

## What is application performance monitoring?

These are tools to monitor up time on systems. for example for example allows you to know if something went down or if it stole alive by checking HTTP responses or reading logs. When you have multiple IT systems it might be very difficult to know what's going on or to individually check each system So you need something to bring it back all together. we can think of it kind of like the equivalent of a data warehouse in terms of centralizing information but in terms of systems and infrastructure. it allows you to monitor cloud environments and ensure that they are available and the performance is adequate.

It might involve monitoring the front-end (user's perspective - such as inability to access a web page) and the backend monitoring (databases or other services which power the whole).

Effective application performance monitoring platforms should focus on:
1. [[Infrastructure Monitoring]]
2. [[User experience design|User experience]]
3. performance and reliability of transactions

> Application performance monitoring (APM) tools allow users to monitor and track the performance of particular software or web applications to identify and solve any performance issues that may arise. These solutions provide performance metrics for applications, with specific insights into the statistics such as the amount of transactions processed by the application or the response time to process such transactions. APM products form a baseline for these metrics and monitor the applications for any variance from the baseline. The metrics are displayed in a variety of data visualizations for easy conceptualization of the overall performance. They are very commonly used by application administrators to manage web applications in hopes to discover possible reasons for delays in response time. With the ability to identify and fix any performance issues, businesses can provide an optimal [[User experience design|user experience]]. Some APM solutions may offer similar functionality to [database management systems](https://www.g2.com/categories/database-management) and [network monitoring](https://www.g2.com/categories/network-management) solutions.^[https://www.g2.com/categories/application-performance-monitoring-apm]

## Key factors to monitor in apm

1.  runtime application architecture
2.  [real user monitoring](https://www.techtarget.com/searchitoperations/definition/real-user-monitoring-RUM)
3.  business transactions
4.  component monitoring
5.  analytics and reporting

### Real user monitoring

> Also known as _end user experience monitoring_, this component gathers user-based performance data to understand how well the application is performing for users and to gauge potential performance problems. For example, APM might monitor the response time of a critical website and flag response times that exceed a comfortable threshold, alerting stakeholders of lag or application response issues. Real user monitoring enables an organization to efficiently respond to faults and understand their effect. There are two ways of tracking end user experience:
>
> 1.  **Synthetic monitoring.** This tracking method uses **probes and bots to simulate an end user (similar to how [[Monitoring as code|Checkly does it]])** to determine problems before the app is opened. [Synthetic monitoring](https://www.techtarget.com/searchsoftwarequality/definition/synthetic-monitoring) is also used to monitor service-level agreements (SLAs) associated with the app.
> 2.  **Agentless monitoring.** This method uses data probes to analyze [network traffic that travels through load balancers](https://www.techtarget.com/searchnetworking/answer/Application-vs-network-load-balancing-Whats-the-difference) and switches. Agentless monitoring reveals information about performance throughout the entire infrastructure, as well as details on the analyzed client -- such as their location, OS and browser.

## Commonly tracked metrics in application performance monitoring

These tools will gather and quantify all data which are related to  application performance. In a nutshell, it just checks the performance or health of the system. Think of it as a doctor's diagnosis, but for IT infrastructure.

They achieve this by looking at:
- process utilization
- memory demands
- disk read/write speeds
- processor utilization (how well the CPU is chugging along)

## Common tools application performance monitoring tools

- Datadog
- SumoLogic
- Splunk
- Dynatrace
- [Prometheus - Monitoring system & time series database](https://prometheus.io/) is open-source
