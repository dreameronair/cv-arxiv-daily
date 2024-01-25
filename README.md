[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]

## Updated on 2024.01.25
> Usage instructions: [here](./docs/README.md#usage)

<details>
  <summary>Table of Contents</summary>
  <ol>
    <li><a href=#3d>3D</a></li>
    <li><a href=#mllm>MLLM</a></li>
    <li><a href=#diffusion>Diffusion</a></li>
    <li><a href=#avatar>avatar</a></li>
  </ol>
</details>

## 3D

|Publish Date|Title|Abstract|PDF|Code|
|---|---|-----------------------------------|---|---|
|**2024-01-23**|**IRIS: Inverse Rendering of Indoor Scenes from Low Dynamic Range Images**|尽管许多3D重建和新颖的视图合成方法允许从消费者相机轻松捕捉的多视图图像中真实地渲染场景，但它们在表示中烘焙照明，无法支持高级应用程序，如材质编辑、重新照明和虚拟对象插入。通过反向渲染重建基于物理的材料特性和照明有望实现此类应用。然而，大多数反向渲染技术都需要高动态范围（HDR）图像作为输入，这是大多数用户无法访问的设置。我们提出了一种方法，从多视图、低动态范围（LDR）图像中恢复场景的基于物理的材料特性和空间变化的HDR照明。我们在反向渲染管道中对LDR图像形成过程进行建模，并提出了一种新的材料、照明和相机响应模型的优化策略。与采用LDR或HDR输入的最先进的反向渲染方法相比，我们使用合成场景和真实场景来评估我们的方法。我们的方法优于以LDR图像作为输入的现有方法，并允许高度逼真的重新照明和对象插入。 et.al.|[2401.12977](http://arxiv.org/abs/2401.12977)|null|
|**2024-01-24**|**RGBD Objects in the Wild: Scaling Real-World 3D Object Learning from RGB-D Videos**|我们介绍了一种新的在野外捕获的RGB-D对象数据集，称为WildRGB-D。与大多数现有的仅带有RGB捕获的以对象为中心的真实世界数据集不同，深度通道的直接捕获允许更好的3D注释和更广泛的下游应用。WildRGB-D包括大型类别级RGB-D对象视频，这些视频是用iPhone 360度环绕对象拍摄的。它包含大约8500个记录对象和近20000个RGB-D视频，涉及46个常见对象类别。这些视频是在三种设置的不同杂乱背景下拍摄的，以覆盖尽可能多的真实世界场景：（i）一个视频中的单个对象；（ii）一个视频中的多个对象；以及（iii）在一个视频中具有静止手的对象。该数据集由对象遮罩、真实世界比例的相机姿态和RGBD视频中重建的聚合点云进行注释。我们用WildRGB-D对四个任务进行了基准测试，包括新颖的视图合成、相机姿态估计、物体6d姿态估计和物体表面重建。我们的实验表明，RGB-D对象的大规模捕获为推进3D对象学习提供了巨大的潜力。我们的项目页面是https://wildrgbd.github.io/. et.al.|[2401.12592](http://arxiv.org/abs/2401.12592)|null|
|**2024-01-23**|**Methods and strategies for improving the novel view synthesis quality of neural radiation field**|神经辐射场（NeRF）技术可以从2D图像中学习场景的3D隐式模型，并合成逼真的新视图图像。该技术得到了业界的广泛关注，具有良好的应用前景。针对NeRF图像渲染质量需要提高的问题，近三年来，许多研究人员提出了各种方法来提高渲染质量。对最新的相关论文进行了分类和综述，分析了质量改进背后的技术原理，并讨论了质量改进方法的未来发展方向。这项研究可以帮助研究人员快速了解该领域技术的现状和发展脉络，有助于激发更高效算法的发展，促进NeRF技术在相关领域的应用。 et.al.|[2401.12451](http://arxiv.org/abs/2401.12451)|null|
|**2024-01-22**|**HG3-NeRF: Hierarchical Geometric, Semantic, and Photometric Guided Neural Radiance Fields for Sparse View Inputs**|神经辐射场（NeRF）作为一种通过从离散观测中学习场景表示的新型视图合成范式，已经引起了人们的极大关注。然而，当面对稀疏视图输入时，NeRF表现出明显的性能退化，从而限制了其进一步的适用性。在这项工作中，我们介绍了层次几何、语义和光度引导的NeRF（HG3-NeRF），这是一种新的方法，可以解决上述限制，并增强不同视图中几何、语义内容和外观的一致性。我们提出了分层几何制导（HGG），将运动结构的附加（SfM），即稀疏深度先验，纳入场景表示中。与直接深度监督不同，HGG从局部几何区域到全局几何区域对体积点进行采样，减轻了深度先验中固有偏差引起的偏差。此外，我们从不同分辨率的图像中观察到的语义一致性的显著变化中获得了灵感，并提出了层次语义引导（HSG）来学习粗到细的语义内容，该内容对应于粗到细场景表示。实验结果表明，HG3-NeRF可以在不同的标准基准上优于其他最先进的方法，并实现稀疏视图输入的高保真度合成结果。 et.al.|[2401.11711](http://arxiv.org/abs/2401.11711)|null|
|**2024-01-18**|**Explaining the Implicit Neural Canvas: Connecting Pixels to Neurons by Tracing their Contributions**|隐式神经表示（INRs）的许多变体，其中神经网络被训练为信号的连续表示，对于下游任务具有巨大的实用性，包括新颖的视图合成、视频压缩和图像超分辨率。不幸的是，对这些网络的内部运作方式的研究严重不足。我们的工作，即解释隐式神经画布（XINC），是一个统一的框架，用于通过检查每个神经元对每个输出像素的贡献强度来解释INRs的特性。我们将这些贡献图的集合称为隐式神经画布，并使用这一概念来证明我们研究的INR学会了以令人惊讶的方式“观察”它们所代表的帧。例如，INR往往具有高度分布的表示。虽然缺乏高级对象语义，但它们对颜色和边缘有很大的偏见，而且几乎完全是空间不可知的。我们通过研究视频INR中对象在时间上的表现方式得出了我们的结论，使用聚类来可视化跨层和架构的相似神经元，并表明这是由运动主导的。这些见解证明了我们的分析框架的普遍有用性。我们的项目页面位于https://namithap10.github.io/xinc. et.al.|[2401.10217](http://arxiv.org/abs/2401.10217)|null|
|**2024-01-18**|**GPAvatar: Generalizable and Precise Head Avatar from Image(s)**|头部化身重建对于虚拟现实、在线会议、游戏和电影行业的应用至关重要，在计算机视觉界引起了极大的关注。该领域的基本目标是忠实地再现头部化身，并精确地控制表情和姿势。现有的方法分为基于2D的扭曲、基于网格和神经渲染方法，在保持多视图一致性、结合非面部信息和推广到新身份方面存在挑战。在本文中，我们提出了一个名为GPAvatar的框架，该框架可以在单个前向通道中从一个或多个图像重建3D头部化身。这项工作的关键思想是引入一个由点云驱动的动态基于点的表情场，以精确有效地捕捉表情。此外，我们在三平面规范场中使用多三平面注意力（MTA）融合模块来利用来自多个输入图像的信息。所提出的方法实现了忠实的身份重建、精确的表达控制和多视图一致性，在自由视点渲染和新颖视图合成方面显示了良好的效果。 et.al.|[2401.10215](http://arxiv.org/abs/2401.10215)|**[link](https://github.com/xg-chu/gpavatar)**|
|**2024-01-17**|**Objects With Lighting: A Real-World Dataset for Evaluating Reconstruction and Rendering for Object Relighting**|从照片中重建对象并将其虚拟地放置在新环境中超出了标准的新颖视图合成任务，因为对象的外观不仅要适应新颖的视点，还要适应新的照明条件，而且反向渲染方法的评估依赖于新颖的视图合成数据或用于定量分析的简单合成数据集。这项工作提供了一个真实世界的数据集，用于测量重新照明对象的重建和渲染。为此，我们捕获了多个环境中相同对象的环境照明和地面实况图像，从而可以从一个环境中拍摄的图像中重建对象，并量化看不见的照明环境的渲染视图的质量。此外，我们介绍了一个由现成方法组成的简单基线，并在重新照明任务中测试了几种最先进的方法，表明新的视图合成不是衡量性能的可靠指标。代码和数据集可在https://github.com/isl-org/objects-with-lighting . et.al.|[2401.09126](http://arxiv.org/abs/2401.09126)|**[link](https://github.com/isl-org/objects-with-lighting)**|
|**2024-01-17**|**ICON: Incremental CONfidence for Joint Pose and Radiance Field Optimization**|在给定一组2D图像的情况下，神经辐射场（NeRF）在新视图合成（NVS）中表现出显著的性能。然而，NeRF训练需要每个输入视图的精确相机姿势，通常通过运动结构（SfM）管道获得。最近的作品试图放松这种限制，但它们仍然经常依赖于可以改进的体面的初始姿势。在这里，我们旨在消除姿势初始化的要求。我们提出了增量置信（ICON），这是一种从2D视频帧中训练NeRF的优化过程。ICON仅假设相机运动平滑，以估计姿势的初始猜测。此外，ICON引入了“置信度”：一种用于动态重加权梯度的模型质量自适应度量。ICON依赖于高置信度姿势来学习NeRF，并依赖于高置信度3D结构（由NeRF编码）来学习姿势。我们表明，与使用SfM姿势的方法相比，ICON在没有预先初始化姿势的情况下，在CO3D和HO3D中都实现了卓越的性能。 et.al.|[2401.08937](http://arxiv.org/abs/2401.08937)|null|
|**2024-01-16**|**Fast Dynamic 3D Object Generation from a Single-view Video**|由于缺乏4D标记的数据，从单视图视频生成动态三维（3D）对象是具有挑战性的。现有方法通过传输现成的图像生成模型（如分数蒸馏采样）来扩展文本到3D管道，但由于需要通过大型预训练模型反向传播信息有限的监督信号，这些方法的扩展速度慢且成本高（例如，每个对象150分钟）。为了解决这一限制，我们提出了一种高效的视频到4D对象生成框架，称为Efficient4D。它在不同的相机视图下生成高质量的时空一致图像，然后将其用作标记数据，直接训练具有显式点云几何结构的新型4D高斯飞溅模型，实现在连续相机轨迹下的实时渲染。对合成视频和真实视频的广泛实验表明，与现有技术的替代方案相比，Efficient4D的速度显著提高了10倍，同时保持了相同水平的创新视图合成质量。例如，Efficient4D只需14分钟即可对动态对象进行建模。 et.al.|[2401.08742](http://arxiv.org/abs/2401.08742)|null|
|**2024-01-18**|**ProvNeRF: Modeling per Point Provenance in NeRFs as a Stochastic Process**|神经辐射场（NeRFs）在各种应用中越来越受欢迎。然而，它们在稀疏视图设置中面临挑战，缺乏来自体积渲染的足够约束。在具有多种应用的经典计算机视觉中，从稀疏和无约束的相机重建和理解3D场景是一个长期存在的问题。虽然最近的工作在稀疏、无约束的视图场景中探索了NeRF，但他们的重点主要是增强重建和新颖的视图合成。我们的方法从更广泛的角度出发，提出了一个问题：“从哪里看到了每个点？”——这决定了我们对它的理解和重建程度。换句话说，我们的目标是在稀疏、无约束的视图下确定每个3D点及其相关信息的起源或出处。我们介绍了ProvNeRF，这是一个模型，通过合并每个点的来源，为每个点的可能源位置建模，丰富了传统的NeRF表示。我们通过扩展随机过程的隐式最大似然估计（IMLE）来实现这一点。值得注意的是，我们的方法与任何预先训练的NeRF模型和相关的训练相机姿势兼容。我们证明，与最先进的方法相比，逐点源建模提供了几个优势，包括不确定性估计、基于标准的视图选择和改进的新视图合成。请访问我们的项目页面https://provnerf.github.io et.al.|[2401.08140](http://arxiv.org/abs/2401.08140)|null|

<p align=right>(<a href=#updated-on-20240125>back to top</a>)</p>

## MLLM

|Publish Date|Title|Abstract|PDF|Code|
|---|---|-----------------------------------|---|---|
|**2024-01-23**|**Multilingual and Fully Non-Autoregressive ASR with Large Language Model Fusion: A Comprehensive Study**|在大模型时代，解码的自回归性质往往导致延迟成为一个重要的瓶颈。我们提出了一种非自回归LM融合ASR系统，该系统有效地利用了加速器硬件的并行化能力。我们的方法在每段评分模式中结合了通用语音模型（USM）和PaLM 2语言模型，在FLEURS和YouTube字幕上，所有语言的平均相对WER提高了10.8%和3.6%。此外，我们的综合消融研究分析了LLM大小、上下文长度、词汇大小、融合方法等关键参数。例如，我们探讨了LLM大小在128M到340B参数范围内对ASR性能的影响。这项研究为影响实际大规模LM融合语音识别系统有效性的因素提供了有价值的见解。 et.al.|[2401.12789](http://arxiv.org/abs/2401.12789)|null|
|**2024-01-23**|**Full-Stack Optimization for CAM-Only DNN Inference**|在过去的几年里，神经网络的准确性在各个领域都有了很大的提高。然而，它们不断增加的复杂性导致了冯·诺依曼系统中令人望而却步的高能量需求和延迟。最近已经提出了几种内存计算（CIM）系统来克服这一问题，但涉及大型模型的准确性、硬件可靠性和可扩展性的权衡仍然是一个挑战。此外，对于一些CIM设计，激活运动仍然需要相当大的时间和能量。本文探讨了三元权重神经网络和使用跑道存储器（RTM）实现的关联处理器（AP）的算法优化的组合。我们提出了一种新的编译流程，通过降低AP的算术强度来优化AP上的卷积。通过利用基于RTM的AP的优势，这种方法大大减少了存储器内的数据传输，同时解决了准确性、能效和可靠性问题。具体而言，与内存加速器中的纵横制相比，我们的解决方案将ImageNet上的ResNet-18推理的能效提高了7.5倍，同时保持了软件的准确性。 et.al.|[2401.12630](http://arxiv.org/abs/2401.12630)|null|
|**2024-01-17**|**Computing in the Era of Large Generative Models: From Cloud-Native to AI-Native**|在本文中，我们研究了大型生成人工智能模型和云原生计算架构的交叉点。最近的大型机型，如ChatGPT，虽然其功能具有革命性，但面临着成本和高端GPU需求不断上升等挑战。通过对大模型即服务（LMaaS）和云数据库即服务（DBaaS）进行类比，我们描述了一种利用云原生技术（例如，多租户和无服务器计算）和高级机器学习运行时（例如，批量LoRA推理）的人工智能原生计算范式。这些共同努力旨在优化商品销售成本（COGS）并提高资源可及性。合并这两个领域的旅程才刚刚开始，我们希望刺激该领域未来的研究和发展。 et.al.|[2401.12230](http://arxiv.org/abs/2401.12230)|null|
|**2024-01-22**|**A Saliency Enhanced Feature Fusion based multiscale RGB-D Salient Object Detection Network**|多尺度卷积神经网络（CNN）在解决各种视觉问题方面表现出了非凡的能力。然而，融合不同尺度的特征总是导致模型尺寸大，阻碍了多尺度细胞神经网络在RGB-D显著性检测中的应用。在本文中，我们提出了一种定制的特征融合模块，称为显著性增强特征融合（SEFF），用于RGB-D显著性检测。SEFF利用相邻尺度的显著性图来增强融合所需的特征，从而产生更具代表性的融合特征。我们的多尺度RGB-D显著性检测器使用SEFF并处理具有三个不同尺度的图像。SEFF用于融合RGB和深度图像的特征，以及不同尺度的解码器的特征。在五个基准数据集上的大量实验已经证明了我们的方法优于十个SOTA显著性检测器。 et.al.|[2401.11914](http://arxiv.org/abs/2401.11914)|null|
|**2024-01-22**|**SuperCLUE-Math6: Graded Multi-Step Math Reasoning Benchmark for LLMs in Chinese**|我们介绍了SuperCLUE-Math6（SC-Math6），这是一个新的基准数据集，用于评估汉语模型的数学推理能力。SC-Math6是GSM8K数据集的升级中文版，具有更强的难度、多样性和应用范围。它由2000多个数学单词问题组成，需要多步骤推理并提供自然语言解决方案。我们提出了一种创新方案，根据不同推理步骤问题的性能来量化大型模型的推理能力。在12个具有代表性的中国模型上进行的实验表明，推理水平分层清晰，GPT-4等顶级模型表现出优异的性能。SC-Math6填补了中国数学推理基准的空白，为提高汉语模型的智能性提供了一个全面的测试平台。 et.al.|[2401.11819](http://arxiv.org/abs/2401.11819)|null|
|**2024-01-22**|**P2DT: Mitigating Forgetting in task-incremental Learning with progressive prompt Decision Transformer**|灾难性遗忘对管理由大型模型控制的智能代理提出了重大挑战，当这些代理面临新任务时，会导致性能下降。在我们的工作中，我们提出了一种新的解决方案——渐进式即时决策转换器（P2DT）。该方法通过在新任务训练期间动态附加决策令牌来增强基于转换器的模型，从而促进特定于任务的策略。我们的方法可以缓解持续和离线强化学习场景中的遗忘。此外，P2DT利用了通过传统强化学习从所有任务中收集的轨迹，并在训练过程中生成新的任务特定令牌，从而保留了先前研究的知识。初步结果表明，我们的模型有效地缓解了灾难性遗忘，并能很好地适应不断增加的任务环境。 et.al.|[2401.11666](http://arxiv.org/abs/2401.11666)|null|
|**2024-01-17**|**Generative Denoise Distillation: Simple Stochastic Noises Induce Efficient Knowledge Transfer for Dense Prediction**|知识提炼是将知识从更强大的大模型（教师）转移到更简单的模型（学生）的过程。目前的许多方法都涉及学生直接模仿老师的知识。然而，通过这些流行的方法，在学习的表示中仍然存在冗余，这些方法倾向于不加区别地学习每个空间位置的特征。为了从教师那里获得更紧凑的表示（概念特征），受人类认知的启发，我们提出了一种创新的方法，称为生成去噪蒸馏（GDD），其中将随机噪声添加到学生的概念特征中，以将其嵌入浅层网络生成的实例特征中。然后，将生成的实例特征与来自老师的实例知识对齐。我们对对象检测、实例分割和语义分割进行了广泛的实验，以证明我们的方法的通用性和有效性。值得注意的是，GDD在上述任务中实现了最先进的性能。我们通过增强基于ResNet-18的PspNet和DeepLabV3，在语义分割方面取得了实质性的改进，mIoU得分分别为74.67和77.69，超过了他们之前在20个类别的Cityscapes数据集上的69.85和73.20分。源代码位于https://github.com/ZhgLiu/GDD. et.al.|[2401.08332](http://arxiv.org/abs/2401.08332)|null|
|**2024-01-16**|**Multitask Learning in Minimally Invasive Surgical Vision: A Review**|微创手术（MIS）已经彻底改变了许多程序，并减少了患者的恢复时间和受伤风险。然而，MIS给外科团队带来了额外的复杂性和负担。数据驱动的手术视觉算法被认为是开发具有改进自主性的未来MIS系统的关键构建块。机器学习和计算机视觉的最新进展已成功应用于分析从MIS获得的视频，有望缓解MIS视频中的挑战。手术场景和动作理解包括多个相关任务，当单独解决时，这些任务可能会占用大量记忆，效率低下，并且无法捕捉任务关系。多任务学习（MTL）是一种利用来自多个相关任务的信息来提高性能和帮助泛化的学习范式，非常适合对MIS数据进行细粒度和高级理解。这篇综述概述了当前最先进的MTL系统，这些系统利用了从MIS获得的视频。除了列出已发表的方法外，我们还讨论了这些MTL系统的优点和局限性。此外，本文还分析了MTL在MIS中各个应用领域的文献，包括那些具有大型模型的文献，强调了显著的趋势、新的研究方向和发展。 et.al.|[2401.08256](http://arxiv.org/abs/2401.08256)|null|
|**2024-01-16**|**A Survey of Resource-efficient LLM and Multimodal Foundation Models**|大型基础模型，包括大型语言模型（LLM）、视觉转换器（ViT）、扩散和基于LLM的多模式模型，正在彻底改变从训练到部署的整个机器学习生命周期。然而，这些型号在多功能性和性能方面的巨大进步在硬件资源方面付出了巨大的代价。为了以可扩展和环境可持续的方式支持这些大型模型的发展，人们相当重视制定资源节约型战略。这项调查深入探讨了此类研究的关键重要性，考察了算法和系统两个方面。它提供了从现有文献中收集的全面分析和有价值的见解，涵盖了从尖端模型架构和训练/服务算法到实际系统设计和实现的广泛主题。这项调查的目标是全面了解当前的方法是如何应对大型基础模型带来的资源挑战的，并有可能激励未来在这一领域取得突破。 et.al.|[2401.08092](http://arxiv.org/abs/2401.08092)|**[link](https://github.com/ubiquitouslearning/efficient_foundation_model_survey)**|
|**2024-01-21**|**PDE Generalization of In-Context Operator Networks: A Study on 1D Scalar Nonlinear Conservation Laws**|我们能为广泛的PDE相关科学学习任务建立一个单一的大型模型吗？这个模型能在没有任何微调的情况下推广到新的偏微分方程，甚至是新形式的偏微分函数吗？上下文中操作员学习和相应的上下文中操作员网络（ICON）模型代表了对这些问题的初步探索。ICON关于第一个问题的能力已经在前面进行了演示。在本文中，我们提出了一种使用ICON解决PDE问题的详细方法，并展示了单个ICON模型如何在适当设计的数据提示下，以不同的步长对不同的方程进行正向和反向预测。我们为第二个问题提供了积极的证据，即ICON可以很好地推广到一些具有新形式的偏微分方程，而不需要任何微调。这可以通过对一维标量非线性守恒定律的研究来证明，这是一个具有时间演化的偏微分方程族。我们还展示了如何通过将函数和方程转换到ICON的能力范围来拓宽ICON模型可以解决的问题范围。我们认为，本文的进展是朝着在上下文操作员学习框架下训练PDE相关任务的基础模型的目标迈出的重要一步。 et.al.|[2401.07364](http://arxiv.org/abs/2401.07364)|null|

<p align=right>(<a href=#updated-on-20240125>back to top</a>)</p>

## Diffusion

|Publish Date|Title|Abstract|PDF|Code|
|---|---|-----------------------------------|---|---|
|**2024-01-24**|**Research about the Ability of LLM in the Tamper-Detection Area**|近年来，特别是自20世纪20年代初以来，大型语言模型（LLM）已成为应对各种挑战的最强大的人工智能工具，从自然语言处理到各个领域的复杂问题解决。在篡改检测领域，LLM能够识别基本的篡改活动。为了评估LLM在更专业领域的能力，我们收集了由多家公司开发的五种不同的LLM：GPT-4、LLaMA、Bard、文心一言4.0和同益谦文。这种多样的模型范围允许对其在检测复杂篡改实例方面的性能进行全面评估。我们设计了两个检测领域：人工智能生成内容（AIGC）检测和操纵检测。AIGC检测旨在测试区分图像是真实的还是人工智能生成的能力。另一方面，操纵检测侧重于识别被篡改的图像。根据我们的实验，大多数LLM可以识别与逻辑不一致的合成图片，只有更强大的LLM才能区分逻辑但肉眼可见的篡改迹象。所有的LLM都无法识别精心伪造的图像和人工智能生成的非常逼真的图像。在篡改检测领域，LLM还有很长的路要走，尤其是在可靠地识别高度复杂的伪造品和人工智能产生的接近真实的图像方面。 et.al.|[2401.13504](http://arxiv.org/abs/2401.13504)|null|
|**2024-01-24**|**UNIMO-G: Unified Image Generation through Multimodal Conditional Diffusion**|现有的文本到图像扩散模型主要从文本提示生成图像。然而，文本描述固有的简洁性对忠实地合成具有复杂细节的图像（如特定实体或场景）提出了挑战。本文提出了\textbf{UNIMO-G}，这是一个简单的多模式条件扩散框架，它在具有交错文本和视觉输入的多模式提示上运行，它展示了文本驱动和主题驱动图像生成的统一能力。UNIMO-G包括两个核心组件：用于编码多模式提示的多模式大型语言模型（MLLM）和用于基于编码的多模式输入生成图像的条件去噪扩散网络。我们利用两阶段训练策略来有效训练框架：首先对大规模文本图像对进行预训练，以发展条件图像生成能力，然后使用多模式提示进行指令调整，以实现统一的图像生成能力。采用一个精心设计的数据处理管道，包括语言基础和图像分割，来构建多模式提示。UNIMO-G擅长文本到图像生成和零样本主题驱动合成，并且在从涉及多个图像实体的复杂多模式提示生成高保真图像方面特别有效。 et.al.|[2401.13388](http://arxiv.org/abs/2401.13388)|null|
|**2024-01-24**|**Deep Learning for Improved Polyp Detection from Synthetic Narrow-Band Imaging**|为了应对癌症（CRC）日益流行的情况，息肉检测和切除的筛查计划已证明其有效性。结肠镜检查被认为是CRC筛查的最佳方法。为了简化检查，已经为传统的白光成像（WLI）开发了基于深度学习的息肉自动检测方法。与WLI相比，窄带成像（NBI）可以改善结肠镜检查中的息肉分类，但需要特殊的设备。我们提出了一种基于CycleGAN的框架，将用常规WLI捕获的图像转换为合成NBI（SNBI），作为在NBI不可用时改进WLI上的对象检测的预处理方法。本文首先表明，与相对相似的WLI数据集相比，NBI可以获得更好的息肉检测结果。其次，实验结果表明，与原始WLI相比，我们提出的模态转换可以在WLI生成的SNBI图像上实现更好的息肉检测。这是因为我们的WLI到SNBI转换模型可以增强对生成的SNBI图像中息肉表面图案的观察。 et.al.|[2401.13315](http://arxiv.org/abs/2401.13315)|null|
|**2024-01-24**|**Choose Your Diffusion: Efficient and flexible ways to accelerate the diffusion model in fast high energy physics simulation**|扩散模型在图像生成中显示出了有希望的结果，最近成为主流，并代表了许多生成建模任务的显著进步。扩散模型在高能物理中用于快速事件和探测器模拟的先前应用已显示出卓越的性能，为在有限的计算预算内生成足够的统计数据为高亮度LHC做准备提供了可行的解决方案。然而，这些应用程序中的许多都存在生成速度慢、采样步骤大的问题，并且在找到样本质量和速度之间的最佳平衡方面面临挑战。该研究的重点是基于ODE/SDE的高效采样器、调度器和快速收敛训练技术的最新基准开发。我们在公共CaloChallenge和JetNet数据集上测试了在现有架构上实现的设计，生成的类的性能超过了以前的模型，通过各种评估指标实现了显著的加速。 et.al.|[2401.13162](http://arxiv.org/abs/2401.13162)|null|
|**2024-01-23**|**CIMGEN: Controlled Image Manipulation by Finetuning Pretrained Generative Models on Limited Data**|内容创建和图像编辑可以受益于灵活的用户控件。条件图像生成的常见中间表示是语义图，该语义图具有图像中存在的对象的信息。与原始RGB像素相比，语义图的修改要容易得多。可以使用语义映射并轻松地修改映射以选择性地插入、移除或替换映射中的对象。本文提出的方法引入修改后的语义图，并根据修改后的图对原始图像进行修改。该方法利用传统的预训练的图像到图像翻译GAN，例如CycleGAN或Pix2Pix GAN，它们在与语义图相关联的参考图像的有限数据集上进行微调。我们讨论了我们的技术的定性和定量性能，以说明其在图像伪造和图像编辑领域的能力和可能的应用。我们还证明了所提出的图像伪造技术在挫败众多基于深度学习的图像取证技术方面的有效性，强调了在打击假媒体传播的过程中，迫切需要开发强大且通用的图像取证工具。 et.al.|[2401.13006](http://arxiv.org/abs/2401.13006)|null|
|**2024-01-23**|**Lumiere: A Space-Time Diffusion Model for Video Generation**|我们介绍了Lumiere——一种文本到视频的扩散模型，旨在合成描绘逼真、多样和连贯运动的视频——这是视频合成中的一个关键挑战。为此，我们引入了一种时空U-Net架构，该架构通过模型中的一次传递，一次生成视频的整个时间持续时间。这与现有的视频模型形成了鲜明对比，现有视频模型先合成远处的关键帧，然后再合成时间超分辨率——这种方法固有地使全局时间一致性难以实现。通过部署空间和（重要的）时间下采样和上采样，并利用预先训练的文本到图像扩散模型，我们的模型学会了通过在多个时空尺度上处理来直接生成全帧率、低分辨率的视频。我们展示了最先进的文本到视频生成结果，并表明我们的设计可以轻松地促进广泛的内容创建任务和视频编辑应用程序，包括图像到视频、视频修复和风格化生成。 et.al.|[2401.12945](http://arxiv.org/abs/2401.12945)|null|
|**2024-01-23**|**A Unified Generation-Registration Framework for Improved MR-based CT Synthesis in Proton Therapy**|背景：在MR引导的质子治疗计划中，对齐MR和CT图像是基于MR的CT合成的关键，尤其是在头部和颈部等移动区域。这里的错位可能导致合成CT（sCT）图像的准确性降低，影响治疗精度。目的：本研究介绍了一种新的网络，该网络将图像生成和配准过程连贯统一，以提高从更好对齐的MR图像中提取的sCT的质量和解剖保真度。方法：该方法将生成网络（G）和可变形配准网络（R）协同，在MR到CT合成中对它们进行联合优化。这一目标是通过交替地最小化生成/配准的CT图像与其相应的参考CT对应物之间的差异来实现的。生成网络采用UNet架构，而配准网络利用可变形矢量场（DVF）的隐式神经表示。我们在包括60名头颈部患者的数据集上验证了这种方法，保留了12例病例进行顽固性测试。结果：与MAE为124.95\pm 30.74 HU的基线Pix2Pix方法相比，所提出的技术显示出80.98\pm 7.55 HU。统一的平移配准网络产生了更清晰、更符合解剖学的输出，在将MR图像转换为sCTs方面显示出优越的功效。此外，从剂量测定的角度来看，根据由此产生的sCTs重新计算的计划显著减少了与参考质子计划的差异。结论：本研究最终证明，基于MR的整体CT合成方法，结合图像到图像的平移和可变形配准，显著提高了sCT生成的精度和质量，特别是对于具有挑战性的身体区域，在相应的MR和CT之间具有不同的解剖变化。 et.al.|[2401.12878](http://arxiv.org/abs/2401.12878)|null|
|**2024-01-23**|**UniHDA: Towards Universal Hybrid Domain Adaptation of Image Generators**|生成域自适应已经取得了显著的进展，使我们能够将预先训练的生成器自适应到新的目标域。然而，现有的方法只是将生成器适应于单个目标域，并且仅限于文本驱动或图像驱动的单个模态。此外，它们容易过度拟合特定领域的属性，这不可避免地会损害跨领域的一致性。在本文中，我们提出了UniHDA，这是一个统一而通用的生成混合域自适应框架，具有来自多个域的多模态引用。我们使用CLIP编码器将多模态参考投影到统一的嵌入空间中，然后对来自多个目标域的方向向量进行线性插值，以实现混合域自适应。为了确保跨域一致性，我们提出了一种新的跨域空间结构（CSS）损失，该损失保持源生成器和目标生成器之间的详细空间结构信息。实验表明，自适应生成器可以合成具有各种属性组成的逼真图像。此外，我们的框架适用于多个生成器，例如StyleGAN2和Diffusion Models。 et.al.|[2401.12596](http://arxiv.org/abs/2401.12596)|null|
|**2024-01-23**|**The Neglected Tails of Vision-Language Models**|视觉语言模型（VLM）在零样本识别方面表现出色，但在视觉概念方面表现出严重的不平衡性能。例如，尽管在ImageNet上有令人印象深刻的平均零样本准确率（72.7%），但CLIP在十个概念（例如陀螺和夜蛇）上产生了 $<$ 10%的收益，这可能是因为这些概念在VLM的不平衡预训练数据中未得到充分体现。然而，评估这种不平衡是具有挑战性的，因为计算VLM大规模预训练数据中特定概念的频率并非易事。我们的工作首次尝试通过分析预训练文本来测量概念频率。我们使用现成的语言模型来帮助统计包含给定概念的同义词的相关文本，并解决语言歧义。我们证实，像LAION这样的流行VLM数据集确实表现出长尾概念分布，这与每类精度密切相关。此外，当代的多模式系统，例如视觉聊天机器人和文本到图像生成器，也在与我们的方法所识别的罕见概念作斗争。为了缓解VLM在零样本识别中的不平衡性能，我们提出了REtrieval-AugmentedLearningREAL。首先，REAL不使用原始类名提示VLM，而是使用VLM预训练文本中最常见的同义词。在九个基准数据集中，这已经优于人工设计和LLM生成的提示，这可能是因为VLM看到了更多与常用同义词相关的图像。其次，REAL使用所有概念同义词来检索一组小的、类平衡的预训练数据，以训练一个健壮的分类器。REAL超越了最近的检索增强解决方案REACT，使用的存储空间减少了400倍，训练时间减少了10000倍！ et.al.|[2401.12425](http://arxiv.org/abs/2401.12425)|null|
|**2024-01-23**|**Control of OSIRIS-REx OTES Observations using OCAMS TAG Images**|当OSIRIS REx航天器朝着小行星本努下降，在即用即用（TAG）程序中从表面收集样本时，许多仪器都在积极收集观测数据。我们应用摄影测量控制过程来准确确定190幅OCAMS MapCam和SamCam下降图像在曝光时的位置和姿态。图像的平均像素分辨率为10厘米（中值为7厘米）。使用Bennu的高分辨率（5厘米、44厘米和88厘米地面样本距离）形状模型生成的模拟图像将图像控制到地面。经过最小二乘调整后，所有图像测量残差的均方根（rms）为0.16像素。通过使用从OCAMS到OTES帧的帧变换对OCAMS MapCam和SamCam仪器的更新星历表进行插值，将这些结果应用于581个OTES观测。然后，通过在44cm形状的模型上追踪调整后的视线方向的光线，重新计算OTES视场的表面截距。调整后的OTES视轴表面截距的平均值与88cm形状模型上的先验位置相差约37cm，不确定性小于5cm。 et.al.|[2401.12177](http://arxiv.org/abs/2401.12177)|null|

<p align=right>(<a href=#updated-on-20240125>back to top</a>)</p>

## avatar

|Publish Date|Title|Abstract|PDF|Code|
|---|---|-----------------------------------|---|---|
|**2024-01-09**|**DiffSHEG: A Diffusion-Based Approach for Real-Time Speech-driven Holistic 3D Expression and Gesture Generation**|我们提出了DiffSHEG，这是一种基于扩散的方法，用于语音驱动的任意长度的整体三维表达和手势生成。虽然之前的工作专注于共同语音手势或单独生成表情，但同步表情和手势的联合生成仍然很少被探索。为了解决这一问题，我们基于扩散的协同语音运动生成转换器实现了从表情到手势的单向信息流，有助于改进联合表情手势分布的匹配。此外，我们还介绍了一种基于外绘的采样策略，用于扩散模型中的任意长序列生成，提供了灵活性和计算效率。我们的方法提供了一种实用的解决方案，可以产生由语音驱动的高质量同步表情和手势生成。在两个公共数据集上进行评估后，我们的方法在数量和质量上都达到了最先进的性能。此外，一项用户研究证实了DiffSHEG优于先前的方法。通过实现表达和同步运动的实时生成，DiffSHEG展示了其在数字人和具体代理开发中的各种应用潜力。 et.al.|[2401.04747](http://arxiv.org/abs/2401.04747)|null|
|**2024-01-11**|**Jump Cut Smoothing for Talking Heads**|跳跃式剪裁给观看体验带来了一种突然的、有时是不必要的变化。我们提出了一个新颖的框架来平滑这些跳跃剪辑，在谈话头部视频的背景下。我们利用视频中其他源帧中受试者的外观，将其与由DensePose关键点和面部标志驱动的中级表示融合。为了实现运动，我们在切割周围的结束帧之间插入关键点和地标。然后，我们使用来自关键点和源帧的图像翻译网络来合成像素。由于关键点可能包含错误，我们提出了一种跨模态注意力方案，以在每个关键点的多个选项中选择最合适的来源。通过利用这种中级表示，我们的方法可以获得比强大的视频插值基线更强的结果。我们在会说话的头部视频中演示了我们的方法，如剪切填充词、停顿，甚至随机剪切。我们的实验表明，即使在有挑战性的情况下，我们也可以实现无缝转换，其中会说话的头部在跳跃切割中旋转或剧烈移动。 et.al.|[2401.04718](http://arxiv.org/abs/2401.04718)|null|
|**2024-01-01**|**Graph-Convolutional Autoencoder Ensembles for the Humanities, Illustrated with a Study of the American Slave Trade**|我们介绍了一个图形感知的自动编码器集成框架，以及相关的形式主义和工具，旨在促进人文学科学术的深度学习。通过组成子体系结构以生成同构于人文领域的模型，我们保持了可解释性，同时为每个子体系结构选择提供功能签名，允许传统和计算研究人员在不干扰既定实践的情况下进行合作。我们展示了我们的方法在美国后大西洋奴隶贸易历史研究中的实际应用，并做出了一些具体的技术贡献：一种新的混合图卷积自动编码器机制，用于常见图拓扑的批处理策略，以及用于特定用例的掩蔽技术。越来越多的20多项研究证明了该框架扩大不同领域参与的有效性，这些研究既有与人文主义者的合作，也有机器学习文献中的既定任务，涵盖了各种领域和数据模式。我们对几种不同的体系结构选择进行了性能比较，最后列出了这项研究即将采取的下一步行动。 et.al.|[2401.00824](http://arxiv.org/abs/2401.00824)|null|
|**2023-12-23**|**Human101: Training 100+FPS Human Gaussians in 100s from 1 View**|从单视角视频中重构人体在虚拟现实领域发挥着关键作用。一种流行的应用场景需要快速重建高保真3D数字人，同时确保实时渲染和交互。现有的方法往往难以满足这两个要求。在本文中，我们介绍了Human101，这是一种新颖的框架，通过在100秒内训练3D高斯人并以100+FPS进行渲染，能够从单视图视频中生成高保真动态3D人体重建。我们的方法利用了3D高斯飞溅的优势，它提供了3D人类的明确而有效的表示。与之前基于NeRF的管道不同，Human101巧妙地应用了以人为中心的前向高斯动画方法来变形3D高斯的参数，从而提高了渲染速度（即，以令人印象深刻的60+FPS渲染1024个分辨率的图像，以100+FPS渲染512个分辨率的图片）。实验结果表明，我们的方法大大超过了当前的方法，每秒帧数激增了10倍，并提供了相当或卓越的渲染质量。代码和演示将在上发布https://github.com/longxiang-ai/Human101. et.al.|[2312.15258](http://arxiv.org/abs/2312.15258)|**[link](https://github.com/longxiang-ai/human101)**|
|**2023-12-23**|**Prompt-Propose-Verify: A Reliable Hand-Object-Interaction Data Generation Framework using Foundational Models**|扩散模型以文本提示为条件，生成具有复杂细节的逼真图像。但是，当涉及到手、牙齿等人类特征时，大多数预先训练的模型都无法生成准确的图像。我们假设，可以通过注释良好的高质量数据来克服扩散模型的这种无能。在本文中，我们专门研究了使用扩散模型改进手-物体交互图像的生成。我们收集了一个注释良好的手-物交互合成数据集，该数据集使用Prompt Propose-Verify框架进行策划，并在其上微调稳定的扩散模型。我们根据CLIPScore、ImageReward、Fedility和alignment等定性和定量指标对图像-文本数据集进行评估，并显示出比当前最先进的基准测试更好的性能。 et.al.|[2312.15247](http://arxiv.org/abs/2312.15247)|null|
|**2023-12-23**|**TransFace: Unit-Based Audio-Visual Speech Synthesizer for Talking Head Translation**|直接语音到语音翻译通过引入自监督学习中获得的离散单元来实现高质量的结果。这种方法避免了与模型级联相关的延迟和级联错误。然而，与音频语音相比，有声头翻译，即将视听语音（即有声头视频）从一种语言转换为另一种语言，仍然面临着几个挑战：（1）现有方法总是依赖于级联，通过音频和文本进行合成，导致延迟和级联错误。（2） 会说话的头翻译有一套有限的参考框架。如果生成的翻译超过了原始语音的长度，则需要通过重复帧来补充视频序列，从而导致不和谐的视频转换。在这项工作中，我们提出了一个有声头翻译模型\textbf{TransFace}，它可以直接将视听语音翻译成其他语言的视听语音。它由一个语音到单元的翻译模型和一个基于单元的视听语音合成器Unit2Lip组成，前者将音频语音转换为离散单元，后者并行地从离散单元重新合成同步的视听语音。此外，我们还引入了一个有界持续时间预测器，确保等轴测头的平移并防止重复的参考帧。实验表明，我们提出的Unit2Lip模型显著提高了同步性（原始和生成的音频语音在LSE-C上分别为1.601和0.982），并将LRS2上的推理速度提高了4.35倍。此外，TransFace在LRS3-T和100%等时翻译上的Es-En和Fr-En的BLEU得分分别为61.93和47.55。 et.al.|[2312.15197](http://arxiv.org/abs/2312.15197)|null|
|**2023-12-22**|**Deformable 3D Gaussian Splatting for Animatable Human Avatars**|神经辐射场的最新进展使得能够在动态设置中对照片真实感图像进行新颖的视图合成，这可以应用于具有人类动画的场景。然而，通常使用的隐式主干来建立准确的模型，需要许多输入视图和额外的注释，如人体遮罩、UV贴图和深度贴图。在这项工作中，我们提出了ParDy Human（参数化动态人类化身），这是一种完全明确的方法，可以从一个单一的单目序列中构建数字化身。ParDy Human在3D高斯飞溅中引入了参数驱动的动力学，其中通过人体姿势模型使3D高斯变形以使化身动画化。我们的方法由两个部分组成：第一个模块根据SMPL顶点使标准3D高斯变形，第二个模块进一步采用其设计的联合编码并预测每高斯变形，以处理SMPL顶点变形之外的动力学。然后通过光栅化器合成图像。ParDy Human构成了逼真动态人类化身的显式模型，其需要显著更少的训练视图和图像。我们的化身学习不需要额外的注释，如掩码，并且可以在可变背景下进行训练，同时即使在消费硬件上也能高效地推断出全分辨率图像。我们提供的实验证据表明，在ZJU MoCap和THUman4.0数据集上，ParDy-Human在数量和视觉上都优于最先进的方法。 et.al.|[2312.15059](http://arxiv.org/abs/2312.15059)|null|
|**2023-12-22**|**Latents2Semantics: Leveraging the Latent Space of Generative Models for Localized Style Manipulation of Face Images**|随着元宇宙慢慢成为现实，以及数字人类的快速发展，对人脸原则风格编辑管道的需求势必会增加。我们通过引入潜在2语义自动编码器（L2SAE）来满足这一需求，这是一种生成式自动编码器模型，有助于对人脸图像中几个感兴趣区域（ROI）的风格属性进行高度本地化编辑。L2SAE学习编码图像的结构和风格信息的单独潜在表示。因此，允许对所选择的ROI进行保留结构的样式编辑。编码的结构表示是具有减少的空间维度的多通道2D张量，其捕获局部和全局结构属性。样式表示是捕获全局样式属性的1D张量。在我们的框架中，我们对结构表示进行切片，以建立与不同ROI的强且不纠缠的对应关系。因此，所选ROI的样式编辑相当于（a）从切片结构表示生成的ROI掩模和（b）具有全局样式变化的解码图像的简单组合，该全局样式变化是从操纵的（使用高斯噪声）全局样式和不变的结构张量生成的。在没有额外人力监督的情况下进行风格编辑是对SOTA风格编辑管道的重大胜利，因为大多数现有作品都需要额外的人力（监督）后期培训，才能将语义归因于风格编辑。我们还取消了基于迭代优化的反演或在训练后确定可控的潜在方向，这需要额外的计算成本高昂的操作。我们在多个应用程序中为相同的应用程序提供定性和定量结果，例如使用从多个数据集采样的测试图像进行选择性风格编辑和交换。 et.al.|[2312.15037](http://arxiv.org/abs/2312.15037)|null|
|**2023-12-21**|**From Past to Future: Digital Methods Towards Artefact Analysis**|在过去的二十年里，数字人文改变了人文和社会科学的格局，实现了对广泛数据集的高级计算分析和解释。值得注意的是，东南亚，特别是新加坡最近的举措侧重于对历史数据进行分类和归档，如艺术品、文学作品，尤其是考古文物。这项研究通过在两个不同的人工制品数据集上应用统计方法，展示了数字人文的巨大潜力。具体而言，我们展示了对公元1千年中期东南亚大陆“旭日”铸币的自动模具研究结果，随后对从新加坡中部殖民前圣安德鲁大教堂遗址挖掘的13-14世纪陶器的2D图像使用了无监督统计方法。这项研究提供了一个比较评估，展示了基于统计的方法对不同考古材料的解释和分析以及数字人文整体的变革影响。 et.al.|[2312.13790](http://arxiv.org/abs/2312.13790)|null|
|**2023-12-18**|**Relightable Neural Actor with Intrinsic Decomposition and Pose Control**|在视觉和图形学中，创建一个可欣赏、可驾驶和逼真的数字人类化身是一个具有挑战性的重要问题。人类是高度立体化的，会产生依赖姿势的外观效果，如自我阴影和皱纹，皮肤和衣服需要复杂且空间变化的BRDF模型。虽然最近的人类重新照明方法可以从多视图视频中恢复看似合理的材料光分解，但它们不能推广到新颖的姿势，并且仍然存在视觉伪影。为了解决这一问题，我们提出了Relightable Neural Actor，这是第一种基于视频的方法，用于学习照片真实感的神经人体模型，该模型可以重新照明，允许外观编辑，并可以由任意骨骼姿势控制。重要的是，为了学习我们的人类化身，我们只需要在已知但静态的照明条件下对人类进行多视图记录。为了实现这一点，我们用可驱动的密度场来表示演员的几何体，该密度场对姿势相关的服装变形进行建模，并提供3D和UV空间之间的映射，其中对法线、可见性和材质进行编码。为了在现实世界场景中评估我们的方法，我们收集了一个新的数据集，其中包括在室内和室外不同光照条件下记录的四个参与者，为人类重新照明提供了第一个此类基准，并展示了最先进的新人类姿势的重新照明结果。 et.al.|[2312.11587](http://arxiv.org/abs/2312.11587)|null|

<p align=right>(<a href=#updated-on-20240125>back to top</a>)</p>

[contributors-shield]: https://img.shields.io/github/contributors/Vincentqyw/cv-arxiv-daily.svg?style=for-the-badge
[contributors-url]: https://github.com/Vincentqyw/cv-arxiv-daily/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/Vincentqyw/cv-arxiv-daily.svg?style=for-the-badge
[forks-url]: https://github.com/Vincentqyw/cv-arxiv-daily/network/members
[stars-shield]: https://img.shields.io/github/stars/Vincentqyw/cv-arxiv-daily.svg?style=for-the-badge
[stars-url]: https://github.com/Vincentqyw/cv-arxiv-daily/stargazers
[issues-shield]: https://img.shields.io/github/issues/Vincentqyw/cv-arxiv-daily.svg?style=for-the-badge
[issues-url]: https://github.com/Vincentqyw/cv-arxiv-daily/issues

