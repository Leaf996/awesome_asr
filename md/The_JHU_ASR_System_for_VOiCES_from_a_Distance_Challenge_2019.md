# The_JHU_ASR_System_for_VOiCES_from_a_Distance_Challenge_2019
## Questions
- TODO
## Abstract
- The training data was first augmented with both background noises and simulated reverberation.
- Both systems utilized RNN language models trained on original and reversed text forrescoring.
## Introduction
- Far-field automatic speech recognition under reverberant and noisy conditions is important in real-world applications of ASR.
## Data Augmentation
- Babble
- Music
- Noise
- Reverb
## Acoustic Modeling
- We use factorized TDNN(F-TDNN) with skip connections for acoustic modeling.
## Language Modeling
- We follow Kaldi-RNNLM to train TDNN-LSTM language models using the transcripts of Librispeech-80h.