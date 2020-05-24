# 2017_icassp_reverberation
## Questions
- How many point-source noise to be added ?
## Abstract
- The environmental robustness of DNN-based acoustic models can be `significantly improved` by using `multicondition training data`.
- We find that the performance gap between using simulated and readl RIRs can be eliminated when point-source noises are added.
- Further we show that the trained acoustic models not only perform well in the distant-talking scenario but also provide better results in the close-talking scenario.
## Introduction
- A DNN is unable to extrapolate to test samples that are sufficiently different from the training examples.
- Multi-style training is a widely adopted strategy to train robust acoustic models.
- `Far-field data typically has reverberated speech and point-source noises, in addition to the isotropic noise at the receiver position`.
- Among the other things, these RIRs are affected by the room, receiver position and type, speaker position and positions of different obstacles.
## Simulation of far-field speech
### Room Impulse Responses
- Real RIRs
    - the RWCP sound scene database
    - the REVERB challenge database
    - the Aachen impulse reponse database
- Simulated RIRs
    - image method
    - One of the significant differences between the two RIRs is the lack of rich `late-reverberations` in the simulated RIR.
### Noises
- The isotropic noises available in the real RER database
- The point-source noises are sampled from the `Freesound portion of the MUSAN corpus`
## Experimental setup
- The LF-MMI criterion was used to train the acoustic models
- `Clean data` was used to generate the decision tree for context-dependent state clustering and the numerator lattices for LF-MMI training.
## Room Impulse Response Generator
- [RIR-Generator][1]


[1]:https://github.com/ehabets/RIR-Generator