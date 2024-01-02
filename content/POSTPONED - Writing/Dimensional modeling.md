---
aliases:
  - Dimensional modeling organizes data into dimensions and measures to support easy and efficient data analysis
  - dimensional modeling
  - data modeling technique
  - Dimensional modeling is a data modeling technique used in data warehousing.
  - organizing data into dimensions and measures to support easy and efficient analysis
tags:
  - computer-science/data
file-created: 2023-09-01
file-modified: 2023-10-05
note-type: general
description: 
linter-yaml-title-alias: Dimensional modeling organizes data into dimensions and measures to support easy and efficient data analysis
---
#status/postponed

Related to [[Metadata for contacts or people]]

# Dimensional modeling organizes data into dimensions and measures to support easy and efficient data analysis

- Used in databases, [[data engineering]], [[Data Warehouse|data warehousing]] and data visualization.
- Had to do this for my prior work at Samsung and Unity
- More of an art form at times

> [!ai]+ AI
>
> Dimensional modeling is a data modeling technique used in [[Data Warehouse|data warehousing]]. It involves organizing data into dimensions and measures to support easy and efficient analysis. Dimensions represent the characteristics or attributes of the data, while measures represent the numerical values being analyzed. The model is designed to provide a clear, intuitive structure for querying and reporting, allowing users to easily understand and navigate the data. It is commonly used in decision support systems and business intelligence applications.

The four-steps of performing dimensional modeling
1. Identify the process
2. Determine the grain
3. Identify the dimension
4. Identify the facts

## Data dimensions

> Dimensions fall out of the question, “How do business people describe the data resulting from the business process measurement events?”
>
> You need to decorate fact tables with a robust set of dimensions representing all possible descriptions that take on single values in the context of each measurement. If you are clear about the grain, the dimensions typically can easily be identified as they represent the “who, what, where, when, why, and how” associated with the event.
>
> Examples of common dimensions include:
> - Date
> - Product
> - Customer
> - Employee
> - Facility
>
> With the choice of each dimension, you then list all the discrete, text-like attributes that flesh out each dimension table.
> \- [[The Data Warehouse Toolkit by Ralph Kimball|The Data Warehouse Toolkit by Ralph Kimball]]


