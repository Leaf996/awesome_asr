# 2015_interspeech_aspire
## Abstract
- In reverberant environments there are long term interactions between speech and corupting sources.
## Introduction
- In reverberant environments the reflections of the signal affect the signal over several time frames. Recurrent neural networks (RNNs) which use a dynamically changing contextual window over all of the sequence history rather than a fixed context window are a viable choice for learning reverberation robust representations.
## Relevant Prior Work
- `Signal and feature enhancement` techniques are widely used to tackle reverberation in ASR systems using standard acoustic models.
- Reverberant speech is assumed to be composed of direct-path response, early reflections and late reverberations.
    - Early reflection : Reflections within a delay of **50ms** of the direct signal are categorized as early reflections.
    - Late reverberations : which comprise of later reflections, have reverberation time from **200 to 1000ms** in typical office environments.
## Neural Network Architecture
- In a TDNN architecture the initial transforms are learnt on narrow contexts and the deeper layers process the hidden activations from increasingly wider contexts.
## iVector Extraction
- We found empirically that excluding the silence from the statistics for iVector estimation was very helpful.
## Experimental Setup
- Multi-condition training data was created by distorting speech with real world room impulse response (RIR) and noise recordings available from three different databases vis., the **RWCP** sound scene database, the **REVERB** challenge database, and the **Aachen** impulse response database.
- Speed perturbation, which emulates `pitch and tempo` variations in speech, was shown to provide on average 4.3% relative gain in a variety of LVCSR tasks.