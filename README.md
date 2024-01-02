[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]

## Updated on 2024.01.02
> Usage instructions: [here](./docs/README.md#usage)

<details>
  <summary>Table of Contents</summary>
  <ol>
    <li><a href=#mllm>MLLM</a></li>
  </ol>
</details>

## MLLM

|Publish Date|Title|Abstract|PDF|Code|
|---|---|-----------------------------------|---|---|
|**2023-12-28**|**Structured Packing in LLM Training Improves Long Context Utilization**|长上下文大型语言模型（LCLMs）的最新进展引起了人们的极大兴趣，尤其是在查询科学研究论文等应用中。然而，它们的潜力往往受到上下文利用不足的限制。我们将典型训练数据中缺乏长程语义依赖性确定为主要障碍。为了解决这一问题，我们深入研究了经常将相关文档纳入培训输入的好处。使用代码数据的固有目录结构作为训练示例的来源，我们展示了困惑的改善，即使是对于与编码无关的任务也是如此。在这些发现的基础上，但着眼于更广泛的领域，我们引入了长上下文结构化包装（SPLiCe）。SPLiCe是一种创新的创建训练示例的方法，它使用检索方法将最相关的文档整理到单个训练上下文中。我们的结果表明，\方法｛｝提高了模型性能，可以用于训练大型模型更好地利用长上下文。我们通过训练一个价值30亿美元的大型模型来验证我们的结果，显示出困惑的改善和下游任务上更好的长上下文性能。 et.al.|[2312.17296](http://arxiv.org/abs/2312.17296)|null|
|**2023-12-27**|**PanGu- $π$: Enhancing Language Model Architectures via Nonlinearity Compensation**|大型语言模型（LLM）最近的趋势是增加模型大小（即参数的数量）和数据集的规模，以获得更好的生成能力，这一点已经被著名的GPT和Llama等许多工作所证明。然而，大型模型往往涉及巨大的计算成本，实际应用无法承受如此高的价格。然而，构建LLM的强模型体系结构的方法很少被讨论。我们首先分析了最先进的语言模型体系结构，并观察了特征崩溃问题。基于理论分析，我们提出非线性对于语言模型也非常重要，这通常在卷积神经网络中用于视觉任务。然后引入序列通知激活函数，并进行可以忽略的微小计算，并进一步使用增广快捷方式来增强模型的非线性。然后，我们证明了所提出的方法在通过精心设计的烧蚀来增强模型非线性方面是显著有效的；因此，我们提出了一种新的建立现代有效的模型体系结构，即PanGu-$\pi$。然后使用相同的数据集和训练策略进行实验，将PanGu-$\pi$与最先进的LLM进行比较。结果表明，PanGu-$\pi$-7B可以以大约10%的推理加速实现与基准测试相当的性能，PanGu-\pi$-1B可以在准确性和效率方面实现最先进的性能。此外，我们还在金融和法律的高价值领域部署了PanGu-$\pi$ -7B，开发了一个名为云山的LLM以供实际应用。结果表明，在基准测试中，云山模型可以超越其他尺度相似的模型。 et.al.|[2312.17276](http://arxiv.org/abs/2312.17276)|null|
|**2023-12-28**|**Multi-Prompts Learning with Cross-Modal Alignment for Attribute-based Person Re-Identification**|细粒度的属性描述可以显著地补充人物图像中有价值的语义信息，这对人物重新识别任务的成功至关重要。然而，当前的ReID算法通常无法有效利用可用的丰富上下文信息，主要是因为它们依赖于图像属性的简单和粗略利用。人工智能生成内容的最新进展使自动生成大量细粒度的属性描述并充分利用它们成为可能。因此，本文探索了在现有（大型）模型的ReID任务中使用生成的多人属性作为提示的潜力，以获得更准确的检索结果。为此，我们提出了一个新的框架，称为多提示ReID（MP ReID），基于提示学习和语言模型，以充分挖掘精细属性来帮助ReID任务。具体来说，MP ReID首先学会产生幻觉，产生各种各样的、信息丰富的、可提示的句子来描述查询图像。该程序包括（i）一个人具有哪些属性的明确提示，以及（ii）用于调整/调节用于该人身份匹配的标准的隐含可学习提示。显式提示是通过集合生成模型（如ChatGPT和VQA模型）来获得的。此外，还设计了一个对齐模块，以逐步融合多提示（即显式提示和隐式提示），并减轻跨模态间隙。在现有的涉及属性的ReID数据集，即Market1501和DukeMTMC ReID上进行的大量实验证明了所提出的MP ReID解决方案的有效性和合理性。 et.al.|[2312.16797](http://arxiv.org/abs/2312.16797)|null|
|**2023-12-27**|**Mobility and Cost Aware Inference Accelerating Algorithm for Edge Intelligence**|边缘智能近年来得到了广泛的应用。在设备、边缘服务器和云之间拆分模型可以大大提高EI的性能。先前的工作已经深入研究了没有用户移动性的模型分割。然而，在EI的大多数使用情况下，终端设备是移动的。在这方面只进行了少数工作。这些工作仍然存在许多问题，如忽视移动设备的能耗、网络假设不当、自适应用户移动性的有效性低等。因此，为了解决以往工作中模型分割和资源分配的不足，我们提出了移动和成本感知的模型分割和资源分配算法，以加速边缘推理（MCSA）。具体地，在没有用户移动性的场景中，提供了循环交互梯度下降（Li-GD）算法。当移动用户有较大的模型推理任务需要计算时，它会考虑移动用户的能耗、通信和计算资源租用成本以及推理延迟，以找到最优的模型分割和资源分配策略。在具有用户移动性的场景中，提出了移动感知Li-GD（MLi-GD）算法来计算最优策略。然后，研究了所提出算法的性质，包括收敛性、复杂度和近似率。实验结果验证了所提算法的有效性。 et.al.|[2312.16497](http://arxiv.org/abs/2312.16497)|null|
|**2023-12-30**|**Group Multi-View Transformer for 3D Shape Analysis with Spatial Encoding**|近年来，基于视图的三维形状识别方法的结果已经饱和，并且具有优异性能的模型由于其庞大的参数大小而无法部署在内存有限的设备上。为了解决这个问题，我们为该领域引入了一种基于知识蒸馏的压缩方法，该方法在尽可能保持模型性能的同时，大大减少了参数的数量。具体来说，为了增强较小模型的功能，我们设计了一个高性能的大型模型，称为Group Multi-view Vision Transformer（GMViT）。在GMViT中，视图级ViT首先建立视图级特征之间的关系。此外，为了捕捉更深层次的特征，我们使用分组模块将视图级特征增强为组级特征。最后，组级ViT将组级特征聚合为完整的、良好形成的3D形状描述符。值得注意的是，在这两个ViT中，我们都引入了相机坐标的空间编码作为创新的位置嵌入。此外，我们提出了两个基于GMViT的压缩版本，即GMViT simple和GMViT mini。为了提高小模型的训练有效性，我们在整个GMViT过程中引入了一种知识提取方法，其中每个GMViT组件的关键输出作为提取目标。大量实验证明了该方法的有效性。大模型GMViT在基准数据集ModelNet、ShapeNetCore55和MCB上实现了出色的3D分类和检索结果。较小的模型GMViT simple和GMViT mini分别将参数大小减少了8倍和17.6倍，形状识别速度平均提高了1.5倍，同时保持了至少90%的分类和检索性能。 et.al.|[2312.16477](http://arxiv.org/abs/2312.16477)|null|
|**2023-12-25**|**Revisiting Knowledge Distillation under Distribution Shift**|知识提炼将知识从大模型转移到小模型，最近取得了显著的成就。然而，很少有研究探讨知识蒸馏对抗分布转移的机制。分布偏移是指训练和测试阶段之间的数据分布漂移。在这篇文章中，我们通过重新表述转移情况下的目标函数来重新考虑知识提炼的范式。在真实场景下，我们提出了一个统一而系统的框架，以对照两种普遍的分布变化（包括多样性和相关性变化）来衡量知识提取。评估基准涵盖了五个基准数据集的30多种算法、数据驱动和优化方法。总的来说，我们对学生模型进行了广泛的实验。我们揭示了分布变化下教学表现不佳的有趣观察结果；特别是，复杂的算法和数据扩充在许多情况下提供了有限的增益。 et.al.|[2312.16242](http://arxiv.org/abs/2312.16242)|null|
|**2023-12-26**|**Black-Box Tuning of Vision-Language Models with Effective Gradient Approximation**|参数有效微调（PEFT）方法为使大型视觉语言模型适应特定任务或场景提供了一种有效的方法。通常，他们在白盒公式中为预先训练的模型学习非常小范围的参数，该公式假设模型架构是已知的，参数是可访问的。然而，出于防止滥用或商业因素的考虑，大型模型往往不是开源的，因此对白盒PEFT方法的部署构成了障碍。为了减轻对模型可访问性的依赖，我们引入了协作黑盒调优（CBBT），用于黑盒模型的文本提示优化和输出特征自适应。具体来说，考虑到反向传播梯度被阻塞，我们通过分析具有扰动提示的预测来近似文本提示的梯度。其次，在不可访问模型的输出特性上部署了一个轻量级适配器，进一步方便了模型的自适应过程。有了这些设计，我们的CBBT在11个下游基准上进行了广泛评估，与现有的黑盒VL自适应方法相比，取得了显著的改进。代码发布于https://github.com/guozix/cbbt. et.al.|[2312.15901](http://arxiv.org/abs/2312.15901)|**[link](https://github.com/guozix/cbbt)**|
|**2023-12-26**|**High Efficiency Inference Accelerating Algorithm for NOMA-based Mobile Edge Computing**|在设备、边缘服务器和云之间拆分推理模型可以大大提高EI的性能。此外，非正交多址（NOMA）作为B5G/6G的关键支持技术，可以实现大规模连接和高频谱效率。受NOMA优点的启发，将NOMA与MEC中的模型分割相结合以减少推理延迟变得更有吸引力。然而，在以前的工作中，没有适当考虑分裂推理过程中基于NOMA的通信。因此，在本文中，我们将NOMA集成到MEC中的分裂推理中，并提出了有效的通信和计算资源分配算法来加速边缘的模型推理。具体来说，当移动用户在基于NOMA的MEC中有大量的模型推理任务需要计算时，它将考虑设备和边缘服务器的能耗以及推理延迟，以找到最佳的模型分割策略、子信道分配策略（上行链路和下行链路）和传输功率分配策略（下行链路和上行链路）。由于不能同时满足最小推理延迟和能量消耗，并且子信道分配和模型分割的变量是离散的，因此采用梯度下降算法来寻找它们之间的最优折衷。此外，还提出了循环迭代GD方法（Li-GD），以降低参数离散引起的GD算法的复杂度。此外，还研究了所提出的算法的性质，证明了所提出算法的有效性。 et.al.|[2312.15850](http://arxiv.org/abs/2312.15850)|null|
|**2023-12-25**|**IQAGPT: Image Quality Assessment with Vision-language and ChatGPT Models**|大型语言模型（LLM），如ChatGPT，在各种任务中表现出了令人印象深刻的功能，并作为跨许多领域的自然语言接口吸引了越来越多的兴趣。最近，像BLIP-2和GPT-4这样的大型视觉语言模型（VLM）被深入研究，它们从图像-文本对中学习丰富的视觉语言相关性。然而，尽管有这些发展，LLM和VLM在图像质量评估（IQA）中的应用，特别是在医学成像中的应用仍有待探索，这对于客观的性能评估和放射科医生意见的潜在补充甚至替代是有价值的。为此，本文介绍了IQAGPT，这是一种创新的图像质量评估系统，将图像质量字幕VLM与ChatGPT集成在一起，用于生成质量分数和文本报告。首先，我们构建了一个用于训练和评估的CT-IQA数据集，包括1000个具有不同质量水平的专业注释的CT切片。为了更好地利用LLM的功能，我们使用提示模板将带注释的质量分数转换为语义丰富的文本描述。其次，我们对CT-IQA数据集上的图像质量字幕VLM进行微调，以生成质量描述。字幕模型通过跨模态注意力融合了图像和文本特征。第三，基于质量描述，用户可以与ChatGPT对话，对图像质量分数进行评分或生成放射质量报告。我们的初步结果证明了用大型模型评估图像质量的可行性。值得注意的是，我们的IQAGPT优于GPT-4和CLIP-IQA，以及仅依赖图像的多任务分类和回归模型。 et.al.|[2312.15663](http://arxiv.org/abs/2312.15663)|null|
|**2023-12-24**|**Fairness-Aware Structured Pruning in Transformers**|大型语言模型（LLM）的规模不断扩大，给它们的训练和推理带来了挑战。删除模型组件被视为解决大模型大小的解决方案，然而，现有的修剪方法只关注性能，而没有考虑LLM的负责任使用的一个重要方面：模型公平性。至关重要的是，要解决LLM对不同群体的公平性问题，如妇女、黑人、LGBTQ+、犹太社区等，因为LLM正在部署并向广大受众开放。在这项工作中，首先，我们研究了在预先训练的基于transformer的语言模型中，注意力头如何影响公平性和性能。然后，我们提出了一种新的方法来修剪对公平性产生负面影响的注意力头部，同时保留对性能至关重要的头部，即语言建模能力。我们的方法在时间和资源方面是实用的，因为它不需要对最终修剪过的、更公平的模型进行微调。我们的研究结果表明，与有偏见的模型相比，两种不同大小的DistilGPT-2、GPT-2和GPT-Neo模型（GPT-J和Llama 2模型）的性别偏见分别减少了19%、19.5%、39.5%、34.7%、23%和8%，性能仅略有下降。 et.al.|[2312.15398](http://arxiv.org/abs/2312.15398)|null|

<p align=right>(<a href=#updated-on-20240102>back to top</a>)</p>

[contributors-shield]: https://img.shields.io/github/contributors/Vincentqyw/cv-arxiv-daily.svg?style=for-the-badge
[contributors-url]: https://github.com/Vincentqyw/cv-arxiv-daily/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/Vincentqyw/cv-arxiv-daily.svg?style=for-the-badge
[forks-url]: https://github.com/Vincentqyw/cv-arxiv-daily/network/members
[stars-shield]: https://img.shields.io/github/stars/Vincentqyw/cv-arxiv-daily.svg?style=for-the-badge
[stars-url]: https://github.com/Vincentqyw/cv-arxiv-daily/stargazers
[issues-shield]: https://img.shields.io/github/issues/Vincentqyw/cv-arxiv-daily.svg?style=for-the-badge
[issues-url]: https://github.com/Vincentqyw/cv-arxiv-daily/issues

