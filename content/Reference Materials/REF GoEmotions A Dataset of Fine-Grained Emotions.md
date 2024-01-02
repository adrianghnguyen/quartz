---
dg-publish: true
aliases:
  - "REF GoEmotions: A Dataset of Fine-Grained Emotions"
  - GoEmotions dataset
  - emotion dataset for natural language processing
  - NLP dataset
  - emotion taxonomy
  - emotion classification
tags:
  - reference-material/read-it-later/article
  - intelligence/artificial-intelligence
  - psychology/emotions
note-type:
  - reference
description: 
file-created: 2023-11-29
file-modified: 2023-11-29
author:
  - Dorottya Demszky
linter-yaml-title-alias: "REF GoEmotions: A Dataset of Fine-Grained Emotions"
original-title: "Papers with Code - GoEmotions: A Dataset of Fine-Grained Emotions"
reference: true
source:
  - https://paperswithcode.com/paper/goemotions-a-dataset-of-fine-grained-emotions
website: 
---
 #status/done

# REF GoEmotions: A Dataset of Fine-Grained Emotions

> [!Warning] Reference note
> The original source can be found here: https://paperswithcode.com/paper/goemotions-a-dataset-of-fine-grained-emotions

---

> [!summary] Abstract
> Understanding emotion expressed in language has a wide range of applications, from building empathetic chatbots to detecting harmful online behavior. Advancement in this area can be improved using large-scale datasets with a fine-grained typology, adaptable to multiple downstream tasks. We introduce GoEmotions, the largest manually annotated dataset of 58k English Reddit comments, labeled for 27 emotion categories or Neutral. We demonstrate the high quality of the annotations via Principal Preserved Component Analysis. We conduct transfer learning experiments with existing emotion benchmarks to show that our dataset generalizes well to other domains and different emotion taxonomies. Our BERT-based model achieves an average F1-score of .46 across our proposed taxonomy, leaving much room for improvement.
>
> [PDF](https://arxiv.org/pdf/2005.00547v2.pdf) [Abstract](https://arxiv.org/abs/2005.00547v2) [ACL 2020 PDF](https://aclanthology.org/2020.acl-main.372.pdf) [ACL 2020 Abstract](https://aclanthology.org/2020.acl-main.372)

> [!Tip] In the future, perhaps revisit this paper to learn more about these topics:
> - May be useful to discover new papers to understand SOTA for [[Natural Language Processing (NLP)|natural language processing (NLP)]]
> - Emotion datasets
> - Emotion taxonomy
> - Emotion classification models

> [!question] How does BERT work? And how does multi-label classification work?
> I guess there's an idea for a future area of learning and [[Interesting Project Ideas|interesting project]]
>


- Talks about the dataset used in the [[Machine Learning|machine learning]] model for [[Sentiment analysis and emotion detection technology|emotion classification]] using the BERT model
- I believe this type of task falls under [[Natural Language Processing (NLP)|natural language processing (NLP)]]
- I want to understand how the labels were developed and from which psychological theories they decided to derive their taxonomy
- Prior to the work of the GoEmotions dataset, it seems like most datasets had the followings flaws:
	- Datasets were too small/not big enough corpus
	- Limited emotion taxonomy where categories were too broad - following Ekman or Plutchik emotions
- The GoEmotions dataset developed its own emotion taxonomy and created one of the largest human-annotated datasets for emotion classification work
- Taxonomy was developed using Principal Preserve Component Analysis (PPCA) to create 27 broad categories in the hope of to ease further downstream tasks such as customer feedback or chatbots (like [[OpenAI|ChatGPT]])
	- Note that this is a different technique to Principal Component Analysis (PCA)
- Once the dataset was developed, they fine-tuned a BERT-base model for the emotion classification task with this dataset
- Objectives of the emotion taxonomy within model
	1. Model should be able to cover the spectrum of emotions within the datset
	2. Provide coverage of emotional expression drawning from pscyhology literature on emotion expression and recognition
	3. Limit overlap of emotions and limit the number of emotions - make them distinct
- Words were encoded to specific emotions and they applied techniques to extract the relevant dimensions to each emotion - despite that there are emotion-ambiguous texts.
	- ![[Pasted image 20231129170748.png]]


## Data hierarchy and associatiosn from the model






## Model limitations

- What's considered a good F1 (overall performance of the model in its ability to  perform precision and recall) score for a model?
- This one was able to achieve F1=0.46 with std of 0.19 on the GoEmotions taxonomy
	- Performance was better on sentiment-grouped data (four categories of ambiguous, negative, neutral, positive) or using Ekman's (anger/disgust/fear/joy/neutral/sadness/surprise)
	- Guess you can't hold it against the model 

## Emotion taxonomy

> [!NOTE] Excerpt from [[REF GoEmotions A Dataset of Fine-Grained Emotions|REF GoEmotions: A Dataset of Fine-Grained Emotions]]
> Recent advances in psychology have offered new conceptual and methodological approaches to capturing the more complex “semantic space” of emotion (Cowen et al., 2019a) by studying the distribution of emotion responses to a diverse array of stimuli via computational techniques. Studies guided by these principles have identified 27 distinct varieties of emotional experience conveyed by short videos (Cowen and Keltner, 2017), 13 by music (Cowen et al., in press), 28 by facial expression (Cowen and Keltner, 2019), 12 by speech prosody (Cowen et al., 2019b), and 24 by nonverbal vocalization (Cowen et al., 2018). In this work, we build on these methods and findings to devise our granular taxonomy for text-based emotion recognition and study the dimensionality of language-based emotion space.

It seems like Cowen is an important player to follow in terms of the understanding of the semantic space of emotions. They make reference to someting called Semantic Space theory.


The [[REF GoEmotions A Dataset of Fine-Grained Emotions|GoEmotions dataset]] model used the following taxonomy for its data:
- Sentiment
	1. Positive
	2. Negative
	3. Ambiguous
	4. Neutral
- Ekman emotions
	1. Anger
	2. Disgust
	3. Fear
	4. Joy
	5. Neutral
	6. Sadness
	7. Surprise
- Detailed
	- admiration
	- amusement
	- anger
	- annoyance
	- approval
	- caring
	- confusion
	- curiosity
	- desire
	- disappointment
	- disapproval
	- disgust
	- embarrassment
	- excitement
	- fear
	- gratitude
	- grief
	- joy
	- love
	- nervousness
	- neutral
	- optimism
	- pride
	- realization
	- relief
	- remorse
	- sadness
	- surprise

Consider using plotly to chart this?


### Semantic space theory

> [!ai]+ AI
>
> Semantic Space theory is a concept in linguistics and cognitive science that explores the organization and representation of meaning in language. It suggests that words and concepts are organized in a multidimensional semantic space, where similar or related words are located closer to each other and dissimilar words are farther apart.
> 
> According to this theory, the meaning of a word is not solely defined by its individual characteristics but also by its relationship with other words in the semantic space. The proximity or distance between words in this space reflects their semantic similarity or dissimilarity.
> 
> Semantic Space theory has been applied in various fields, including natural language processing, computational linguistics, and psycholinguistics. It has been used to develop models for word embeddings, sentiment analysis, information retrieval, and semantic clustering.

> Cowen, Alan S., and Dacher Keltner. "Semantic space theory: A computational approach to emotion." _Trends in Cognitive Sciences_ 25.2 (2021): 124-136


## Natural Language Understanding

- NLU focuses specifically on helping machine understand the meaning, context and nuances within natural language input
- It's a subset of the broader discipline of [[Natural Language Processing (NLP)|NLP (Natural language processing)]]

> NLP involves various tasks such as text parsing, part-of-speech tagging, and named entity recognition, which are fundamental for language understanding. NLU, however, delves deeper into semantic analysis, aiming to extract meaning from language inputs. It goes beyond mere syntactic structure to comprehend the intent, sentiment, and context embedded in human communication.

> [!ai]+ AI
>
> NLU stands for Natural Language Understanding. It is a subfield of artificial intelligence (AI) that focuses on the ability of machines to comprehend and interpret human language in a way that is similar to how humans understand it. NLU involves various techniques and algorithms that enable AI systems to analyze and understand text or speech data, extract meaning, identify entities, infer sentiments, and respond appropriately. It encompasses tasks such as sentiment analysis, entity recognition, language translation, question answering, and more. NLU is a crucial component in building AI systems that can effectively interact with humans using natural language.

## Books which can serve as good introduction to cognitive linguistics

[[2023-11-29]] I currently do not understand enough of linguistics theory to understand how language affects how we think - perhaps it's worth reading some of the key paper

If one wants to understand the state of the art of how language affects how humans think, in terms of cognitive science, what are some good introduction books?

> [!ai]+ AI
>
> 1. "Metaphors We Live By" by George Lakoff and Mark Johnson - This book explores the influence of metaphorical language on human thought and how it shapes our understanding of the world.
> 2. "The Language Instinct: How the Mind Creates Language" by Steven Pinker - Pinker explores the relationship between language and the mind, discussing how language is uniquely human and its impact on our thoughts and behaviors.
> 3. "Words That Work: It's Not What You Say, It's What People Hear" by Frank Luntz - This book delves into the power of language in shaping public opinion and influencing people's thoughts and beliefs.
> 4. "The Stuff of Thought: Language as a Window into Human Nature" by Steven Pinker - Pinker examines how language reveals our thoughts, emotions, and beliefs, offering insights into how linguistic choices shape our understanding of the world.
> 5. "Through the Language Glass: Why the World Looks Different in Other Languages" by Guy Deutscher - Deutscher explores how different languages shape our perception of reality, challenging the notion that all languages are fundamentally similar.
> 6. "Language in Thought and Action" by S.I. Hayakawa - This classic book explores the relationship between language, thought, and behavior, highlighting how language shapes our understanding of ourselves and others.
> 7. "The Power of Babel: A Natural History of Language" by John McWhorter - McWhorter provides an overview of the diversity of human languages, discussing how they shape our thoughts and influence cultural dynamics.
> 8. "Thinking in Systems: A Primer" by Donella H. Meadows - While not specifically focused on language, this book introduces systems thinking, which can be valuable in understanding how language interacts with cognitive processes.
> 9. "Language at the Speed of Sight: How We Read, Why So Many Can't, And What Can Be Done About It" by Mark Seidenberg - Seidenberg explores the relationship between language, reading, and cognitive processes, shedding light on how language affects our thinking and learning abilities.
> 10. "The Language of Thought" by Jerry A. Fodor - Fodor explores the idea that thought is inherently linguistic, discussing how language structures our cognitive processes and shapes our understanding of the world.

Recent advances in psychology have offered new conceptual and methodological approaches to capturing the more complex “semantic space” of emotion (Cowen et al., 2019a) by studying the distribution of emotion responses to a diverse array of stimuli via computational techniques.

Studies guided by these principles have identified 27 distinct varieties of emotional experience conveyed by short videos (Cowen and Keltner, 2017), 13 by music (Cowen et al., in press), 28 by facial expression (Cowen and Keltner, 2019), 12 by speech prosody (Cowen et al., 2019b), and 24 by nonverbal vocalization (Cowen et al., 2018).

In this work, we build on these methods and findings to devise our granular taxonomy for text-based emotion recognition and study the dimensionality of language-based emotion space.
Recent advances in psychology have offered new conceptual and methodological approaches to capturing the more complex "semantic space" of emotion (Cowen et al., 2019a) by studying the distribution of emotion responses to a diverse array of stimuli via computational techniques. Studies guided by these principles have identified 27 distinct varieties of emotional experience conveyed by short videos (Cowen and Keltner, 2017), 13 by music (Cowen et al., in press), 28 by facial expression (Cowen and Keltner, 2019), 12 by speech prosody (Cowen et al., 2019b), and 24 by nonverbal vocalization (Cowen et al., 2018).

In this work, we build on these methods and findings to devise our granular taxonomy for text-based emotion recognition and study the dimensionality of language-based emotion space.
