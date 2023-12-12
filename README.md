[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]

## Updated on 2023.12.12
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
|**2023-12-11**|**UpFusion: Novel View Diffusion from Unposed Sparse View Observations**|我们提出了UpFusion，这是一种在没有相应姿态信息的情况下，在给定稀疏参考图像集的情况下可以执行新颖的视图合成并推断对象的3D表示的系统。当前的稀疏视图3D推理方法通常依赖于相机姿态来几何地聚合来自输入视图的信息，但当这种信息不可用/不准确时，这种方法在野外并不稳健。相反，UpFusion通过学习在条件生成模型中隐含地利用可用图像作为上下文来合成新视图，从而避开了这一要求。我们将两种互补的条件反射形式结合到扩散模型中，以利用输入视图：a）通过使用场景级变换器推断与查询视图对齐的特征，b）通过可以直接观察输入图像标记的中间注意力层。我们表明，这种机制允许生成高保真度的新视图，同时在给定额外（未着色）图像的情况下提高合成质量。我们在Co3Dv2和Google Scanned Objects数据集上评估了我们的方法，并展示了与依赖姿势的稀疏视图方法以及无法利用其他视图的单视图方法相比，我们的方法的优势。最后，我们还表明，我们学习的模型可以超越训练类别进行推广，甚至可以从野外通用对象的自捕获图像中进行重建。 et.al.|[2312.06661](http://arxiv.org/abs/2312.06661)|null|
|**2023-12-11**|**Learning Naturally Aggregated Appearance for Efficient 3D Editing**|将3D场景表示为颜色场和密度场的神经辐射场在新视图合成方面取得了巨大进展，但由于其隐含性，不利于编辑。鉴于这种不足，我们建议用显式的2D外观聚合（也称为规范图像）来代替颜色场，用户可以通过2D图像处理轻松地自定义他们的3D编辑。为了避免失真效应并便于编辑，我们用投影场来补充规范图像，该投影场将3D点映射到2D像素上以进行纹理查找。该字段使用伪规范相机模型仔细初始化，并使用偏移规则性进行优化，以确保聚合外观的自然度。在三个数据集上的大量实验结果表明，我们称为AGAP的表示很好地支持各种3D编辑方式（例如，风格化、交互式绘图和内容提取），而无需对每种情况进行重新优化，证明了其可推广性和效率。项目页面位于https://felixcheng97.github.io/agap/. et.al.|[2312.06657](http://arxiv.org/abs/2312.06657)|**[link](https://github.com/felixcheng97/agap)**|
|**2023-12-11**|**CorresNeRF: Image Correspondence Priors for Neural Radiance Fields**|神经辐射场（NeRFs）在新的视图合成和表面重建任务中取得了令人印象深刻的结果。然而，在具有稀疏输入视图的具有挑战性的场景下，它们的性能会受到影响。我们提出了CorresNeRF，这是一种利用现有方法计算的图像对应先验来监督NeRF训练的新方法。我们设计了用于增强和滤波的自适应过程，以生成密集和高质量的对应关系。然后，通过对应像素重投影和深度损失项，使用对应来正则化NeRF训练。我们在不同的数据集上使用基于密度和基于SDF的NeRF模型评估了我们在新的视图合成和表面重建任务中的方法。我们的方法在光度和几何度量方面都优于以前的方法。我们表明，这种使用对应先验的简单而有效的技术可以作为即插即用模块应用于不同的NeRF变体。项目页面位于https://yxlao.github.io/corres-nerf. et.al.|[2312.06642](http://arxiv.org/abs/2312.06642)|**[link](https://github.com/yxlao/corres-nerf)**|
|**2023-12-11**|**NVFi: Neural Velocity Fields for 3D Physics Learning from Dynamic Videos**|在本文中，我们的目标是从多视图视频中对3D场景动力学进行建模。与大多数现有工作通常专注于训练时间段内的新视图合成这一常见任务不同，我们建议仅从视频帧中同时学习3D场景的几何、外观和物理速度，从而支持多种理想的应用，包括未来的帧外推、无监督的3D语义场景分解和动态运动转移。我们的方法由三个主要组成部分组成，1）关键帧动态辐射场，2）帧间速度场，以及3）联合关键帧和帧间优化模块，这是我们框架的核心，可以有效地训练两个网络。为了验证我们的方法，我们进一步引入了两个动态3D数据集：1）动态对象数据集和2）动态室内场景数据集。我们在多个数据集上进行了广泛的实验，证明了我们的方法在所有基线上的优越性能，特别是在未来的帧外推和无监督三维语义场景分解的关键任务中。 et.al.|[2312.06398](http://arxiv.org/abs/2312.06398)|null|
|**2023-12-11**|**Optimized View and Geometry Distillation from Multi-view Diffuser**|使用图像条件扩散模型从单个输入视图生成多视图图像是最近的进展，并且已经显示出相当大的潜力。然而，合成视图中缺乏一致性和提取的几何体中过度平滑等问题仍然存在。先前的方法集成了多视图一致性模块或施加额外的监督以增强视图一致性，同时损害了相机定位的灵活性并限制了视图合成的多功能性。在这项研究中，与之前的工作中使用的体积和光线聚集相比，我们认为在几何提取过程中优化的辐射场是一种更严格的一致性先验。我们通过多视图扩散器的分数提取，进一步识别并纠正了传统辐射场优化过程中的关键偏差。我们介绍了一种无偏分数蒸馏（USD），它利用来自2D扩散模型的无条件噪声，极大地提高了辐射场保真度。我们利用优化辐射场的渲染视图作为基础，开发了二维扩散模型的两步专业化过程，该模型擅长于进行特定对象的去噪和生成高质量的多视图图像。最后，我们直接从细化的多视图图像中恢复忠实的几何体和纹理。经验评估表明，我们的优化几何结构和视图提取技术产生的结果与在大量数据集上训练的最先进的模型相当，同时保持了相机定位的自由度。 et.al.|[2312.06198](http://arxiv.org/abs/2312.06198)|null|
|**2023-12-10**|**NeVRF: Neural Video-based Radiance Fields for Long-duration Sequences**|将神经辐射场（NeRF）应用于长时间动态序列一直是一项挑战。现有的方法难以在质量和存储大小之间取得平衡，并且在复杂的场景变化（如拓扑变化和大的运动）中遇到困难。为了解决这些问题，我们提出了一种新的基于神经视频的辐射场（NeVRF）表示。NeVRF将神经辐射场与基于图像的渲染相结合，支持在长时间动态内向场景中进行照片逼真的新视图合成。我们介绍了一种新的多视图辐射混合方法，可以直接从多视图视频中预测辐射。通过结合连续学习技术，NeVRF可以有效地从序列数据中重建帧，而无需重新访问先前的帧，从而实现长时间的免费视点视频。此外，通过量身定制的压缩方法，NeVRF可以紧凑地表示动态场景，使动态辐射场在现实世界场景中更加实用。我们的大量实验证明了NeVRF在实现长持续时间序列渲染、序列数据重建和紧凑数据存储方面的有效性。 et.al.|[2312.05855](http://arxiv.org/abs/2312.05855)|null|
|**2023-12-11**|**Nuvo: Neural UV Mapping for Unruly 3D Representations**|现有的UV映射算法被设计为在性能良好的网格上操作，而不是由最先进的3D重建和生成技术产生的几何表示。因此，将这些方法应用于由神经辐射场和相关技术（或从这些场三角化的网格）恢复的体积密度会导致纹理图谱过于分散，无法用于视图合成或外观编辑等任务。我们提出了一种UV映射方法，旨在对通过3D重建和生成技术产生的几何体进行操作。我们的方法Nuvo不是计算在网格顶点上定义的映射，而是使用神经场来表示连续的UV映射，并将其优化为仅针对一组可见点（即仅影响场景外观的点）的有效且性能良好的映射。我们展示了我们的模型对不良几何体带来的挑战是稳健的，并且它生成了可以表示详细外观的可编辑UV映射。 et.al.|[2312.05283](http://arxiv.org/abs/2312.05283)|null|
|**2023-12-08**|**MuVieCAST: Multi-View Consistent Artistic Style Transfer**|我们介绍了MuVieCAST，这是一种模块化多视图一致风格传输网络架构，可实现同一场景的多个视点之间的一致风格传输。这种网络架构同时支持稀疏视图和密集视图，使其具有足够的通用性，可以处理广泛的多视图图像数据集。该方法由三个模块组成，它们执行与风格传递相关的特定任务，即内容保存、图像转换和多视图一致性强制执行。我们在多个应用领域广泛评估了我们的方法，包括基于深度图的点云融合、网格重建和新颖的视图合成。我们的实验表明，所提出的框架实现了风格化图像的特殊生成，在不同视角下表现出一致的结果。一项专注于新视图合成的用户研究进一步证实了这些结果，与最近最先进的方法相比，大约68%的案例参与者表示更喜欢我们生成的输出。我们的模块化框架是可扩展的，可以很容易地与各种主干架构集成，使其成为多视图风格传输的灵活解决方案。更多结果在我们的项目页面上展示：muviecast.github.io et.al.|[2312.05046](http://arxiv.org/abs/2312.05046)|null|
|**2023-12-07**|**MuRF: Multi-Baseline Radiance Fields**|我们提出了多基线辐射场（MuRF），这是一种通用的前馈方法，用于解决多个不同基线设置（小基线和大基线，以及不同数量的输入视图）下的稀疏视图合成问题。为了渲染目标新视图，我们将3D空间离散为平行于目标图像平面的平面，并相应地构建目标视图截头体。这样的目标体积表示与目标视图在空间上对齐，这有效地聚集了来自输入视图的相关信息以进行高质量渲染。由于其轴对齐性质，它还便于随后使用卷积网络进行辐射场回归。卷积网络建模的3D上下文使我们的方法能够合成比先前工作更清晰的场景结构。我们的MuRF在从简单物体（DTU）到复杂室内外场景（RealEstate10K和LLFF）的多种不同基线设置和不同场景中实现了最先进的性能。我们还在Mip-NeRF 360数据集上展示了有前景的零样本泛化能力，证明了MuRF的普遍适用性。 et.al.|[2312.04565](http://arxiv.org/abs/2312.04565)|**[link](https://github.com/autonomousvision/murf)**|
|**2023-12-07**|**Free3D: Consistent Novel View Synthesis without 3D Representation**|我们介绍了Free3D，这是一种用于从单个图像进行开集新视图合成（NVS）的简单方法。与Zero-1-to-3类似，我们从预先训练的2D图像生成器开始进行泛化，并对其进行NVS微调。与最近和同时进行的工作相比，我们在不使用显式3D表示的情况下获得了显著的改进，这是缓慢的、消耗内存的或训练额外的3D网络。我们通过新的每像素光线调节归一化（RCN）层对目标相机姿态进行更好的编码来实现这一点。后者通过告诉每个像素其特定的观看方向，在底层2D图像生成器中注入姿势信息。我们还通过轻量级的多视图注意力层和多视图噪声共享来提高多视图一致性。我们在Ob厌恶数据集上训练Free3D，并在包括OminiObject3D和GSO在内的几个新数据集中展示了对各种新类别的出色概括。我们希望我们简单有效的方法将成为一个坚实的基线，并有助于未来以更准确的姿态进行NVS研究。项目页面位于https://chuanxiaz.com/free3d/. et.al.|[2312.04551](http://arxiv.org/abs/2312.04551)|**[link](https://github.com/lyndonzheng/Free3D)**|

<p align=right>(<a href=#updated-on-20231212>back to top</a>)</p>

## 3D Reconstruction

|Publish Date|Title|Abstract|PDF|Code|
|---|---|---|---|---|
|**2023-12-10**|**SuperPrimitive: Scene Reconstruction at a Primitive Level**|由于其计算复杂性和固有的视觉模糊性，从一组图像或单目视频中进行联合相机姿态和密集几何估计仍然是一个具有挑战性的问题。大多数密集增量重建系统直接对图像像素进行操作，并使用多视图几何提示来求解其3D位置。这种像素级方法存在模糊性或违反多视图一致性的问题（例如，由无纹理或镜面引起）。我们用一种新的图像表示来解决这个问题，我们称之为超原始。超基元是通过将图像分割成语义相关的局部区域并用估计的表面法线方向对其进行增强来获得的，这两者都是由最先进的单图像神经网络预测的。这提供了每个SuperPrimitive的局部几何体估计，而它们的相对位置是基于多视图观测进行调整的。我们通过解决三个3D重建任务来展示我们新表示的多功能性：深度完成、运动中的少量视图结构和单目密集视觉里程计。 et.al.|[2312.05889](http://arxiv.org/abs/2312.05889)|null|
|**2023-12-09**|**Light detection and Cosmic Rejection in the ICARUS LArTPC at Fermilab**|ICARUS-T600探测器是一个760吨的液氩时间投影室（LArPC），目前在费米实验室作为短基线中微子（SBN）计划中的远探测器运行。SBN计划由三个LArPC组成，其中心目标是测试无菌中微子假说。在Gran Sasso地下实验室工作了3年后，ICARUS探测器被运往欧洲核子研究中心，在那里它配备了360个8“光电倍增管用于新的光学检测系统。PMT系统检测来自液氩中相互作用的带电粒子的快速闪烁光，为全探测器生成触发信号，并允许对事件进行3D重建。现在探测器在浅层运行，暴露在高通量的宇宙射线中，这些宇宙射线可以伪造中微子的相互作用。为了减轻这种影响，安装了宇宙射线标记仪（CRT）和3米厚的混凝土。来自PMT和CRT子系统的精确定时信息可以帮助识别相互作用是来自ICARUS低温恒温器内部还是外部。本文综述了ICARUS中CRT和PMT光探测系统的宇宙成因背景减少和定时校准方法。 et.al.|[2312.05684](http://arxiv.org/abs/2312.05684)|null|
|**2023-12-08**|**Multi-view Inversion for 3D-aware Generative Adversarial Networks**|当前用于人类头部的3D GAN反演方法通常仅使用一个单个正面图像来重建整个3D头部模型。当多视图数据或动态视频可用时，这会遗漏有意义的信息。我们的方法建立在现有最先进的3D GAN反演技术的基础上，以实现同一主题的多个视图的一致和同时反演。我们使用多潜在扩展来处理动态人脸视频中存在的不一致性，以从序列中重新合成一致的3D表示。由于我们的方法使用了有关目标对象的额外信息，我们观察到几何精度和图像质量都有显著提高，尤其是在从宽视角进行渲染时。此外，我们展示了我们的反向3D渲染的可编辑性，这将它们与基于NeRF的场景重建区分开来。 et.al.|[2312.05330](http://arxiv.org/abs/2312.05330)|null|
|**2023-12-11**|**Nuvo: Neural UV Mapping for Unruly 3D Representations**|现有的UV映射算法被设计为在性能良好的网格上操作，而不是由最先进的3D重建和生成技术产生的几何表示。因此，将这些方法应用于由神经辐射场和相关技术（或从这些场三角化的网格）恢复的体积密度会导致纹理图谱过于分散，无法用于视图合成或外观编辑等任务。我们提出了一种UV映射方法，旨在对通过3D重建和生成技术产生的几何体进行操作。我们的方法Nuvo不是计算在网格顶点上定义的映射，而是使用神经场来表示连续的UV映射，并将其优化为仅针对一组可见点（即仅影响场景外观的点）的有效且性能良好的映射。我们展示了我们的模型对不良几何体带来的挑战是稳健的，并且它生成了可以表示详细外观的可编辑UV映射。 et.al.|[2312.05283](http://arxiv.org/abs/2312.05283)|null|
|**2023-12-08**|**Fine Dense Alignment of Image Bursts through Camera Pose and Depth Estimation**|本文介绍了一种新的方法来对手持相机拍摄的突发图像进行精细对准。与估计帧对之间的二维变换或依赖于离散对应关系的传统技术相比，所提出的算法通过优化每个像素的相机运动和表面深度和方向来建立密集的对应关系。这种方法改进了对齐，特别是在具有视差挑战的场景中。以小基线甚至微小基线为特征的合成爆发的广泛实验表明，在这种情况下，它的性能优于目前可用的最佳光流方法，而不需要任何训练。除了增强对齐之外，我们的方法还为简单图像恢复之外的任务开辟了途径，如深度估计和3D重建，这得到了有希望的初步结果的支持。这将我们的方法定位为用于各种突发图像处理应用的通用工具。 et.al.|[2312.05190](http://arxiv.org/abs/2312.05190)|null|
|**2023-12-08**|**SuperNormal: Neural Surface Reconstruction via Multi-View Normal Integration**|我们介绍了SuperNormal，这是一种使用曲面法线贴图进行多视图三维重建的快速高保真方法。只需几分钟，SuperNormal就可以生成与3D扫描仪不相上下的详细曲面。我们利用体绘制来优化由多分辨率哈希编码提供支持的神经符号距离函数（SDF）。为了加速训练，我们提出了方向有限差分和基于补丁的射线行进来数值逼近SDF梯度。在不影响重建质量的同时，该策略的效率几乎是分析梯度的两倍，比轴对齐有限差分快约三倍。在基准数据集上的实验表明，与现有的多视图光度立体方法相比，SuperNormal在效率和准确性方面具有优势。在我们捕获的对象上，SuperNormal比最近的神经3D重建方法产生了更细粒度的几何体。 et.al.|[2312.04803](http://arxiv.org/abs/2312.04803)|null|
|**2023-12-07**|**FitDiff: Robust monocular 3D facial shape and reflectance estimation using Diffusion Models**|三维人脸重建的显著进展已经产生了高细节和逼真的人脸表示。最近，扩散模型实现了比GANs更好的性能，从而彻底改变了生成方法的能力。在这项工作中，我们提出了FitDiff，一个基于扩散的三维人脸化身生成模型。该模型利用从“野外”2D面部图像中提取的身份嵌入，准确地生成可重新点亮的面部化身。我们的多模式漫射模型同时输出面部反射率图（漫射和镜面反照率和法线）和形状，显示出强大的泛化能力。它只在公共面部数据集的注释子集上进行训练，并与3D重建相结合。我们通过使用感知和人脸识别损失来引导反向扩散过程，重新审视典型的3D人脸拟合方法。FitDiff是第一个以人脸识别嵌入为条件的LDM，它重建了可重新照明的人类化身，可以像在普通渲染引擎中一样使用，只从不受约束的面部图像开始，并实现了最先进的性能。 et.al.|[2312.04465](http://arxiv.org/abs/2312.04465)|null|
|**2023-12-07**|**Cascade-Zero123: One Image to Highly Consistent 3D with Self-Prompted Nearby Views**|从单个图像合成多视图3D是一项重要而富有挑战性的任务。为此，Zero-1-to-3方法旨在将2D潜在扩散模型扩展到3D范围。这些方法生成具有单个视点图像和相机姿态作为条件信息的目标视点图像。然而，Zero-1-to-3中采用的一对一方式给在视图之间建立几何和视觉一致性带来了挑战，尤其是对于复杂对象。为了解决这个问题，我们提出了一个由两个Zero-1-to-3模型构建的级联生成框架，称为cascade-Zero123，该框架从源图像中逐步提取3D信息。具体而言，设计了一种自提示机制，用于首先生成几个附近的视图。然后将这些视图与源图像一起作为生成条件馈送到第二阶段模型中。以自我提示的多个视图作为补充信息，我们的Cascade-Zero123生成了比Zero-1-3更高度一致的新视图图像。该促销活动对各种复杂和具有挑战性的场景具有重要意义，包括昆虫、人类、透明物体和堆叠的多个物体等。项目页面位于https://cascadezero123.github.io/. et.al.|[2312.04424](http://arxiv.org/abs/2312.04424)|null|
|**2023-12-06**|**DreamComposer: Controllable 3D Object Generation via Multi-View Conditions**|利用预先训练的2D大规模生成模型，最近的工作能够从单个野生图像中生成高质量的新视图。然而，由于缺乏来自多个视角的信息，这些作品在生成可控的小说视角方面遇到了困难。在本文中，我们提出了DreamComposer，这是一个灵活且可扩展的框架，可以通过注入多视图条件来增强现有的视图感知扩散模型。具体而言，DreamComposer首先使用视图感知三维提升模块从多个视图中获得对象的三维表示。然后，利用多视图特征融合模块从三维表示中提取目标视图的潜在特征。最后，将从多视图输入中提取的目标视图特征注入到预先训练的扩散模型中。实验表明，DreamComposer与用于零样本新视图合成的最先进的扩散模型兼容，进一步增强了它们以生成具有多视图条件的高保真度新视图图像，为可控3D对象重建和各种其他应用做好了准备。 et.al.|[2312.03611](http://arxiv.org/abs/2312.03611)|null|
|**2023-12-06**|**Gaussian-Flow: 4D Reconstruction with Dynamic 3D Gaussian Particle**|我们介绍了高斯流，这是一种新的基于点的方法，用于快速动态场景重建和多视图和单目视频的实时渲染。与因训练和渲染速度缓慢而受到阻碍的流行的基于NeRF的方法相比，我们的方法利用了基于点的3D高斯散射（3DGS）的最新进展。具体而言，提出了一种新的双域变形模型（DDDM）来显式地对每个高斯点的属性变形进行建模，其中通过时域中的多项式拟合和频域中的傅立叶级数拟合来捕获每个属性的时间相关残差。所提出的DDDM能够对长视频镜头中的复杂场景变形进行建模，消除了为每帧训练单独的3DGS的需要，或者引入了额外的隐式神经场来对3D动力学进行建模。此外，离散高斯点的显式变形建模确保了4D场景的超快速训练和渲染，这与为静态3D重建设计的原始3DGS相当。我们提出的方法展示了显著的效率提高，与每帧3DGS建模相比，训练速度快了5倍。此外，定量结果表明，所提出的高斯流在新视图渲染质量方面显著优于以前的主流方法。项目页面：https://nju-3dv.github.io/projects/gaussian-flow et.al.|[2312.03431](http://arxiv.org/abs/2312.03431)|null|

<p align=right>(<a href=#updated-on-20231212>back to top</a>)</p>

## Diffusion

|Publish Date|Title|Abstract|PDF|Code|
|---|---|---|---|---|
|**2023-12-11**|**CAD: Photorealistic 3D Generation via Adversarial Distillation**|AR/VR、机器人和游戏应用中对3D数据的需求不断增加，催生了能够合成高质量3D对象的强大生成管道。这些模型中的大多数依赖于分数蒸馏采样（SDS）算法来优化3D表示，使得渲染图像保持由预训练的扩散模型评估的高似然性。然而，在由扩散模型产生的高维分布中找到正确的模式是具有挑战性的，并且经常导致诸如过饱和、过平滑和类Janus伪像之类的问题。在本文中，我们提出了一种新的3D合成学习范式，该范式利用了预先训练的扩散模型。我们的方法不是专注于模式搜索，而是以对抗性的方式直接对多视图渲染和扩散先验之间的分布差异进行建模，这解锁了高保真度和照片级真实感3D内容的生成，条件是单个图像和提示。此外，通过利用GANs的潜在空间和表达的扩散模型先验，我们的方法促进了广泛的3D应用，包括单视图重建、高多样性生成和开放域中的连续3D插值。实验表明，与以前的工作相比，我们的管道在发电质量和多样性方面具有优势。 et.al.|[2312.06663](http://arxiv.org/abs/2312.06663)|null|
|**2023-12-11**|**Photorealistic Video Generation with Diffusion Models**|我们提出了W.A.L.T，这是一种通过扩散建模生成真实感视频的基于变换器的方法。我们的方法有两个关键的设计决策。首先，我们使用因果编码器在统一的潜在空间内联合压缩图像和视频，实现跨模态的训练和生成。其次，为了提高记忆和训练效率，我们使用了一种专门为联合空间和时空生成建模量身定制的窗口注意力架构。总之，这些设计决策使我们能够在不使用无分类器指导的情况下，在已建立的视频（UCF-101和Kinetics-600）和图像（ImageNet）生成基准上实现最先进的性能。最后，我们还为文本到视频生成任务训练了三个模型的级联，其中包括一个基本潜在视频扩散模型和两个视频超分辨率扩散模型，以每秒 $8$帧的速度生成分辨率为$512\乘以896$ 的视频。 et.al.|[2312.06662](http://arxiv.org/abs/2312.06662)|null|
|**2023-12-11**|**UpFusion: Novel View Diffusion from Unposed Sparse View Observations**|我们提出了UpFusion，这是一种在没有相应姿态信息的情况下，在给定稀疏参考图像集的情况下可以执行新颖的视图合成并推断对象的3D表示的系统。当前的稀疏视图3D推理方法通常依赖于相机姿态来几何地聚合来自输入视图的信息，但当这种信息不可用/不准确时，这种方法在野外并不稳健。相反，UpFusion通过学习在条件生成模型中隐含地利用可用图像作为上下文来合成新视图，从而避开了这一要求。我们将两种互补的条件反射形式结合到扩散模型中，以利用输入视图：a）通过使用场景级变换器推断与查询视图对齐的特征，b）通过可以直接观察输入图像标记的中间注意力层。我们表明，这种机制允许生成高保真度的新视图，同时在给定额外（未着色）图像的情况下提高合成质量。我们在Co3Dv2和Google Scanned Objects数据集上评估了我们的方法，并展示了与依赖姿势的稀疏视图方法以及无法利用其他视图的单视图方法相比，我们的方法的优势。最后，我们还表明，我们学习的模型可以超越训练类别进行推广，甚至可以从野外通用对象的自捕获图像中进行重建。 et.al.|[2312.06661](http://arxiv.org/abs/2312.06661)|null|
|**2023-12-11**|**Sherpa3D: Boosting High-Fidelity Text-to-3D Generation via Coarse 3D Prior**|最近，通过利用2D和3D扩散模型，从文本提示创建3D内容已经显示出显著的进展。虽然3D扩散模型确保了良好的多视图一致性，但其生成高质量和多样化3D资产的能力受到有限3D数据的阻碍。相比之下，2D扩散模型找到了一种蒸馏方法，该方法在没有任何3D数据的情况下实现了出色的泛化和丰富的细节。然而，2D提升方法存在固有的视图不可知的模糊性，从而导致严重的多面Janus问题，其中文本提示无法提供足够的指导来学习连贯的3D结果。我们研究了如何充分利用易于访问的粗略3D知识来增强提示并指导2D提升优化进行细化，而不是重新训练成本高昂的视点感知模型。在本文中，我们提出了Sherpa3D，这是一种新的文本到3D框架，它同时实现了高保真度、可推广性和几何一致性。具体而言，我们设计了一对从3D扩散模型生成的粗略3D先验导出的引导策略：用于几何保真度的结构引导和用于3D连贯性的语义引导。采用这两种类型的引导，2D扩散模型以多样化和高质量的结果丰富了3D内容。大量实验表明，我们的Sherpa3D在质量和3D一致性方面优于最先进的文本到3D方法。 et.al.|[2312.06655](http://arxiv.org/abs/2312.06655)|**[link](https://github.com/liuff19/Sherpa3D)**|
|**2023-12-11**|**Upscale-A-Video: Temporal-Consistent Diffusion Model for Real-World Video Super-Resolution**|基于文本的扩散模型在生成和编辑方面取得了显著的成功，显示出利用其生成先验增强视觉内容的巨大前景。然而，由于对输出保真度和时间一致性的高要求，将这些模型应用于视频超分辨率仍然具有挑战性，而扩散模型中固有的随机性使其变得复杂。我们的研究介绍了Upscale-A-Video，一种用于视频放大的文本引导潜在扩散框架。该框架通过两个关键机制确保时间一致性：在本地，它将时间层集成到U-Net和VAE解码器中，保持短序列内的一致性；在全局范围内，在没有训练的情况下，引入了一个流引导的递归潜在传播模块，通过在整个序列中传播和融合潜在信息来增强整体视频稳定性。得益于扩散范式，我们的模型还提供了更大的灵活性，允许文本提示来指导纹理创建，并允许可调节的噪声水平来平衡恢复和生成，从而实现保真度和质量之间的权衡。大量实验表明，Upscale-A-Video在合成和真实世界的基准测试以及人工智能生成的视频中都超越了现有方法，展现了令人印象深刻的视觉真实感和时间一致性。 et.al.|[2312.06640](http://arxiv.org/abs/2312.06640)|null|
|**2023-12-11**|**DiAD: A Diffusion-based Framework for Multi-class Anomaly Detection**|基于重建的方法在异常检测方面取得了显著的成果。最近流行的扩散模型的特殊图像重建能力引发了利用它们来增强异常图像重建的研究努力。尽管如此，在更实用的多类别设置中，这些方法可能面临与图像类别和像素结构完整性的保存相关的挑战。为了解决上述问题，我们提出了一种用于多类异常检测的基于Difusion的异常检测（DiAD）框架，该框架由像素空间自动编码器、连接到稳定扩散去噪网络的潜在空间语义引导（SG）网络和特征空间预训练的特征提取器组成。首先，提出了SG网络，用于在保留原始图像语义信息的同时重建异常区域。其次，我们引入了空间感知特征融合（SFF）块，以在处理大规模重建区域时最大限度地提高重建精度。第三，输入图像和重建图像由预训练的特征提取器处理，以基于在不同尺度上提取的特征生成异常图。在MVTec AD和VisA数据集上的实验证明了我们的方法的有效性，它超越了最先进的方法，例如，在多类MVTec AD数据集上分别实现了96.8/52.6和97.2/99.0（AUROC/AP）的定位和检测。代码将在https://lewandofskee.github.io/projects/diad. et.al.|[2312.06607](http://arxiv.org/abs/2312.06607)|**[link](https://github.com/lewandofskee/DiAD)**|
|**2023-12-11**|**ControlNet-XS: Designing an Efficient and Effective Architecture for Controlling Text-to-Image Diffusion Models**|在过去的几年里，图像合成领域取得了巨大的进步。除了用文本提示定义期望的输出图像之外，直观的方法是另外使用图像形式的空间引导，例如深度图。为此，最近非常流行的方法是将控制网络（如ControlNet）与预训练的图像生成模型（如稳定扩散）相结合。在评估现有控制网络的设计时，我们观察到它们都面临着相同的问题，即生成和控制过程之间的信息流动延迟。这反过来意味着控制网络必须具有生成能力。在这项工作中，我们提出了一种新的控制体系结构，称为ControlNet XS，它不存在这个问题，因此可以专注于学习控制的给定任务。与ControlNet相比，我们的模型只需要一小部分参数，因此在推理和训练时间内的速度大约是ControlNet的两倍。此外，生成的图像具有更高的质量，并且控制具有更高保真度。所有代码和预先训练的模型都将公开。 et.al.|[2312.06573](http://arxiv.org/abs/2312.06573)|**[link](https://github.com/vislearn/ControlNet-XS)**|
|**2023-12-11**|**HOI-Diff: Text-Driven Synthesis of 3D Human-Object Interactions using Diffusion Models**|我们解决了由文本提示驱动的生成逼真的3D人机交互（HOI）的问题。我们的关键见解是采用模块化设计，将复杂的任务分解为更简单的子任务，而不是单一的模型。我们首先开发了一个双分支扩散模型（HOI-DM），以在输入文本的条件下生成人和物体的运动，并通过人和物体运动生成分支之间的交叉注意力通信模块来鼓励连贯的运动。我们还开发了一个可供性预测扩散模型（APDM）来预测在文本提示驱动的交互过程中人和物体之间的接触面积。APDM独立于HOI-DM的结果，因此可以校正后者的潜在误差。此外，它随机地生成接触点，以使生成的运动多样化。最后，我们将估计的接触点纳入分类器引导中，以实现人与物体之间的准确和密切接触。为了训练和评估我们的方法，我们用文本描述对BEHAVE数据集进行了注释。实验结果表明，我们的方法能够产生具有各种交互和不同类型对象的逼真HOI。 et.al.|[2312.06553](http://arxiv.org/abs/2312.06553)|null|
|**2023-12-11**|**In-situ Synchrotron X-Ray Photoelectron Spectroscopy Study of Medium-Temperature Baking of Niobium for SRF Application**|在本工作中，通过同步辐射X射线光电子能谱（XPS）原位探索了在200-400｛\deg｝C的烘烤下铌表面的化学成分，类似于空腔的“中温烘烤”和“炉烘烤”。我们的发现表明，在 $Nb_2O_5$层的临界厚度以下（约1nm），铌开始与表面杂质（如碳和磷）积极相互作用。通过研究天然氧化物还原的动力学，确定了活化能和速率常数的关系，并用于计算氧浓度深度分布。已经确定，当天然氧化物层代表氧源时，氧的受控扩散是在200-300｛\deg｝C的温度下实现的，而在400｛\ddeg｝C时，五氧化二物被完全还原，掺杂水平由环境氧分压决定。发现缓冲化学抛光后的氟（F与Nb的原子比约为0.2）被掺入XPS探测的表面层（约4.6nm）中，并且其浓度在低温烘焙期间增加（F/Nb在230｛deg｝C下高达0.35）并且在更高的温度下耗尽（F/Nb＝0.11在400｛deg｝C）。因此，必须考虑氟对中T烘烤、温和烘烤（120｛\deg｝C/48 h）和氮掺杂空腔性能的影响。还讨论了氟在室温下和热处理过程中在X射线束的影响下导出的$Nb^｛+5｝$到$Nb^{+4｝$ 反应中的可能作用。铌表面不会被杂质污染的热处理的温度和持续时间参数的范围是为工业应用而确定的。 et.al.|[2312.06529](http://arxiv.org/abs/2312.06529)|null|
|**2023-12-11**|**On One Dimensional Advection -- Diffusion Equation with Variable Diffusivity**|本文讨论了一个具有狄利克雷齐次边界条件的含时一维线性平流扩散方程。该方程采用变量分离法进行解析求解，并采用有限差分法进行数值求解。计算输出包括解决方案的三维（3D）图，重点关注氨、一氧化碳、二氧化碳和二氧化硫等污染物。浓度及其各自的扩散率通过3D图和实际计算进行分析。为了理解预测污染物在空气中运动的扩散率-浓度关系，该领域分为两半。该研究使用2D和3D图探索了扩散率较高的污染物进入扩散率较低区域的行为，反之亦然。这项任务对于有效的污染控制战略、保护环境和公众健康至关重要。 et.al.|[2312.06493](http://arxiv.org/abs/2312.06493)|null|

<p align=right>(<a href=#updated-on-20231212>back to top</a>)</p>

## NeRF

|Publish Date|Title|Abstract|PDF|Code|
|---|---|---|---|---|
|**2023-12-11**|**Representing stimulus motion with waves in adaptive neural fields**|神经活动的行波在皮层网络中自发出现，并对刺激做出反应。波的时空结构可以指示它们编码的信息以及维持它们的生理过程。在这里，我们研究了作为视觉运动处理模型的自适应神经场中出现的行波的刺激响应关系。神经场方程将皮层组织的活动建模为连续的可兴奋介质，自适应过程提供负反馈，产生局部活动模式。在我们的模型中，突触连接由一个积分核来描述，该积分核由于依赖于活动的突触抑制而动态减弱，导致边缘稳定的行进前沿（具有衰减的后部）或固定速度的脉冲。我们的分析量化了弱刺激如何随着时间的推移改变这些波的相对位置，其特征是我们扰动地获得的波响应函数。持续和连续可见的刺激模拟移动的视觉对象。在视觉空间中跳跃的间歇性闪光可以产生流畅的视觉运动体验。我们的理论和数值模拟很好地描述了波对两种运动刺激的夹带，提供了视觉运动感知的机制描述。 et.al.|[2312.06100](http://arxiv.org/abs/2312.06100)|null|
|**2023-12-10**|**Accurate Differential Operators for Hybrid Neural Fields**|神经场已广泛应用于从形状表示到神经渲染以及求解偏微分方程（PDE）的各个领域。随着混合神经场表示的出现，如利用小MLP和显式表示的即时NGP，这些模型训练迅速，可以适应大型场景。然而，在渲染和模拟等许多应用中，混合神经场可能会导致明显且不合理的伪影。这是因为它们不能产生这些下游应用所需的精确的空间导数。在这项工作中，我们提出了两种规避这些挑战的方法。我们的第一种方法是一种事后算子，它使用局部多项式拟合从预先训练的混合神经场中获得更准确的导数。此外，我们还提出了一种自监督微调方法，该方法在保留初始信号的同时，对神经场进行细化，以直接产生准确的导数。我们展示了我们的方法在渲染、碰撞模拟和求解偏微分方程中的应用。我们观察到，使用我们的方法可以产生更准确的导数，减少伪影，并在下游应用中实现更准确的模拟。 et.al.|[2312.05984](http://arxiv.org/abs/2312.05984)|null|
|**2023-12-11**|**Nuvo: Neural UV Mapping for Unruly 3D Representations**|现有的UV映射算法被设计为在性能良好的网格上操作，而不是由最先进的3D重建和生成技术产生的几何表示。因此，将这些方法应用于由神经辐射场和相关技术（或从这些场三角化的网格）恢复的体积密度会导致纹理图谱过于分散，无法用于视图合成或外观编辑等任务。我们提出了一种UV映射方法，旨在对通过3D重建和生成技术产生的几何体进行操作。我们的方法Nuvo不是计算在网格顶点上定义的映射，而是使用神经场来表示连续的UV映射，并将其优化为仅针对一组可见点（即仅影响场景外观的点）的有效且性能良好的映射。我们展示了我们的模型对不良几何体带来的挑战是稳健的，并且它生成了可以表示详细外观的可编辑UV映射。 et.al.|[2312.05283](http://arxiv.org/abs/2312.05283)|null|
|**2023-12-08**|**Dynamic LiDAR Re-simulation using Compositional Neural Fields**|我们介绍了DyNFL，这是一种新的基于神经场的方法，用于动态驾驶场景中激光雷达扫描的高保真度重新模拟。DyNFL处理来自动态环境的激光雷达测量，并伴随着移动物体的边界框，以构建可编辑的神经场。该字段包括单独重建的静态背景和动态对象，允许用户在重新模拟的场景中修改视点、调整对象位置以及无缝添加或删除对象。我们方法的一个关键创新是神经场合成技术，该技术通过光线下降测试有效地集成了来自各种场景的重建神经资产，考虑到了遮挡和透明表面。我们对合成和真实世界环境的评估表明，\ShortName大大改进了基于激光雷达扫描的动态场景模拟，提供了物理保真度和灵活编辑功能的组合。 et.al.|[2312.05247](http://arxiv.org/abs/2312.05247)|null|
|**2023-12-08**|**TriHuman : A Real-time and Controllable Tri-plane Representation for Detailed Human Geometry and Appearance Synthesis**|仅从视频数据中创建可控、逼真和几何细节的真人数字替身是计算机图形学和视觉领域的一个关键挑战，尤其是在需要实时性能的情况下。最近的方法将神经辐射场（NeRF）连接到关节结构，例如身体模型或骨骼，以将点映射到姿势规范空间中，同时将NeRF调节在骨骼姿势上。这些方法通常使用多层感知器（MLP）对神经场进行参数化，导致运行时间缓慢。为了解决这一缺点，我们提出了一种新的人体定制、可变形和高效的三平面表示TriHuman，它实现了实时性能、最先进的姿态可控几何合成以及逼真的渲染质量。在核心，我们将全局光线样本非刚性地扭曲到未变形的三平面纹理空间中，这有效地解决了全局点映射到相同三平面位置的问题。然后，我们展示了如何将这种三平面特征表示以骨骼运动为条件，以考虑动态外观和几何结构的变化。我们的研究结果表明，在人类的几何形状和外观建模以及运行时性能方面，朝着更高质量迈出了明确的一步。 et.al.|[2312.05161](http://arxiv.org/abs/2312.05161)|null|
|**2023-12-08**|**GIR: 3D Gaussian Inverse Rendering for Relightable Scene Factorization**|本文提出了一种用于可重照明场景分解的三维高斯逆绘制方法GIR。与利用离散网格或神经隐式场进行反向渲染的现有方法相比，我们的方法利用3D高斯从多视图图像中估计对象的材料特性、照明和几何结构。我们的研究动机是有证据表明，在性能、多功能性和效率方面，3D高斯是比神经领域更有前途的主干。在本文中，我们旨在回答以下问题：“如何应用3D高斯来提高反向渲染的性能？”为了解决基于离散且通常在均匀分布的3D高斯表示中估计法线的复杂性，我们提出了一种高效的自正则化方法，该方法有助于在不需要额外监督的情况下对曲面法线进行建模。为了重建间接照明，我们提出了一种模拟光线跟踪的方法。大量实验证明，在反向渲染中，我们提出的GIR在各种广泛使用的数据集上跨多个任务的性能优于现有方法。这证实了它的功效和广泛的适用性，突出了它作为重新照明和重建中有影响力的工具的潜力。项目页面：https://3dgir.github.io et.al.|[2312.05133](http://arxiv.org/abs/2312.05133)|null|
|**2023-12-06**|**Gaussian-Flow: 4D Reconstruction with Dynamic 3D Gaussian Particle**|我们介绍了高斯流，这是一种新的基于点的方法，用于快速动态场景重建和多视图和单目视频的实时渲染。与因训练和渲染速度缓慢而受到阻碍的流行的基于NeRF的方法相比，我们的方法利用了基于点的3D高斯散射（3DGS）的最新进展。具体而言，提出了一种新的双域变形模型（DDDM）来显式地对每个高斯点的属性变形进行建模，其中通过时域中的多项式拟合和频域中的傅立叶级数拟合来捕获每个属性的时间相关残差。所提出的DDDM能够对长视频镜头中的复杂场景变形进行建模，消除了为每帧训练单独的3DGS的需要，或者引入了额外的隐式神经场来对3D动力学进行建模。此外，离散高斯点的显式变形建模确保了4D场景的超快速训练和渲染，这与为静态3D重建设计的原始3DGS相当。我们提出的方法展示了显著的效率提高，与每帧3DGS建模相比，训练速度快了5倍。此外，定量结果表明，所提出的高斯流在新视图渲染质量方面显著优于以前的主流方法。项目页面：https://nju-3dv.github.io/projects/gaussian-flow et.al.|[2312.03431](http://arxiv.org/abs/2312.03431)|null|
|**2023-12-06**|**Artist-Friendly Relightable and Animatable Neural Heads**|创建照片逼真数字化身的一种越来越常见的方法是通过使用体积神经场。当在一组多视图图像上训练时，原始神经辐射场（NeRF）允许静态头部进行令人印象深刻的新颖视图合成，后续方法表明，这些神经表示可以扩展到动态化身。最近，新的变体也超过了神经表示中烘焙照明的常见缺点，表明静态神经化身可以在任何环境中重新发光。在这项工作中，我们同时解决了运动和照明问题，为可重新照明和可动画化的神经头提出了一种新方法。我们的方法建立在一种已验证的动态化身方法的基础上，该方法基于体积基元的混合，结合最近提出的用于可重新照明神经场的轻量级硬件设置，并包括一种新的架构，该架构允许重新照明动态神经化身在任何环境中执行看不见的表情，即使是在近场照明和视点的情况下。 et.al.|[2312.03420](http://arxiv.org/abs/2312.03420)|null|
|**2023-12-06**|**RING-NeRF: A Versatile Architecture based on Residual Implicit Neural Grids**|自引入以来，神经场在三维重建和新视图合成方面变得非常流行。最近的研究集中在加速这一过程，以及提高对观测距离和有限监督视点数量变化的鲁棒性。然而，这些方法往往导致无法轻易结合的专门解决方案。为了解决这个问题，我们引入了一种新的简单但高效的架构，称为RING-NeRF，基于残差隐式神经网格，它提供了对场景和潜在空间之间映射函数的细节级别的控制。与距离感知的前向映射机制和连续的从粗到细的重建过程相关联，我们的多功能架构在以下方面展示了快速训练和最先进的性能：（1）抗混叠渲染，（2）从很少监督的视点的重建质量，以及（3）对于基于SDF的NeRF在没有适当的场景特定初始化的情况下的鲁棒性。我们还证明了我们的架构可以动态添加网格来增加重建的细节，为自适应重建开辟了道路。 et.al.|[2312.03357](http://arxiv.org/abs/2312.03357)|null|
|**2023-12-06**|**Multifractality in critical neural field dynamics**|大脑临界性框架在很大程度上认为大脑动力学是单分形的，尽管实验证据表明大脑表现出显著的多重分形。为了理解多重分形是如何在类临界系统中出现的，我们使用了临界神经振荡的计算模型。我们发现多重分形在同步相变附近出现。这些发现表明，时间动力学的多重分形在神经场的临界点达到峰值，为解释大脑记录中的多重分形提供了一个生成模型。 et.al.|[2312.03219](http://arxiv.org/abs/2312.03219)|null|

<p align=right>(<a href=#updated-on-20231212>back to top</a>)</p>

[contributors-shield]: https://img.shields.io/github/contributors/Vincentqyw/cv-arxiv-daily.svg?style=for-the-badge
[contributors-url]: https://github.com/Vincentqyw/cv-arxiv-daily/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/Vincentqyw/cv-arxiv-daily.svg?style=for-the-badge
[forks-url]: https://github.com/Vincentqyw/cv-arxiv-daily/network/members
[stars-shield]: https://img.shields.io/github/stars/Vincentqyw/cv-arxiv-daily.svg?style=for-the-badge
[stars-url]: https://github.com/Vincentqyw/cv-arxiv-daily/stargazers
[issues-shield]: https://img.shields.io/github/issues/Vincentqyw/cv-arxiv-daily.svg?style=for-the-badge
[issues-url]: https://github.com/Vincentqyw/cv-arxiv-daily/issues

