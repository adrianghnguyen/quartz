---
aliases:
  - Data warehouse centralizes and processes raw information into a universally accessible database
  - data warehousing
  - data warehouse
  - centralized and transformative database which collects processed raw information
tags:
  - computer-science/data
  - computer-science/data/data-engineering
file-created: 2023-03-19
file-modified: 2023-09-03
note-type: general
description: 
linter-yaml-title-alias: Data warehouse centralizes and processes raw information into a universally accessible database
---

# Data warehouse centralizes and processes raw information into a universally accessible database

#status/postponed

---

## Data warehouse

It's a centralized and transformative database which collects processed raw information. It is typically used for analysis and reports. There are three main steps called extract, transform and load often abbreviated to ETL. It's something I worked with in my previous roles at Samsung and at Unity.

Data is typically shaped according to [[POSTPONED - Writing/Dimensional modeling|dimensional modeling]] techniques.

> [!ai]+ AI
>
> Data warehousing is the process of collecting, organizing, and storing large volumes of data from various sources into a central repository. It involves extracting data from operational systems, transforming it into a consistent format, and loading it into a data warehouse. The purpose of data warehousing is to provide a unified and integrated view of an organization's data to support business intelligence and decision-making processes. Data in a warehouse is typically structured, optimized for querying, and can be analyzed to gain insights and [[make informed decisions]].

[[The Data Warehouse Toolkit by Ralph Kimball|The Data Warehouse Toolkit by Ralph Kimball]]
Related to [[Metadata for contacts or people]]

> [!ai] AI
>
> Data warehousing is a process of collecting, storing, and managing data from various sources to provide meaningful insights and analysis for decision-making purposes. It involves integrating data from different sources, transforming it into a common format, and loading it into a centralized repository known as the data warehouse. The data warehouse enables organizations to analyze historical data trends, identify patterns, and make [[Develop situational awareness to understand the environment|informed decisions]] based on the insights gained from the data. Data warehousing is essential for organizations that deal with large volumes of data and require timely access to accurate information for strategic decision-making.

## Key concepts in data warehousing

### Data reusability

Data reusability refers to the ability to use raw data from a data source to build different data models or analytical applications without having to recreate the data model from scratch. In other words, it allows you to reuse the same raw data for different purposes and build different models or applications on top of it. We can think of it as the data equivalent to a function being reused.

This concept is important in data warehousing because it enables organizations to be more agile and responsive to changing business needs. Instead of having to start from scratch every time a new data model or analytical application is required, data reusability allows organizations to reuse existing data assets and quickly adapt to changing business requirements.

To achieve data reusability, data warehousing systems often use a standardized data model and data integration process, so that data can be easily shared and reused across different applications and business units. Additionally, data quality and data governance practices must be in place to ensure that the raw data is reliable, accurate, and consistent across different data models and applications. Data governance is important because garbage in equals garbage out.

### Data lineage

Data lineage refers to the ability to track the flow of data from its origin to its destination, including any transformations or modifications that occur along the way. In other words, it allows you to trace the path of a data point from its source through to its final representation in a data model or report. We can think of it as ancestry for data. It allows us to see where it came (the source), how it's been transformed words it's being used (descendant tables and databases) and allows teams to use standardized definitions.

Data lineage is important in data warehousing because it provides visibility into the data transformation process, allowing you to understand how data has been manipulated or modified and ensuring the accuracy and reliability of the final output. If something has changed in the source data or the data model, data lineage allows you to identify the impacted areas and rebuild the affected parts of the data model or report.

Data lineage is typically captured and managed through metadata, which provides information about the data, such as its source, location, format, and any transformations or modifications that have been applied to it. By maintaining a comprehensive record of data lineage, organizations can ensure data accuracy, meet regulatory compliance requirements, and improve decision-making by providing a clear understanding of where data comes from and how it has been processed.

## Idempotence in data

> [!ai] AI
>
> Idempotence refers to the property of a function or operation that can be applied multiple times without changing the result beyond its initial application. In data warehouses, idempotence is essential to ensure that data is not duplicated or overwritten during extraction, transformation, and loading (ETL) processes.
>
> When ETL processes are designed with idempotence in mind, they can handle repeated loads of the same data without creating duplicate records or modifying existing ones. This ensures that the warehouse's data remains consistent and accurate over time.
>
> To achieve idempotence in ETL processes, developers use techniques such as:
>
> - Using unique identifiers: Each record is assigned a unique identifier, such as a primary key, which is used to compare incoming data with existing records. If an incoming record has the same identifier as an existing one, it is either updated or ignored.
> - Performing delta loads: Instead of loading all data every time, only new or updated records are loaded into the warehouse. This reduces processing time and ensures that duplicate records are not created.
> - Using staging tables: Data is first loaded into staging tables before being moved into the main warehouse tables. This allows for validation and de-duplication of records before they are added to the main tables.
>
> Overall, idempotence plays a crucial role in ensuring that data warehouses maintain their integrity and consistency over time. By designing ETL processes with this property in mind, developers can build robust and reliable systems that meet business requirements for accurate and up-to-date information.

> Idempotency is a property of a data processing operation that can be applied multiple times without changing the result beyond the initial application. In data warehousing, idempotent operations are used to ensure that data processing is reliable and consistent, even in the face of errors or unexpected events. For example, an idempotent operation might be used to load data into a database, so that if the same data is loaded multiple times, only one copy is stored in the database.

- See also [[Referential transparency]]

## Determinism in data warehousing

[[Deterministic|Determinism]] is a property of a data processing operation that always produces the same output given the same input, without any randomness or unpredictability. In data warehousing, deterministic operations are used to ensure that data transformations are consistent and repeatable, regardless of the context or environment in which they are executed. For example, a deterministic operation might be used to clean and standardize data, so that the same input data always produces the same output data.

See also [[Difference between Deterministic and Referential Transparency]]


## Data warehousing

Related to [[Interview with Candid Co]]

Query writing (subqueries, advanced functions such as window, views, materialized views etc.)
[https://www.astera.com/type/blog/data-warehouse-concepts/](https://www.astera.com/type/blog/data-warehouse-concepts/)
Refresh tool knolwedge
Look over his profile again Kevin's
