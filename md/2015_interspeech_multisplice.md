# A time delay neural network architecture for efficient modeling of long temporal contexts
## Abstract
- TDNN architecture in learning wider temporal dependencies in both small and large data scenarios.
## Introduction
- Modeling the temporal dynamics in speech, to capture the long term dependencies between acoustic events, requires an acoustic model which can effectively deal with long temporal contexts.
- Two types of approaches to exploit long term temporal contexts:
    - feature-based
    - model-based
- Neural network architectures have been shown to benefit from speaker adaptation. iVectors which capture both speaker and environment specific information have been shown to be useful for instantaneout and discriminative adaptation of the neural network adaptation.
## Relevant work
- Through unfolding of the recurrent network during training, matrix-matrix operations can be exploited to speed-up training. However the unfolded RNN still has dependencies across hidden-representations computed for various time-steps.
## Neural network architecture
- The transforms in the TDNN architecture are tied across time steps and for this reason they are seen as a precursor to the convolutional neural networks. During back-propagation, due to typing, the lower layers of the network are updated by a gradient accumulated over all the time steps of the input temporal context. Thus the lower layers of the network are forced to learn translation invariant feature transforms.
- Empirically we found that what seems to work best is to splice together increasingly wide context as we go to higherlayers of the network.