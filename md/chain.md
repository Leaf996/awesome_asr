# Chain Model
## 简介
- 在语音识别领域，与交叉熵训练(Cross-Entropy Training)相比，序列鉴别性训练(Sequence Discriminative Training)能够显著提升语音识别系统的性能。序列鉴别性训练需要**所有的可能的单词序列**组合来做训练，一般而言我们会首先用交叉熵训练一个模型，配合使用一个**相对较弱的语言模型**来生成相应的**词图(Lattice)**。Lattice里面除了包含正确识别结果相对应的路径外，还包含了与正确路径足够接近的其它路径，鉴别性训练就是要**提高模型走正确路径的概率，同时降低走相似路径的概率**。
- 近年来CTC(Connectionist Temporal Classification)在语音识别领域受到很大关注，但相比传统模型，CTC的优势需要在很大的数据集上才能体现出来。与鉴别性训练中常用的MMI(Maximum Mutual Information)准则类似，CTC训练准则的目标是最大化正确标注的条件概率(Locally-Normalized)，而MMI着重优化正确路径和其他相似路径的概率差(Global-Normalized)。
- LF-MMI训练准则能够在训练过程中直接计算所有可能路径的后验概率(Posterior Probability)，省去了区分性训练前需要提前生成Lattice的麻烦，所以这种方法被叫做Lattice-Free MMI。
## 参考
- [kaldi chain model][1]
- [kaldi中的chain model(LFMMI)详解][2]
- [Kaldi Chain model 文件解析][3]


[1]:https://liuyanfeier.github.io/2018/05/08/kaldi-chain-model/
[2]:https://zhuanlan.zhihu.com/p/65557682
[3]:https://www.jianshu.com/p/51278adfffde