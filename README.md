[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]

## Updated on 2023.12.23
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
|**2023-12-21**|**SyncDreamer for 3D Reconstruction of Endangered Animal Species with NeRF and NeuS**|本研究的主要目的是演示如何使用创新的视图合成和3D重建技术，使用单目RGB图像创建濒危物种的模型。为了实现这一点，我们使用SyncDreamer来产生独特的视角，并使用NeuS和NeRF来重建3D表示。我们选择了四种不同的动物，包括东方鹳、青蛙、蜻蜓和老虎，作为我们的研究对象。我们的研究结果表明，SyncDreamer、NeRF和NeuS技术的结合可以成功创建濒危动物的3D模型。然而，我们也观察到NeuS产生了模糊的图像，而NeRF产生了更清晰但更嘈杂的图像。这项研究突出了模拟濒危动物的潜力，并为该领域的未来研究提供了新的方向。通过展示这些先进技术的有效性，我们希望鼓励进一步探索和发展保护和研究濒危物种的技术。 et.al.|[2312.13832](http://arxiv.org/abs/2312.13832)|null|
|**2023-12-21**|**DyBluRF: Dynamic Deblurring Neural Radiance Fields for Blurry Monocular Video**|视频视图合成允许从任意视点和时间创建具有视觉吸引力的帧，提供身临其境的观看体验。神经辐射场，特别是最初为静态场景开发的NeRF，刺激了视频视图合成的各种方法的产生。然而，视频视图合成的挑战来自运动模糊，这是物体或相机在曝光过程中移动的结果，阻碍了清晰的时空视图的精确合成。作为回应，我们提出了一种用于模糊单目视频的新的动态去模糊NeRF框架，称为DyBluRF，由Interleave Ray Refinement（IRR）阶段和基于运动分解的去模糊（MDD）阶段组成。我们的DyBluRF是第一个解决和处理模糊单目视频的新型视图合成的公司。IRR阶段联合重建动态3D场景，并细化不准确的相机姿态信息，以对抗从给定模糊帧中提取的不准确姿态信息。MDD阶段是一种新的增量潜在锐射线预测（ILSP）方法，用于模糊单目视频帧，将潜在锐射线分解为全局相机运动和局部对象运动分量。大量的实验结果表明，我们的DyBluRF在质量和数量上都优于最新的最先进的方法。我们的项目页面包括源代码和预训练模型，可在https://kaist-viclab.github.io/dyblurf-site/. et.al.|[2312.13528](http://arxiv.org/abs/2312.13528)|null|
|**2023-12-20**|**NeRF-VO: Real-Time Sparse Visual Odometry with Neural Radiance Fields**|我们介绍了一种新的单目视觉里程计（VO）系统NeRF VO，该系统集成了用于低延迟相机跟踪的基于学习的稀疏视觉里程计和用于复杂密集重建和新颖视图合成的神经辐射场景表示。我们的系统使用稀疏视觉里程计初始化相机姿态，并从单目深度预测网络中获得与视图相关的密集几何先验。我们协调姿势的尺度和密集的几何体，将它们视为训练神经隐式场景表示的监督线索。NeRF VO通过联合优化关键帧姿势的滑动窗口和底层密集几何体，在场景表示的光度和几何保真度方面表现出非凡的性能，这是通过使用体渲染训练辐射场来实现的。我们在各种合成和真实世界数据集的姿态估计精度、新颖的视图合成保真度和密集的重建质量方面超过了最先进的方法，同时实现了更高的相机跟踪频率和更少的GPU内存消耗。 et.al.|[2312.13471](http://arxiv.org/abs/2312.13471)|null|
|**2023-12-20**|**SWAGS: Sampling Windows Adaptively for Dynamic 3D Gaussian Splatting**|最近，新的视图合成显示出快速的进展，其方法能够产生越来越逼真的结果。3D高斯飞溅已成为一种特别有前途的方法，可以产生高质量的静态场景渲染，并实现实时帧率的交互式观看。然而，它目前仅限于静态场景。在这项工作中，我们扩展了三维高斯飞溅来重建动态场景。我们使用可调MLP对场景的动力学进行建模，该MLP学习从规范空间到每帧一组3D高斯的变形场。为了理清场景的静态和动态部分，我们为每个高斯学习一个可调谐的参数，该参数对各自的MLP参数进行加权，以将注意力集中在动态部分上。这提高了模型在静态区域与动态区域不平衡的场景中捕捉动态的能力。为了处理任意长度的场景，同时保持高渲染质量，我们引入了一种自适应窗口采样策略，根据序列中的移动量将序列划分为多个窗口。我们为每个窗口训练一个单独的动态高斯飞溅模型，允许规范表示发生变化，从而能够重建具有显著几何或拓扑变化的场景。在随机采样的新视图上，使用具有自监督一致性损失的微调步骤来增强时间一致性。因此，我们的方法可以生成具有竞争性定量性能的一般动态场景的高质量渲染图，可以使用我们的动态交互式查看器实时查看。 et.al.|[2312.13308](http://arxiv.org/abs/2312.13308)|null|
|**2023-12-21**|**DiffPortrait3D: Controllable Diffusion for Zero-Shot Portrait View Synthesis**|我们提出了DiffPortrait3D，这是一种条件扩散模型，能够从野生肖像中的一张照片中合成3D一致的照片逼真的新颖视图。具体来说，在给定单个RGB输入的情况下，我们的目标是合成从新颖的相机视图中呈现的看似合理但一致的面部细节，同时保留身份和面部表情。除了耗时的优化和微调外，我们的零样本方法很好地推广到任意面部肖像，具有无污染的相机视图、极端的面部表情和多样化的艺术描绘。其核心是，我们利用在大规模图像数据集上预先训练的2D扩散模型的生成先验作为我们的渲染骨干，而去噪是通过对外观和相机姿态的细致控制来指导的。为了实现这一点，我们首先将参考图像的外观上下文注入冻结的UNets的自关注层。然后利用新颖的条件控制模块来操纵渲染视图，该条件控制模块通过从同一视图观看交叉对象的条件图像来解释相机姿态。此外，我们插入了一个可训练的跨视图注意力模块来增强视图一致性，在推理过程中，通过一个新颖的3D感知噪声生成过程进一步增强了视图一致性。我们在野外和多视图基准测试中展示了最先进的定性和定量结果。 et.al.|[2312.13016](http://arxiv.org/abs/2312.13016)|**[link](https://github.com/FreedomGu/DiffPortrait3D)**|
|**2023-12-20**|**Radar Fields: An Extension of Radiance Fields to SAR**|辐射场是多视图图像采集中复杂场景的反向渲染、新颖视图合成和3D建模领域的一个重大突破。自从它们被引入以来，已经表明它们可以扩展到其他模式，如激光雷达、射频、X射线或超声波。在本文中，我们表明，尽管光学和合成孔径雷达（SAR）图像形成模型之间存在重要差异，但有可能将辐射场扩展到雷达图像，从而呈现第一个“雷达场”。这使我们能够仅使用雷达图像的集合来学习表面模型，类似于规则辐射场的学习方式，并且平均具有相同的计算复杂度。由于这两个领域的定义方式相似，这项工作也显示了将光学图像和SAR图像相结合的混合方法的潜力。 et.al.|[2312.12961](http://arxiv.org/abs/2312.12961)|null|
|**2023-12-21**|**pixelSplat: 3D Gaussian Splats from Image Pairs for Scalable Generalizable 3D Reconstruction**|我们介绍了pixelSplat，这是一种前馈模型，它学习从成对的图像中重建由3D高斯基元参数化的3D辐射场。我们的模型具有实时和内存高效的渲染功能，可进行可扩展训练，并在推理时进行快速3D重建。为了克服稀疏和局部支持表示固有的局部极小值，我们预测了三维上的稠密概率分布，并根据该概率分布对高斯均值进行采样。我们通过重新参数化技巧使这种采样操作可微分，允许我们通过高斯飞溅表示反向传播梯度。我们在真实世界的RealEstate10k和ACID数据集上以宽基线新视图合成为基准，在那里我们优于最先进的光场变换器，并将渲染加速2.5个数量级，同时重建可解释和可编辑的3D辐射场。 et.al.|[2312.12337](http://arxiv.org/abs/2312.12337)|null|
|**2023-12-20**|**MixRT: Mixed Neural Representations For Real-Time NeRF Rendering**|神经辐射场（NeRF）由于其令人印象深刻的真实感重建和渲染能力，已成为新型视图合成的领先技术。然而，在大规模场景中实现实时NeRF渲染带来了挑战，通常导致采用具有大量三角形的复杂烘焙网格表示或烘焙表示中的资源密集型光线行进。我们对这些约定提出了质疑，注意到由具有实质三角形的网格表示的高质量几何体对于实现照片级真实感渲染质量是不必要的。因此，我们提出了MixRT，这是一种新的NeRF表示，包括低质量网格、视图相关位移图和压缩的NeRF模型。这种设计有效地利用了现有图形硬件的功能，从而实现了边缘设备上的实时NeRF渲染。利用高度优化的基于WebGL的渲染框架，我们提出的MixRT在边缘设备上实现了实时渲染速度（在MacBook M1 Pro笔记本电脑上以1280 x 720的分辨率超过30 FPS）、更好的渲染质量（在Unboundd-360数据集的室内场景中高出0.2 PSNR）和更小的存储大小（与最先进的方法相比，小于80%）。 et.al.|[2312.11841](http://arxiv.org/abs/2312.11841)|null|
|**2023-12-18**|**GauFRe: Gaussian Deformation Fields for Real-time Dynamic Novel View Synthesis**|我们提出了一种使用可变形3D高斯进行动态场景重建的方法，该方法适用于单目视频。在高斯飞溅效率的基础上，我们的方法通过位于规范空间中的可变形高斯集和由多层感知器（MLP）定义的时间相关变形场来扩展表示以适应动态元素。此外，在大多数自然场景都有保持静态的大区域的假设下，我们允许MLP通过额外包括静态高斯点云来集中其代表能力。串联的动态和静态点云形成高斯飞溅光栅化器的输入，从而实现实时渲染。在自监督渲染损失的情况下，对可微管道进行端到端优化。我们的方法获得的结果与最先进的动态神经辐射场方法相当，同时允许更快的优化和渲染。项目网站：https://lynl7130.github.io/gaufre/index.html et.al.|[2312.11458](http://arxiv.org/abs/2312.11458)|null|
|**2023-12-18**|**SinMPI: Novel View Synthesis from a Single Image with Expanded Multiplane Images**|单图像新视图合成是一个具有挑战性且正在进行的问题，其目的是从单个输入图像生成无限数量的一致视图。尽管已经做出了重大努力来提高生成的新视图的质量，但对底层场景表示的扩展却关注较少，这对生成逼真的新视图图像至关重要。本文提出了SinMPI，这是一种使用扩展多平面图像（MPI）作为3D场景表示的新方法，可以显著扩展MPI的透视范围，并从大的多平面空间生成高质量的新视图。我们的方法的关键思想是使用稳定扩散生成视图外内容，根据单目深度估计器预测的深度将所有场景内容投影到扩展的多平面图像中，然后在深度感知扭曲和修复模块生成的伪多视图数据的监督下优化多平面图像。我们进行了定性和定量实验，以验证我们的方法相对于现有技术的优越性。我们的代码和数据可在https://github.com/trickygo/sinmpi. et.al.|[2312.11037](http://arxiv.org/abs/2312.11037)|**[link](https://github.com/trickygo/sinmpi)**|

<p align=right>(<a href=#updated-on-20231223>back to top</a>)</p>

## 3D Reconstruction

|Publish Date|Title|Abstract|PDF|Code|
|---|---|---|---|---|
|**2023-12-21**|**3D Pose Estimation of Two Interacting Hands from a Monocular Event Camera**|由于手的相互作用、遮挡、左右手模糊和快速运动，单目视频中的3D手跟踪是一个非常具有挑战性的问题。大多数现有的方法都依赖于RGB输入，而RGB输入在弱光条件下具有严重的局限性，并且存在运动模糊。相比之下，事件相机捕捉局部亮度变化而不是完整的图像帧，并且不会受到所描述的效果的影响。不幸的是，由于数据模态的显著差异，现有的基于图像的技术不能直接应用于事件。为了应对这些挑战，本文介绍了第一个从单目事件相机对两个快速移动和相互作用的手进行3D跟踪的框架。我们的方法使用一种新颖的半监督特征式注意力机制来解决左右手模糊问题，并集成交叉点损失来修复手碰撞。为了促进这一研究领域的进展，我们发布了一个由两只相互作用的手组成的新的合成大规模数据集Ev2Hands-S，以及一个具有真实事件流和地面实况3D注释的新的真实基准Ev2Hands-R。在3D重建精度方面，我们的方法优于现有方法，并在恶劣的光照条件下推广到真实数据。 et.al.|[2312.14157](http://arxiv.org/abs/2312.14157)|null|
|**2023-12-21**|**DUSt3R: Geometric 3D Vision Made Easy**|野外的多视角立体重建（MVS）需要首先估计相机参数，例如内在和外在参数。这些通常是乏味和繁琐的，但它们必须在3D空间中对相应的像素进行三角测量，这是所有性能最好的MVS算法的核心。在这项工作中，我们采取了相反的立场，并引入了DUSt3R，这是一种对任意图像集合进行密集和无约束立体3D重建的全新范式，即在没有关于相机校准或视点姿态的先验信息的情况下操作。我们将成对重建问题视为点图的回归，放松了通常投影相机模型的硬约束。我们证明了这个公式平滑地统一了单目和双目重建的情况。在提供两个以上图像的情况下，我们进一步提出了一种简单而有效的全局对齐策略，该策略在公共参考系中表达所有成对的点图。我们的网络架构基于标准的Transformer编码器和解码器，使我们能够利用强大的预训练模型。我们的公式直接提供了场景的3D模型以及深度信息，但有趣的是，我们可以从中无缝恢复，像素匹配，相对和绝对相机。对所有这些任务的详尽实验表明，所提出的DUSt3R可以统一各种3D视觉任务，并在单目/多视角深度估计和相对姿态估计上设置新的SoTA。总之，DUSt3R使许多几何三维视觉任务变得容易。 et.al.|[2312.14132](http://arxiv.org/abs/2312.14132)|null|
|**2023-12-21**|**Anatomical basis of sex differences in human post-myocardial infarction ECG phenotypes identified by novel automated torso-cardiac 3D reconstruction**|心电图（ECG）在心脏病学中经常使用，尽管其解释因解剖变异而混淆。一种新颖的自动计算管道能够从磁共振成像中量化躯干心室解剖指标，并与心电图特征进行比较。基于英国生物银行的1051名健康受试者和425名心肌梗死后受试者，研究了性别和心肌梗死的差异。女性较小的心室比男性解释了约50%的QRS持续时间较短，并导致女性STJ振幅较低（也是由于更靠上和靠后的位置）。在女性中，躯干心室解剖结构，特别是来自较大BMI的解剖结构，比男性更能调节MI后T波振幅降低和左偏R轴角。因此，女性MI表型较少反映病理，基线STJ振幅和QRS持续时间离临床阈值更远。因此，量化解剖性别差异及其对健康和疾病心电图的影响对于避免临床性别偏见至关重要。 et.al.|[2312.13976](http://arxiv.org/abs/2312.13976)|null|
|**2023-12-21**|**SyncDreamer for 3D Reconstruction of Endangered Animal Species with NeRF and NeuS**|本研究的主要目的是演示如何使用创新的视图合成和3D重建技术，使用单目RGB图像创建濒危物种的模型。为了实现这一点，我们使用SyncDreamer来产生独特的视角，并使用NeuS和NeRF来重建3D表示。我们选择了四种不同的动物，包括东方鹳、青蛙、蜻蜓和老虎，作为我们的研究对象。我们的研究结果表明，SyncDreamer、NeRF和NeuS技术的结合可以成功创建濒危动物的3D模型。然而，我们也观察到NeuS产生了模糊的图像，而NeRF产生了更清晰但更嘈杂的图像。这项研究突出了模拟濒危动物的潜力，并为该领域的未来研究提供了新的方向。通过展示这些先进技术的有效性，我们希望鼓励进一步探索和发展保护和研究濒危物种的技术。 et.al.|[2312.13832](http://arxiv.org/abs/2312.13832)|null|
|**2023-12-21**|**Visual Tomography: Physically Faithful Volumetric Models of Partially Translucent Objects**|当从真实世界的数据中忠实地创建时，对象的数字3D表示可用于人类或计算机辅助分析。这种模型还可以用于在难以获得数据或训练数据太少的情况下，例如通过在不同条件下提供新的视图或图像，为机器学习方法生成训练数据。虽然大量的视觉3D重建方法侧重于非物理模型、纹理物体表面或形状，但在这篇文章中，我们提出了一种体积重建方法，该方法可以获得包括浮游生物或昆虫等部分半透明物体内部的物理模型。我们的技术在明亮的白色光源前拍摄不同姿势的物体，并计算每个体素的吸收和散射。它可以解释为我们通过反向光线追踪解决的视觉断层扫描。我们还提出了一种将非物理NeRF介质转换为基于物理的体积网格进行初始化的方法，并使用两个真实世界的浮游生物验证集说明了该方法的有用性，实验室扫描的模型最终也被重新照明，并在具有增强介质和照明条件的场景中被虚拟淹没。请访问项目主页www.marine.informattik.uni-kiel.de/go/vito et.al.|[2312.13494](http://arxiv.org/abs/2312.13494)|null|
|**2023-12-20**|**UniSDF: Unifying Neural Representations for High-Fidelity 3D Reconstruction of Complex Scenes with Reflections**|神经3D场景表示已经显示出从2D图像进行3D重建的巨大潜力。然而，重建复杂场景的真实世界捕捉仍然是一个挑战。现有的通用3D重建方法通常难以表示精细的几何细节，并且不能充分地对大规模场景的反射表面进行建模。明确关注反射表面的技术可以通过利用更好的反射参数化来对复杂和详细的反射进行建模。然而，我们观察到，在存在非反射和反射组件的真实无界场景中，这些方法通常是不稳健的。在这项工作中，我们提出了UniSDF，这是一种通用的3D重建方法，可以重建具有反射的大型复杂场景。我们研究了基于视图和基于反射的颜色预测参数化技术，发现在3D空间中显式混合这些表示可以重建几何精度更高的表面，尤其是反射表面。我们进一步将这种表示与多分辨率网格主干相结合，该主干以从粗到细的方式进行训练，从而实现比先前方法更快的重建。在对象级数据集DTU、Shiny Blender以及无界数据集Mip NeRF 360和Ref NeRF real上进行的大量实验表明，我们的方法能够稳健地重建具有精细细节和反射表面的复杂大规模场景。请参阅我们的项目页面https://fangjinhuawang.github.io/unisdf. et.al.|[2312.13285](http://arxiv.org/abs/2312.13285)|null|
|**2023-12-20**|**Splatter Image: Ultra-Fast Single-View 3D Reconstruction**|我们介绍了飞溅图像，这是一种用于单目3D对象重建的超快速方法，其操作速度为38 FPS。飞溅图像是基于高斯飞溅的，它最近为多视图重建带来了实时渲染、快速训练和出色的缩放能力。我们首次在单目重建设置中应用高斯散射。我们的方法是基于学习的，在测试时，重建只需要对神经网络进行前馈评估。Splatter Image的主要创新是令人惊讶的简单设计：它使用2D图像到图像网络将输入图像映射到每个像素一个3D高斯。由此产生的高斯图像具有图像的形式，即飞溅图像。我们进一步扩展了该方法，将多个图像作为输入，我们通过添加跨视图注意力来实现这一点。由于渲染器的速度（588 FPS），我们可以使用单个GPU进行训练，同时在每次迭代时生成整个图像，以优化LPIPS等感知指标。在标准基准上，我们不仅证明了快速重建，而且在PSNR、LPIPS和其他指标方面，比最近的更昂贵的基线取得了更好的结果。 et.al.|[2312.13150](http://arxiv.org/abs/2312.13150)|**[link](https://github.com/szymanowiczs/splatter-image)**|
|**2023-12-21**|**pixelSplat: 3D Gaussian Splats from Image Pairs for Scalable Generalizable 3D Reconstruction**|我们介绍了pixelSplat，这是一种前馈模型，它学习从成对的图像中重建由3D高斯基元参数化的3D辐射场。我们的模型具有实时和内存高效的渲染功能，可进行可扩展训练，并在推理时进行快速3D重建。为了克服稀疏和局部支持表示固有的局部极小值，我们预测了三维上的稠密概率分布，并根据该概率分布对高斯均值进行采样。我们通过重新参数化技巧使这种采样操作可微分，允许我们通过高斯飞溅表示反向传播梯度。我们在真实世界的RealEstate10k和ACID数据集上以宽基线新视图合成为基准，在那里我们优于最先进的光场变换器，并将渲染加速2.5个数量级，同时重建可解释和可编辑的3D辐射场。 et.al.|[2312.12337](http://arxiv.org/abs/2312.12337)|null|
|**2023-12-19**|**EVI-SAM: Robust, Real-time, Tightly-coupled Event-Visual-Inertial State Estimation and 3D Dense Mapping**|事件摄像机是受生物启发的运动激活传感器，在处理具有挑战性的情况（如运动模糊和高动态范围）方面表现出巨大的潜力。在本文中，我们提出了EVI-SAM来解决使用单目事件相机进行6自由度姿态跟踪和三维重建的问题。利用特征匹配的鲁棒性和直接对准的精度，设计了一种新的基于事件的混合跟踪框架来估计姿态。具体来说，我们开发了一种基于事件的2D-2D对齐来构建光度约束，并将其与基于事件的重投影约束紧密集成。映射模块通过基于图像引导的事件映射方法来恢复场景的密集和丰富多彩的深度。随后，可以通过使用截断符号距离函数（TSDF）融合来自多个视点的密集深度图来重建3D场景的外观、纹理和表面网格。据我们所知，这是第一个实现基于事件的密集映射的非学习工作。在公开的和自行收集的数据集上进行了数值评估，定性和定量地证明了我们方法的优越性能。我们的EVI-SAM有效地平衡了准确性和稳健性，同时保持了计算效率，在具有挑战性的场景中展示了卓越的姿态跟踪和密集映射性能。视频演示：https://youtu.be/nn40u4e5si8. et.al.|[2312.11911](http://arxiv.org/abs/2312.11911)|null|
|**2023-12-17**|**Primitive-based 3D Human-Object Interaction Modelling and Programming**|在三维环境中嵌入人与关节对象交互（HAOI）是深入理解人类活动的一个重要方向。与以往使用参数化和CAD模型来表示人和物体的工作不同，在这项工作中，我们提出了一种新的基于三维几何图元的语言来对人和物体进行编码。在我们的新范式下，人和物体都是原语的组成部分，而不是异构实体。因此，可以在人类的有限3D数据和不同对象类别之间实现相互信息学习。此外，考虑到表达式的简单性和所包含信息的丰富性，我们选择超二次曲面作为原始表示。为了探索机器的HAOI的有效嵌入，我们在由基元及其图像组成的3D HAOI上建立了一个新的基准，并提出了一项任务，要求机器使用图像中的基元恢复三维HAOI。此外，我们提出了基于HAOI的单视图三维重建的基线。我们相信，这种基于原始的3D HAOI表示将为3D HAOI研究铺平道路。我们的代码和数据可在https://mvig-rhos.com/p3haoi. et.al.|[2312.10714](http://arxiv.org/abs/2312.10714)|null|

<p align=right>(<a href=#updated-on-20231223>back to top</a>)</p>

## Diffusion

|Publish Date|Title|Abstract|PDF|Code|
|---|---|---|---|---|
|**2023-12-21**|**Diffusion Reward: Learning Rewards via Conditional Video Diffusion**|从专家视频中获得的学习奖励提供了一种经济有效的解决方案，可以指定强化学习任务的预期行为。在这项工作中，我们提出了Diffusion-Reward，这是一种新的框架，通过条件视频扩散模型从专家视频中学习奖励，用于解决复杂的视觉RL问题。我们的关键见解是，当以专家轨迹为条件时，会观察到较低的生成多样性。扩散奖励相应地通过条件熵的负值形式化，条件熵鼓励对类似专家的行为进行富有成效的探索。我们展示了我们的方法在MetaWorld和Adroit的10个机器人操作任务中的有效性，这些任务具有视觉输入和稀疏奖励。此外，扩散奖励甚至可以成功有效地解决看不见的任务，大大超过了基线方法。项目页面和代码：https://diffusion-reward.github.io/. et.al.|[2312.14134](http://arxiv.org/abs/2312.14134)|null|
|**2023-12-21**|**Neural Point Cloud Diffusion for Disentangled 3D Shape and Appearance Generation**|3D资产的可控生成对于许多实际应用非常重要，如电影、游戏和工程以及AR/VR中的内容创建。最近，扩散模型在3D对象的生成质量方面显示出显著的结果。然而，现有的模型都无法使解纠缠的生成分别控制形状和外观。我们首次通过引入混合点云和神经辐射场方法，为3D扩散模型提供了一种合适的表示方式，以实现这种解纠缠。我们将点位置上的扩散过程与局部密度和辐射解码器的高维特征空间联合建模。虽然点位置表示对象的粗略形状，但点特征允许对几何体和外观细节进行建模。这种解纠缠使我们能够独立地对两者进行采样，从而分别控制两者。与以前的具有解纠缠能力的方法相比，我们的方法在生成方面创下了新的技术水平，FID得分降低了30-90%，与其他不具有解纠缠功能的技术水平方法不相上下。 et.al.|[2312.14124](http://arxiv.org/abs/2312.14124)|**[link](https://github.com/lmb-freiburg/neural-point-cloud-diffusion)**|
|**2023-12-21**|**HD-Painter: High-Resolution and Prompt-Faithful Text-Guided Image Inpainting with Diffusion Models**|基于文本到图像扩散模型的空前成功，文本引导图像修复的最新进展已经产生了异常逼真和视觉上合理的结果。然而，当前的文本到图像修复模型仍有很大的改进潜力，特别是在更好地将修复区域与用户提示对齐和执行高分辨率修复方面。因此，在本文中，我们介绍了HD Painter，这是一种完全无训练的方法，可以准确地遵循提示并连贯地缩放到高分辨率图像修复。为此，我们设计了提示感知内向注意力（PAIntA）层，通过提示信息提高自我注意力得分，并产生更好的文本对齐生成。为了进一步提高即时一致性，我们引入了重新加权注意力得分指导（RASG）机制，将事后抽样策略无缝集成到一般形式的DDIM中，以防止分布外的潜在转变。此外，HD Painter通过引入专门为修复而定制的超分辨率技术，可以扩展到更大的规模，从而完成高达2K分辨率的图像中的缺失区域。我们的实验表明，HD Painter在质量和数量上都超过了现有的最先进的方法，实现了61.4%和51.9%的令人印象深刻的生成精度提高。我们将在以下网站上公开代码：https://github.com/picsart-ai-research/hd-painter et.al.|[2312.14091](http://arxiv.org/abs/2312.14091)|**[link](https://github.com/picsart-ai-research/hd-painter)**|
|**2023-12-21**|**Designing Artificial Intelligence Equipped Social Decentralized Autonomous Organizations for Tackling Sextortion Cases Version 0.7**|随着社交网络与移动电话的迅速普及，出现了一种新的性侵犯社会威胁，弱势年轻女性基本上被其露骨的共享多媒体内容勒索。心理学家、社会学家、犯罪学家等现在对性侵犯现象进行了广泛研究。这些发现已经转化为非政府组织、专业执法单位和治疗师的零散帮助，他们通常不会相互协调。本文解决了缺乏协调系统以有效和高效地使用现代信息技术的差距，这些信息技术使分散和不一致的性侵权帮助组织的努力保持一致。因此，本文不仅调查了系统设计和开发的目标、激励因素和抑制因素，该系统不仅有效地管理各种性侵犯受害者案件，而且有针对性地利用人工智能。它探讨了人工智能，特别是自主认知实体如何改进受害者档案分析，简化支持机制，并为性侵犯案件提供智能洞察。此外，本文从概念上研究了这些努力可以在多大程度上以可持续的方式货币化。遵循可信区块链去中心化应用程序设计的新设计方法，本文提出了一组概念需求和系统模型，在此基础上可以推导出快速实施部署的最佳实践技术堆栈。 et.al.|[2312.14090](http://arxiv.org/abs/2312.14090)|null|
|**2023-12-21**|**The influence of controlled vibration effects on fluid flow**|本文介绍了研究结果，证明了在振动谐波效应下层流的非线性效应对流体流动和传热的影响。本文总结了振动对各种流体流动问题影响的研究结果。显示了在各种单晶生长过程中，周期振荡对扩散器中非对称流的对称性、瑞利-伯纳德对流和边界层宽度的影响。 et.al.|[2312.14079](http://arxiv.org/abs/2312.14079)|null|
|**2023-12-21**|**Tearing-mediated reconnection in magnetohydrodynamic poorly ionized plasmas. I. Onset and linear evolution**|在高伦德奎斯特数等离子体中，重新连接通过撕裂的开始进行，随后是非线性阶段，在该阶段等离子体团连续形成、合并并从电流片（CS）中喷出。这一过程可以在完全电离的磁流体动力学等离子体中理解。然而，许多等离子体环境，如恒星形成的分子云和太阳色球层，电离较差。我们使用理论和计算来研究这种低电离系统中撕裂介导的重联。在本文中，我们重点讨论了这一过程的开始和线性演化。在低电离等离子体中，低于 $v_｛\rm A，n0｝/\nu_｛\ rm ni0｝$的磁零点，其中$v_{e}n速度和$\nu_｛\rm ni0｝$中性离子碰撞频率将通过双极扩散自锐化。这种锐化以越来越快的速度发生，抑制了重新连接的开始。然而，一旦CS变得足够薄，离子就会与中性离子解耦，CS的变薄速度就会减慢，从而使撕裂在$\nu_｛\rm ni0｝^｛-1｝$的时间内开始。我们发现，首先破坏成形片材的模式的波长和生长速率可以从电离不良的撕裂色散关系中预测；随着等离子体复合速率的增加和电离分数的降低，生长速率变为$\nu_｛ni0｝$的递增倍数，波长变为$ v_｛\rmA，n0｝/\nu_{\rm-ni0｝美元的递减分数。 et.al.|[2312.14076](http://arxiv.org/abs/2312.14076)|null|
|**2023-12-21**|**OH as a probe of the warm water cycle in planet-forming disks**|正如我们所知，水是生命出现的关键成分。然而，在温暖的气体中，水在太空中的破坏和改造仍然是不可能的。在这里，我们用詹姆斯·韦伯太空望远镜探测了暴露于外部远紫外线（FUV）辐射的行星形成盘的羟基自由基（OH）发射。观测结果与量子动力学计算的结果相矛盾。高度激发的OH红外旋转线是FUV破坏H2O的信号。OH红外ro振动线归因于通过关键反应O+H＝OH+H的化学激发，该反应在气相中形成水。我们推断，相当于地球海洋价值的水每月被破坏并补充。这些结果表明，在温暖和辐照的条件下，水通过气相反应被破坏并有效地重整。这一过程在扩散传输的帮助下，可以降低行星形成盘温暖区域的HDO/H2O比率。 et.al.|[2312.14056](http://arxiv.org/abs/2312.14056)|null|
|**2023-12-21**|**Identifying diffusive length scales in one-dimensional Bose gases**|在可积模型的流体力学中，扩散是对弹道传播的一种次级修正。在这里，我们量化了一维玻色气体的扩散贡献，并发现它在气体的主要热力学状态之间的交叉中影响最大。通过分析单个密度模式的实验测量动力学，我们发现扩散仅与高波长激发有关。相反，观察到的弛豫仅由弹道学驱动的去相位过程引起，其时间尺度与系统的声子寿命有关，因此有助于评估量子场模拟器中通常使用的声子基的适用性。 et.al.|[2312.14007](http://arxiv.org/abs/2312.14007)|null|
|**2023-12-21**|**Carve3D: Improving Multi-view Reconstruction Consistency for Diffusion Models with RL Finetuning**|文本到3D任务的最新进展利用微调的文本到图像扩散模型生成多视图图像，然后进行NeRF重建。然而，现有的监督微调（SFT）扩散模型仍然存在多视图不一致性和由此产生的NeRF伪影。尽管使用SFT进行更长时间的训练可以提高一致性，但它也会导致分布变化，从而减少多样性和逼真的细节。我们认为，多视图扩散模型的SFT类似于LLM对齐流水线的指令微调阶段，并且可以受益于RL微调（RLFT）方法。从本质上讲，RLFT方法通过使用自己的输出来优化超出其SFT数据分布的模型，从而有效地缓解分布偏移。为此，我们引入了Carve3D，这是一种结合多视图重建一致性（MRC）度量的RLFT方法，以提高多视图扩散模型的一致性。为了计算一组多视图图像的MRC，我们将它们与相同视点下重建的NeRF的相应渲染进行比较。我们通过在受控的不一致性水平下进行的大量实验验证了MRC的稳健性。我们增强了基本的RLFT算法，以稳定训练过程，减少分布偏移，并识别缩放规律。通过定性和定量实验，以及用户研究，我们证明了与较长的SFT相比，Carve3D提高了多视图一致性，从而获得了卓越的NeRF重建质量和最小的分布偏移。项目网页：https://desaixie.github.io/carve-3d. et.al.|[2312.13980](http://arxiv.org/abs/2312.13980)|null|
|**2023-12-21**|**Controllable 3D Face Generation with Conditional Style Code Diffusion**|根据给定条件生成照片级真实感三维人脸是一项具有挑战性的任务。现有的方法通常依赖于耗时的一个接一个的优化方法，这些方法对于对相同的分发内容（例如人脸）进行建模是无效的。此外，理想的可控3D人脸生成模型应该同时考虑人脸属性和表情。因此，我们提出了一种称为TEx-Face（TExt&Expression to Face）的新方法，该方法通过将任务分为三个部分来解决这些挑战，即3D GAN反转、条件风格代码扩散和3D人脸解码。对于三维GAN反演，我们介绍了两种方法，旨在增强样式代码的表示并减轻三维不一致性。此外，我们设计了一个风格代码去噪器，将多个条件合并到风格代码中，并提出了一种数据扩充策略，以解决配对视觉语言数据不足的问题。在FFHQ、CelebA-HQ和CelebA-Dialog上进行的大量实验证明了我们的TEx Face在实现高效可控的真实感3D人脸生成方面的良好性能。代码将在https://github.com/sxl142/tex-face. et.al.|[2312.13941](http://arxiv.org/abs/2312.13941)|**[link](https://github.com/sxl142/tex-face)**|

<p align=right>(<a href=#updated-on-20231223>back to top</a>)</p>

## NeRF

|Publish Date|Title|Abstract|PDF|Code|
|---|---|---|---|---|
|**2023-12-21**|**Geometric Awareness in Neural Fields for 3D Human Registration**|将模板与三维人体点云对齐是一个长期存在的问题，对于动画、重建和启用监督学习管道等任务至关重要。最近的数据驱动方法利用了预测的表面对应关系；然而，它们对不同的姿态或分布并不鲁棒。相比之下，工业解决方案往往依赖于昂贵的手动注释或多视图捕获系统。最近，神经场已经显示出有希望的结果，但它们纯粹的数据驱动性质缺乏几何意识，通常导致模板配准的微小错位。在这项工作中，我们提出了两种解决方案：LoVD，一种新的神经场模型，它预测朝向目标表面上的局部SMPL顶点的方向；和INT，这是第一个专门用于神经领域的自监督任务，在测试时，它利用目标几何结构来细化主干。我们将它们组合到INLoVD中，这是一个在大型MoCap数据集上训练的强大的3D人体注册管道。INLoVD是高效的（不到一分钟），在公共基准上稳定地达到了最先进的水平，并对分布外的数据提供了前所未有的概括。我们将在\url｛url｝中发布代码和检查点。 et.al.|[2312.14024](http://arxiv.org/abs/2312.14024)|null|
|**2023-12-20**|**Neural feels with neural fields: Visuo-tactile perception for in-hand manipulation**|为了实现人类水平的灵活性，机器人必须从多模式感知推断空间意识，以推理接触互动。在新物体的手操作过程中，这种空间意识包括估计物体的姿势和形状。手内感知的现状主要采用视觉，并局限于跟踪先验已知对象。此外，在操作过程中，手上物体的视觉遮挡迫在眉睫，这阻止了当前系统在没有遮挡的情况下超越任务。我们将多指手的视觉和触摸传感相结合，在手内操作过程中估计物体的姿势和形状。我们的方法NeuralFeels通过在线学习神经场来编码对象几何，并通过优化姿态图问题来联合跟踪它。我们研究了模拟和现实世界中的多模式手部感知，通过本体感觉驱动的策略与不同的物体进行交互。我们的实验显示，使用已知的CAD模型，最终重建F分数为 $81$%，平均姿势漂移为$4.7\，\text｛mm｝$，进一步降低到$2.3\，\text{mm｝$。此外，我们观察到，与仅使用视觉的方法相比，在严重的视觉遮挡下，我们可以实现高达94$ %的跟踪改进。我们的研究结果表明，在手部操作过程中，触摸至少可以改善视觉估计，并在最好的情况下消除视觉估计的歧义。我们发布了70个实验的评估数据集FeelSight，作为在该领域进行基准测试的一步。我们由多模态感知驱动的神经表示可以作为提高机器人灵活性的感知支柱。视频可以在我们的项目网站上找到https://suddhu.github.io/neural-feels/ et.al.|[2312.13469](http://arxiv.org/abs/2312.13469)|null|
|**2023-12-20**|**Deep Learning on 3D Neural Fields**|近年来，神经场（NFs）已成为编码各种连续信号（如图像、视频、音频和3D形状）的有效工具。当应用于3D数据时，NFs提供了一种解决方案来解决与流行的离散表示相关的碎片化和局限性。然而，鉴于神经网络本质上是神经网络，目前尚不清楚它们是否以及如何无缝集成到深度学习管道中，以解决下游任务。本文解决了这一研究问题，并介绍了nf2vec，这是一个能够在单个推理过程中为输入NF生成紧凑的潜在表示的框架。我们证明了nf2vec有效地嵌入了由输入NF表示的3D对象，并展示了如何在深度学习管道中使用由此产生的嵌入来成功地处理各种任务，同时只处理NF。我们在几个用于表示3D曲面的NFs上测试了这个框架，例如无符号/有符号距离和占用字段。此外，我们用更复杂的NFs证明了我们的方法的有效性，这些NFs包括3D对象的几何形状和外观，如神经辐射场。 et.al.|[2312.13277](http://arxiv.org/abs/2312.13277)|null|
|**2023-12-16**|**How to Train Neural Field Representations: A Comprehensive Study and Benchmark**|神经场（NeFs）最近已成为一种用于对各种模态（包括图像、形状和场景）的信号进行建模的通用方法。随后，许多工作探索了使用NeF作为下游任务的表示，例如，根据适合的NeF的参数对图像进行分类。然而，NeF超参数对其作为下游表示的质量的影响很少被理解，而且在很大程度上仍未被探索。这在一定程度上是由于拟合神经场数据集所需的大量时间造成的。在这项工作中，我们提出了 $\verb|fit-a-nef|$ ，这是一个基于JAX的库，它利用并行化来实现大规模nef数据集的快速优化，从而显著加快速度。有了这个库，我们进行了一项全面的研究，研究了不同超参数——包括初始化、网络架构和优化策略——对下游任务的NeF拟合的影响。我们的研究为如何训练NeF提供了宝贵的见解，并为优化其在下游应用中的有效性提供了指导。最后，基于所提出的库和我们的分析，我们提出了Neural Field Arena，这是一个由流行视觉数据集的神经场变体组成的基准，包括MNIST、CIFAR、ImageNet和ShapeNetv2的变体。我们的图书馆和神经领域竞技场将是开源的，以引入标准化的基准测试，并促进对神经领域的进一步研究。 et.al.|[2312.10531](http://arxiv.org/abs/2312.10531)|**[link](https://github.com/samuelepapa/fit-a-nef)**|
|**2023-12-18**|**LatentEditor: Text Driven Local Editing of 3D Scenes**|虽然神经领域在视图合成和场景重建方面取得了重大进展，但由于其对来自多视图输入的几何和纹理信息的隐式编码，编辑它们带来了巨大的挑战。在本文中，我们介绍了\textsc｛LatentEditor｝，这是一个创新的框架，旨在让用户能够使用文本提示对神经字段进行精确和本地控制的编辑。利用去噪扩散模型，我们成功地将真实世界的场景嵌入到潜在空间中，与传统方法相比，产生了更快、更具适应性的NeRF主干进行编辑。为了提高编辑精度，我们引入了一个delta分数来计算潜在空间中的2D掩模，该分数可以作为局部修改的指南，同时保留不相关的区域。我们新颖的像素级评分方法利用InstructPix2Pix（IP2P）的能力来辨别潜在空间中IP2P条件和无条件噪声预测之间的差异。然后在训练集中迭代地更新以2D掩码为条件的编辑的潜伏时间，以实现3D局部编辑。与现有的3D编辑模型相比，我们的方法实现了更快的编辑速度和卓越的输出质量，弥合了文本指令和潜在空间中高质量3D场景编辑之间的差距。我们在LLFF、IN2N、NeRFStudio和NeRFArt四个基准3D数据集上展示了我们的方法的优势。 et.al.|[2312.09313](http://arxiv.org/abs/2312.09313)|**[link](https://github.com/umarkhalidAI/LatentEditor)**|
|**2023-12-14**|**ZeroRF: Fast Sparse View 360° Reconstruction with Zero Pretraining**|我们提出了ZeroRF，这是一种新的每场景优化方法，解决了神经场表示中稀疏视图360重建的挑战。目前的突破，如神经辐射场（NeRF）已经证明了高保真度的图像合成，但难以处理稀疏的输入视图。现有的方法，如可泛化的NeRF和每场景优化方法，在数据依赖性、计算成本和跨不同场景的泛化方面面临限制。为了克服这些挑战，我们提出了ZeroRF，其关键思想是将定制的深度图像先验集成到因子分解的NeRF表示中。与传统方法不同，ZeroRF使用神经网络生成器对特征网格进行参数化，从而实现高效的稀疏视图360重建，而无需任何预训练或额外的正则化。大量实验展示了ZeroRF在质量和速度方面的多功能性和优势，在基准数据集上取得了最先进的结果。ZeroRF的意义延伸到3D内容生成和编辑的应用。项目页面：https://sarahweiii.github.io/zerorf/ et.al.|[2312.09249](http://arxiv.org/abs/2312.09249)|null|
|**2023-12-12**|**SMERF: Streamable Memory Efficient Radiance Fields for Real-Time Large-Scene Exploration**|最近的实时视图合成技术在保真度和速度上迅速进步，现代方法能够以交互式帧速率渲染接近照片级真实感的场景。与此同时，在易于光栅化的显式场景表示和基于射线行进的神经场之间出现了紧张关系，后者的最先进实例在质量上超过了前者，同时对于实时应用来说成本高得令人望而却步。在这项工作中，我们介绍了SMERF，这是一种视图合成方法，在占地面积高达3亿 $^2$、体积分辨率为3.5毫米$^3$ 的大型场景中，它实现了实时方法中最先进的精度。我们的方法建立在两个主要贡献之上：一个是分层模型划分方案，它在限制计算和内存消耗的同时增加了模型容量，另一个是蒸馏训练策略，它同时产生高保真度和内部一致性。我们的方法能够在网络浏览器中实现全六自由度（6DOF）导航，并在商品智能手机和笔记本电脑上实时渲染。大量实验表明，我们的方法在实时新视图合成方面，在标准基准上超过了当前最先进的0.78 dB，在大型场景上超过了1.78 dB，渲染帧的速度比最先进的辐射场模型快三个数量级，并在包括智能手机在内的各种商品设备上实现了实时性能。我们鼓励读者在我们的项目网站上亲自探索这些模型：https://smerf-3d.github.io. et.al.|[2312.07541](http://arxiv.org/abs/2312.07541)|null|
|**2023-12-11**|**Representing stimulus motion with waves in adaptive neural fields**|神经活动的行波在皮层网络中自发出现，并对刺激做出反应。波的时空结构可以指示它们编码的信息以及维持它们的生理过程。在这里，我们研究了作为视觉运动处理模型的自适应神经场中出现的行波的刺激响应关系。神经场方程将皮层组织的活动建模为连续的可兴奋介质，自适应过程提供负反馈，产生局部活动模式。在我们的模型中，突触连接由一个积分核来描述，该积分核由于依赖于活动的突触抑制而动态减弱，导致边缘稳定的行进前沿（具有衰减的后部）或固定速度的脉冲。我们的分析量化了弱刺激如何随着时间的推移改变这些波的相对位置，其特征是我们扰动地获得的波响应函数。持续和连续可见的刺激模拟移动的视觉对象。在视觉空间中跳跃的间歇性闪光可以产生流畅的视觉运动体验。我们的理论和数值模拟很好地描述了波对两种运动刺激的夹带，提供了视觉运动感知的机制描述。 et.al.|[2312.06100](http://arxiv.org/abs/2312.06100)|null|
|**2023-12-10**|**Accurate Differential Operators for Hybrid Neural Fields**|神经场已广泛应用于从形状表示到神经渲染以及求解偏微分方程（PDE）的各个领域。随着混合神经场表示的出现，如利用小MLP和显式表示的即时NGP，这些模型训练迅速，可以适应大型场景。然而，在渲染和模拟等许多应用中，混合神经场可能会导致明显且不合理的伪影。这是因为它们不能产生这些下游应用所需的精确的空间导数。在这项工作中，我们提出了两种规避这些挑战的方法。我们的第一种方法是一种事后算子，它使用局部多项式拟合从预先训练的混合神经场中获得更准确的导数。此外，我们还提出了一种自监督微调方法，该方法在保留初始信号的同时，对神经场进行细化，以直接产生准确的导数。我们展示了我们的方法在渲染、碰撞模拟和求解偏微分方程中的应用。我们观察到，使用我们的方法可以产生更准确的导数，减少伪影，并在下游应用中实现更准确的模拟。 et.al.|[2312.05984](http://arxiv.org/abs/2312.05984)|null|
|**2023-12-11**|**Nuvo: Neural UV Mapping for Unruly 3D Representations**|现有的UV映射算法被设计为在性能良好的网格上操作，而不是由最先进的3D重建和生成技术产生的几何表示。因此，将这些方法应用于由神经辐射场和相关技术（或从这些场三角化的网格）恢复的体积密度会导致纹理图谱过于分散，无法用于视图合成或外观编辑等任务。我们提出了一种UV映射方法，旨在对通过3D重建和生成技术产生的几何体进行操作。我们的方法Nuvo不是计算在网格顶点上定义的映射，而是使用神经场来表示连续的UV映射，并将其优化为仅针对一组可见点（即仅影响场景外观的点）的有效且性能良好的映射。我们展示了我们的模型对不良几何体带来的挑战是稳健的，并且它生成了可以表示详细外观的可编辑UV映射。 et.al.|[2312.05283](http://arxiv.org/abs/2312.05283)|null|

<p align=right>(<a href=#updated-on-20231223>back to top</a>)</p>

[contributors-shield]: https://img.shields.io/github/contributors/Vincentqyw/cv-arxiv-daily.svg?style=for-the-badge
[contributors-url]: https://github.com/Vincentqyw/cv-arxiv-daily/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/Vincentqyw/cv-arxiv-daily.svg?style=for-the-badge
[forks-url]: https://github.com/Vincentqyw/cv-arxiv-daily/network/members
[stars-shield]: https://img.shields.io/github/stars/Vincentqyw/cv-arxiv-daily.svg?style=for-the-badge
[stars-url]: https://github.com/Vincentqyw/cv-arxiv-daily/stargazers
[issues-shield]: https://img.shields.io/github/issues/Vincentqyw/cv-arxiv-daily.svg?style=for-the-badge
[issues-url]: https://github.com/Vincentqyw/cv-arxiv-daily/issues

