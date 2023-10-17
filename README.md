[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]

## Updated on 2023.10.17
> Usage instructions: [here](./docs/README.md#usage)

<details>
  <summary>Table of Contents</summary>
  <ol>
    <li><a href=#3d>3D</a></li>
    <li><a href=#3d-reconstruction>3D Reconstruction</a></li>
    <li><a href=#diffusion>Diffusion</a></li>
    <li><a href=#nerf>NeRF</a></li>
  </ol>
</details>

## 3D

|Publish Date|Title|Abstract|PDF|Code|
|---|---|---|---|---|
|**2023-10-16**|**TOSS:High-quality Text-guided Novel View Synthesis from a Single Image**|在本文中，我们提出了TOSS，它将文本引入到仅从单个RGB图像进行新颖视图合成（NVS）的任务中。虽然Zero-1-3展示了令人印象深刻的零样本开集NVS功能，但它将NVS视为一个纯粹的图像到图像的转换问题。这种方法受到了单视图NVS具有挑战性的欠约束性质的影响：该过程缺乏明确的用户控制手段，并且经常导致令人难以置信的NVS生成。为了解决这一限制，TOSS使用文本作为高级语义信息来约束NVS解决方案空间。TOSS微调在大规模文本图像对上预先训练的文本到图像稳定扩散，并引入专门针对图像和相机姿势调节定制的模块，以及姿势正确性和精细细节保存的专门训练。进行了全面的实验，结果表明，我们提出的TOSS优于Zero-1-to-3，具有更合理、可控和多视角一致的NVS结果。我们通过全面的消融进一步支持这些结果，强调了引入的语义指导和架构设计的有效性和潜力。 et.al.|[2310.10644](http://arxiv.org/abs/2310.10644)|null|
|**2023-10-16**|**GTA: A Geometry-Aware Attention Mechanism for Multi-View Transformers**|由于变换器对输入标记的排列是等变的，因此对标记的位置信息进行编码对于许多任务是必要的。然而，由于现有的位置编码方案最初是为NLP任务设计的，因此它们对视觉任务的适用性是值得怀疑的，视觉任务通常在其数据中表现出不同的结构特性。我们认为，现有的位置编码方案对于3D视觉任务来说是次优的，因为它们不尊重其潜在的3D几何结构。基于这一假设，我们提出了一种几何感知注意力机制，该机制将令牌的几何结构编码为由查询和键值对之间的几何关系确定的相对变换。通过在稀疏宽基线多视图设置中对多个新视图合成（NVS）数据集进行评估，我们表明，我们的注意力（称为几何变换注意力（GTA））提高了最先进的基于变换器的NVS模型的学习效率和性能，而无需任何额外的学习参数和较小的计算开销。 et.al.|[2310.10375](http://arxiv.org/abs/2310.10375)|**[link](https://github.com/autonomousvision/gta)**|
|**2023-10-15**|**CBARF: Cascaded Bundle-Adjusting Neural Radiance Fields from Imperfect Camera Poses**|现有的体积神经渲染技术，如神经辐射场（NeRF），在输入图像的相机姿态不完美时，在合成高质量的新视图方面面临限制。为了解决这个问题，我们提出了一种新的3D重建框架，该框架能够同时优化相机姿势，称为CBARF（级联束调整NeRF）。简而言之，我们的框架以粗略到精细的方式优化相机姿态，然后根据校正后的姿势重建场景。观察到，相机姿态的初始化对束调整（BA）的性能有显著影响。因此，我们以不同的尺度级联多个BA模块，以逐步改善相机姿势。同时，我们制定了邻居替换策略，以进一步优化BA在每个阶段的结果。在这一步中，我们引入了一种新的标准来有效地识别估计不足的相机姿势。然后我们将它们替换为相邻相机的姿势，从而进一步消除相机姿势不准确的影响。一旦相机姿态得到优化，我们就使用密度体素网格在新视图中生成高质量的3D重建场景和图像。实验结果表明，我们的CBARF模型在姿态优化和新视图合成方面都达到了最先进的性能，尤其是在存在大的相机姿态噪声的情况下。 et.al.|[2310.09776](http://arxiv.org/abs/2310.09776)|null|
|**2023-10-12**|**Is Generalized Dynamic Novel View Synthesis from Monocular Videos Possible Today?**|从新颖的视角渲染单目视频中观察到的场景是一个具有挑战性的问题。对于静态场景，社区研究了在每个测试场景上进行优化的特定场景优化技术，以及只在测试场景上运行深网前向传递的通用技术。相反，对于动态场景，存在特定场景的优化技术，但据我们所知，目前还没有从给定的单目视频中合成动态新视图的通用方法。为了回答从单目视频中进行广义动态新视图合成在今天是否可行，我们基于现有技术建立了一个分析框架，并致力于广义方法。我们发现，在没有特定场景外观优化的情况下，伪广义过程是可能的，但需要几何和时间一致的深度估计。尽管没有特定场景的外观优化，但伪广义方法改进了一些特定场景的方法。 et.al.|[2310.08587](http://arxiv.org/abs/2310.08587)|null|
|**2023-10-12**|**Im4D: High-Fidelity and Real-Time Novel View Synthesis for Dynamic Scenes**|本文旨在解决多视图视频动态视图合成的挑战。关键的观察结果是，虽然以前的基于网格的方法提供了一致的渲染，但它们在捕捉复杂动态场景的外观细节方面做不到，在这个领域中，基于多视图图像的渲染方法表现出相反的特性。为了将两个世界中最好的结合起来，我们引入了Im4D，这是一种混合场景表示，由基于网格的几何表示和基于多视图图像的外观表示组成。具体而言，动态几何被编码为由时空特征平面和小型MLP网络组成的4D密度函数，该函数对场景结构进行全局建模，并促进渲染一致性。我们通过原始多视图视频和网络来表示场景外观，该网络学习从图像特征预测3D点的颜色，而不是完全用网络来记忆详细的外观，从而自然地使网络的学习变得更容易。我们的方法在五个动态视图合成数据集上进行了评估，包括DyNeRF、ZJU MoCap、NHR、DNA Rendering和ENeRF Outdoor数据集。结果表明，Im4D在渲染质量方面表现出最先进的性能，并且可以有效地进行训练，同时在单个RTX 3090 GPU上以79.8 FPS的速度实现512x512图像的实时渲染。 et.al.|[2310.08585](http://arxiv.org/abs/2310.08585)|null|
|**2023-10-12**|**SingleInsert: Inserting New Concepts from a Single Image into Text-to-Image Models for Flexible Editing**|文本到图像（T2I）模型的最新进展使得能够通过灵活的文本控制生成高质量的图像。为了利用现成的T2I模型中丰富的视觉先验，一系列方法试图将图像反转为与T2I模型的语义空间对齐的适当嵌入。然而，这些图像到文本（I2T）反转方法通常需要包含相同概念的多个源图像，或者难以解决编辑灵活性和视觉逼真度之间的不平衡问题。在这项工作中，我们指出在学习预期概念时，关键问题在于前景-背景纠缠，并提出了一种简单有效的单图像I2T反演基线，称为SingleInsert。SingleInsert采用两阶段方案。在第一阶段，我们调节学习的嵌入，使其集中在前景区域，而不与无关背景相关联。在第二阶段，我们对T2I模型进行了微调，以获得更好的视觉相似性，并设计了语义损失来防止语言漂移问题。利用所提出的技术，SingleInsert在单概念生成方面表现出色，视觉逼真度高，同时允许灵活编辑。此外，SingleInsert可以在不需要联合训练的情况下进行单图像新视图合成和多概念合成。为了便于评估，我们设计了一个编辑提示列表，并引入了一个名为编辑成功率（ESR）的指标来定量评估编辑灵活性。我们的项目页面是：https://jarrentwu1031.github.io/SingleInsert-web/ et.al.|[2310.08094](http://arxiv.org/abs/2310.08094)|null|
|**2023-10-12**|**Consistent123: Improve Consistency for One Image to 3D Object Synthesis**|大图像扩散模型能够实现具有高质量和优异的零样本能力的新颖视图合成。然而，这种基于图像到图像转换的模型不能保证视图的一致性，这限制了诸如3D重建和图像到3D生成之类的下游任务的性能。为了增强一致性，我们提出了Consistent123，通过结合额外的跨视图注意力层和共享的自注意机制，同时合成新的视图。所提出的注意力机制改善了所有合成视图之间的交互，以及条件视图和新视图之间的一致性。在采样阶段，这种架构支持在以固定长度进行训练的同时同时生成任意数量的视图。我们还引入了一种渐进的无分类器引导策略，以实现合成对象视图的纹理和几何之间的权衡。定性和定量实验表明，Consistent123在视图一致性方面大大优于基线。此外，我们展示了Consistent123在不同下游任务上的显著改进，显示了其在3D生成领域的巨大潜力。项目页面位于consistent-123.github.io。 et.al.|[2310.08092](http://arxiv.org/abs/2310.08092)|null|
|**2023-10-11**|**rpcPRF: Generalizable MPI Neural Radiance Field for Satellite Camera**|卫星图像的新视图合成具有广泛的实际应用。虽然神经辐射场的最新进展主要针对针孔相机，而卫星相机的模型通常需要足够的输入视图。本文提出了一种用于有理多项式相机（RPC）的基于多平面图像（MPI）的平面神经辐射场rpcPRF。与需要一个场景的足够视图的基于坐标的神经辐射场不同，我们的模型适用于单个或少量输入，并且在来自看不见的场景的图像上表现良好。为了实现跨场景的泛化，我们建议使用重投影监督来诱导预测的MPI来学习3D坐标和图像之间的正确几何结构。此外，我们通过引入辐射场的绘制技术，消除了基于深度多视点立体的方法对密集深度监督的严格要求。rpcPRF结合了隐式表示的优势和RPC模型的优势，在学习三维结构的同时捕捉连续的高度空间。给定RGB图像及其相应的RPC，端到端模型学习将新视图与新的RPC合成，并重建场景的海拔高度。当提供多个视图作为输入时，rpcPRF施加由额外视图提供的额外监督。在ZY-3的TLC数据集和WV-3的城市场景的SatMVS3D数据集上，对于单视图和多视图任务，rpcPRF在图像保真度、重建精度和效率方面显著优于最先进的基于nerf的方法。 et.al.|[2310.07179](http://arxiv.org/abs/2310.07179)|null|
|**2023-10-06**|**Improving Neural Radiance Field using Near-Surface Sampling with Point Cloud Generation**|神经辐射场（NeRF）是一种新兴的视图合成方法，它对三维空间中的点进行采样，并估计它们的存在和颜色概率。NeRF的缺点是它需要很长的训练时间，因为它对许多3D点进行采样。此外，如果从遮挡区域或在不太可能存在对象的空间中采样点，则NeRF的渲染质量可能会降低。这些问题可以通过估计3D场景的几何形状来解决。本文提出了一种近表面采样框架来提高NeRF的渲染质量。为此，所提出的方法使用训练集的深度图像来估计3D对象的表面，并且仅在那里执行采样。为了获得新视图的深度信息，本文提出了一种三维点云生成方法和一种简单的点云投影深度细化方法。实验结果表明，与原始的NeRF和最先进的基于深度的NeRF方法相比，所提出的近表面采样NeRF框架可以显著提高渲染质量。此外，使用所提出的近表面采样框架，可以显著加快NeRF模型的训练时间。 et.al.|[2310.04152](http://arxiv.org/abs/2310.04152)|null|
|**2023-10-06**|**ILSH: The Imperial Light-Stage Head Dataset for Human Head View Synthesis**|本文介绍了Imperial Light Stage Head（ILSH）数据集，这是一个新颖的Light Stage捕获的人头数据集，旨在支持人头的视图合成学术挑战。ILSH数据集旨在促进各种方法，如场景特定或通用神经渲染、多视图几何、3D视觉和计算机图形学，以进一步推动照片逼真的人类化身的开发。本文详细介绍了专门用于捕捉高分辨率（4K）人头图像的光台的设置，并描述了在收集高质量数据时应对挑战（预处理、道德问题）的过程。除了数据收集之外，我们还将数据集拆分为训练集、验证集和测试集。我们的目标是为这个新的数据集设计和支持一个公平视图综合挑战任务，以便在使用测试集时，如在使用验证集时，可以保持和预期类似的性能水平。ILSH数据集由52名受试者组成，这些受试者使用24台相机拍摄，所有82个光源都打开，共产生1248张特写头部图像、边界遮罩和相机姿势对。 et.al.|[2310.03952](http://arxiv.org/abs/2310.03952)|null|

<p align=right>(<a href=#updated-on-20231017>back to top</a>)</p>

## 3D Reconstruction

|Publish Date|Title|Abstract|PDF|Code|
|---|---|---|---|---|
|**2023-10-16**|**In-Situ Single Particle Reconstruction Reveals 3D Evolution of PtNi Nanocatalysts During Heating**|定制纳米颗粒的组成和形态对于提高其催化性能具有特别的意义。这种方法的一个挑战是，优化的纳米颗粒初始结构在使用过程中经常发生变化。因此，在原位可视化三维（3D）结构转变是至关重要的，但在实验上往往非常困难。尽管电子断层扫描为3D成像提供了机会，但原位支架倾斜范围的限制以及电子剂量的考虑限制了原位电子断层扫描研究的可能性。在这里，我们提出了一种使用单粒子重建（SPR）的原位3D成像方法，该方法允许在控制电子剂量和不倾斜显微镜台的情况下对纳米颗粒进行3D重建。这种原位SPR方法用于研究高温下PtNi纳米颗粒群体中的结构重组和元素再分配。我们进一步研究了PtNi的原子结构，发现了热诱导的从无序相到有序相的转变。结构和元素分布的变化与氧还原反应中催化活性的丧失有关。这里使用的原位SPR方法可以扩展到广泛的原位研究，不仅使用加热，还使用气体、水性或电化学环境，以揭示3D中操作中的纳米颗粒进化。 et.al.|[2310.10253](http://arxiv.org/abs/2310.10253)|null|
|**2023-10-16**|**Long-term Dependency for 3D Reconstruction of Freehand Ultrasound Without External Tracker**|目的：在没有任何外部跟踪器的情况下重建徒手超声一直是超声辅助手术中的一个长期挑战。我们的目标是定义参数化长期依赖关系的新方法，并评估性能。方法：首先，通过帧序列中的变换位置对长期依赖性进行编码。这是通过将序列模型与多变换预测相结合来实现的。其次，提出了两个依赖因素，解剖图像内容和扫描协议，以促进精确重建。通过减少各自的训练方差，对每个因素进行实验量化。结果：1）与基线性能相比，以每秒20帧（fps）的速度增加的高达400帧的长期依赖性确实改善了重建，累积误差降低了82.4%。发现改进取决于序列长度、转换间隔和扫描协议，出乎意料的是，不取决于使用具有长短期模块的递归网络；2） 训练中解剖或方案差异的减少导致重建准确性较差。有趣的是，与代表性解剖特征相比，代表性方案模式获得了更高的性能。结论：所提出的算法使用超参数调整来有效地利用长期依赖性。所提出的依赖因子对收集不同的训练数据、规范扫描协议和开发高效的网络具有实际意义。意义：所提出的新方法采用了公开的志愿者数据和代码，用于参数化长期依赖性，实验表明这是性能改进的有效来源，可能会导致更好的模型开发和重建应用的实际优化。 et.al.|[2310.10248](http://arxiv.org/abs/2310.10248)|**[link](https://github.com/ucl-candi/freehand)**|
|**2023-10-16**|**Self-supervised Fetal MRI 3D Reconstruction Based on Radiation Diffusion Generation Model**|尽管使用多个堆栈可以处理切片到体积的运动校正和伪影去除问题，但仍存在以下几个问题：1）切片到体积方法通常使用切片作为输入，无法解决不同胎儿MRI堆栈区域中强度分布均匀和互补的问题；2） 没有考虑3D空间的完整性，这对胎儿MRI中全局一致信息的识别和生成产生了不利影响；3） 现实世界中存在严重运动伪影的胎儿MRI无法实现高质量的超分辨率重建。为了解决这些问题，我们提出了一种新的胎儿大脑MRI高质量体积重建方法，称为辐射扩散生成模型（RDGM）。它是一种自监督生成方法，融合了基于坐标生成的神经辐射场（NeRF）和基于超分辨率生成的扩散模型的思想。为了解决不同方向的区域强度异质性，我们使用预先训练的变换器模型进行切片配准，然后提出了一个新的区域一致隐式神经表示（CINR）网络子模块。CINR可以通过组合两个不同坐标映射空间的坐标关联图来生成初始体积。为了增强体积全局一致性和区分性，我们引入了体积扩散超分辨率生成（VDSG）机制。使用扩散生成的思想进行从体积到体积的全局强度判别生成，CINR成为体积到体积扩散模型的偏差强度生成网络。最后，在真实世界的胎儿大脑MRI堆栈上的实验结果证明了我们方法的最先进性能。 et.al.|[2310.10209](http://arxiv.org/abs/2310.10209)|null|
|**2023-10-15**|**Tabletop Transparent Scene Reconstruction via Epipolar-Guided Optical Flow with Monocular Depth Completion Prior**|使用价格合理的RGB-D相机重建透明物体是机器人感知的一个持续挑战，因为RGB域中视图之间的外观不一致，每个视图中的深度读数不准确。我们介绍了一种两阶段流水线，用于重构为移动平台量身定制的透明对象。在第一阶段，利用现成的单目对象分割和深度完成网络来预测透明对象的深度，从而提前提供单视图形状。随后，我们提出了Epipolar引导光流（EOF），在给定从场景不透明部分估计的相机姿态的情况下，将第一阶段的几个单视图形状先验融合到跨视图一致的3D重建。我们的关键创新在于EOF，它将边界敏感采样和极线约束应用到光流中，以在透明物体的多个视图之间准确地建立2D对应关系。定量评估表明，我们的管道在3D重建质量方面显著优于基线方法，为机器人更熟练地感知和与透明物体的交互铺平了道路。 et.al.|[2310.09956](http://arxiv.org/abs/2310.09956)|null|
|**2023-10-15**|**CBARF: Cascaded Bundle-Adjusting Neural Radiance Fields from Imperfect Camera Poses**|现有的体积神经渲染技术，如神经辐射场（NeRF），在输入图像的相机姿态不完美时，在合成高质量的新视图方面面临限制。为了解决这个问题，我们提出了一种新的3D重建框架，该框架能够同时优化相机姿态，称为CBARF（级联束调整NeRF）。简而言之，我们的框架以粗略到精细的方式优化相机姿势，然后根据校正后的姿势重建场景。观察到，相机姿态的初始化对束调整（BA）的性能有显著影响。因此，我们以不同的尺度级联多个BA模块，以逐步改善相机姿势。同时，我们制定了邻居替换策略，以进一步优化BA在每个阶段的结果。在这一步中，我们引入了一种新的标准来有效地识别估计不足的相机姿势。然后我们将它们替换为相邻相机的姿势，从而进一步消除相机姿势不准确的影响。一旦相机姿态得到优化，我们就使用密度体素网格在新视图中生成高质量的3D重建场景和图像。实验结果表明，我们的CBARF模型在姿态优化和新视图合成方面都达到了最先进的性能，尤其是在存在大的相机姿态噪声的情况下。 et.al.|[2310.09776](http://arxiv.org/abs/2310.09776)|null|
|**2023-10-15**|**Efficient and Effective Multi-View Subspace Clustering for Large-scale Data**|最近的多视图子空间聚类利用深度网络取得了令人印象深刻的结果，其中自表达相关性通常由全连接（FC）层建模。然而，它们仍然受到两个限制：i）从同时满足最小充分性和可区分性的多个视图中提取统一表示的探索不足。ii）FC层的参数规模是样本数量的二次方，导致高时间和内存成本，这显著降低了它们在大规模数据集中的可行性。有鉴于此，我们提出了一个新的深度框架，称为高效有效的大规模多视图子空间聚类（E $^2$LMVSC）。具体来说，为了提高统一表示的质量，设计了一种软聚类分配相似性约束，用于明确解耦多视图数据中的一致、互补和多余信息。然后，根据信息瓶颈理论，得到了一个充分而又最小的统一特征表示。此外，E$^2$LMVSC采用最大编码率降低原理来促进统一表示中的簇内聚合和簇间可分性。最后，为了提高效率，通过关系度量网而不是参数化FC层来学习自表达系数。大量实验表明，E$^2$ LMVSC产生了与现有方法相当的结果，并在大规模多视图数据集中实现了最先进的聚类性能。 et.al.|[2310.09718](http://arxiv.org/abs/2310.09718)|null|
|**2023-10-14**|**JM3D & JM3D-LLM: Elevating 3D Representation with Joint Multi-modal Cues**|3D表示学习在计算机视觉、自动驾驶和机器人技术中起着至关重要的作用，其重要性与日俱增。然而，一种直接诉诸于将2D对齐策略转移到3D领域的流行趋势遇到了三个不同的挑战：（1）信息退化：这是由于3D数据与仅单个视图的2D图像和通用文本对齐，忽略了对多视图图像和详细子类别文本的需要。（2） 协同不足：这些策略将3D表示与图像和文本功能单独对齐，阻碍了3D模型的整体优化。（3） 利用不足：学习到的表示中固有的细粒度信息往往没有得到充分利用，这表明细节可能会丢失。为了解决这些问题，我们介绍了JM3D，这是一种集成点云、文本和图像的综合方法。主要贡献包括结构化多模式组织器（SMO），它用多个视图和分层文本丰富视觉语言表示，以及联合多模式对齐（JMA），它将语言理解与视觉表示相结合。我们的高级模型JM3D-LLM通过有效的微调将3D表示与大型语言模型相结合。通过对ModelNet40和ScanObjectNN的评估，确立了JM3D的优越性。JM3D-LLM的卓越性能进一步强调了我们的表示转移方法的有效性。我们的代码和型号可在https://github.com/Mr-Neko/JM3D. et.al.|[2310.09503](http://arxiv.org/abs/2310.09503)|**[link](https://github.com/mr-neko/jm3d)**|
|**2023-10-13**|**PonderV2: Pave the Way for 3D Foundation Model with A Universal Pre-training Paradigm**|与众多的NLP和2D计算机视觉基础模型相比，学习一个稳健且高度通用的3D基础模型带来了更大的挑战。这主要是由于固有的数据可变性和下游任务的多样性。在本文中，我们介绍了一个全面的3D预训练框架，旨在促进高效的3D表示的获取，从而建立一条通往3D基础模型的途径。基于信息丰富的3D特征应该能够编码丰富的几何形状和外观线索，这些线索可以用来渲染逼真的图像，我们提出了一种新的通用范式，通过可微分神经渲染来学习点云表示，作为3D和2D世界之间的桥梁。我们通过将渲染图像与真实图像进行比较，在设计的体积神经渲染器中训练点云编码器。值得注意的是，我们的方法展示了将学习的3D编码器无缝集成到各种下游任务中。这些任务不仅包括3D检测和分割等高级别挑战，还包括3D重建和图像合成等低级别目标，涵盖室内和室外场景。此外，我们还说明了使用所提出的通用方法对2D主干进行预训练的能力，大大超过了传统的预训练方法。PonderV2首次在11个室内和室外基准上实现了最先进的性能。在各种情况下的持续改进表明了所提出方法的有效性。代码和型号将在https://github.com/OpenGVLab/PonderV2. et.al.|[2310.08586](http://arxiv.org/abs/2310.08586)|**[link](https://github.com/OpenGVLab/PonderV2)**|
|**2023-10-12**|**Is ImageNet worth 1 video? Learning strong image encoders from 1 long unlabelled video**|自监督学习释放了将预训练扩展到数十亿张图像的潜力，因为注释是不必要的。但我们是否充分利用了数据？我们能节约多少？在这项工作中，我们试图通过作出两项贡献来回答这个问题。首先，我们调查了第一人称视频，并介绍了一个“徒步旅行”数据集。这些视频是高分辨率的，长达数小时，在一次不间断的拍摄中捕捉到，描绘了大量具有自然场景转换的物体和动作。它们是未标记和未评级的，因此对于自我监督来说是现实的，并且可以与人类的学习相比较。其次，我们介绍了一种新的自监督图像预训练方法，该方法专为从连续视频中学习而设计。现有的方法通常采用基于图像的预训练方法来合并更多的帧。相反，我们提倡一种“跟踪以学会识别”的方法。我们的方法称为DoRA，它使用转换器交叉注意力，以端到端的方式生成注意图，发现和tRAck对象。我们从轨迹中导出多个视图，并将它们用于经典的自监督蒸馏损失。使用我们的新方法，一个徒步旅行视频显著地成为ImageNet在几个图像和视频下游任务中的强大竞争对手。 et.al.|[2310.08584](http://arxiv.org/abs/2310.08584)|null|
|**2023-10-12**|**Consistent123: Improve Consistency for One Image to 3D Object Synthesis**|大图像扩散模型能够实现具有高质量和优异的零样本能力的新颖视图合成。然而，这种基于图像到图像转换的模型不能保证视图的一致性，这限制了诸如3D重建和图像到3D生成之类的下游任务的性能。为了增强一致性，我们提出了Consistent123，通过结合额外的跨视图注意力层和共享的自注意机制，同时合成新的视图。所提出的注意力机制改善了所有合成视图之间的交互，以及条件视图和新视图之间的一致性。在采样阶段，这种架构支持在以固定长度进行训练的同时同时生成任意数量的视图。我们还引入了一种渐进的无分类器引导策略，以实现合成对象视图的纹理和几何之间的权衡。定性和定量实验表明，Consistent123在视图一致性方面大大优于基线。此外，我们展示了Consistent123在不同下游任务上的显著改进，显示了其在3D生成领域的巨大潜力。项目页面位于consistent-123.github.io。 et.al.|[2310.08092](http://arxiv.org/abs/2310.08092)|null|

<p align=right>(<a href=#updated-on-20231017>back to top</a>)</p>

## Diffusion

|Publish Date|Title|Abstract|PDF|Code|
|---|---|---|---|---|
|**2023-10-16**|**A Survey on Video Diffusion Models**|最近的人工智能生成内容（AIGC）浪潮见证了计算机视觉的巨大成功，扩散模型在这一成就中发挥了至关重要的作用。由于其令人印象深刻的生成能力，扩散模型正在逐渐取代基于GANs和自回归变换器的方法，不仅在图像生成和编辑方面，而且在视频相关研究领域都表现出了卓越的性能。然而，现有的调查主要集中在图像生成背景下的扩散模型上，很少有关于其在视频领域应用的最新评论。为了解决这一差距，本文对AIGC时代的视频扩散模型进行了全面的回顾。具体来说，我们首先简要介绍扩散模型的基本原理和演变。随后，我们概述了视频领域扩散模型的研究，将工作分为三个关键领域：视频生成、视频编辑和其他视频理解任务。我们对这三个关键领域的文献进行了彻底的回顾，包括进一步的分类和在该领域的实际贡献。最后，我们讨论了该领域研究面临的挑战，并概述了未来潜在的发展趋势。本次调查中研究的视频扩散模型的综合列表可在https://github.com/ChenHsing/Awesome-Video-Diffusion-Models. et.al.|[2310.10647](http://arxiv.org/abs/2310.10647)|**[link](https://github.com/ChenHsing/Awesome-Video-Diffusion-Models)**|
|**2023-10-16**|**TOSS:High-quality Text-guided Novel View Synthesis from a Single Image**|在本文中，我们提出了TOSS，它将文本引入到仅从单个RGB图像进行新颖视图合成（NVS）的任务中。虽然Zero-1-3展示了令人印象深刻的零样本开集NVS功能，但它将NVS视为一个纯粹的图像到图像的转换问题。这种方法受到了单视图NVS具有挑战性的欠约束性质的影响：该过程缺乏明确的用户控制手段，并且经常导致令人难以置信的NVS生成。为了解决这一限制，TOSS使用文本作为高级语义信息来约束NVS解决方案空间。TOSS微调在大规模文本图像对上预先训练的文本到图像稳定扩散，并引入专门针对图像和相机姿势调节定制的模块，以及姿势正确性和精细细节保存的专门训练。进行了全面的实验，结果表明，我们提出的TOSS优于Zero-1-to-3，具有更合理、可控和多视角一致的NVS结果。我们通过全面的消融进一步支持这些结果，强调了引入的语义指导和架构设计的有效性和潜力。 et.al.|[2310.10644](http://arxiv.org/abs/2310.10644)|null|
|**2023-10-16**|**LLM Blueprint: Enabling Text-to-Image Generation with Complex and Detailed Prompts**|基于扩散的生成模型显著提高了文本到图像的生成，但在处理描述具有多个对象的复杂场景的冗长而复杂的文本提示时遇到了挑战。虽然这些模型在从简短的单一对象描述中生成图像方面表现出色，但它们往往难以在更长、更精细的文本输入中忠实地捕捉到所有细微的细节。作为回应，我们提出了一种利用大型语言模型（LLM）从文本提示中提取关键组件的新方法，包括前景对象的边界框坐标、单个对象的详细文本描述和简洁的背景上下文。这些组件构成了我们的布局到图像生成模型的基础，该模型分两个阶段运行。初始的“全局场景生成”使用对象布局和背景上下文来创建初始场景，但在忠实地表示提示中指定的对象特性方面往往做不到。为了解决这一限制，我们引入了一种迭代优化方案，该方案迭代评估和优化框级内容，使其与文本描述保持一致，并根据需要重新组合对象以确保一致性。我们对具有多个对象的复杂提示的评估表明，与基线扩散模型相比，召回率有了显著提高。一项用户研究进一步验证了这一点，强调了我们的方法在从复杂的文本输入中生成连贯和详细场景方面的有效性。 et.al.|[2310.10640](http://arxiv.org/abs/2310.10640)|**[link](https://github.com/hananshafi/llmblueprint)**|
|**2023-10-16**|**Zero-Shot Robotic Manipulation with Pretrained Image-Editing Diffusion Models**|如果多面手机器人要在真正的非结构化环境中工作，他们需要能够识别和推理新的对象和场景。这样的物体和场景可能不存在于机器人自己的训练数据中。我们提出了SuSIE，这是一种利用图像编辑扩散模型作为高级规划器的方法，通过提出低级控制器可以实现的中间子目标。具体来说，我们对视频数据（包括人类视频和机器人的推出）进行了微调，使其在给定机器人当前观察和语言命令的情况下输出假设的未来“子目标”观察。我们还使用机器人数据来训练一个低级目标条件策略，以充当上述低级控制器。我们发现，高级子目标预测可以利用互联网规模的预训练和视觉理解来指导低级目标条件策略，实现比传统语言条件策略更好的泛化和精度。我们在CALVIN基准上取得了最先进的结果，并在现实世界的操作任务上表现出了强大的泛化能力，击败了能够访问特权信息或利用数量级以上计算和训练数据的强大基线。项目网站位于http://rail-berkeley.github.io/susie。 et.al.|[2310.10639](http://arxiv.org/abs/2310.10639)|null|
|**2023-10-16**|**DynVideo-E: Harnessing Dynamic NeRF for Large-Scale Motion- and View-Change Human-Centric Video Editing**|尽管在基于扩散的视频编辑方面取得了显著的研究进展，但由于长距离一致性和逐帧编辑之间的矛盾，现有的方法仅限于短视频。最近的方法试图通过引入视频-2D表示来解决这一挑战，从而将视频编辑降级为图像编辑。然而，他们在处理大规模的运动和视图变化视频时遇到了很大的困难，尤其是在以人为中心的视频中。这促使我们引入动态神经辐射场（NeRF）作为以人为中心的视频表示，以缓解3D空间编辑任务中的视频编辑问题。这样，可以在3D空间中执行编辑，并通过变形场传播到整个视频。为了提供更精细和直接的可控编辑，我们提出了基于图像的三维空间编辑管道，并提供了一组有效的设计。其中包括来自2D个性化扩散先验和3D扩散先验的多视图多姿态分数蒸馏采样（SDS）、参考图像上的重建损失、文本引导的局部超分辨率以及3D背景空间的风格转移。大量实验表明，我们的方法被称为DynVideo-E，在两个具有挑战性的数据集上，在人类偏好方面显著优于SOTA方法，相差50%~95%。项目页面中提供了令人信服的视频比较https://showlab.github.io/DynVideo-E/.我们的代码和数据将发布给社区。 et.al.|[2310.10624](http://arxiv.org/abs/2310.10624)|null|
|**2023-10-16**|**ForceGen: End-to-end de novo protein generation based on nonlinear mechanical unfolding responses using a protein language diffusion model**|经过进化，自然界已经呈现出一系列引人注目的蛋白质材料，包括弹性蛋白、丝、角蛋白和胶原，它们具有优异的机械性能，在机械生物学中发挥着至关重要的作用。然而，超越自然设计，发现符合特定机械性能的蛋白质仍然具有挑战性。在这里，我们报告了一个生成模型，该模型预测蛋白质设计以满足复杂的非线性机械性能设计目标。我们的模型利用了来自预先训练的蛋白质语言模型的蛋白质序列的深层知识，并绘制了机械展开反应图，以创建新的蛋白质。通过直接验证的全原子分子模拟，我们证明了设计的蛋白质是新颖的，并实现了目标机械性能，包括展开能和机械强度，以及详细的展开力分离曲线。我们的模型提供了探索不受生物合成约束的巨大机械生物学蛋白质序列空间的快速途径，利用机械特征作为目标，能够发现具有优异机械性能的蛋白质材料。 et.al.|[2310.10605](http://arxiv.org/abs/2310.10605)|null|
|**2023-10-16**|**Generation or Replication: Auscultating Audio Latent Diffusion Models**|音频潜在扩散模型的引入能够根据文本描述的需求生成逼真的声音片段，这有可能彻底改变我们使用音频的方式。在这项工作中，我们初步尝试通过研究音频潜在扩散模型的音频输出与训练数据的比较来理解其内部工作，类似于医生如何通过倾听患者器官的声音来听诊。使用在AudioCaps数据集上训练的文本到音频潜在扩散模型，我们系统地分析了记忆行为作为训练集大小的函数。我们还评估了不同的检索指标，以获得训练数据记忆的证据，发现mel谱图之间的相似性在检测匹配方面比学习的嵌入向量更稳健。在分析音频潜在扩散模型中的记忆过程中，我们还发现AudioCaps数据库中存在大量重复的音频片段。 et.al.|[2310.10604](http://arxiv.org/abs/2310.10604)|null|
|**2023-10-16**|**Corrections to diffusion in interacting quantum systems**|经典和量子相互作用系统中的输运和平衡方法是一个具有挑战性的理论和实验兴趣的问题。表征平衡的一个有用的组织原理是耗散普适性类，最普遍的是扩散。本文利用扩散的有效场论（EFT），系统地得到了扩散的普遍幂律修正。然后，我们使用经典和量子系统的大规模模拟来探索它们的有效性。特别地，我们发现了在具有和不具有粒子-空穴对称性的系统中，在存在单个 $U（1）$或$SU（2）$电荷的情况下，对动力学结构因子$langle n（x，t）n\rangle$ 的校正的通用标度函数，并提出了将计算推广到多个电荷的框架。经典模拟显示出与分段修正的EFT预测显著一致，将热化系统有效理论的精度测试推向了前所未有的水平。转到量子系统，我们在具有守恒磁化的酉和有噪声的1d Floquet系统中进行大规模张量网络模拟。我们发现了与EFT的定性一致性，在有噪声系统的情况下，EFT变成了定量的。此外，我们展示了EFT校正的知识如何允许拟合方法，该方法可以改进模拟和实验可获得的中间时间的传输参数估计。最后，我们探索了量子系统中的非线性响应，发现EFT为其行为提供了准确的预测。我们的结果为更好地理解热化系统中存在的非线性现象提供了基础。 et.al.|[2310.10564](http://arxiv.org/abs/2310.10564)|null|
|**2023-10-16**|**Stability and bifurcation analysis of a two-patch model with Allee effect and dispersal**|在当前的手稿中，提出了第一个具有Allee效应和非线性扩散的两块模型。我们在这里研究ODE情况和PDE情况。在ODE模型中，讨论了平衡点的稳定性和鞍节点分岔的存在性。通过数值模拟，给出了该模型的相图和分岔曲线。此外，还给出了相应的线性扩散情况。我们发现，当Allee效应较大时，高强度的线性扩散不利于物种的持久性。我们进一步表明，当Allee效应较大时，非线性扩散比线性扩散更有利于种群的生存。此外，PDE模型的结果将我们的发现从离散补丁扩展到连续补丁。 et.al.|[2310.10558](http://arxiv.org/abs/2310.10558)|null|
|**2023-10-16**|**ViPE: Visualise Pretty-much Everything**|形象表达和非文字表达在人类交往中有着深刻的融合。视觉化这样的表达可以让我们传达我们的创造性想法，并唤起细致入微的情感。另一方面，最近的文本到图像模型，如稳定扩散，很难描绘非文字表达。最近的工作主要通过小规模编译人工注释的数据集来处理这个问题，这不仅需要专业知识，而且效率很低。为了解决这个问题，我们引入了ViPE：可视化几乎所有的东西。ViPE提供了一系列轻量级和健壮的语言模型，这些模型是在一组大规模的歌词上训练的，这些歌词带有嘈杂的视觉描述，代表了它们的隐含含义。合成视觉描述由GPT3.5生成，既不依赖于人类注释也不依赖于图像。ViPE有效地将任意文本片段表达为可视化描述，从而实现有意义的高质量图像生成。我们提供了令人信服的证据，证明ViPE在合成视觉细节方面比GPT3.5更稳健。ViPE还展示了与人类专家相当的对比喻表达的理解，为音乐视频和字幕生成等许多下游应用程序提供了强大的开源主干。 et.al.|[2310.10543](http://arxiv.org/abs/2310.10543)|**[link](https://github.com/hazel1994/vipe)**|

<p align=right>(<a href=#updated-on-20231017>back to top</a>)</p>

## NeRF

|Publish Date|Title|Abstract|PDF|Code|
|---|---|---|---|---|
|**2023-10-12**|**S4C: Self-Supervised Semantic Scene Completion with Neural Fields**|三维语义场景理解是计算机视觉中的一个基本挑战。它使移动代理能够自主规划和导航任意环境。SSC将这一挑战形式化为从场景的稀疏观测中联合估计密集的几何结构和语义信息。当前的SSC方法通常基于聚合的激光雷达扫描在3D地面实况上进行训练。这一过程依赖于特殊的传感器和手工注释，这些传感器和注释成本高昂且规模不大。为了克服这个问题，我们的工作提出了第一种称为S4C的SSC自监督方法，该方法不依赖于3D地面实况数据。我们提出的方法可以从单个图像重建场景，并且只依赖于训练期间从现成的图像分割网络生成的视频和伪分割地面实况。与使用离散体素网格的现有方法不同，我们将场景表示为隐式语义场。该公式允许查询相机截锥体内的任何点的占用率和语义类。我们的架构是通过基于渲染的自监督损失进行训练的。尽管如此，我们的方法实现了接近于完全监督的最先进方法的性能。此外，我们的方法表现出强大的泛化能力，可以为遥远的视点合成准确的分割图。 et.al.|[2310.07522](http://arxiv.org/abs/2310.07522)|null|
|**2023-10-07**|**HI-SLAM: Monocular Real-time Dense Mapping with Hybrid Implicit Fields**|在这封信中，我们提出了一个基于神经场的实时单目映射框架，用于精确和密集的同时定位和映射（SLAM）。最近的神经映射框架显示出有希望的结果，但依赖于RGB-D或姿势输入，或者无法实时运行。为了解决这些局限性，我们的方法将密集SLAM与神经隐式场相结合。具体来说，我们的密集SLAM方法运行并行跟踪和全局优化，而基于神经场的映射是基于最新的SLAM估计逐步构建的。为了有效地构造神经场，我们采用了多分辨率网格编码和符号距离函数（SDF）表示。这使我们能够始终保持地图的最新状态，并通过循环关闭立即适应全球更新。为了全局一致性，我们提出了一种有效的基于Sim（3）的姿态图束调整（PGBA）方法来运行在线闭环并减轻姿态和尺度漂移。为了进一步提高深度精度，我们结合了学习的单目深度先验。我们提出了一种新的深度和尺度联合调整（JDSA）模块来解决深度先验中固有的尺度模糊性。对合成和真实世界数据集的广泛评估验证了我们的方法在准确性和地图完整性方面优于现有方法，同时保持了实时性能。 et.al.|[2310.04787](http://arxiv.org/abs/2310.04787)|null|
|**2023-10-05**|**Variational Barycentric Coordinates**|我们提出了一种变分技术来优化广义重心坐标，与现有模型相比，该技术提供了额外的控制。先前的工作使用网格或闭式公式表示重心坐标，在实践中限制了目标函数的选择。相反，我们使用神经场直接参数化连续函数，该函数将多面体内部的任何坐标映射到其重心坐标。这个公式是通过我们对重心坐标的理论表征实现的，这使我们能够构建将有效坐标的整个函数类参数化的神经场。我们使用各种目标函数展示了我们模型的灵活性，包括多重光滑性和变形感知能量；作为补充，我们还提出了数学上合理的方法来测量和最小化目标，如不连续神经场的总变化。我们提供了一个实用的加速策略，对我们的算法进行了彻底的验证，并展示了几个应用。 et.al.|[2310.03861](http://arxiv.org/abs/2310.03861)|null|
|**2023-10-05**|**High-Degrees-of-Freedom Dynamic Neural Fields for Robot Self-Modeling and Motion Planning**|机器人自模型是机器人物理形态的任务不可知表示，在没有经典几何运动学模型的情况下，可用于运动规划任务。特别是，当后者难以设计或机器人的运动学发生意外变化时，人类自由的自我建模是真正自主智能体的必要特征。在这项工作中，我们利用神经场使机器人能够将其运动学自建模为仅从带有相机姿势和配置的2D图像中学习的神经隐式查询模型。这使得比依赖于深度图像或几何知识的现有方法具有更大的适用性。为此，除了课程数据采样策略外，我们还提出了一种新的基于编码器的神经密度场架构，用于高自由度（DOF）条件下的动态对象中心场景。在7自由度机器人测试装置中，学习的自模型实现了机器人工作空间尺寸2%的倒角-L2距离。作为一个示例性的下游应用程序，我们展示了该模型在运动规划任务中的能力。 et.al.|[2310.03624](http://arxiv.org/abs/2310.03624)|null|
|**2023-10-02**|**Neural Processing of Tri-Plane Hybrid Neural Fields**|在用于存储和通信3D数据的神经场的吸引人的特性的驱动下，直接处理它们以解决分类和零件分割等任务的问题已经出现，并在最近的工作中进行了研究。早期的方法使用由在整个数据集上训练的共享网络参数化的神经场，实现了良好的任务性能，但牺牲了重建质量。为了改进后者，后来的方法侧重于参数化为大型多层感知器（MLP）的单个神经场，然而，由于权重空间的高维性、固有的权重空间对称性和对随机初始化的敏感性，这些神经元场的处理具有挑战性。因此，结果明显不如通过处理显式表示（例如点云或网格）所获得的结果。与此同时，混合表示，特别是基于三平面的混合表示，已经成为实现神经场的一种更有效的替代方案，但其直接处理尚未得到研究。在本文中，我们证明了三平面离散数据结构编码了丰富的信息，标准的深度学习机器可以有效地处理这些信息。我们定义了一个广泛的基准，涵盖了一组不同的字段，如占用率、有符号/无符号距离，以及首次定义的辐射字段。在处理具有相同重建质量的字段时，我们实现的任务性能远远优于处理大型MLP的框架，并且首次几乎与处理显式表示的架构不相上下。 et.al.|[2310.01140](http://arxiv.org/abs/2310.01140)|null|
|**2023-09-27**|**Neural Acoustic Context Field: Rendering Realistic Room Impulse Response With Neural Fields**|房间脉冲响应（RIR）测量声音在环境中的传播，对于合成给定环境下的高保真音频至关重要。一些先前的工作已经提出将RIR表示为声音发射器和接收器位置的神经场函数。然而，这些方法没有充分考虑音频场景的声学特性，导致性能不令人满意。这封信提出了一种新的神经声学上下文场方法，称为NACF，通过利用多个声学上下文（如几何结构、材料特性和空间信息）来参数化音频场景。在RIR的独特性质，即时间不光滑性和单调能量衰减的驱动下，我们设计了一个时间相关模块和多尺度能量衰减准则。实验结果表明，NACF的性能显著优于现有的基于字段的方法。请访问我们的项目页面了解更多定性结果。 et.al.|[2309.15977](http://arxiv.org/abs/2309.15977)|null|
|**2023-09-27**|**SHACIRA: Scalable HAsh-grid Compression for Implicit Neural Representations**|隐式神经表示（INR）或神经场已成为编码多媒体信号（如图像和辐射场）同时保持高质量的流行框架。最近，Instant NGP提出的可学习特征网格通过用特征向量的多分辨率查找表和更小的神经网络取代大型神经网络，在训练和INR采样方面实现了显著的加速。然而，这些功能网格是以大量内存消耗为代价的，这可能是存储和流应用程序的瓶颈。在这项工作中，我们提出了SHACIRA，这是一个简单而有效的任务无关框架，用于压缩这种特征网格，而不需要额外的事后修剪/量化阶段。我们用量化的潜在权重对特征网格进行重新参数化，并在潜在空间中应用熵正则化，以在各个领域实现高水平的压缩。在由图像、视频和辐射场组成的不同数据集上的定量和定性结果表明，我们的方法优于现有的INR方法，而不需要任何大型数据集或特定领域的启发式方法。我们的项目页面可在http://shacira.github.io。 et.al.|[2309.15848](http://arxiv.org/abs/2309.15848)|null|
|**2023-09-27**|**NeuRBF: A Neural Fields Representation with Adaptive Radial Basis Functions**|我们提出了一种新型的神经场，它使用一般的径向基来表示信号。现有技术的神经领域通常依赖于用于存储局部神经特征的基于网格的表示和用于在连续查询点处插值特征的N维线性核。它们的神经特征的空间位置固定在网格节点上，不能很好地适应目标信号。相反，我们的方法建立在具有灵活内核位置和形状的通用径向基上，这些径向基具有更高的空间自适应性，可以更紧密地拟合目标信号。为了进一步提高径向基函数的信道容量，我们建议将它们与多频率正弦函数组合。该技术将径向基扩展到不同频带的多个傅立叶径向基，而不需要额外的参数，便于细节的表示。此外，通过将自适应径向基与基于网格的径向基相结合，我们的混合组合继承了自适应性和插值平滑性。我们精心设计了加权方案，使径向基有效地适应不同类型的信号。我们在2D图像和3D符号距离场表示上的实验证明了我们的方法比现有技术更高的精度和紧凑性。当应用于神经辐射场重建时，我们的方法实现了最先进的渲染质量，模型大小小，训练速度相当。 et.al.|[2309.15426](http://arxiv.org/abs/2309.15426)|**[link](https://github.com/oppo-us-research/NeuRBF)**|
|**2023-09-29**|**3D Reconstruction with Generalizable Neural Fields using Scene Priors**|由于神经领域的最新进展，高保真3D场景重建得到了实质性的推进。然而，大多数现有的方法为每个单独的场景从头开始训练单独的网络。这是不可扩展的，效率低下，并且在视图有限的情况下无法产生良好的结果。虽然基于学习的多视图立体方法在一定程度上缓解了这一问题，但它们的多视图设置使其扩展和广泛应用的灵活性降低。相反，我们引入了结合场景先验（NFP）的训练可推广神经场。NFP网络将任何单视图RGB-D图像映射为带符号的距离和辐射值。在没有融合模块的情况下，可以通过合并体积空间中的各个帧来重建完整的场景，这提供了更好的灵活性。场景先验可以在大规模数据集上进行训练，从而能够快速适应具有较少视图的新场景的重建。NFP不仅展示了SOTA场景重建的性能和效率，而且还支持单图像新视图合成，这在神经领域还没有得到充分的探索。更多定性结果可在以下网站获得：https://oasisyang.github.io/neural-prior et.al.|[2309.15164](http://arxiv.org/abs/2309.15164)|null|
|**2023-09-22**|**NOC: High-Quality Neural Object Cloning with 3D Lifting of Segment Anything**|随着神经领域的发展，从多视图输入重建目标物体的3D模型最近越来越受到社会的关注。现有的方法通常学习整个场景的神经场，而如何在飞行中重建用户指示的特定对象仍在探索之中。考虑到分段任意模型（SAM）在分割任何2D图像方面都显示出了有效性，本文提出了一种新的高质量3D对象重建方法——神经对象克隆（NOC），它从两个方面利用了神经场和SAM的优点。首先，为了将目标对象从场景中分离出来，我们提出了一种新的策略，将SAM的多视图2D分割掩模提升到一个统一的3D变化场中。然后，3D变化场被投影到2D空间中，并生成SAM的新提示。这个过程是迭代的，直到收敛，以将目标对象从场景中分离出来。然后，除了2D掩模之外，我们进一步将SAM编码器的2D特征提升到3D SAM场中，以提高目标对象的重建质量。NOC将SAM的2D掩模和特征提升到3D神经场中，用于高质量的目标对象重建。我们在几个基准数据集上进行了详细的实验，以证明我们的方法的优势。代码将被发布。 et.al.|[2309.12790](http://arxiv.org/abs/2309.12790)|null|

<p align=right>(<a href=#updated-on-20231017>back to top</a>)</p>

[contributors-shield]: https://img.shields.io/github/contributors/Vincentqyw/cv-arxiv-daily.svg?style=for-the-badge
[contributors-url]: https://github.com/Vincentqyw/cv-arxiv-daily/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/Vincentqyw/cv-arxiv-daily.svg?style=for-the-badge
[forks-url]: https://github.com/Vincentqyw/cv-arxiv-daily/network/members
[stars-shield]: https://img.shields.io/github/stars/Vincentqyw/cv-arxiv-daily.svg?style=for-the-badge
[stars-url]: https://github.com/Vincentqyw/cv-arxiv-daily/stargazers
[issues-shield]: https://img.shields.io/github/issues/Vincentqyw/cv-arxiv-daily.svg?style=for-the-badge
[issues-url]: https://github.com/Vincentqyw/cv-arxiv-daily/issues

