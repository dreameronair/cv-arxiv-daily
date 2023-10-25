[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]

## Updated on 2023.10.25
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
|**2023-10-23**|**Relit-NeuLF: Efficient Relighting and Novel View Synthesis via Neural 4D Light Field**|在本文中，我们解决了在光源数量有限的情况下，从多视图图像中同时重新照明和合成复杂场景的新视图的问题。我们提出了一种称为Relit NeuLF的分析综合方法。继最近的神经4D光场网络（NeuLF）之后，Relit NeuLF首先利用两平面光场表示来参数化4D坐标系中的每条光线，从而实现高效的学习和推理。然后，我们以自监督的方式恢复三维场景的空间变化双向反射率分布函数（SVBRDF）。DecomposeNet学习将每条光线映射到其SVBRDF组件：反照率、法线和粗糙度。基于分解的BRDF分量和条件光方向，RenderNet学习合成光线的颜色。为了自我监督SVBRDF分解，我们鼓励使用微平面模型使预测的光线颜色接近基于物理的渲染结果。综合实验表明，该方法在合成数据和真实人脸数据上都是有效的，并且优于最先进的结果。我们在GitHub上公开发布了我们的代码。你可以在这里找到它：https://github.com/oppo-us-research/RelitNeuLF et.al.|[2310.14642](http://arxiv.org/abs/2310.14642)|**[link](https://github.com/oppo-us-research/relitneulf)**|
|**2023-10-23**|**VQ-NeRF: Vector Quantization Enhances Implicit Neural Representations**|隐式神经表示的最新进展有助于高保真度的表面重建和真实感的新视图合成。然而，这些方法中固有的计算复杂性是一个巨大的障碍，限制了实际应用中可达到的帧速率和分辨率。针对这一困境，我们提出了VQ-NeRF，这是一种通过矢量量化增强隐式神经表示的有效管道。我们的方法的本质包括将NeRF的采样空间减少到较低的分辨率，然后使用预训练的VAE解码器将其恢复到原始大小，从而有效地缓解渲染过程中遇到的采样时间瓶颈。尽管码本提供了代表性的特征，但由于高压缩率，重建场景的精细纹理细节仍然具有挑战性。为了克服这一限制，我们设计了一种创新的多尺度NeRF采样方案，该方案在压缩和原始尺度上同时优化NeRF模型，以增强网络保存精细细节的能力。此外，我们引入了语义损失函数，以提高三维重建的几何保真度和语义连贯性。大量实验证明了我们的模型在实现渲染质量和效率之间的最佳权衡方面的有效性。对DTU、BlendMVS和H3DS数据集的评估证实了我们方法的卓越性能。 et.al.|[2310.14487](http://arxiv.org/abs/2310.14487)|null|
|**2023-10-20**|**ManifoldNeRF: View-dependent Image Feature Supervision for Few-shot Neural Radiance Fields**|随着神经辐射场（NeRF）的出现，新的视图合成最近取得了重大进展。DietNeRF是NeRF的扩展，旨在通过为没有输入图像的未知视点引入新的损失函数，仅从少数图像中实现这一任务。损失函数假设预先训练的特征提取器应该输出相同的特征，即使输入图像是在不同的视点捕获的，因为图像包含相同的对象。然而，尽管这种假设是理想的，但在现实中，众所周知，随着视点的不断变化，特征向量也在不断变化。因此，这种假设可能会损害训练。为了避免这种有害的训练，我们提出了ManifoldNeRF，这是一种使用来自相邻已知视点的插值特征来监督未知视点的特征向量的方法。由于该方法通过插值特征为每个未知视点提供了适当的监督，因此体积表示比DietNeRF学习得更好。实验结果表明，在复杂场景下，该方法的性能优于其他方法。我们还对一组视点中的几个视点子集进行了实验，并为真实环境确定了一组有效的视点。这为实际应用程序提供了视点模式的基本策略。代码可在https://github.com/haganelego/ManifoldNeRF_BMVC2023 et.al.|[2310.13670](http://arxiv.org/abs/2310.13670)|null|
|**2023-10-23**|**Perceptual Assessment and Optimization of High Dynamic Range Image Rendering**|高动态范围（HDR）成像由于能够忠实地再现自然场景中的亮度水平而越来越受欢迎。因此，HDR图像质量评估（IQA）是至关重要的，但已被肤浅地处理。大多数现有的IQA模型都是针对低动态范围（LDR）图像开发和校准的，低动态范围图像已被证明与人类对HDR图像质量的感知相关性较差。在这项工作中，我们通过转移LDR IQA的最新进展，提出了一系列HDR IQA模型。我们方法的关键步骤是指定一个简单的反向显示模型，该模型将HDR图像分解为一组具有不同曝光的LDR图像，这些图像将由现有的LDR质量模型进行评估。然后，在简单的良好曝光度测量的帮助下，将每个曝光的局部质量分数聚合为每个曝光的全局质量分数，该全局质量分数将在曝光之间进一步加权，以获得总体质量分数。在评估LDR图像时，所提出的HDR质量模型优雅地降低到具有相同性能的原始LDR模型。在四个人类评级的HDR图像数据集上的实验表明，我们的HDR质量模型始终优于现有的IQA方法，包括HDR-VDP系列。此外，我们还展示了它们在HDR新视图合成的感知优化方面的优势。 et.al.|[2310.12877](http://arxiv.org/abs/2310.12877)|null|
|**2023-10-18**|**4K4D: Real-Time 4D View Synthesis at 4K Resolution**|本文以4K分辨率下动态三维场景的高保真度和实时视图合成为目标。最近，一些动态视图合成方法已经显示出令人印象深刻的渲染质量。然而，在渲染高分辨率图像时，它们的速度仍然有限。为了克服这个问题，我们提出了4K4D，这是一种支持硬件光栅化并实现前所未有的渲染速度的4D点云表示。我们的表示建立在4D特征网格上，这样点就可以自然正则化，并且可以进行稳健优化。此外，我们设计了一种新颖的混合外观模型，在保持效率的同时显著提高了渲染质量。此外，我们开发了一种可微分深度剥离算法，以有效地从RGB视频中学习所提出的模型。实验表明，使用RTX 4090 GPU，我们的表示可以在1080p分辨率的DNA渲染数据集上以超过400 FPS的速度渲染，在4K分辨率的ENeRF Outdoor数据集上可以以80 FPS的速度绘制，这比以前的方法快30倍，并达到了最先进的渲染质量。我们的项目页面可在https://zju3dv.github.io/4k4d/. et.al.|[2310.11448](http://arxiv.org/abs/2310.11448)|null|
|**2023-10-16**|**TOSS:High-quality Text-guided Novel View Synthesis from a Single Image**|在本文中，我们提出了TOSS，它将文本引入到仅从单个RGB图像进行新颖视图合成（NVS）的任务中。虽然Zero-1-3展示了令人印象深刻的零样本开集NVS功能，但它将NVS视为一个纯粹的图像到图像的转换问题。这种方法受到了单视图NVS具有挑战性的欠约束性质的影响：该过程缺乏明确的用户控制手段，并且经常导致令人难以置信的NVS生成。为了解决这一限制，TOSS使用文本作为高级语义信息来约束NVS解决方案空间。TOSS微调在大规模文本图像对上预先训练的文本到图像稳定扩散，并引入专门针对图像和相机姿势调节定制的模块，以及姿势正确性和精细细节保存的专门训练。进行了全面的实验，结果表明，我们提出的TOSS优于Zero-1-to-3，具有更合理、可控和多视角一致的NVS结果。我们通过全面的消融进一步支持这些结果，强调了引入的语义指导和架构设计的有效性和潜力。 et.al.|[2310.10644](http://arxiv.org/abs/2310.10644)|null|
|**2023-10-16**|**GTA: A Geometry-Aware Attention Mechanism for Multi-View Transformers**|由于变换器对输入标记的排列是等变的，因此对标记的位置信息进行编码对于许多任务是必要的。然而，由于现有的位置编码方案最初是为NLP任务设计的，因此它们对视觉任务的适用性是值得怀疑的，视觉任务通常在其数据中表现出不同的结构特性。我们认为，现有的位置编码方案对于3D视觉任务来说是次优的，因为它们不尊重其潜在的3D几何结构。基于这一假设，我们提出了一种几何感知注意力机制，该机制将令牌的几何结构编码为由查询和键值对之间的几何关系确定的相对变换。通过在稀疏宽基线多视图设置中对多个新视图合成（NVS）数据集进行评估，我们表明，我们的注意力（称为几何变换注意力（GTA））提高了最先进的基于变换器的NVS模型的学习效率和性能，而无需任何额外的学习参数和较小的计算开销。 et.al.|[2310.10375](http://arxiv.org/abs/2310.10375)|**[link](https://github.com/autonomousvision/gta)**|
|**2023-10-15**|**CBARF: Cascaded Bundle-Adjusting Neural Radiance Fields from Imperfect Camera Poses**|现有的体积神经渲染技术，如神经辐射场（NeRF），在输入图像的相机姿态不完美时，在合成高质量的新视图方面面临限制。为了解决这个问题，我们提出了一种新的3D重建框架，该框架能够同时优化相机姿态，称为CBARF（级联束调整NeRF）。简而言之，我们的框架以粗略到精细的方式优化相机姿势，然后根据校正后的姿势重建场景。观察到，相机姿态的初始化对束调整（BA）的性能有显著影响。因此，我们以不同的尺度级联多个BA模块，以逐步改善相机姿势。同时，我们制定了邻居替换策略，以进一步优化BA在每个阶段的结果。在这一步中，我们引入了一种新的标准来有效地识别估计不足的相机姿势。然后我们将它们替换为相邻相机的姿势，从而进一步消除相机姿势不准确的影响。一旦相机姿态得到优化，我们就使用密度体素网格在新视图中生成高质量的3D重建场景和图像。实验结果表明，我们的CBARF模型在姿态优化和新视图合成方面都达到了最先进的性能，尤其是在存在大的相机姿态噪声的情况下。 et.al.|[2310.09776](http://arxiv.org/abs/2310.09776)|null|
|**2023-10-12**|**Is Generalized Dynamic Novel View Synthesis from Monocular Videos Possible Today?**|从新颖的视角渲染单目视频中观察到的场景是一个具有挑战性的问题。对于静态场景，社区研究了在每个测试场景上进行优化的特定场景优化技术，以及只在测试场景上运行深网前向传递的通用技术。相反，对于动态场景，存在特定场景的优化技术，但据我们所知，目前还没有从给定的单目视频中合成动态新视图的通用方法。为了回答从单目视频中进行广义动态新视图合成在今天是否可行，我们基于现有技术建立了一个分析框架，并致力于广义方法。我们发现，在没有特定场景外观优化的情况下，伪广义过程是可能的，但需要几何和时间一致的深度估计。尽管没有特定场景的外观优化，但伪广义方法改进了一些特定场景的方法。 et.al.|[2310.08587](http://arxiv.org/abs/2310.08587)|null|
|**2023-10-12**|**Im4D: High-Fidelity and Real-Time Novel View Synthesis for Dynamic Scenes**|本文旨在解决多视图视频动态视图合成的挑战。关键的观察结果是，虽然以前的基于网格的方法提供了一致的渲染，但它们在捕捉复杂动态场景的外观细节方面做不到，在这个领域中，基于多视图图像的渲染方法表现出相反的特性。为了将两个世界中最好的结合起来，我们引入了Im4D，这是一种混合场景表示，由基于网格的几何表示和基于多视图图像的外观表示组成。具体而言，动态几何被编码为由时空特征平面和小型MLP网络组成的4D密度函数，该函数对场景结构进行全局建模，并促进渲染一致性。我们通过原始多视图视频和网络来表示场景外观，该网络学习从图像特征预测3D点的颜色，而不是完全用网络来记忆详细的外观，从而自然地使网络的学习变得更容易。我们的方法在五个动态视图合成数据集上进行了评估，包括DyNeRF、ZJU MoCap、NHR、DNA Rendering和ENeRF Outdoor数据集。结果表明，Im4D在渲染质量方面表现出最先进的性能，并且可以有效地进行训练，同时在单个RTX 3090 GPU上以79.8 FPS的速度实现512x512图像的实时渲染。 et.al.|[2310.08585](http://arxiv.org/abs/2310.08585)|null|

<p align=right>(<a href=#updated-on-20231025>back to top</a>)</p>

## 3D Reconstruction

|Publish Date|Title|Abstract|PDF|Code|
|---|---|---|---|---|
|**2023-10-23**|**Novel-View Acoustic Synthesis from 3D Reconstructed Rooms**|我们研究了将盲音频记录与3D场景信息相结合用于新视图声学合成的好处。给定2-4个麦克风的音频记录以及包含多个未知声源的场景的3D几何形状和材料，我们估计场景中任何地方的声音。我们确定了新观点声学合成的主要挑战是声源定位、分离和去混响。虽然天真地训练端到端网络无法产生高质量的结果，但我们表明，结合从3D重建房间中导出的房间脉冲响应（RIR）使同一网络能够联合处理这些任务。我们的方法优于为单个任务设计的现有方法，证明了它在利用3D视觉信息方面的有效性。在对Matterport3D NVAS数据集的模拟研究中，我们的模型在源定位方面实现了近乎完美的精度，在源分离和去混响方面实现了26.44dB的PSNR和14.23dB的SDR，在新视图声学合成方面实现了25.55dB的PSNR和14.20dB的SDR。代码、预训练模型和视频结果可在项目网页上获得(https://github.com/apple/ml-nvas3d)。 et.al.|[2310.15130](http://arxiv.org/abs/2310.15130)|**[link](https://github.com/apple/ml-nvas3d)**|
|**2023-10-23**|**Interaction-Driven Active 3D Reconstruction with Object Interiors**|我们介绍了一种主动三维重建方法，该方法集成了视觉感知、机器人-物体交互和三维扫描，以恢复目标三维物体的外部和内部，即未暴露的几何形状。与主动视觉中专注于优化相机视点以更好地研究环境的其他工作不同，我们重建的主要特征是分析目标物体各个部分的相互作用性，以及机器人随后进行的部分操作，以实现对遮挡区域的扫描。因此，在完整的几何结构采集的基础上，获得了对目标物体的部分关节的理解。我们的方法由一个内置RGBD传感器的Fetch机器人完全自动操作。它在交互分析和交互驱动的重建之间迭代，一次扫描和重建检测到的可移动零件，其中关节零件检测和网格重建都由神经网络执行。在最后一步中，重建所有剩余的非铰接部件，包括通过先前部件操作暴露并随后扫描的所有内部结构，以完成采集。我们通过定性和定量评估、消融研究、与替代方案的比较以及在真实环境中的实验来证明我们的方法的性能。 et.al.|[2310.14700](http://arxiv.org/abs/2310.14700)|null|
|**2023-10-23**|**VQ-NeRF: Vector Quantization Enhances Implicit Neural Representations**|隐式神经表示的最新进展有助于高保真度的表面重建和真实感的新视图合成。然而，这些方法中固有的计算复杂性是一个巨大的障碍，限制了实际应用中可达到的帧速率和分辨率。针对这一困境，我们提出了VQ-NeRF，这是一种通过矢量量化增强隐式神经表示的有效管道。我们的方法的本质包括将NeRF的采样空间减少到较低的分辨率，然后使用预训练的VAE解码器将其恢复到原始大小，从而有效地缓解渲染过程中遇到的采样时间瓶颈。尽管码本提供了代表性的特征，但由于高压缩率，重建场景的精细纹理细节仍然具有挑战性。为了克服这一限制，我们设计了一种创新的多尺度NeRF采样方案，该方案在压缩和原始尺度上同时优化NeRF模型，以增强网络保存精细细节的能力。此外，我们引入了语义损失函数，以提高三维重建的几何保真度和语义连贯性。大量实验证明了我们的模型在实现渲染质量和效率之间的最佳权衡方面的有效性。对DTU、BlendMVS和H3DS数据集的评估证实了我们方法的卓越性能。 et.al.|[2310.14487](http://arxiv.org/abs/2310.14487)|null|
|**2023-10-22**|**A Quantitative Evaluation of Dense 3D Reconstruction of Sinus Anatomy from Monocular Endoscopic Video**|根据内窥镜视频生成准确的3D重建是对鼻窦解剖结构和手术结果进行纵向无辐射分析的一种很有前途的途径。已经提出了几种单目重建方法，通过从运动类型算法中检索具有结构的相对相机姿态并融合单目深度估计，产生视觉上令人愉快的3D解剖结构。然而，由于底层算法和内窥镜场景的复杂特性，重建管道可能表现不佳或意外失败。此外，获取医疗数据带来了额外的挑战，在定量基准测试这些模型、了解故障案例和确定有助于其准确性的关键组件方面存在困难。在这项工作中，我们对一种自监督的鼻窦重建方法进行了定量分析，该方法使用内窥镜序列与从9个离体标本中采集的光学跟踪和高分辨率计算机断层扫描相结合。我们的结果表明，生成的重建与解剖结构高度一致，在重建和CT分割之间产生0.91mm的平均点到网格误差。然而，在与内窥镜跟踪和导航相关的点对点匹配场景中，我们发现平均目标配准误差为6.58 mm。我们发现，姿态和深度估计的不准确度对该误差的贡献相同，轨迹较短的局部一致序列会产生更准确的重建。这些结果表明，实现相对相机姿态和估计深度与解剖结构之间的全局一致性至关重要。通过这样做，我们可以确保管道的所有组成部分之间的适当协同作用，以改进重建，从而促进这项创新技术的临床应用。 et.al.|[2310.14364](http://arxiv.org/abs/2310.14364)|null|
|**2023-10-20**|**Longer-range Contextualized Masked Autoencoder**|掩模图像建模（MIM）已成为一种很有前途的自监督学习（SSL）策略。MIM预训练通过随机掩蔽一些输入像素并从剩余的像素重建掩蔽的像素，有助于使用编码器-解码器框架来学习强大的表示。然而，由于编码器是用部分像素训练的，MIM预训练可能存在理解长程依赖性的能力低的问题。这种限制可能会阻碍其完全理解多个范围依赖性的能力，导致注意力图中突出显示的区域狭窄，从而可能导致准确性下降。为了减轻这种限制，我们提出了一个自监督学习框架，称为长距离上下文化屏蔽自动编码器（LC-MAE）。LC-MAE有效地利用了对视觉表示的全局上下文理解，同时减少了输入的空间冗余。我们的方法引导编码器从多个视图中的整个像素学习，同时也从稀疏像素学习局部表示。因此，LC-MAE学习了更多的判别表示，导致性能提高，在ImageNet-1K上使用ViT-B以0.6%p的增益实现84.2%的前1级精度。我们将成功归因于增强的预训练方法，奇异值谱和注意力分析证明了这一点。最后，LC-MAE在下游语义分割和细粒度视觉分类任务中实现了显著的性能提升；以及不同的稳健评估指标。我们的代码将公开。 et.al.|[2310.13593](http://arxiv.org/abs/2310.13593)|null|
|**2023-10-20**|**Single-view 3D reconstruction via inverse procedural modeling**|我们提出了一种通过逆过程建模进行三维重建的方法，并研究了该方法的两种变体。第一种选择是使用遗传算法对输入参数进行拟合。我们展示了我们在树模型（复杂对象）上的工作结果，其中重建是大多数现有方法无法处理的。第二种选择允许我们通过在模因算法、可微分渲染和可微分过程生成器中使用梯度来显著提高精度。在我们的工作中，我们看到了两个主要贡献。首先，我们提出了一种连接可微绘制和逆过程建模的方法。当有少量输入图像可用时（即使是单个图像），这为我们提供了一个比现有方法更准确地重建3D模型的机会。其次，我们将可微和不可微的过程生成器连接在一个框架中，这使我们能够将逆过程建模应用于相当复杂的生成器：当梯度可用时，重建是精确的，当梯度不可用时，重构是近似的，但总是高质量的，没有视觉伪影。 et.al.|[2310.13373](http://arxiv.org/abs/2310.13373)|null|
|**2023-10-20**|**UE4-NeRF:Neural Radiance Field for Real-Time Rendering of Large-Scale Scene**|神经辐射场（NeRF）是一种新的隐式三维重建方法，显示出巨大的潜力，越来越受到人们的关注。它能够仅从一组照片中重建3D场景。然而，它的实时渲染能力，特别是对于大规模场景的交互式实时渲染，仍然存在很大的局限性。为了应对这些挑战，在本文中，我们提出了一种名为UE4-NeRF的新型神经渲染系统，专门为大规模场景的实时渲染而设计。我们将每个大场景划分为不同的子NeRF。为了表示分割的独立场景，我们通过在场景内构建多个规则八面体来初始化多边形网格，并在训练过程中不断优化多边形面的顶点。从细节层次（LOD）技术中获得灵感，我们针对不同的观察层次训练了不同细节层次的网格。我们的方法与虚幻引擎4（UE4）中的光栅化流水线相结合，以高达43 FPS的帧速率实现了4K分辨率的大规模场景的实时渲染。UE4内的渲染也便于在后续阶段中进行场景编辑。此外，通过实验，我们已经证明我们的方法达到了与最先进的方法相当的渲染质量。项目页面：https://jamchaos.github.io/UE4-NeRF/. et.al.|[2310.13263](http://arxiv.org/abs/2310.13263)|null|
|**2023-10-19**|**Real space iterative reconstruction for vector tomography (RESIRE-V)**|层析成像对物理、生物和医学产生了重要影响。到目前为止，大多数断层摄影应用都集中在三维标量重建上。然而，在一些关键应用中，需要矢量层析成像来重建三维矢量场，例如电场和磁场。多年来，已经开发了几种矢量层析成像方法。在这里，我们介绍了用于矢量层析成像的REal空间迭代重建的数学基础和算法实现，称为RESIRE-V。RESIRE-V使用多个倾斜系列的投影，并在投影和3D重建之间迭代。每次迭代包括使用Radon变换的前向步骤和使用其转置的后向步骤，然后通过梯度下降更新对象。结合3D支撑约束，该算法迭代地最小化误差度量，该误差度量定义为测量投影和计算投影之间的差。该算法还可以用于细化倾斜角度并进一步改进3D重建。为了验证RESIRE-V，我们首先将其应用于3D磁化矢量场的模拟数据集，该数据集由两个正交倾斜序列组成，每个倾斜序列都有一个缺失的楔块。我们的定量分析表明，重建的磁化矢量场的三个分量与地面实况相一致。然后，我们使用RESIRE-V重建了由三个倾斜序列组成的铁磁超晶格的三维磁化矢量场。我们的三维矢量重建揭示了具有正电荷和负电荷的拓扑磁缺陷的存在。我们期望RESIRE-V可以作为一种通用的矢量层析成像方法被纳入不同的成像模式中。 et.al.|[2310.12513](http://arxiv.org/abs/2310.12513)|**[link](https://github.com/minhpham0309/resire-v)**|
|**2023-10-19**|**MTS-LOF: Medical Time-Series Representation Learning via Occlusion-Invariant Features**|医疗时间序列数据在医疗保健中不可或缺，为疾病诊断、治疗计划和患者管理提供重要见解。在先进传感器技术的推动下，数据复杂性呈指数级增长，这给数据标签带来了挑战。自我监督学习（SSL）已成为应对这些挑战的一种变革性方法，消除了对大量人工注释的需求。在本研究中，我们介绍了一种新的医学时间序列表示学习框架，称为MTS-LOF。MTS-LOF利用了对比学习和掩蔽自动编码器（MAE）方法的优势，为医学时间序列数据的表示学习提供了一种独特的方法。通过结合这些技术，MTS-LOF通过提供更复杂、上下文丰富的表示，增强了医疗保健应用的潜力。此外，MTS-LOF采用多掩蔽策略来促进遮挡不变特征学习。这种方法允许模型通过屏蔽部分数据来创建数据的多个视图。通过最小化这些屏蔽补丁和完全可见补丁的表示之间的差异，MTS-LOF学会了在医学时间序列数据集中捕获丰富的上下文信息。在不同的医学时间序列数据集上进行的实验结果证明了MTS-LOF优于其他方法。这些发现有望通过改进表征学习来显著增强医疗保健应用。此外，我们的工作深入研究了联合嵌入SSL和MAE技术的集成，揭示了医疗保健数据中时间和结构依赖性之间的复杂相互作用。这种理解至关重要，因为它使我们能够掌握医疗保健数据分析的复杂性。 et.al.|[2310.12451](http://arxiv.org/abs/2310.12451)|null|
|**2023-10-18**|**ShapeGraFormer: GraFormer-Based Network for Hand-Object Reconstruction from a Single Depth Map**|手对象操作的三维重建对于模拟人类动作是重要的。大多数处理具有挑战性的对象操作场景的方法都专注于孤立的手部重建，忽略了由于对象接触而产生的物理和运动学约束。一些方法通过联合重建3D手-对象交互来产生更真实的结果。然而，它们专注于粗略的姿态估计或依赖于已知的手和物体形状。我们提出了第一种从单个深度图重建逼真的3D手对象形状和姿势的方法。与之前的工作不同，我们基于体素的重建网络回归手和物体的顶点坐标，并重建更真实的交互。我们的管道还预测了体素化的手对象形状，具有与输入体素化深度的一对一映射。然后，我们利用最近的GraFormer网络和位置嵌入，从模板网格中重建形状，从而利用手和物体形状的图形特性。此外，我们还展示了添加另一个GraFormer组件的影响，该组件基于手与物体的交互来细化重建的形状，并能够重建更准确的物体形状。我们对HO-3D和DexYCB数据集进行了广泛的评估，并表明我们的方法在手部重建方面优于现有方法，并为物体产生了合理的重建 et.al.|[2310.11811](http://arxiv.org/abs/2310.11811)|null|

<p align=right>(<a href=#updated-on-20231025>back to top</a>)</p>

## Diffusion

|Publish Date|Title|Abstract|PDF|Code|
|---|---|---|---|---|
|**2023-10-24**|**From Posterior Sampling to Meaningful Diversity in Image Restoration**|图像恢复问题通常是病态的，因为每个退化的图像都可以以无限多种有效的方式进行恢复。为了适应这一点，许多作品通过尝试在给定退化输入的情况下从自然图像的后验分布中随机采样来生成一组不同的输出。在这里，我们认为这种策略通常具有有限的实用价值，因为后验分布的尾部很重。例如，考虑修复图像中缺失的天空区域。由于缺失区域很有可能只包含云而不包含任何物体，因此来自后方的任何一组样本都将完全由（实际上相同的）天空完整性所支配。然而，可以说，只向用户展示一个晴朗的天空，以及飞艇、鸟类和气球等几种替代解决方案，会更好地勾勒出一系列可能性。在本文中，我们开始了有意义的多样化图像恢复的研究。我们探索了几种后处理方法，这些方法可以与任何不同的图像恢复方法相结合，以产生语义上有意义的多样性。此外，我们提出了一种实用的方法，允许基于扩散的图像恢复方法生成有意义的不同输出，同时只产生疏忽的计算开销。我们进行了广泛的用户研究来分析所提出的技术，并发现降低输出之间相似性的策略比后验采样更有利。代码和示例可在https://noa-cohen.github.io/MeaningfulDiversityInIR et.al.|[2310.16047](http://arxiv.org/abs/2310.16047)|null|
|**2023-10-24**|**The ballistic to diffusive crossover in a weakly-interacting Fermi gas**|即使在没有无序的情况下，电荷和能量也会在有限温度下在费米子的相互作用系统中扩散，相互作用会导致从早期的准粒子的相干和弹道流到后期的非相干扩散行为的交叉。相关的交叉时间尺度和传输系数都受到相互作用强度的控制。在这项工作中，我们开发了一种数值方法，通过将耗散辅助算子进化（DAOE）应用于费米子，在高温下模拟这种系统，适用于广泛的相互作用强度。我们的费米子DAOE通过系统地丢弃高 $n$-点函数中的信息来近似精确的动力学，它被定制为精确地捕捉非相互作用动力学，从而为弱相互作用问题提供了一个良好的起点。将我们的方法应用于弱相互作用费米子的微观模型，我们数值证明了从弹道输运到扩散输运的交叉发生在时间$t_D\sim1/\Delta^｛2｝$，并且扩散常数类似于$D\sim 1/\Delta ^2$，其中$\Delta$是相互作用强度。我们用算子展开图中的费米黄金法则计算来证实这种缩放，将$t_D$ 解释为单粒子格林函数的费米子-费米子散射时间和寿命。 et.al.|[2310.16043](http://arxiv.org/abs/2310.16043)|null|
|**2023-10-24**|**Weak well-posedness of stochastic Volterra equations with completely monotone kernels and non-degenerate noise**|在温和正则性假设下，我们建立了具有完全单调核和非退化噪声的随机Volterra方程（简称SVE）的弱存在唯一性律。特别地，我们的结果揭示了具有奇异核的SVE的噪声效应正则化，允许具有H\“{o}lder扩散系数。为了证明我们的结果，我们将SVE重新表述为定义在Hilbert空间的Gelfand三元组上的等价随机演化方程（简称SEE）。我们使用随机控制自变量证明了SEE的弱适定性，然后将其转化为原始的SVE。 et.al.|[2310.16030](http://arxiv.org/abs/2310.16030)|null|
|**2023-10-24**|**Regularization estimates of the Landau-Coulomb diffusion**|目前，Landau-Coulomb方程对于任意大次数是否具有唯一的光滑解还不确定。除了扩散项，这个方程还包括一个反应项，它可以快速地将良好的构型转化为奇点。在这篇文章中，我们证明了朗道-库仑方程中的扩散算子比其线性对应算子拉普拉斯算子提供了更强的L^1到L^infty正则化效应。我们的新量化表明，当寻求全局适定性的证明时，非线性扩散项可能发挥关键作用。 et.al.|[2310.16012](http://arxiv.org/abs/2310.16012)|null|
|**2023-10-24**|**CVPR 2023 Text Guided Video Editing Competition**|人类每天观看超过十亿小时的视频。这个视频的大部分都是手动编辑的，这是一个乏味的过程。然而，人工智能视频生成和视频编辑正在兴起。在稳定扩散和Imagen等文本到图像模型的基础上，生成人工智能在视频任务上有了显著的改进。但很难评估这些视频任务的进展，因为没有标准的基准。因此，我们提出了一个用于文本引导视频编辑（TGVE）的新数据集，并在CVPR举办了一场竞赛，以评估TGVE数据集上的模型。在这篇文章中，我们回顾了这场比赛，并描述了获胜的方法。竞争数据集可在https://sites.google.com/view/loveucvpr23/track4. et.al.|[2310.16003](http://arxiv.org/abs/2310.16003)|null|
|**2023-10-24**|**Classical wave-particle localization in disordered landscapes**|从生物学、活性物质到电子学，了解粒子在无序环境中移动的能力是无数环境中的核心问题。当宏观粒子的能量超过随机背景的特征势垒时，它们最终表现出扩散运动。相比之下，量子波粒二象性导致无序介质中的亚原子粒子即使在电势很弱的情况下也会静止下来——这是一种被称为Anderson局域化的显著现象，迄今为止被认为是量子领域独有的。在这里，我们提出了一个流体动力学波粒系统，一个在淹没的随机地形上由自己的波场自我引导的毫米液滴，其动力学表现出类似于量子系统的局部统计。对粒子轨迹集合的考虑揭示了当波场在无序地形上延伸时不存在扩散。通过液滴与自激导波场之间的共振耦合，对涌现统计进行了合理化。这种流体动力学模拟物展示了经典粒子如何像波浪一样定位，为未来各个领域的研究提供了新的方向，包括波浪定位、多体定位和拓扑物质。 et.al.|[2310.16000](http://arxiv.org/abs/2310.16000)|null|
|**2023-10-24**|**Improving Robustness and Reliability in Medical Image Classification with Latent-Guided Diffusion and Nested-Ensembles**|虽然深度学习模型在一系列医学图像分析任务中取得了显著成功，但在实际临床环境中部署这些模型需要它们对采集图像的可变性具有鲁棒性。虽然许多方法应用预定义的转换来增强训练数据以增强测试时间的稳健性，但这些转换可能无法确保模型对患者图像中看到的各种可变性的稳健性。在本文中，我们介绍了一种新的基于变压器和条件扩散模型的三阶段方法，目的是提高模型对实践中常见的成像可变性的鲁棒性，而不需要预先确定的数据增强策略。为此，多个图像编码器首先学习层次特征表示，以构建判别潜在空间。接下来，在潜在代码的引导下，反向扩散过程作用于信息先验，并以生成的方式提出预测候选者。最后，在双层聚合协议中聚合几个预测候选者以产生最终输出。通过在医学成像基准数据集上进行的大量实验，我们表明我们的方法在稳健性和置信度校准方面优于最先进的方法。此外，我们引入了一种策略来量化实例级别的预测不确定性，提高了它们对临床实践中使用它们的临床医生的可信度。 et.al.|[2310.15952](http://arxiv.org/abs/2310.15952)|null|
|**2023-10-24**|**Language-driven Scene Synthesis using Multi-conditional Diffusion Model**|场景合成是一个具有挑战性的问题，具有多种工业应用。最近，已经进行了大量的努力来使用人体运动、房间布局或空间图作为输入来合成场景。然而，很少有研究从多种模式，特别是结合文本提示来解决这个问题。在本文中，我们提出了一种语言驱动的场景合成任务，这是一种集成文本提示、人体运动和现有对象进行场景合成的新任务。与其他单条件合成任务不同，我们的问题涉及多个条件，需要一种将它们处理和编码到统一空间中的策略。为了应对这一挑战，我们提出了一个多条件扩散模型，该模型与其他扩散文献的隐式统一方法不同，它明确预测了原始数据分布的指导点。我们证明，我们的方法在理论上是支持性的。密集的实验结果表明，我们的方法优于最先进的基准测试，并支持自然场景编辑应用。源代码和数据集可以访问https://lang-scene-synth.github.io/. et.al.|[2310.15948](http://arxiv.org/abs/2310.15948)|**[link](https://github.com/andvg3/LSDM)**|
|**2023-10-24**|**$L^2$-Wasserstein contraction for Euler schemes of elliptic diffusions and interacting particle systems**|我们展示了离散扩散过程的过渡核的$L^2$-Waserstein收缩，在漂移的无穷大收缩性条件下，以及足够高的扩散率要求。这扩展了最近的结果，即在漂移的类似假设下，但没有扩散率限制，显示$L^1$-Waserstein收缩，或$p>1$的$L^p$-Wasenstein边界，然而，这不是真正的收缩。我们解释了如何显示真正的$L^2$-Waserstein收缩对于获得扩散Euler格式的过渡核的局部Poincar不等式是至关重要的。此外，我们还讨论了收缩结果的其他后果，如KL散度和总变异中的集中不等式和收敛率。我们还研究了相互作用扩散离散化的相应$L^2$ -Waserstein收缩。作为一个特殊的应用，这使我们能够分析粒子系统的行为，这些行为可以用来近似最近在平均场优化文献中研究的一类McKean Vlasov SDE。 et.al.|[2310.15897](http://arxiv.org/abs/2310.15897)|null|
|**2023-10-24**|**Long time behavior of a porous medium model with degenerate hysteresis**|在非饱和多孔介质中，由于液气界面上的表面张力引起的压力-饱和关系的滞后，在所得到的质量平衡方程中表现出强烈的简并性。作为先前存在性和唯一性结果的推广，我们证明了在物理容许的初始条件下，在不与外部进行质量交换的情况下，流体扩散问题的唯一全局解是存在的，并且随着时间趋于无穷大，渐近收敛于可能的非齐次质量分布和先验未知的常压。 et.al.|[2310.15881](http://arxiv.org/abs/2310.15881)|null|

<p align=right>(<a href=#updated-on-20231025>back to top</a>)</p>

## NeRF

|Publish Date|Title|Abstract|PDF|Code|
|---|---|---|---|---|
|**2023-10-24**|**LiCROM: Linear-Subspace Continuous Reduced Order Modeling with Neural Fields**|线性降阶建模（ROM）通过使用简化的运动学表示来近似系统的行为，从而简化了复杂的模拟。通常，ROM在使用特定空间离散化创建的输入模拟上进行训练，然后用于使用相同的离散化加速模拟。这种离散化依赖性是有限制的。独立于特定的离散化将提供在训练数据中混合和匹配网格分辨率、连通性和类型（四面体、六面体）的灵活性；以在训练过程中看不到的新颖离散化来加速模拟；以及加速在时间上或参数化地改变离散化的自适应模拟。我们提出了一种灵活的、独立于离散化的降阶建模方法。与传统ROM一样，我们将配置表示为位移场的线性组合。与传统的ROM不同，我们的位移场是从参考域上的每个点到相应位移矢量的连续映射；这些映射被表示为隐式神经场。使用线性连续ROM（LiCROM），我们的训练集可以包括经历多个加载条件的多个几何体，与它们的离散化无关。这为降阶建模的新应用打开了大门。我们现在可以加速在运行时修改几何体的模拟，例如通过切割、打孔，甚至交换整个网格。我们还可以加速对训练中看不见的几何形状的模拟。我们演示了一次性泛化，在单个几何体上进行训练，然后模拟各种看不见的几何体。 et.al.|[2310.15907](http://arxiv.org/abs/2310.15907)|null|
|**2023-10-12**|**S4C: Self-Supervised Semantic Scene Completion with Neural Fields**|三维语义场景理解是计算机视觉中的一个基本挑战。它使移动代理能够自主规划和导航任意环境。SSC将这一挑战形式化为从场景的稀疏观测中联合估计密集的几何结构和语义信息。当前的SSC方法通常基于聚合的激光雷达扫描在3D地面实况上进行训练。这一过程依赖于特殊的传感器和手工注释，这些传感器和注释成本高昂且规模不大。为了克服这个问题，我们的工作提出了第一种称为S4C的SSC自监督方法，该方法不依赖于3D地面实况数据。我们提出的方法可以从单个图像重建场景，并且只依赖于训练期间从现成的图像分割网络生成的视频和伪分割地面实况。与使用离散体素网格的现有方法不同，我们将场景表示为隐式语义场。该公式允许查询相机截锥体内的任何点的占用率和语义类。我们的架构是通过基于渲染的自监督损失进行训练的。尽管如此，我们的方法实现了接近于完全监督的最先进方法的性能。此外，我们的方法表现出强大的泛化能力，可以为遥远的视点合成准确的分割图。 et.al.|[2310.07522](http://arxiv.org/abs/2310.07522)|null|
|**2023-10-07**|**HI-SLAM: Monocular Real-time Dense Mapping with Hybrid Implicit Fields**|在这封信中，我们提出了一个基于神经场的实时单目映射框架，用于精确和密集的同时定位和映射（SLAM）。最近的神经映射框架显示出有希望的结果，但依赖于RGB-D或姿势输入，或者无法实时运行。为了解决这些局限性，我们的方法将密集SLAM与神经隐式场相结合。具体来说，我们的密集SLAM方法运行并行跟踪和全局优化，而基于神经场的映射是基于最新的SLAM估计逐步构建的。为了有效地构造神经场，我们采用了多分辨率网格编码和符号距离函数（SDF）表示。这使我们能够始终保持地图的最新状态，并通过循环关闭立即适应全球更新。为了全局一致性，我们提出了一种有效的基于Sim（3）的姿态图束调整（PGBA）方法来运行在线闭环并减轻姿态和尺度漂移。为了进一步提高深度精度，我们结合了学习的单目深度先验。我们提出了一种新的深度和尺度联合调整（JDSA）模块来解决深度先验中固有的尺度模糊性。对合成和真实世界数据集的广泛评估验证了我们的方法在准确性和地图完整性方面优于现有方法，同时保持了实时性能。 et.al.|[2310.04787](http://arxiv.org/abs/2310.04787)|null|
|**2023-10-05**|**Variational Barycentric Coordinates**|我们提出了一种变分技术来优化广义重心坐标，与现有模型相比，该技术提供了额外的控制。先前的工作使用网格或闭式公式表示重心坐标，在实践中限制了目标函数的选择。相反，我们使用神经场直接参数化连续函数，该函数将多面体内部的任何坐标映射到其重心坐标。这个公式是通过我们对重心坐标的理论表征实现的，这使我们能够构建将有效坐标的整个函数类参数化的神经场。我们使用各种目标函数展示了我们模型的灵活性，包括多重光滑性和变形感知能量；作为补充，我们还提出了数学上合理的方法来测量和最小化目标，如不连续神经场的总变化。我们提供了一个实用的加速策略，对我们的算法进行了彻底的验证，并展示了几个应用。 et.al.|[2310.03861](http://arxiv.org/abs/2310.03861)|null|
|**2023-10-05**|**High-Degrees-of-Freedom Dynamic Neural Fields for Robot Self-Modeling and Motion Planning**|机器人自模型是机器人物理形态的任务不可知表示，在没有经典几何运动学模型的情况下，可用于运动规划任务。特别是，当后者难以设计或机器人的运动学发生意外变化时，人类自由的自我建模是真正自主智能体的必要特征。在这项工作中，我们利用神经场使机器人能够将其运动学自建模为仅从带有相机姿势和配置的2D图像中学习的神经隐式查询模型。这使得比依赖于深度图像或几何知识的现有方法具有更大的适用性。为此，除了课程数据采样策略外，我们还提出了一种新的基于编码器的神经密度场架构，用于高自由度（DOF）条件下的动态对象中心场景。在7自由度机器人测试装置中，学习的自模型实现了机器人工作空间尺寸2%的倒角-L2距离。作为一个示例性的下游应用程序，我们展示了该模型在运动规划任务中的能力。 et.al.|[2310.03624](http://arxiv.org/abs/2310.03624)|null|
|**2023-10-02**|**Neural Processing of Tri-Plane Hybrid Neural Fields**|在用于存储和通信3D数据的神经场的吸引人的特性的驱动下，直接处理它们以解决分类和零件分割等任务的问题已经出现，并在最近的工作中进行了研究。早期的方法使用由在整个数据集上训练的共享网络参数化的神经场，实现了良好的任务性能，但牺牲了重建质量。为了改进后者，后来的方法侧重于参数化为大型多层感知器（MLP）的单个神经场，然而，由于权重空间的高维性、固有的权重空间对称性和对随机初始化的敏感性，这些神经元场的处理具有挑战性。因此，结果明显不如通过处理显式表示（例如点云或网格）所获得的结果。与此同时，混合表示，特别是基于三平面的混合表示，已经成为实现神经场的一种更有效的替代方案，但其直接处理尚未得到研究。在本文中，我们证明了三平面离散数据结构编码了丰富的信息，标准的深度学习机器可以有效地处理这些信息。我们定义了一个广泛的基准，涵盖了一组不同的字段，如占用率、有符号/无符号距离，以及首次定义的辐射字段。在处理具有相同重建质量的字段时，我们实现的任务性能远远优于处理大型MLP的框架，并且首次几乎与处理显式表示的架构不相上下。 et.al.|[2310.01140](http://arxiv.org/abs/2310.01140)|**[link](https://github.com/CVLAB-Unibo/triplane_processing)**|
|**2023-09-27**|**Neural Acoustic Context Field: Rendering Realistic Room Impulse Response With Neural Fields**|房间脉冲响应（RIR）测量声音在环境中的传播，对于合成给定环境下的高保真音频至关重要。一些先前的工作已经提出将RIR表示为声音发射器和接收器位置的神经场函数。然而，这些方法没有充分考虑音频场景的声学特性，导致性能不令人满意。这封信提出了一种新的神经声学上下文场方法，称为NACF，通过利用多个声学上下文（如几何结构、材料特性和空间信息）来参数化音频场景。在RIR的独特性质，即时间不光滑性和单调能量衰减的驱动下，我们设计了一个时间相关模块和多尺度能量衰减准则。实验结果表明，NACF的性能显著优于现有的基于字段的方法。请访问我们的项目页面了解更多定性结果。 et.al.|[2309.15977](http://arxiv.org/abs/2309.15977)|null|
|**2023-09-27**|**SHACIRA: Scalable HAsh-grid Compression for Implicit Neural Representations**|隐式神经表示（INR）或神经场已成为编码多媒体信号（如图像和辐射场）同时保持高质量的流行框架。最近，Instant NGP提出的可学习特征网格通过用特征向量的多分辨率查找表和更小的神经网络取代大型神经网络，在训练和INR采样方面实现了显著的加速。然而，这些功能网格是以大量内存消耗为代价的，这可能是存储和流应用程序的瓶颈。在这项工作中，我们提出了SHACIRA，这是一个简单而有效的任务无关框架，用于压缩这种特征网格，而不需要额外的事后修剪/量化阶段。我们用量化的潜在权重对特征网格进行重新参数化，并在潜在空间中应用熵正则化，以在各个领域实现高水平的压缩。在由图像、视频和辐射场组成的不同数据集上的定量和定性结果表明，我们的方法优于现有的INR方法，而不需要任何大型数据集或特定领域的启发式方法。我们的项目页面可在http://shacira.github.io。 et.al.|[2309.15848](http://arxiv.org/abs/2309.15848)|null|
|**2023-09-27**|**NeuRBF: A Neural Fields Representation with Adaptive Radial Basis Functions**|我们提出了一种新型的神经场，它使用一般的径向基来表示信号。现有技术的神经领域通常依赖于用于存储局部神经特征的基于网格的表示和用于在连续查询点处插值特征的N维线性核。它们的神经特征的空间位置固定在网格节点上，不能很好地适应目标信号。相反，我们的方法建立在具有灵活内核位置和形状的通用径向基上，这些径向基具有更高的空间自适应性，可以更紧密地拟合目标信号。为了进一步提高径向基函数的信道容量，我们建议将它们与多频率正弦函数组合。该技术将径向基扩展到不同频带的多个傅立叶径向基，而不需要额外的参数，便于细节的表示。此外，通过将自适应径向基与基于网格的径向基相结合，我们的混合组合继承了自适应性和插值平滑性。我们精心设计了加权方案，使径向基有效地适应不同类型的信号。我们在2D图像和3D符号距离场表示上的实验证明了我们的方法比现有技术更高的精度和紧凑性。当应用于神经辐射场重建时，我们的方法实现了最先进的渲染质量，模型大小小，训练速度相当。 et.al.|[2309.15426](http://arxiv.org/abs/2309.15426)|**[link](https://github.com/oppo-us-research/NeuRBF)**|
|**2023-09-29**|**3D Reconstruction with Generalizable Neural Fields using Scene Priors**|由于神经领域的最新进展，高保真3D场景重建得到了实质性的推进。然而，大多数现有的方法为每个单独的场景从头开始训练单独的网络。这是不可扩展的，效率低下，并且在视图有限的情况下无法产生良好的结果。虽然基于学习的多视图立体方法在一定程度上缓解了这一问题，但它们的多视图设置使其扩展和广泛应用的灵活性降低。相反，我们引入了结合场景先验（NFP）的训练可推广神经场。NFP网络将任何单视图RGB-D图像映射为带符号的距离和辐射值。在没有融合模块的情况下，可以通过合并体积空间中的各个帧来重建完整的场景，这提供了更好的灵活性。场景先验可以在大规模数据集上进行训练，从而能够快速适应具有较少视图的新场景的重建。NFP不仅展示了SOTA场景重建的性能和效率，而且还支持单图像新视图合成，这在神经领域还没有得到充分的探索。更多定性结果可在以下网站获得：https://oasisyang.github.io/neural-prior et.al.|[2309.15164](http://arxiv.org/abs/2309.15164)|null|

<p align=right>(<a href=#updated-on-20231025>back to top</a>)</p>

[contributors-shield]: https://img.shields.io/github/contributors/Vincentqyw/cv-arxiv-daily.svg?style=for-the-badge
[contributors-url]: https://github.com/Vincentqyw/cv-arxiv-daily/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/Vincentqyw/cv-arxiv-daily.svg?style=for-the-badge
[forks-url]: https://github.com/Vincentqyw/cv-arxiv-daily/network/members
[stars-shield]: https://img.shields.io/github/stars/Vincentqyw/cv-arxiv-daily.svg?style=for-the-badge
[stars-url]: https://github.com/Vincentqyw/cv-arxiv-daily/stargazers
[issues-shield]: https://img.shields.io/github/issues/Vincentqyw/cv-arxiv-daily.svg?style=for-the-badge
[issues-url]: https://github.com/Vincentqyw/cv-arxiv-daily/issues

