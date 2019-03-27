# Introduction

Clear **hypothesis** statement

Hypothesis is several:

- attention helps create better melodies in LSTM networks
  - solving the problem of structure from the Challenges paper
- dataset contents greatly influences generated melodies.
  - a homogenous dataset can create better melodies (closer to training set), but is limited to that style
  - heterogenous creates less coherent melodies, but are more stylistically varied
- encoding greatly influences quality of generated melodies and training process
  - than traditional pianoroll encoding it's smaller 
  - creates better melodies

Rigorous **methodology**

- compare attention with model that does not have attention mechanism
- compare results from homogenous and heterogenous datasets
- compare results from score encoding with results from pianoroll encoding

**Error** analysis - relation to hypothesis

- objective metrics
  - tools
    - mgeval
    - jsymbolic
  - comparison with training data
- subjective evaluation
  - turing test
  - quality scale

Motivation

- these are tools that can greatly help a musician in composing new ideas
- this is one of the many ways in which technology can be used as a tool for creativity (list others)

Sell the reader

Plan for the rest of the paper
