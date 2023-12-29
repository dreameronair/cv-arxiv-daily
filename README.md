[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]

## Updated on 2023.12.29
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
|**2023-12-28**|**iFusion: Inverting Diffusion for Pose-Free Reconstruction from Sparse Views**|我们提出了iFusion，这是一种新颖的3D对象重建框架，只需要两个具有未知相机姿态的视图。虽然单视图重建会产生视觉上吸引人的结果，但它可能会与实际对象有很大的偏差，尤其是在看不见的一侧。附加视图提高了重建保真度，但需要已知的摄影机姿势。然而，假设姿态的可用性可能是不现实的，并且现有的姿态估计器在稀疏视图场景中失败。为了解决这一问题，我们利用了一个预先训练的新颖视图合成扩散模型，该模型嵌入了关于不同对象的几何形状和外观的隐含知识。我们的策略分为三个步骤：（1）我们反转用于相机姿态估计的扩散模型，而不是合成新的视图。（2） 使用提供的视图和估计的姿态对扩散模型进行微调，使其成为为目标对象量身定制的新型视图合成器。（3） 利用配准的视图和微调的扩散模型，我们重建了3D对象。实验表明，在姿态估计和新视图合成方面都有很强的性能。此外，iFusion与各种重建方法无缝集成，并对其进行了增强。 et.al.|[2312.17250](http://arxiv.org/abs/2312.17250)|**[link](https://github.com/chinhsuanwu/ifusion)**|
|**2023-12-28**|**Spacetime Gaussian Feature Splatting for Real-Time Dynamic View Synthesis**|动态场景的新颖视图合成一直是一个有趣但具有挑战性的问题。尽管取得了最新进展，但同时实现高分辨率的真实照片效果、实时渲染和紧凑的存储仍然是一项艰巨的任务。为了应对这些挑战，我们提出了时空高斯特征飞溅作为一种新的动态场景表示，由三个关键组件组成。首先，我们通过增强具有时间不透明度和参数运动/旋转的3D高斯，来形成富有表现力的时空高斯。这使得时空高斯能够捕捉场景中的静态、动态以及瞬态内容。其次，我们介绍了飞溅特征渲染，它用神经特征代替了球面谐波。这些功能有助于在保持小尺寸的同时对视图和与时间相关的外观进行建模。第三，我们利用训练误差和粗略深度的指导，在难以与现有管道融合的区域对新的高斯采样。在几个已建立的真实世界数据集上的实验表明，我们的方法在保持紧凑存储的同时，实现了最先进的渲染质量和速度。在8K分辨率下，我们的lite版本模型可以在Nvidia RTX 4090 GPU上以60 FPS的速度渲染。 et.al.|[2312.16812](http://arxiv.org/abs/2312.16812)|null|
|**2023-12-26**|**DL3DV-10K: A Large-Scale Scene Dataset for Deep Learning-based 3D Vision**|我们见证了基于深度学习的3D视觉的重大进展，从基于神经辐射场（NeRF）的3D表示学习到在新视图合成（NVS）中的应用。然而，用于基于深度学习的3D视觉的现有场景级数据集，仅限于合成环境或现实世界场景的狭窄选择，是非常不足的。这种不足不仅阻碍了现有方法的全面基准，而且限制了在基于深度学习的3D分析中可以探索的内容。为了解决这一关键差距，我们展示了DL3DV-10K，这是一个大型场景数据集，其特征是从65种类型的兴趣点（POI）位置捕获的10510个视频中的5120万帧，涵盖了有界和无界场景，具有不同的反射、透明度和光照水平。我们在DL3DV-10K上对最近的NVS方法进行了全面的基准测试，为未来的NVS研究提供了宝贵的见解。此外，我们在一项从DL3DV-10K学习可推广NeRF的试点研究中获得了令人鼓舞的结果，这表明了大规模场景级数据集的必要性，以打造学习3D表示的基础模型。我们的DL3DV-10K数据集、基准测试结果和模型将在https://dl3dv-10k.github.io/DL3DV-10K/. et.al.|[2312.16256](http://arxiv.org/abs/2312.16256)|null|
|**2023-12-26**|**fMPI: Fast Novel View Synthesis in the Wild with Layered Scene Representations**|在这项研究中，我们为基于分层场景表示的新视图合成（NVS）方法提出了两种新的输入处理范式，这两种方法在不影响质量的情况下显著提高了它们的运行时间。我们的方法识别并减轻了传统管道最耗时的两个方面：构建和处理所谓的平面扫描体积（PSV），这是输入相机视图的平面重新投影的高维张量。特别是，我们建议在并行组中处理该张量，以提高计算效率，并对相邻输入平面进行超采样，从而生成更密集、更准确的场景表示。所提出的增强提供了显著的灵活性，允许在性能和速度之间取得平衡，从而朝着实时应用迈出了实质性的步伐。此外，它们非常通用，因为任何基于PSV的方法都可以使用它们，包括使用多平面图像、多球体图像和分层深度图像的方法。在一组全面的实验中，我们证明了我们提出的范式能够设计出一种NVS方法，该方法在公共基准上达到最先进的水平，同时比现有的最先进的方法快50倍。它在速度方面也比目前的前辈高出3倍多，同时实现了明显更好的渲染质量。 et.al.|[2312.16109](http://arxiv.org/abs/2312.16109)|null|
|**2023-12-25**|**Sparse-view CT Reconstruction with 3D Gaussian Volumetric Representation**|稀疏视图CT是减少传统CT扫描辐射剂量的一种很有前途的策略，但从不完整和有噪声的数据中重建高质量图像是一项挑战。最近，3D高斯已被应用于复杂自然场景的建模，与隐式神经表示（INRs）相比，它表现出快速收敛和更好的新颖视图渲染。我们从3D高斯在自然场景建模和新视图合成中的成功应用中获得灵感，研究了它们在稀疏视图CT重建中的潜力。我们利用来自滤波后的反投影重建图像的先验信息来初始化高斯；并且通过比较投影空间中的差异来更新它们的参数。自适应密度控制进一步提高了性能。与INRs相比，3D高斯从先验信息中受益更多，可以明确绕过空白空间中的学习，并有效地分配容量，加速收敛。3D高斯还可以有效地学习高频细节。3D高斯以自我监督的方式进行训练，避免了对大规模配对数据的需要。我们在AAPM-Mayo数据集上的实验表明，与基于INR的方法相比，3D高斯可以提供优越的性能。这项工作正在进行中，代码将公开。 et.al.|[2312.15676](http://arxiv.org/abs/2312.15676)|null|
|**2023-12-22**|**Deformable 3D Gaussian Splatting for Animatable Human Avatars**|神经辐射场的最新进展使得能够在动态设置中对照片真实感图像进行新颖的视图合成，这可以应用于具有人类动画的场景。然而，通常使用的隐式主干来建立准确的模型，需要许多输入视图和额外的注释，如人体遮罩、UV贴图和深度贴图。在这项工作中，我们提出了ParDy Human（参数化动态人类化身），这是一种完全明确的方法，可以从一个单一的单目序列中构建数字化身。ParDy Human在3D高斯飞溅中引入了参数驱动的动力学，其中通过人体姿势模型使3D高斯变形以使化身动画化。我们的方法由两个部分组成：第一个模块根据SMPL顶点使标准3D高斯变形，第二个模块进一步采用其设计的联合编码并预测每高斯变形，以处理SMPL顶点变形之外的动力学。然后通过光栅化器合成图像。ParDy Human构成了逼真动态人类化身的显式模型，其需要显著更少的训练视图和图像。我们的化身学习不需要额外的注释，如掩码，并且可以在可变背景下进行训练，同时即使在消费硬件上也能高效地推断出全分辨率图像。我们提供的实验证据表明，在ZJU MoCap和THUman4.0数据集上，ParDy-Human在数量和视觉上都优于最先进的方法。 et.al.|[2312.15059](http://arxiv.org/abs/2312.15059)|null|
|**2023-12-21**|**PlatoNeRF: 3D Reconstruction in Plato's Cave via Single-View Two-Bounce Lidar**|由于单目线索的模糊性和缺乏关于遮挡区域的信息，从单个视图进行3D重建是具有挑战性的。神经辐射场（NeRF）虽然在视图合成和3D重建中很受欢迎，但通常依赖于多视图图像。现有的使用NeRF进行单视图3D重建的方法要么依赖于数据先验来幻觉被遮挡区域的视图，这在物理上可能不准确，要么依赖于RGB相机观察到的阴影，这在环境光和低反照率背景中很难检测到。我们建议使用单光子雪崩二极管捕获的飞行时间数据来克服这些限制。我们的方法使用NeRF对两个反弹光路进行建模，使用激光雷达瞬态数据进行监督。通过利用激光雷达测量的NeRF和双反射光的优势，我们证明了我们可以在没有数据先验或依赖受控环境照明或场景反照率的情况下重建可见和遮挡的几何结构。此外，我们还展示了在传感器空间和时间分辨率的实际约束下改进的泛化能力。我们相信，随着单光子激光雷达在手机、平板电脑和耳机等消费设备上无处不在，我们的方法是一个很有前途的方向。 et.al.|[2312.14239](http://arxiv.org/abs/2312.14239)|null|
|**2023-12-21**|**SyncDreamer for 3D Reconstruction of Endangered Animal Species with NeRF and NeuS**|本研究的主要目的是演示如何使用创新的视图合成和3D重建技术，使用单目RGB图像创建濒危物种的模型。为了实现这一点，我们使用SyncDreamer来产生独特的视角，并使用NeuS和NeRF来重建3D表示。我们选择了四种不同的动物，包括东方鹳、青蛙、蜻蜓和老虎，作为我们的研究对象。我们的研究结果表明，SyncDreamer、NeRF和NeuS技术的结合可以成功创建濒危动物的3D模型。然而，我们也观察到NeuS产生了模糊的图像，而NeRF产生了更清晰但更嘈杂的图像。这项研究突出了模拟濒危动物的潜力，并为该领域的未来研究提供了新的方向。通过展示这些先进技术的有效性，我们希望鼓励进一步探索和发展保护和研究濒危物种的技术。 et.al.|[2312.13832](http://arxiv.org/abs/2312.13832)|null|
|**2023-12-21**|**DyBluRF: Dynamic Deblurring Neural Radiance Fields for Blurry Monocular Video**|视频视图合成允许从任意视点和时间创建具有视觉吸引力的帧，提供身临其境的观看体验。神经辐射场，特别是最初为静态场景开发的NeRF，刺激了视频视图合成的各种方法的产生。然而，视频视图合成的挑战来自运动模糊，这是物体或相机在曝光过程中移动的结果，阻碍了清晰的时空视图的精确合成。作为回应，我们提出了一种用于模糊单目视频的新的动态去模糊NeRF框架，称为DyBluRF，由Interleave Ray Refinement（IRR）阶段和基于运动分解的去模糊（MDD）阶段组成。我们的DyBluRF是第一个解决和处理模糊单目视频的新型视图合成的公司。IRR阶段联合重建动态3D场景，并细化不准确的相机姿态信息，以对抗从给定模糊帧中提取的不准确姿态信息。MDD阶段是一种新的增量潜在锐射线预测（ILSP）方法，用于模糊单目视频帧，将潜在锐射线分解为全局相机运动和局部对象运动分量。大量的实验结果表明，我们的DyBluRF在质量和数量上都优于最新的最先进的方法。我们的项目页面包括源代码和预训练模型，可在https://kaist-viclab.github.io/dyblurf-site/. et.al.|[2312.13528](http://arxiv.org/abs/2312.13528)|null|
|**2023-12-20**|**NeRF-VO: Real-Time Sparse Visual Odometry with Neural Radiance Fields**|我们介绍了一种新的单目视觉里程计（VO）系统NeRF VO，该系统集成了用于低延迟相机跟踪的基于学习的稀疏视觉里程计和用于复杂密集重建和新颖视图合成的神经辐射场景表示。我们的系统使用稀疏视觉里程计初始化相机姿态，并从单目深度预测网络中获得与视图相关的密集几何先验。我们协调姿势的尺度和密集的几何体，将它们视为训练神经隐式场景表示的监督线索。NeRF VO通过联合优化关键帧姿势的滑动窗口和底层密集几何体，在场景表示的光度和几何保真度方面表现出非凡的性能，这是通过使用体渲染训练辐射场来实现的。我们在各种合成和真实世界数据集的姿态估计精度、新颖的视图合成保真度和密集的重建质量方面超过了最先进的方法，同时实现了更高的相机跟踪频率和更少的GPU内存消耗。 et.al.|[2312.13471](http://arxiv.org/abs/2312.13471)|null|

<p align=right>(<a href=#updated-on-20231229>back to top</a>)</p>

## MLLM

|Publish Date|Title|Abstract|PDF|Code|
|---|---|-----------------------------------|---|---|
|**2023-12-28**|**Multi-Prompts Learning with Cross-Modal Alignment for Attribute-based Person Re-Identification**|细粒度的属性描述可以显著地补充人物图像中有价值的语义信息，这对人物重新识别任务的成功至关重要。然而，当前的ReID算法通常无法有效利用可用的丰富上下文信息，主要是因为它们依赖于图像属性的简单和粗略利用。人工智能生成内容的最新进展使自动生成大量细粒度的属性描述并充分利用它们成为可能。因此，本文探索了在现有（大型）模型的ReID任务中使用生成的多人属性作为提示的潜力，以获得更准确的检索结果。为此，我们提出了一个新的框架，称为多提示ReID（MP ReID），基于提示学习和语言模型，以充分挖掘精细属性来帮助ReID任务。具体来说，MP ReID首先学会产生幻觉，产生各种各样的、信息丰富的、可提示的句子来描述查询图像。该程序包括（i）一个人具有哪些属性的明确提示，以及（ii）用于调整/调节用于该人身份匹配的标准的隐含可学习提示。显式提示是通过集合生成模型（如ChatGPT和VQA模型）来获得的。此外，还设计了一个对齐模块，以逐步融合多提示（即显式提示和隐式提示），并减轻跨模态间隙。在现有的涉及属性的ReID数据集，即Market1501和DukeMTMC ReID上进行的大量实验证明了所提出的MP ReID解决方案的有效性和合理性。 et.al.|[2312.16797](http://arxiv.org/abs/2312.16797)|null|
|**2023-12-27**|**Mobility and Cost Aware Inference Accelerating Algorithm for Edge Intelligence**|边缘智能近年来得到了广泛的应用。在设备、边缘服务器和云之间拆分模型可以大大提高EI的性能。先前的工作已经深入研究了没有用户移动性的模型分割。然而，在EI的大多数使用情况下，终端设备是移动的。在这方面只进行了少数工作。这些工作仍然存在许多问题，如忽视移动设备的能耗、网络假设不当、自适应用户移动性的有效性低等。因此，为了解决以往工作中模型分割和资源分配的不足，我们提出了移动和成本感知的模型分割和资源分配算法，以加速边缘推理（MCSA）。具体地，在没有用户移动性的场景中，提供了循环交互梯度下降（Li-GD）算法。当移动用户有较大的模型推理任务需要计算时，它会考虑移动用户的能耗、通信和计算资源租用成本以及推理延迟，以找到最优的模型分割和资源分配策略。在具有用户移动性的场景中，提出了移动感知Li-GD（MLi-GD）算法来计算最优策略。然后，研究了所提出算法的性质，包括收敛性、复杂度和近似率。实验结果验证了所提算法的有效性。 et.al.|[2312.16497](http://arxiv.org/abs/2312.16497)|null|
|**2023-12-27**|**Group Multi-View Transformer for 3D Shape Analysis with Spatial Encoding**|近年来，基于视图的三维形状识别方法的结果已经饱和，并且具有优异性能的模型由于其庞大的参数大小而无法部署在内存有限的设备上。为了解决这个问题，我们为该领域引入了一种基于知识蒸馏的压缩方法，该方法在尽可能保持模型性能的同时，大大减少了参数的数量。具体来说，为了增强较小模型的功能，我们设计了一个高性能的大型模型，称为Group Multi-view Vision Transformer（GMViT）。在GMViT中，视图级ViT首先建立视图级特征之间的关系。此外，为了捕捉更深层次的特征，我们使用分组模块将视图级特征增强为组级特征。最后，组级ViT将组级特征聚合为完整的、良好形成的3D形状描述符。值得注意的是，在这两个ViT中，我们都引入了相机坐标的空间编码作为创新的位置嵌入。此外，我们提出了两个基于GMViT的压缩版本，即GMViT simple和GMViT mini。为了提高小模型的训练有效性，我们在整个GMViT过程中引入了一种知识提取方法，其中每个GMViT组件的关键输出作为提取目标。大量实验证明了该方法的有效性。大模型GMViT在基准数据集ModelNet、ShapeNetCore55和MCB上实现了出色的3D分类和检索结果。较小的模型GMViT simple和GMViT mini分别将参数大小减少了8倍和17.6倍，形状识别速度平均提高了1.5倍，同时保持了至少90%的分类和检索性能。 et.al.|[2312.16477](http://arxiv.org/abs/2312.16477)|null|
|**2023-12-25**|**Revisiting Knowledge Distillation under Distribution Shift**|知识提炼将知识从大模型转移到小模型，最近取得了显著的成就。然而，很少有研究探讨知识蒸馏对抗分布转移的机制。分布偏移是指训练和测试阶段之间的数据分布漂移。在这篇文章中，我们通过重新表述转移情况下的目标函数来重新考虑知识提炼的范式。在真实场景下，我们提出了一个统一而系统的框架，以对照两种普遍的分布变化（包括多样性和相关性变化）来衡量知识提取。评估基准涵盖了五个基准数据集的30多种算法、数据驱动和优化方法。总的来说，我们对学生模型进行了广泛的实验。我们揭示了分布变化下教学表现不佳的有趣观察结果；特别是，复杂的算法和数据扩充在许多情况下提供了有限的增益。 et.al.|[2312.16242](http://arxiv.org/abs/2312.16242)|null|
|**2023-12-26**|**Black-Box Tuning of Vision-Language Models with Effective Gradient Approximation**|参数有效微调（PEFT）方法为使大型视觉语言模型适应特定任务或场景提供了一种有效的方法。通常，他们在白盒公式中为预先训练的模型学习非常小范围的参数，该公式假设模型架构是已知的，参数是可访问的。然而，出于防止滥用或商业因素的考虑，大型模型往往不是开源的，因此对白盒PEFT方法的部署构成了障碍。为了减轻对模型可访问性的依赖，我们引入了协作黑盒调优（CBBT），用于黑盒模型的文本提示优化和输出特征自适应。具体来说，考虑到反向传播梯度被阻塞，我们通过分析具有扰动提示的预测来近似文本提示的梯度。其次，在不可访问模型的输出特性上部署了一个轻量级适配器，进一步方便了模型的自适应过程。有了这些设计，我们的CBBT在11个下游基准上进行了广泛评估，与现有的黑盒VL自适应方法相比，取得了显著的改进。代码发布于https://github.com/guozix/cbbt. et.al.|[2312.15901](http://arxiv.org/abs/2312.15901)|**[link](https://github.com/guozix/cbbt)**|
|**2023-12-26**|**High Efficiency Inference Accelerating Algorithm for NOMA-based Mobile Edge Computing**|在设备、边缘服务器和云之间拆分推理模型可以大大提高EI的性能。此外，非正交多址（NOMA）作为B5G/6G的关键支持技术，可以实现大规模连接和高频谱效率。受NOMA优点的启发，将NOMA与MEC中的模型分割相结合以减少推理延迟变得更有吸引力。然而，在以前的工作中，没有适当考虑分裂推理过程中基于NOMA的通信。因此，在本文中，我们将NOMA集成到MEC中的分裂推理中，并提出了有效的通信和计算资源分配算法来加速边缘的模型推理。具体来说，当移动用户在基于NOMA的MEC中有大量的模型推理任务需要计算时，它将考虑设备和边缘服务器的能耗以及推理延迟，以找到最佳的模型分割策略、子信道分配策略（上行链路和下行链路）和传输功率分配策略（下行链路和上行链路）。由于不能同时满足最小推理延迟和能量消耗，并且子信道分配和模型分割的变量是离散的，因此采用梯度下降算法来寻找它们之间的最优折衷。此外，还提出了循环迭代GD方法（Li-GD），以降低参数离散引起的GD算法的复杂度。此外，还研究了所提出的算法的性质，证明了所提出算法的有效性。 et.al.|[2312.15850](http://arxiv.org/abs/2312.15850)|null|
|**2023-12-25**|**IQAGPT: Image Quality Assessment with Vision-language and ChatGPT Models**|大型语言模型（LLM），如ChatGPT，在各种任务中表现出了令人印象深刻的功能，并作为跨许多领域的自然语言接口吸引了越来越多的兴趣。最近，像BLIP-2和GPT-4这样的大型视觉语言模型（VLM）被深入研究，它们从图像-文本对中学习丰富的视觉语言相关性。然而，尽管有这些发展，LLM和VLM在图像质量评估（IQA）中的应用，特别是在医学成像中的应用仍有待探索，这对于客观的性能评估和放射科医生意见的潜在补充甚至替代是有价值的。为此，本文介绍了IQAGPT，这是一种创新的图像质量评估系统，将图像质量字幕VLM与ChatGPT集成在一起，用于生成质量分数和文本报告。首先，我们构建了一个用于训练和评估的CT-IQA数据集，包括1000个具有不同质量水平的专业注释的CT切片。为了更好地利用LLM的功能，我们使用提示模板将带注释的质量分数转换为语义丰富的文本描述。其次，我们对CT-IQA数据集上的图像质量字幕VLM进行微调，以生成质量描述。字幕模型通过跨模态注意力融合了图像和文本特征。第三，基于质量描述，用户可以与ChatGPT对话，对图像质量分数进行评分或生成放射质量报告。我们的初步结果证明了用大型模型评估图像质量的可行性。值得注意的是，我们的IQAGPT优于GPT-4和CLIP-IQA，以及仅依赖图像的多任务分类和回归模型。 et.al.|[2312.15663](http://arxiv.org/abs/2312.15663)|null|
|**2023-12-24**|**Fairness-Aware Structured Pruning in Transformers**|大型语言模型（LLM）的规模不断扩大，给它们的训练和推理带来了挑战。删除模型组件被视为解决大模型大小的解决方案，然而，现有的修剪方法只关注性能，而没有考虑LLM的负责任使用的一个重要方面：模型公平性。至关重要的是，要解决LLM对不同群体的公平性问题，如妇女、黑人、LGBTQ+、犹太社区等，因为LLM正在部署并向广大受众开放。在这项工作中，首先，我们研究了在预先训练的基于transformer的语言模型中，注意力头如何影响公平性和性能。然后，我们提出了一种新的方法来修剪对公平性产生负面影响的注意力头部，同时保留对性能至关重要的头部，即语言建模能力。我们的方法在时间和资源方面是实用的，因为它不需要对最终修剪过的、更公平的模型进行微调。我们的研究结果表明，与有偏见的模型相比，两种不同大小的DistilGPT-2、GPT-2和GPT-Neo模型（GPT-J和Llama 2模型）的性别偏见分别减少了19%、19.5%、39.5%、34.7%、23%和8%，性能仅略有下降。 et.al.|[2312.15398](http://arxiv.org/abs/2312.15398)|null|
|**2023-12-23**|**ZO-AdaMU Optimizer: Adapting Perturbation by the Momentum and Uncertainty in Zeroth-order Optimization**|在大型模型的全参数训练中，降低内存需求已成为一个研究热点。MeZO在零阶SGD优化器（ZO-SGD）中仅通过前向传递对大型语言模型（LLM）进行微调，在与推理相同的GPU内存使用情况下表现出优异的性能。然而，MeZO中梯度估计的模拟扰动随机近似会导致严重的振荡，并导致大量的时间开销。此外，在没有动量正则化的情况下，MeZO表现出严重的过拟合问题。最后，ZO-SGD上的扰动无关动量并不能提高收敛速度。本研究提出ZO-AdaMU通过在其随机近似中调整具有动量的模拟扰动来解决上述问题。与现有的自适应动量方法不同，我们在随机梯度近似中在模拟扰动上重新定位动量。我们的收敛性分析和实验证明，这是一种更好的方法来提高ZO-SGD的收敛稳定性和收敛速度。大量实验表明，与MeZO及其动量变体相比，ZO-AdaMU在各种NLP任务中对LLM微调产生了更好的泛化能力。 et.al.|[2312.15184](http://arxiv.org/abs/2312.15184)|**[link](https://github.com/mathisall/zo-adamu)**|
|**2023-12-22**|**MMGPL: Multimodal Medical Data Analysis with Graph Prompt Learning**|即时学习在将多模式大型模型微调为广泛的下游任务方面表现出了令人印象深刻的效果。尽管如此，将现有的即时学习方法应用于神经系统疾病的诊断仍然存在两个问题：（i）现有的方法通常平等地对待所有贴片，尽管神经成像中只有少量贴片与疾病相关；（ii）它们忽略了大脑连接网络中固有的结构信息，这对理解和诊断神经系统疾病至关重要。为了解决这些问题，我们在诊断神经系统疾病的多模式大模型的微调过程中，通过学习图提示，引入了一种新的提示学习模型。具体来说，我们首先利用GPT-4来获得相关的疾病概念，并计算这些概念与所有补丁之间的语义相似性。其次，我们根据每个补丁与疾病相关概念之间的语义相似性来减少不相关补丁的权重。此外，我们基于这些概念在标记之间构建了一个图，并使用图卷积网络层来提取图的结构信息，用于提示预先训练的多模式大型模型用于诊断神经系统疾病。大量实验表明，与最先进的方法相比，我们的方法在神经系统疾病诊断方面取得了卓越的性能，并得到了临床医生的验证。 et.al.|[2312.14574](http://arxiv.org/abs/2312.14574)|null|

<p align=right>(<a href=#updated-on-20231229>back to top</a>)</p>

## Diffusion

|Publish Date|Title|Abstract|PDF|Code|
|---|---|-----------------------------------|---|---|
|**2023-12-28**|**Unified-IO 2: Scaling Autoregressive Multimodal Models with Vision, Language, Audio, and Action**|我们提出了Unified IO 2，这是第一个能够理解和生成图像、文本、音频和动作的自回归多模式模型。为了统一不同的模态，我们将输入和输出（图像、文本、音频、动作、边界框等）标记到共享的语义空间中，然后使用单个编码器-解码器-转换器模型对其进行处理。由于使用如此多样化的模式进行训练是具有挑战性的，我们提出了各种架构改进来稳定模型训练。我们在来自不同来源的大型多模式预训练语料库上从头开始训练我们的模型，目标是多模式混合去噪器。为了学习一套广泛的技能，例如遵循多模式指令，我们通过提示和增强在120个数据集的集合上构建和微调。通过单一的统一模型，unified IO 2在GRIT基准测试中实现了最先进的性能，并在超过35个基准测试中取得了优异的成绩，包括图像生成和理解、自然语言理解、视频和音频理解以及机器人操作。我们向研究界发布所有模型。 et.al.|[2312.17172](http://arxiv.org/abs/2312.17172)|null|
|**2023-12-27**|**Prompt Expansion for Adaptive Text-to-Image Generation**|文本到图像生成模型功能强大，但难以使用。用户制作特定的提示以获得更好的图像，尽管图像可能是重复的。本文提出了一个Prompt Expansion框架，帮助用户用更少的精力生成高质量、多样化的图像。Prompt Expansion模型将文本查询作为输入，并输出一组经过优化的扩展文本提示，以便在传递到文本到图像模型时，生成更广泛的吸引人的图像。我们进行了一项人类评估研究，该研究表明，通过Prompt Expansion生成的图像比通过基线方法生成的图像更具美感和多样性。总的来说，本文提出了一种新颖有效的方法来改善文本到图像的生成体验。 et.al.|[2312.16720](http://arxiv.org/abs/2312.16720)|null|
|**2023-12-27**|**I2V-Adapter: A General Image-to-Video Adapter for Video Diffusion Models**|在数字内容生成的快速发展领域，焦点已经从文本到图像（T2I）模型转移到更先进的视频扩散模型，尤其是文本到视频（T2V）和图像到视频（I2V）。本文解决了I2V带来的复杂挑战：将静态图像转换为动态、逼真的视频序列，同时保持原始图像的保真度。传统的方法通常包括将整个图像集成到扩散过程中，或者使用预训练的编码器进行交叉关注。然而，这些方法往往需要改变T2I模型的基本权重，从而限制了它们的可重用性。我们介绍了一种新的解决方案，即I2V适配器，旨在克服这些限制。我们的方法保留了T2I模型及其固有运动模块的结构完整性。I2V适配器通过使用轻量级适配器模块与输入图像并行处理带噪视频帧来进行操作。该模块充当桥梁，有效地将输入链接到模型的自注意机制，从而在不需要对T2I模型进行结构更改的情况下保持空间细节。此外，I2V适配器只需要传统模型的一小部分参数，并确保与现有社区驱动的T2I模型和控制工具的兼容性。我们的实验结果证明了I2V适配器能够产生高质量的视频输出。这种性能，加上其多功能性和对可训练参数的需求减少，代表着人工智能驱动的视频生成领域的重大进步，尤其是在创意应用领域。 et.al.|[2312.16693](http://arxiv.org/abs/2312.16693)|null|
|**2023-12-27**|**Participatory prompting: a user-centric research method for eliciting AI assistance opportunities in knowledge workflows**|生成型人工智能，如图像生成模型和大型语言模型，将在创意和知识工作流程中为最终用户程序员提供巨大价值。目前的研究方法很难让最终用户参与到一场现实的对话中，以平衡生成人工智能的实际现有能力与用户工作流程的开放性以及该技术应用的许多机会。在这篇正在进行的工作中，我们介绍了参与式提示，这是一种在最终用户工作流程中为生成人工智能寻找机会的方法。参与式提示方法将情境探究和研究者介导的互动与生成模型相结合，这有助于研究参与者与生成模型互动，而不必制定自己的提示策略。我们讨论了一项正在进行的研究的进展，该研究的目的是确定数据分析工作流程中生成人工智能的最终用户编程机会。 et.al.|[2312.16633](http://arxiv.org/abs/2312.16633)|null|
|**2023-12-27**|**A Non-Uniform Low-Light Image Enhancement Method with Multi-Scale Attention Transformer and Luminance Consistency Loss**|微光图像增强旨在提高在昏暗环境中采集的图像的感知能力，并为图像识别任务提供高质量的数据支持。在处理非均匀光照下拍摄的照片时，现有的方法无法自适应地提取差异化的亮度信息，容易导致曝光过度和曝光不足。从无监督学习的角度来看，我们提出了一种名为MSATr的多尺度注意力转换器，该转换器充分提取局部和全局特征以实现光平衡，从而提高视觉质量。具体来说，我们提出了一种多尺度窗口划分方案，该方案使用指数序列来调整每一层的窗口大小。在不同大小的窗口内，可以细化自关注计算，确保模型的像素级特征处理能力。对于跨窗口的特征交互，构建了全局变换器分支，以提供全面的亮度感知并缓解曝光问题。此外，我们提出了一种循环训练策略，利用加权混合生成的不同图像和亮度一致性损失来有效提高模型的泛化能力。在几个基准数据集上进行的大量实验定量和定性地证明，我们的MSATr优于最先进的微光图像增强方法，增强后的图像具有更自然的亮度和突出的细节。代码发布于https://github.com/fang001021/MSATr. et.al.|[2312.16498](http://arxiv.org/abs/2312.16498)|null|
|**2023-12-27**|**PanGu-Draw: Advancing Resource-Efficient Text-to-Image Synthesis with Time-Decoupled Training and Reusable Coop-Diffusion**|当前的大规模扩散模型代表了条件图像合成的巨大飞跃，能够解释文本、人体姿势和边缘等各种线索。然而，它们对大量计算资源和广泛数据收集的依赖仍然是一个瓶颈。另一方面，由于图像分辨率和潜在空间嵌入结构不兼容，阻碍了它们的联合使用，现有扩散模型的集成带来了挑战，每个扩散模型专门用于不同的控制，并在独特的潜在空间中运行。针对这些限制，我们提出了“PanGu Draw”，这是一种新的潜在扩散模型，旨在实现资源高效的文本到图像合成，能够熟练地适应多个控制信号。我们首先提出了一种资源高效的时间解耦训练策略，该策略将单片文本到图像模型拆分为结构生成器和纹理生成器。每个生成器都使用一种方案进行训练，该方案可以最大限度地提高数据利用率和计算效率，将数据准备减少48%，并将训练资源减少51%。其次，我们介绍了“Coop Diffusion”，这是一种算法，能够在统一的去噪过程中合作使用具有不同潜在空间和预定义分辨率的各种预先训练的扩散模型。这允许以任意分辨率进行多控制图像合成，而不需要额外的数据或重新训练。Pangu Draw的经验验证显示了其在文本到图像和多控件图像生成方面的非凡能力，为未来的模型训练效率和生成多功能性提供了一个有希望的方向。最大的5B T2I PanGu Draw模型在Ascend平台上发布。项目页面：https://pangu-draw.github.io et.al.|[2312.16486](http://arxiv.org/abs/2312.16486)|null|
|**2023-12-27**|**Bellman Optimal Step-size Straightening of Flow-Matching Models**|流匹配是在各种应用中生成高质量样本的强大框架，尤其是在图像合成中。然而，这些模型的密集计算需求，特别是在微调过程和采样过程中，对低资源场景提出了重大挑战。本文介绍了用于提取流匹配生成模型的Bellman最优步长校正（BOSS）技术：它专门针对在遵守计算预算约束的情况下进行几步有效的图像采样。首先，该技术涉及一种动态规划算法，该算法优化预训练网络的步长。然后，它对速度网络进行细化，以匹配最佳步长，旨在拉直生成路径。对图像生成任务的广泛实验评估证明了BOSS在资源利用率和图像质量方面的有效性。我们的研究结果表明，BOSS在保持有竞争力的样本质量的同时，实现了显著的效率提升，有效地弥合了低资源约束和流匹配生成模型的苛刻要求之间的差距。我们的论文还加强了人工智能的负责任开发，提供了一个更可持续的生成模型，减少了计算成本和环境足迹。我们的代码可以在https://anonymous.4open.science/r/DRL-8E88. et.al.|[2312.16414](http://arxiv.org/abs/2312.16414)|null|
|**2023-12-26**|**SSR-Encoder: Encoding Selective Subject Representation for Subject-Driven Generation**|主题驱动图像生成的最新进展导致了零样本生成，但精确选择和关注关键主题表示仍然具有挑战性。针对这一点，我们介绍了SSR编码器，这是一种新颖的架构，旨在从单个或多个参考图像中选择性地捕捉任何对象。它响应包括文本和掩码在内的各种查询模式，而无需对测试时间进行微调。SSR编码器结合了将查询输入与图像补丁对齐的令牌到补丁对齐器和用于提取和保存主题的精细特征的细节保留主题编码器，从而生成主题嵌入。这些嵌入与原始文本嵌入一起使用，为生成过程提供条件。SSR编码器具有模型通用性和效率的特点，适用于一系列自定义模型和控制模块。通过改进训练的嵌入一致性正则化损失增强，我们的大量实验证明了它在多功能和高质量图像生成中的有效性，表明它具有广泛的适用性。项目页面：https://ssr-encoder.github.io et.al.|[2312.16272](http://arxiv.org/abs/2312.16272)|null|
|**2023-12-26**|**One-dimensional Adapter to Rule Them All: Concepts, Diffusion Models and Erasing Applications**|用于文本到图像生成的商业和开源扩散模型（DM）的普遍使用促使风险缓解以防止不期望的行为。学术界现有的概念擦除方法都是基于全参数或基于规范的微调，从中我们观察到以下问题：1）向侵蚀的生成交替：目标消除过程中的参数漂移导致所有生成的交替和潜在变形，甚至不同程度地侵蚀其他概念，这一点在多概念消除后更为明显；2） 转移能力和部署效率低下：以前的特定于模型的擦除阻碍了概念的灵活组合和向其他模型的无训练转移，导致随着部署场景的增加，成本线性增长。为了实现非侵入性、精确、可定制和可转移的消除，我们将擦除框架建立在一维适配器上，以便在多功能擦除应用程序中同时从大多数DM中擦除多个概念。将概念半渗透结构作为膜（SPM）注入到任何DM中，以学习有针对性的擦除，同时通过一种新的潜在锚定微调策略有效地缓解了变化和侵蚀现象。一旦获得，SPM可以灵活组合，并为其他DM即插即用，而无需特定的重新调整，从而能够及时有效地适应不同的场景。在生成过程中，我们的促进传输机制动态调节每个SPM的渗透率，以响应不同的输入提示，进一步将对其他概念的影响降至最低。40个概念、7个DM和4个擦除应用程序的定量和定性结果证明了SPM的卓越擦除。我们的代码和预调SPM将在项目页面上提供https://lyumengyao.github.io/projects/spm. et.al.|[2312.16145](http://arxiv.org/abs/2312.16145)|null|
|**2023-12-26**|**Semantic Guidance Tuning for Text-To-Image Diffusion Models**|文本到图像（T2I）扩散模型的最新进展表明，在生成具有零样本泛化能力的高质量图像方面取得了令人印象深刻的成功。然而，当前的模型很难严格遵守提示语义，经常歪曲或忽略特定的属性。为了解决这一问题，我们提出了一种简单的、无需训练的方法，该方法在推理过程中调节扩散模型的引导方向。我们首先将提示语义分解为一组概念，并监控与每个概念相关的引导轨迹。我们的关键观察结果是，模型对提示语义的遵守程度的偏差与这些概念中的一个或多个概念的指导意见的偏差高度相关。基于这一观察结果，我们设计了一种技术，将引导方向引向模型偏离的任何概念。大量实验验证了我们的方法改进了扩散模型响应提示生成的图像的语义对齐。项目页面位于：https://korguy.github.io/ et.al.|[2312.15964](http://arxiv.org/abs/2312.15964)|null|

<p align=right>(<a href=#updated-on-20231229>back to top</a>)</p>

## avatar

|Publish Date|Title|Abstract|PDF|Code|
|---|---|-----------------------------------|---|---|
|**2023-12-23**|**Human101: Training 100+FPS Human Gaussians in 100s from 1 View**|从单视角视频中重构人体在虚拟现实领域发挥着关键作用。一种流行的应用场景需要快速重建高保真3D数字人，同时确保实时渲染和交互。现有的方法往往难以满足这两个要求。在本文中，我们介绍了Human101，这是一种新颖的框架，通过在100秒内训练3D高斯人并以100+FPS进行渲染，能够从单视图视频中生成高保真动态3D人体重建。我们的方法利用了3D高斯飞溅的优势，它提供了3D人类的明确而有效的表示。与之前基于NeRF的管道不同，Human101巧妙地应用了以人为中心的前向高斯动画方法来变形3D高斯的参数，从而提高了渲染速度（即，以令人印象深刻的60+FPS渲染1024个分辨率的图像，以100+FPS渲染512个分辨率的图片）。实验结果表明，我们的方法大大超过了当前的方法，每秒帧数激增了10倍，并提供了相当或卓越的渲染质量。代码和演示将在上发布https://github.com/longxiang-ai/Human101. et.al.|[2312.15258](http://arxiv.org/abs/2312.15258)|**[link](https://github.com/longxiang-ai/human101)**|
|**2023-12-23**|**Prompt-Propose-Verify: A Reliable Hand-Object-Interaction Data Generation Framework using Foundational Models**|扩散模型以文本提示为条件，生成具有复杂细节的逼真图像。但是，当涉及到手、牙齿等人类特征时，大多数预先训练的模型都无法生成准确的图像。我们假设，可以通过注释良好的高质量数据来克服扩散模型的这种无能。在本文中，我们专门研究了使用扩散模型改进手-物体交互图像的生成。我们收集了一个注释良好的手-物交互合成数据集，该数据集使用Prompt Propose-Verify框架进行策划，并在其上微调稳定的扩散模型。我们根据CLIPScore、ImageReward、Fedility和alignment等定性和定量指标对图像-文本数据集进行评估，并显示出比当前最先进的基准测试更好的性能。 et.al.|[2312.15247](http://arxiv.org/abs/2312.15247)|null|
|**2023-12-23**|**TransFace: Unit-Based Audio-Visual Speech Synthesizer for Talking Head Translation**|直接语音到语音翻译通过引入自监督学习中获得的离散单元来实现高质量的结果。这种方法避免了与模型级联相关的延迟和级联错误。然而，与音频语音相比，有声头翻译，即将视听语音（即有声头视频）从一种语言转换为另一种语言，仍然面临着几个挑战：（1）现有方法总是依赖于级联，通过音频和文本进行合成，导致延迟和级联错误。（2） 会说话的头翻译有一套有限的参考框架。如果生成的翻译超过了原始语音的长度，则需要通过重复帧来补充视频序列，从而导致不和谐的视频转换。在这项工作中，我们提出了一个有声头翻译模型\textbf{TransFace}，它可以直接将视听语音翻译成其他语言的视听语音。它由一个语音到单元的翻译模型和一个基于单元的视听语音合成器Unit2Lip组成，前者将音频语音转换为离散单元，后者并行地从离散单元重新合成同步的视听语音。此外，我们还引入了一个有界持续时间预测器，确保等轴测头的平移并防止重复的参考帧。实验表明，我们提出的Unit2Lip模型显著提高了同步性（原始和生成的音频语音在LSE-C上分别为1.601和0.982），并将LRS2上的推理速度提高了4.35倍。此外，TransFace在LRS3-T和100%等时翻译上的Es-En和Fr-En的BLEU得分分别为61.93和47.55。 et.al.|[2312.15197](http://arxiv.org/abs/2312.15197)|null|
|**2023-12-22**|**Deformable 3D Gaussian Splatting for Animatable Human Avatars**|神经辐射场的最新进展使得能够在动态设置中对照片真实感图像进行新颖的视图合成，这可以应用于具有人类动画的场景。然而，通常使用的隐式主干来建立准确的模型，需要许多输入视图和额外的注释，如人体遮罩、UV贴图和深度贴图。在这项工作中，我们提出了ParDy Human（参数化动态人类化身），这是一种完全明确的方法，可以从一个单一的单目序列中构建数字化身。ParDy Human在3D高斯飞溅中引入了参数驱动的动力学，其中通过人体姿势模型使3D高斯变形以使化身动画化。我们的方法由两个部分组成：第一个模块根据SMPL顶点使标准3D高斯变形，第二个模块进一步采用其设计的联合编码并预测每高斯变形，以处理SMPL顶点变形之外的动力学。然后通过光栅化器合成图像。ParDy Human构成了逼真动态人类化身的显式模型，其需要显著更少的训练视图和图像。我们的化身学习不需要额外的注释，如掩码，并且可以在可变背景下进行训练，同时即使在消费硬件上也能高效地推断出全分辨率图像。我们提供的实验证据表明，在ZJU MoCap和THUman4.0数据集上，ParDy-Human在数量和视觉上都优于最先进的方法。 et.al.|[2312.15059](http://arxiv.org/abs/2312.15059)|null|
|**2023-12-22**|**Latents2Semantics: Leveraging the Latent Space of Generative Models for Localized Style Manipulation of Face Images**|随着元宇宙慢慢成为现实，以及数字人类的快速发展，对人脸原则风格编辑管道的需求势必会增加。我们通过引入潜在2语义自动编码器（L2SAE）来满足这一需求，这是一种生成式自动编码器模型，有助于对人脸图像中几个感兴趣区域（ROI）的风格属性进行高度本地化编辑。L2SAE学习编码图像的结构和风格信息的单独潜在表示。因此，允许对所选择的ROI进行保留结构的样式编辑。编码的结构表示是具有减少的空间维度的多通道2D张量，其捕获局部和全局结构属性。样式表示是捕获全局样式属性的1D张量。在我们的框架中，我们对结构表示进行切片，以建立与不同ROI的强且不纠缠的对应关系。因此，所选ROI的样式编辑相当于（a）从切片结构表示生成的ROI掩模和（b）具有全局样式变化的解码图像的简单组合，该全局样式变化是从操纵的（使用高斯噪声）全局样式和不变的结构张量生成的。在没有额外人力监督的情况下进行风格编辑是对SOTA风格编辑管道的重大胜利，因为大多数现有作品都需要额外的人力（监督）后期培训，才能将语义归因于风格编辑。我们还取消了基于迭代优化的反演或在训练后确定可控的潜在方向，这需要额外的计算成本高昂的操作。我们在多个应用程序中为相同的应用程序提供定性和定量结果，例如使用从多个数据集采样的测试图像进行选择性风格编辑和交换。 et.al.|[2312.15037](http://arxiv.org/abs/2312.15037)|null|
|**2023-12-21**|**From Past to Future: Digital Methods Towards Artefact Analysis**|在过去的二十年里，数字人文改变了人文和社会科学的格局，实现了对广泛数据集的高级计算分析和解释。值得注意的是，东南亚，特别是新加坡最近的举措侧重于对历史数据进行分类和归档，如艺术品、文学作品，尤其是考古文物。这项研究通过在两个不同的人工制品数据集上应用统计方法，展示了数字人文的巨大潜力。具体而言，我们展示了对公元1千年中期东南亚大陆“旭日”铸币的自动模具研究结果，随后对从新加坡中部殖民前圣安德鲁大教堂遗址挖掘的13-14世纪陶器的2D图像使用了无监督统计方法。这项研究提供了一个比较评估，展示了基于统计的方法对不同考古材料的解释和分析以及数字人文整体的变革影响。 et.al.|[2312.13790](http://arxiv.org/abs/2312.13790)|null|
|**2023-12-18**|**Relightable Neural Actor with Intrinsic Decomposition and Pose Control**|在视觉和图形学中，创建一个可欣赏、可驾驶和逼真的数字人类化身是一个具有挑战性的重要问题。人类是高度立体化的，会产生依赖姿势的外观效果，如自我阴影和皱纹，皮肤和衣服需要复杂且空间变化的BRDF模型。虽然最近的人类重新照明方法可以从多视图视频中恢复看似合理的材料光分解，但它们不能推广到新颖的姿势，并且仍然存在视觉伪影。为了解决这一问题，我们提出了Relightable Neural Actor，这是第一种基于视频的方法，用于学习照片真实感的神经人体模型，该模型可以重新照明，允许外观编辑，并可以由任意骨骼姿势控制。重要的是，为了学习我们的人类化身，我们只需要在已知但静态的照明条件下对人类进行多视图记录。为了实现这一点，我们用可驱动的密度场来表示演员的几何体，该密度场对姿势相关的服装变形进行建模，并提供3D和UV空间之间的映射，其中对法线、可见性和材质进行编码。为了在现实世界场景中评估我们的方法，我们收集了一个新的数据集，其中包括在室内和室外不同光照条件下记录的四个参与者，为人类重新照明提供了第一个此类基准，并展示了最先进的新人类姿势的重新照明结果。 et.al.|[2312.11587](http://arxiv.org/abs/2312.11587)|null|
|**2023-12-18**|**VectorTalker: SVG Talking Face Generation with Progressive Vectorisation**|高保真度和高效的音频驱动谈话头生成一直是计算机图形学和计算机视觉领域的一个关键研究课题。在这项工作中，我们研究了基于矢量图像的音频驱动的谈话头生成。与现有作品中使用最广泛的光栅图像直接动画相比，矢量图像具有良好的可扩展性，可用于多种应用。基于矢量图像的会说话的头生成面临两个主要挑战：高质量的矢量图像重建（相对于源肖像图像）和生动的动画（相对于音频信号）。为了解决这些问题，我们提出了一种新的可扩展矢量图形重建和动画方法，称为VectorTalker。具体而言，对于高保真度重建，VectorTalker以从粗到细的方式分层重建矢量图像。对于生动的音频驱动的面部动画，我们建议使用面部标志作为中间运动表示，并提出一个有效的标志驱动的矢量图像变形模块。我们的方法可以在一个统一的框架内处理各种风格的肖像图像，包括日本漫画、卡通和照片真实感图像。我们进行了广泛的定量和定性评估，实验结果证明了VectorTalker在矢量图形重建和音频驱动动画方面的优势。 et.al.|[2312.11568](http://arxiv.org/abs/2312.11568)|null|
|**2023-12-18**|**AE-NeRF: Audio Enhanced Neural Radiance Field for Few Shot Talking Head Synthesis**|音频驱动的会说话的头部合成是一个很有前途的课题，在数字人、电影制作和虚拟现实等领域有着广泛的应用。与之前的研究相比，最近基于NeRF的方法在质量和保真度方面显示出优势。然而，当涉及到少镜头会说话的头部生成时，在一个身份只有几秒钟会说话的视频的实际场景中，出现了两个限制：1）它们要么没有基本模型，作为快速收敛的面部先验，要么在构建先验时忽略了音频的重要性；2） 它们大多忽略了不同面部区域与音频之间的相关性，例如，嘴与音频相关，而耳朵与音频无关。在本文中，我们提出了音频增强神经辐射场（AE NeRF）来解决上述问题，它可以用最少的镜头数据集生成新扬声器的逼真肖像。具体来说，我们在参考方案的特征融合阶段引入了音频感知聚合模块，其中权重由参考图像和目标图像之间音频的相似性决定。然后，提出了一种基于双NeRF框架的音频对齐人脸生成策略，分别对音频相关区域和音频无关区域进行建模。大量实验表明，即使在有限的训练集或训练迭代中，AE NeRF在图像保真度、音频嘴唇同步和泛化能力方面也超过了最先进的技术。 et.al.|[2312.10921](http://arxiv.org/abs/2312.10921)|null|
|**2023-12-19**|**MM-TTS: Multi-modal Prompt based Style Transfer for Expressive Text-to-Speech Synthesis**|文本到语音中的风格转换任务是指将风格信息转换为文本内容，以生成具有特定风格的相应语音的过程。然而，现有的大多数风格转移方法要么基于固定的情感标签，要么基于参考语音片段，无法实现灵活的风格转移。最近，一些方法采用文本描述来引导风格转移。在本文中，我们提出了一个更灵活的多模式和风格可控的TTS框架MM-TTS。它可以在统一的多模态提示空间中使用任何模态作为提示，包括参考语音、情感面部图像和文本描述，以控制系统中生成的语音的风格。建模这种多模态风格可控的TTS的挑战主要在于两个方面：1）将多模态信息对齐到统一的风格空间中，以允许在单个系统中输入任意模态作为风格提示，从而赋予生成提示风格相关语音的能力。为了解决这些问题，我们提出了一种对齐的多模态提示编码器，该编码器将不同的模态嵌入到统一的风格空间中，支持不同模态的风格转换。此外，我们提出了一种新的自适应风格转换方法，称为风格自适应卷积，以实现更好的风格表示。此外，我们还设计了一种基于整流流的细化器，以解决Mel频谱图过于平滑的问题，并生成高保真度的音频。由于没有公共的多模态TTS数据集，我们构建了一个名为MEAD-TTS的数据集，该数据集与表达性谈话头部领域有关。我们在MEAD-TTS数据集和域外数据集上的实验表明，基于多模态提示的MM-TTS可以获得令人满意的结果。 et.al.|[2312.10687](http://arxiv.org/abs/2312.10687)|null|

<p align=right>(<a href=#updated-on-20231229>back to top</a>)</p>

[contributors-shield]: https://img.shields.io/github/contributors/Vincentqyw/cv-arxiv-daily.svg?style=for-the-badge
[contributors-url]: https://github.com/Vincentqyw/cv-arxiv-daily/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/Vincentqyw/cv-arxiv-daily.svg?style=for-the-badge
[forks-url]: https://github.com/Vincentqyw/cv-arxiv-daily/network/members
[stars-shield]: https://img.shields.io/github/stars/Vincentqyw/cv-arxiv-daily.svg?style=for-the-badge
[stars-url]: https://github.com/Vincentqyw/cv-arxiv-daily/stargazers
[issues-shield]: https://img.shields.io/github/issues/Vincentqyw/cv-arxiv-daily.svg?style=for-the-badge
[issues-url]: https://github.com/Vincentqyw/cv-arxiv-daily/issues

