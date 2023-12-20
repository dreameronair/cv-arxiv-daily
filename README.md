[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]

## Updated on 2023.12.20
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
|**2023-12-19**|**pixelSplat: 3D Gaussian Splats from Image Pairs for Scalable Generalizable 3D Reconstruction**|我们介绍了pixelSplat，这是一种前馈模型，它学习从成对的图像中重建由3D高斯基元参数化的3D辐射场。我们的模型具有实时和内存高效的渲染功能，可进行可扩展训练，并在推理时进行快速3D重建。为了克服稀疏和局部支持表示固有的局部极小值，我们预测了三维上的稠密概率分布，并根据该概率分布对高斯均值进行采样。我们通过重新参数化技巧使这种采样操作可微分，允许我们通过高斯飞溅表示反向传播梯度。我们在真实世界的RealEstate10k和ACID数据集上以宽基线新视图合成为基准，在那里我们优于最先进的光场变换器，并将渲染加速2.5个数量级，同时重建可解释和可编辑的3D辐射场。 et.al.|[2312.12337](http://arxiv.org/abs/2312.12337)|null|
|**2023-12-19**|**MixRT: Mixed Neural Representations For Real-Time NeRF Rendering**|神经辐射场（NeRF）由于其令人印象深刻的真实感重建和渲染能力，已成为新型视图合成的领先技术。然而，在大规模场景中实现实时NeRF渲染带来了挑战，通常导致采用具有大量三角形的复杂烘焙网格表示或烘焙表示中的资源密集型光线行进。我们对这些约定提出了质疑，注意到由具有实质三角形的网格表示的高质量几何体对于实现照片级真实感渲染质量是不必要的。因此，我们提出了MixRT，这是一种新的NeRF表示，包括低质量网格、视图相关位移图和压缩的NeRF模型。这种设计有效地利用了现有图形硬件的功能，从而实现了边缘设备上的实时NeRF渲染。利用高度优化的基于WebGL的渲染框架，我们提出的MixRT在边缘设备上实现了实时渲染速度（在MacBook M1 Pro笔记本电脑上以1280 x 720的分辨率超过30 FPS）、更好的渲染质量（在Unboundd-360数据集的室内场景中高出0.2 PSNR）和更小的存储大小（与最先进的方法相比，小于80%）。 et.al.|[2312.11841](http://arxiv.org/abs/2312.11841)|null|
|**2023-12-18**|**GauFRe: Gaussian Deformation Fields for Real-time Dynamic Novel View Synthesis**|我们提出了一种使用可变形3D高斯进行动态场景重建的方法，该方法适用于单目视频。在高斯飞溅效率的基础上，我们的方法通过位于规范空间中的可变形高斯集和由多层感知器（MLP）定义的时间相关变形场来扩展表示以适应动态元素。此外，在大多数自然场景都有保持静态的大区域的假设下，我们允许MLP通过额外包括静态高斯点云来集中其代表能力。串联的动态和静态点云形成高斯飞溅光栅化器的输入，从而实现实时渲染。在自监督渲染损失的情况下，对可微管道进行端到端优化。我们的方法获得的结果与最先进的动态神经辐射场方法相当，同时允许更快的优化和渲染。项目网站：https://lynl7130.github.io/gaufre/index.html et.al.|[2312.11458](http://arxiv.org/abs/2312.11458)|null|
|**2023-12-18**|**SinMPI: Novel View Synthesis from a Single Image with Expanded Multiplane Images**|单图像新视图合成是一个具有挑战性且正在进行的问题，其目的是从单个输入图像生成无限数量的一致视图。尽管已经做出了重大努力来提高生成的新视图的质量，但对底层场景表示的扩展却关注较少，这对生成逼真的新视图图像至关重要。本文提出了SinMPI，这是一种使用扩展多平面图像（MPI）作为3D场景表示的新方法，可以显著扩展MPI的透视范围，并从大的多平面空间生成高质量的新视图。我们的方法的关键思想是使用稳定扩散生成视图外内容，根据单目深度估计器预测的深度将所有场景内容投影到扩展的多平面图像中，然后在深度感知扭曲和修复模块生成的伪多视图数据的监督下优化多平面图像。我们进行了定性和定量实验，以验证我们的方法相对于现有技术的优越性。我们的代码和数据可在https://github.com/trickygo/sinmpi. et.al.|[2312.11037](http://arxiv.org/abs/2312.11037)|null|
|**2023-12-18**|**T-Code: Simple Temporal Latent Code for Efficient Dynamic View Synthesis**|动态场景的新颖视图合成是计算机视觉研究的热点之一。有效的动态视图合成的关键是找到一个紧凑的表示来存储跨时间的信息。尽管现有的方法通过张量分解或哈希网格特征级联来实现快速的动态视图合成，但它们的混合表示忽略了时域和空域之间的结构差异，导致计算和存储成本次优。本文提出了仅在时间维度上有效解耦的潜码T码。分解的功能设计使定制模块能够满足不同场景的个性化需求，并以更低的成本产生所需的结果。基于T代码，我们提出了用于多摄像机设置的高度紧凑的混合神经图形基元（HybridNGP）和用于单目场景的具有T代码的变形神经图形基基元（DNGP-T）。实验表明，HybridNGP以极低的存储消耗以最高的处理速度提供高保真度结果，而DNGP-T则实现了最先进的单目重建质量和高训练速度。 et.al.|[2312.11015](http://arxiv.org/abs/2312.11015)|null|
|**2023-12-17**|**PNeRFLoc: Visual Localization with Point-based Neural Radiance Fields**|由于能够合成高质量的新视图，神经辐射场（NeRF）最近被用来改善已知环境中的视觉定位。然而，现有的方法大多利用NeRFs进行数据扩充来改进回归模型的训练，并且由于缺乏几何约束，在新的视点和外观上的性能仍然有限。在本文中，我们提出了一种新的基于统一点表示的视觉定位框架，即PNeRFLoc。一方面，PNeRFLoc像传统的基于结构的方法一样，通过匹配2D和3D特征点来支持初始姿态估计；另一方面，它还通过使用基于渲染的优化的新颖视图合成来实现姿态细化。具体来说，我们提出了一种新的特征自适应模块来缩小视觉定位和神经渲染特征之间的差距。为了提高基于神经渲染的优化的有效性和效率，我们还开发了一个具有扭曲损失函数的高效基于渲染的框架。此外，还开发了几种鲁棒性技术来处理室外场景的照明变化和动态对象。实验表明，当NeRF模型可以很好地学习时，PNeRFLoc在合成数据上表现最好，并且在视觉定位基准数据集上表现与SOTA方法相当。 et.al.|[2312.10649](http://arxiv.org/abs/2312.10649)|null|
|**2023-12-15**|**SlimmeRF: Slimmable Radiance Fields**|神经辐射场（NeRF）及其变体最近已成为新型视图合成和3D场景重建的成功方法。然而，大多数当前的NeRF模型要么使用大的模型尺寸来实现高精度，要么通过权衡精度来实现高存储效率。这限制了任何单个模型的适用范围，因为高精度模型可能不适合低内存设备，而高效内存模型可能无法满足高质量要求。为此，我们提出了SlimmeRF模型，该模型允许通过精简在模型大小和准确性之间进行即时测试时间权衡，从而使模型同时适用于具有不同计算预算的场景。我们通过一种新提出的名为张量秩增量（TRaIn）的算法来实现这一点，该算法在训练过程中逐渐增加模型张量表示的秩。我们还观察到，我们的模型允许在稀疏视图场景中进行更有效的权衡，有时甚至在精简后实现更高的精度。我们将此归功于这样一个事实，即错误信息（如浮动信息）往往存储在与更高级别相对应的组件中。我们的实施可在https://github.com/shiran-yuan/slimmerf. et.al.|[2312.10034](http://arxiv.org/abs/2312.10034)|**[link](https://github.com/shiran-yuan/slimmerf)**|
|**2023-12-15**|**RANRAC: Robust Neural Scene Representations via Random Ray Consensus**|我们介绍了RANRAC，这是一种用于处理遮挡和分心图像的3D对象的鲁棒重建算法，这是现有鲁棒重建方法无法处理的一个特别具有挑战性的场景。我们的解决方案通过涉及光场网络支持单镜头重建，也适用于基于神经辐射场的真实世界图像的照片逼真、鲁棒、多视图重建。虽然该算法对场景表示以及支持的场景类型施加了一定的限制，但它可靠地检测并排除了不一致的视角，从而产生了没有浮动伪影的干净图像。我们的解决方案基于随机样本一致性范式的模糊自适应，使其能够应用于大规模模型。我们将确定模型参数的最小样本数解释为可调超参数。这是适用的，因为更干净的样本集提高了重建质量。此外，此过程还处理异常值。特别是对于条件模型，它可以在潜在空间中产生与完全干净集相同的局部最小值。我们报告了在遮挡场景中新视图合成的显著改进，与基线相比，PSNR高达8dB。 et.al.|[2312.09780](http://arxiv.org/abs/2312.09780)|null|
|**2023-12-15**|**SLS4D: Sparse Latent Space for 4D Novel View Synthesis**|神经辐射场（NeRF）在静态场景的新视图合成和三维表示方面取得了巨大成功。现有的动态NeRF通常利用局部密集网格来拟合变形场；然而，它们未能捕捉到全局动力学，并随之产生重参数模型。我们观察到4D空间本质上是稀疏的。首先，由于运动的连续性，变形场在空间上是稀疏的，但在时间上是密集的。其次，辐射场仅在底层场景的表面有效，通常只占整个空间的一小部分。因此，我们建议使用可学习的稀疏潜在空间（也称为SLS4D）来表示4D场景。具体而言，SLS4D首先使用密集的可学习时隙特征来描述时间空间，从该时间空间中，变形场与线性多层感知（MLP）相拟合，以预测任何时候3D位置的位移。然后，它使用另一个稀疏的潜在空间来学习3D位置的空间特征。这是通过利用注意力机制学习每个潜在代码的自适应权重来实现的。大量实验证明了我们的SLS4D的有效性：它仅使用最近工作的大约 $6\%$ 参数就实现了最佳的4D新视图合成。 et.al.|[2312.09743](http://arxiv.org/abs/2312.09743)|null|
|**2023-12-15**|**TIFace: Improving Facial Reconstruction through Tensorial Radiance Fields and Implicit Surfaces**|本报告描述了在ICCV 2023研讨会上获得“人类头部视图综合挑战（VSCHH）”第一名的解决方案。考虑到人类头部的稀疏视图图像，这一挑战的目标是从新的视点合成图像。由于面部纹理的复杂性和光线的影响，基线方法TensoRF产生的结果具有显著的伪影，严重影响了面部重建。为了解决这个问题，我们提出了TI Face，它分别通过张量辐射场（T-Face）和隐式曲面（I-Face）来改进面部重建。具体来说，我们采用基于SAM的方法来获得前景遮罩，从而过滤掉背景中的强烈照明。此外，我们还设计了基于掩模的约束和稀疏性约束，以有效地消除渲染伪影。实验结果证明了所提出的改进方法的有效性和我们的方法在人脸重建方面的优越性能。代码将在https://github.com/ruijiezhu94/ti-face. et.al.|[2312.09527](http://arxiv.org/abs/2312.09527)|**[link](https://github.com/ruijiezhu94/ti-face)**|

<p align=right>(<a href=#updated-on-20231220>back to top</a>)</p>

## 3D Reconstruction

|Publish Date|Title|Abstract|PDF|Code|
|---|---|---|---|---|
|**2023-12-19**|**pixelSplat: 3D Gaussian Splats from Image Pairs for Scalable Generalizable 3D Reconstruction**|我们介绍了pixelSplat，这是一种前馈模型，它学习从成对的图像中重建由3D高斯基元参数化的3D辐射场。我们的模型具有实时和内存高效的渲染功能，可进行可扩展训练，并在推理时进行快速3D重建。为了克服稀疏和局部支持表示固有的局部极小值，我们预测了三维上的稠密概率分布，并根据该概率分布对高斯均值进行采样。我们通过重新参数化技巧使这种采样操作可微分，允许我们通过高斯飞溅表示反向传播梯度。我们在真实世界的RealEstate10k和ACID数据集上以宽基线新视图合成为基准，在那里我们优于最先进的光场变换器，并将渲染加速2.5个数量级，同时重建可解释和可编辑的3D辐射场。 et.al.|[2312.12337](http://arxiv.org/abs/2312.12337)|null|
|**2023-12-19**|**EVI-SAM: Robust, Real-time, Tightly-coupled Event-Visual-Inertial State Estimation and 3D Dense Mapping**|事件摄像机是受生物启发的运动激活传感器，在处理具有挑战性的情况（如运动模糊和高动态范围）方面表现出巨大的潜力。在本文中，我们提出了EVI-SAM来解决使用单目事件相机进行6自由度姿态跟踪和三维重建的问题。利用特征匹配的鲁棒性和直接对准的精度，设计了一种新的基于事件的混合跟踪框架来估计姿态。具体来说，我们开发了一种基于事件的2D-2D对齐来构建光度约束，并将其与基于事件的重投影约束紧密集成。映射模块通过基于图像引导的事件映射方法来恢复场景的密集和丰富多彩的深度。随后，可以通过使用截断符号距离函数（TSDF）融合来自多个视点的密集深度图来重建3D场景的外观、纹理和表面网格。据我们所知，这是第一个实现基于事件的密集映射的非学习工作。在公开的和自行收集的数据集上进行了数值评估，定性和定量地证明了我们方法的优越性能。我们的EVI-SAM有效地平衡了准确性和稳健性，同时保持了计算效率，在具有挑战性的场景中展示了卓越的姿态跟踪和密集映射性能。视频演示：https://youtu.be/nn40u4e5si8. et.al.|[2312.11911](http://arxiv.org/abs/2312.11911)|null|
|**2023-12-17**|**Primitive-based 3D Human-Object Interaction Modelling and Programming**|在三维环境中嵌入人与关节对象交互（HAOI）是深入理解人类活动的一个重要方向。与以往使用参数化和CAD模型来表示人和物体的工作不同，在这项工作中，我们提出了一种新的基于三维几何图元的语言来对人和物体进行编码。在我们的新范式下，人和物体都是原语的组成部分，而不是异构实体。因此，可以在人类的有限3D数据和不同对象类别之间实现相互信息学习。此外，考虑到表达式的简单性和所包含信息的丰富性，我们选择超二次曲面作为原始表示。为了探索机器的HAOI的有效嵌入，我们在由基元及其图像组成的3D HAOI上建立了一个新的基准，并提出了一项任务，要求机器使用图像中的基元恢复三维HAOI。此外，我们提出了基于HAOI的单视图三维重建的基线。我们相信，这种基于原始的3D HAOI表示将为3D HAOI研究铺平道路。我们的代码和数据可在https://mvig-rhos.com/p3haoi. et.al.|[2312.10714](http://arxiv.org/abs/2312.10714)|null|
|**2023-12-16**|**Triplane Meets Gaussian Splatting: Fast and Generalizable Single-View 3D Reconstruction with Transformers**|生成模型的发展推动了从单个图像进行3D重建的最新进展。其中最突出的是基于分数蒸馏采样（SDS）的方法和3D域中扩散模型的自适应。尽管这些技术取得了进展，但由于优化或渲染过程缓慢，导致训练和优化时间过长，这些技术往往面临限制。在本文中，我们介绍了一种新的单视图重建方法，该方法通过前馈推理从单个图像有效地生成3D模型。我们的方法利用两个基于变换器的网络，即点解码器和三平面解码器，使用混合三平面高斯中间表示来重建3D对象。这种混合表示实现了平衡，与隐式表示相比，实现了更快的渲染速度，同时提供了比显式表示更高的渲染质量。点解码器被设计用于从单个图像生成点云，提供显式表示，然后由三平面解码器使用该显式表示来查询每个点的高斯特征。这种设计选择解决了与直接回归以其非结构性质为特征的显式三维高斯属性相关的挑战。随后，通过MLP对3D高斯进行解码，以实现通过飞溅的快速渲染。这两个解码器都建立在可扩展的、基于转换器的架构上，并在大规模3D数据集上进行了有效的训练。对合成数据集和真实世界图像进行的评估表明，与以前最先进的技术相比，我们的方法不仅实现了更高的质量，而且确保了更快的运行时间。请参阅我们的项目页面https://zouzx.github.io/triplanegaussian/. et.al.|[2312.09147](http://arxiv.org/abs/2312.09147)|null|
|**2023-12-14**|**Living Scenes: Multi-object Relocalization and Reconstruction in Changing 3D Environments**|对动态3D场景理解的研究主要集中在密集观测的短期变化跟踪上，而很少关注稀疏观测的长期变化。我们用MoRE解决了这一差距，MoRE是一种在进化环境中进行多对象重新定位和重建的新方法。我们将这些环境视为“真实场景”，并考虑将在不同时间点进行的扫描转换为对象实例的3D重建的问题，其准确性和完整性会随着时间的推移而提高。我们方法的核心是在合成数据上训练的单个编码器-解码器网络中的SE（3）-等变表示。这种表示使我们能够无缝地处理实例匹配、注册和重建。我们还引入了一种联合优化算法，该算法有助于在不同时间点进行的多次扫描中积累源自同一实例的点云。我们在合成和真实世界的数据上验证了我们的方法，并在端到端性能和单个子任务中展示了最先进的性能。 et.al.|[2312.09138](http://arxiv.org/abs/2312.09138)|null|
|**2023-12-14**|**Learned Fusion: 3D Object Detection using Calibration-Free Transformer Feature Fusion**|使用传感器融合的3D对象检测的现有技术在很大程度上依赖于校准质量，这在实验室环境之外的大规模部署中很难维持。我们提出了第一种用于三维物体检测的无校准方法。因此，消除了对复杂且昂贵的校准程序的需要。我们的方法使用转换器在多个抽象级别上映射不同传感器的多个视图之间的特征。在对物体检测的广泛评估中，我们不仅表明我们的方法在BEV mAP中比单模态设置好14.1%，而且转换器确实学习了映射。通过表明传感器融合不需要校准，我们希望激励其他研究人员遵循无校准融合的方向。此外，由此产生的方法对旋转和平移变化具有相当大的弹性。 et.al.|[2312.09082](http://arxiv.org/abs/2312.09082)|null|
|**2023-12-14**|**Scene 3-D Reconstruction System in Scattering Medium**|随着新模型和扩展的发展，用于新视图合成的神经辐射场研究经历了爆炸式增长。适用于水下场景或散射介质的NERF算法也在不断发展。现有的水下三维重建系统仍然面临训练时间长、渲染效率低等挑战。本文提出了一种改进的水下三维重建系统来解决这些问题，并实现快速、高质量的三维重建。首先，我们增强了单眼相机拍摄的水下视频，以纠正水介质物理特性造成的图像质量差的问题，同时确保相邻帧增强的一致性。随后，我们对视频帧进行关键帧选择，以优化资源利用率，消除动态对象对重建结果的影响。所选关键帧在使用COLMAP进行姿态估计后，使用基于多分辨率哈希编码的神经辐射场进行三维重建改进过程，用于模型构建和渲染。 et.al.|[2312.09005](http://arxiv.org/abs/2312.09005)|null|
|**2023-12-13**|**ProNeRF: Learning Efficient Projection-Aware Ray Sampling for Fine-Grained Implicit Neural Radiance Fields**|神经渲染的最新进展表明，尽管速度较慢，但隐式紧凑模型可以从多个视图中学习场景的几何图形和视图相关外观。为了保持如此小的内存占用，但实现更快的推理时间，最近的工作采用了“采样器”网络，该网络自适应地对隐式神经辐射场中沿每条射线的一小部分点进行采样。尽管这些方法在渲染时间上减少了10美元\倍，但与香草NeRF相比，它们的质量仍有相当大的下降。相反，我们提出了ProNeRF，它在内存占用（类似于NeRF）、速度（比HyperReel快）和质量（比K-Planes好）之间提供了最佳折衷。ProNeRF配备了一种新的投影感知采样（PAS）网络，以及一种用于射线探测和利用的新训练策略，从而实现高效的细粒度粒子采样。我们的ProNeRF产生了最先进的指标，比NeRF快15-23倍，PSNR比NeRF高0.65dB，比已发表的最佳基于采样器的方法HyperReel高0.95dB。我们的探索和开发训练策略使ProNeRF能够学习完整场景的颜色和密度分布，同时学习聚焦于最高密度区域的高效光线采样。我们提供了广泛的实验结果，分别在广泛采用的前向和360数据集LLFF和Blender上支持我们的方法的有效性。 et.al.|[2312.08136](http://arxiv.org/abs/2312.08136)|null|
|**2023-12-13**|**Denoising diffusion-based synthetic generation of three-dimensional (3D) anisotropic microstructures from two-dimensional (2D) micrographs**|集成计算材料工程（ICME）显著增强了对微观结构与材料性能之间关系的系统分析，为高性能材料的发展铺平了道路。然而，由于缺乏三维（3D）微观结构数据集，分析微观结构敏感材料的行为仍然具有挑战性。此外，如果微观结构是各向异性的，这一挑战会被放大，因为这也会导致材料的各向异性。在本文中，我们提出了一种仅基于二维（2D）显微照片使用基于条件扩散的生成模型（DGM）重建各向异性微观结构的框架。所提出的框架涉及多个2D条件DGM的空间连接，每个条件DGM都经过训练以生成三个不同正交平面的2D微观结构样本。连接的多个反向扩散过程使得能够对马尔可夫链进行有效建模，以将噪声转换为3D微观结构样本。此外，采用改进的协调采样来提高样本质量，同时在3D空间中保持各向异性微观结构样本切片之间的空间连接。为了验证所提出的框架，根据空间相关函数和物理材料行为对二维到三维重建的各向异性微观结构样品进行了评估。结果表明，该框架不仅能够再现材料相的统计分布，而且能够再现三维空间中的材料性质。这突出了所提出的二维到三维重建框架在建立微观结构-性能联系方面的潜在应用，这可能有助于未来研究的高通量材料设计 et.al.|[2312.07832](http://arxiv.org/abs/2312.07832)|null|
|**2023-12-12**|**Adaptive Confidence Multi-View Hashing for Multimedia Retrieval**|多视图哈希方法将多个视图中的异构数据转换为二进制哈希码，是多媒体检索的关键技术之一。然而，目前的方法主要探讨多个观点之间的互补性，而缺乏信心学习和融合。此外，在实际应用场景中，单视图数据包含冗余噪声。为了进行置信度学习并消除不必要的噪声，我们提出了一种新的自适应置信度多视图哈希（ACMVH）方法。首先，开发了置信网络来从各种单视图特征中提取有用信息并去除噪声信息。此外，采用自适应置信度多视图网络来测量每个视图的置信度，然后通过加权求和来融合多视图特征。最后，设计了一个扩展网络来进一步增强融合特征的特征表示。据我们所知，我们率先将置信学习应用于多媒体检索领域。在两个公共数据集上进行的大量实验表明，所提出的ACMVH比最先进的方法性能更好（最大增加了3.24%）。源代码可在https://github.com/hackerhyper/acmvh. et.al.|[2312.07327](http://arxiv.org/abs/2312.07327)|**[link](https://github.com/hackerhyper/acmvh)**|

<p align=right>(<a href=#updated-on-20231220>back to top</a>)</p>

## Diffusion

|Publish Date|Title|Abstract|PDF|Code|
|---|---|---|---|---|
|**2023-12-19**|**On Inference Stability for Diffusion Models**|去噪概率模型（DPM）代表了一个新兴的生成模型领域，擅长生成多样化和高质量的图像。然而，目前大多数DPM的训练方法往往忽略了时间步长之间的相关性，限制了模型在有效生成图像方面的性能。值得注意的是，我们从理论上指出，这个问题可能是由预测轨迹和实际轨迹之间的累积估计差距引起的。为了最大限度地减少这一差距，我们提出了一种新的\textit{序列感知}损失，旨在减少估计差距以提高采样质量。此外，我们在理论上表明，与DPM中的传统损失相比，我们提出的损失函数是估计损失的更严格的上界。在包括CIFAR10、CelebA和CelebA-HQ在内的几个基准数据集上的实验结果一致表明，与几个DPM基线相比，我们提出的方法在FID和Inception Score测量的图像泛化质量方面有了显著改进。我们的代码和预先培训的检查点位于\url{https://github.com/viettmab/sa-dpm}。 et.al.|[2312.12431](http://arxiv.org/abs/2312.12431)|**[link](https://github.com/viettmab/sa-dpm)**|
|**2023-12-19**|**SegRefiner: Towards Model-Agnostic Segmentation Refinement with Discrete Diffusion Process**|在本文中，我们探索了一种提高不同分割模型生成的对象掩码质量的主要方法。我们提出了一种称为SegRefiner的模型无关解决方案，该解决方案通过将分割细化解释为数据生成过程，为这个问题提供了一个新的视角。因此，通过一系列去噪扩散步骤，可以顺利地实现细化过程。具体来说，SegRefiner将粗略的掩码作为输入，并使用离散扩散过程对其进行细化。通过预测每个像素的标签和相应的状态转移概率，SegRefiner以条件去噪的方式逐步细化噪声掩模。为了评估SegRefiner的有效性，我们对各种分割任务进行了全面的实验，包括语义分割、实例分割和二分图像分割。结果从多个方面证明了我们的SegRefiner的优越性。首先，它在不同类型的粗掩模上一致地改进了分割度量和边界度量。其次，它显著优于以前的模型无关细化方法。最后，在细化高分辨率图像时，它表现出捕捉极其精细细节的强大能力。源代码和经过训练的模型可在https://github.com/mengyuwang826/segrefiner. et.al.|[2312.12425](http://arxiv.org/abs/2312.12425)|**[link](https://github.com/mengyuwang826/segrefiner)**|
|**2023-12-19**|**Scene-Conditional 3D Object Stylization and Composition**|最近，3D生成模型取得了令人印象深刻的进展，使得能够从文本或图像输入生成几乎任意的3D资产。然而，这些方法在不考虑最终放置对象的场景的情况下孤立地生成对象。在本文中，我们提出了一个框架，该框架允许对现有的3D资产进行风格化，以适应给定的2D场景，并额外生成照片级真实感合成，就好像资产被放置在环境中一样。这不仅为对象样式化打开了一个新的控制级别，例如，可以对相同的资源进行样式化，以反映环境的变化，例如夏天到冬天，或者幻想与未来的设置，还可以使对象场景的组成更加可控。我们通过将建模和优化对象的纹理和环境照明相结合，通过可微分光线跟踪和从预训练的文本到图像扩散模型的图像先验来实现这一点。我们证明了我们的方法适用于各种各样的室内和室外场景以及任意对象。 et.al.|[2312.12419](http://arxiv.org/abs/2312.12419)|null|
|**2023-12-19**|**LASA: Instance Reconstruction from Real Scans using A Large-scale Aligned Shape Annotation Dataset**|从3D场景重建实例形状涉及在语义实例级别恢复多个对象的完整几何形状。由于场景复杂性和显著的室内遮挡的复杂性，许多方法都利用了数据驱动的学习。训练这些方法通常需要一个大规模、高质量的数据集，该数据集具有与真实世界扫描对齐和成对的形状注释。现有的数据集要么是合成的，要么是错位的，这限制了数据驱动方法在真实数据上的性能。为此，我们介绍了LASA，这是一个大规模对齐形状注释数据集，包括10412个高质量的CAD注释，与专业艺术家手动创建的ArkitScenes的920个真实世界场景扫描对齐。在此基础上，我们提出了一种新的基于扩散的跨模态形状重建（DisCo）方法。它通过混合特征聚合设计来融合多模态输入并恢复高保真对象几何图形。此外，我们提出了一种占用引导的3D对象检测（OccGOD）方法，并证明我们的形状注释提供了场景占用线索，可以进一步改进3D对象检测。在LASA的支持下，大量实验表明，我们的方法在实例级场景重建和3D对象检测任务中都达到了最先进的性能。 et.al.|[2312.12418](http://arxiv.org/abs/2312.12418)|null|
|**2023-12-19**|**Prompting Hard or Hardly Prompting: Prompt Inversion for Text-to-Image Diffusion Models**|提供给文本到图像扩散模型的提示的质量决定了生成的内容对用户意图的忠诚度，这通常需要“提示工程”。为了在没有即时工程的情况下利用目标图像中的视觉概念，当前的方法在很大程度上依赖于通过优化嵌入反转，然后将其映射到伪标记。然而，使用这种高维向量表示是具有挑战性的，因为它们缺乏语义和可解释性，并且在使用它们时只允许简单的向量操作。相反，这项工作专注于反转扩散模型，以直接获得可解释的语言提示。这样做的挑战在于这样一个事实，即由此产生的优化问题从根本上是离散的，并且提示的空间呈指数级大；这使得使用标准优化技术（如随机梯度下降）变得困难。为此，我们使用延迟投影方案来优化表示模型中词汇空间的提示。此外，我们利用了扩散过程的不同时间步长满足图像中不同细节水平的发现。前向扩散过程的较晚的、有噪声的时间步长对应于语义信息，因此，在该范围内的提示反转提供了表示图像语义的标记。我们表明，我们的方法可以为目标图像识别语义可解释和有意义的提示，该提示可用于合成具有相似内容的不同图像。我们进一步说明了优化提示在进化图像生成和概念去除中的应用。 et.al.|[2312.12416](http://arxiv.org/abs/2312.12416)|null|
|**2023-12-19**|**Diffusion limited aggregation in the layers model**|在Witten和Sander引入的扩散有限聚集（DLA）经典模型中，该过程从放置在空间原点的单个粒子簇开始，然后，粒子一次一个地从无穷远处随机行走，直到与现有的粒子簇碰撞并粘附。我们在具有指定源和汇顶点的大型但有限的图上考虑这个过程的类似版本。最初，暂停粒子的簇在汇点顶点包含单个粒子。从源一次一个开始，每个粒子在汇点顶点的方向上随机行走。在行走第一次进入簇之前，粒子会停在最后一个未占用的顶点，从而增加簇的大小。这种情况一直持续到源顶点被占用为止，此时过程结束。我们研究了几类分层图的DLA过程，包括具有大分支因子的树，该树的下沉顶点附着在叶子上。我们确定了一类给定图的进程的完成时间，并表明链接源到汇的最终集群的子组件本质上是一条唯一的路径。 et.al.|[2312.12326](http://arxiv.org/abs/2312.12326)|null|
|**2023-12-19**|**Heavy quark momentum broadening in a non-Abelian plasma away from thermal equilibrium**|我们进行了经典的统计实时晶格模拟，以计算在存在强填充非阿贝尔规范场的情况下夸克的实时谱函数和动量加宽。基于一种提取相对论性夸克动量加宽的新方法，我们发现夸克的动量分布表现出有趣的非微扰特征，作为时间的函数，这是由于它从介质接收到相关的动量踢，最终进入扩散状态。我们提取了描述魅力夸克和底夸克的质量范围的动量扩散系数，并发现与重夸克极限有相当大的差异。 et.al.|[2312.12280](http://arxiv.org/abs/2312.12280)|null|
|**2023-12-19**|**Travelling pulses on three spatial scales in a Klausmeier-type vegetation-autotoxicity model**|描述植被和水之间相互作用的反应扩散模型揭示了与现实生活中观察到的结构相对应的几种类型的模式和行波解的出现。通过同时考虑被称为自毒性的生态因素来提高它们的准确性，导致了支持复杂动态模式存在的更多相关模型。在这项工作中，我们在Klausmeier型植被-水自毒性模型中包括了生物量的额外承载能力，这导致了两个渐近小参数的存在： $\varepsilon$，代表植被-水模型中的常见尺度分离，$\delta$，直接与自毒性相关。我们基于涉及$\varepsilon$和$\delta$ 的两种不同标度方案，构建了三种不同类型的同宿行波脉冲解，有和没有所谓的超低平台。小参数的相对排序显著影响脉冲解的构造所依据的相空间几何形状。我们通过对所构建的脉冲解的数值延拓来补充分析，并通过对全PDE模型的直接数值模拟来证明它们的存在性（和稳定性）。 et.al.|[2312.12277](http://arxiv.org/abs/2312.12277)|null|
|**2023-12-19**|**Intrinsic Image Diffusion for Single-view Material Estimation**|我们提出了一种用于室内场景外观分解的生成模型“内在图像扩散”。在给定单个输入视图的情况下，我们采样了多种可能的材料解释，如反照率、粗糙度和金属图。由于光照和材料特性之间固有的模糊性以及缺乏真实的数据集，外观分解在计算机视觉中构成了相当大的挑战。为了解决这个问题，我们提倡一种概率公式，其中我们不试图直接预测真实的材料性质，而是使用条件生成模型从解空间进行采样。此外，我们表明，利用最近在大规模真实世界图像上训练的扩散模型的强学习先验可以适应材料估计，并大大提高对真实图像的泛化能力。我们的方法产生了明显更清晰、更一致、更详细的材料，在PSNR上优于最先进的方法1.5dB $，在反照率预测上优于FID分数45\%$ 。我们通过在合成数据集和真实世界数据集上的实验证明了我们的方法的有效性。 et.al.|[2312.12274](http://arxiv.org/abs/2312.12274)|null|
|**2023-12-19**|**Brush Your Text: Synthesize Any Scene Text on Images via Diffusion Model**|最近，基于扩散的图像生成方法因其卓越的文本到图像生成能力而备受赞誉，同时在准确生成多语言场景文本图像方面仍面临挑战。为了解决这个问题，我们提出了Diff-Text，这是一个适用于任何语言的无训练场景文本生成框架。我们的模型输出一个照片逼真的图像，给定任何语言的文本以及场景的文本描述。该模型利用渲染的草图图像作为先验，从而激发预训练的稳定扩散的潜在多语言生成能力。基于对交叉注意力图对生成图像中对象放置的影响的观察，我们在交叉注意力层中提出了一个局部注意力约束，以解决场景文本的不合理定位问题。此外，我们引入了对比图像级别的提示，以进一步细化文本区域的位置，实现更准确的场景文本生成。实验表明，该方法在文本识别的准确性和前景-背景混合的自然度方面都优于现有方法。 et.al.|[2312.12232](http://arxiv.org/abs/2312.12232)|**[link](https://github.com/ecnuljzhang/brush-your-text)**|

<p align=right>(<a href=#updated-on-20231220>back to top</a>)</p>

## NeRF

|Publish Date|Title|Abstract|PDF|Code|
|---|---|---|---|---|
|**2023-12-16**|**How to Train Neural Field Representations: A Comprehensive Study and Benchmark**|神经场（NeFs）最近已成为一种用于对各种模态（包括图像、形状和场景）的信号进行建模的通用方法。随后，许多工作探索了使用NeF作为下游任务的表示，例如，根据适合的NeF的参数对图像进行分类。然而，NeF超参数对其作为下游表示的质量的影响很少被理解，而且在很大程度上仍未被探索。这在一定程度上是由于拟合神经场数据集所需的大量时间造成的。在这项工作中，我们提出了 $\verb|fit-a-nef|$ ，这是一个基于JAX的库，它利用并行化来实现大规模nef数据集的快速优化，从而显著加快速度。有了这个库，我们进行了一项全面的研究，研究了不同超参数——包括初始化、网络架构和优化策略——对下游任务的NeF拟合的影响。我们的研究为如何训练NeF提供了宝贵的见解，并为优化其在下游应用中的有效性提供了指导。最后，基于所提出的库和我们的分析，我们提出了Neural Field Arena，这是一个由流行视觉数据集的神经场变体组成的基准，包括MNIST、CIFAR、ImageNet和ShapeNetv2的变体。我们的图书馆和神经领域竞技场将是开源的，以引入标准化的基准测试，并促进对神经领域的进一步研究。 et.al.|[2312.10531](http://arxiv.org/abs/2312.10531)|**[link](https://github.com/samuelepapa/fit-a-nef)**|
|**2023-12-18**|**LatentEditor: Text Driven Local Editing of 3D Scenes**|虽然神经领域在视图合成和场景重建方面取得了重大进展，但由于其对来自多视图输入的几何和纹理信息的隐式编码，编辑它们带来了巨大的挑战。在本文中，我们介绍了\textsc｛LatentEditor｝，这是一个创新的框架，旨在让用户能够使用文本提示对神经字段进行精确和本地控制的编辑。利用去噪扩散模型，我们成功地将真实世界的场景嵌入到潜在空间中，与传统方法相比，产生了更快、更具适应性的NeRF主干进行编辑。为了提高编辑精度，我们引入了一个delta分数来计算潜在空间中的2D掩模，该分数可以作为局部修改的指南，同时保留不相关的区域。我们新颖的像素级评分方法利用InstructPix2Pix（IP2P）的能力来辨别潜在空间中IP2P条件和无条件噪声预测之间的差异。然后在训练集中迭代地更新以2D掩码为条件的编辑的潜伏时间，以实现3D局部编辑。与现有的3D编辑模型相比，我们的方法实现了更快的编辑速度和卓越的输出质量，弥合了文本指令和潜在空间中高质量3D场景编辑之间的差距。我们在LLFF、IN2N、NeRFStudio和NeRFArt四个基准3D数据集上展示了我们的方法的优势。 et.al.|[2312.09313](http://arxiv.org/abs/2312.09313)|**[link](https://github.com/umarkhalidAI/LatentEditor)**|
|**2023-12-14**|**ZeroRF: Fast Sparse View 360° Reconstruction with Zero Pretraining**|我们提出了ZeroRF，这是一种新的每场景优化方法，解决了神经场表示中稀疏视图360重建的挑战。目前的突破，如神经辐射场（NeRF）已经证明了高保真度的图像合成，但难以处理稀疏的输入视图。现有的方法，如可泛化的NeRF和每场景优化方法，在数据依赖性、计算成本和跨不同场景的泛化方面面临限制。为了克服这些挑战，我们提出了ZeroRF，其关键思想是将定制的深度图像先验集成到因子分解的NeRF表示中。与传统方法不同，ZeroRF使用神经网络生成器对特征网格进行参数化，从而实现高效的稀疏视图360重建，而无需任何预训练或额外的正则化。大量实验展示了ZeroRF在质量和速度方面的多功能性和优势，在基准数据集上取得了最先进的结果。ZeroRF的意义延伸到3D内容生成和编辑的应用。项目页面：https://sarahweiii.github.io/zerorf/ et.al.|[2312.09249](http://arxiv.org/abs/2312.09249)|null|
|**2023-12-12**|**SMERF: Streamable Memory Efficient Radiance Fields for Real-Time Large-Scene Exploration**|最近的实时视图合成技术在保真度和速度上迅速进步，现代方法能够以交互式帧速率渲染接近照片级真实感的场景。与此同时，在易于光栅化的显式场景表示和基于射线行进的神经场之间出现了紧张关系，后者的最先进实例在质量上超过了前者，同时对于实时应用来说成本高得令人望而却步。在这项工作中，我们介绍了SMERF，这是一种视图合成方法，在占地面积高达3亿 $^2$、体积分辨率为3.5毫米$^3$ 的大型场景中，它实现了实时方法中最先进的精度。我们的方法建立在两个主要贡献之上：一个是分层模型划分方案，它在限制计算和内存消耗的同时增加了模型容量，另一个是蒸馏训练策略，它同时产生高保真度和内部一致性。我们的方法能够在网络浏览器中实现全六自由度（6DOF）导航，并在商品智能手机和笔记本电脑上实时渲染。大量实验表明，我们的方法在实时新视图合成方面，在标准基准上超过了当前最先进的0.78 dB，在大型场景上超过了1.78 dB，渲染帧的速度比最先进的辐射场模型快三个数量级，并在包括智能手机在内的各种商品设备上实现了实时性能。我们鼓励读者在我们的项目网站上亲自探索这些模型：https://smerf-3d.github.io. et.al.|[2312.07541](http://arxiv.org/abs/2312.07541)|null|
|**2023-12-09**|**Robo360: A 3D Omnispective Multi-Material Robotic Manipulation Dataset**|长期以来，制造能够自动化劳动密集型任务的机器人一直是计算机视觉和机器人界进步的核心动力。最近人们对利用3D算法，特别是神经领域的兴趣，导致了机器人在操作场景中的感知和物理理解方面的进步。然而，现实世界的复杂性带来了重大挑战。为了应对这些挑战，我们提出了Robo360，这是一个以机器人操作为特征的数据集，具有密集的视图覆盖范围，能够实现高质量的3D神经表示学习，以及一组具有各种物理和光学特性的不同对象，有助于各种对象操作和物理世界建模任务的研究。我们使用现有的动态NeRF来确认我们的数据集的有效性，并评估其在学习多视图策略方面的潜力。我们希望Robo360能够在理解3D物理世界和机器人控制的交叉点上开辟新的研究方向。 et.al.|[2312.06686](http://arxiv.org/abs/2312.06686)|null|
|**2023-12-11**|**Representing stimulus motion with waves in adaptive neural fields**|神经活动的行波在皮层网络中自发出现，并对刺激做出反应。波的时空结构可以指示它们编码的信息以及维持它们的生理过程。在这里，我们研究了作为视觉运动处理模型的自适应神经场中出现的行波的刺激响应关系。神经场方程将皮层组织的活动建模为连续的可兴奋介质，自适应过程提供负反馈，产生局部活动模式。在我们的模型中，突触连接由一个积分核来描述，该积分核由于依赖于活动的突触抑制而动态减弱，导致边缘稳定的行进前沿（具有衰减的后部）或固定速度的脉冲。我们的分析量化了弱刺激如何随着时间的推移改变这些波的相对位置，其特征是我们扰动地获得的波响应函数。持续和连续可见的刺激模拟移动的视觉对象。在视觉空间中跳跃的间歇性闪光可以产生流畅的视觉运动体验。我们的理论和数值模拟很好地描述了波对两种运动刺激的夹带，提供了视觉运动感知的机制描述。 et.al.|[2312.06100](http://arxiv.org/abs/2312.06100)|null|
|**2023-12-10**|**Accurate Differential Operators for Hybrid Neural Fields**|神经场已广泛应用于从形状表示到神经渲染以及求解偏微分方程（PDE）的各个领域。随着混合神经场表示的出现，如利用小MLP和显式表示的即时NGP，这些模型训练迅速，可以适应大型场景。然而，在渲染和模拟等许多应用中，混合神经场可能会导致明显且不合理的伪影。这是因为它们不能产生这些下游应用所需的精确的空间导数。在这项工作中，我们提出了两种规避这些挑战的方法。我们的第一种方法是一种事后算子，它使用局部多项式拟合从预先训练的混合神经场中获得更准确的导数。此外，我们还提出了一种自监督微调方法，该方法在保留初始信号的同时，对神经场进行细化，以直接产生准确的导数。我们展示了我们的方法在渲染、碰撞模拟和求解偏微分方程中的应用。我们观察到，使用我们的方法可以产生更准确的导数，减少伪影，并在下游应用中实现更准确的模拟。 et.al.|[2312.05984](http://arxiv.org/abs/2312.05984)|null|
|**2023-12-11**|**Nuvo: Neural UV Mapping for Unruly 3D Representations**|现有的UV映射算法被设计为在性能良好的网格上操作，而不是由最先进的3D重建和生成技术产生的几何表示。因此，将这些方法应用于由神经辐射场和相关技术（或从这些场三角化的网格）恢复的体积密度会导致纹理图谱过于分散，无法用于视图合成或外观编辑等任务。我们提出了一种UV映射方法，旨在对通过3D重建和生成技术产生的几何体进行操作。我们的方法Nuvo不是计算在网格顶点上定义的映射，而是使用神经场来表示连续的UV映射，并将其优化为仅针对一组可见点（即仅影响场景外观的点）的有效且性能良好的映射。我们展示了我们的模型对不良几何体带来的挑战是稳健的，并且它生成了可以表示详细外观的可编辑UV映射。 et.al.|[2312.05283](http://arxiv.org/abs/2312.05283)|null|
|**2023-12-08**|**Dynamic LiDAR Re-simulation using Compositional Neural Fields**|我们介绍了DyNFL，这是一种新的基于神经场的方法，用于动态驾驶场景中激光雷达扫描的高保真度重新模拟。DyNFL处理来自动态环境的激光雷达测量，并伴随着移动物体的边界框，以构建可编辑的神经场。该字段包括单独重建的静态背景和动态对象，允许用户在重新模拟的场景中修改视点、调整对象位置以及无缝添加或删除对象。我们方法的一个关键创新是神经场合成技术，该技术通过光线下降测试有效地集成了来自各种场景的重建神经资产，考虑到了遮挡和透明表面。我们对合成和真实世界环境的评估表明，\ShortName大大改进了基于激光雷达扫描的动态场景模拟，提供了物理保真度和灵活编辑功能的组合。 et.al.|[2312.05247](http://arxiv.org/abs/2312.05247)|null|
|**2023-12-08**|**TriHuman : A Real-time and Controllable Tri-plane Representation for Detailed Human Geometry and Appearance Synthesis**|仅从视频数据中创建可控、逼真和几何细节的真人数字替身是计算机图形学和视觉领域的一个关键挑战，尤其是在需要实时性能的情况下。最近的方法将神经辐射场（NeRF）连接到关节结构，例如身体模型或骨骼，以将点映射到姿势规范空间中，同时将NeRF调节在骨骼姿势上。这些方法通常使用多层感知器（MLP）对神经场进行参数化，导致运行时间缓慢。为了解决这一缺点，我们提出了一种新的人体定制、可变形和高效的三平面表示TriHuman，它实现了实时性能、最先进的姿态可控几何合成以及逼真的渲染质量。在核心，我们将全局光线样本非刚性地扭曲到未变形的三平面纹理空间中，这有效地解决了全局点映射到相同三平面位置的问题。然后，我们展示了如何将这种三平面特征表示以骨骼运动为条件，以考虑动态外观和几何结构的变化。我们的研究结果表明，在人类的几何形状和外观建模以及运行时性能方面，朝着更高质量迈出了明确的一步。 et.al.|[2312.05161](http://arxiv.org/abs/2312.05161)|null|

<p align=right>(<a href=#updated-on-20231220>back to top</a>)</p>

[contributors-shield]: https://img.shields.io/github/contributors/Vincentqyw/cv-arxiv-daily.svg?style=for-the-badge
[contributors-url]: https://github.com/Vincentqyw/cv-arxiv-daily/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/Vincentqyw/cv-arxiv-daily.svg?style=for-the-badge
[forks-url]: https://github.com/Vincentqyw/cv-arxiv-daily/network/members
[stars-shield]: https://img.shields.io/github/stars/Vincentqyw/cv-arxiv-daily.svg?style=for-the-badge
[stars-url]: https://github.com/Vincentqyw/cv-arxiv-daily/stargazers
[issues-shield]: https://img.shields.io/github/issues/Vincentqyw/cv-arxiv-daily.svg?style=for-the-badge
[issues-url]: https://github.com/Vincentqyw/cv-arxiv-daily/issues

