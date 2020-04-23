# Purely sequence-trained neural networks for ASR based on lattice-free MMI
## Question
- How to understand **CTC locally normalized** and **MMI globally normalized** ?
## Key Concepts
- LF-MMI
- sequence discriminative training
- phone n-gram language model
- forward-backward algorithm
- **Without the need for frame-level cross-entropy pre-training**
## Knowledge
- Sequence discriminative training of neural networks for Automatic Speech Recognition(ASR) has been shown to provide significant reduction in word error rates(WERs), vs. crossentropy training
- Recently, Connectionist Temporal Classification(CTC) has attracted a lot of attention in speech recognition applications, although **the only reports of its success have been with huge amounts of data**
- The computation of the derivatives of the objective function requires us to compute two sets of posterior quantities: one from the `numerator graph`, which is specific to each utterance and which encodes the supervision information; and one for the `denominator graph`, which encodes all possible word sequences and which is the same for all utterances.