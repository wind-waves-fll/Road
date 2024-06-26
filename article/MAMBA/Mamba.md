doi:https://arxiv.org/abs/2312.00752
# Mamba: Linear-Time Sequence Modeling with Selective State Spaces
## ABSTRACT
在深度学习上很多表现优秀的模型大多数都是基于Transformer架构和它的注意力机制。
许多次二次时间结构，如线性注意力、门控卷积和递归模型以及结构化状态空间模型（SSM），已经被开发出来，以解决变压器在长序列上的计算效率低的问题，但他们并不能和attention一样表现得很好。
我们发现这种模型的一个关键弱点是它们无法执行基于内容的推理，并进行了一些改进。
首先，简单地让SSM参数是输入的函数，就可以用离散模态来解决它们的弱点，允许模型根据当前令牌沿着序列长度维度选择性地传播或忘记信息。
其次，尽管这种变化阻止了高效卷积的使用，但我们在递归模式下设计了一种硬件感知的并行算法。我们将这些选择性SSM集成到一个简化的端到端神经网络架构中，而无需注意，甚至无需MLP块（Mamba）。Mamba具有快速推理（比Transformers高5倍的吞吐量）和序列长度的线性缩放，其性能在高达百万长度的真实数据序列上得到了提高。
作为通用序列模型的主干，Mamba在语言、音频和基因组学等多种模式中实现了最先进的性能。
在语言建模方面，我们的Mamba-3B模型在预训练和下游评估方面都优于相同大小的Transformers，并与两倍于其大小的Transformer相匹配。
