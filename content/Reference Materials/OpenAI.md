---
aliases:
  - OpenAI is a big player within the large language model industry
  - popular large language model
  - LLM company
  - OpenAI
  - ChatGPT
tags:
  - reference-material/read-it-later/snippet
  - productivity/tool
  - intelligence/artificial-intelligence
  - computer-science
note-type: 
description: 
file-created: 2023-03-09
file-modified: 2023-10-27
linter-yaml-title-alias: OpenAI is a big player within the large language model industry
---

#status/postponed

# OpenAI is a big player within the large language model industry

They are currently one of the biggest players within the [[Large language models produce human text using big data|large language model (LLM)]] industry.

Here are some academic papers which help illustrate how we can create better prompts for open AI: [GitHub - openai/openai-cookbook: Examples and guides for using the OpenAI API](https://github.com/openai/openai-cookbook#papers-on-advanced-prompting-to-improve-reasoning)

## Working with the OpenAI API

[[Strategies for working with large language models]]

### Context length VS Max token VS Maximum length in LLMs

This is to help understand the difference between these three concepts in working with [[Large language models produce human text using big data|large language models (LLM)]]. It's applicable to using models from [[OpenAI|OpenAI]].
1. Context length
2. Max token (parameter of API)
3. Maximum length (parameter found in Playground)

> Any API call has an _input_ and an _output_. Depending on the endpoint you use, the input equals `prompt` or `messages` parameter.
>
> The number of total tokens (input + output) allowed by OpenAI depends on the model you use: 4k for `text-davinci-003`, 8k for `gpt-4`, etc:
>
> 1- **Context length (or context window)** usually refers to the total number of tokens permitted by your model. It can also refer to the number of tokens of your input (depends on the context).
> **2 and 3 - these ones are equivalent**. They refer to the max number of tokens that you allow your API call to generate. It’s just a cap: it doesn’t mean that your call will actually generate all these tokens. It should always be less than `context_window - input_tokens`, or you’ll get an error from OpenAI.
> [Context length VS Max token VS Maximum length - API - OpenAI Developer Forum](https://community.openai.com/t/context-length-vs-max-token-vs-maximum-length/125585/2)
