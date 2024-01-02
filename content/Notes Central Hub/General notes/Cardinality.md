---
dg-publish: true
aliases: Cardinality, cardinality, attributes, multiple values
file-created: 2023-03-06
file-modified: 2023-05-05
tags: [computer-science/data]
linter-yaml-title-alias: Cardinality
---

# Cardinality

#status/done

Related to [[Dimensionality]]

---

## Definition of cardinality

The cardinality of a data attribute refers to the number of distinct values that it can have.

If we take the analogy, also used within [[Dimensionality|dimensionality]], of a car, it would be how serial numbers do you have for a specific car model (dimension)? There are tons of unique values so a car serial number would have high cardinality.

## In the context of data systems

> A boolean column, which only can have the values of true or false, has a cardinality of 2. HTTP status codes – 200, 301, 302, 404, 500 – might have a cardinality under a few dozen. These low cardinality fields are useful to track broad trends in your system: separating your service out by AWS Zone, or by current build of your code, or by endpoint.
>
> High cardinality refers to a column that can have many possible values. For an online shopping system, fields like userId, shoppingCartId, and orderId are often high-cardinality columns that can take take hundreds of thousands of distinct values.^[https://docs.honeycomb.io/concepts/high-cardinality/#:~:text=The%20term%20%E2%80%9Chigh%20cardinality%E2%80%9D%20means,different%20attributes%20attached%20to%20events.]
