# Lower_Frame_Rate_Neural_Network_Acoustic_Models
## Abstract
- As opposed to conventional models, CTC learns an alignment jointly with the acoustic model, and outputs a blank symbol in addition to the regular acoustic state units. This allows the CTC model to run with a lower frame rate, outputting decisions every 30ms rather than 10ms as in conventional models, thus improving overall system speed.
## Introduction
- CTC drawbacks
    - severly overfit to the training data
    - arbitrarily delay
## Acoustic Modeling with LSTM RNNs
- hard alignments : Viterbi
- soft alignments : Baum-welch