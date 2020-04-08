## SpecAugment
### Questions
- SpecAugment is suitable for traditional asr ?
- What does time-warping do ?


### Key Concepts
- warping the features(time warp)
- masking blocks of frequency
- masking blocks of time steps
- LAS(listen, attend and spell)
- Similiar to **unsupervised pre-training**
- **Label smoothing**


### Methods
- Vocal Tract Length Normalization(VTLN)
- Noisy Data Synthesised
- Speed Perturbation
- Acoustic Room Simulator


### Reference Repo
- [SpecAugment][1]
- [las][3]
- [clova-speech-hackathon][4]
- [**sparse_image_warp_pytorch**][5]
- [**espnet.transform.spec_augment**][6]


### Reference Blog
- [SpecAugment][2]


### TODO
- [ ] Reference paper
- [ ] Implement SpecAugment with numpy


[1]:https://github.com/DemisEom/SpecAugment
[2]:https://ai.googleblog.com/2019/04/specaugment-new-data-augmentation.html
[3]:https://github.com/hgstudent/las
[4]:https://github.com/jw9730/clova-speech-hackathon
[5]:https://github.com/bobchennan/sparse_image_warp_pytorch
[6]:https://espnet.github.io/espnet/_modules/espnet/transform/spec_augment.html