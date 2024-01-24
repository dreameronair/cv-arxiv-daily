[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]

## Updated on 2024.01.24
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
|**2024-01-22**|**HG3-NeRF: Hierarchical Geometric, Semantic, and Photometric Guided Neural Radiance Fields for Sparse View Inputs**|神经辐射场（NeRF）作为一种通过从离散观测中学习场景表示的新型视图合成范式，已经引起了人们的极大关注。然而，当面对稀疏视图输入时，NeRF表现出明显的性能退化，从而限制了其进一步的适用性。在这项工作中，我们介绍了层次几何、语义和光度引导的NeRF（HG3-NeRF），这是一种新的方法，可以解决上述限制，并增强不同视图中几何、语义内容和外观的一致性。我们提出了分层几何制导（HGG），将运动结构的附加（SfM），即稀疏深度先验，纳入场景表示中。与直接深度监督不同，HGG从局部几何区域到全局几何区域对体积点进行采样，减轻了深度先验中固有偏差引起的偏差。此外，我们从不同分辨率的图像中观察到的语义一致性的显著变化中获得了灵感，并提出了层次语义引导（HSG）来学习粗到细的语义内容，该内容对应于粗到细场景表示。实验结果表明，HG3-NeRF可以在不同的标准基准上优于其他最先进的方法，并实现稀疏视图输入的高保真度合成结果。 et.al.|[2401.11711](http://arxiv.org/abs/2401.11711)|null|
|**2024-01-18**|**Explaining the Implicit Neural Canvas: Connecting Pixels to Neurons by Tracing their Contributions**|隐式神经表示（INRs）的许多变体，其中神经网络被训练为信号的连续表示，对于下游任务具有巨大的实用性，包括新颖的视图合成、视频压缩和图像超分辨率。不幸的是，对这些网络的内部运作方式的研究严重不足。我们的工作，即解释隐式神经画布（XINC），是一个统一的框架，用于通过检查每个神经元对每个输出像素的贡献强度来解释INRs的特性。我们将这些贡献图的集合称为隐式神经画布，并使用这一概念来证明我们研究的INR学会了以令人惊讶的方式“观察”它们所代表的帧。例如，INR往往具有高度分布的表示。虽然缺乏高级对象语义，但它们对颜色和边缘有很大的偏见，而且几乎完全是空间不可知的。我们通过研究视频INR中对象在时间上的表现方式得出了我们的结论，使用聚类来可视化跨层和架构的相似神经元，并表明这是由运动主导的。这些见解证明了我们的分析框架的普遍有用性。我们的项目页面位于https://namithap10.github.io/xinc. et.al.|[2401.10217](http://arxiv.org/abs/2401.10217)|null|
|**2024-01-18**|**GPAvatar: Generalizable and Precise Head Avatar from Image(s)**|头部化身重建对于虚拟现实、在线会议、游戏和电影行业的应用至关重要，在计算机视觉界引起了极大的关注。该领域的基本目标是忠实地再现头部化身，并精确地控制表情和姿势。现有的方法分为基于2D的扭曲、基于网格和神经渲染方法，在保持多视图一致性、结合非面部信息和推广到新身份方面存在挑战。在本文中，我们提出了一个名为GPAvatar的框架，该框架可以在单个前向通道中从一个或多个图像重建3D头部化身。这项工作的关键思想是引入一个由点云驱动的动态基于点的表情场，以精确有效地捕捉表情。此外，我们在三平面规范场中使用多三平面注意力（MTA）融合模块来利用来自多个输入图像的信息。所提出的方法实现了忠实的身份重建、精确的表达控制和多视图一致性，在自由视点渲染和新颖视图合成方面显示了良好的效果。 et.al.|[2401.10215](http://arxiv.org/abs/2401.10215)|**[link](https://github.com/xg-chu/gpavatar)**|
|**2024-01-17**|**Objects With Lighting: A Real-World Dataset for Evaluating Reconstruction and Rendering for Object Relighting**|从照片中重建对象并将其虚拟地放置在新环境中超出了标准的新颖视图合成任务，因为对象的外观不仅要适应新颖的视点，还要适应新的照明条件，而且反向渲染方法的评估依赖于新颖的视图合成数据或用于定量分析的简单合成数据集。这项工作提供了一个真实世界的数据集，用于测量重新照明对象的重建和渲染。为此，我们捕获了多个环境中相同对象的环境照明和地面实况图像，从而可以从一个环境中拍摄的图像中重建对象，并量化看不见的照明环境的渲染视图的质量。此外，我们介绍了一个由现成方法组成的简单基线，并在重新照明任务中测试了几种最先进的方法，表明新的视图合成不是衡量性能的可靠指标。代码和数据集可在https://github.com/isl-org/objects-with-lighting. et.al.|[2401.09126](http://arxiv.org/abs/2401.09126)|**[link](https://github.com/isl-org/objects-with-lighting)**|
|**2024-01-17**|**ICON: Incremental CONfidence for Joint Pose and Radiance Field Optimization**|在给定一组2D图像的情况下，神经辐射场（NeRF）在新视图合成（NVS）中表现出显著的性能。然而，NeRF训练需要每个输入视图的精确相机姿势，通常通过运动结构（SfM）管道获得。最近的作品试图放松这种限制，但它们仍然经常依赖于可以改进的体面的初始姿势。在这里，我们旨在消除姿势初始化的要求。我们提出了增量置信（ICON），这是一种从2D视频帧中训练NeRF的优化过程。ICON仅假设相机运动平滑，以估计姿势的初始猜测。此外，ICON引入了“置信度”：一种用于动态重加权梯度的模型质量自适应度量。ICON依赖于高置信度姿势来学习NeRF，并依赖于高置信度3D结构（由NeRF编码）来学习姿势。我们表明，与使用SfM姿势的方法相比，ICON在没有预先初始化姿势的情况下，在CO3D和HO3D中都实现了卓越的性能。 et.al.|[2401.08937](http://arxiv.org/abs/2401.08937)|null|
|**2024-01-16**|**Fast Dynamic 3D Object Generation from a Single-view Video**|由于缺乏4D标记的数据，从单视图视频生成动态三维（3D）对象是具有挑战性的。现有方法通过传输现成的图像生成模型（如分数蒸馏采样）来扩展文本到3D管道，但由于需要通过大型预训练模型反向传播信息有限的监督信号，这些方法的扩展速度慢且成本高（例如，每个对象150分钟）。为了解决这一限制，我们提出了一种高效的视频到4D对象生成框架，称为Efficient4D。它在不同的相机视图下生成高质量的时空一致图像，然后将其用作标记数据，直接训练具有显式点云几何结构的新型4D高斯飞溅模型，实现在连续相机轨迹下的实时渲染。对合成视频和真实视频的广泛实验表明，与现有技术的替代方案相比，Efficient4D的速度显著提高了10倍，同时保持了相同水平的创新视图合成质量。例如，Efficient4D只需14分钟即可对动态对象进行建模。 et.al.|[2401.08742](http://arxiv.org/abs/2401.08742)|null|
|**2024-01-18**|**ProvNeRF: Modeling per Point Provenance in NeRFs as a Stochastic Process**|神经辐射场（NeRFs）在各种应用中越来越受欢迎。然而，它们在稀疏视图设置中面临挑战，缺乏来自体积渲染的足够约束。在具有多种应用的经典计算机视觉中，从稀疏和无约束的相机重建和理解3D场景是一个长期存在的问题。虽然最近的工作在稀疏、无约束的视图场景中探索了NeRF，但他们的重点主要是增强重建和新颖的视图合成。我们的方法从更广泛的角度出发，提出了一个问题：“从哪里看到了每个点？”——这决定了我们对它的理解和重建程度。换句话说，我们的目标是在稀疏、无约束的视图下确定每个3D点及其相关信息的起源或出处。我们介绍了ProvNeRF，这是一个模型，通过合并每个点的来源，为每个点的可能源位置建模，丰富了传统的NeRF表示。我们通过扩展随机过程的隐式最大似然估计（IMLE）来实现这一点。值得注意的是，我们的方法与任何预先训练的NeRF模型和相关的训练相机姿势兼容。我们证明，与最先进的方法相比，逐点源建模提供了几个优势，包括不确定性估计、基于标准的视图选择和改进的新视图合成。请访问我们的项目页面https://provnerf.github.io et.al.|[2401.08140](http://arxiv.org/abs/2401.08140)|null|
|**2024-01-11**|**TRIPS: Trilinear Point Splatting for Real-Time Radiance Field Rendering**|基于点的辐射场渲染在新颖的视图合成中表现出了令人印象深刻的结果，提供了令人信服的渲染质量和计算效率的结合。然而，这一领域的最新方法也并非没有缺点。3D高斯飞溅[Kerbl和Kopanas等人2023]在渲染高度详细的场景时，由于模糊和模糊的伪影，会遇到困难。另一方面ADOP[R\“uckert et al.2022]可以容纳更清晰的图像，但神经重建网络会降低性能，它会处理时间不稳定性，并且无法有效地解决点云中的大间隙。在本文中，我们提出了TRIPS（Trilinear point Splatting），一种结合了Gaussian Splatting和ADOP思想的方法。我们的新技术背后的基本概念包括将点光栅化为屏幕空间图像金字塔，金字塔层的选择由投影点的大小决定。这种方法允许使用单个三线性写入来渲染任意大的点。然后使用轻量级神经网络来重建包括超出飞溅分辨率的细节的无孔图像。重要的是，我们的渲染管道是完全可微分的，允许点大小和位置的自动优化。我们的评估表明，TRIPS在渲染质量方面超过了现有的最先进的方法，同时在现成的硬件上保持了每秒60帧的实时帧速率。这种性能扩展到具有挑战性的场景，例如具有复杂几何形状、广阔景观和自动曝光镜头的场景。 et.al.|[2401.06003](http://arxiv.org/abs/2401.06003)|null|
|**2024-01-10**|**Diffusion Priors for Dynamic View Synthesis from Monocular Videos**|动态新颖视图合成旨在捕捉视频中视觉内容的时间演变。现有的方法很难区分运动和结构，特别是在相机姿态与对象运动相比未知或受约束的情况下。此外，仅使用来自参考图像的信息，对在给定视频中被遮挡或部分观察到的看不见的区域产生幻觉是极具挑战性的。为了解决这些问题，我们首先使用定制技术在视频帧上微调预训练的RGB-D扩散模型。随后，我们将微调模型中的知识提取为包括动态和静态神经辐射场（NeRF）分量的4D表示。所提出的流水线在保持场景同一性的同时实现了几何一致性。我们进行了深入的实验，以定性和定量地评估所提出方法的有效性。我们的结果证明了我们的方法在具有挑战性的情况下的稳健性和实用性，进一步推进了动态新视图合成。 et.al.|[2401.05583](http://arxiv.org/abs/2401.05583)|null|
|**2024-01-09**|**Morphable Diffusion: 3D-Consistent Diffusion for Single-image Avatar Creation**|生成扩散模型的最新进展已经实现了从单个输入图像或文本提示生成3D资产的先前不可行的能力。在这项工作中，我们的目标是提高这些模型的质量和功能，以完成创建可控、照片真实感的人类化身的任务。我们通过将3D可变形模型集成到最先进的多视角一致扩散方法中来实现这一点。我们证明了生成管道在关节式3D模型上的精确调节增强了基线模型在从单个图像合成新视图任务中的性能。更重要的是，这种集成有助于将面部表情和身体姿势控制无缝准确地结合到生成过程中。据我们所知，我们提出的框架是第一个扩散模型，能够从看不见的物体的单个图像中创建完全3D一致、可动画化和照片真实感的人类化身；大量的定量和定性评估证明了我们的方法在新视角和新表情合成任务上优于现有的最先进的化身创建模型。 et.al.|[2401.04728](http://arxiv.org/abs/2401.04728)|null|

<p align=right>(<a href=#updated-on-20240124>back to top</a>)</p>

## MLLM

|Publish Date|Title|Abstract|PDF|Code|
|---|---|-----------------------------------|---|---|
|**2024-01-22**|**A Saliency Enhanced Feature Fusion based multiscale RGB-D Salient Object Detection Network**|多尺度卷积神经网络（CNN）在解决各种视觉问题方面表现出了非凡的能力。然而，融合不同尺度的特征总是导致模型尺寸大，阻碍了多尺度细胞神经网络在RGB-D显著性检测中的应用。在本文中，我们提出了一种定制的特征融合模块，称为显著性增强特征融合（SEFF），用于RGB-D显著性检测。SEFF利用相邻尺度的显著性图来增强融合所需的特征，从而产生更具代表性的融合特征。我们的多尺度RGB-D显著性检测器使用SEFF并处理具有三个不同尺度的图像。SEFF用于融合RGB和深度图像的特征，以及不同尺度的解码器的特征。在五个基准数据集上的大量实验已经证明了我们的方法优于十个SOTA显著性检测器。 et.al.|[2401.11914](http://arxiv.org/abs/2401.11914)|null|
|**2024-01-22**|**SuperCLUE-Math6: Graded Multi-Step Math Reasoning Benchmark for LLMs in Chinese**|我们介绍了SuperCLUE-Math6（SC-Math6），这是一个新的基准数据集，用于评估汉语模型的数学推理能力。SC-Math6是GSM8K数据集的升级中文版，具有更强的难度、多样性和应用范围。它由2000多个数学单词问题组成，需要多步骤推理并提供自然语言解决方案。我们提出了一种创新方案，根据不同推理步骤问题的性能来量化大型模型的推理能力。在12个具有代表性的中国模型上进行的实验表明，推理水平分层清晰，GPT-4等顶级模型表现出优异的性能。SC-Math6填补了中国数学推理基准的空白，为提高汉语模型的智能性提供了一个全面的测试平台。 et.al.|[2401.11819](http://arxiv.org/abs/2401.11819)|null|
|**2024-01-22**|**P2DT: Mitigating Forgetting in task-incremental Learning with progressive prompt Decision Transformer**|灾难性遗忘对管理由大型模型控制的智能代理提出了重大挑战，当这些代理面临新任务时，会导致性能下降。在我们的工作中，我们提出了一种新的解决方案——渐进式即时决策转换器（P2DT）。该方法通过在新任务训练期间动态附加决策令牌来增强基于转换器的模型，从而促进特定于任务的策略。我们的方法可以缓解持续和离线强化学习场景中的遗忘。此外，P2DT利用了通过传统强化学习从所有任务中收集的轨迹，并在训练过程中生成新的任务特定令牌，从而保留了先前研究的知识。初步结果表明，我们的模型有效地缓解了灾难性遗忘，并能很好地适应不断增加的任务环境。 et.al.|[2401.11666](http://arxiv.org/abs/2401.11666)|null|
|**2024-01-17**|**Generative Denoise Distillation: Simple Stochastic Noises Induce Efficient Knowledge Transfer for Dense Prediction**|知识提炼是将知识从更强大的大模型（教师）转移到更简单的模型（学生）的过程。目前的许多方法都涉及学生直接模仿老师的知识。然而，通过这些流行的方法，在学习的表示中仍然存在冗余，这些方法倾向于不加区别地学习每个空间位置的特征。为了从教师那里获得更紧凑的表示（概念特征），受人类认知的启发，我们提出了一种创新的方法，称为生成去噪蒸馏（GDD），其中将随机噪声添加到学生的概念特征中，以将其嵌入浅层网络生成的实例特征中。然后，将生成的实例特征与来自老师的实例知识对齐。我们对对象检测、实例分割和语义分割进行了广泛的实验，以证明我们的方法的通用性和有效性。值得注意的是，GDD在上述任务中实现了最先进的性能。我们通过增强基于ResNet-18的PspNet和DeepLabV3，在语义分割方面取得了实质性的改进，mIoU得分分别为74.67和77.69，超过了他们之前在20个类别的Cityscapes数据集上的69.85和73.20分。源代码位于https://github.com/ZhgLiu/GDD. et.al.|[2401.08332](http://arxiv.org/abs/2401.08332)|null|
|**2024-01-16**|**Multitask Learning in Minimally Invasive Surgical Vision: A Review**|微创手术（MIS）已经彻底改变了许多程序，并减少了患者的恢复时间和受伤风险。然而，MIS给外科团队带来了额外的复杂性和负担。数据驱动的手术视觉算法被认为是开发具有改进自主性的未来MIS系统的关键构建块。机器学习和计算机视觉的最新进展已成功应用于分析从MIS获得的视频，有望缓解MIS视频中的挑战。手术场景和动作理解包括多个相关任务，当单独解决时，这些任务可能会占用大量记忆，效率低下，并且无法捕捉任务关系。多任务学习（MTL）是一种利用来自多个相关任务的信息来提高性能和帮助泛化的学习范式，非常适合对MIS数据进行细粒度和高级理解。这篇综述概述了当前最先进的MTL系统，这些系统利用了从MIS获得的视频。除了列出已发表的方法外，我们还讨论了这些MTL系统的优点和局限性。此外，本文还分析了MTL在MIS中各个应用领域的文献，包括那些具有大型模型的文献，强调了显著的趋势、新的研究方向和发展。 et.al.|[2401.08256](http://arxiv.org/abs/2401.08256)|null|
|**2024-01-16**|**A Survey of Resource-efficient LLM and Multimodal Foundation Models**|大型基础模型，包括大型语言模型（LLM）、视觉转换器（ViT）、扩散和基于LLM的多模式模型，正在彻底改变从训练到部署的整个机器学习生命周期。然而，这些型号在多功能性和性能方面的巨大进步在硬件资源方面付出了巨大的代价。为了以可扩展和环境可持续的方式支持这些大型模型的发展，人们相当重视制定资源节约型战略。这项调查深入探讨了此类研究的关键重要性，考察了算法和系统两个方面。它提供了从现有文献中收集的全面分析和有价值的见解，涵盖了从尖端模型架构和训练/服务算法到实际系统设计和实现的广泛主题。这项调查的目标是全面了解当前的方法是如何应对大型基础模型带来的资源挑战的，并有可能激励未来在这一领域取得突破。 et.al.|[2401.08092](http://arxiv.org/abs/2401.08092)|**[link](https://github.com/ubiquitouslearning/efficient_foundation_model_survey)**|
|**2024-01-21**|**PDE Generalization of In-Context Operator Networks: A Study on 1D Scalar Nonlinear Conservation Laws**|我们能为广泛的PDE相关科学学习任务建立一个单一的大型模型吗？这个模型能在没有任何微调的情况下推广到新的偏微分方程，甚至是新形式的偏微分函数吗？上下文中操作员学习和相应的上下文中操作员网络（ICON）模型代表了对这些问题的初步探索。ICON关于第一个问题的能力已经在前面进行了演示。在本文中，我们提出了一种使用ICON解决PDE问题的详细方法，并展示了单个ICON模型如何在适当设计的数据提示下，以不同的步长对不同的方程进行正向和反向预测。我们为第二个问题提供了积极的证据，即ICON可以很好地推广到一些具有新形式的偏微分方程，而不需要任何微调。这可以通过对一维标量非线性守恒定律的研究来证明，这是一个具有时间演化的偏微分方程族。我们还展示了如何通过将函数和方程转换到ICON的能力范围来拓宽ICON模型可以解决的问题范围。我们认为，本文的进展是朝着在上下文操作员学习框架下训练PDE相关任务的基础模型的目标迈出的重要一步。 et.al.|[2401.07364](http://arxiv.org/abs/2401.07364)|null|
|**2024-01-11**|**HAP: SPMD DNN Training on Heterogeneous GPU Clusters with Automated Program Synthesis**|单程序多数据并行（SPMD）最近被用于训练大型深度神经网络（DNN）。很少有研究探讨其在异构集群中的适用性，以充分利用可用资源进行大型模型学习。本文介绍了OurSystem，这是一个旨在加快异构集群上SPMD DNN训练的自动化系统。\OurSystem联合优化了张量分片策略、异构设备的分片率以及张量交换的通信方法，以实现SPMD并行性的优化分布式训练。我们新颖地将模型划分公式化为程序合成问题，在该问题中，我们在语义上类似于为单个设备设计的程序的分布式指令集上从头开始生成分布式程序，并使用基于a*的搜索算法系统地探索解空间。我们通过将其公式化为线性规划问题来推导最优张量分片率。此外，\OurSystem探索了异构集群中的张量通信优化，并将其集成为节目合成过程的一部分，用于自动选择最佳集体通信原语并应用充分因子广播技术。在具有代表性的工作负载上进行的大量实验表明，\OurSystem在异构集群上实现了高达2.41x的加速。 et.al.|[2401.05965](http://arxiv.org/abs/2401.05965)|**[link](https://github.com/alibaba/hap)**|
|**2024-01-11**|**MatSAM: Efficient Materials Microstructure Extraction via Visual Large Model**|准确有效地提取材料微观图像中的微观结构在探索结构-性能关系和优化工艺参数方面发挥着关键作用。基于深度学习的图像分割技术依赖于手动注释，耗时耗力，难以满足模型可移植性和泛化的要求。Segment Anything Model（SAM）是一种具有强大的深度特征表示和零样本泛化能力的大型视觉模型，为图像分割提供了新的解决方案。然而，在没有人为注释的情况下直接应用SAM来分割材料微观图像中的微观结构并不能达到预期的结果，因为难以使其原生的即时工程适应材料微观图像的关键微观结构的密集和分散特征。在本文中，我们提出了一种基于SAM的通用高效的微观结构提取解决方案MatSAM。根据材料微观结构的分布和形状，设计了一种新的基于点的提示生成策略。它为不同的微观图像生成提示，融合感兴趣区域（ROI）关键点和网格关键点的提示，并集成后处理方法对材料微观结构进行定量表征。对于包括晶界和相在内的常见微观结构，MatSAM实现了优于传统方法的分割性能，甚至优于对光学显微镜（OM）和扫描电子显微镜（SEM）成像的18种材料微观结构进行评估的监督学习方法。我们相信，MatSAM可以显著降低材料微观结构定量表征的成本，并加快新材料的设计。 et.al.|[2401.05638](http://arxiv.org/abs/2401.05638)|null|
|**2024-01-10**|**Large Model based Sequential Keyframe Extraction for Video Summarization**|关键帧提取旨在用视频的最小帧数来总结视频的语义。本文提出了一种基于大模型的视频摘要序列关键帧提取方法，称为LMSKE，它包括以下三个阶段。首先，我们使用大模型“TransNetV21”将视频剪切成连续的镜头，并使用大模型”CLIP2“生成每个镜头中每帧的视觉特征；其次，我们开发了一种自适应聚类算法，为每个镜头生成候选关键帧，每个候选关键帧位于离聚类中心最近的位置；第三，我们通过在每个镜头内消除冗余来进一步减少上述候选关键帧，并最终根据镜头的顺序将它们连接起来，作为最终的顺序关键帧。为了评估LMSKE，我们策划了一个基准数据集并进行了丰富的实验，实验结果表明，LMSKE的性能比相当多的SOTA竞争对手要好得多，平均F1为0.5311，平均保真度为0.8141，平均压缩比为0.9922。 et.al.|[2401.04962](http://arxiv.org/abs/2401.04962)|null|

<p align=right>(<a href=#updated-on-20240124>back to top</a>)</p>

## Diffusion

|Publish Date|Title|Abstract|PDF|Code|
|---|---|-----------------------------------|---|---|
|**2024-01-22**|**Control of OSIRIS-REx OTES Observations using OCAMS TAG Images**|当OSIRIS REx航天器朝着小行星本努下降，在即用即用（TAG）程序中从表面收集样本时，许多仪器都在积极收集观测数据。我们应用摄影测量控制过程来准确确定190幅OCAMS MapCam和SamCam下降图像在曝光时的位置和姿态。图像的平均像素分辨率为10厘米（中值为7厘米）。使用Bennu的高分辨率（5厘米、44厘米和88厘米地面样本距离）形状模型生成的模拟图像将图像控制到地面。经过最小二乘调整后，所有图像测量残差的均方根（rms）为0.16像素。通过使用从OCAMS到OTES帧的帧变换对OCAMS MapCam和SamCam仪器的更新星历表进行插值，将这些结果应用于581个OTES观测。然后，通过在44cm形状的模型上追踪调整后的视线方向的光线，重新计算OTES视场的表面截距。调整后的OTES视轴表面截距的平均值与88cm形状模型上的先验位置相差约37cm，不确定性小于5cm。 et.al.|[2401.12177](http://arxiv.org/abs/2401.12177)|null|
|**2024-01-22**|**Mastering Text-to-Image Diffusion: Recaptioning, Planning, and Generating with Multimodal LLMs**|扩散模型在文本到图像的生成和编辑方面表现出非凡的性能。然而，在处理涉及具有多个属性和关系的多个对象的复杂文本提示时，现有方法往往面临挑战。在本文中，我们提出了一种全新的无训练文本到图像生成/编辑框架，即重新适应、计划和生成（RPG），利用多模式LLM强大的思想链推理能力来增强文本到图像扩散模型的合成性。我们的方法使用MLLM作为全局规划器，将生成复杂图像的过程分解为子区域内的多个更简单的生成任务。我们提出了互补的区域扩散，以实现区域成分生成。此外，我们以闭环的方式将文本引导的图像生成和编辑集成在所提出的RPG中，从而增强了泛化能力。大量实验表明，我们的RPG优于最先进的文本到图像扩散模型，包括DALL-E 3和SDXL，特别是在多类别对象合成和文本-图像语义对齐方面。值得注意的是，我们的RPG框架与各种MLLM架构（例如，MiniGPT-4）和扩散骨干网（例如，ControlNet）具有广泛的兼容性。我们的代码位于：https://github.com/YangLing0818/RPG-DiffusionMaster et.al.|[2401.11708](http://arxiv.org/abs/2401.11708)|**[link](https://github.com/yangling0818/rpg-diffusionmaster)**|
|**2024-01-21**|**Text-to-Image Cross-Modal Generation: A Systematic Review**|我们从“跨模态生成”的角度回顾了从文本生成视觉数据的研究。这一观点使我们能够在不将分析局限于狭窄的子领域的情况下，将各种用于处理输入文本和产生视觉输出的方法进行比较。它还导致了该领域常见模板的识别，然后在类似方法库内和跨研究线进行比较和对比。我们将文本到图像的生成细分为各种风格的图像从文本方法、视频从文本方法，图像编辑、自监督和基于图的方法。在这场讨论中，我们重点关注2016-2022年在8次领先的机器学习会议上发表的研究论文，其中也包括一些与概述的搜索标准不匹配的相关论文。所进行的审查表明，该领域发表的论文数量显著增加，并突出了研究差距和潜在的调查方向。据我们所知，这是第一次从“跨模态生成”的角度系统地看待文本到图像的生成 et.al.|[2401.11631](http://arxiv.org/abs/2401.11631)|null|
|**2024-01-21**|**Scalable High-Resolution Pixel-Space Image Synthesis with Hourglass Diffusion Transformers**|我们提出了Hourglass Diffusion Transformer（HDiT），这是一种图像生成模型，它表现出与像素计数的线性缩放，支持直接在像素空间中进行高分辨率（例如1024美元\ 1024倍）的训练。基于已知可扩展到数十亿个参数的Transformer架构，它弥合了卷积U-Nets的效率和Transformer的可扩展性之间的差距。HDiT在没有典型的高分辨率训练技术（如多尺度架构、潜在的自动编码器或自我调节）的情况下成功训练。我们证明，HDiT在ImageNet $256^2美元上与现有模型相比具有竞争力，并在FFHQ上为扩散模型设置了新的最先进的技术——$ 124^2美元。 et.al.|[2401.11605](http://arxiv.org/abs/2401.11605)|null|
|**2024-01-19**|**Sat2Scene: 3D Urban Scene Generation from Satellite Images with Diffusion**|从卫星图像直接生成场景为集成到游戏和地图服务等应用程序提供了令人兴奋的可能性。然而，显著的视图变化和场景规模带来了挑战。以往的工作主要集中在图像或视频生成上，缺乏对场景生成对任意视图的适应性的探索。现有的3D生成工作要么在物体层面进行操作，要么难以利用从卫星图像中获得的几何形状。为了克服这些限制，我们提出了一种新的直接3D场景生成架构，方法是将扩散模型引入3D稀疏表示中，并将其与神经渲染技术相结合。具体而言，我们的方法首先使用3D扩散模型在给定几何体的点级别生成纹理颜色，然后以前馈方式将其转换为场景表示。该表示可以用于渲染任意视图，这些视图在单帧质量和帧间一致性方面都很出色。在两个城市规模的数据集上的实验表明，我们的模型证明了从卫星图像中生成照片逼真的街景图像序列和交叉视图城市场景的能力。 et.al.|[2401.10786](http://arxiv.org/abs/2401.10786)|null|
|**2024-01-18**|**Inflation with Diffusion: Efficient Temporal Adaptation for Text-to-Video Super-Resolution**|我们提出了一种有效的基于扩散的文本到视频超分辨率（SR）调整方法，该方法利用像素级图像扩散模型的易于学习的能力来捕获用于视频生成的空间信息。为了实现这一目标，我们通过将文本到图像SR模型的权重膨胀到我们的视频生成框架中来设计一种有效的架构。此外，我们还加入了一个时间适配器，以确保视频帧之间的时间一致性。我们研究了基于膨胀架构的不同调整方法，并报告了计算成本和超分辨率质量之间的权衡。对Shutterstock视频数据集的定量和定性实证评估表明，我们的方法能够以良好的视觉质量和时间一致性执行文本到视频的SR生成。为了评估时间连贯性，我们还将视频格式的可视化呈现在https://drive.google.com/drive/folders/1YVc-KMSJqOrEUdQWVaI-Yfu8Vsfu_1aO?usp=sharing. et.al.|[2401.10404](http://arxiv.org/abs/2401.10404)|null|
|**2024-01-22**|**Motion-Zero: Zero-Shot Moving Object Control Framework for Diffusion-Based Video Generation**|最近的大规模预训练扩散模型已经证明了从详细的文本描述中产生高质量视频的强大生成能力。然而，对由任何视频扩散模型生成的视频中的对象的运动施加控制是一个具有挑战性的问题。在本文中，我们提出了一种新的零样本运动物体轨迹控制框架Motion-zero，以实现边界-边界-目标-控制的文本到视频扩散模型。为此，初始噪声先验模块被设计为提供基于位置的先验，以提高移动物体的外观稳定性和位置精度。此外，基于U-net的注意力图，将空间约束直接应用于扩散模型的去噪过程，进一步确保了推理过程中运动对象的位置和空间一致性。此外，所提出的转移时间注意力机制保证了时间一致性。我们的方法可以灵活地应用于各种最先进的视频扩散模型，而无需任何训练过程。大量实验表明，我们提出的方法可以控制物体的运动轨迹，生成高质量的视频。 et.al.|[2401.10150](http://arxiv.org/abs/2401.10150)|null|
|**2024-01-18**|**DiffusionGPT: LLM-Driven Text-to-Image Generation System**|扩散模型为图像生成领域开辟了新的途径，导致开源平台上共享的高质量模型激增。然而，一个主要挑战仍然存在于当前的文本到图像系统中，该系统通常无法处理不同的输入，或者仅限于单个模型结果。目前的统一尝试通常分为两个正交方面：一是在输入阶段解析不同的提示；ii）激活专家模型进行输出。为了将两者的优点结合起来，我们提出了DiffusionGPT，它利用大型语言模型（LLM）提供一个统一的生成系统，能够无缝地适应各种类型的提示并集成领域专家模型。DiffusionGPT基于先验知识为各种生成模型构建领域特定树。当提供输入时，LLM解析提示，并使用思想树来指导选择适当的模型，从而放松输入约束，确保跨不同领域的卓越性能。此外，我们引入了优势数据库，其中思想树富含人类反馈，使模型选择过程与人类偏好保持一致。通过广泛的实验和比较，我们展示了DiffusionGPT的有效性，展示了其在不同领域突破图像合成边界的潜力。 et.al.|[2401.10061](http://arxiv.org/abs/2401.10061)|null|
|**2024-01-18**|**WorldDreamer: Towards General World Models for Video Generation via Predicting Masked Tokens**|世界模型在理解和预测世界动态方面发挥着至关重要的作用，这对视频生成至关重要。然而，现有的世界模型仅限于游戏或驾驶等特定场景，限制了它们捕捉一般世界动态环境复杂性的能力。因此，我们引入了WorldDreamer，这是一个开创性的世界模型，旨在促进对一般世界物理和运动的全面理解，从而显著增强视频生成的能力。WorldDreamer从大型语言模型的成功中汲取灵感，将世界建模视为一种无监督的视觉序列建模挑战。这是通过将视觉输入映射到离散标记并预测被屏蔽的标记来实现的。在这个过程中，我们结合了多模式提示，以促进世界模型中的交互。我们的实验表明，WorldDreamer擅长在不同场景中生成视频，包括自然场景和驾驶环境。WorldDreamer展示了执行文本到视频转换、图像到视频合成和视频编辑等任务的多功能性。这些结果强调了WorldDreamer在不同的一般世界环境中捕捉动态元素的有效性。 et.al.|[2401.09985](http://arxiv.org/abs/2401.09985)|null|
|**2024-01-18**|**CustomVideo: Customizing Text-to-Video Generation with Multiple Subjects**|定制的文本到视频生成旨在通过文本提示和主题参考生成高质量的视频。目前为单一主题设计的方法难以解决多个主题，这是一个更具挑战性和实用性的场景。在这项工作中，我们旨在促进多主题引导文本到视频定制。我们提出了CustomVideo，这是一个新的框架，可以在多个主题的指导下生成身份保护视频。具体来说，首先，我们通过将多个主体组合在一个图像中来鼓励它们的共同出现。此外，在一个基本的文本到视频扩散模型的基础上，我们设计了一种简单而有效的注意力控制策略来解开扩散模型潜在空间中的不同主体。此外，为了帮助模型聚焦于特定的对象区域，我们从给定的参考图像中分割对象，并为注意力学习提供相应的对象掩码。此外，我们收集了一个多主题文本到视频生成数据集作为综合基准，其中包括69个单独的主题和57个有意义的配对。大量的定性、定量和用户研究结果表明，与以前最先进的方法相比，我们的方法具有优越性。 et.al.|[2401.09962](http://arxiv.org/abs/2401.09962)|null|

<p align=right>(<a href=#updated-on-20240124>back to top</a>)</p>

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

<p align=right>(<a href=#updated-on-20240124>back to top</a>)</p>

[contributors-shield]: https://img.shields.io/github/contributors/Vincentqyw/cv-arxiv-daily.svg?style=for-the-badge
[contributors-url]: https://github.com/Vincentqyw/cv-arxiv-daily/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/Vincentqyw/cv-arxiv-daily.svg?style=for-the-badge
[forks-url]: https://github.com/Vincentqyw/cv-arxiv-daily/network/members
[stars-shield]: https://img.shields.io/github/stars/Vincentqyw/cv-arxiv-daily.svg?style=for-the-badge
[stars-url]: https://github.com/Vincentqyw/cv-arxiv-daily/stargazers
[issues-shield]: https://img.shields.io/github/issues/Vincentqyw/cv-arxiv-daily.svg?style=for-the-badge
[issues-url]: https://github.com/Vincentqyw/cv-arxiv-daily/issues

