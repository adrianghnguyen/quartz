---
dg-publish: 
aliases:
  - Quantization
  - machine learning model optimization
  - machine learning model compression technique
  - quantization
tags: 
note-type:
  - general
description: 
file-created: 2023-10-19
file-modified: 2023-10-19
linter-yaml-title-alias: Quantization
review:
---

# Quantization

#status/postponed 

---

## Quantization in machine learning and artificial intelligence

> Quantization is a model size reduction technique that converts model weights from high-precision floating-point representation to low-precision floating-point (FP) or integer (INT) representations, such as 16-bit or 8-bit.
> 
> [The Ultimate Guide to Deep Learning Model Quantization and Quantization-Aware Training | Deci](https://deci.ai/quantization-and-quantization-aware-training/#:~:text=Quantization%20is%20a%20model%20size,%2Dbit%20or%208%2Dbit.)


It's an optimization technique used in [[Deep neural networks|deep neural networks]] which can be used to reduce the size of a model to a smaller size by reducing its precision, model size and inference speed without sacrificing too much speed. One way to think about quantization is that it's similar to compression techniques for images. 

I became curious to learn more about this as I started experimenting with LM studio which relies on the [[Machine learning collaboration platforms|HuggingFace]]. When selecting models to choose from and play with, there are options to change quantized models so I wanted to understand what it meant exactly. 

