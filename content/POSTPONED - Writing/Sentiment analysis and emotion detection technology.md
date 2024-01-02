---
dg-publish: 
aliases:
  - Sentiment analysis
  - sentiment analysis
  - computational technique used to classify and analyze text data in order to determine the sentiment expressed within
  - extracting subjective information from text
  - Sentiment analysis
  - detecting empathy in text
  - cues for empathy in conversation
  - detect text cues for empathy
  - detecting empathy cues in text
  - emotion encoding
  - intent classification
  - emotion classification
  - emotion detection
  - detect emotions
tags:
  - intelligence/artificial-intelligence
  - society/healthcare
  - psychology/therapy
note-type:
  - general
description: 
file-created: 2023-09-06
file-modified: 2023-10-26
linter-yaml-title-alias: Sentiment analysis
review:
---

# Sentiment analysis

#status/postponed

---

Related to [[Natural Language Processing (NLP)]]

Sentiment analysis, also known as opinion mining, is a computational technique used to classify and analyze text data in order to determine the sentiment expressed within. It involves extracting subjective information from text to identify whether the expressed sentiment is positive, negative, or neutral.  It seems closely related to the concept of intent classification.

Sentiment analysis utilizes natural language processing (NLP) techniques, machine learning algorithms, and lexicon-based methods to capture and interpret sentiments. By analyzing the sentiment of text data, businesses and organizations can gain valuable insights into public opinions, text cues for empathy, customer satisfaction.

For example in [[Artificial intelligence (AI) in mental healthcare technologies|mental healthcare technologies using artificial intelligence (AI)]], researchers were able to detect text cues for empathy.

## RoBERTa - A Robustly Optimized BERT Pretraining Approach

It seems that one of the most popular models for [[Sentiment analysis and emotion detection technology|intent classification]] is called RoBERTa. 

According to this article, [RoBERTa vs. GPT: A Comprehensive Comparison of State-of-the-Art Language Models, with Expert Insights from CronJ | by liva jorge | Medium](https://medium.com/@livajorge7/roberta-vs-86ee82a44969#:~:text=Bidirectionality%3A%20RoBERTa%20processes%20input%20sequences,left%20to%20right%20(4).), RoBERTa is better at deep contextual understanding which allows it to be a bit better at  sentiment analysis, question-answering, and named entity recognition. This contrastes something like GPT which is better at text generation. 


## Tech stack for sentiment analysis

Some people used RoBERTa to train it to detect Ekman's 6 basic emotions
- [j-hartmann/emotion-english-roberta-large · Hugging Face](https://huggingface.co/j-hartmann/emotion-english-roberta-large)
- [michellejieli/emotion\_text\_classifier · Hugging Face](https://huggingface.co/michellejieli/emotion_text_classifier)
	- this one is a bit better as it was trained on a dataset from the show friends but I still feel like there might be potential weaknesses

But I feel like the model is still quite weak.

- [GitHub - helliun/perspectives: Pandas-based library for emotion graphing and semantic search with LMs](https://github.com/helliun/perspectives)
- [j-hartmann/emotion-english-roberta-large · Hugging Face](https://huggingface.co/j-hartmann/emotion-english-roberta-large)

## Extracting meanings and empathy cues from text

Related to [[REF Augmenting Psychotherapy with AI]]

There is [[Artificial intelligence (AI) in mental healthcare technologies|potential use for AI (artificial intelligence) in healthcare and  therapeutic settings]] to extract meaning from texts and encode emotions such as [[Empathy is the ability to relate to others|empathy]] using [[Natural Language Processing (NLP)|NLP systems]].

- A key topic is to determine if [[Natural Language Processing (NLP)|NLP systems]] are able to extract meaningful information from therapy sessions.

### Epitome linguistic computational framework for expressed empathy

Researchers within the paper [[2009.08441] A Computational Approach to Understanding Empathy Expressed in Text-Based Mental Health Support](https://arxiv.org/abs/2009.08441)^[https://arxiv.org/pdf/2009.08441.pdf] developed a computational linguistic framework called EPITOME which can detect empathy cues within texts.

It uses a multi-task bi-encoder model based on RoBERTa.
> [!ai]+ AI
>
> A multi-task bi-encoder model based on RoBERTa is a type of natural language processing model that is designed to handle multiple tasks simultaneously. It uses the RoBERTa architecture, which is a variant of the popular BERT model, known for its strong performance in language understanding tasks. The bi-encoder structure means that it has separate encoders for input and output representations, allowing it to encode and decode information efficiently. This model can be used for various tasks such as text classification, named entity recognition, sentiment analysis, and question answering. Its ability to handle multiple tasks makes it a versatile and powerful tool in natural language processing.

Their experiment was run on online text forums to limit transcription issues, from TalkLife and Reddit.

> [!ai]+ AI
>
> The text introduces EPITOME, a conceptual framework that aims to understand empathy in text-based, asynchronous, peer-to-peer support conversations. The framework consists of three communication mechanisms: Emotional Reactions, Interpretations, and Explorations.
>
> - Emotional Reactions involve expressing emotions such as warmth and compassion in response to the seeker's post.
> - Interpretations involve communicating an understanding of the seeker's feelings and experiences inferred from their post.
> - Explorations focus on improving understanding by probing gently into the seeker's unexpressed feelings and experiences.
>
>   The framework differentiates between weak and strong expressions of empathy for each mechanism. The text also states that responses that give advice, provide factual information, or are offensive or abusive are not considered empathic within this framework.
