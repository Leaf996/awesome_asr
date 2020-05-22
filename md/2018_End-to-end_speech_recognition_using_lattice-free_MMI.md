# 2018_End-to-end_speech_recognition_using_lattice-free_MMI
## Questions
- How to understand full biphones ?
- How to understand composite HMM and acyclic graph ?
## Abstract
- By end-to-end training, we mean `flat-start` training of a single DNN in `one stage without using any previously trained models, forced alignments, or building state-typing decision trees`.
## Introduction
- E2E approaches
    - CTC
    - RNN-T
    - Attention-Based(`Very Large Dataset`)
## Regular LF-MMI
- objective function
    - ML(Maximum likelihood)
    - MMI(Maximum mutual information)
- The Denominator graph has traditionally been estimated using n-best and later using lattices.
- `The phone LM for the denominator graph was pruned n-gram LM trained using the phone alignments of the training data`
## CTC
- The CTC objective function can be thought of as the HMM likelihood over a composite HMM, where each label (e.g. a character, in character-based CTC) has a special 2-state HMM topology
## Eend-to-End LF-MMI
- In regular LF-MMI, the DNN outputs correspond to tied biphone or triphoen HMM states, where the tying is done according to a context-dependency tree.
- To enable context-dependent modeling in an end-to-end manner, we adopt a simple approach where we use full left biphones(or bichars in the character-based case). This will create biphones that never occur in the training data, but they are never activated during training and the network learns to ignore them.
## Experiments
- In regular LF-MMI, all utterances are split into chunks of 150 frames to make GPU computations efficient. However, in end-to-end LF-MMI, we can't split the utterances because we don't have alignments.
## Repo
- [PyTorch implementation of LF-MMI for End-to-end ASR ][1]


[1]:https://github.com/YiwenShaoStephen/pychain