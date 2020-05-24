# 2018_icassp_semisupervised_mmi
## Questions
- TODO
## Abstract
- The lattice-free MMI objective (LF-MMI) has been used in supervised training of state-of-the-art neural network acoustic models for automatic speech recognition (ASR)
- In this paper, we describe various extensions to standard LF-MMI training to **allow the use as supervision of lattices obtained via decoding of unsupervised data**.
## Introduction
- The most common approach to semi-supervised learning is self-training.
    - The general recipe here is to use a system trained on supervised data to generate tarnscripts for unsupervised data and select the transcripts based on various confidence score based filtering schemes.
## LF-MMI training
- In this work's upsupervised scenario, we can use a `seed LF-MMI` system to dump lattices of alternate pronunciations of `the best path transcripts obtained from decoding unsupervised utterances`.
## Numerator graph creation
### Lattices: Naive splitting
- In this approach, we convert a lattice of word sequences obtained from the decoding of an utterance into phone graphs that are compiled into utterance-specific FSTs.
### Lattices: No splitting
- However, for training efficiency we ensure that all the utterances in the unsupervised dataset are modified to be of around 20 distinct lengths.