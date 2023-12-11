[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]

## Updated on 2023.12.11
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
|**2023-12-07**|**MuRF: Multi-Baseline Radiance Fields**|我们提出了多基线辐射场（MuRF），这是一种通用的前馈方法，用于解决多个不同基线设置（小基线和大基线，以及不同数量的输入视图）下的稀疏视图合成问题。为了渲染目标新视图，我们将3D空间离散为平行于目标图像平面的平面，并相应地构建目标视图截头体。这样的目标体积表示与目标视图在空间上对齐，这有效地聚集了来自输入视图的相关信息以进行高质量渲染。由于其轴对齐性质，它还便于随后使用卷积网络进行辐射场回归。卷积网络建模的3D上下文使我们的方法能够合成比先前工作更清晰的场景结构。我们的MuRF在从简单物体（DTU）到复杂室内外场景（RealEstate10K和LLFF）的多种不同基线设置和不同场景中实现了最先进的性能。我们还在Mip-NeRF 360数据集上展示了有前景的零样本泛化能力，证明了MuRF的普遍适用性。 et.al.|[2312.04565](http://arxiv.org/abs/2312.04565)|**[link](https://github.com/autonomousvision/murf)**|
|**2023-12-07**|**Free3D: Consistent Novel View Synthesis without 3D Representation**|我们介绍了Free3D，这是一种用于从单个图像进行开集新视图合成（NVS）的简单方法。与Zero-1-to-3类似，我们从预先训练的2D图像生成器开始进行泛化，并对其进行NVS微调。与最近和同时进行的工作相比，我们在不使用显式3D表示的情况下获得了显著的改进，这是缓慢的、消耗内存的或训练额外的3D网络。我们通过新的每像素光线调节归一化（RCN）层对目标相机姿态进行更好的编码来实现这一点。后者通过告诉每个像素其特定的观看方向，在底层2D图像生成器中注入姿势信息。我们还通过轻量级的多视图注意力层和多视图噪声共享来提高多视图一致性。我们在Ob厌恶数据集上训练Free3D，并在包括OminiObject3D和GSO在内的几个新数据集中展示了对各种新类别的出色概括。我们希望我们简单有效的方法将成为一个坚实的基线，并有助于未来以更准确的姿态进行NVS研究。项目页面位于https://chuanxiaz.com/free3d/. et.al.|[2312.04551](http://arxiv.org/abs/2312.04551)|**[link](https://github.com/lyndonzheng/Free3D)**|
|**2023-12-07**|**Multi-View Unsupervised Image Generation with Cross Attention Guidance**|在神经辐射场（NeRF）模型的驱动下，人们对新视图合成越来越感兴趣，但由于它们依赖于精确注释的多视图图像，因此受到可扩展性问题的阻碍。最近的模型通过在合成多视图数据上微调大文本2图像扩散模型来解决这一问题。尽管有强大的零样本泛化，但它们可能需要后处理，并可能由于合成域间隙而面临质量问题。本文介绍了一种新的流水线，用于在单类别数据集上对姿态条件扩散模型进行无监督训练。在预训练的自监督视觉变换器（DINOv2）的帮助下，我们通过比较特定对象部分的可见性和位置来对数据集进行聚类，从而识别对象姿态。在姿势标签上训练并在推理时配备跨帧注意力的姿势条件扩散模型确保了跨视图的一致性，这进一步得益于我们新颖的硬注意力引导。我们的模型，MIRAGE，在真实图像的新颖视图合成方面超越了以往的工作。此外，正如我们在使用预训练的稳定扩散生成的合成图像上的实验所证明的那样，MIRAGE对不同的纹理和几何形状是鲁棒的。 et.al.|[2312.04337](http://arxiv.org/abs/2312.04337)|null|
|**2023-12-07**|**Towards 4D Human Video Stylization**|我们向4D（3D和时间）人类视频风格化迈出了第一步，它在一个统一的框架内解决了风格转换、新颖的视图合成和人类动画。虽然已经开发了许多视频风格化方法，但它们往往局限于在输入视频的特定视点中渲染图像，缺乏在动态场景中推广到新颖视图和新颖姿势的能力。为了克服这些限制，我们利用神经辐射场（NeRF）来表示视频，在渲染的特征空间中进行风格化。我们的创新方法包括使用两个NeRF同时表示人类主体和周围场景。这种双重表现促进了人类主体在各种姿势和新颖视角下的动画化。具体来说，我们引入了一种新的几何引导的三平面表示，与直接三平面优化相比，显著增强了特征表示的鲁棒性。在视频重建之后，在NeRF的渲染特征空间内执行风格化。大量实验表明，所提出的方法在风格化纹理和时间连贯性之间取得了卓越的平衡，超过了现有的方法。此外，我们的框架独特地扩展了其功能，以适应新颖的姿势和视角，使其成为创造性人类视频风格化的多功能工具。 et.al.|[2312.04143](http://arxiv.org/abs/2312.04143)|**[link](https://github.com/tiantianwang/4d_video_stylization)**|
|**2023-12-06**|**DreamComposer: Controllable 3D Object Generation via Multi-View Conditions**|利用预先训练的2D大规模生成模型，最近的工作能够从单个野生图像中生成高质量的新视图。然而，由于缺乏来自多个视角的信息，这些作品在生成可控的小说视角方面遇到了困难。在本文中，我们提出了DreamComposer，这是一个灵活且可扩展的框架，可以通过注入多视图条件来增强现有的视图感知扩散模型。具体而言，DreamComposer首先使用视图感知三维提升模块从多个视图中获得对象的三维表示。然后，利用多视图特征融合模块从三维表示中提取目标视图的潜在特征。最后，将从多视图输入中提取的目标视图特征注入到预先训练的扩散模型中。实验表明，DreamComposer与用于零样本新视图合成的最先进的扩散模型兼容，进一步增强了它们以生成具有多视图条件的高保真度新视图图像，为可控3D对象重建和各种其他应用做好了准备。 et.al.|[2312.03611](http://arxiv.org/abs/2312.03611)|null|
|**2023-12-06**|**Artist-Friendly Relightable and Animatable Neural Heads**|创建照片逼真数字化身的一种越来越常见的方法是通过使用体积神经场。当在一组多视图图像上训练时，原始神经辐射场（NeRF）允许静态头部进行令人印象深刻的新颖视图合成，后续方法表明，这些神经表示可以扩展到动态化身。最近，新的变体也超过了神经表示中烘焙照明的常见缺点，表明静态神经化身可以在任何环境中重新发光。在这项工作中，我们同时解决了运动和照明问题，为可重新照明和可动画化的神经头提出了一种新方法。我们的方法建立在一种已验证的动态化身方法的基础上，该方法基于体积基元的混合，结合最近提出的用于可重新照明神经场的轻量级硬件设置，并包括一种新的架构，该架构允许重新照明动态神经化身在任何环境中执行看不见的表情，即使是在近场照明和视点的情况下。 et.al.|[2312.03420](http://arxiv.org/abs/2312.03420)|null|
|**2023-12-06**|**RING-NeRF: A Versatile Architecture based on Residual Implicit Neural Grids**|自引入以来，神经场在三维重建和新视图合成方面变得非常流行。最近的研究集中在加速这一过程，以及提高对观测距离和有限监督视点数量变化的鲁棒性。然而，这些方法往往导致无法轻易结合的专门解决方案。为了解决这个问题，我们引入了一种新的简单但高效的架构，称为RING-NeRF，基于残差隐式神经网格，它提供了对场景和潜在空间之间映射函数的细节级别的控制。与距离感知的前向映射机制和连续的从粗到细的重建过程相关联，我们的多功能架构在以下方面展示了快速训练和最先进的性能：（1）抗混叠渲染，（2）从很少监督的视点的重建质量，以及（3）对于基于SDF的NeRF在没有适当的场景特定初始化的情况下的鲁棒性。我们还证明了我们的架构可以动态添加网格来增加重建的细节，为自适应重建开辟了道路。 et.al.|[2312.03357](http://arxiv.org/abs/2312.03357)|null|
|**2023-12-06**|**Feature 3DGS: Supercharging 3D Gaussian Splatting to Enable Distilled Feature Fields**|近年来，3D场景表示已经获得了巨大的普及。使用神经辐射场的方法适用于传统任务，如新颖的视图合成。近年来，出现了一些工作，旨在将NeRF的功能扩展到视图合成之外，用于语义感知任务，如使用2D基础模型中的3D特征场提取进行编辑和分割。然而，这些方法有两个主要的局限性：（a）它们受到NeRF管道的渲染速度的限制，以及（b）隐式表示的特征场受到连续性伪影的影响，从而降低了特征质量。最近，3D高斯散射在实时辐射场渲染方面表现出了最先进的性能。在这项工作中，我们更进一步：除了辐射场渲染外，我们还通过2D基础模型蒸馏实现了对任意维度语义特征的3D高斯飞溅。这种转换并不简单：天真地将特征字段合并到3DGS框架中会导致扭曲级别的差异。我们建议对架构和培训进行更改，以有效地避免此问题。我们提出的方法是通用的，我们的实验展示了新颖的视图语义分割、语言引导编辑和通过从最先进的2D基础模型（如SAM和CLIP-LSeg）中学习特征字段来分割任何内容。在整个实验中，我们的蒸馏方法能够提供类似或更好的结果，同时训练和渲染速度明显更快。此外，据我们所知，我们是第一个通过利用SAM模型启用点和边界框提示进行辐射场操作的方法。项目网站：https://feature-3dgs.github.io/ et.al.|[2312.03203](http://arxiv.org/abs/2312.03203)|null|
|**2023-12-05**|**HybridNeRF: Efficient Neural Rendering via Adaptive Volumetric Surfaces**|神经辐射场提供了最先进的视图合成质量，但渲染速度往往较慢。一个原因是它们使用体积渲染，因此在渲染时每条光线需要许多采样（和模型查询）。尽管这种表示方式灵活且易于优化，但大多数真实世界的对象都可以使用曲面而不是体积更有效地建模，因此每条射线所需的采样数要少得多。这一观察结果促使表面表示（如符号距离函数）取得了相当大的进展，但这些方法可能难以对半透明和薄结构进行建模。我们提出了一种名为HybridNeRF的方法，该方法通过将大多数对象渲染为曲面，同时对（通常）一小部分具有挑战性的区域进行体积建模，来利用这两种表示的优势。我们针对具有挑战性的Eyeful Tower数据集以及其他常用的视图合成数据集对HybridNeRF进行了评估。与最先进的基线（包括最近的基于光栅化的方法）相比，我们将错误率提高了15-30%，同时实现了虚拟现实分辨率（2Kx2K）的实时帧速率（至少36 FPS）。 et.al.|[2312.03160](http://arxiv.org/abs/2312.03160)|null|
|**2023-12-05**|**ReconFusion: 3D Reconstruction with Diffusion Priors**|神经辐射场（NeRFs）等3D重建方法擅长于绘制复杂场景的逼真新颖视图。然而，恢复高质量的NeRF通常需要数十到数百个输入图像，这导致了耗时的捕获过程。我们提出ReconFusion，只使用几张照片来重建真实世界的场景。我们的方法利用扩散先验进行新的视图合成，在合成和多视图数据集上训练，使基于NeRF的3D重建管道在输入图像集捕获的新相机姿态之外的新相机姿势下正则化。我们的方法在欠约束区域中合成逼真的几何体和纹理，同时保留观察到的区域的外观。我们在各种真实世界的数据集上进行了广泛的评估，包括前向和360度场景，证明了与以前的少数视图NeRF重建方法相比，性能有了显著提高。 et.al.|[2312.02981](http://arxiv.org/abs/2312.02981)|null|

<p align=right>(<a href=#updated-on-20231211>back to top</a>)</p>

## 3D Reconstruction

|Publish Date|Title|Abstract|PDF|Code|
|---|---|---|---|---|
|**2023-12-07**|**FitDiff: Robust monocular 3D facial shape and reflectance estimation using Diffusion Models**|三维人脸重建的显著进展已经产生了高细节和逼真的人脸表示。最近，扩散模型实现了比GANs更好的性能，从而彻底改变了生成方法的能力。在这项工作中，我们提出了FitDiff，一个基于扩散的三维人脸化身生成模型。该模型利用从“野外”2D面部图像中提取的身份嵌入，准确地生成可重新点亮的面部化身。我们的多模式漫射模型同时输出面部反射率图（漫射和镜面反照率和法线）和形状，显示出强大的泛化能力。它只在公共面部数据集的注释子集上进行训练，并与3D重建相结合。我们通过使用感知和人脸识别损失来引导反向扩散过程，重新审视典型的3D人脸拟合方法。FitDiff是第一个以人脸识别嵌入为条件的LDM，它重建了可重新照明的人类化身，可以像在普通渲染引擎中一样使用，只从不受约束的面部图像开始，并实现了最先进的性能。 et.al.|[2312.04465](http://arxiv.org/abs/2312.04465)|null|
|**2023-12-07**|**Cascade-Zero123: One Image to Highly Consistent 3D with Self-Prompted Nearby Views**|从单个图像合成多视图3D是一项重要而富有挑战性的任务。为此，Zero-1-to-3方法旨在将2D潜在扩散模型扩展到3D范围。这些方法生成具有单个视点图像和相机姿态作为条件信息的目标视点图像。然而，Zero-1-to-3中采用的一对一方式给在视图之间建立几何和视觉一致性带来了挑战，尤其是对于复杂对象。为了解决这个问题，我们提出了一个由两个Zero-1-to-3模型构建的级联生成框架，称为cascade-Zero123，该框架从源图像中逐步提取3D信息。具体而言，设计了一种自提示机制，用于首先生成几个附近的视图。然后将这些视图与源图像一起作为生成条件馈送到第二阶段模型中。以自我提示的多个视图作为补充信息，我们的Cascade-Zero123生成了比Zero-1-3更高度一致的新视图图像。该促销活动对各种复杂和具有挑战性的场景具有重要意义，包括昆虫、人类、透明物体和堆叠的多个物体等。项目页面位于https://cascadezero123.github.io/. et.al.|[2312.04424](http://arxiv.org/abs/2312.04424)|null|
|**2023-12-06**|**DreamComposer: Controllable 3D Object Generation via Multi-View Conditions**|利用预先训练的2D大规模生成模型，最近的工作能够从单个野生图像中生成高质量的新视图。然而，由于缺乏来自多个视角的信息，这些作品在生成可控的小说视角方面遇到了困难。在本文中，我们提出了DreamComposer，这是一个灵活且可扩展的框架，可以通过注入多视图条件来增强现有的视图感知扩散模型。具体而言，DreamComposer首先使用视图感知三维提升模块从多个视图中获得对象的三维表示。然后，利用多视图特征融合模块从三维表示中提取目标视图的潜在特征。最后，将从多视图输入中提取的目标视图特征注入到预先训练的扩散模型中。实验表明，DreamComposer与用于零样本新视图合成的最先进的扩散模型兼容，进一步增强了它们以生成具有多视图条件的高保真度新视图图像，为可控3D对象重建和各种其他应用做好了准备。 et.al.|[2312.03611](http://arxiv.org/abs/2312.03611)|null|
|**2023-12-06**|**Gaussian-Flow: 4D Reconstruction with Dynamic 3D Gaussian Particle**|我们介绍了高斯流，这是一种新的基于点的方法，用于快速动态场景重建和多视图和单目视频的实时渲染。与因训练和渲染速度缓慢而受到阻碍的流行的基于NeRF的方法相比，我们的方法利用了基于点的3D高斯散射（3DGS）的最新进展。具体而言，提出了一种新的双域变形模型（DDDM）来显式地对每个高斯点的属性变形进行建模，其中通过时域中的多项式拟合和频域中的傅立叶级数拟合来捕获每个属性的时间相关残差。所提出的DDDM能够对长视频镜头中的复杂场景变形进行建模，消除了为每帧训练单独的3DGS的需要，或者引入了额外的隐式神经场来对3D动力学进行建模。此外，离散高斯点的显式变形建模确保了4D场景的超快速训练和渲染，这与为静态3D重建设计的原始3DGS相当。我们提出的方法展示了显著的效率提高，与每帧3DGS建模相比，训练速度快了5倍。此外，定量结果表明，所提出的高斯流在新视图渲染质量方面显著优于以前的主流方法。项目页面：https://nju-3dv.github.io/projects/gaussian-flow et.al.|[2312.03431](http://arxiv.org/abs/2312.03431)|null|
|**2023-12-06**|**Evaluating the point cloud of individual trees generated from images based on Neural Radiance fields (NeRF) method**|树木的三维重建一直是林业精确管理和研究的关键任务。由于树木本身的树枝形态结构复杂，以及树干、树枝和树叶的遮挡，传统的摄影测量方法很难从二维图像中重建完整的三维树木模型。在本研究中，基于各种相机以不同方式收集的树木图像，将神经辐射场（NeRF）方法用于单个树木的重建，并将导出的点云模型与摄影测量重建和激光扫描方法获得的点云进行比较。结果表明，NeRF方法在单株树木三维重建中表现良好，重建成功率较高，在树冠区域重建效果较好，所需图像量较少。与摄影测量重建方法相比，NeRF在重建效率上具有显著优势，适用于复杂场景，但生成的点云往往具有噪声大、分辨率低的特点。从摄影测量点云中提取的树木结构参数（树高和胸径）的精度仍然高于从NeRF点云中导出的精度。该研究结果说明了NeRF方法在个体树木重建方面的巨大潜力，为复杂森林场景的三维重建和可视化提供了新的思路和研究方向。 et.al.|[2312.03372](http://arxiv.org/abs/2312.03372)|null|
|**2023-12-06**|**RING-NeRF: A Versatile Architecture based on Residual Implicit Neural Grids**|自引入以来，神经场在三维重建和新视图合成方面变得非常流行。最近的研究集中在加速这一过程，以及提高对观测距离和有限监督视点数量变化的鲁棒性。然而，这些方法往往导致无法轻易结合的专门解决方案。为了解决这个问题，我们引入了一种新的简单但高效的架构，称为RING-NeRF，基于残差隐式神经网格，它提供了对场景和潜在空间之间映射函数的细节级别的控制。与距离感知的前向映射机制和连续的从粗到细的重建过程相关联，我们的多功能架构在以下方面展示了快速训练和最先进的性能：（1）抗混叠渲染，（2）从很少监督的视点的重建质量，以及（3）对于基于SDF的NeRF在没有适当的场景特定初始化的情况下的鲁棒性。我们还证明了我们的架构可以动态添加网格来增加重建的细节，为自适应重建开辟了道路。 et.al.|[2312.03357](http://arxiv.org/abs/2312.03357)|null|
|**2023-12-06**|**Bile Duct Segmentation Methods Under 3D Slicer Applied to ERCP: Advantages and Disadvantages**|本文对用于3D重建的胆道分割方法进行了评估，该方法在各种关键干预措施中可能非常有用，如使用3D Slicer软件的内镜逆行胰胆管造影（ERCP）。本文对用于3D重建的胆道分割技术进行了评估，通过使用3D Slicer软件，该技术在内镜逆行胰胆管造影（ERCP）等各种关键程序中具有很高的价值。评估了三种不同的方法，即阈值法、洪水填充法和区域增长法的优缺点。该研究涉及10个患者病例，并采用定量指标和定性评估来评估不同分割方法获得的分割结果。结果表明，阈值法几乎是手动的且耗时，而洪水填充法是半自动的且耗时。尽管这两种方法都提高了分割质量，但它们是不可重复的。因此，开发了一种基于区域生长的自动方法来减少分割时间，尽管这是以牺牲质量为代价的。这些发现突出了不同传统分割方法的优缺点，并强调了探索替代方法的必要性，如深度学习，以优化ERCP背景下的胆道分割。 et.al.|[2312.03356](http://arxiv.org/abs/2312.03356)|null|
|**2023-12-05**|**Fully Convolutional Slice-to-Volume Reconstruction for Single-Stack MRI**|在磁共振成像（MRI）中，切片到体积重建（SVR）是指从被运动破坏的2D切片堆中计算重建未知的3D磁共振体积。虽然很有前景，但目前的SVR方法需要多个切片堆栈来进行精确的3D重建，这导致了长扫描，并限制了它们在胎儿功能磁共振成像等时间敏感应用中的使用。在这里，我们提出了一种SVR方法，该方法克服了先前工作的缺点，并在存在极端片间运动的情况下产生了最先进的重建。受最近单视图深度估计方法成功的启发，我们将SVR公式化为单堆栈运动估计任务，并训练全卷积网络来预测给定切片堆栈的运动堆栈，从而产生3D重建作为预测运动的副产品。对成人和胎儿大脑的SVR进行的广泛实验表明，我们的全卷积方法的准确性是以前的SVR方法的两倍。我们的代码可在github.com/seannz/svr上获得。 et.al.|[2312.03102](http://arxiv.org/abs/2312.03102)|null|
|**2023-12-05**|**ReconFusion: 3D Reconstruction with Diffusion Priors**|神经辐射场（NeRFs）等3D重建方法擅长于绘制复杂场景的逼真新颖视图。然而，恢复高质量的NeRF通常需要数十到数百个输入图像，这导致了耗时的捕获过程。我们提出ReconFusion，只使用几张照片来重建真实世界的场景。我们的方法利用扩散先验进行新的视图合成，在合成和多视图数据集上训练，使基于NeRF的3D重建管道在输入图像集捕获的新相机姿态之外的新相机姿势下正则化。我们的方法在欠约束区域中合成逼真的几何体和纹理，同时保留观察到的区域的外观。我们在各种真实世界的数据集上进行了广泛的评估，包括前向和360度场景，证明了与以前的少数视图NeRF重建方法相比，性能有了显著提高。 et.al.|[2312.02981](http://arxiv.org/abs/2312.02981)|null|
|**2023-12-05**|**R3D-SWIN:Use Shifted Window Attention for Single-View 3D Reconstruction**|最近，视觉转换器在各种计算机视觉任务中表现良好，包括体素3D重建。然而，视觉转换器的窗口不是多尺度的，并且窗口之间没有连接，这限制了体素三维重建的准确性。因此，我们提出了一种移位窗口关注体素三维重建网络。据我们所知，这是第一项将移位窗口注意力应用于体素3D重建的工作。在ShapeNet上的实验结果验证了我们的方法在单视图重建中达到了SOTA的精度。 et.al.|[2312.02725](http://arxiv.org/abs/2312.02725)|null|

<p align=right>(<a href=#updated-on-20231211>back to top</a>)</p>

## Diffusion

|Publish Date|Title|Abstract|PDF|Code|
|---|---|---|---|---|
|**2023-12-07**|**Gen2Det: Generate to Detect**|最近，扩散模型已经显示出合成图像质量的改善以及生成中更好的控制。我们激励并展示了Gen2Det，这是一个简单的模块化管道，通过利用最先进的基础图像生成方法，免费创建用于对象检测的合成训练数据。与现有的生成单个对象实例的工作不同，现有的工作需要识别前景，然后粘贴到其他图像上，我们简化为直接生成以场景为中心的图像。除了合成数据，Gen2Det还提出了一套技术来最好地利用生成的数据，包括图像级滤波、实例级滤波和更好的训练配方，以解决生成中的缺陷。使用Gen2Det，我们展示了在各种设置和检测方法不可知的情况下，对象检测和分割任务的健康改进。在LVIS的长尾检测设置中，Gen2Det在很大程度上提高了稀有类别的性能，同时也显著提高了其他类别的性能。例如，与使用Mask R-CNN在LVIS上仅对真实数据进行训练相比，我们看到了2.13 Box AP和1.84 Mask AP的改进。在COCO的低数据状态设置中，Gen2Det始终将Box和Mask AP分别提高2.27和1.85点。在最通用的检测设置中，Gen2Det仍然表现出强大的性能增益，例如，它将COCO上的Box和Mask AP提高了0.45和0.32点。 et.al.|[2312.04566](http://arxiv.org/abs/2312.04566)|null|
|**2023-12-07**|**NeRFiller: Completing Scenes via Generative 3D Inpainting**|我们提出了NeRFiller，这是一种通过使用现成的2D视觉生成模型进行生成3D修复来完成3D捕捉的缺失部分的方法。通常，由于网格重建失败或缺乏观察（例如，接触区域，例如对象的底部，或难以到达的区域），捕获的3D场景或对象的部分丢失。我们通过利用2D修复扩散模型来解决这个具有挑战性的3D修复问题。我们发现了这些模型的一个令人惊讶的行为，当图像形成2 $\times$ 2网格时，它们会生成更多的3D一致性修复，并展示了如何将这种行为推广到四个以上的图像。然后，我们提出了一个迭代框架，将这些修复区域提取到一个一致的3D场景中。与相关工作相比，我们专注于完成场景，而不是删除前景对象，并且我们的方法不需要严格的2D对象遮罩或文本。我们将我们的方法与适用于我们在各种场景中的设置的相关基线进行了比较，其中NeRFiller创建了最具3D一致性和合理性的场景完成。我们的项目页面位于https://ethanweber.me/nerfiller. et.al.|[2312.04560](http://arxiv.org/abs/2312.04560)|null|
|**2023-12-07**|**PrimDiffusion: Volumetric Primitives Diffusion for 3D Human Generation**|我们介绍了PrimDiffusion，这是第一个基于扩散的3D人体生成框架。由于3D表示的密集计算成本和3D人类的关节拓扑结构，为3D人类生成设计扩散模型是困难的。为了应对这些挑战，我们的关键见解是直接在一组体积基元上操作去噪扩散过程，该基元将人体建模为具有辐射和运动学信息的多个小体积。此体积基元表示将体积表示的容量与基于基元的渲染的效率相结合。我们的PrimDiffusion框架具有三个吸引人的特性：1）扩散模型的参数空间紧凑且富有表现力，2）结合人类先验的灵活3D表示，以及3）用于高效的新视图和新姿势合成的无解码器渲染。大量实验验证了PrimDiffusion在3D人体生成方面优于最先进的方法。值得注意的是，与基于GAN的方法相比，我们的PrimDiffusion支持在去噪过程完成后以 $512\times512$ 的分辨率实时渲染高质量的3D人类。我们还展示了我们的框架在无训练条件生成（如纹理转移和3D修复）方面的灵活性。 et.al.|[2312.04559](http://arxiv.org/abs/2312.04559)|**[link](https://github.com/frozenburning/primdiffusion)**|
|**2023-12-07**|**GenTron: Delving Deep into Diffusion Transformers for Image and Video Generation**|在这项研究中，我们探索了用于图像和视频生成的基于Transformer的扩散模型。尽管Transformer架构由于其灵活性和可扩展性在各个领域占据主导地位，但视觉生成领域主要利用基于CNN的U-Net架构，特别是在基于扩散的模型中。我们介绍了GenTron，一个使用基于Transformer的扩散的生成模型家族，以解决这一差距。我们的第一步是将扩散变换器（DiTs）从课堂条件反射到文本条件反射，这一过程涉及对条件反射机制的彻底实证探索。然后，我们将GenTron的参数从大约900M扩展到超过3B，观察到视觉质量的显著改善。此外，我们将GenTron扩展到文本到视频生成，结合新颖的无运动指导来提高视频质量。在针对SDXL的人类评估中，GenTron在视觉质量方面获得了51.1%的胜率（19.8%的胜率），在文本对齐方面获得了42.3%的胜率。GenTron还擅长T2I CompBench，突出了其在合成生成方面的优势。我们相信这项工作将提供有意义的见解，并为未来的研究提供宝贵的参考。 et.al.|[2312.04557](http://arxiv.org/abs/2312.04557)|null|
|**2023-12-07**|**SPIDeRS: Structured Polarization for Invisible Depth and Reflectance Sensing**|我们能隐形捕捉形状和反射率吗？这种能力对视觉、xR、机器人和人机交互等许多应用领域都很有价值。我们介绍了结构化偏振，这是第一种使用偏振光图案的深度和反射率传感方法（SPIDeRS）。关键思想是调制每个像素处投影光的线偏振角（AoLP）。偏振的使用使其不可见，不仅可以恢复深度，还可以直接恢复曲面法线甚至反射率。我们用液晶空间光调制器（SLM）和偏振相机实现SPIDeRS。我们推导了一种新的方法，用于从偏振物体的外观中稳健地提取投影的结构化偏振模式。我们通过将SPIDeRS应用于许多真实世界的对象来评估其有效性。结果表明，我们的方法成功地重建了各种材料的物体形状，并且对漫反射和环境光具有鲁棒性。我们还演示了使用恢复的曲面法线和反射率重新照明。我们相信SPIDeRS为偏振在视觉传感中的应用开辟了一条新的途径。 et.al.|[2312.04553](http://arxiv.org/abs/2312.04553)|null|
|**2023-12-07**|**Generating Illustrated Instructions**|我们介绍了生成图解说明的新任务，即根据用户需求定制的视觉说明。我们确定了这项任务特有的需求，并通过一套自动和人工评估指标将其形式化，旨在衡量几代人的有效性、一致性和功效。我们将大型语言模型（LLM）的强大功能与强文本到图像的生成扩散模型相结合，提出了一种称为StackedDiffusion的简单方法，该方法在给定文本作为输入的情况下生成这样的说明性指令。由此产生的模型大大优于基线方法和最先进的多模式LLM；在30%的情况下，用户甚至更喜欢它而不是人工生成的文章。最值得注意的是，它实现了各种新的、令人兴奋的应用程序，远远超出了网络上静态文章所能提供的范围，例如个性化指令，以及响应用户个人情况的中间步骤和图片。 et.al.|[2312.04552](http://arxiv.org/abs/2312.04552)|null|
|**2023-12-07**|**PlayFusion: Skill Acquisition via Diffusion from Language-Annotated Play**|从非结构化和非结构化数据中学习已经成为语言和视觉生成方法的主导范式。这种非结构化和无指导的行为数据，通常被称为游戏，在机器人中也更容易收集，但由于其固有的多模式、噪声和次优性质，学习起来要困难得多。在本文中，我们研究了从事后用语言标记的非结构化游戏数据中学习目标导向的技能策略的问题。具体来说，我们利用扩散模型的进步来学习多任务扩散模型，从游戏数据中提取机器人技能。使用状态和动作空间中的条件去噪扩散过程，我们可以优雅地处理游戏数据的复杂性和多模态，并生成各种有趣的机器人行为。为了使扩散模型对技能学习更有用，我们鼓励机器人代理通过在条件行为生成过程中引入离散瓶颈来获取技能词汇。在我们的实验中，我们展示了我们的方法在模拟和现实世界中的各种环境中的有效性。上的结果可视化和视频https://play-fusion.github.io et.al.|[2312.04549](http://arxiv.org/abs/2312.04549)|null|
|**2023-12-07**|**HyperDreamer: Hyper-Realistic 3D Content Generation and Editing from a Single Image**|从单个图像创建3D内容是一项长期但非常理想的任务。最近的进展引入了二维扩散先验，产生了合理的结果。然而，现有的方法对于后期生成的使用来说不够逼真，因为用户无法从全范围查看、渲染和编辑生成的3D内容。为了应对这些挑战，我们推出了HyperDreamer，它具有几个关键设计和吸引人的特性：1）可观看：具有高分辨率纹理的360度网格建模，可以从全方位的观察点创建视觉上引人注目的3D模型。2） 可渲染：结合细粒度语义分割和数据驱动先验作为指导，学习材料的合理反照率、粗糙度和镜面特性，实现语义感知的任意材料估计。3） 可编辑：对于生成的模型或他们自己的数据，用户可以通过点击几下交互式地选择任何区域，并通过基于文本的指导有效地编辑纹理。大量实验证明了HyperDreamer在使用高分辨率纹理建模区域感知材质和实现用户友好编辑方面的有效性。我们相信HyperDreamer有望推进3D内容创建和在各个领域寻找应用程序。 et.al.|[2312.04543](http://arxiv.org/abs/2312.04543)|null|
|**2023-12-07**|**Diffusion Reflectance Map: Single-Image Stochastic Inverse Rendering of Illumination and Reflectance**|反射限制了对象外观中照明的频谱。在本文中，我们介绍了第一种随机逆绘制方法，该方法从单个图像中联合恢复照明的全频谱和物体反射率。我们的关键思想是通过学习使用一种新的扩散模型（我们称之为扩散反射图网络（DRMNet））来反转图像形成，从而解决反射图中的这种盲逆问题，反射图是一种对底层几何结构不变的外观表示。给定从单个输入图像转换和完成的观测反射率图，DRMNet生成与完美镜面球体相对应的反射率图，同时联合估计反射率。正向过程可以理解为逐渐过滤具有越来越低的频率反射率和加性高斯噪声的自然照明。DRMNet学会了用两个子网络IllNet和RefNet来反转这一过程，这两个子网络协同工作来实现这一联合估计。该网络在广泛的合成数据集上进行了训练，并被证明可以推广到真实图像，在已建立的数据集上显示出最先进的准确性。 et.al.|[2312.04529](http://arxiv.org/abs/2312.04529)|null|
|**2023-12-07**|**RAVE: Randomized Noise Shuffling for Fast and Consistent Video Editing with Diffusion Models**|基于扩散的模型的最新进展已经证明在从文本生成图像方面取得了重大成功。然而，视频编辑模型在视觉质量和用户控制方面还没有达到同样的水平。为了解决这一问题，我们引入了RAVE，这是一种零样本视频编辑方法，利用预先训练的文本到图像扩散模型，而无需额外训练。RAVE采用输入视频和文本提示来生成高质量的视频，同时保留原始运动和语义结构。它采用了一种新颖的噪声混洗策略，利用帧之间的时空交互，以比现有方法更快的速度生成时间一致的视频。它在内存需求方面也很高效，可以处理更长的视频。RAVE能够进行广泛的编辑，从局部属性修改到形状转换。为了展示RAVE的多功能性，我们创建了一个全面的视频评估数据集，从以对象为中心的场景到复杂的人类活动，如跳舞和打字，以及以游泳的鱼和船为特色的动态场景。与现有方法相比，我们的定性和定量实验突出了RAVE在不同视频编辑场景中的有效性。我们的代码、数据集和视频可以在中找到https://rave-video.github.io. et.al.|[2312.04524](http://arxiv.org/abs/2312.04524)|**[link](https://github.com/rehg-lab/rave)**|

<p align=right>(<a href=#updated-on-20231211>back to top</a>)</p>

## NeRF

|Publish Date|Title|Abstract|PDF|Code|
|---|---|---|---|---|
|**2023-12-06**|**Gaussian-Flow: 4D Reconstruction with Dynamic 3D Gaussian Particle**|我们介绍了高斯流，这是一种新的基于点的方法，用于快速动态场景重建和多视图和单目视频的实时渲染。与因训练和渲染速度缓慢而受到阻碍的流行的基于NeRF的方法相比，我们的方法利用了基于点的3D高斯散射（3DGS）的最新进展。具体而言，提出了一种新的双域变形模型（DDDM）来显式地对每个高斯点的属性变形进行建模，其中通过时域中的多项式拟合和频域中的傅立叶级数拟合来捕获每个属性的时间相关残差。所提出的DDDM能够对长视频镜头中的复杂场景变形进行建模，消除了为每帧训练单独的3DGS的需要，或者引入了额外的隐式神经场来对3D动力学进行建模。此外，离散高斯点的显式变形建模确保了4D场景的超快速训练和渲染，这与为静态3D重建设计的原始3DGS相当。我们提出的方法展示了显著的效率提高，与每帧3DGS建模相比，训练速度快了5倍。此外，定量结果表明，所提出的高斯流在新视图渲染质量方面显著优于以前的主流方法。项目页面：https://nju-3dv.github.io/projects/gaussian-flow et.al.|[2312.03431](http://arxiv.org/abs/2312.03431)|null|
|**2023-12-06**|**Artist-Friendly Relightable and Animatable Neural Heads**|创建照片逼真数字化身的一种越来越常见的方法是通过使用体积神经场。当在一组多视图图像上训练时，原始神经辐射场（NeRF）允许静态头部进行令人印象深刻的新颖视图合成，后续方法表明，这些神经表示可以扩展到动态化身。最近，新的变体也超过了神经表示中烘焙照明的常见缺点，表明静态神经化身可以在任何环境中重新发光。在这项工作中，我们同时解决了运动和照明问题，为可重新照明和可动画化的神经头提出了一种新方法。我们的方法建立在一种已验证的动态化身方法的基础上，该方法基于体积基元的混合，结合最近提出的用于可重新照明神经场的轻量级硬件设置，并包括一种新的架构，该架构允许重新照明动态神经化身在任何环境中执行看不见的表情，即使是在近场照明和视点的情况下。 et.al.|[2312.03420](http://arxiv.org/abs/2312.03420)|null|
|**2023-12-06**|**RING-NeRF: A Versatile Architecture based on Residual Implicit Neural Grids**|自引入以来，神经场在三维重建和新视图合成方面变得非常流行。最近的研究集中在加速这一过程，以及提高对观测距离和有限监督视点数量变化的鲁棒性。然而，这些方法往往导致无法轻易结合的专门解决方案。为了解决这个问题，我们引入了一种新的简单但高效的架构，称为RING-NeRF，基于残差隐式神经网格，它提供了对场景和潜在空间之间映射函数的细节级别的控制。与距离感知的前向映射机制和连续的从粗到细的重建过程相关联，我们的多功能架构在以下方面展示了快速训练和最先进的性能：（1）抗混叠渲染，（2）从很少监督的视点的重建质量，以及（3）对于基于SDF的NeRF在没有适当的场景特定初始化的情况下的鲁棒性。我们还证明了我们的架构可以动态添加网格来增加重建的细节，为自适应重建开辟了道路。 et.al.|[2312.03357](http://arxiv.org/abs/2312.03357)|null|
|**2023-12-06**|**Multifractality in critical neural field dynamics**|大脑临界性框架在很大程度上认为大脑动力学是单分形的，尽管实验证据表明大脑表现出显著的多重分形。为了理解多重分形是如何在类临界系统中出现的，我们使用了临界神经振荡的计算模型。我们发现多重分形在同步相变附近出现。这些发现表明，时间动力学的多重分形在神经场的临界点达到峰值，为解释大脑记录中的多重分形提供了一个生成模型。 et.al.|[2312.03219](http://arxiv.org/abs/2312.03219)|null|
|**2023-12-04**|**GaussianHead: Impressive 3D Gaussian-based Head Avatars with Dynamic Hybrid Neural Field**|以前的头部化身方法大多依赖于固定的显式基元（网格、点）或隐式曲面（符号距离函数）和体积神经辐射场，难以在高保真度、训练速度和资源消耗之间取得平衡。混合场最近的流行带来了新的表示，但受到通过固定映射获得的参数化因子的限制。我们提出了GaussianHead：一种基于各向异性三维高斯基元的头部化身算法。我们利用规范高斯来表示动态场景。使用显式“动态”三平面作为参数化头部几何的有效容器，与底层几何和三平面中的因子很好地对齐，我们获得了正则高斯的对齐正则因子。利用微小的MLP，因子被解码为3D高斯基元的不透明度和球面谐波系数。最后，我们使用高效的可微高斯光栅化器进行渲染。我们的方法显著受益于我们基于3D高斯的新表示，并且三平面中底层几何结构和因子的适当对齐变换消除了固定映射引入的偏差。与最先进的技术相比，我们在自我重建、新视图合成和跨身份再现等任务中实现了最佳的视觉效果，同时保持了高渲染效率（每帧0.12秒）。在某些情况下，甚至鼻子周围的毛孔也清晰可见。代码和其他视频可以在项目主页上找到。 et.al.|[2312.01632](http://arxiv.org/abs/2312.01632)|null|
|**2023-11-29**|**Accelerating Neural Field Training via Soft Mining**|我们提出了一种通过有效选择采样位置来加速神经场训练的方法。虽然神经场最近变得很流行，但它通常是通过对训练域进行统一采样或通过手工启发式进行训练的。我们证明，通过基于重要性采样的软挖掘技术可以提高收敛性和最终训练质量：我们不是完全考虑或忽略一个像素，而是用标量来衡量相应的损失。为了实现我们的想法，我们使用Langevin蒙特卡罗采样。我们表明，通过这样做，具有更高误差的区域被更频繁地选择，导致收敛速度提高了2倍以上。本研究的代码和相关资源可在https://ubc-vision.github.io/nf-soft-mining/. et.al.|[2312.00075](http://arxiv.org/abs/2312.00075)|null|
|**2023-11-29**|**Neural Fields with Thermal Activations for Arbitrary-Scale Super-Resolution**|最近的任意尺度单图像超分辨率（ASSR）方法已经使用局部神经场来表示可以以不同速率采样的连续信号。然而，在这样的公式中，场值的逐点查询并不自然地与给定像素的点扩散函数（PSF）匹配。在这项工作中，我们提出了一种设计神经场的新方法，使得可以使用高斯PSF来查询点，该函数在ASSR的分辨率之间移动时起到抗混叠的作用。我们使用从傅立叶理论和热方程导出的新激活函数来实现这一点。这不需要额外的成本：与图像域中的滤波不同，在我们的框架中使用高斯PSF查询点不会影响计算成本。与超网络相结合，我们的方法不仅提供了理论上有保证的抗混叠，而且为ASSR设置了一个新的标准，同时也比以前的方法更具参数效率。 et.al.|[2311.17643](http://arxiv.org/abs/2311.17643)|null|
|**2023-11-28**|**In Search of a Data Transformation That Accelerates Neural Field Training**|神经场是数据表示中一种新兴的范式，它训练神经网络来逼近给定的信号。阻碍其广泛采用的一个关键障碍是编码速度——生成神经场需要神经网络的过拟合，这可能需要大量的SGD步骤才能达到所需的保真度水平。在本文中，我们深入研究了数据转换对神经场训练速度的影响，特别是关注像素位置的排列如何影响SGD的收敛速度。与直觉相反，我们发现随机排列像素位置可以显著加速训练。为了解释这一现象，我们通过PSNR曲线、损失景观和误差模式来检验神经场训练。我们的分析表明，随机像素排列去除了易于拟合的模式，这有助于在早期阶段进行简单的优化，但阻碍了捕捉信号的精细细节。 et.al.|[2311.17094](http://arxiv.org/abs/2311.17094)|null|
|**2023-11-28**|**HumanGaussian: Text-Driven 3D Human Generation with Gaussian Splatting**|根据文本提示生成逼真的三维人体是一项理想但具有挑战性的任务。现有的方法通过分数蒸馏采样（SDS）优化3D表示，如网格或神经场，其存在细节不足或训练时间过长的问题。在本文中，我们提出了一个高效而有效的框架HumanGaussian，它可以生成具有细粒度几何结构和逼真外观的高质量3D人。我们的关键见解是，3D高斯飞溅是一种具有周期性高斯收缩或增长的高效渲染器，其中这种自适应密度控制可以由内在的人体结构自然引导。具体而言，1）我们首先提出了一种结构感知SDS，它可以同时优化人体外观和几何形状。利用RGB和深度空间的多模态得分函数来提取高斯致密化和修剪过程。2） 此外，我们通过将SDS分解为更嘈杂的生成分数和更干净的分类器分数，设计了一种退火的负提示引导，很好地解决了过饱和问题。在仅修剪阶段中，基于高斯大小进一步消除浮动伪影，以增强生成平滑度。大量实验证明了我们的框架具有卓越的效率和竞争力，在不同的场景下呈现了生动的3D人类。项目页面：https://alvinliu0.github.io/projects/humangaussian et.al.|[2311.17061](http://arxiv.org/abs/2311.17061)|null|
|**2023-11-28**|**SplitNeRF: Split Sum Approximation Neural Field for Joint Geometry, Illumination, and Material Estimation**|我们提出了一种新的方法，通过从一组具有固定照明的姿势图像中估计真实世界物体的几何结构、材料特性和环境照明来数字化它们。我们的方法将分割和近似与基于图像的照明结合到神经辐射场（NeRF）管道中，用于基于物理的实时渲染。我们建议使用单个场景特定的MLP来建模场景的照明，该MLP表示任意分辨率的预集成的基于图像的照明。我们通过开发一种基于有效蒙特卡罗采样的新型正则化子来实现预集成照明的精确建模。此外，我们还提出了一种新的方法，通过利用基于蒙特卡罗采样的类似正则化子来监督自遮挡预测。实验结果证明了我们的方法在估计场景几何、材料特性和照明方面的效率和有效性。我们的方法能够在单个NVIDIA A100 GPU中仅经过 ${\sim}1$ 小时的训练后就获得最先进的重新照明质量。 et.al.|[2311.16671](http://arxiv.org/abs/2311.16671)|null|

<p align=right>(<a href=#updated-on-20231211>back to top</a>)</p>

[contributors-shield]: https://img.shields.io/github/contributors/Vincentqyw/cv-arxiv-daily.svg?style=for-the-badge
[contributors-url]: https://github.com/Vincentqyw/cv-arxiv-daily/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/Vincentqyw/cv-arxiv-daily.svg?style=for-the-badge
[forks-url]: https://github.com/Vincentqyw/cv-arxiv-daily/network/members
[stars-shield]: https://img.shields.io/github/stars/Vincentqyw/cv-arxiv-daily.svg?style=for-the-badge
[stars-url]: https://github.com/Vincentqyw/cv-arxiv-daily/stargazers
[issues-shield]: https://img.shields.io/github/issues/Vincentqyw/cv-arxiv-daily.svg?style=for-the-badge
[issues-url]: https://github.com/Vincentqyw/cv-arxiv-daily/issues

