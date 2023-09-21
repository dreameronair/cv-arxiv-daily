[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]

## Updated on 2023.09.21
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
|**2023-09-20**|**Controllable Dynamic Appearance for Neural 3D Portraits**|神经辐射场（NeRF）的最新进展使得通过控制头部姿势、面部表情和观看方向来重建和恢复动态人像场景成为可能。然而，训练这样的模型假设变形区域的光度一致性，例如，随着头部姿势和面部表情的变化，面部变形时必须均匀照明。即使在工作室环境中，视频各帧之间的这种光度一致性也很难保持，因此，创建的可重影神经肖像在重影过程中容易出现伪影。在这项工作中，我们提出了CoDyNeRF，这是一种能够在真实世界的捕捉条件下创建完全可控的3D肖像的系统。CoDyNeRF通过规范空间中的动态外观模型来学习近似照明相关效果，该模型以预测的表面法线、面部表情和头部姿势变形为条件。表面法线预测是使用3DMM法线来指导的，3DMM法线充当人类头部法线的粗略先验，其中由于头部姿势和面部表情变化引起的刚性和非刚性变形，很难直接预测法线。仅使用智能手机拍摄的受试者短视频进行训练，我们就展示了我们的方法在具有明确的头部姿势和表情控制以及逼真照明效果的人像场景的自由视图合成方面的有效性。项目页面可在此处找到：http://shahrukhathar.github.io/2023/08/22/CoDyNeRF.html et.al.|[2309.11009](http://arxiv.org/abs/2309.11009)|null|
|**2023-09-19**|**ReShader: View-Dependent Highlights for Single Image View-Synthesis**|近年来，由于3D场景表示和图像修复技术的快速发展，从单个图像进行的新颖视图合成已经取得了重大进展。虽然目前的方法能够合成几何一致的新视图，但它们往往不能正确处理视图相关的效果。具体来说，他们合成图像中的高光通常看起来粘在表面上，这使得新颖的视图不切实际。为了解决这个主要问题，我们进行了一项关键观察，即合成新视图的过程需要改变基于新相机的像素的阴影，并将它们移动到适当的位置。因此，我们建议将视图合成过程拆分为两个独立的任务，即像素重新加载和重新定位。在重影过程中，我们以单个图像为输入，并基于新型相机调整其明暗度。然后将该重新加载的图像用作现有视图合成方法的输入，以重新定位像素并产生最终的新颖视图图像。我们建议使用神经网络来执行重新加载，并生成一大组合成输入重新加载对来训练我们的网络。我们证明，我们的方法在各种现实世界场景中产生了具有逼真运动亮点的看似新颖的视图图像。 et.al.|[2309.10689](http://arxiv.org/abs/2309.10689)|null|
|**2023-09-19**|**Locally Stylized Neural Radiance Fields**|近年来，人们对将风格化应用于参考风格图像的3D场景，特别是应用于神经辐射场（NeRF）越来越感兴趣。虽然直接在NeRF上执行风格化可以保证在任意新颖视图上的外观一致性，但引导图案从风格图像转移到NeRF场景的不同部分是一个具有挑战性的问题。在这项工作中，我们提出了一个基于局部风格转移的NeRF风格化框架。特别是，我们使用哈希网格编码来学习外观和几何组件的嵌入，并表明哈希表定义的映射允许我们在一定程度上控制风格化。然后通过优化外观分支同时保持几何体分支固定来实现样式化。为了支持局部风格转移，我们提出了一种新的损失函数，该函数利用分割网络和二分匹配来建立风格图像和从体绘制中获得的内容图像之间的区域对应关系。我们的实验表明，我们的方法通过新的视图合成产生了合理的风格化结果，同时通过操纵和定制区域对应关系具有灵活的可控性。 et.al.|[2309.10684](http://arxiv.org/abs/2309.10684)|null|
|**2023-09-19**|**Anti-Aliased Neural Implicit Surfaces with Encoding Level of Detail**|我们提出了LoD-NeuS，这是一种用于高频几何细节恢复和抗锯齿新视图渲染的有效神经表示。从具有细节水平（LoD）的基于体素的表示中汲取灵感，我们引入了一种基于多尺度三平面的场景表示，该表示能够捕捉符号距离函数（SDF）的LoD和空间辐射。我们的表示聚合了来自圆锥台内沿射线的多重卷积特征的空间特征，并通过可微分渲染优化了LoD特征体积。此外，我们提出了一种误差引导采样策略，以在优化过程中引导SDF的增长。定性和定量评估都表明，与最先进的方法相比，我们的方法实现了卓越的表面重建和真实感视图合成。 et.al.|[2309.10336](http://arxiv.org/abs/2309.10336)|null|
|**2023-09-16**|**ExBluRF: Efficient Radiance Fields for Extreme Motion Blurred Images**|我们提出了ExBluRF，这是一种基于有效辐射场优化的极端运动模糊图像的新视图合成方法。我们的方法由两个主要组成部分组成：基于6自由度相机轨迹的运动模糊公式和基于体素的辐射场。从极其模糊的图像中，我们通过联合估计生成模糊图像的相机轨迹来优化清晰的辐射场。在训练中，沿着相机轨迹的多条光线被累积以重建单个模糊的颜色，这相当于物理运动模糊操作。我们最小化了模糊图像空间上的照片一致性损失，并获得了具有相机轨迹的清晰辐射场，这些轨迹解释了所有图像的模糊。模糊图像空间上的联合优化需要与模糊大小成比例地痛苦地增加计算和资源。我们的方法通过将基于MLP的框架替换为低维6自由度相机姿态和基于体素的辐射场来解决这个问题。与现有作品相比，我们的方法从具有挑战性的运动模糊视图中恢复了更清晰的3D场景，训练时间和GPU内存消耗减少了10倍。 et.al.|[2309.08957](http://arxiv.org/abs/2309.08957)|null|
|**2023-09-16**|**DynaMoN: Motion-Aware Fast And Robust Camera Localization for Dynamic NeRF**|利用神经辐射场（NeRF）进行动态重建需要精确的相机姿态。这些通常很难用现有的运动结构（SfM）管道来检索，因为相机和场景内容都可能发生变化。我们提出了DynaMoN，它利用同步定位和映射（SLAM）与运动掩蔽相结合来处理动态场景内容。我们基于SLAM的稳健跟踪模块显著加快了动态NeRF的训练过程，同时提高了合成视图的质量。对TUM RGB-D、BONN RGB-D Dynamic和DyCheck的iPhone数据集这三个真实世界的数据集进行了广泛的实验验证，显示了DynaMoN在相机姿态估计和新颖视图合成方面的优势。 et.al.|[2309.08927](http://arxiv.org/abs/2309.08927)|null|
|**2023-09-14**|**Viewpoint Textual Inversion: Unleashing Novel View Synthesis with Pretrained 2D Diffusion Models**|文本到图像的扩散模型理解物体之间的空间关系，但它们是否仅从2D监督中代表了世界的真实3D结构？我们证明，是的，3D知识被编码在2D图像扩散模型中，如稳定扩散，我们证明这种结构可以用于3D视觉任务。我们的方法，视点神经纹理反演（ViewNeTI），控制从冻结扩散模型生成的图像中对象的3D视点。我们训练一个小型神经映射器来获取相机视点参数并预测文本编码器延迟；潜伏时间然后调节扩散生成过程以产生具有期望的相机视点的图像。ViewNeTI自然地解决了新颖视图合成（NVS）问题。通过利用冻结扩散模型作为先验，我们可以用很少的输入视图来解决NVS；我们甚至可以做单一视角的小说视角合成。与先前的方法相比，我们的单视图NVS预测具有良好的语义细节和真实感。我们的方法非常适合对稀疏三维视觉问题中固有的不确定性进行建模，因为它可以有效地生成不同的样本。我们的视图控制机制是通用的，甚至可以更改用户定义提示生成的图像中的相机视图。 et.al.|[2309.07986](http://arxiv.org/abs/2309.07986)|null|
|**2023-09-14**|**CoRF : Colorizing Radiance Fields using Knowledge Distillation**|基于神经辐射场（NeRF）的方法能够实现多视图图像的高质量新视图合成。本文提出了一种从输入的灰度多视图图像中合成彩色新视图的方法。当我们在生成的灰度级新视图上应用基于图像或视频的着色方法时，我们会观察到由于视图之间的不一致而产生的伪影。在彩色灰度图像序列上训练辐射场网络也不能解决3D一致性问题。我们提出了一种基于蒸馏的方法，将颜色知识从在自然图像上训练的着色网络转移到辐射场网络。具体来说，我们的方法使用辐射场网络作为3D表示，并从现有的2D着色方法中转移知识。实验结果表明，与基线相比，该方法在保持跨视图一致性的同时，为室内和室外场景生成了更好的彩色新视图。此外，我们展示了我们的方法在应用中的有效性，如从1.）红外（IR）多视图图像和2.）旧灰度多视图图像序列训练的辐射场网络的彩色化。 et.al.|[2309.07668](http://arxiv.org/abs/2309.07668)|null|
|**2023-09-13**|**Dynamic NeRFs for Soccer Scenes**|新颖视角合成这个长期存在的问题有很多应用，尤其是在体育广播中。特别是足球动作的逼真新颖视角合成，引起了广播业的极大兴趣。然而，只有少数几个工业解决方案被提出，甚至很少能达到合成回放的近广播质量。除了在操场周围设置多个静态摄像头外，最好的专有系统几乎没有透露任何关于其内部工作的信息。由于缺乏公共数据集，利用多个静态相机执行这样的任务确实是一个文献中很少解决的挑战：用小而快速的元素重建大规模的、主要是静态的环境。最近，神经辐射场的出现在许多新颖的视图合成应用中取得了惊人的进展，利用深度学习原理在最具挑战性的环境中产生逼真的结果。在这项工作中，我们研究了基于动态NeRF的任务解决方案的可行性，即旨在重建一般动态内容的神经模型。我们构建了合成足球环境，并使用它们进行了多项实验，确定了有助于用动态NeRF重建足球场景的关键组件。我们表明，尽管这种方法不能完全满足目标应用程序的质量要求，但它为实现成本效益高的自动解决方案提供了有希望的途径。我们还公开了我们的工作数据集和代码，目的是鼓励研究界进一步致力于动态足球场景的新颖视图合成任务。有关代码、数据和视频结果，请参阅https://soccernerfs.isach.be. et.al.|[2309.06802](http://arxiv.org/abs/2309.06802)|null|
|**2023-09-13**|**SAMPLING: Scene-adaptive Hierarchical Multiplane Images Representation for Novel View Synthesis from a Single Image**|最近的新颖视图合成方法对于相对较小的场景（例如，室内环境和具有少数对象的场景）获得了有希望的结果，但对于具有单个图像作为输入的无边界室外场景往往失败。在本文中，我们介绍了SAMPLING，这是一种基于改进的多平面图像（MPI）的场景自适应分层多平面图像表示，用于从单个图像合成新视图。观察到无边界户外场景的深度分布变化很大，我们为MPI采用了自适应仓策略，根据每个场景图像排列平面。为了表示复杂的几何结构和多尺度细节，我们进一步引入了一个层次细化分支，它可以产生高质量的合成新视图。我们的方法在KITTI数据集上使用单个图像合成大规模无界户外场景时表现出了相当大的性能提升，并很好地推广到了看不见的Tanks和Temples数据集。代码和模型将很快提供。 et.al.|[2309.06323](http://arxiv.org/abs/2309.06323)|null|

<p align=right>(<a href=#updated-on-20230921>back to top</a>)</p>

## 3D Reconstruction

|Publish Date|Title|Abstract|PDF|Code|
|---|---|---|---|---|
|**2023-09-20**|**Language-driven Object Fusion into Neural Radiance Fields with Pose-Conditioned Dataset Updates**|神经辐射场是一种新兴的渲染方法，它通过神经场景表示和体积渲染生成高质量的多视图一致图像。尽管基于神经辐射场的技术对于场景重建是稳健的，但它们添加或移除对象的能力仍然有限。本文提出了一种新的语言驱动方法，通过数据集更新实现具有神经辐射场的对象操作。具体而言，为了将由一组多视图图像表示的新前景对象插入背景辐射场，我们使用文本到图像的扩散模型来学习并生成组合图像，该组合图像将感兴趣的对象融合到视图之间的给定背景中。然后，这些组合图像用于细化背景辐射场，以便我们可以渲染包含对象和背景的视图一致的图像。为了确保视图的一致性，我们提出了一种数据集更新策略，该策略在将训练传播到剩余视图之前，优先考虑与已训练视图接近的相机视图的辐射场训练。我们表明，在相同的数据集更新策略下，我们可以使用文本到三维模型的数据以及对象移除来轻松地调整我们的对象插入方法。实验结果表明，我们的方法可以生成编辑场景的真实感图像，在三维重建和神经辐射场混合方面优于现有技术。 et.al.|[2309.11281](http://arxiv.org/abs/2309.11281)|null|
|**2023-09-19**|**PLVS: A SLAM System with Points, Lines, Volumetric Mapping, and 3D Incremental Segmentation**|本文介绍了PLVS：一个利用稀疏SLAM、体积映射和3D无监督增量分割的实时系统。PLVS代表点、线、体积映射和分割。它支持RGB-D和立体声相机，这些相机可以选择配备IMU。SLAM模块基于关键帧，提取并跟踪稀疏点和线段作为特征。体积映射相对于SLAM前端并行运行，并通过融合从关键帧反向投影的点云来生成探索环境的3D重建。PLVS支持并集成了不同的体积映射方法。我们使用一种新的重投影误差来对调整线段进行集束。该误差利用可用的深度信息来稳定线段端点的位置估计。在PLVS框架下，为RGB-D相机实现并集成了一种基于几何的增量分割方法。我们在一些公开的数据集上对PLVS框架进行了定性和定量评估。附录详细介绍了所采用的立体线三角测量方法，并对我们用于线误差项的雅可比矩阵进行了推导。该软件是开源的。 et.al.|[2309.10896](http://arxiv.org/abs/2309.10896)|null|
|**2023-09-19**|**SHOWMe: Benchmarking Object-agnostic Hand-Object 3D Reconstruction**|最近的手-物体交互数据集显示出有限的真实物体可变性，并且依赖于拟合MANO参数模型来获得真实的手形状。为了超越这些限制并推动进一步的研究，我们引入了SHOWMe数据集，该数据集由96个视频组成，用真实和详细的手对象3D纹理网格进行注释。根据最近的工作，我们考虑了一个刚性手对象场景，其中手相对于对象的姿势在整个视频序列中保持不变。这一假设使我们能够将亚毫米精度的地面实况3D扫描注册到SHOWMe中的图像序列中。尽管更简单，但这一假设在所需精度和细节水平很重要的应用中是有意义的，例如，人机协作中的对象移交、对象扫描或操作和接触点分析。重要的是，手对象系统的刚性允许使用由刚性配准步骤和多视图重建（MVR）部分组成的两阶段流水线来处理未知手持对象的基于视频的3D重建。我们仔细评估了这两个阶段的一组非平凡基线，并表明使用SfM工具箱或手部姿态估计器来恢复刚性变换和现成的MVR算法，可以实现有前景的对象不可知的3D手部对象重建。然而，这些方法对最初的相机姿态估计仍然敏感，由于物体上缺乏纹理或手的严重遮挡，这些估计可能不精确，这为重建留下了改进的空间。代码和数据集可在https://europe.naverlabs.com/research/showme et.al.|[2309.10748](http://arxiv.org/abs/2309.10748)|null|
|**2023-09-14**|**TCGF: A unified tensorized consensus graph framework for multi-view representation learning**|多视图学习技术最近在机器学习领域获得了极大的关注，因为它们能够利用多个视图之间的一致性和互补信息。然而，对于将现有工作统一为可扩展和稳健的学习框架的广义多视图框架，仍然缺乏足够的研究，因为目前的大多数工作都集中在特定风格的多视图模型上。此外，大多数多视角学习工作严重依赖于特定的量表场景，无法有效地全面理解多个量表。这些限制阻碍了来自多个视图的重要信息的有效融合，导致泛化能力差。为了解决这些局限性，本文提出了一个通用的多视图表示学习框架，称为张量化共识图框架（TCGF）。具体而言，它首先为现有的多视图作品提供了一个统一的框架，以利用单个视图的表示，该框架旨在适用于任意假设和不同规模的数据集。然后，在对齐基础上将它们堆叠成张量，作为高阶表示，允许一致性和互补信息在所有视图中平滑传播。此外，TCGF提出通过自适应地协作所有视图来学习共享的共识嵌入，以揭示多视图数据的基本结构，该方法利用视图共识分组效应来正则化视图共识表示。为了进一步促进相关研究，我们为大规模数据集提供了TCGF的具体实现，可以通过应用交替优化策略来有效解决。在七个不同规模的数据集上进行的实验结果表明，与现有最先进的多视图学习方法相比，所提出的TCGF具有优势。 et.al.|[2309.09987](http://arxiv.org/abs/2309.09987)|null|
|**2023-09-18**|**Improving Neural Indoor Surface Reconstruction with Mask-Guided Adaptive Consistency Constraints**|从2D图像重建3D场景一直是一项长期任务。最近的研究利用神经隐式表面作为3D重建的统一表示，而不是估计每帧深度图并将其融合到3D中。这些方法配备了数据驱动的预训练几何线索，表现出了良好的性能。然而，不准确的先验估计（这通常是不可避免的）可能导致次优重建质量，特别是在一些几何复杂的区域。在本文中，我们提出了一个两阶段的训练过程，解耦视图相关和视图无关的颜色，并利用两个新的一致性约束来提高细节重建性能，而不需要额外的先验。此外，我们引入了一个基本的掩码方案来自适应地影响监督约束的选择，从而提高自监督范式中的性能。在合成数据集和真实世界数据集上的实验表明，该方法能够减少先验估计误差的干扰，并实现具有丰富几何细节的高质量场景重建。 et.al.|[2309.09739](http://arxiv.org/abs/2309.09739)|null|
|**2023-09-18**|**Robust Geometry-Preserving Depth Estimation Using Differentiable Rendering**|在这项研究中，我们解决了从单目深度估计中恢复3D场景结构的挑战。虽然传统的深度估计方法利用标记的数据集来直接预测绝对深度，但最近的进展提倡混合数据集训练，增强了在不同场景中的泛化能力。然而，这种混合数据集训练只能产生未知规模和偏移的深度预测，阻碍了精确的3D重建。现有的解决方案需要额外的3D数据集或几何体完整的深度注释，这些限制了它们的通用性。在本文中，我们提出了一种学习框架，该框架训练模型来预测几何保持深度，而不需要额外的数据或注释。为了产生逼真的3D结构，我们渲染重建场景的新颖视图，并设计损失函数，以提高不同视图之间的深度估计一致性。全面的实验强调了我们框架卓越的泛化能力，在几个基准数据集上超越了现有的最先进的方法，而不需要利用额外的训练信息。此外，我们创新的损失函数使模型能够仅使用未标记的图像自主恢复特定领域的尺度和偏移系数。 et.al.|[2309.09724](http://arxiv.org/abs/2309.09724)|null|
|**2023-09-18**|**Self-supervised Multi-view Clustering in Computer Vision: A Survey**|近年来，多视图聚类（MVC）在跨模态表示学习和数据驱动决策中具有重要意义。它通过利用多个视图之间的一致性和互补信息将样本聚类到不同的组中来实现这一点。然而，随着对比学习在计算机视觉领域的不断发展，自监督学习也取得了实质性的研究进展，并逐渐在MVC方法中占据主导地位。它通过设计代理任务来指导聚类过程，以挖掘图像和视频数据本身作为监督信息的表示。尽管自监督MVC发展迅速，但目前还没有一个全面的调查来分析和总结研究进展的现状。因此，本文探讨了自监督MVC出现的原因和优势，并讨论了常见数据集的内部联系和分类、数据问题、表示学习方法和自监督学习方法。本文不仅介绍了每一类方法的机制，还举例说明了如何使用这些技术。最后指出了一些有待进一步研究和发展的问题。 et.al.|[2309.09473](http://arxiv.org/abs/2309.09473)|null|
|**2023-09-17**|**Uncertainty-aware 3D Object-Level Mapping with Deep Shape Priors**|三维对象级映射是机器人技术中的一个基本问题，当推理过程中对象CAD模型不可用时，这一问题尤其具有挑战性。在这项工作中，我们提出了一个框架，可以为未知对象重建高质量的对象级映射。我们的方法以多个RGB-D图像作为输入，并为检测到的对象输出密集的3D形状和9-DoF姿势（包括3个比例参数）。我们方法的核心思想是利用形状类别的学习生成模型作为先验，并为3D重建制定概率、不确定性感知的优化框架。我们推导了一个概率公式，该公式通过两个新的损失函数传播形状并带来不确定性。与当前最先进的方法不同，我们在优化过程中明确地对对象形状和姿态的不确定性进行建模，从而产生高质量的对象级映射系统。此外，我们证明，由此产生的形状和姿态不确定性可以准确地反映我们物体地图的真实误差，也可以用于下游机器人任务，如主动视觉。我们对室内和室外真实世界的数据集进行了广泛的评估，实现了对最先进方法的实质性改进。我们的代码将在https://github.com/TRAILab/UncertainShapePose. et.al.|[2309.09118](http://arxiv.org/abs/2309.09118)|null|
|**2023-09-15**|**Uncertainty-Aware Multi-View Visual Semantic Embedding**|图像文本检索的关键挑战是有效地利用语义信息来测量视觉和语言数据之间的相似性。然而，使用实例级二进制标签，即每个图像与单个文本配对，无法捕捉不同语义单元之间的多个对应关系，导致多模态语义理解的不确定性。尽管最近的研究通过更复杂的模型结构或预训练技术捕获了细粒度的信息，但很少有研究直接建模对应关系的不确定性，以充分利用二进制标签。为了解决这个问题，我们提出了一个不确定性感知的多视图视觉语义嵌入（UAMVSE）}框架，该框架将整个图像-文本匹配分解为多视图-文本匹配。我们的框架引入了一个不确定性感知损失函数（UALoss），通过自适应地建模每个视图文本对应关系中的不确定性来计算每个视图文本损失的权重。不同的权重引导模型关注不同的语义信息，增强了模型理解图像和文本对应关系的能力。我们还通过对相似度矩阵进行归一化，设计了一种优化的图像-文本匹配策略，以提高模型性能。在Flicker30k和MS-COCO数据集上的实验结果表明，UAMVSE的性能优于最先进的模型。 et.al.|[2309.08154](http://arxiv.org/abs/2309.08154)|null|
|**2023-09-14**|**High-fidelity 3D Reconstruction of Solar Coronal Physics with the Updated CROBAR Method**|我们提出了一种将冠状重建到B对齐区域（CROBAR）方法扩展到线性无力场（LFFF）外推的方法，并将其应用于AIA、MDI和STEREO EUVI数据集的重建。结果表明，CROBAR不仅可以重建日冕发射结构，而且可以通过LFFF的螺旋度 $\alpha$ 参数帮助约束日冕场外推。他们还提供了一个真实世界的例子，说明CROBAR如何轻松地从多个角度整合信息，以改进其重建，我们还使用其他角度来帮助验证重建。我们还谈到了使用真实世界的发射通带，而不是使用DEM的理想化幂律型通带。最后，我们将CROBAR产生的发射与观测到的发射以及基于理想DEM的幂律产生的发射进行了比较。这些结果进一步说明了CROBAR在现实世界应用中的前景，我们提供了该软件的初步版本供下载。 et.al.|[2309.08053](http://arxiv.org/abs/2309.08053)|null|

<p align=right>(<a href=#updated-on-20230921>back to top</a>)</p>

## Diffusion

|Publish Date|Title|Abstract|PDF|Code|
|---|---|---|---|---|
|**2023-09-20**|**FreeU: Free Lunch in Diffusion U-Net**|在本文中，我们揭示了扩散U-Net尚未开发的潜力，它是一种“免费午餐”，大大提高了动态生成质量。我们最初研究了U-Net架构对去噪过程的关键贡献，并确定其主干主要有助于去噪，而其跳跃连接主要将高频特征引入解码器模块，导致网络忽略主干语义。利用这一发现，我们提出了一种称为“FreeU”的简单而有效的方法，该方法无需额外的训练或微调即可提高生成质量。我们的关键见解是从战略上重新评估U-Net的跳过连接和主干功能图的贡献，以利用U-Net架构的两个组件的优势。图像和视频生成任务的良好结果表明，我们的FreeU可以很容易地集成到现有的扩散模型中，例如Stable diffusion、DreamBooth、ModelScope、Rerender和ReVersion，只需几行代码即可提高生成质量。您所需要的只是在推理过程中调整两个缩放因子。项目页面：https://chenyangsi.top/FreeU/. et.al.|[2309.11497](http://arxiv.org/abs/2309.11497)|null|
|**2023-09-20**|**Generative Agent-Based Modeling: Unveiling Social System Dynamics through Coupling Mechanistic Models with Generative Artificial Intelligence**|我们讨论了使用生成人工智能构建社会系统的反馈丰富的计算模型的新机会。这种个体级模型被称为基于生成代理的模型（GABM），利用诸如ChatGPT之类的大型语言模型来表示社会环境中的人类决策。我们提供了一个GABM案例，通过将人类交互的机制模型与预先训练的大型语言模型相结合，可以将人类行为纳入模拟模型中。这是通过在组织中引入社会规范扩散的简单GABM来实现的。出于教育目的，该模型有意保持简单。我们研究了广泛的场景以及结果对提示中的几个变化的敏感性。我们希望这篇文章和模型能作为建立有用的扩散模型的指南，包括现实的人类推理和决策。 et.al.|[2309.11456](http://arxiv.org/abs/2309.11456)|null|
|**2023-09-20**|**Brain-inspired computing with fluidic iontronic nanochannels**|大脑无与伦比的能量效率促使研究人员寻找新的大脑启发（神经形态）计算范式。人工水离子通道正在成为一个令人兴奋的神经形态计算新平台，通过直接模拟大脑中的流体离子传输，代表着与传统固态设备的背离。然而，尽管最近人们对此感兴趣，但神经形态计算的具体演示仍然是一个挑战。在这里，我们使用易于制造的锥形微通道成功地进行了神经形态储层计算，该通道在胶体之间嵌入了流体纳米通道的导电网络，我们证明这是一种新型忆阻器（记忆电阻器）。值得注意的是，通过构建不同长度的通道，可以很容易地实现广泛的典型电导记忆时间尺度，这是一个独特且非常理想的特征。这项工作受到了一个新的理论模型的启发和支持，该模型直接源于传统的扩散传导方程，并与实验显示出极好的一致性，预测了本文提出的特征和相关参数。我们的研究结果代表着实现离子通道作为一个模拟大脑丰富水动力学的新平台的前景的基本步骤。 et.al.|[2309.11438](http://arxiv.org/abs/2309.11438)|null|
|**2023-09-20**|**On the diffusion approximation of the stationary radiative transfer equation with absorption and emission**|我们研究了一个物体由于与辐射相互作用而导致温度分布的情况。在局部热力学平衡的假设下，我们考虑了稳态辐射传输方程的边值问题。我们研究了在没有散射的情况下的扩散平衡近似。我们认为吸收系数与频率 $\nu$（所谓的格雷近似）和光子平均自由程趋于零时的极限无关，即吸收系数趋于无穷大。我们证明，由于Stefan-Boltzmann定律，辐射能量的密度$u$ 与温度的四次方成正比，它在极限下求解了一个椭圆方程，其中边界值可以根据原始边界条件唯一确定。我们用匹配渐近展开法形式地导出了极限问题的边界条件，并通过对一些非局部积分算子的仔细分析，严格地证明了极限问题解的收敛性。这里开发的方法允许仅使用最大原理自变量来证明所有结果。 et.al.|[2309.11437](http://arxiv.org/abs/2309.11437)|null|
|**2023-09-20**|**Deep Networks as Denoising Algorithms: Sample-Efficient Learning of Diffusion Models in High-Dimensional Graphical Models**|我们研究了深度神经网络在基于扩散的生成建模中对分数函数的逼近效率。虽然现有的近似理论利用了得分函数的光滑性，但对于本质上高维的数据，它们却受到了维数的诅咒。这种限制在诸如马尔可夫随机场的图形模型中是明显的，马尔可夫随机场对于图像分布是常见的，其中得分函数的近似效率仍然是不稳定的。为了解决这个问题，我们观察到分数函数通常可以通过变分推理去噪算法在图形模型中很好地近似。此外，这些算法适用于有效的神经网络表示。我们在图形模型的例子中证明了这一点，包括伊辛模型、条件伊辛模型，限制玻尔兹曼机和稀疏编码模型。结合基于扩散采样的现成离散化误差边界，当深度神经网络学习分数函数时，我们为基于扩散的生成建模提供了一个有效的样本复杂度边界。 et.al.|[2309.11420](http://arxiv.org/abs/2309.11420)|null|
|**2023-09-20**|**EDMP: Ensemble-of-costs-guided Diffusion for Motion Planning**|用于机器人操作的经典运动规划包括一组通用算法，旨在最小化执行给定计划的特定场景成本。这种方法提供了显著的适应性，因为它们可以直接用于任何新场景，而不需要特定的训练数据集。然而，如果事先不了解什么是不同的有效轨迹，也没有为给定场景专门设计的成本函数，总体解决方案的成功率往往很低。虽然基于深度学习的算法极大地提高了成功率，但如果没有专门的训练数据集，它们就很难被采用。我们提出了EDMP，这是一个以成本为导向的运动规划扩散集成，旨在结合经典和基于深度学习的运动规划的优势。我们基于扩散的网络是在一组不同的运动学有效轨迹上训练的。与经典规划一样，对于推理时的任何新场景，我们计算特定场景的成本，如“碰撞成本”，并引导扩散生成满足特定场景约束的有效轨迹。此外，我们使用成本集合来指导扩散过程，与经典规划者相比，显著提高了成功率，而不是单一的成本函数可能不足以捕捉场景间的多样性。EDMP的性能与基于SOTA的深度学习方法相当，同时保留了主要与经典规划者相关的泛化能力。 et.al.|[2309.11414](http://arxiv.org/abs/2309.11414)|null|
|**2023-09-20**|**Mesoscale modeling of deformations and defects in crystalline sheets**|我们使用粗晶相场晶体（PFC）模型研究了具有晶序的柔性薄板的变形和缺陷。PFC模型描述了通过表示原子序数密度的连续周期场在扩散时间尺度上的晶体。在其振幅展开（APFC）中，实现了以缓慢变化的场为特征的粗粒度描述，保留了晶格变形、弹性和位错的高级描述。我们在一个方便的高度公式中引入了表面PFC和APFC模型，编码法向变形。利用这个框架，我们研究了应变片的屈曲、规定变形表面上的缺陷成核以及位错附近的平面外弛豫的一般方面。我们通过观察弹性变形下屈曲的连续极限，以及缺陷和缺陷排列处变形的微观模型的证据，来对我们的结果进行基准测试和讨论。我们通过观察位错偶极子的湮灭效应，阐明了位错晶格畸变和平面外变形之间的基本相互作用。设计的中尺度框架的尺度桥接能力也通过对含有许多位错的代表性薄板的模拟得到了展示。 et.al.|[2309.11371](http://arxiv.org/abs/2309.11371)|null|
|**2023-09-20**|**Face Aging via Diffusion-based Editing**|在这篇论文中，我们解决了面部衰老的问题：通过将与年龄相关的变化结合到给定的面部来生成过去或未来的面部图像。以前的老化方法仅依赖于人脸图像数据集，因此受到其固有规模和偏差的限制。这将其应用限制在有限的可生成年龄范围内，并且无法处理较大的年龄差距。我们提出了FADING，这是一种通过基于DIffusion的editiNG解决面部衰老问题的新方法。我们通过利用大规模语言图像扩散模型的丰富先验，超越了现有的方法。首先，我们通过使用年龄感知微调方案，将预先训练的扩散模型专门用于人脸年龄编辑任务。接下来，我们将输入图像反转为潜在噪声，并获得优化的空文本嵌入。最后，我们通过注意力控制执行文本引导的本地年龄编辑。定量和定性分析表明，我们的方法在老化精度、属性保存和老化质量方面优于现有方法。 et.al.|[2309.11321](http://arxiv.org/abs/2309.11321)|null|
|**2023-09-20**|**Social interactions for a sustainable lifestyle: The design of an experimental case study**|我们每天都面临着许多生活方式的决定，有些是由习惯决定的，有些是更有意识的，这些决定可能会也可能不会促进可持续生活。在数字技术的帮助下，可持续行为可以在社会群体和包容性社区中传播。本文概述了在智能住宅的背景下，社会影响对可持续性行为变化的纵向实验研究。参与者居住在被称为KTH Live in Lab的校园内的住房中，他们的行为与关键的生活方式选择有关，如食物、资源、流动性、消费和环境公民身份。重点是案例研究的准备阶段以及在设立过程中遇到的挑战和局限性。特别是，这项工作提出了对环境重要行为的可持续性指标的定义，并假设通过将家庭数字化为互动租户的社会网络，可以促进可持续生活。初步结果证实了所提出的实验方法的可行性。 et.al.|[2309.11310](http://arxiv.org/abs/2309.11310)|null|
|**2023-09-20**|**FaceDiffuser: Speech-Driven 3D Facial Animation Synthesis Using Diffusion**|语音驱动的三维人脸动画合成在工业和研究中都是一项具有挑战性的任务。最近的方法大多集中在确定性深度学习方法上，这意味着给定语音输入，输出总是相同的。然而，在现实中，遍布面部的非语言面部线索本质上是不确定的。此外，大多数方法都集中在基于3D顶点的数据集上，与现有的带有操纵角色的面部动画管道兼容的方法很少。为了消除这些问题，我们提出了FaceDiffuser，这是一种非确定性的深度学习模型，用于生成语音驱动的面部动画，该模型使用基于3D顶点和混合形状的数据集进行训练。我们的方法基于扩散技术，并使用预先训练的大语音表示模型HuBERT对音频输入进行编码。据我们所知，我们是第一个将扩散方法用于语音驱动的三维人脸动画合成任务的人。我们进行了广泛的客观和主观分析，结果表明，与最先进的方法相比，我们的方法取得了更好或可比的结果。我们还引入了一个新的内部数据集，该数据集基于基于blendshape的操纵角色。我们建议您观看随附的补充视频。代码和数据集将公开。 et.al.|[2309.11306](http://arxiv.org/abs/2309.11306)|null|

<p align=right>(<a href=#updated-on-20230921>back to top</a>)</p>

## NeRF

|Publish Date|Title|Abstract|PDF|Code|
|---|---|---|---|---|
|**2023-09-15**|**Breathing New Life into 3D Assets with Generative Repainting**|基于扩散的文本到图像模型引发了视觉社区、艺术家和内容创作者的巨大关注。这些模型的广泛采用是由于世代质量的显著提高以及对各种模式的有效调节，而不仅仅是文本。然而，将这些2D模型的丰富生成先验提升到3D中是具有挑战性的。最近的工作提出了由扩散模型和神经场的纠缠提供动力的各种管道。我们探索了预训练的2D扩散模型和标准3D神经辐射场作为独立工具的威力，并展示了它们以非学习方式协同工作的能力。这种模块化具有易于部分升级的内在优势，这在这样一个快节奏的领域中成为了一个重要的特性。我们的管道接受任何遗留的可渲染几何体，如纹理或无纹理网格，协调2D生成细化和3D一致性强制工具之间的交互，并以多种格式输出绘制的输入几何体。我们对ShapeNetSem数据集中的广泛对象和类别进行了大规模研究，并从定性和定量两个方面展示了我们方法的优势。项目页面：https://www.obukhov.ai/repainting_3d_assets et.al.|[2309.08523](http://arxiv.org/abs/2309.08523)|**[link](https://github.com/kongdai123/repainting_3d_assets)**|
|**2023-09-14**|**Neural Field Representations of Articulated Objects for Robotic Manipulation Planning**|传统的操作规划方法依赖于环境的显式几何模型来将给定任务公式化为优化问题。然而，从原始传感器输入推断准确的模型本身就是一个难题，尤其是对于铰接物体（例如壁橱、抽屉）。在本文中，我们提出了一种关节对象的神经场表示（NFR），可以直接从图像中进行操作规划。具体来说，在拍摄了一个新的关节物体的几张照片后，我们可以向前模拟它可能的运动，因此，可以直接使用该神经模型进行轨迹优化规划。此外，这种表示可以用于形状重建、语义分割和图像渲染，这在训练和泛化过程中提供了强大的监督信号。我们表明，我们的模型仅在合成图像上训练，能够在模拟和真实图像中为同类看不见的物体提取有意义的表示。此外，我们证明了该表示能够直接从图像中对现实世界中的关节物体进行机器人操作。 et.al.|[2309.07620](http://arxiv.org/abs/2309.07620)|null|
|**2023-09-13**|**Generalizable Neural Fields as Partially Observed Neural Processes**|神经场将信号表示为由神经网络参数化的函数，是传统离散矢量或基于网格的表示的一种很有前途的替代方案。与离散表示相比，神经表示既能很好地扩展分辨率，又是连续的，并且可以是多次可微的。然而，给定我们想要表示的信号数据集，必须为每个信号优化单独的神经场是低效的，并且不能利用信号之间的共享信息或结构。现有的泛化方法将其视为元学习问题，并采用基于梯度的元学习来学习初始化，然后通过测试时间优化对初始化进行微调，或者学习超网络来产生神经场的权重。相反，我们提出了一种新的范式，将神经表征的大规模训练视为部分观察到的神经过程框架的一部分，并利用神经过程算法来解决这一任务。我们证明，这种方法优于最先进的基于梯度的元学习方法和超网络方法。 et.al.|[2309.06660](http://arxiv.org/abs/2309.06660)|null|
|**2023-09-08**|**Single View Refractive Index Tomography with Neural Fields**|折射率层析成像是一个反问题，我们试图从2D投影图像测量中重建场景的3D折射场。折射场本身是不可见的，而是影响光线在空间中传播时路径的连续弯曲。折射场出现在各种各样的科学应用中，从显微镜中的半透明细胞样本到弯曲来自遥远星系的光的暗物质场。这个问题带来了一个独特的挑战，因为折射场直接影响光的路径，使其恢复成为一个非线性问题。此外，与传统的层析成像相比，我们试图通过利用散射在整个介质中的光源的知识，仅从单个视点使用投影图像来恢复折射场。在这项工作中，我们介绍了一种使用基于坐标的神经网络对场景中潜在的连续折射场进行建模的方法。然后，我们使用射线三维空间曲率的显式建模来优化该网络的参数，通过综合分析方法重建折射场。通过在模拟中恢复折射场，并分析光源分布对恢复的影响，证明了我们方法的有效性。然后，我们在模拟暗物质映射问题上测试了我们的方法，在该问题中，我们恢复了真实模拟暗物质分布下的折射场。 et.al.|[2309.04437](http://arxiv.org/abs/2309.04437)|null|
|**2023-09-07**|**BluNF: Blueprint Neural Field**|神经辐射场（NeRF）彻底改变了场景新颖的视图合成，提供了视觉逼真、精确和稳健的隐式重建。虽然最近的方法允许NeRF编辑，例如对象删除、3D形状修改或材料特性操纵，但在这种编辑之前的手动注释使该过程变得乏味。此外，传统的2D交互工具缺乏对3D空间的准确感知，阻碍了对场景的精确操作和编辑。在本文中，我们介绍了一种新的方法，称为蓝图神经场（BluNF），以解决这些编辑问题。BluNF提供了一个强大且用户友好的2D蓝图，实现了直观的场景编辑。通过利用隐式神经表示，BluNF使用先前的语义和深度信息构建场景的蓝图。生成的蓝图可以轻松编辑和操作NeRF表示。我们通过直观的点击和更改机制展示了BluNF的可编辑性，实现了3D操作，如遮罩、外观修改和对象移除。我们的方法对视觉内容创作做出了重大贡献，为该领域的进一步研究铺平了道路。 et.al.|[2309.03933](http://arxiv.org/abs/2309.03933)|null|
|**2023-09-07**|**SimNP: Learning Self-Similarity Priors Between Neural Points**|用于3D对象重建的现有神经场表示要么（1）利用对象级表示，但由于对全局潜在代码的限制而遭受低质量细节，要么（2）能够完美地重建观测，但未能利用对象级先验知识来推断未观察到的区域。我们提出了一种学习类别级自相似性的方法SimNP，它通过将神经点辐射场与类别级自类似性表示相连接，结合了两个世界的优点。我们的贡献是双重的。（1） 我们利用相干点云的概念设计了第一个类别级别的神经点表示。由此产生的神经点辐射场为局部支持的对象区域存储了高级别的细节。（2） 我们了解了如何以无约束和无监督的方式在神经点之间共享信息，这允许在重建过程中根据给定的观测值导出对象的未观察区域。我们表明，SimNP在重建对称的看不见物体区域方面优于以前的方法，超过了建立在类别级或像素对齐辐射场上的方法，同时提供了实例之间的语义对应 et.al.|[2309.03809](http://arxiv.org/abs/2309.03809)|null|
|**2023-09-06**|**CoNeS: Conditional neural fields with shift modulation for multi-sequence MRI translation**|多序列磁共振成像（MRI）在现代临床研究和深度学习研究中都有广泛的应用。然而，在临床实践中，由于患者的不同图像采集协议或造影剂禁忌症，经常会出现一个或多个MRI序列缺失的情况，这限制了在多序列数据上训练的深度学习模型的使用。一种很有前途的方法是利用生成模型来合成缺失的序列，这可以作为替代获取。解决这一问题的最先进方法是基于卷积神经网络（CNN），该网络通常存在频谱偏差，导致高频精细细节的重建较差。在本文中，我们提出了具有移位调制的条件神经场（CoNeS），这是一种以体素坐标为输入并学习用于多序列MRI平移的目标图像的表示的模型。所提出的模型使用多层感知器（MLP）代替CNN作为像素到像素映射的解码器。因此，每个目标图像被表示为神经场，该神经场通过利用学习的潜码的移位调制而被调节在源图像上。在BraTS 2018和前庭神经鞘瘤患者的内部临床数据集上进行的实验表明，所提出的方法在视觉和定量上都优于最先进的多序列MRI翻译方法。此外，我们进行了光谱分析，表明CoNeS能够克服传统CNN模型中常见的光谱偏差问题。为了进一步评估合成图像在临床下游任务中的使用，我们在推理时使用合成图像测试了分割网络。 et.al.|[2309.03320](http://arxiv.org/abs/2309.03320)|**[link](https://github.com/cyjdswx/cones)**|
|**2023-09-06**|**ResFields: Residual Neural Fields for Spatiotemporal Signals**|神经场是一类被训练来表示高频信号的神经网络，近年来由于其在复杂三维数据建模方面的出色性能，特别是通过单个多层感知器（MLP）的大神经符号距离（SDFs）或辐射场（NeRFs），而受到了极大的关注。然而，尽管用MLP表示信号的能力和简单性很强，但由于MLP的容量有限，这些方法在建模大而复杂的时间信号时仍然面临挑战。在本文中，我们提出了一种有效的方法来解决这一限制，将时间残差层纳入神经场，称为ResFields，这是一类专门设计用于有效表示复杂时间信号的新型网络。我们对ResFields的性质进行了全面的分析，并提出了一种矩阵分解技术来减少可训练参数的数量并增强泛化能力。重要的是，我们的公式与现有技术无缝集成，并在各种具有挑战性的任务中持续改进结果：2D视频近似、通过时间SDF的动态形状建模和动态NeRF重建。最后，我们通过展示ResFields在从轻量级捕捉系统的稀疏感官输入捕捉动态3D场景方面的有效性，展示了它的实用性。 et.al.|[2309.03160](http://arxiv.org/abs/2309.03160)|**[link](https://github.com/markomih/ResFields)**|
|**2023-09-01**|**GNFactor: Multi-Task Real Robot Learning with Generalizable Neural Feature Fields**|开发能够在非结构化现实世界环境中通过视觉观察执行各种操作任务的代理是机器人技术中的一个长期问题。为了实现这一目标，机器人需要对场景的3D结构和语义有全面的了解。在这项工作中，我们提出了 $\textbf｛GNFactor｝$，一种用于多任务机器人操作的视觉行为克隆代理，具有$\textbf｛G｝$通用$\textbf｛N｝$eural功能$\textbf｛F｝$字段。GNFactor联合优化了作为重建模块的可推广神经场（GNF）和作为决策模块的感知转换器，利用了共享的深度3D体素表示。为了在3D中结合语义，重建模块利用视觉语言基础模型（$\textit｛例如｝$ ，Stable Diffusion）将丰富的语义信息提取到深度3D体素中。我们在3个真实机器人任务中评估了GNFactor，并在10个RLBench任务中进行了详细的消融，演示次数有限。我们观察到GNFactor在可见和不可见任务中比当前最先进的方法有了实质性的改进，证明了GNFactor强大的泛化能力。我们的项目网站是https://yanjieze.com/GNFactor/。 et.al.|[2308.16891](http://arxiv.org/abs/2308.16891)|**[link](https://github.com/YanjieZe/GNFactor)**|
|**2023-08-30**|**Active Neural Mapping**|我们用不断学习的神经场景表示来解决主动映射的问题，即主动神经映射。关键在于通过有效的代理移动积极找到要探索的目标空间，从而最大限度地减少在以前看不见的环境中飞行中的地图不确定性。在本文中，我们检验了连续学习神经场的权重空间，并从经验上表明，神经变异性，即对随机权重扰动的预测鲁棒性，可以直接用于测量神经映射的瞬时不确定性。结合神经映射中继承的连续几何信息，可以引导agent找到一条可遍历的路径，以逐渐获得环境知识。我们首次提出了一种用于在线场景重建的具有基于坐标的隐式神经表示的主动映射系统。在视觉逼真的Gibson和Matterport3D环境中的实验证明了所提出方法的有效性。 et.al.|[2308.16246](http://arxiv.org/abs/2308.16246)|null|

<p align=right>(<a href=#updated-on-20230921>back to top</a>)</p>

[contributors-shield]: https://img.shields.io/github/contributors/Vincentqyw/cv-arxiv-daily.svg?style=for-the-badge
[contributors-url]: https://github.com/Vincentqyw/cv-arxiv-daily/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/Vincentqyw/cv-arxiv-daily.svg?style=for-the-badge
[forks-url]: https://github.com/Vincentqyw/cv-arxiv-daily/network/members
[stars-shield]: https://img.shields.io/github/stars/Vincentqyw/cv-arxiv-daily.svg?style=for-the-badge
[stars-url]: https://github.com/Vincentqyw/cv-arxiv-daily/stargazers
[issues-shield]: https://img.shields.io/github/issues/Vincentqyw/cv-arxiv-daily.svg?style=for-the-badge
[issues-url]: https://github.com/Vincentqyw/cv-arxiv-daily/issues

