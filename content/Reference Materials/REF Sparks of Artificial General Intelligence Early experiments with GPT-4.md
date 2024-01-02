---
aliases:
  - Microsoft Research on GPT-4
  - Sparks of Artificial General Intelligence Early Experiments with GPT-4
  - spark of AGI
tags:
  - reference-material/read-it-later/article
  - intelligence/artificial-intelligence
  - productivity/tool
  - computer-science
file-created: 2023-03-25
file-modified: 2023-09-03
note-type: article
description: 
author:
  - Submitted on 22 Mar 2023
linter-yaml-title-alias: Sparks of Artificial General Intelligence Early Experiments with GPT-4
original-title: "Sparks of Artificial General Intelligence: Early experiments with GPT-4"
reference: true
source: https://arxiv.org/abs/2303.12712
website: arXiv.org
---

#status/postponed

# Sparks of Artificial General Intelligence Early Experiments with GPT-4

## Introduction

### Industry Context

Key breakthrough in recent years was a result of [[Natural Language Processing (NLP)|natural language processing]] achieved by [[Large language models produce human text using big data]] (LLMs)
Most of these are based on the Transformer architecture

### GPT-4

- GPT-4 uses self-supervised objective of predicting next work in a partial sentence
- Missing definition of intelligence focusing on "learn quickly and learn from experience" as model is not continuously learning
- patterns of intelligence are not human like
- "One of the key aspects of GPT4’s intelligence is its generality, the ability to seemingly understand and connect any topic, and to perform tasks that go beyond the typical scope of narrow AI systems"
- the primary strength of the system is usage of natural language and creating text to summarizing translating and answering general sets of questions

### Objective of the Paper

- explore the current capabilities and limitations of GPT-4
- the paper purports that there's a paradigm shift in the field of [[Map of Content/Computer Science|computer science]] as a result of this product
- they plan on using an approach closer to traditional psychology to understand how it uses creativity and curiosity
- they need to rule out the possibility that the AI is using memorization or copying existing data
	- they do this by changing the prompt and asking to do the same task in a different context
- the paper will try to prove that GPT 4 actually understands the concept rather than improvising
	- can it produce new knowledge is one of the questions asked which would symbolize intelligence

## Multimodal and Interdisciplinary Composition

- Can it integrate knowledge from different domains or modalities? Can it apply it?
- My feeling when it's talking about Section 2.1 and integrative ability, they often ask questions that tell it to use algorithms, or just write in a similar style rather than truly producing knowledge. It's more imitation than actual application of knowledge. I feel like a lot of the questions asked or just do a certain question in a certain style, which is just understanding the syntax behind something.
- Is the ability of chaining multiple tasks together, equivalent to intelligence?
- GPT4 could be combined with other models like stable diffusion. GPT4 can provide an outline or help direct the other models. It would act as a central brain or information processor?
- They asked it a bunch of tasks, such as creating music or creating images with specific instructions and constraints.

## Coding

- It was able to pass novel coding scenarios after its pre trained data such as LeetCode
- They also created end to end tasks That would mirror real life scenarios such as database realization, algorithms, data structures and using multiple libraries and front end development.
- It was asked to interpret code and write a comments of all those intermediary steps and it was able to do that in natural language without access to a Python compiler…supposedly
- Likewise, apparently it can create code from pseudo code

## Math Knowledge

- When testing the math knowledge, they tried to mitigate overfitting by asking it to break down the steps to a question and a theoretical way before giving out the actual answers. Supposedly, it was able to answer this without looking at the answer keys.
- When they varied the inputs to the question, it was able to answer correctly. It can apply general solution methods. The criticism may be that GPT4 memorizes the solution template, but it's also how humans solve general math problems by remembering the framework or the concept.
- They were asked to come up with mathematical models for a construct, with reasoning provided and it was able to accomplish this task
- They asked GPT Fermi questions, which are general mathematical problems with unclear answers ("How many piano tuners in Chicago")
	- This requires general knowledge and quantitative thinking.

## Interaction with the World

- GPT4 is able to use external tools such as search engines or API in order to overcome knowledge limitations on its data set if prompted
- It's even able to play limited text games. And understand the context and environments it's in. However, this cannot be used as a general statement, as it is limited in nature.

## Theory of Mind and GPT-4

- They tried to test various aspects of it.
- When given certain prompts, it seems to be able to understand intentions and frames of mind.
- Process consistency
	- Ability to make predictions about future behavior of the model or different contexts
		- Given the same kind of question, will it provide the same consistent logic in answering it
		- In the example provided, it said that professor is typically feminine when translated to Portuguese yet when asked in a new session, it did not follow this internal logic. Another way of saying this is that the internal logic is not consistent.
		- "An example of process inconsistency. GPT-4 translates “nurse”, “secretary”, and “actress” into feminine nouns, but not “teacher” (see Section 9.3 for a more detailed discussion of bias issues)."
	- What humans expect or desire from explanations when we [[Curiosity is a basic motivation|want to understand]]/debug/trust a system
	- Evaluate this by creating new inputs where explanation should predict behavior
	- Increase in this should lead to to higher fidelity and less arbitrariness aka process-consistent
	- output consistency is not process consistency
- Output consistency
	- whether the explanation is consistent with the output y given the input x and the context c. In other words, an output-consistent explanation provides a plausible causal account of how y was derived from x and c.
	- By this criterion, GPT-4 is remarkably good at generating reasonable and coherent explanations, even when the output is nonsensical or wrong
	- Given the provided logic, does the following sequence make sense?
	- i.e. toddler logic is internally consistent

See also [[Theory of mind]]

## Discriminative Capabilities of GPT 4

?

See also [[Discriminative intelligence]]

## Limitations of Autoregressive Architecture Highlighted by GPT-4

- The system has no inner dialogue. It's only moving forward and has no concept of working memory. It seems to move forward with its input data. It lacks the ability to plan ahead and has to sequentially process information.
- The system is limited when it has to face a problem which cannot be solved in a sequential manner.
- Two types of tasks
	- incremental task
		- task which can be solving a gradual continuous way
		- things which can be solved with content generation
		- application of current knowledge and skills but do not require [[Conceptual change is the process of changing our mental models over time|conceptual change]]
	- discontinuous task which require creativity and are 'harder' problems which are abstract
		- Math problems require innovative applications application of concepts
		- creating a philosophical argument
		- writing a joke
- they link this back to [[Thinking Fast and Slow by Daniel Kahneman]]  and the [[Dual thinking process theory explains implicit and conscious reasoning|dual process model]] of thinking.
- at this time, GPT4 is not able to use [[Explicit reasoning is analytical and higher-level thinking|explicit reasoning]] which is the [[Implicit reasoning uses heuristics|implicit reasoning]].

## Erroneous Generations aka Hallucinations

[[Large language models produce human text using big data|LLMs]] have the possibility of generating errors without warning and other conceptual errors. these are typically called hallucinations and may appear reasonable or aligned with truthful inference.

![[Pasted image 20230325174103.png]]

there are two types:
1. Open-domain hallucination
2. Closed domain hallucination

Close domain hallucinations are error made within a context and can be fact-checked. we can identify inconsistencies through fact checking.

Open domain hallucinations

> Open domain hallucinations provide more difficult challenges, per requiring more extensive research including searches and information gathering outside of the session. The veracity of inferences may be of lesser criticality for uses of LLMs centering on creativity and exploration, such as in assisting writers with the creation of fictional literature. Hallucinations may also be more tolerated in contexts where there are clear, well-understood grounding materials and an assume cycle of intensive review of generations by end users, such as in supporting people with rewriting their own content.

## Paper's conclusions

I thought the ending was quite poignant
- Talked about future of AGI
	- Confidence calibration
	- Long term memory
	- Continual learning
	- Personalization
	- Planning and conceptual leaps
	- Transparency and reproducibility
	- Cognitive biases and irrationality
	- Challenges with sensitive to input and particular framing
- Notes that GPT-4 has a form of general intelligence but not true AGI
- Paper was more focused on demonstrating *possibilities* - a phenomenological study. Not understanding the deep root mechanics which is still a misunderstood part of [[Large language models produce human text using big data|LLMs]] .

![[Exceprt conclusion sparks of AGI.pdf]]

> How does it reason, plan, and create? Why does it exhibit such general and flexible intelligence when it is at its core merely the combination of simple algorithmic components—gradient descent and large-scale transformers with extremely large amounts of data? These questions are part of the mystery and fascination of LLMs, which challenge our understanding of learning and cognition, fuel our curiosity, and motivate deeper research.
>
> One general hypothesis [OCS+20] is that the large amount of data (especially the diversity of the content) forces neural networks to learn generic and useful “neural circuits”, such as the ones discovered in [One+22, ZBB+22, LAG+22], while the large size of models provide enough redundancy and diversity for the neural circuits to specialize and fine-tune to specific tasks. Proving these hypotheses for large-scale models remains a challenge, and, moreover, it is all but certain that the conjecture is only part of the answer. On another direction of thinking, the huge size of the model could have several other benefits, such as making gradient descent more effective by connecting different minima [VBB19] or by simply enabling smooth fitting of high-dimensional data [ES16, BS21]. Overall, elucidating the nature and mechanisms of AI systems such as GPT-4 is a formidable challenge that has suddenly become important and urgent.

---

## Sparks of Artificial General Intelligence: Early Experiments with GPT-4

> [!Warning] Reference note
> The original source can be found here: https://arxiv.org/abs/2303.12712

---

## Article Content

%%make it easy to delete under a heading%%
Authors:[Sébastien Bubeck](https://arxiv.org/search/cs?searchtype=author&query=Bubeck%2C+S), [Varun Chandrasekaran](https://arxiv.org/search/cs?searchtype=author&query=Chandrasekaran%2C+V), [Ronen Eldan](https://arxiv.org/search/cs?searchtype=author&query=Eldan%2C+R), [Johannes Gehrke](https://arxiv.org/search/cs?searchtype=author&query=Gehrke%2C+J), [Eric Horvitz](https://arxiv.org/search/cs?searchtype=author&query=Horvitz%2C+E), [Ece Kamar](https://arxiv.org/search/cs?searchtype=author&query=Kamar%2C+E), [Peter Lee](https://arxiv.org/search/cs?searchtype=author&query=Lee%2C+P), [Yin Tat Lee](https://arxiv.org/search/cs?searchtype=author&query=Lee%2C+Y+T), [Yuanzhi Li](https://arxiv.org/search/cs?searchtype=author&query=Li%2C+Y), [Scott Lundberg](https://arxiv.org/search/cs?searchtype=author&query=Lundberg%2C+S), [Harsha Nori](https://arxiv.org/search/cs?searchtype=author&query=Nori%2C+H), [Hamid Palangi](https://arxiv.org/search/cs?searchtype=author&query=Palangi%2C+H), [Marco Tulio Ribeiro](https://arxiv.org/search/cs?searchtype=author&query=Ribeiro%2C+M+T), [Yi Zhang](https://arxiv.org/search/cs?searchtype=author&query=Zhang%2C+Y)

[Download PDF](https://arxiv.org/pdf/2303.12712)

> Abstract: Artificial intelligence (AI) researchers have been developing and refining [[Large language models produce human text using big data|large language models (LLMs)]] that exhibit remarkable capabilities across a variety of domains and tasks, challenging our understanding of learning and cognition. The latest model developed by OpenAI, GPT-4, was trained using an unprecedented scale of compute and data. In this paper, we report on our investigation of an early version of GPT-4, when it was still in active development by OpenAI. We contend that (this early version of) GPT-4 is part of a new cohort of LLMs (along with ChatGPT and Google's PaLM for example) that exhibit more general intelligence than previous AI models. We discuss the rising capabilities and implications of these models. We demonstrate that, beyond its mastery of language, GPT-4 can solve novel and difficult tasks that span mathematics, coding, vision, medicine, law, psychology and more, without needing any special prompting. Moreover, in all of these tasks, GPT-4's performance is strikingly close to human-level performance, and often vastly surpasses prior models such as ChatGPT. Given the breadth and depth of GPT-4's capabilities, we believe that it could reasonably be viewed as an early (yet still incomplete) version of an artificial general intelligence (AGI) system. In our exploration of GPT-4, we put special emphasis on discovering its limitations, and we discuss the challenges ahead for advancing towards deeper and more comprehensive versions of AGI, including the possible need for pursuing a new paradigm that moves beyond next-word prediction. We conclude with reflections on societal influences of the recent technological leap and future research directions.
