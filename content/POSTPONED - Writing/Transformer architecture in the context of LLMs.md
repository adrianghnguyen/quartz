---
note-type:
  - general
aliases: 
 - Transformer architecture in the context of LLMs
---

#status/postponed 

Related to [[Large language models produce human text using big data]]

---

## Transformer architecture in the context of LLMs

> [!ai]+ AI
>
> Transformers are a type of deep learning model that have revolutionized natural language processing tasks. They are based on a self-attention mechanism that allows them to capture dependencies between words in a sentence. Unlike traditional recurrent neural networks (RNNs), transformers can process sentences in parallel, making them more efficient. Transformers have achieved state-of-the-art performance in various NLP tasks, such as machine translation, sentiment analysis, and question answering. They are widely used in modern language models like GPT-3 and BERT.
>
> Fun fact: GPT stands for Generative-Pretrained Transformer.

- Read more: [Introduction to Large Language Models and the Transformer Architecture | by Pradeep Menon | Medium](https://rpradeepmenon.medium.com/introduction-to-large-language-models-and-the-transformer-architecture-534408ed7e61)
- [Transformers, Explained: Understand the Model Behind GPT-3, BERT, and T5](https://daleonai.com/transformers-explained)

It is the fundamental building block of all language models which use transformers which has gained a lot of popularity with current [[Large language models produce human text using big data|LLMs]]. It's one architecture style and is a peer to Recurrent Neural networks (RNNs) or Long short-term memory (LSTMs) for [[Natural Language Processing (NLP)|natural language processing (NLP)]].

It was established as a groundbreaking technique in the paper Attention is All You Need and uses an 'attention technique' which allows is to decipher entire inputs at once rather than individual tokens and does not run into the issue of too many layers (vanishing gradient problem apparently) that occurs in LSTMs.

Three core advantages of transformers^[https://daleonai.com/transformers-explained]
1. Positional Encodings
2. Attention
3. Self-Attention

> - It lets the model selectively focus on different parts of the input sequence instead of treating everything the same way.
> - It can capture relationships between inputs far away from each other in the sequence, which is helpful for natural language tasks.
> - It needs fewer parameters to model long-term dependencies since it only has to pay attention to the inputs that matter.
> - It’s really good at handling inputs of different lengths since it can adjust its attention based on the sequence length.

