# An_Overview_of_Noise-Robust_Automatic_Speech_Recognition
## Abstract
- Specifically, we have analyzed and categorized a wide range of noise-robust techniques using five different criteria:
    - feature-domain vs. model-domain
    - the use of prior knowledge about the acoustic environment distortion
    - the use of explicit environment-distortion models
    - deterministic vs. uncertainty
    - the use of acoustic models trained jointly with the same feature enhancement or model adaptation process used in the testing stage
## The background and scope
- A natural way to deal with noise in the acoustic environment is to use multi-style training, which train the acoustic model with all availabel noisy speedh data. The hope is that one of the noise types in the training set will appear in the deployment scenario. However, there are two major problems with multi-style training:
    - during training, it is hard to enumerate all noise types and SNRs encountered in test environments
    - the model trained with multi-style training has a very broad distribution because it needs to model all the environments.
- Given the unsatisfactory behavior of multi-style training, it is necessary to work on technologies that directly deal with the noise and channel impacts.