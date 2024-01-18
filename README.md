[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]

## Updated on 2024.01.18
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
|**2024-01-17**|**Objects With Lighting: A Real-World Dataset for Evaluating Reconstruction and Rendering for Object Relighting**|从照片中重建对象并将其虚拟地放置在新环境中超出了标准的新颖视图合成任务，因为对象的外观不仅要适应新颖的视点，还要适应新的照明条件，而且反向渲染方法的评估依赖于新颖的视图合成数据或用于定量分析的简单合成数据集。这项工作提供了一个真实世界的数据集，用于测量重新照明对象的重建和渲染。为此，我们捕获了多个环境中相同对象的环境照明和地面实况图像，从而可以从一个环境中拍摄的图像中重建对象，并量化看不见的照明环境的渲染视图的质量。此外，我们介绍了一个由现成方法组成的简单基线，并在重新照明任务中测试了几种最先进的方法，表明新的视图合成不是衡量性能的可靠指标。代码和数据集可在https://github.com/isl-org/objects-with-lighting. et.al.|[2401.09126](http://arxiv.org/abs/2401.09126)|null|
|**2024-01-17**|**ICON: Incremental CONfidence for Joint Pose and Radiance Field Optimization**|在给定一组2D图像的情况下，神经辐射场（NeRF）在新视图合成（NVS）中表现出显著的性能。然而，NeRF训练需要每个输入视图的精确相机姿势，通常通过运动结构（SfM）管道获得。最近的作品试图放松这种限制，但它们仍然经常依赖于可以改进的体面的初始姿势。在这里，我们旨在消除姿势初始化的要求。我们提出了增量置信（ICON），这是一种从2D视频帧中训练NeRF的优化过程。ICON仅假设相机运动平滑，以估计姿势的初始猜测。此外，ICON引入了“置信度”：一种用于动态重加权梯度的模型质量自适应度量。ICON依赖于高置信度姿势来学习NeRF，并依赖于高置信度3D结构（由NeRF编码）来学习姿势。我们表明，与使用SfM姿势的方法相比，ICON在没有预先初始化姿势的情况下，在CO3D和HO3D中都实现了卓越的性能。 et.al.|[2401.08937](http://arxiv.org/abs/2401.08937)|null|
|**2024-01-16**|**Fast Dynamic 3D Object Generation from a Single-view Video**|由于缺乏4D标记的数据，从单视图视频生成动态三维（3D）对象是具有挑战性的。现有方法通过传输现成的图像生成模型（如分数蒸馏采样）来扩展文本到3D管道，但由于需要通过大型预训练模型反向传播信息有限的监督信号，这些方法的扩展速度慢且成本高（例如，每个对象150分钟）。为了解决这一限制，我们提出了一种高效的视频到4D对象生成框架，称为Efficient4D。它在不同的相机视图下生成高质量的时空一致图像，然后将其用作标记数据，直接训练具有显式点云几何结构的新型4D高斯飞溅模型，实现在连续相机轨迹下的实时渲染。对合成视频和真实视频的广泛实验表明，与现有技术的替代方案相比，Efficient4D的速度显著提高了10倍，同时保持了相同水平的创新视图合成质量。例如，Efficient4D只需14分钟即可对动态对象进行建模。 et.al.|[2401.08742](http://arxiv.org/abs/2401.08742)|null|
|**2024-01-16**|**ProvNeRF: Modeling per Point Provenance in NeRFs as a Stochastic Process**|神经辐射场（NeRFs）在各种应用中越来越受欢迎。然而，它们在稀疏视图设置中面临挑战，缺乏来自体积渲染的足够约束。在具有多种应用的经典计算机视觉中，从稀疏和无约束的相机重建和理解3D场景是一个长期存在的问题。虽然最近的工作在稀疏、无约束的视图场景中探索了NeRF，但他们的重点主要是增强重建和新颖的视图合成。我们的方法从更广泛的角度出发，提出了一个问题：“从哪里看到了每个点？”——这决定了我们对它的理解和重建程度。换句话说，我们的目标是在稀疏、无约束的视图下确定每个3D点及其相关信息的起源或出处。我们介绍了ProvNeRF，这是一个模型，通过合并每个点的来源，为每个点的可能源位置建模，丰富了传统的NeRF表示。我们通过扩展随机过程的隐式最大似然估计（IMLE）来实现这一点。值得注意的是，我们的方法与任何预先训练的NeRF模型和相关的训练相机姿势兼容。我们证明，与最先进的方法相比，逐点源建模提供了几个优势，包括不确定性估计、基于标准的视图选择和改进的新视图合成。 et.al.|[2401.08140](http://arxiv.org/abs/2401.08140)|null|
|**2024-01-11**|**TRIPS: Trilinear Point Splatting for Real-Time Radiance Field Rendering**|基于点的辐射场渲染在新颖的视图合成中表现出了令人印象深刻的结果，提供了令人信服的渲染质量和计算效率的结合。然而，这一领域的最新方法也并非没有缺点。3D高斯飞溅[Kerbl和Kopanas等人2023]在渲染高度详细的场景时，由于模糊和模糊的伪影，会遇到困难。另一方面ADOP[R\“uckert et al.2022]可以容纳更清晰的图像，但神经重建网络会降低性能，它会处理时间不稳定性，并且无法有效地解决点云中的大间隙。在本文中，我们提出了TRIPS（Trilinear point Splatting），一种结合了Gaussian Splatting和ADOP思想的方法。我们的新技术背后的基本概念包括将点光栅化为屏幕空间图像金字塔，金字塔层的选择由投影点的大小决定。这种方法允许使用单个三线性写入来渲染任意大的点。然后使用轻量级神经网络来重建包括超出飞溅分辨率的细节的无孔图像。重要的是，我们的渲染管道是完全可微分的，允许点大小和位置的自动优化。我们的评估表明，TRIPS在渲染质量方面超过了现有的最先进的方法，同时在现成的硬件上保持了每秒60帧的实时帧速率。这种性能扩展到具有挑战性的场景，例如具有复杂几何形状、广阔景观和自动曝光镜头的场景。 et.al.|[2401.06003](http://arxiv.org/abs/2401.06003)|null|
|**2024-01-10**|**Diffusion Priors for Dynamic View Synthesis from Monocular Videos**|动态新颖视图合成旨在捕捉视频中视觉内容的时间演变。现有的方法很难区分运动和结构，特别是在相机姿态与对象运动相比未知或受约束的情况下。此外，仅使用来自参考图像的信息，对在给定视频中被遮挡或部分观察到的看不见的区域产生幻觉是极具挑战性的。为了解决这些问题，我们首先使用定制技术在视频帧上微调预训练的RGB-D扩散模型。随后，我们将微调模型中的知识提取为包括动态和静态神经辐射场（NeRF）分量的4D表示。所提出的流水线在保持场景同一性的同时实现了几何一致性。我们进行了深入的实验，以定性和定量地评估所提出方法的有效性。我们的结果证明了我们的方法在具有挑战性的情况下的稳健性和实用性，进一步推进了动态新视图合成。 et.al.|[2401.05583](http://arxiv.org/abs/2401.05583)|null|
|**2024-01-09**|**Morphable Diffusion: 3D-Consistent Diffusion for Single-image Avatar Creation**|生成扩散模型的最新进展已经实现了从单个输入图像或文本提示生成3D资产的先前不可行的能力。在这项工作中，我们的目标是提高这些模型的质量和功能，以完成创建可控、照片真实感的人类化身的任务。我们通过将3D可变形模型集成到最先进的多视角一致扩散方法中来实现这一点。我们证明了生成管道在关节式3D模型上的精确调节增强了基线模型在从单个图像合成新视图任务中的性能。更重要的是，这种集成有助于将面部表情和身体姿势控制无缝准确地结合到生成过程中。据我们所知，我们提出的框架是第一个扩散模型，能够从看不见的物体的单个图像中创建完全3D一致、可动画化和照片真实感的人类化身；大量的定量和定性评估证明了我们的方法在新视角和新表情合成任务上优于现有的最先进的化身创建模型。 et.al.|[2401.04728](http://arxiv.org/abs/2401.04728)|null|
|**2024-01-07**|**See360: Novel Panoramic View Interpolation**|我们介绍了See360，它是一种使用潜在空间视点估计进行360全景插值的通用且高效的框架。大多数现有的视图渲染方法只关注室内或合成三维环境，并渲染小对象的新视图。相反，我们建议将以相机为中心的视图合成作为2D仿射变换来处理，而不使用点云或深度图，这使得能够实现有效的360？全景场景探索。给定一对参考图像，See360模型通过提出的新颖的多尺度仿射变换器（MSAT）来学习渲染新颖的视图，从而实现从粗到细的特征渲染。我们还提出了一种条件潜在空间自动编码器（C-LAE）来实现任意角度的视图插值。为了展示我们方法的多功能性，我们引入了四个训练数据集，即UrbanCity360、Archinterior360、HungHom360和Lab360，它们是从室内和室外环境中收集的，用于真实和合成渲染。实验结果表明，该方法具有足够的通用性，可以实现四个数据集任意视图的实时绘制。此外，我们的See360模型可以应用于野外的视图合成：只需很短的额外训练时间（约10分钟），并且能够渲染未知的真实世界场景。See360的卓越性能为以相机为中心的视图渲染和360全景视图插值开辟了一个很有前途的方向。 et.al.|[2401.03431](http://arxiv.org/abs/2401.03431)|**[link](https://github.com/Holmes-Alan/See360)**|
|**2024-01-06**|**RustNeRF: Robust Neural Radiance Field with Low-Quality Images**|最近在神经辐射场（NeRF）方面的工作利用了多视图三维一致性，在三维场景建模和高保真新颖视图合成方面取得了令人印象深刻的结果。然而，也有局限性。首先，现有方法假设有足够的高质量图像可用于训练NeRF模型，忽略了真实世界的图像退化。其次，由于不同视图之间未建模的不一致性，以前的方法在训练集中难以解决模糊性问题。在这项工作中，我们为真实世界的高质量NeRF提供了RustNeRF。为了提高NeRF在真实世界输入下的鲁棒性，我们训练了一个包含真实世界退化建模的3D感知预处理网络。我们提出了一种新的隐式多视图引导来解决图像退化和恢复过程中的信息丢失问题。大量实验证明了RustNeRF在实际退化情况下优于现有方法。代码将被发布。 et.al.|[2401.03257](http://arxiv.org/abs/2401.03257)|null|
|**2024-01-02**|**Street Gaussians for Modeling Dynamic Urban Scenes**|本文旨在解决从单目视频中建模动态城市街道场景的问题。最近的方法扩展了NeRF，将跟踪车辆姿态纳入车辆动画，实现了动态城市街道场景的照片逼真视图合成。然而，它们的显著局限性在于训练和渲染速度慢，再加上履带车辆姿态对高精度的迫切需求。我们介绍了Street Gaussians，一种新的明确的场景表示，它解决了所有这些限制。具体地说，动态城市街道被表示为一组点云，这些点云配备有语义logits和3D Gaussians，每一个都与前景车辆或背景相关联。为了对前景对象车辆的动力学进行建模，使用可优化的跟踪姿态以及动态外观的动态球面谐波模型对每个对象点云进行优化。显式表示允许容易地合成目标车辆和背景，这反过来又允许在半小时的训练内以133 FPS（1066 $\times$ 1600分辨率）进行场景编辑操作和渲染。所提出的方法在多个具有挑战性的基准上进行了评估，包括KITTI和Waymo Open数据集。实验表明，在所有数据集上，所提出的方法始终优于最先进的方法。此外，尽管仅依赖于现成跟踪器的姿态，但所提出的表示提供的性能与使用精确的地面实况姿态所实现的性能不相上下。代码位于https://zju3dv.github.io/street_gaussians/. et.al.|[2401.01339](http://arxiv.org/abs/2401.01339)|null|

<p align=right>(<a href=#updated-on-20240118>back to top</a>)</p>

## MLLM

|Publish Date|Title|Abstract|PDF|Code|
|---|---|-----------------------------------|---|---|
|**2024-01-17**|**Generative Denoise Distillation: Simple Stochastic Noises Induce Efficient Knowledge Transfer for Dense Prediction**|知识提炼是将知识从更强大的大模型（教师）转移到更简单的模型（学生）的过程。目前的许多方法都涉及学生直接模仿老师的知识。然而，通过这些流行的方法，在学习的表示中仍然存在冗余，这些方法倾向于不加区别地学习每个空间位置的特征。为了从教师那里获得更紧凑的表示（概念特征），受人类认知的启发，我们提出了一种创新的方法，称为生成去噪蒸馏（GDD），其中将随机噪声添加到学生的概念特征中，以将其嵌入浅层网络生成的实例特征中。然后，将生成的实例特征与来自老师的实例知识对齐。我们对对象检测、实例分割和语义分割进行了广泛的实验，以证明我们的方法的通用性和有效性。值得注意的是，GDD在上述任务中实现了最先进的性能。我们通过增强基于ResNet-18的PspNet和DeepLabV3，在语义分割方面取得了实质性的改进，mIoU得分分别为74.67和77.69，超过了他们之前在20个类别的Cityscapes数据集上的69.85和73.20分。源代码位于https://github.com/ZhgLiu/GDD. et.al.|[2401.08332](http://arxiv.org/abs/2401.08332)|**[link](https://github.com/ZhgLiu/GDD)**|
|**2024-01-16**|**Multitask Learning in Minimally Invasive Surgical Vision: A Review**|微创手术（MIS）已经彻底改变了许多程序，并减少了患者的恢复时间和受伤风险。然而，MIS给外科团队带来了额外的复杂性和负担。数据驱动的手术视觉算法被认为是开发具有改进自主性的未来MIS系统的关键构建块。机器学习和计算机视觉的最新进展已成功应用于分析从MIS获得的视频，有望缓解MIS视频中的挑战。手术场景和动作理解包括多个相关任务，当单独解决时，这些任务可能会占用大量记忆，效率低下，并且无法捕捉任务关系。多任务学习（MTL）是一种利用来自多个相关任务的信息来提高性能和帮助泛化的学习范式，非常适合对MIS数据进行细粒度和高级理解。这篇综述概述了当前最先进的MTL系统，这些系统利用了从MIS获得的视频。除了列出已发表的方法外，我们还讨论了这些MTL系统的优点和局限性。此外，本文还分析了MTL在MIS中各个应用领域的文献，包括那些具有大型模型的文献，强调了显著的趋势、新的研究方向和发展。 et.al.|[2401.08256](http://arxiv.org/abs/2401.08256)|null|
|**2024-01-16**|**A Survey of Resource-efficient LLM and Multimodal Foundation Models**|大型基础模型，包括大型语言模型（LLM）、视觉转换器（ViT）、扩散和基于LLM的多模式模型，正在彻底改变从训练到部署的整个机器学习生命周期。然而，这些型号在多功能性和性能方面的巨大进步在硬件资源方面付出了巨大的代价。为了以可扩展和环境可持续的方式支持这些大型模型的发展，人们相当重视制定资源节约型战略。这项调查深入探讨了此类研究的关键重要性，考察了算法和系统两个方面。它提供了从现有文献中收集的全面分析和有价值的见解，涵盖了从尖端模型架构和训练/服务算法到实际系统设计和实现的广泛主题。这项调查的目标是全面了解当前的方法是如何应对大型基础模型带来的资源挑战的，并有可能激励未来在这一领域取得突破。 et.al.|[2401.08092](http://arxiv.org/abs/2401.08092)|**[link](https://github.com/ubiquitouslearning/efficient_foundation_model_survey)**|
|**2024-01-14**|**PDE Generalization of In-Context Operator Networks: A Study on 1D Scalar Nonlinear Conservation Laws**|我们能为广泛的PDE相关科学学习任务建立一个单一的大型模型吗？这个模型能在没有任何微调的情况下推广到新的偏微分方程，甚至是新形式的偏微分函数吗？上下文中算子学习和相应的模型上下文中算子网络（ICON）[1]代表了对这些问题的初步探索。ICON关于第一个问题的能力已在[1]中得到证明。在本文中，我们通过研究ICON对守恒定律（一类具有时间演化的偏微分方程）的泛化能力来探索第二个问题。我们给出了第二个问题的积极答案，即ICON可以很好地推广到一些具有新形式的偏微分方程，而不需要任何微调。我们还展示了如何通过将函数和方程转换到ICON的能力范围来扩大ICON可以解决的问题的范围。我们认为，本文的进展是朝着在上下文操作员学习框架下训练PDE相关任务的基础模型的目标迈出的重要一步。 et.al.|[2401.07364](http://arxiv.org/abs/2401.07364)|null|
|**2024-01-17**|**LightHouse: A Survey of AGI Hallucination**|随着人工智能的发展，大型模型变得越来越智能。然而，大量研究表明，这些大型模型中的幻觉是阻碍人工智能研究发展的瓶颈。为了实现强大的人工智能，大量的研究工作正在投入到AGI（通用人工智能）幻觉研究中。先前的探索已经在LLM（大型语言模型）中进行了幻觉研究。至于多模式AGI，对幻觉的研究仍处于早期阶段。为了进一步推进幻觉现象领域的研究进展，我们对AGI中的幻觉进行了鸟瞰，总结了当前对AGI幻觉的研究，并提出了未来研究的方向。 et.al.|[2401.06792](http://arxiv.org/abs/2401.06792)|**[link](https://github.com/zurichrain/agi-hallucination)**|
|**2024-01-11**|**HAP: SPMD DNN Training on Heterogeneous GPU Clusters with Automated Program Synthesis**|单程序多数据并行（SPMD）最近被用于训练大型深度神经网络（DNN）。很少有研究探讨其在异构集群中的适用性，以充分利用可用资源进行大型模型学习。本文介绍了OurSystem，这是一个旨在加快异构集群上SPMD DNN训练的自动化系统。\OurSystem联合优化了张量分片策略、异构设备的分片率以及张量交换的通信方法，以实现SPMD并行性的优化分布式训练。我们新颖地将模型划分公式化为程序合成问题，在该问题中，我们在语义上类似于为单个设备设计的程序的分布式指令集上从头开始生成分布式程序，并使用基于a*的搜索算法系统地探索解空间。我们通过将其公式化为线性规划问题来推导最优张量分片率。此外，\OurSystem探索了异构集群中的张量通信优化，并将其集成为节目合成过程的一部分，用于自动选择最佳集体通信原语并应用充分因子广播技术。在具有代表性的工作负载上进行的大量实验表明，\OurSystem在异构集群上实现了高达2.41x的加速。 et.al.|[2401.05965](http://arxiv.org/abs/2401.05965)|**[link](https://github.com/alibaba/hap)**|
|**2024-01-11**|**MatSAM: Efficient Materials Microstructure Extraction via Visual Large Model**|准确有效地提取材料微观图像中的微观结构在探索结构-性能关系和优化工艺参数方面发挥着关键作用。基于深度学习的图像分割技术依赖于手动注释，耗时耗力，难以满足模型可移植性和泛化的要求。Segment Anything Model（SAM）是一种具有强大的深度特征表示和零样本泛化能力的大型视觉模型，为图像分割提供了新的解决方案。然而，在没有人为注释的情况下直接应用SAM来分割材料微观图像中的微观结构并不能达到预期的结果，因为难以使其原生的即时工程适应材料微观图像的关键微观结构的密集和分散特征。在本文中，我们提出了一种基于SAM的通用高效的微观结构提取解决方案MatSAM。根据材料微观结构的分布和形状，设计了一种新的基于点的提示生成策略。它为不同的微观图像生成提示，融合感兴趣区域（ROI）关键点和网格关键点的提示，并集成后处理方法对材料微观结构进行定量表征。对于包括晶界和相在内的常见微观结构，MatSAM实现了优于传统方法的分割性能，甚至优于对光学显微镜（OM）和扫描电子显微镜（SEM）成像的18种材料微观结构进行评估的监督学习方法。我们相信，MatSAM可以显著降低材料微观结构定量表征的成本，并加快新材料的设计。 et.al.|[2401.05638](http://arxiv.org/abs/2401.05638)|null|
|**2024-01-10**|**Large Model based Sequential Keyframe Extraction for Video Summarization**|关键帧提取旨在用视频的最小帧数来总结视频的语义。本文提出了一种基于大模型的视频摘要序列关键帧提取方法，称为LMSKE，它包括以下三个阶段。首先，我们使用大模型“TransNetV21”将视频剪切成连续的镜头，并使用大模型”CLIP2“生成每个镜头中每帧的视觉特征；其次，我们开发了一种自适应聚类算法，为每个镜头生成候选关键帧，每个候选关键帧位于离聚类中心最近的位置；第三，我们通过在每个镜头内消除冗余来进一步减少上述候选关键帧，并最终根据镜头的顺序将它们连接起来，作为最终的顺序关键帧。为了评估LMSKE，我们策划了一个基准数据集并进行了丰富的实验，实验结果表明，LMSKE的性能比相当多的SOTA竞争对手要好得多，平均F1为0.5311，平均保真度为0.8141，平均压缩比为0.9922。 et.al.|[2401.04962](http://arxiv.org/abs/2401.04962)|null|
|**2024-01-09**|**Know Your Needs Better: Towards Structured Understanding of Marketer Demands with Analogical Reasoning Augmented LLMs**|在本文中，我们探索了一种新的用户定位方式，即非专业营销人员可以以自然语言的形式仅在给定需求的情况下选择目标用户。这一问题的关键是如何将自然语言转化为实用的结构化逻辑语言，即对营销人员需求的结构化理解。考虑到大型语言模型（LLM）令人印象深刻的自然语言处理能力，我们试图利用LLM来解决这个问题。以往的研究表明，通过思维链提示可以有效地提高LLM的推理能力。但现有的方法仍有一些局限性：（1）以前的方法要么使用简单的“让我们一步一步地思考”咒语，要么在演示中提供固定的例子，而不考虑提示和问题之间的兼容性，这使得LLM在一些复杂的推理任务（如结构化语言转换）中无效。（2） 以前的方法往往在闭源模型或过大的模型中实现，不适合在工业实际场景中实现。在此基础上，我们提出了ARALLM（即类比推理增强的大型语言模型），它由两个模块组成：基于类比推理的提示和推理增强的多任务模型提取。 et.al.|[2401.04319](http://arxiv.org/abs/2401.04319)|null|
|**2024-01-09**|**Advancing Deep Active Learning & Data Subset Selection: Unifying Principles with Information-Theory Intuitions**|本文的核心是通过提高深度学习模型的标签和训练效率来增强深度学习的实用性。为此，我们研究了基于信息论原理的数据子集选择技术，特别是主动学习和主动采样。主动学习提高了标签效率，而主动采样提高了训练效率。有监督的深度学习模型通常需要使用标记数据进行广泛的训练。标签获取可能既昂贵又耗时，而且训练大型模型是资源密集型的，阻碍了学术研究和“大技术”之外的采用。深度学习中现有的数据子集选择方法往往依赖于启发式方法，或者缺乏原则性的信息论基础。相比之下，本文研究了数据子集选择的几个目标及其在深度学习中的应用，力求在信息理论的启发下找到一种更有原则的方法。我们首先将单前向传递深度神经网络中的认知不确定性和任意不确定性解开，这为不同形式的不确定性及其与数据子集选择的相关性提供了有益的直觉和见解。然后，我们提出并研究了在（贝叶斯）深度学习中进行主动学习和数据子集选择的各种方法。最后，我们将各种现有的和提出的方法与权重或预测空间中的信息量的近似联系起来。这项工作的基础是对包括随机变量和观测结果的信息论量的原则性和实用性的表示法。本文展示了从统一的角度工作的好处，并强调了我们对深度学习实际应用的贡献的潜在影响。 et.al.|[2401.04305](http://arxiv.org/abs/2401.04305)|null|

<p align=right>(<a href=#updated-on-20240118>back to top</a>)</p>

## Diffusion

|Publish Date|Title|Abstract|PDF|Code|
|---|---|-----------------------------------|---|---|
|**2024-01-17**|**Vlogger: Make Your Dream A Vlog**|在这项工作中，我们介绍了Vlogger，这是一个通用的人工智能系统，用于生成用户描述的分钟级视频博客（即vlog）。与几秒钟的短视频不同，vlog通常包含复杂的故事情节和多样化的场景，这对大多数现有的视频生成方法来说都是一个挑战。为了突破这一瓶颈，我们的Vlogger巧妙地利用大型语言模型（LLM）作为导演，将vlog的长视频生成任务分解为四个关键阶段，在这四个阶段，我们调用各种基础模型来扮演vlog专业人士的关键角色，包括（1）脚本、（2）演员、（3）ShowMaker和（4）配音员。有了这样一种模仿人类的设计，我们的Vlogger可以通过自上而下的计划和自下而上的拍摄的可解释的合作来生成vlog。此外，我们还介绍了一种新颖的视频扩散模型ShowMaker，它在我们的Vlogger中充当摄像师，用于生成每个拍摄场景的视频片段。通过将Script和Actor作为文本和视觉提示，可以有效地增强片段的时空连贯性。此外，我们为ShowMaker设计了一个简洁的混合训练范式，提高了其T2V生成和预测的能力。最后，广泛的实验表明，我们的方法在零样本T2V生成和预测任务上实现了最先进的性能。更重要的是，Vlogger可以根据开放世界的描述生成超过5分钟的视频日志，而不会失去脚本和演员的视频连贯性。代码和型号均位于https://github.com/zhuangshaobin/Vlogger. et.al.|[2401.09414](http://arxiv.org/abs/2401.09414)|null|
|**2024-01-17**|**UniVG: Towards UNIfied-modal Video Generation**|基于扩散的视频生成受到了学术界和工业界的广泛关注，并取得了相当大的成功。然而，当前的努力主要集中在单目标或单任务视频生成上，例如由文本、图像或由文本和图像的组合驱动的生成。这不能完全满足现实应用场景的需求，因为用户可能会以灵活的方式输入图像和文本条件，无论是单独输入还是组合输入。为了解决这一问题，我们提出了一种统一模式的视频生成系统，该系统能够处理文本和图像模式之间的多个视频生成任务。为此，我们从生成自由的角度重新审视了我们系统中的各种视频生成任务，并将其分为高自由度和低自由度视频生成类别。对于高自由度视频生成，我们使用多条件交叉注意来生成与输入图像或文本的语义一致的视频。对于低自由度视频生成，我们引入有偏高斯噪声来代替纯随机高斯噪声，这有助于更好地保留输入条件的内容。我们的方法在公共学术基准MSR-VTT上实现了最低的Fr’echet视频距离（FVD），在人类评估中超过了当前的开源方法，与当前的近源方法Gen2不相上下。欲了解更多样品，请访问https://univg-baidu.github.io. et.al.|[2401.09084](http://arxiv.org/abs/2401.09084)|null|
|**2024-01-17**|**VideoCrafter2: Overcoming Data Limitations for High-Quality Video Diffusion Models**|文本到视频生成旨在根据给定提示生成视频。最近，一些商业视频模型已经能够以最小的噪声、出色的细节和高的美学分数生成看似合理的视频。然而，这些模型依赖于大规模、过滤良好、高质量的视频，而这些视频是社区无法访问的。许多现有的研究工作使用低质量的WebVid-10M数据集训练模型，但由于模型经过优化以适合WebVid-10M，因此难以生成高质量的视频。在这项工作中，我们探索了从稳定扩散扩展的视频模型的训练方案，并研究了利用低质量视频和合成的高质量图像来获得高质量视频模型的可行性。我们首先分析了视频模型的空间和时间模块与向低质量视频的分布转变之间的联系。我们观察到，与仅训练时间模块相比，所有模块的完全训练导致空间和时间模块之间更强的耦合。基于这种更强的耦合，我们通过用高质量图像微调空间模块，将分布转移到更高质量，而不会出现运动退化，从而产生通用的高质量视频模型。进行了评估，以证明所提出的方法的优越性，特别是在图像质量、运动和概念合成方面。 et.al.|[2401.09047](http://arxiv.org/abs/2401.09047)|null|
|**2024-01-16**|**Fast Dynamic 3D Object Generation from a Single-view Video**|由于缺乏4D标记的数据，从单视图视频生成动态三维（3D）对象是具有挑战性的。现有方法通过传输现成的图像生成模型（如分数蒸馏采样）来扩展文本到3D管道，但由于需要通过大型预训练模型反向传播信息有限的监督信号，这些方法的扩展速度慢且成本高（例如，每个对象150分钟）。为了解决这一限制，我们提出了一种高效的视频到4D对象生成框架，称为Efficient4D。它在不同的相机视图下生成高质量的时空一致图像，然后将其用作标记数据，直接训练具有显式点云几何结构的新型4D高斯飞溅模型，实现在连续相机轨迹下的实时渲染。对合成视频和真实视频的广泛实验表明，与现有技术的替代方案相比，Efficient4D的速度显著提高了10倍，同时保持了相同水平的创新视图合成质量。例如，Efficient4D只需14分钟即可对动态对象进行建模。 et.al.|[2401.08742](http://arxiv.org/abs/2401.08742)|null|
|**2024-01-16**|**Fixed Point Diffusion Models**|我们介绍了不动点扩散模型（FPDM），这是一种新的图像生成方法，它将不动点求解的概念集成到基于扩散的生成建模框架中。我们的方法将隐式不动点求解层嵌入到扩散模型的去噪网络中，将扩散过程转化为一系列密切相关的不动点问题。与一种新的随机训练方法相结合，这种方法显著减少了模型大小，减少了内存使用，并加速了训练。此外，它还允许开发两种新技术来提高采样效率：跨时间步长重新分配计算和在时间步长之间重用不动点解。我们在ImageNet、FFHQ、CelebA HQ和LSUN Church上对最先进的模型进行了广泛的实验，证明了性能和效率的显著提高。与最先进的DiT模型相比，FPDM包含的参数减少了87%，在训练过程中消耗的内存减少了60%，并在采样计算或时间有限的情况下提高了图像生成质量。我们的代码和预训练模型可在https://lukemelas.github.io/fixed-point-diffusion-models. et.al.|[2401.08741](http://arxiv.org/abs/2401.08741)|null|
|**2024-01-16**|**Revealing Vulnerabilities in Stable Diffusion via Targeted Attacks**|文本到图像模型的最新发展，特别是稳定扩散，在各种应用中取得了重大成就。随着这些进步，人们越来越担心恶意实体利用模型的漏洞来生成有针对性的有害图像。然而，现有的模型漏洞方法主要评估提示图像和生成图像之间的一致性，但未能揭示与目标图像生成相关的漏洞。在这项研究中，我们提出了稳定扩散上的目标对抗性攻击问题，并提出了一个生成对抗性提示的框架。具体而言，我们设计了一种基于梯度的嵌入优化方法，以制作可靠的对抗性提示，引导稳定扩散生成特定图像。此外，在获得成功的对抗性提示后，我们揭示了导致模型漏洞的机制。在两个目标攻击任务上的大量实验证明了我们的方法在目标攻击中的有效性。代码可在中获取https://github.com/datar001/Revealing-Vulnerabilities-in-Stable-Diffusion-via-Targeted-Attacks. et.al.|[2401.08725](http://arxiv.org/abs/2401.08725)|null|
|**2024-01-16**|**Connect, Collapse, Corrupt: Learning Cross-Modal Tasks with Uni-Modal Data**|由于成对的多模态数据有限，构建跨模态应用程序具有挑战性。最近的工作表明，利用预先训练的多模态对比表示空间，可以从单模态数据中学习跨模态任务。这是基于这样一种假设，即对比优化使来自不同模态的嵌入可以互换。然而，由于对多模态对比空间的几何结构了解不足，这一假设被低估了，其中存在模态缺口。在我们的研究中，我们对这个空间的几何结构进行了理论解释，并引入了一种三步方法 $C^3$（Connect，Collapse，Corrupt），以弥合模态差距，增强嵌入的互换性。我们的$C^3$ 方法显著改进了单模态数据的跨模态学习，在零样本图像/音频/视频字幕和文本到图像生成方面实现了最先进的结果。 et.al.|[2401.08567](http://arxiv.org/abs/2401.08567)|**[link](https://github.com/yuhui-zh15/c3)**|
|**2024-01-16**|**Instilling Multi-round Thinking to Text-guided Image Generation**|在本文中，我们研究了文本引导的图像生成任务。我们的重点在于在给定用户文本反馈的情况下修改参考图像，使其具有特定的所需属性。尽管最近在这一领域取得了进展，但一个持续的挑战仍然是，单轮优化往往忽略了关键细节，尤其是在鞋子或袖子等细粒度变化领域。这种错位积累严重阻碍了交互过程中的多轮定制。为了解决这一挑战，我们在现有框架中引入了一种新的自监督正则化，即多轮正则化。它建立在观察到修改顺序不会影响最终结果的基础上。顾名思义，多轮正则化鼓励模型在不同的修改顺序之间保持一致性。具体而言，与传统的一轮学习相比，我们提出的方法解决了最初未能捕获细粒度细节导致多轮学习后出现重大差异的问题。定性和定量实验都表明，与文本引导的生成任务相比，该方法实现了高保真度的生成质量，尤其是局部修改。此外，我们通过将我们的方法应用于文本引导的检索数据集，如FahisonIQ，将评估扩展到与文本的语义对齐，在那里它展示了竞争性能。 et.al.|[2401.08472](http://arxiv.org/abs/2401.08472)|null|
|**2024-01-16**|**Key-point Guided Deformable Image Manipulation Using Diffusion Model**|在本文中，我们介绍了一种关键点引导的扩散概率模型（KDM），该模型通过操纵对象的关键点来获得对图像的精确控制。我们提出了一个两阶段生成模型，其中包含一个光流图作为中间输出。通过这样做，可以对图像和稀疏关键点之间的语义关系进行密集的像素理解，从而生成更真实的图像。此外，光流的集成有助于调节序列图像的帧间方差，证明了真实的序列图像生成。KDM通过各种关键点条件图像合成任务进行评估，包括面部图像生成、人体姿态合成和超声心动图视频预测，证明与最先进的模型相比，KDM能够增强图像的一致性和照片逼真度。 et.al.|[2401.08178](http://arxiv.org/abs/2401.08178)|null|
|**2024-01-16**|**E2HQV: High-Quality Video Generation from Event Camera via Theory-Inspired Model-Aided Deep Learning**|受生物启发的事件相机或动态视觉传感器能够在高时间分辨率和高动态范围内异步捕捉每像素的亮度变化（称为事件流）。然而，非结构化的时空事件流使得为人类视觉提供具有丰富语义信息的直观可视化具有挑战性。它需要事件到视频（E2V）解决方案，该解决方案将事件流作为输入，并生成高质量的视频帧以实现直观的可视化。然而，当前的解决方案主要是数据驱动的，而不考虑与事件流和视频帧相关的基础统计的先验知识。它高度依赖于深度神经网络的非线性和泛化能力，因此在场景复杂时难以重建细节纹理。在这项工作中，我们提出了\textbf{E2HQV}，这是一种新的E2V范式，旨在从事件中产生高质量的视频帧。这种方法利用了一个模型辅助的深度学习框架，该框架以受理论启发的E2V模型为基础，该模型是从事件相机的基本成像原理精心推导而来的。为了解决E2HQV循环分量中的状态重置问题，我们还设计了一个时移嵌入模块，以进一步提高视频帧的质量。对真实世界事件摄像机数据集的全面评估验证了我们的方法，其中E2HQV显著优于最先进的方法，例如，在某些评估指标上超过第二好方法40%以上。 et.al.|[2401.08117](http://arxiv.org/abs/2401.08117)|**[link](https://github.com/vincentqqu/e2hqv)**|

<p align=right>(<a href=#updated-on-20240118>back to top</a>)</p>

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

<p align=right>(<a href=#updated-on-20240118>back to top</a>)</p>

[contributors-shield]: https://img.shields.io/github/contributors/Vincentqyw/cv-arxiv-daily.svg?style=for-the-badge
[contributors-url]: https://github.com/Vincentqyw/cv-arxiv-daily/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/Vincentqyw/cv-arxiv-daily.svg?style=for-the-badge
[forks-url]: https://github.com/Vincentqyw/cv-arxiv-daily/network/members
[stars-shield]: https://img.shields.io/github/stars/Vincentqyw/cv-arxiv-daily.svg?style=for-the-badge
[stars-url]: https://github.com/Vincentqyw/cv-arxiv-daily/stargazers
[issues-shield]: https://img.shields.io/github/issues/Vincentqyw/cv-arxiv-daily.svg?style=for-the-badge
[issues-url]: https://github.com/Vincentqyw/cv-arxiv-daily/issues

