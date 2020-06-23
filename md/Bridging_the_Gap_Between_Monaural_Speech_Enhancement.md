# Bridging the Gap Between Monaural(单声道) Speech Enhancement and Recognition with Distortion-Independent(扭曲独立) Acoustic Modeling
## Key Word
- Monaural Speech Enhancement
- Distortion-Independent Acoustic Modeling
- additive noise vs. reverberation
## Abstract
- Although enhanced speech has been demonstrated to have better intelligibility and quality for human listeners, feeding it directly to automatic speech recognition (ASR) systems trained with **noisy** speech has not produced expected improvements in ASR performance.
## Introduction
- Along with the progress in speech enhancement, researchers have investigated using speech enhancement models as frontends for automatic speech recognition systems.
- With a Gaussian mixture model (GMM) as backend, the enhancement frontend was shown to reduce word error rate (WER) significantly. In a subsequent paper using DNN as backend, the benefit of speech ehnahcement is **mixed**, depending on training features.
- One way to alleviate the distortion problem is to reduce or eliminate speech distortions in enhancement frontends.
- `In this study, we analyze the distortion problem by viewing it as a noise mismatch between training and testing.`
## System Description
- The **distortion** in this study refers to the alteration to clean speech signal introduced by speech enhancement that may cause performance degradation in an ASR system.
- Since this strategy typically used a large variety of additive noises to train acoustic models, we denote it **noise-independent** acoustic modeling. An advantage of noise-independent training is that its efficacy is not influenced by speech enhancement frontends.
- Another strategy to alleviate the distortion problem is to train the acoustic model directly with enhanced speech.
## Concluding Remarks
- Distortion-independent acoustic modeling emerges as the best among the five acoustic models.