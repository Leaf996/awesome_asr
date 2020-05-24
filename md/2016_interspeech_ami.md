# 2016_interspeech_ami
## Questions
- **alignments from close-talk microphone data** vs. **alignments from distant-talk microphone data**
## Abstract
- In far-field speech recognition systems, training acoustic models with alignments generated from parallel close-talk microphone data provides significant improvements.
## Introduction
- In far-field speech recognition systems, alignments for training the acoustic models are typically generated using the distant microphoen recordings.
- parallel data
    - the training data recorded with both distant and close-talk microphone, e.e. AMI meeting corpus
    - the far-field audio is simulated by distorting close-talk microphoen recordings, e.g. ASpIRE, REVERB-2014
- Empirical analysis shows that the use of these comparatively higher quality alignments leads to significant improvements, **~8%** relative improvement in word error rate
- pronged strategy
    - Firstly, we use the LF-MMI objective function, which is tolerant to minor mis-alignment errors
    - Secondly, we propose a `quality estimate` which is used for selecting reliable utterances for training
## Analysis of alignment errors
### Minor mis-alignment errors
- A majority of the errors were `minor` mis-alignment errors
### Speaker overlap errors
- In a significant number of utterances, there were speaker overlaps in both IHM and SDM audio.
### Transcription errors
- As in other databases, there were minor transcription errors.
## Proposed techniques
### LF_MMI objective
- However, our interest in this objective function arises from the fact that it is `inherently tolerant to alignment errors`, as we can specify a range of time frames for a particular context-dependent phone state using a desired tolerance.
- Prior to training the neural net, a GMM-based system is used to generate lattices representing alternative pronunciations of the training utterances.
### Lattice oracle WER
- edit distance
- One drawback of this approach is that short segments that have a single word in the reference will almost always be given an oracle WER of 0
## Experimental Setup
- We perform speaker-adaptive training of the HMM-GMM systems, as we found the alignments from SAT HMM-GMM systems to be beneficial for neural network training
- beam-forming: [BeamformIt][1]


[1]:https://github.com/xanguera/BeamformIt