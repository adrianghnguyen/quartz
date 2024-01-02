---
dg-publish: true
aliases: Graph theory, graphs, network, interconnection, relationship. relationship between, pairwise, connection, connectivity, links, lines
file-created: 2023-02-20
file-modified: 2023-05-05
tags: [theory, network, mathematics, network, computer-science/data/data-engineering, computer-science]
linter-yaml-title-alias: Graph theory
---

# Graph theory

#status/done

---

## Definition of graph theory

[Introduction to Graph Theory: A Computer Science Perspective - YouTube](https://www.youtube.com/watch?v=LFKZLXVO-Dg&feature=youtu.be)

![[Pasted image 20230221104502.png|500]]

A network that helps define and visualize relationships between various components. Kinda like what Obsidian ([[Why I write in Obsidian]]) uses to displays connections between its notes.

- Edge = **Relationship**
- Vertex = **Node or point of connection**

### Mathematical definition of graph

![[Pasted image 20230221111411.png|500]]

A graph $G = (V,E)$ is a set of Vertices $V$ and edges $E$ where each edge $(u,v)$ is a connection between vertices $u, v\ \epsilon\ V$

We can use **set notation** to describe edges and vertices.

$V = \{0,1,2,3,4,5\}$

$E = \{(0,1), (0,2), (0,3), (1,3), (2,3), (3,4)\}$

Notice how for edge definitions, that resembles tuples inside of a list?

### Key terminology in graph theory

### Neighbors

Neighbors

vertices u and v are neighbors if an edge connects them

[[Pasted image 20230221112109.png]]

$neighbors(0) = \{4,6,8\}$

Often we'll ask ourselves what are the neighbors - how are they connected to another neighboring vertex?

Degree

Degree ($v$) is equal to the **number of edges ($E$)** connected to $v$

[[Pasted image 20230221112151.png]]

$degree(0) = 3$

Think of is a function where the input is the current node which we want to examine, and the resulting output/function is how many edge connections

- How strong is the node's connection to the others? Is it dense?

Path

Sequence of vertices connected by edges

[[Pasted image 20230221112327.png]]

Path length

**Number of edges** in a path

related to path.

Kinda like doing path.length() within Python code

Cycle

Path that stars and ends at same vertex

Like a circular loop - you can get back to the beginning. Like going around in a neighborhood circle.

There can be multiple cycles possible within a graph

connectivity

two possible contexts

1. two vertices are **connected** if a *path exists between them*
2. A graph is called **connected** when *all vertices are connected*. If you had to physically walk through it, could you get to any point? or is there a certain gap? i.e. are there isolated nodes? [[Pasted image 20230221112734.png|Disconnected graph]]

> [!Warning] I stopped here timestamp
> [Introduction to Graph Theory: A Computer Science Perspective - YouTube](https://youtu.be/LFKZLXVO-Dg?t=505)

Connected component

Subsert of vertices $V_{i} $

## Usefulness of graphs - why study them?

Anything which has examples of connectivity can be represented by graphs.

[![](https://i.imgur.com/Wu1wud5m.png)](https://i.imgur.com/Wu1wud5.png)

Practical example | Explained
---| ---
Mapping and GPS navigation systems | To get from point A to point B. Streets represent edges. Intersections represent nodes.
Social networks | Display the relationships between people and friend recommendation algorithms by finding the next external edge
Sudoku | Each square grid can represent a sub-graph [Sudoku graph example](https://i.imgur.com/6CtUooO.png)

## Terminology

## Graph representations as data structures

## Interesting problems in graph theory

### Directed graphs

> Formal definition: A **directed graph** or **digraph** is a graph in which **edges have orientations**.^[Wikipedia]
> ![|100](https://upload.wikimedia.org/wikipedia/commons/thumb/a/a2/Directed.svg/330px-Directed.svg.png)

So the directions…means it's directed. I guess that makes sense. So that's what a DAG from Airflow is! It implies **directionality** versus being unstructured or the relationship of the entities going both ways.

## Personal relevance

Obsidian ([[Why I write in Obsidian]]) uses graphs to represent the connections between notes which are representations of our thoughts as nodes.

Learning about graph theory would help me understand how those relationships can be explored. Since we talked about relationship, would the [[Relational Proximity Framework]] be applicable?

[[Rohit Moni]] was also talking to me about how his current project is focused on using nodes to represent animation queue orders for the Unity game engine.

## Related

[Introduction to Graph Theory: A Computer Science Perspective - YouTube](https://www.youtube.com/watch?v=LFKZLXVO-Dg&feature=youtu.be)
