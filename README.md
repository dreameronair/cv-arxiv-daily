[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]

## Updated on 2023.12.05
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
|**2023-12-04**|**GPS-Gaussian: Generalizable Pixel-wise 3D Gaussian Splatting for Real-time Human Novel View Synthesis**|我们提出了一种新的方法，称为GPS高斯，用于实时合成角色的新视图。所提出的方法能够在稀疏视图相机设置下实现2K分辨率的渲染。与需要按主题优化的原始高斯飞溅或神经隐式渲染方法不同，我们引入了在源视图上定义的高斯参数图，并直接回归高斯飞溅特性，用于即时新视图合成，而无需任何微调或优化。为此，我们在大量人体扫描数据上训练我们的高斯参数回归模块，并与深度估计模块一起将2D参数图提升到3D空间。所提出的框架是完全可微分的，在几个数据集上的实验表明，我们的方法优于最先进的方法，同时实现了超高的渲染速度。 et.al.|[2312.02155](http://arxiv.org/abs/2312.02155)|null|
|**2023-12-04**|**Fast View Synthesis of Casual Videos**|由于场景动力学和缺乏视差等挑战，从野外视频中合成新颖的视图是困难的。虽然现有的方法在隐式神经辐射场方面显示出了有希望的结果，但它们的训练和渲染速度很慢。本文重新审视了显式视频表示，以有效地从单目视频中合成高质量的新颖视图。我们分别处理静态和动态视频内容。具体来说，我们使用基于扩展平面的场景表示来构建全局静态场景模型，以合成时间相干的新颖视频。我们的基于平面的场景表示通过球面谐波和位移图来增强，以捕捉与视图相关的效果并对非平面复杂曲面几何体进行建模。为了提高效率，我们选择按帧点云来表示动态内容。虽然这种表示容易出现不一致，但由于运动，轻微的时间不一致在感知上被掩盖了。我们开发了一种快速估计这种混合视频表示并实时渲染新视图的方法。我们的实验表明，我们的方法可以从野外视频中渲染高质量的新视图，其质量与最先进的方法相当，同时在训练和实时渲染方面速度快100倍。 et.al.|[2312.02135](http://arxiv.org/abs/2312.02135)|null|
|**2023-12-04**|**SplaTAM: Splat, Track & Map 3D Gaussians for Dense RGB-D SLAM**|密集同时定位和映射（SLAM）对于具体场景的理解至关重要。最近的工作表明，3D高斯可以使用多个姿势的相机进行高质量的场景重建和实时渲染。在这种情况下，我们首次展示了通过3D高斯表示场景可以使用单个非聚焦单目RGB-D相机实现密集SLAM。我们的方法SplaTAM解决了先前基于辐射场的表示的局限性，包括快速渲染和优化、确定区域是否先前已映射的能力，以及通过添加更多高斯来进行结构化地图扩展。我们使用在线跟踪和映射管道，同时对其进行剪裁，以专门使用底层高斯表示和轮廓引导的优化，通过可微分渲染进行优化。大量实验表明，SplaTAM在相机姿态估计、地图构建和新颖视图合成方面实现了高达两倍的最先进性能，证明了其优于现有方法，同时允许实时渲染高分辨率密集3D地图。 et.al.|[2312.02126](http://arxiv.org/abs/2312.02126)|null|
|**2023-12-04**|**ColonNeRF: Neural Radiance Fields for High-Fidelity Long-Sequence Colonoscopy Reconstruction**|结肠镜重建是诊断结直肠癌的关键。然而，准确的长序列结肠镜重建面临三个主要挑战：（1）由于结肠弯曲和卷曲的形状，结肠各段之间存在差异；（2） 简单和复杂折叠的几何结构的共存；（3） 由于受约束的相机轨迹而导致的稀疏视点。为了应对这些挑战，我们引入了一种新的基于神经辐射场（NeRF）的重建框架，名为ColonNeRF，它利用神经渲染进行长序列结肠镜检查的新视图合成。具体来说，为了以分段的方式重建整个结肠，我们的ColonNeRF引入了一个区域划分和集成模块，有效地减少了形状的差异，并确保了每个片段的几何一致性。为了在一个统一的框架中学习简单和复杂的几何结构，我们的ColonNeRF集成了一个多层次融合模块，该模块从简单到困难逐步对结肠区域进行建模。此外，为了克服稀疏视图带来的挑战，我们设计了一个DensiNet模块，用于在语义一致性的指导下加密相机姿势。我们在合成数据集和真实世界数据集上进行了广泛的实验，以评估我们的ColonNeRF。从数量上讲，我们的ColonNeRF在两个基准和四个评估指标上优于现有方法。值得注意的是，在SimCol-to-3D数据集上，我们的LPIPS-ALEX分数显著增加了约67%-85%。从质量上讲，我们的重建可视化显示了更清晰的纹理和更准确的几何细节。这些充分证明了我们优于最先进方法的优越性能。 et.al.|[2312.02015](http://arxiv.org/abs/2312.02015)|null|
|**2023-12-04**|**GaussianHead: Impressive 3D Gaussian-based Head Avatars with Dynamic Hybrid Neural Field**|以前的头部化身方法大多依赖于固定的显式基元（网格、点）或隐式曲面（符号距离函数）和体积神经辐射场，难以在高保真度、训练速度和资源消耗之间取得平衡。混合场最近的流行带来了新的表示，但受到通过固定映射获得的参数化因子的限制。我们提出了GaussianHead：一种基于各向异性三维高斯基元的头部化身算法。我们利用规范高斯来表示动态场景。使用显式“动态”三平面作为参数化头部几何的有效容器，与底层几何和三平面中的因子很好地对齐，我们获得了正则高斯的对齐正则因子。利用微小的MLP，因子被解码为3D高斯基元的不透明度和球面谐波系数。最后，我们使用高效的可微高斯光栅化器进行渲染。我们的方法显著受益于我们基于3D高斯的新表示，并且三平面中底层几何结构和因子的适当对齐变换消除了固定映射引入的偏差。与最先进的技术相比，我们在自我重建、新视图合成和跨身份再现等任务中实现了最佳的视觉效果，同时保持了高渲染效率（每帧0.12秒）。在某些情况下，甚至鼻子周围的毛孔也清晰可见。代码和其他视频可以在项目主页上找到。 et.al.|[2312.01632](http://arxiv.org/abs/2312.01632)|null|
|**2023-12-03**|**SANeRF-HQ: Segment Anything for NeRF in High Quality**|最近，Segment Anything Model（SAM）展示了零样本分割的显著能力，而NeRF（Neural Radiance Fields）作为一种解决新视图合成之外的各种3D问题的方法而广受欢迎。尽管最初尝试将这两种方法结合到3D分割中，但它们面临着在复杂场景中准确、一致地分割对象的挑战。在本文中，我们介绍了高质量NeRF的任何分割（SANeRF-HQ），以实现给定场景中任何对象的高质量3D分割。SANeRF HQ利用SAM在用户提供的提示的指导下进行开放世界对象分割，同时利用NeRF从不同角度聚合信息。为了克服上述挑战，我们在聚合过程中使用密度场和RGB相似性来提高分割边界的准确性。强调分割的准确性，我们在多个NeRF数据集上定量评估我们的方法，在这些数据集上可以获得或手动注释高质量的基本事实。SANeRF HQ在NeRF对象分割方面比以前最先进的方法有了显著的质量改进，为对象定位提供了更高的灵活性，并实现了跨多个视图的更一致的对象分割。其他信息可在https://lyclyc52.github.io/sanerf-hq/. et.al.|[2312.01531](http://arxiv.org/abs/2312.01531)|null|
|**2023-12-03**|**ViVid-1-to-3: Novel View Synthesis with Video Diffusion Models**|从单个图像生成对象的新颖视图是一项具有挑战性的任务。它需要从图像中了解对象的基本3D结构，并呈现高质量、空间一致的新视图。尽管最近基于扩散的视图合成方法已经显示出巨大的进步，但实现各种视图估计之间的一致性，同时遵守所需的相机姿态，仍然是一个有待解决的关键问题。在这项工作中，我们展示了一种非常简单的方法，即使用预先训练的视频扩散模型来解决这个问题。我们的关键想法是，合成一个新的视图可以重新表述为合成一个摄像机在感兴趣的物体周围移动的视频——一个扫描视频——这使我们能够利用视频扩散模型所学到的强大先验。因此，为了执行新颖的视图合成，我们创建了到我们希望渲染的目标视图的平滑相机轨迹，并使用视图条件扩散模型和视频扩散模型进行去噪。通过这样做，我们获得了高度一致的新视图合成，优于现有技术。 et.al.|[2312.01305](http://arxiv.org/abs/2312.01305)|null|
|**2023-12-02**|**Self-Evolving Neural Radiance Fields**|近年来，神经辐射场（NeRF）在新的视图合成和三维重建中表现出了显著的性能。然而，它仍然需要大量高质量的图像，这限制了它在现实世界场景中的适用性。为了克服这一限制，最近的工作集中在通过提供额外的正则化（通常称为少镜头NeRF）仅使用稀疏视点来训练NeRF。我们观察到，由于任务的欠约束性质，仅使用额外的正则化不足以防止模型过拟合到稀疏视点。在本文中，我们提出了一个新的框架，称为自进化神经辐射场（SE NeRF），将自训练框架应用于NeRF来解决这些问题。我们将少镜头NeRF公式化为师生框架，通过用教师生成的额外伪标签训练学生，引导网络学习更稳健的场景表示。通过使用我们新的可靠性估计方法获得的可靠和不可靠射线的不同蒸馏方案来蒸馏射线级伪标签，我们使NeRF能够学习3D场景的更准确和稳健的几何结构。我们展示并评估了将我们的自训练框架应用于现有模型可以提高渲染图像的质量，并在多种设置中实现最先进的性能。 et.al.|[2312.01003](http://arxiv.org/abs/2312.01003)|null|
|**2023-12-01**|**Gaussian Grouping: Segment and Edit Anything in 3D Scenes**|最近的Gaussian Splatting实现了3D场景的高质量实时新颖视图合成。然而，它只专注于外观和几何建模，而缺乏细粒度的对象级场景理解。为了解决这个问题，我们提出了高斯分组，它扩展了高斯飞溅，以联合重建和分割开放世界3D场景中的任何内容。我们用紧凑的身份编码来增强每个高斯，允许高斯根据其在3D场景中的对象实例或物质成员身份进行分组。我们没有求助于昂贵的3D标签，而是通过利用SAM的2D掩模预测以及引入的3D空间一致性正则化，在可微分渲染期间监督身份编码。与隐式NeRF表示相比，我们表明离散和分组的3D高斯可以以高视觉质量、细粒度和效率重建、分割和编辑3D中的任何内容。在高斯分组的基础上，我们进一步提出了一种局部高斯编辑方案，该方案在多功能场景编辑应用中显示了有效性，包括3D对象去除、修复、着色和场景重组。我们的代码和模型将在https://github.com/lkeab/gaussian-grouping. et.al.|[2312.00732](http://arxiv.org/abs/2312.00732)|**[link](https://github.com/lkeab/gaussian-grouping)**|
|**2023-12-01**|**EvE: Exploiting Generative Priors for Radiance Field Enrichment**|从野外不受约束的图像采集中建模大规模场景已被证明是计算机视觉的一大挑战。现有的处理野生神经渲染的方法在封闭世界环境中运行，其中知识仅限于训练集中场景的捕获图像。我们提出了EvE，据我们所知，这是第一种利用生成先验来改进野生场景建模的方法。我们使用预先训练的生成网络来用外部知识丰富K-Plane表示。为此，我们定义了一个交替训练程序，以对在训练集上训练的K-Planes进行优化指导。我们进行了广泛的实验，并在合成数据和真实的旅游照片集上验证了我们的方法的优点。EvE以更丰富的细节增强渲染场景，并在野外新颖的视图合成任务上优于现有技术。我们的项目页面可以在https://eve-nvs.github.io。 et.al.|[2312.00639](http://arxiv.org/abs/2312.00639)|null|

<p align=right>(<a href=#updated-on-20231205>back to top</a>)</p>

## 3D Reconstruction

|Publish Date|Title|Abstract|PDF|Code|
|---|---|---|---|---|
|**2023-12-04**|**Steerers: A framework for rotation equivariant keypoint descriptors**|在视点的大变化上具有判别性和可匹配性的图像关键点描述对于3D重建至关重要。然而，由学习的描述符输出的描述通常对相机旋转不具有鲁棒性。虽然它们可以通过例如数据增强而变得更健壮，但这会降低直立图像的性能。另一种方法是增加测试时间，这会显著增加运行时间。相反，我们在描述空间中学习对输入图像的旋转进行编码的线性变换。我们称这种线性变换为转向器，因为它允许我们像旋转图像一样变换描述。根据表示理论，我们知道了旋转群的所有可能的转向器。转向器可以优化（A）给定固定描述符，（B）与描述符联合，或者（C）我们可以优化给定固定转向器的描述符。我们在所有这三种设置中进行了实验，并在旋转不变图像匹配基准AIMS和Roto-360上获得了最先进的结果。我们在github.com/georg-bn/rotation-steelers上发布代码和模型权重。 et.al.|[2312.02152](http://arxiv.org/abs/2312.02152)|**[link](https://github.com/georg-bn/rotation-steerers)**|
|**2023-12-04**|**iMatching: Imperative Correspondence Learning**|学习特征对应关系是计算机视觉的一项基础任务，对视觉里程计和三维重建等下游应用具有极其重要的意义。尽管最近在数据驱动模型方面取得了进展，但由于缺乏准确的每像素对应标签，特征对应学习仍然受到限制。为了克服这一困难，我们引入了一种新的自监督方案，即命令式学习（IL），用于训练特征对应关系。它可以在没有任何相机姿势或深度标签的情况下，在任意不间断的视频上进行函授学习，预示着自我监督函授学习的新时代。具体来说，我们将对应学习问题公式化为双层优化，将束调整的重投影误差作为模型的监督信号。为了避免大的内存和计算开销，我们利用驻点通过束调整有效地反向传播隐式梯度。通过广泛的实验，我们在包括特征匹配和姿态估计在内的任务上表现出了卓越的性能，在这些任务中，我们获得了比最先进的匹配模型平均30%的精度增益。 et.al.|[2312.02141](http://arxiv.org/abs/2312.02141)|null|
|**2023-12-04**|**Light Field Imaging in the Restrictive Object Space based on Flexible Angular Plane**|在一些应用中，光场成像系统的对象空间是有限的，例如工业和医疗内窥镜。如果传统的光场成像系统直接用于限制性物体空间（ROS），但没有任何具体考虑，ROS将导致严重的微透镜图像失真，进而影响光场解码、校准和3D重建。限制性物体空间中的光场成像是复杂而重要的。在本文中，我们首先推导出微透镜图像偏移的原因是角平面的位置变化，然后我们提出了ROS-LF的柔性角平面，而在传统的光场中，角平面总是与主透镜平面重合。随后，我们提出了ROS-LF的微透镜图像无失真原理，并介绍了ROS-LF的成像原理。我们证明了ROS-LF和传统光场成像模型之间的差异是孔径常数项。最后，我们设计了一个ROS-LF模拟系统，并对其进行了校准，以验证本文提出的原理。 et.al.|[2312.01761](http://arxiv.org/abs/2312.01761)|null|
|**2023-12-03**|**SANeRF-HQ: Segment Anything for NeRF in High Quality**|最近，Segment Anything Model（SAM）展示了零样本分割的显著能力，而NeRF（Neural Radiance Fields）作为一种解决新视图合成之外的各种3D问题的方法而广受欢迎。尽管最初尝试将这两种方法结合到3D分割中，但它们面临着在复杂场景中准确、一致地分割对象的挑战。在本文中，我们介绍了高质量NeRF的任何分割（SANeRF-HQ），以实现给定场景中任何对象的高质量3D分割。SANeRF HQ利用SAM在用户提供的提示的指导下进行开放世界对象分割，同时利用NeRF从不同角度聚合信息。为了克服上述挑战，我们在聚合过程中使用密度场和RGB相似性来提高分割边界的准确性。强调分割的准确性，我们在多个NeRF数据集上定量评估我们的方法，在这些数据集上可以获得或手动注释高质量的基本事实。SANeRF HQ在NeRF对象分割方面比以前最先进的方法有了显著的质量改进，为对象定位提供了更高的灵活性，并实现了跨多个视图的更一致的对象分割。其他信息可在https://lyclyc52.github.io/sanerf-hq/. et.al.|[2312.01531](http://arxiv.org/abs/2312.01531)|null|
|**2023-12-02**|**RNb-NeuS: Reflectance and Normal-based Multi-View 3D Reconstruction**|本文介绍了一种用于集成通过光度立体获得的多视图反射率和法线图的通用范式。我们的方法采用了反射率和法线的逐像素联合重新参数化，将它们视为在模拟的变化照明下渲染的弧度向量。这种重新参数化实现了反射图和法线图作为输入数据在基于神经体积渲染的3D重建中的无缝集成，同时保留了单个优化目标。相比之下，最近的多视图光度立体（MVPS）方法依赖于多个潜在冲突的目标。尽管我们提出的方法明显简单，但在F分数、倒角距离和平均角误差度量方面，它在MVPS基准测试中优于最先进的方法。值得注意的是，它显著改善了高曲率或低可见性区域的详细3D重建。 et.al.|[2312.01215](http://arxiv.org/abs/2312.01215)|null|
|**2023-12-02**|**Self-Evolving Neural Radiance Fields**|近年来，神经辐射场（NeRF）在新的视图合成和三维重建中表现出了显著的性能。然而，它仍然需要大量高质量的图像，这限制了它在现实世界场景中的适用性。为了克服这一限制，最近的工作集中在通过提供额外的正则化（通常称为少镜头NeRF）仅使用稀疏视点来训练NeRF。我们观察到，由于任务的欠约束性质，仅使用额外的正则化不足以防止模型过拟合到稀疏视点。在本文中，我们提出了一个新的框架，称为自进化神经辐射场（SE NeRF），将自训练框架应用于NeRF来解决这些问题。我们将少镜头NeRF公式化为师生框架，通过用教师生成的额外伪标签训练学生，引导网络学习更稳健的场景表示。通过使用我们新的可靠性估计方法获得的可靠和不可靠射线的不同蒸馏方案来蒸馏射线级伪标签，我们使NeRF能够学习3D场景的更准确和稳健的几何结构。我们展示并评估了将我们的自训练框架应用于现有模型可以提高渲染图像的质量，并在多种设置中实现最先进的性能。 et.al.|[2312.01003](http://arxiv.org/abs/2312.01003)|null|
|**2023-12-01**|**NeuSG: Neural Implicit Surface Reconstruction with 3D Gaussian Splatting Guidance**|现有的神经隐式表面重建方法通过利用诸如深度图或点云之类的显式几何先验作为正则化，在多视图3D重建中取得了令人印象深刻的性能。然而，由于过度平滑的深度图或稀疏的点云，重建结果仍然缺乏精细的细节。在这项工作中，我们提出了一种在三维高斯散射的指导下进行神经隐式表面重建的管道，以恢复高度详细的表面。三维高斯散射的优点是可以生成具有详细结构的密集点云。尽管如此，天真地采用3D高斯飞溅可能会失败，因为生成的点是不一定位于表面上的3D高斯的中心。因此，我们引入了一种尺度正则化子，通过强制3D高斯极薄来将中心拉向表面。此外，我们建议使用神经隐式模型预测的曲面的法线先验，而不是使用固定的点集作为指导，来细化3D高斯散射中的点云。因此，通过更精确的3D高斯飞溅的引导，表面重建的质量得以提高。通过联合优化3D高斯飞溅和神经隐式模型，我们的方法从这两种表示中受益，并生成具有复杂细节的完整曲面。在坦克和寺庙上的实验验证了我们提出的方法的有效性。 et.al.|[2312.00846](http://arxiv.org/abs/2312.00846)|null|
|**2023-12-01**|**UAVs and Birds: Enhancing Short-Range Navigation through Budgerigar Flight Studies**|这项研究深入研究了布吉鸟的飞行行为，以深入了解它们的飞行轨迹和运动。利用立体摄像机记录的三维重建，我们仔细检查了起飞、飞行和着陆三个飞行运动过程中的速度和加速度模式。这些发现不仅有助于我们理解鸟类的行为，而且对无人机算法的发展具有重要意义。这项研究旨在弥合在鸟类身上观察到的生物学原理与这些见解在开发更高效、更自主的无人机方面的应用之间的差距。在无人机使用日益增多的背景下，本研究重点关注从鸟类行为中汲取的生物学启发原理，特别是在起飞、飞行和着陆飞行过程中，以增强无人机的能力。为这项研究创建的数据集揭示了布吉鸟的起飞、飞行和着陆技术，强调了它们在不同情况和表面上控制速度的能力。这项研究强调了将这些原理纳入无人机算法的潜力，以应对与短程导航、起飞、飞行和着陆相关的挑战。 et.al.|[2312.00597](http://arxiv.org/abs/2312.00597)|null|
|**2023-12-01**|**MultiView Independent Component Analysis with Delays**|线性独立分量分析（ICA）是一种盲源分离技术，已在各个领域用于从观测信号中识别独立的潜在源。为了获得更高的信噪比，可以使用相同源的多个视图的存在。在这项工作中，我们提出了具有延迟的多视图独立分量分析（MVICAD）。该算法建立在多视图ICA模型的基础上，允许源是某些共享源的延迟版本：源在视图之间共享，直到一些特定于视图和源的未知延迟。通过模拟，我们证明了MVICAD可以更好地分解源。此外，由于ICA经常用于神经科学，我们表明，当应用于大规模脑磁图（MEG）数据集Cam CAN时，潜伏期与年龄有关。这些结果表明，MVICAD模型可以在没有人类监督的情况下揭示对神经信号的丰富影响。 et.al.|[2312.00484](http://arxiv.org/abs/2312.00484)|null|
|**2023-12-01**|**Towards Aligned Canonical Correlation Analysis: Preliminary Formulation and Proof-of-Concept Results**|规范相关分析（CCA）已被广泛应用于将数据的多个视图联合嵌入到最大相关的潜在空间中。然而，传统方法所要求的各种数据视角之间的一致性在许多实际情况下并不明确。在这项工作中，我们提出了一个新的框架——对齐规范相关分析（ACCA），通过迭代求解对齐和多视图嵌入来应对这一挑战。 et.al.|[2312.00296](http://arxiv.org/abs/2312.00296)|null|

<p align=right>(<a href=#updated-on-20231205>back to top</a>)</p>

## Diffusion

|Publish Date|Title|Abstract|PDF|Code|
|---|---|---|---|---|
|**2023-12-04**|**Latent Feature-Guided Diffusion Models for Shadow Removal**|由于难以从阴影图像中推断出无阴影场景，因此在阴影下恢复纹理仍然是一个具有挑战性的问题。在本文中，我们建议使用扩散模型，因为它们提供了一种很有前途的方法，可以在扩散过程中逐步细化阴影区域的细节。我们的方法通过以继承无阴影图像特征的学习潜在特征空间为条件来改进这一过程，从而避免了仅以退化图像为条件的传统方法的局限性。此外，我们建议通过将噪声特征与扩散网络融合来缓解训练过程中的潜在局部最优。我们在AISTD数据集上证明了我们的方法的有效性，该方法在RMSE方面比之前的最佳方法高出13%。此外，我们探索了实例级阴影去除，在DESOBA数据集上，我们的模型在RMSE方面比以前的最佳方法高出82%。 et.al.|[2312.02156](http://arxiv.org/abs/2312.02156)|null|
|**2023-12-04**|**Readout Guidance: Learning Control from Diffusion Features**|我们提出了Readout Guidance，这是一种用学习信号控制文本到图像扩散模型的方法。Readout Guidance使用读出头，这是一种经过训练的轻量级网络，可以在每个时间步长从预先训练的冻结扩散模型的特征中提取信号。这些读数可以对单个图像属性进行编码，例如姿势、深度和边缘；或者诸如对应性和外观相似性之类的与多个图像相关的更高阶特性。此外，通过将读出估计值与用户定义的目标进行比较，并通过读出头反向传播梯度，这些估计值可用于指导采样过程。与现有的条件生成方法相比，Readout Guidance所需的添加参数和训练样本要少得多，并且提供了一个方便简单的方法，可以在单一的框架下，通过单一的架构和采样程序，再现不同形式的条件控制。我们在基于拖动的操纵、身份一致生成和空间对齐控制的应用中展示了这些优势。项目页面：https://readout-guidance.github.io. et.al.|[2312.02150](http://arxiv.org/abs/2312.02150)|null|
|**2023-12-04**|**Generative Powers of Ten**|我们提出了一种方法，该方法使用文本到图像模型在多个图像尺度上生成一致的内容，从而实现对场景的极端语义缩放，例如，从森林的广角景观视图到坐在树枝上的昆虫的微距镜头。我们通过联合多尺度扩散采样方法实现了这一点，该方法鼓励不同尺度的一致性，同时保持每个单独采样过程的完整性。由于每个生成的尺度都由不同的文本提示引导，因此与传统的超分辨率方法相比，我们的方法能够实现更深层次的缩放，而传统的超分辨方法可能难以在截然不同的尺度上创建新的上下文结构。我们在图像超分辨率和画外处理方面将我们的方法与其他技术进行了定性比较，并表明我们的方法在生成一致的多尺度内容方面最有效。 et.al.|[2312.02149](http://arxiv.org/abs/2312.02149)|null|
|**2023-12-04**|**Repurposing Diffusion-Based Image Generators for Monocular Depth Estimation**|单目深度估计是一项基本的计算机视觉任务。从单个图像中恢复3D深度在几何上是不合理的，需要场景理解，因此深度学习的兴起带来了突破也就不足为奇了。单目深度估计器的令人印象深刻的进展反映了模型容量的增长，从相对适中的CNN到大型Transformer架构。尽管如此，当呈现具有不熟悉内容和布局的图像时，单目深度估计器往往会遇到困难，因为他们对视觉世界的了解受到训练期间看到的数据的限制，并且受到对新领域的零镜头泛化的挑战。这促使我们探索在最近的生成扩散模型中捕获的广泛先验是否能够实现更好、更普遍的深度估计。我们介绍了Marigold，这是一种仿射不变的单目深度估计方法，它源于稳定扩散，并保留了其丰富的先验知识。估计器可以在几天内仅使用合成训练数据在单个GPU上进行微调。它在广泛的数据集中提供了最先进的性能，包括在特定情况下超过20%的性能提升。项目页面：https://marigoldmonodepth.github.io. et.al.|[2312.02145](http://arxiv.org/abs/2312.02145)|null|
|**2023-12-04**|**DiffiT: Diffusion Vision Transformers for Image Generation**|扩散模型凭借其强大的表现力和高样本质量，在各个领域中实现了许多新的应用程序和用例。对于样本生成，这些模型依赖于通过迭代去噪生成图像的去噪神经网络。然而，去噪网络架构的作用并没有得到很好的研究，大多数工作都依赖于卷积残差U-Nets。在本文中，我们研究了视觉转换器在基于扩散的生成学习中的有效性。具体来说，我们提出了一个新的模型，称为扩散视觉转换器（DiffiT），它由一个具有U形编码器和解码器的混合层次结构组成。我们引入了一种新的时间相关自注意模块，该模块允许注意层以有效的方式调整其在去噪过程的不同阶段的行为。我们还介绍了潜在的DiffiT，它由具有所提出的自注意层的变换器模型组成，用于高分辨率图像生成。我们的结果表明，DiffiT在生成高保真图像方面出奇地有效，并且在各种类别的条件和无条件合成任务上实现了最先进的（SOTA）基准。在潜在空间中，DiffiT在ImageNet-256数据集上获得了1.73的新SOTA FID分数。存储库：https://github.com/nvlabs/diffit et.al.|[2312.02139](http://arxiv.org/abs/2312.02139)|**[link](https://github.com/nvlabs/diffit)**|
|**2023-12-04**|**Style Aligned Image Generation via Shared Attention**|大规模文本到图像（T2I）模型在创意领域迅速崭露头角，从文本提示中产生了视觉上引人注目的输出。然而，控制这些模型以确保风格一致仍然具有挑战性，现有的方法需要微调和手动干预来理清内容和风格。在本文中，我们介绍了StyleAligned，这是一种新技术，旨在在一系列生成的图像之间建立风格对齐。通过在扩散过程中采用最小的“注意力共享”，我们的方法在T2I模型中保持了图像之间的风格一致性。这种方法允许通过直接的反转操作使用参考样式来创建样式一致的图像。我们的方法在不同风格和文本提示中的评估展示了高质量的合成和保真度，强调了其在各种输入中实现一致风格的功效。 et.al.|[2312.02133](http://arxiv.org/abs/2312.02133)|null|
|**2023-12-04**|**VideoSwap: Customized Video Subject Swapping with Interactive Semantic Point Correspondence**|当前基于扩散的视频编辑主要关注结构保留的编辑，通过利用各种密集的对应关系来确保时间一致性和运动对齐。但是，当目标编辑涉及形状更改时，这些方法往往无效。为了开始改变形状的视频编辑，我们在这项工作中探索了定制的视频主题交换，我们的目标是用具有不同身份和潜在不同形状的目标主题替换源视频中的主要主题。与以前依赖密集对应关系的方法不同，我们引入了利用语义点对应关系的VideoSwap框架，其灵感来自于我们的观察，即只有少量的语义点才能对齐受试者的运动轨迹并修改其形状。我们还介绍了各种用户点交互（例如，删除点和拖动点），以解决各种语义点对应关系。大量实验证明了在各种真实世界的视频中最先进的视频主题交换结果。 et.al.|[2312.02087](http://arxiv.org/abs/2312.02087)|null|
|**2023-12-04**|**Fisher information susceptibility for multiparameter quantum estimation**|我们将Fisher信息测量噪声易感性的概念扩展到多参数量子估计场景。在给出其数学定义后，我们导出了磁化率的上界和下界。然后，我们将这些技术应用于多参数估计的两个典型例子：相位和相位扩散的联合估计以及描述光学点源的非相干混合的不同参数的估计。我们的图清楚地表明了允许或阻碍多参数测量稳健性的条件。 et.al.|[2312.02035](http://arxiv.org/abs/2312.02035)|null|
|**2023-12-04**|**Stochastic Optimal Control Matching**|随机最优控制以驱动噪声系统的行为为目标，在科学、工程和人工智能领域有着广泛的应用。我们的工作介绍了随机最优控制匹配（SOCM），这是一种用于随机最优控制的新的迭代扩散优化（IDO）技术，源于与扩散模型的条件分数匹配损失相同的哲学。也就是说，通过尝试拟合匹配向量场，通过最小二乘问题来学习控制。与交叉熵损失密切相关的训练损失针对控制函数和出现在匹配向量场中的一系列重新参数化矩阵进行优化。关于重新参数化矩阵的优化旨在最小化匹配向量场的方差。在实验上，对于四种不同的控制设置，我们的算法实现了比所有现有的IDO技术更低的随机最优控制误差。SOCM的关键思想是路径重新参数化技巧，这是一种独立感兴趣的新技术，例如用于生成建模。 et.al.|[2312.02027](http://arxiv.org/abs/2312.02027)|null|
|**2023-12-04**|**Computational Investigation on Collective Dynamical Behaviors of Flickering Laminar Buoyant Diffusion Flames in Circular Arrays**|复杂系统中集体动力行为的出现具有其个体所不具备的独特特性。在这项研究中，对一系列八重闪烁层流浮力扩散火焰的圆形阵列进行了计算研究，以了解它们的集体行为。从涡旋动力学的角度识别和解释了五种不同的动力学模式，如合并模式、同相模式、旋转模式、闪烁死亡模式、部分闪烁死亡模式和反相模式。发现所有模式都由三个无量纲参数控制，即归一化的火焰频率f/f_0、火焰分离距离与火焰直径的比值和Grashof数Gr。根据f/f-0和组合的类雷诺数参数获得了统一的状态图。此外，从同相模式和反相模式到完全或部分闪烁死亡的分叉转变发生在620+-50处。 et.al.|[2312.02018](http://arxiv.org/abs/2312.02018)|null|

<p align=right>(<a href=#updated-on-20231205>back to top</a>)</p>

## NeRF

|Publish Date|Title|Abstract|PDF|Code|
|---|---|---|---|---|
|**2023-12-04**|**GaussianHead: Impressive 3D Gaussian-based Head Avatars with Dynamic Hybrid Neural Field**|以前的头部化身方法大多依赖于固定的显式基元（网格、点）或隐式曲面（符号距离函数）和体积神经辐射场，难以在高保真度、训练速度和资源消耗之间取得平衡。混合场最近的流行带来了新的表示，但受到通过固定映射获得的参数化因子的限制。我们提出了GaussianHead：一种基于各向异性三维高斯基元的头部化身算法。我们利用规范高斯来表示动态场景。使用显式“动态”三平面作为参数化头部几何的有效容器，与底层几何和三平面中的因子很好地对齐，我们获得了正则高斯的对齐正则因子。利用微小的MLP，因子被解码为3D高斯基元的不透明度和球面谐波系数。最后，我们使用高效的可微高斯光栅化器进行渲染。我们的方法显著受益于我们基于3D高斯的新表示，并且三平面中底层几何结构和因子的适当对齐变换消除了固定映射引入的偏差。与最先进的技术相比，我们在自我重建、新视图合成和跨身份再现等任务中实现了最佳的视觉效果，同时保持了高渲染效率（每帧0.12秒）。在某些情况下，甚至鼻子周围的毛孔也清晰可见。代码和其他视频可以在项目主页上找到。 et.al.|[2312.01632](http://arxiv.org/abs/2312.01632)|null|
|**2023-11-29**|**Accelerating Neural Field Training via Soft Mining**|我们提出了一种通过有效选择采样位置来加速神经场训练的方法。虽然神经场最近变得很流行，但它通常是通过对训练域进行统一采样或通过手工启发式进行训练的。我们证明，通过基于重要性采样的软挖掘技术可以提高收敛性和最终训练质量：我们不是完全考虑或忽略一个像素，而是用标量来衡量相应的损失。为了实现我们的想法，我们使用Langevin蒙特卡罗采样。我们表明，通过这样做，具有更高误差的区域被更频繁地选择，导致收敛速度提高了2倍以上。本研究的代码和相关资源可在https://ubc-vision.github.io/nf-soft-mining/. et.al.|[2312.00075](http://arxiv.org/abs/2312.00075)|null|
|**2023-11-29**|**Neural Fields with Thermal Activations for Arbitrary-Scale Super-Resolution**|最近的任意尺度单图像超分辨率（ASSR）方法已经使用局部神经场来表示可以以不同速率采样的连续信号。然而，在这样的公式中，场值的逐点查询并不自然地与给定像素的点扩散函数（PSF）匹配。在这项工作中，我们提出了一种设计神经场的新方法，使得可以使用高斯PSF来查询点，该函数在ASSR的分辨率之间移动时起到抗混叠的作用。我们使用从傅立叶理论和热方程导出的新激活函数来实现这一点。这不需要额外的成本：与图像域中的滤波不同，在我们的框架中使用高斯PSF查询点不会影响计算成本。与超网络相结合，我们的方法不仅提供了理论上有保证的抗混叠，而且为ASSR设置了一个新的标准，同时也比以前的方法更具参数效率。 et.al.|[2311.17643](http://arxiv.org/abs/2311.17643)|null|
|**2023-11-28**|**In Search of a Data Transformation That Accelerates Neural Field Training**|神经场是数据表示中一种新兴的范式，它训练神经网络来逼近给定的信号。阻碍其广泛采用的一个关键障碍是编码速度——生成神经场需要神经网络的过拟合，这可能需要大量的SGD步骤才能达到所需的保真度水平。在本文中，我们深入研究了数据转换对神经场训练速度的影响，特别是关注像素位置的排列如何影响SGD的收敛速度。与直觉相反，我们发现随机排列像素位置可以显著加速训练。为了解释这一现象，我们通过PSNR曲线、损失景观和误差模式来检验神经场训练。我们的分析表明，随机像素排列去除了易于拟合的模式，这有助于在早期阶段进行简单的优化，但阻碍了捕捉信号的精细细节。 et.al.|[2311.17094](http://arxiv.org/abs/2311.17094)|null|
|**2023-11-28**|**HumanGaussian: Text-Driven 3D Human Generation with Gaussian Splatting**|根据文本提示生成逼真的三维人体是一项理想但具有挑战性的任务。现有的方法通过分数蒸馏采样（SDS）优化3D表示，如网格或神经场，其存在细节不足或训练时间过长的问题。在本文中，我们提出了一个高效而有效的框架HumanGaussian，它可以生成具有细粒度几何结构和逼真外观的高质量3D人。我们的关键见解是，3D高斯飞溅是一种具有周期性高斯收缩或增长的高效渲染器，其中这种自适应密度控制可以由内在的人体结构自然引导。具体而言，1）我们首先提出了一种结构感知SDS，它可以同时优化人体外观和几何形状。利用RGB和深度空间的多模态得分函数来提取高斯致密化和修剪过程。2） 此外，我们通过将SDS分解为更嘈杂的生成分数和更干净的分类器分数，设计了一种退火的负提示引导，很好地解决了过饱和问题。在仅修剪阶段中，基于高斯大小进一步消除浮动伪影，以增强生成平滑度。大量实验证明了我们的框架具有卓越的效率和竞争力，在不同的场景下呈现了生动的3D人类。项目页面：https://alvinliu0.github.io/projects/humangaussian et.al.|[2311.17061](http://arxiv.org/abs/2311.17061)|null|
|**2023-11-28**|**SplitNeRF: Split Sum Approximation Neural Field for Joint Geometry, Illumination, and Material Estimation**|我们提出了一种新的方法，通过从一组具有固定照明的姿势图像中估计真实世界物体的几何结构、材料特性和环境照明来数字化它们。我们的方法将分割和近似与基于图像的照明结合到神经辐射场（NeRF）管道中，用于基于物理的实时渲染。我们建议使用单个场景特定的MLP来建模场景的照明，该MLP表示任意分辨率的预集成的基于图像的照明。我们通过开发一种基于有效蒙特卡罗采样的新型正则化子来实现预集成照明的精确建模。此外，我们还提出了一种新的方法，通过利用基于蒙特卡罗采样的类似正则化子来监督自遮挡预测。实验结果证明了我们的方法在估计场景几何、材料特性和照明方面的效率和有效性。我们的方法能够在单个NVIDIA A100 GPU中仅经过 ${\sim}1$ 小时的训练后就获得最先进的重新照明质量。 et.al.|[2311.16671](http://arxiv.org/abs/2311.16671)|null|
|**2023-11-27**|**MeshGPT: Generating Triangle Meshes with Decoder-Only Transformers**|我们介绍了MeshGPT，这是一种生成三角形网格的新方法，它反映了艺术家创建的网格的典型紧凑性，而不是通过等表面方法从神经场中提取的密集三角形网格。受强大的大型语言模型最近进展的启发，我们采用了一种基于序列的方法来自回归生成三角形网格作为三角形序列。我们首先使用图卷积来学习潜在量化嵌入的词汇表，图卷积为这些嵌入提供了局部网格几何和拓扑的信息。这些嵌入被解码器排序并解码为三角形，确保它们能够有效地重建网格。然后在这个学习的词汇表上训练转换器，以在给定先前嵌入的情况下预测下一个嵌入的索引。一旦训练好，我们的模型就可以进行自回归采样以生成新的三角形网格，直接生成具有尖锐边缘的紧凑网格，更接近于模仿手工网格的有效三角测量模式。与最先进的网格生成方法相比，MeshGPT有了显著的改进，形状覆盖率提高了9%，各种类别的FID得分提高了30分。 et.al.|[2311.15475](http://arxiv.org/abs/2311.15475)|null|
|**2023-11-26**|**Distributed Delay and Desynchronization in a Brain Network Model**|我们考虑一个神经场模型，该模型由任意数量的Wilson Cowan节点的网络组成，该网络具有抑制性耦合强度和延时兴奋性耦合的稳态调节。我们扩展了以前对该模型的研究，将具有常用核分布的分布式时延包括在内：德尔塔函数、均匀分布和伽玛分布。重点讨论满足常行和条件的网络，我们展示了连通矩阵的每个特征值如何与Hopf分支相关，并且特征值决定了分支是导致同步还是去同步的振荡行为。我们考虑两个示例网络，一个具有所有实特征值（双向环），另一个具有一些复特征值（单向环）。在双向环中，Hopf曲线被组织起来，使得只有同步的Hopf才会导致渐近稳定的行为。因此，网络中的行为总是同步的。然而，在单向环网络中，异步和同步Hopf曲线的交点可能会出现双Hopf分岔点。因此，可以出现渐近稳定的同步和异步极限环，以及结合同步和异步行为的类环面解。增加网络的大小或平均时延会使这些交叉点和相关的异步行为更有可能发生。数值方法用于证实这一发现，并使用Wolfram Mathematica绘制了Hopf分岔曲线。这些见解提供了对大型振荡器网络中去同步机制的更深入理解。 et.al.|[2311.15329](http://arxiv.org/abs/2311.15329)|null|
|**2023-11-25**|**Coordinate-Aware Modulation for Neural Fields**|将低维输入坐标映射到相应信号的神经场在表示各种信号方面显示出了有希望的结果。已经提出了许多方法，并且使用MLP和网格表示的技术已经取得了实质性的成功。MLP允许紧凑和高表达性，但经常受到光谱偏差和缓慢收敛速度的影响。另一方面，使用网格的方法不受光谱偏差的影响，并且以高空间复杂度为代价实现了快速的训练速度。在这项工作中，我们提出了一种在神经领域中利用MLP和网格表示的新方法。与顺序组合它们（首先从网格中提取特征并将其提供给MLP）的流行方法不同，我们将无光谱偏差的网格表示注入MLP中的中间特征。更具体地说，我们提出了一种坐标感知调制（CAM），它使用从网格表示中提取的比例和偏移参数来调制中间特征。这可以保持MLP的优势，同时减轻任何剩余的潜在偏差，促进高频成分的快速学习。此外，我们根据经验发现，在神经领域文献中尚未成功的特征归一化，在与所提出的CAM结合应用时被证明是有效的。实验结果表明，CAM增强了神经表示的性能，并提高了一系列信号的学习稳定性。特别是在新颖的视图合成任务中，我们以最少的参数数量和快速的训练速度实现了最先进的动态场景性能，并在1MB内存下实现了静态场景的最佳性能。CAM的性能也大大优于使用神经场的最佳视频压缩方法。 et.al.|[2311.14993](http://arxiv.org/abs/2311.14993)|null|
|**2023-11-22**|**Compact 3D Gaussian Representation for Radiance Field**|神经辐射场（NeRFs）在高保真度捕捉复杂三维场景方面显示出非凡的潜力。然而，阻碍NeRFs广泛采用的一个持续挑战是体积绘制造成的计算瓶颈。另一方面，3D高斯飞溅（3DGS）最近作为一种替代表示出现，它利用了基于3D高斯的表示，并采用光栅化流水线来渲染图像，而不是体积渲染，实现了非常快的渲染速度和有希望的图像质量。然而，一个显著的缺点出现了，因为3DGS需要大量的3D高斯来维持渲染图像的高保真度，这需要大量的存储器和存储。为了解决这一关键问题，我们特别强调两个关键目标：在不牺牲性能的情况下减少高斯点的数量，以及压缩高斯属性，如与视图相关的颜色和协方差。为此，我们提出了一种可学习的掩码策略，该策略在保持高性能的同时显著减少高斯数。此外，我们通过使用基于网格的神经场而不是依赖于球面谐波，提出了一种紧凑但有效的视图相关颜色表示。最后，我们学习码本，通过矢量量化来紧凑地表示高斯的几何属性。在我们广泛的实验中，我们一致表明，与3DGS相比，存储空间减少了10美元，渲染速度提高，同时保持了场景表示的质量。我们的工作为3D场景表示提供了一个全面的框架，实现了高性能、快速训练、紧凑性和实时渲染。我们的项目页面位于https://maincold2.github.io/c3dgs/. et.al.|[2311.13681](http://arxiv.org/abs/2311.13681)|null|

<p align=right>(<a href=#updated-on-20231205>back to top</a>)</p>

[contributors-shield]: https://img.shields.io/github/contributors/Vincentqyw/cv-arxiv-daily.svg?style=for-the-badge
[contributors-url]: https://github.com/Vincentqyw/cv-arxiv-daily/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/Vincentqyw/cv-arxiv-daily.svg?style=for-the-badge
[forks-url]: https://github.com/Vincentqyw/cv-arxiv-daily/network/members
[stars-shield]: https://img.shields.io/github/stars/Vincentqyw/cv-arxiv-daily.svg?style=for-the-badge
[stars-url]: https://github.com/Vincentqyw/cv-arxiv-daily/stargazers
[issues-shield]: https://img.shields.io/github/issues/Vincentqyw/cv-arxiv-daily.svg?style=for-the-badge
[issues-url]: https://github.com/Vincentqyw/cv-arxiv-daily/issues

