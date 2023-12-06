[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]

## Updated on 2023.12.06
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
|**2023-12-05**|**ReconFusion: 3D Reconstruction with Diffusion Priors**|神经辐射场（NeRFs）等3D重建方法擅长于绘制复杂场景的逼真新颖视图。然而，恢复高质量的NeRF通常需要数十到数百个输入图像，这导致了耗时的捕获过程。我们提出ReconFusion，只使用几张照片来重建真实世界的场景。我们的方法利用扩散先验进行新的视图合成，在合成和多视图数据集上训练，使基于NeRF的3D重建管道在输入图像集捕获的新相机姿态之外的新相机姿势下正则化。我们的方法在欠约束区域中合成逼真的几何体和纹理，同时保留观察到的区域的外观。我们在各种真实世界的数据集上进行了广泛的评估，包括前向和360度场景，证明了与以前的少数视图NeRF重建方法相比，性能有了显著提高。 et.al.|[2312.02981](http://arxiv.org/abs/2312.02981)|null|
|**2023-12-04**|**Calibrated Uncertainties for Neural Radiance Fields**|神经辐射场在新的视图合成方面取得了显著的成果，但仍然缺乏一个关键组成部分：精确测量其预测中的不确定性。概率NeRF方法试图解决这一问题，但它们的输出概率通常没有准确校准，因此无法捕捉模型的真实置信水平。在稀疏视图设置中，校准是一个特别具有挑战性的问题，因为在稀疏视图中，无法获得额外的保留数据来拟合推广到测试分布的校准器。在本文中，我们介绍了从NeRF模型中获得校准不确定性的第一种方法。我们的方法基于稳健有效的度量，从预测后验分布中计算每像素的不确定性。我们提出了两种技术来消除对保留数据的需求。第一种基于补丁采样，包括为每个场景训练两个NeRF模型。第二种是一种新的元校准器，只需要训练一个NeRF模型。我们提出的获得校准不确定性的方法在保持图像质量的同时，在稀疏视图设置中实现了最先进的不确定性。我们进一步证明了我们的方法在视图增强和次优视图选择等应用中的有效性。 et.al.|[2312.02350](http://arxiv.org/abs/2312.02350)|null|
|**2023-12-04**|**Re-Nerfing: Enforcing Geometric Constraints on Neural Radiance Fields through Novel Views Synthesis**|即使在大规模、无边界的场景中，神经辐射场（NeRF）也显示出了非凡的新颖视图合成能力，尽管需要数百个视图或在更稀疏的环境中引入伪影。只要只有很小的视觉重叠，它们的优化就会受到形状辐射模糊的影响。这会导致错误的场景几何体和伪影。在本文中，我们提出了Re-Nerfing，这是一种简单而通用的多阶段方法，利用NeRF自己的观点综合来解决这些局限性。通过Re-Nerfing，我们增加了场景的覆盖范围，并增强了新颖视图的几何一致性，如下所示：首先，我们用可用视图训练NeRF。然后，我们使用优化的NeRF来合成原始视图旁边的伪视图，以模拟立体或三焦点设置。最后，我们用原始视图和伪视图训练第二个NeRF，同时通过新合成的图像实施结构和核约束。在mip-NeRF 360数据集上进行的大量实验表明，在更密集和更稀疏的输入场景中，Re-Nerfing的有效性，为最先进的Zip-NeRF带来了改进，即使在使用所有视图进行训练时也是如此。 et.al.|[2312.02255](http://arxiv.org/abs/2312.02255)|null|
|**2023-12-03**|**Slice3D: Multi-Slice, Occlusion-Revealing, Single View 3D Reconstruction**|我们引入了多切片推理，这是一种单视图3D重建的新概念，它挑战了当前和主流的观点，即多视图合成是单视图和3D之间最自然的管道。我们的主要观察结果是，对象切片比改变视图以显示被遮挡的结构更有利。具体来说，切片更能揭示闭塞，因为它可以在没有阻塞的情况下剥离任何闭塞物。在极限中，即具有无限多个切片时，可以保证揭开所有隐藏的对象部分。我们通过开发Slice3D来实现我们的想法，Slice3D是一种新的单视图3D重建方法，它首先从单个RGB图像预测多切片图像，然后使用基于坐标的变换网络将切片集成到3D模型中，用于符号距离预测。切片图像可以通过基于U-Net的网络进行回归或生成。对于前者，我们注入可学习的切片指示符代码来将每个解码图像指定到空间切片位置，而切片生成器是对堆叠在输入通道上的整个切片图像进行操作的去噪扩散模型。我们对最先进的替代方案进行了广泛的评估，以证明我们的方法的优越性，特别是在模糊的情况下恢复复杂和严重堵塞的形状结构。所有Slice3D结果都是由在单个Nvidia A40 GPU上训练的网络生成的，推理时间不到20秒。 et.al.|[2312.02221](http://arxiv.org/abs/2312.02221)|null|
|**2023-12-04**|**GPS-Gaussian: Generalizable Pixel-wise 3D Gaussian Splatting for Real-time Human Novel View Synthesis**|我们提出了一种新的方法，称为GPS高斯，用于实时合成角色的新视图。所提出的方法能够在稀疏视图相机设置下实现2K分辨率的渲染。与需要按主题优化的原始高斯飞溅或神经隐式渲染方法不同，我们引入了在源视图上定义的高斯参数图，并直接回归高斯飞溅特性，用于即时新视图合成，而无需任何微调或优化。为此，我们在大量人体扫描数据上训练我们的高斯参数回归模块，并与深度估计模块一起将2D参数图提升到3D空间。所提出的框架是完全可微分的，在几个数据集上的实验表明，我们的方法优于最先进的方法，同时实现了超高的渲染速度。 et.al.|[2312.02155](http://arxiv.org/abs/2312.02155)|null|
|**2023-12-04**|**Fast View Synthesis of Casual Videos**|由于场景动力学和缺乏视差等挑战，从野外视频中合成新颖的视图是困难的。虽然现有的方法在隐式神经辐射场方面显示出了有希望的结果，但它们的训练和渲染速度很慢。本文重新审视了显式视频表示，以有效地从单目视频中合成高质量的新颖视图。我们分别处理静态和动态视频内容。具体来说，我们使用基于扩展平面的场景表示来构建全局静态场景模型，以合成时间相干的新颖视频。我们的基于平面的场景表示通过球面谐波和位移图来增强，以捕捉与视图相关的效果并对非平面复杂曲面几何体进行建模。为了提高效率，我们选择按帧点云来表示动态内容。虽然这种表示容易出现不一致，但由于运动，轻微的时间不一致在感知上被掩盖了。我们开发了一种快速估计这种混合视频表示并实时渲染新视图的方法。我们的实验表明，我们的方法可以从野外视频中渲染高质量的新视图，其质量与最先进的方法相当，同时在训练和实时渲染方面速度快100倍。 et.al.|[2312.02135](http://arxiv.org/abs/2312.02135)|null|
|**2023-12-04**|**SplaTAM: Splat, Track & Map 3D Gaussians for Dense RGB-D SLAM**|密集同时定位和映射（SLAM）对于具体场景的理解至关重要。最近的工作表明，3D高斯可以使用多个姿势的相机进行高质量的场景重建和实时渲染。在这种情况下，我们首次展示了通过3D高斯表示场景可以使用单个非聚焦单目RGB-D相机实现密集SLAM。我们的方法SplaTAM解决了先前基于辐射场的表示的局限性，包括快速渲染和优化、确定区域是否先前已映射的能力，以及通过添加更多高斯来进行结构化地图扩展。我们使用在线跟踪和映射管道，同时对其进行剪裁，以专门使用底层高斯表示和轮廓引导的优化，通过可微分渲染进行优化。大量实验表明，SplaTAM在相机姿态估计、地图构建和新颖视图合成方面实现了高达两倍的最先进性能，证明了其优于现有方法，同时允许实时渲染高分辨率密集3D地图。 et.al.|[2312.02126](http://arxiv.org/abs/2312.02126)|null|
|**2023-12-04**|**ColonNeRF: Neural Radiance Fields for High-Fidelity Long-Sequence Colonoscopy Reconstruction**|结肠镜重建是诊断癌症的关键。然而，准确的长序列结肠镜重建面临三个主要挑战：（1）由于结肠弯曲和卷曲的形状，结肠各段之间存在差异；（2） 简单和复杂折叠的几何结构的共存；（3） 由于受约束的相机轨迹而导致的稀疏视点。为了应对这些挑战，我们引入了一种新的基于神经辐射场（NeRF）的重建框架，名为ColonNeRF，它利用神经渲染进行长序列结肠镜检查的新视图合成。具体来说，为了以分段的方式重建整个结肠，我们的ColonNeRF引入了一个区域划分和集成模块，有效地减少了形状的差异，并确保了每个片段的几何一致性。为了在一个统一的框架中学习简单和复杂的几何结构，我们的ColonNeRF集成了一个多层次融合模块，该模块从简单到困难逐步对结肠区域进行建模。此外，为了克服稀疏视图带来的挑战，我们设计了一个DensiNet模块，用于在语义一致性的指导下加密相机姿势。我们在合成数据集和真实世界数据集上进行了广泛的实验，以评估我们的ColonNeRF。从数量上讲，我们的ColonNeRF在两个基准和四个评估指标上优于现有方法。值得注意的是，在SimCol-to-3D数据集上，我们的LPIPS-ALEX分数显著增加了约67%-85%。从质量上讲，我们的重建可视化显示了更清晰的纹理和更准确的几何细节。这些充分证明了我们优于最先进方法的优越性能。 et.al.|[2312.02015](http://arxiv.org/abs/2312.02015)|null|
|**2023-12-04**|**GaussianHead: Impressive 3D Gaussian-based Head Avatars with Dynamic Hybrid Neural Field**|以前的头部化身方法大多依赖于固定的显式基元（网格、点）或隐式曲面（符号距离函数）和体积神经辐射场，难以在高保真度、训练速度和资源消耗之间取得平衡。混合场最近的流行带来了新的表示，但受到通过固定映射获得的参数化因子的限制。我们提出了GaussianHead：一种基于各向异性三维高斯基元的头部化身算法。我们利用规范高斯来表示动态场景。使用显式“动态”三平面作为参数化头部几何的有效容器，与底层几何和三平面中的因子很好地对齐，我们获得了正则高斯的对齐正则因子。利用微小的MLP，因子被解码为3D高斯基元的不透明度和球面谐波系数。最后，我们使用高效的可微高斯光栅化器进行渲染。我们的方法显著受益于我们基于3D高斯的新表示，并且三平面中底层几何结构和因子的适当对齐变换消除了固定映射引入的偏差。与最先进的技术相比，我们在自我重建、新视图合成和跨身份再现等任务中实现了最佳的视觉效果，同时保持了高渲染效率（每帧0.12秒）。在某些情况下，甚至鼻子周围的毛孔也清晰可见。代码和其他视频可以在项目主页上找到。 et.al.|[2312.01632](http://arxiv.org/abs/2312.01632)|null|
|**2023-12-03**|**SANeRF-HQ: Segment Anything for NeRF in High Quality**|最近，Segment Anything Model（SAM）展示了零样本分割的显著能力，而NeRF（Neural Radiance Fields）作为一种解决新视图合成之外的各种3D问题的方法而广受欢迎。尽管最初尝试将这两种方法结合到3D分割中，但它们面临着在复杂场景中准确、一致地分割对象的挑战。在本文中，我们介绍了高质量NeRF的任何分割（SANeRF-HQ），以实现给定场景中任何对象的高质量3D分割。SANeRF HQ利用SAM在用户提供的提示的指导下进行开放世界对象分割，同时利用NeRF从不同角度聚合信息。为了克服上述挑战，我们在聚合过程中使用密度场和RGB相似性来提高分割边界的准确性。强调分割的准确性，我们在多个NeRF数据集上定量评估我们的方法，在这些数据集上可以获得或手动注释高质量的基本事实。SANeRF HQ在NeRF对象分割方面比以前最先进的方法有了显著的质量改进，为对象定位提供了更高的灵活性，并实现了跨多个视图的更一致的对象分割。其他信息可在https://lyclyc52.github.io/sanerf-hq/. et.al.|[2312.01531](http://arxiv.org/abs/2312.01531)|null|

<p align=right>(<a href=#updated-on-20231206>back to top</a>)</p>

## 3D Reconstruction

|Publish Date|Title|Abstract|PDF|Code|
|---|---|---|---|---|
|**2023-12-05**|**ReconFusion: 3D Reconstruction with Diffusion Priors**|神经辐射场（NeRFs）等3D重建方法擅长于绘制复杂场景的逼真新颖视图。然而，恢复高质量的NeRF通常需要数十到数百个输入图像，这导致了耗时的捕获过程。我们提出ReconFusion，只使用几张照片来重建真实世界的场景。我们的方法利用扩散先验进行新的视图合成，在合成和多视图数据集上训练，使基于NeRF的3D重建管道在输入图像集捕获的新相机姿态之外的新相机姿势下正则化。我们的方法在欠约束区域中合成逼真的几何体和纹理，同时保留观察到的区域的外观。我们在各种真实世界的数据集上进行了广泛的评估，包括前向和360度场景，证明了与以前的少数视图NeRF重建方法相比，性能有了显著提高。 et.al.|[2312.02981](http://arxiv.org/abs/2312.02981)|null|
|**2023-12-05**|**R3D-SWIN:Use Shifted Window Attention for Single-View 3D Reconstruction**|最近，视觉转换器在各种计算机视觉任务中表现良好，包括体素3D重建。然而，视觉转换器的窗口不是多尺度的，并且窗口之间没有连接，这限制了体素三维重建的准确性。因此，我们提出了一种移位窗口关注体素三维重建网络。据我们所知，这是第一项将移位窗口注意力应用于体素3D重建的工作。在ShapeNet上的实验结果验证了我们的方法在单视图重建中达到了SOTA的精度。 et.al.|[2312.02725](http://arxiv.org/abs/2312.02725)|null|
|**2023-12-05**|**DreaMo: Articulated 3D Reconstruction From A Single Casual Video**|关节式三维重建在各个领域都有着宝贵的应用，但它仍然成本高昂，需要领域专家的大量工作。无模板学习方法的最新进展显示出单目视频的良好效果。然而，这些方法需要全面覆盖输入视频中主题的所有观点，从而限制了其适用于从在线来源随意捕获的视频。在这项工作中，我们研究了从一个随意拍摄的互联网视频中进行的立体形状重建，其中受试者的视野覆盖不完整。我们提出了DreaMo，它在解决具有挑战性的低覆盖区域的同时，通过视图条件扩散先验和几个定制的正则化来联合执行形状重建。此外，我们还引入了一种骨骼生成策略，从学习的神经骨骼和蒙皮权重中创建人类可解释的骨骼。我们对一个以不完全视角覆盖为特征的自行收集的互联网视频集进行了研究。DreaMo在新颖的视图渲染、详细的关节形状重建和骨骼生成方面显示出良好的质量。大量的定性和定量研究验证了每个拟议组件的有效性，并表明由于视图覆盖不完整，现有方法无法解决正确的几何问题。 et.al.|[2312.02617](http://arxiv.org/abs/2312.02617)|null|
|**2023-12-05**|**Prompt2NeRF-PIL: Fast NeRF Generation via Pretrained Implicit Latent**|本文探索了可提示的NeRF生成（例如，文本提示或单个图像提示），用于直接调节和快速生成底层3D场景的NeRF参数，从而在提供具有条件控制的完整3D生成的同时，省去复杂的中间步骤。与之前涉及乏味的逐提示优化的基于扩散CLIP的管道不同，Prompt2NeRF PIL能够利用预先训练的NeRF参数的隐式潜在空间，通过单次前向传递生成各种3D对象。此外，在零样本任务中，我们的实验表明，由我们的方法产生的NeRF用作语义信息初始化，显著加速了现有提示-NeRF方法的推理过程。具体来说，我们将展示我们的方法将文本到NeRF模型DreamFusion的速度和图像到NeRF方法Zero-1-to-3的3D重建速度提高了3到5倍。 et.al.|[2312.02568](http://arxiv.org/abs/2312.02568)|null|
|**2023-12-03**|**Slice3D: Multi-Slice, Occlusion-Revealing, Single View 3D Reconstruction**|我们引入了多切片推理，这是一种单视图3D重建的新概念，它挑战了当前和主流的观点，即多视图合成是单视图和3D之间最自然的管道。我们的主要观察结果是，对象切片比改变视图以显示被遮挡的结构更有利。具体来说，切片更能揭示闭塞，因为它可以在没有阻塞的情况下剥离任何闭塞物。在极限中，即具有无限多个切片时，可以保证揭开所有隐藏的对象部分。我们通过开发Slice3D来实现我们的想法，Slice3D是一种新的单视图3D重建方法，它首先从单个RGB图像预测多切片图像，然后使用基于坐标的变换网络将切片集成到3D模型中，用于符号距离预测。切片图像可以通过基于U-Net的网络进行回归或生成。对于前者，我们注入可学习的切片指示符代码来将每个解码图像指定到空间切片位置，而切片生成器是对堆叠在输入通道上的整个切片图像进行操作的去噪扩散模型。我们对最先进的替代方案进行了广泛的评估，以证明我们的方法的优越性，特别是在模糊的情况下恢复复杂和严重堵塞的形状结构。所有Slice3D结果都是由在单个Nvidia A40 GPU上训练的网络生成的，推理时间不到20秒。 et.al.|[2312.02221](http://arxiv.org/abs/2312.02221)|null|
|**2023-12-04**|**Steerers: A framework for rotation equivariant keypoint descriptors**|在视点的大变化上具有判别性和可匹配性的图像关键点描述对于3D重建至关重要。然而，由学习的描述符输出的描述通常对相机旋转不具有鲁棒性。虽然它们可以通过例如数据增强而变得更健壮，但这会降低直立图像的性能。另一种方法是增加测试时间，这会显著增加运行时间。相反，我们在描述空间中学习对输入图像的旋转进行编码的线性变换。我们称这种线性变换为转向器，因为它允许我们像旋转图像一样变换描述。根据表示理论，我们知道了旋转群的所有可能的转向器。转向器可以优化（A）给定固定描述符，（B）与描述符联合，或者（C）我们可以优化给定固定转向器的描述符。我们在所有这三种设置中进行了实验，并在旋转不变图像匹配基准AIMS和Roto-360上获得了最先进的结果。我们在github.com/georg-bn/rotation-steelers上发布代码和模型权重。 et.al.|[2312.02152](http://arxiv.org/abs/2312.02152)|**[link](https://github.com/georg-bn/rotation-steerers)**|
|**2023-12-04**|**iMatching: Imperative Correspondence Learning**|学习特征对应关系是计算机视觉的一项基础任务，对视觉里程计和三维重建等下游应用具有极其重要的意义。尽管最近在数据驱动模型方面取得了进展，但由于缺乏准确的每像素对应标签，特征对应学习仍然受到限制。为了克服这一困难，我们引入了一种新的自监督方案，即命令式学习（IL），用于训练特征对应关系。它可以在没有任何相机姿势或深度标签的情况下，在任意不间断的视频上进行函授学习，预示着自我监督函授学习的新时代。具体来说，我们将对应学习问题公式化为双层优化，将束调整的重投影误差作为模型的监督信号。为了避免大的内存和计算开销，我们利用驻点通过束调整有效地反向传播隐式梯度。通过广泛的实验，我们在包括特征匹配和姿态估计在内的任务上表现出了卓越的性能，在这些任务中，我们获得了比最先进的匹配模型平均30%的精度增益。 et.al.|[2312.02141](http://arxiv.org/abs/2312.02141)|null|
|**2023-12-04**|**Light Field Imaging in the Restrictive Object Space based on Flexible Angular Plane**|在一些应用中，光场成像系统的对象空间是有限的，例如工业和医疗内窥镜。如果传统的光场成像系统直接用于限制性物体空间（ROS），但没有任何具体考虑，ROS将导致严重的微透镜图像失真，进而影响光场解码、校准和3D重建。限制性物体空间中的光场成像是复杂而重要的。在本文中，我们首先推导出微透镜图像偏移的原因是角平面的位置变化，然后我们提出了ROS-LF的柔性角平面，而在传统的光场中，角平面总是与主透镜平面重合。随后，我们提出了ROS-LF的微透镜图像无失真原理，并介绍了ROS-LF的成像原理。我们证明了ROS-LF和传统光场成像模型之间的差异是孔径常数项。最后，我们设计了一个ROS-LF模拟系统，并对其进行了校准，以验证本文提出的原理。 et.al.|[2312.01761](http://arxiv.org/abs/2312.01761)|null|
|**2023-12-03**|**SANeRF-HQ: Segment Anything for NeRF in High Quality**|最近，Segment Anything Model（SAM）展示了零样本分割的显著能力，而NeRF（Neural Radiance Fields）作为一种解决新视图合成之外的各种3D问题的方法而广受欢迎。尽管最初尝试将这两种方法结合到3D分割中，但它们面临着在复杂场景中准确、一致地分割对象的挑战。在本文中，我们介绍了高质量NeRF的任何分割（SANeRF-HQ），以实现给定场景中任何对象的高质量3D分割。SANeRF HQ利用SAM在用户提供的提示的指导下进行开放世界对象分割，同时利用NeRF从不同角度聚合信息。为了克服上述挑战，我们在聚合过程中使用密度场和RGB相似性来提高分割边界的准确性。强调分割的准确性，我们在多个NeRF数据集上定量评估我们的方法，在这些数据集上可以获得或手动注释高质量的基本事实。SANeRF HQ在NeRF对象分割方面比以前最先进的方法有了显著的质量改进，为对象定位提供了更高的灵活性，并实现了跨多个视图的更一致的对象分割。其他信息可在https://lyclyc52.github.io/sanerf-hq/. et.al.|[2312.01531](http://arxiv.org/abs/2312.01531)|null|
|**2023-12-02**|**RNb-NeuS: Reflectance and Normal-based Multi-View 3D Reconstruction**|本文介绍了一种用于集成通过光度立体获得的多视图反射率和法线图的通用范式。我们的方法采用了反射率和法线的逐像素联合重新参数化，将它们视为在模拟的变化照明下渲染的弧度向量。这种重新参数化实现了反射图和法线图作为输入数据在基于神经体积渲染的3D重建中的无缝集成，同时保留了单个优化目标。相比之下，最近的多视图光度立体（MVPS）方法依赖于多个潜在冲突的目标。尽管我们提出的方法明显简单，但在F分数、倒角距离和平均角误差度量方面，它在MVPS基准测试中优于最先进的方法。值得注意的是，它显著改善了高曲率或低可见性区域的详细3D重建。 et.al.|[2312.01215](http://arxiv.org/abs/2312.01215)|null|

<p align=right>(<a href=#updated-on-20231206>back to top</a>)</p>

## Diffusion

|Publish Date|Title|Abstract|PDF|Code|
|---|---|---|---|---|
|**2023-12-05**|**ReconFusion: 3D Reconstruction with Diffusion Priors**|神经辐射场（NeRFs）等3D重建方法擅长于绘制复杂场景的逼真新颖视图。然而，恢复高质量的NeRF通常需要数十到数百个输入图像，这导致了耗时的捕获过程。我们提出ReconFusion，只使用几张照片来重建真实世界的场景。我们的方法利用扩散先验进行新的视图合成，在合成和多视图数据集上训练，使基于NeRF的3D重建管道在输入图像集捕获的新相机姿态之外的新相机姿势下正则化。我们的方法在欠约束区域中合成逼真的几何体和纹理，同时保留观察到的区域的外观。我们在各种真实世界的数据集上进行了广泛的评估，包括前向和360度场景，证明了与以前的少数视图NeRF重建方法相比，性能有了显著提高。 et.al.|[2312.02981](http://arxiv.org/abs/2312.02981)|null|
|**2023-12-05**|**Alchemist: Parametric Control of Material Properties with Diffusion Models**|我们提出了一种控制物体材料属性的方法，如真实图像中的粗糙度、金属、反照率和透明度。我们的方法利用了以照片真实性著称的文本到图像模型的生成先验，使用标量值和指令来改变低级材料属性。针对缺乏具有受控材料属性的数据集的问题，我们使用基于物理的材料生成了一个以对象为中心的合成数据集。在这个合成数据集上对修改后的预训练文本到图像模型进行微调，使我们能够编辑真实世界图像中的材料属性，同时保留所有其他属性。我们展示了我们的模型在材料编辑的NeRF中的潜在应用。 et.al.|[2312.02970](http://arxiv.org/abs/2312.02970)|null|
|**2023-12-05**|**AmbiGen: Generating Ambigrams from Pre-trained Diffusion Model**|Ambigrams是一种书法设计，根据观看方向的不同而有不同的含义。即使对熟练的艺术家来说，创建歧义也是一项具有挑战性的任务，因为它需要同时在两个不同的视角下保持意义。在这项工作中，我们建议通过提取大规模视觉和语言扩散模型（即DeepFloyd IF）来生成歧义图，以优化字母在两个观看方向上的轮廓易读性。从经验上讲，我们证明了我们的方法优于现有的模糊图生成方法。在英语中500个最常见的单词上，我们的方法使单词准确性提高了11.6%以上，编辑距离至少减少了41.9%。 et.al.|[2312.02967](http://arxiv.org/abs/2312.02967)|null|
|**2023-12-05**|**Diffusion-SS3D: Diffusion Model for Semi-supervised 3D Object Detection**|半监督对象检测对于3D场景理解至关重要，有效地解决了获取大规模3D边界框注释的局限性。现有的方法通常使用具有伪标记的师生框架来利用未标记的点云。然而，在多样化的3D空间中产生可靠的伪标签仍然具有挑战性。在这项工作中，我们提出了Diffusion-SS3D，这是一种通过半监督3D对象检测的扩散模型来提高伪标签质量的新视角。具体来说，我们包括噪声来产生损坏的3D对象大小和类标签分布，然后利用扩散模型作为去噪过程来获得边界框输出。此外，我们将扩散模型集成到师生框架中，从而可以使用去噪的边界框来改进伪标签的生成，以及整个半监督学习过程。我们在ScanNet和SUN RGB-D基准数据集上进行了实验，以证明我们的方法相对于现有方法实现了最先进的性能。我们还进行了广泛的分析，以了解我们的扩散模型设计如何影响半监督学习的性能。 et.al.|[2312.02966](http://arxiv.org/abs/2312.02966)|null|
|**2023-12-05**|**Drag-A-Video: Non-rigid Video Editing with Point-based Interaction**|视频编辑是一项具有挑战性的任务，需要在空间和时间维度上操纵视频。现有的视频编辑方法主要集中在改变视频中对象的外观或风格，同时保持其结构不变。然而，没有现有的方法允许用户交互式地“拖动”第一帧上实例的任何点，以在其他帧一致变形的情况下精确地到达目标点。在本文中，我们提出了一种新的基于扩散的交互式点视频操作方法，称为Drag-a-video。我们的方法允许用户在输入视频的第一帧上单击成对的控制点和目标点以及遮罩。然后，我们的方法将输入转换为点集，并在帧之间传播这些集。为了精确地修改视频的内容，我们采用了一种新的视频级运动监督来更新视频的特征，并引入潜在的偏移量，以在多个去噪时间步长实现这种更新。我们提出了一个时间一致的点跟踪模块来协调句柄点集中的点的移动。我们在各种视频中展示了我们的方法的有效性和灵活性。我们的作品网站可在此处获取：https://drag-a-video.github.io/. et.al.|[2312.02936](http://arxiv.org/abs/2312.02936)|null|
|**2023-12-05**|**WoVoGen: World Volume-aware Diffusion for Controllable Multi-camera Driving Scene Generation**|生成多摄像头街景视频对于增强自动驾驶数据集、满足对广泛多样数据的迫切需求至关重要。由于多样性的限制和处理照明条件的挑战，传统的基于渲染的方法越来越多地被基于扩散的方法所取代。然而，基于扩散的方法面临的一个重大挑战是确保生成的传感器数据保持世界内一致性和传感器间一致性。为了应对这些挑战，我们结合了一个额外的显式世界体积，并提出了世界体积感知多摄像头驾驶场景生成器（WoVoGen）。该系统专门设计用于利用4D世界体积作为视频生成的基础元素。我们的模型分为两个不同的阶段：（i）基于车辆控制序列设想未来的4D时间世界体积，以及（ii）根据这种设想的4D时间空间体积和传感器互连性生成多摄像机视频。4D世界卷的加入不仅使WoVoGen能够响应车辆控制输入生成高质量的街景视频，还可以促进场景编辑任务。 et.al.|[2312.02934](http://arxiv.org/abs/2312.02934)|null|
|**2023-12-05**|**Assessing Nonlinear Diffusion Acceleration for Boltzmann Fokker Planck Equation in Slab Geometry**|通过像源迭代这样的迭代过程，Boltzmann-Fokker-Planck解的收敛可以变得任意缓慢。本文推导并研究了求解板几何中Boltzmann—Fokker—Planck方程的非线性扩散加速格式。该方法是一种传统的高阶低阶格式，具有传统的扩散加漂移低阶系统。然而，该方法与早期的变体不同，因为低阶方程的定义是根据玻尔兹曼-福克-普朗克方程的零阶和一阶矩进行调整的。对于所考虑的问题，我们观察到，NDA加速解决方案遵循了未加速的好方法，并且与源迭代相比，在迭代次数和运行时间方面提供了大约一个数量级的节约。 et.al.|[2312.02930](http://arxiv.org/abs/2312.02930)|null|
|**2023-12-05**|**LivePhoto: Real Image Animation with Text-guided Motion Control**|尽管最近在文本到视频的生成方面取得了进展，但现有的研究通常忽略了合成视频中只有空间内容而不是时间运动受文本控制的问题。面对这样的挑战，这项工作提出了一个实用的系统，名为LivePhoto，它允许用户通过文本描述来动画化他们感兴趣的图像。我们首先建立一个强大的基线，帮助学习良好的文本到图像生成器（即稳定扩散）将图像作为进一步的输入。然后，我们为改进的生成器配备了用于时间建模的运动模块，并提出了一个精心设计的训练管道，以更好地连接文本和运动。特别地，考虑到（1）文本只能粗略地描述运动（例如，与移动速度无关）和（2）文本可能包括内容和运动描述这两个事实，我们引入了运动强度估计模块以及文本重新加权模块，以减少文本到运动映射的模糊性。经验证据表明，我们的方法能够很好地将与运动相关的文本指令解码成视频，例如动作、相机运动，甚至凭空变出新的内容（例如，将水倒进空玻璃中）。有趣的是，由于所提出的强度学习机制，我们的系统除了为视频定制提供文本之外，还为用户提供了额外的控制信号（即运动强度）。 et.al.|[2312.02928](http://arxiv.org/abs/2312.02928)|null|
|**2023-12-05**|**A Diffusion Model of Dynamic Participant Inflow Management**|本文研究了一个扩散控制问题，其动机是公共卫生机构运营诊所为公众服务所面临的挑战。这些机构面临的一个关键挑战是激励个人参与所提供的服务。他们必须管理（自愿）参与者的流动，以使诊所的能力得到高度利用，但不会不堪重负。该组织可以部署成本高昂的推广活动，以增加参与者的流入。理想情况下，系统管理员希望有足够的参与者排队等候，为尽可能多的个人提供服务，并有效地利用诊所的容量。然而，如果报名人数过多，导致等待时间过长，参与者可能会感到恼火，并在未来再次参加时犹豫不决。我们开发了一个管理参与者流入机制的扩散模型。每个机制对应于为扩散模型选择特定的漂移速率参数。系统管理者寻求最佳地平衡三种不同的成本：i）捕获拥塞问题的线性持有成本；ii）与浪费诊所容量和对公共卫生的负面影响相对应的闲置处罚，以及iii）推广活动的成本。我们证明了在长期平均成本准则下，参与者流入机制部署的嵌套阈值策略是最优的。在该策略中，随着队列中参与者数量的减少，系统管理器按成本的递增顺序逐步部署机制。我们推导了触发每个促销活动的队列长度阈值的显式公式，为系统管理员提供了何时使用每种机制的指导。 et.al.|[2312.02927](http://arxiv.org/abs/2312.02927)|null|
|**2023-12-05**|**Multimodal Prompt Perceiver: Empower Adaptiveness, Generalizability and Fidelity for All-in-One Image Restoration**|尽管取得了实质性进展，但一体化图像恢复（IR）在处理复杂的真实世界退化方面仍面临着持续的挑战。本文介绍了MPerciver：一种新的多模式即时学习方法，它利用稳定扩散（SD）先验来增强一体化图像恢复的自适应性、可推广性和保真度。具体来说，我们开发了一个双分支模块来掌握两种类型的SD提示：用于整体表示的文本提示和用于多尺度细节表示的视觉提示。这两个提示都通过CLIP图像编码器的退化预测进行动态调整，从而实现对各种未知退化的自适应响应。此外，插件细节细化模块通过直接编码器到解码器的信息转换来提高恢复保真度。为了评估我们的方法，MPerciver接受了9项任务的一体式IR训练，在大多数任务中都优于最先进的特定任务方法。在多任务预训练后，MPerciver在低水平视觉中获得了广泛的表现，在看不见的任务中表现出显著的零样本和少速能力。在16个IR任务和26个基准上进行的大量实验强调了MPerciver在适应性、可推广性和保真度方面的优势。 et.al.|[2312.02918](http://arxiv.org/abs/2312.02918)|null|

<p align=right>(<a href=#updated-on-20231206>back to top</a>)</p>

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

<p align=right>(<a href=#updated-on-20231206>back to top</a>)</p>

[contributors-shield]: https://img.shields.io/github/contributors/Vincentqyw/cv-arxiv-daily.svg?style=for-the-badge
[contributors-url]: https://github.com/Vincentqyw/cv-arxiv-daily/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/Vincentqyw/cv-arxiv-daily.svg?style=for-the-badge
[forks-url]: https://github.com/Vincentqyw/cv-arxiv-daily/network/members
[stars-shield]: https://img.shields.io/github/stars/Vincentqyw/cv-arxiv-daily.svg?style=for-the-badge
[stars-url]: https://github.com/Vincentqyw/cv-arxiv-daily/stargazers
[issues-shield]: https://img.shields.io/github/issues/Vincentqyw/cv-arxiv-daily.svg?style=for-the-badge
[issues-url]: https://github.com/Vincentqyw/cv-arxiv-daily/issues

