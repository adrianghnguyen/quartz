---
dg-publish: true
aliases:
  - Control systems theory
  - control system
  - manipulate a system
  - fundamental tool for understanding and designing systems
  - understanding systems
  - control systems
  - control theory
  - feedback control systems
  - feedback control system
file-created: 2023-02-15
file-modified: 2023-05-05
tags:
  - theory/control
  - productivity
  - engineering
  - mathematics
  - technology
  - engineering/systems
  - biology/human-biology/body/central-nervous-system
linter-yaml-title-alias: Control systems theory
source:
---

# Control systems theory

#status/done

---

> Control theory is a branch of engineering and mathematics that deals with the analysis and design of systems that can be controlled or regulated to achieve specific objectives. In other words, it provides a [[Mental models make it easy for us to understand|framework]] for understanding how to manipulate a system to achieve a desired outcome.
>
> A control system typically consists of three main components: a sensor or measurement device that detects the current state of the system, a controller that calculates and sends control signals based on the measured state, and an actuator that takes the control signals and affects the system's behavior.
>
> Control theory provides tools for analyzing and designing these components to achieve specific control objectives, such as stability, responsiveness, and accuracy. For example, control theory can be used to design a cruise control system for a car that maintains a constant speed, or a temperature control system for a building that maintains a comfortable indoor temperature.
>
> Control theory also provides techniques for analyzing the behavior of a system, such as stability analysis, where the aim is to ensure that the system remains stable under various operating conditions. Additionally, control theory can be used to design controllers that can compensate for disturbances or uncertainties in the system, such as changes in the environment or unexpected inputs.
> 
> Overall, control theory is a fundamental tool for understanding and designing systems that can be controlled to achieve specific objectives, and it is used in a wide range of applications in engineering, science, and technology.

It's a [[Mental models make it easy for us to understand|framework]] to control a system (duh!) to achieve a specific goal or output. That's very loose as a [[Mental models make it easy for us to understand|conceptual framework]] ([[Mental models make it easy for us to understand]]). Control theory can also be used to compensate for disturbances or uncertainties (relationship to [[Uncertainty Principle]]?) within the system. A successor theory to control theory is the [[Difference between control systems theory and dynamic systems theory|dynamic systems theory]]. Control systems theory assumes that the inputs are fixed or linear while dynamic assumes a nonlinear nature of variables ([[Difference between control systems theory and dynamic systems theory]]).

- See [[Machine Learning for Adaptive Control]] to see how it can be used in machine learning algorithms.
- [Feedback Control Systems - an overview | ScienceDirect Topics](https://www.sciencedirect.com/topics/engineering/feedback-control-systems#:~:text=A%20feedback%20control%20system%20is,as%20a%20means%20of%20control.)

## The three components of systems in control theory

Systems are made of three main components:

- **sensor** or measurement device
	- similar to our body's senses which takes in signal from the world such as smell, taste, vision, etc.
- **controller** which sends signals (called control signals)
	- our central nervous system or CNS
- **actuator** which takes these signals and directs the overall system
	- similar to our brain

## Advantages of control theory

Here are some of the benefits as to why one might choose to implement the approach of control theory to a system versus using the [[Dynamic systems theory|dynamic systems theory]] approach.

- Linear systems where a simplified [[Mental models make it easy for us to understand|heuristic]] will work
- We need to optimize for something in particular
- Easier to implement when there's low [[Dimensionality]]

> Linear Systems: If the system under consideration can be modeled as a linear system, control theory may be a better choice. Control theory assumes that the relationship between the inputs and outputs of the system is linear and predictable, which may be a good approximation for some systems.
>
> Specific Performance Criteria: If the goal of the system is to optimize a specific performance criterion, such as minimizing the error between the desired and actual behavior of the system, control theory may be a better choice. Control theory provides a [[Mental models make it easy for us to understand|framework]] for designing controllers that can optimize a specific performance criterion, which may be important in some applications.
>
> Low-dimensional Systems: If the system under consideration has a relatively low number of dimensions, control theory may be a better choice. Control theory is often easier to implement for low-dimensional systems, and can provide accurate control even with limited computational resources.^[ChatGPT]
