---
aliases:
  - Fourier transforms
  - Fourier transformation
  - Fourier transform
  - signal processing
  - Fourier analysis
  - Fast Fourier Transform (FFT)
  - discrete Fourier transform (DFT)
tags:
  - mathematics
  - engineering
  - computer-science
  - physics
  - signal
file-created: 2023-03-18
file-modified: 2023-09-02
note-type:
  - general
description: 
linter-yaml-title-alias: Fourier transform
---

# Fourier transform

#status/postponed

---

## What is a Fourier transform?

![[Pasted image 20230410223443.png|250]]

Fourier transform is a math technique which allows us to break down complex signals and data into individual components (similar to [[Breakdown complex problems using First Principles Thinking|first principles thinking]]) through isolating functions.

> The Fourier transform is a mathematical technique that allows us to analyze complex signals and data by breaking them down into simpler components. It transforms a signal or function **from the time domain into the frequency domain**, which enables us to understand the different frequencies that make up the signal.
>
> This transformation is achieved by decomposing a signal into a sum of sine and cosine waves of different frequencies, amplitudes, and phases. The Fourier transform has applications in various fields such as signal processing, image processing, audio engineering, and quantum mechanics.

In some ways, it seems closely related to [[Gabor functions|Gabor codes]] but this is something I don't fully understand yet. From what I understand, they're both techniques to help us dissect complex information but they take different approaches.

There also seems to be something calling the Fast Fourier Transform. I can learn more about it here: [The Fast Fourier Transform (FFT): Most Ingenious Algorithm Ever? - YouTube](https://www.youtube.com/watch?v=h7apO7q16V0)

## Fourier theorem

> Any continuous periodic function can be expressed in terms of sines and cosines.

## Understanding our ear's ability to perform Fourier transforms

A good example are our ear follicles and each length responding to a specific frequency domain. We can intuitively conceptualize it by thinking of each follicle length as its own tube which creates it own sensitivity region for human hearing.

![[Pasted image 20230318052539.png]]
![[Pasted image 20230318052500.png]]
![[Pasted image 20230318052451.png]]

## Related

- [[REF-Entropy of music and why humans like jazz]]
- [But what is the Fourier Transform? A visual introduction. - YouTube](https://www.youtube.com/watch?v=spUNpyF58BY)
- [Cochlea: function | Cochlea](http://www.cochlea.eu/en/cochlea/function)
