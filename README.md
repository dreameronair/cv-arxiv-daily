[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]

## Updated on 2024.02.01
> Usage instructions: [here](./docs/README.md#usage)

<details>
  <summary>Table of Contents</summary>
  <ol>
    <li><a href=#avatar>avatar</a></li>
  </ol>
</details>

## avatar

|Publish Date|Title|Abstract|PDF|Code|
|---|---|-----------------------------------|---|---|
|**2024-01-29**|**Democratizing the Creation of Animatable Facial Avatars**|在高端视觉效果管道中，（通常）使用定制的（且昂贵的）光舞台系统来扫描演员，以获取各种表情的几何形状和纹理。为了实现民主化，我们提出了一种新的管道，用于获得几何体和纹理以及足够的表达信息，以在不使用灯光舞台或任何其他高端硬件（或手动清理）的情况下构建定制的特定于个人的动画装备。一个关键的新颖想法包括扭曲真实世界的图像以与模板化身的几何形状对齐，并随后将扭曲的图像投影到模板化身的纹理中；重要的是，这使我们能够利用真实世界中的烘焙照明/纹理信息来创建替代面部特征（并弥合领域差距），以便进行几何重建。我们的方法不仅可以用于获得中性的表达几何体和去光纹理，而且还可以用于在将化身导入动画系统后改进化身（注意，这种导入往往是有损的，同时也会产生各种特征的幻觉）。由于默认的动画装备将包含与特定个体的模板表达式不正确对应的模板表达式，因此我们使用Simon Says方法来捕捉各种表达式并构建特定于个人的动画装备（像它们一样移动）。我们前面提到的翘曲/投影方法具有足够高的效率来重建对应于每个表达式的几何结构。 et.al.|[2401.16534](http://arxiv.org/abs/2401.16534)|null|
|**2024-01-27**|**AniDress: Animatable Loose-Dressed Avatar from Sparse Views Using Garment Rigging Model**|最近的社区在从稀疏的多视图视频构建照片逼真的可动画化身方面取得了重大进展。然而，当前的工作流程很难为宽松的角色呈现逼真的服装动态，因为它们主要依赖裸体模型进行人体建模，同时保留未建模的服装部分。这主要是因为宽松服装产生的变形是高度非刚性的，捕捉这种变形通常需要密集的视图作为监督。在本文中，我们介绍了AniDress，这是一种使用非常稀疏的多视图视频（在我们的设置中为4-8）生成宽松衣服中的可动画化人类化身的新方法。为了能够在这种情况下捕捉和学习宽松服装的外观，我们使用了从基于物理的模拟数据中获得的基于虚拟骨骼的服装索具模型。这样的模型使我们能够通过一组低维骨骼变换来捕捉和渲染复杂的服装动力学。从技术上讲，我们开发了一种从稀疏多视图视频中估计时间相干服装动力学的新方法。为了使用粗略估计为看不见的衣服状态建立逼真的渲染，引入了一个以身体和衣服运动为条件的姿势驱动的可变形神经辐射场，提供了对这两个部分的显式控制。在测试时，可以从看不见的情况中捕捉新的服装姿势，这些姿势来自基于物理或神经网络的模拟器，以驱动看不见服装的动力学。为了评估我们的方法，我们创建了一个多视图数据集，捕捉穿着宽松、动作各异的表演者。实验表明，我们的方法能够呈现出与身体高度偏离的自然服装动力学，并很好地推广到看不见的视图和姿势，超过了现有方法的性能。代码和数据将公开。 et.al.|[2401.15348](http://arxiv.org/abs/2401.15348)|null|
|**2024-01-10**|**A General-purpose AI Avatar in Healthcare**|机器学习和自然语言处理的最新进展导致人工智能（AI）作为医疗保健行业的一种宝贵工具得到了快速发展。使用大型语言模型（LLM）作为会话代理或聊天机器人有可能帮助医生诊断患者，检测疾病的早期症状，并为患者提供健康建议。本文重点关注聊天机器人在医疗保健中的作用，并探索使用化身使人工智能交互对患者更具吸引力。通过使用三类提示字典和提示改进机制，展示了通用AI化身应用程序的框架。建议采用两阶段方法来微调通用人工智能语言模型，并创建不同的人工智能化身，与用户讨论医疗问题。即时工程增强了聊天机器人的对话能力和个性特征，培养了与患者更人性化的互动。最终，在聊天机器人中注入个性可能会增加患者的参与度。未来的研究方向包括研究如何提高聊天机器人对上下文的理解，并通过对专业医疗数据集进行微调来确保其输出的准确性。 et.al.|[2401.12981](http://arxiv.org/abs/2401.12981)|null|
|**2024-01-30**|**PSAvatar: A Point-based Morphable Shape Model for Real-Time Head Avatar Animation with 3D Gaussian Splatting**|尽管取得了很大进展，但实现实时高保真度的头部化身动画仍然很困难，并且现有的方法必须在速度和质量之间进行权衡。基于3DMM的方法通常无法对眼镜和发型等非面部结构进行建模，而神经隐式模型则存在变形不灵活和渲染效率低下的问题。尽管3D高斯已经被证明具有很好的几何表示和辐射场重建能力，但在头部化身创建中应用3D高斯仍然是一个主要挑战，因为3D高斯很难对由姿势和表情变化引起的头部形状变化进行建模。在本文中，我们介绍了PSAvatar，这是一种新的可动画化头部化身创建框架，它利用离散几何图元创建参数可变形形状模型，并使用3D高斯进行精细细节表示和高保真渲染。参数变形形状模型是一种基于点的变形形状模型（PMSM），它使用点代替网格进行三维表示，以实现增强的表示灵活性。PMSM首先通过在表面和网格外采样将FLAME网格转换为点，以不仅能够重建表面状结构，而且能够重建复杂的几何形状，如眼镜和发型。通过以综合分析的方式将这些点与头部形状对齐，PMSM可以利用3D高斯进行精细的细节表示和外观建模，从而能够创建高保真化身。我们展示了PSAvatar可以重建各种主题的高保真头部化身，并且化身可以实时动画化（以512 $\times$512的分辨率$\ge$ 25fps）。 et.al.|[2401.12900](http://arxiv.org/abs/2401.12900)|**[link](https://github.com/pcl3dv/PSAvatar)**|
|**2024-01-20**|**UltrAvatar: A Realistic Animatable 3D Avatar Diffusion Model with Authenticity Guided Textures**|3D化身生成的最新进展已经引起了人们的极大关注。这些突破旨在制作更逼真的可动画化化身，缩小虚拟体验和现实世界体验之间的差距。大多数现有的工作都采用了分数蒸馏采样（SDS）损失，结合可微分的渲染器和文本条件，来指导扩散模型生成3D化身。然而，SDS通常生成的结果过于平滑，面部细节很少，因此与祖先采样相比缺乏多样性。另一方面，其他作品从单个图像生成3D化身，其中不想要的光照效果、透视图和较差的图像质量的挑战使得它们难以可靠地重建具有对齐的完整纹理的3D面部网格。在本文中，我们提出了一种新的3D化身生成方法，称为UltrAvatar，该方法具有增强的几何逼真度和卓越的基于物理的渲染（PBR）纹理质量，而没有不需要的照明。为此，该方法提出了一种漫射颜色提取模型和真实性引导的纹理漫射模型。前者去除了不需要的照明效果，以显示真实的漫反射颜色，从而可以在各种照明条件下渲染生成的化身。后者遵循两种基于梯度的指导，用于生成PBR纹理，以更好地与3D网格几何体对齐，呈现不同的人脸身份特征和细节。我们证明了所提出的方法的有效性和稳健性，在实验中大大优于最先进的方法。 et.al.|[2401.11078](http://arxiv.org/abs/2401.11078)|null|
|**2024-01-19**|**Fast Registration of Photorealistic Avatars for VR Facial Animation**|虚拟现实（VR）展示了社交互动的前景，这种互动比其他媒体更具沉浸感。其中的关键是能够在佩戴VR耳机的情况下准确地为自己肖像的真实感化身制作动画。尽管在离线设置中可以将特定于个人的化身高质量地注册到头戴式摄像机（HMC）图像，但通用实时模型的性能显著降低。由于相机视角倾斜和模态差异，在线注册也具有挑战性。在这项工作中，我们首先表明，化身和头戴式耳机相机图像之间的域间隙是困难的主要来源之一，其中基于转换器的架构在域一致性数据上实现了高精度，但当重新引入域间隙时会降低。基于这一发现，我们开发了一种系统设计，将问题解耦为两个部分：1）一个接受域输入的迭代细化模块，以及2）一个基于表情和头部姿势的当前估计的通用化身引导的图像到图像风格传递模块。这两个模块相互加强，因为当显示接近真实的例子时，图像风格的转移变得更容易，而更好的域间隙去除有助于配准。我们的系统可以高效地产生高质量的结果，从而无需昂贵的离线注册来生成个性化标签。我们通过在商品耳机上进行的大量实验验证了我们的方法的准确性和效率，证明了与直接回归方法和离线注册相比的显著改进。 et.al.|[2401.11002](http://arxiv.org/abs/2401.11002)|null|
|**2024-01-18**|**GPAvatar: Generalizable and Precise Head Avatar from Image(s)**|头部化身重建对于虚拟现实、在线会议、游戏和电影行业的应用至关重要，在计算机视觉界引起了极大的关注。该领域的基本目标是忠实地再现头部化身，并精确地控制表情和姿势。现有的方法分为基于2D的扭曲、基于网格和神经渲染方法，在保持多视图一致性、结合非面部信息和推广到新身份方面存在挑战。在本文中，我们提出了一个名为GPAvatar的框架，该框架可以在单个前向通道中从一个或多个图像重建3D头部化身。这项工作的关键思想是引入一个由点云驱动的动态基于点的表情场，以精确有效地捕捉表情。此外，我们在三平面规范场中使用多三平面注意力（MTA）融合模块来利用来自多个输入图像的信息。所提出的方法实现了忠实的身份重建、精确的表达控制和多视图一致性，在自由视点渲染和新颖视图合成方面显示了良好的效果。 et.al.|[2401.10215](http://arxiv.org/abs/2401.10215)|**[link](https://github.com/xg-chu/gpavatar)**|
|**2024-01-17**|**Tri $^{2}$-plane: Volumetric Avatar Reconstruction with Feature Pyramid**|近年来，在利用神经体积绘制进行面部化身重建方面取得了相当大的成就。尽管取得了显著的进步，但从单眼视频中重建复杂而动态的头部运动仍然需要捕捉和恢复细粒度的细节。在这项工作中，我们提出了一种新的方法，命名为Tri$^2$-plane，用于单目照片逼真的体积头部化身重建。与现有的依赖于单个三平面变形场进行动态面部建模的工作不同，所提出的tri$^2$-平面利用了特征金字塔和三个上下横向连接三平面的原理来改进细节。它在多个尺度上采样和渲染面部细节，从整个面部过渡到特定的局部区域，然后过渡到更精细的子区域。此外，我们在训练中加入了一种基于相机的几何感知滑动窗口方法作为增强，它提高了规范空间之外的鲁棒性，特别提高了交叉身份生成能力。实验结果表明，Tri$^2$ -平面不仅超越了现有的方法，而且通过实验在定量指标和定性评估方面都取得了卓越的性能。 et.al.|[2401.09386](http://arxiv.org/abs/2401.09386)|**[link](https://github.com/songluchuan/tri2plane)**|
|**2024-01-13**|**EVOKE: Emotion Enabled Virtual Avatar Mapping Using Optimized Knowledge Distillation**|随着虚拟环境的不断发展，对沉浸式和情感化体验的需求也在增长。为了满足这一需求，我们引入了使用优化知识提取（EVOKE）实现情感的虚拟化身映射，这是一种轻量级的情感识别框架，旨在将情感识别无缝集成到虚拟环境中的3D化身中。我们的方法利用了知识提取，包括在公开的DEAP数据集上进行多标签分类，该数据集涵盖了效价、唤醒和支配作为主要情绪类别。值得注意的是，我们的蒸馏模型，一个只有两个卷积层、参数比教师模型少18倍的CNN，取得了有竞争力的结果，其准确率为87%，同时所需的计算资源要少得多。这种性能和可部署性之间的平衡使我们的框架成为虚拟环境系统的理想选择。此外，多标签分类结果被用于将情绪映射到定制设计的3D化身上。 et.al.|[2401.06957](http://arxiv.org/abs/2401.06957)|null|
|**2024-01-10**|**Analysis and Perspectives on the ANA Avatar XPRIZE Competition**|ANA化身XPRIZE是一项为期四年的竞赛，旨在开发一种机器人“化身”系统，使人类操作员能够在远程环境中感知、交流和行动，就好像身体存在一样。比赛有一个独特的要求，即评委在人机界面上进行不到一个小时的培训后，将操作化身，并根据客观和主观评分标准对化身系统进行评判。本文从技术、评判和组织的角度对竞争进行了统一的总结和分析。我们研究了远程机器人技术的使用以及参赛团队在其化身系统中追求的创新，并将这些技术的使用与评委的任务表现和主观调查评分相关联。它还总结了团队领导、评委和组织者对比赛执行和影响的看法，为远程机器人和远程呈现的未来发展提供信息。 et.al.|[2401.05290](http://arxiv.org/abs/2401.05290)|null|
|**2024-01-09**|**A Simple Baseline for Spoken Language to Sign Language Translation with 3D Avatars**|本文的目的是开发一个将口语翻译成手语的功能系统，称为Spoken2Sign翻译。Spoken2Sign任务与传统的手语到口语（Sign2Spoken）翻译是正交和互补的。为了实现Spoken2Sign翻译，我们提出了一个简单的基线，包括三个步骤：1）使用现有的Sign2Spoken基准创建一个光泽视频词典；2） 为字典中的每个符号视频估计3D符号；3） 借助生成的gloss-3D符号字典，训练Spoken2Sign模型，该模型由Text2Gloss翻译器、符号连接器和渲染模块组成。翻译结果然后通过标志化身来显示。据我们所知，我们是第一个以3D符号的输出格式呈现Spoken2Sign任务的公司。除了Spoken2Sign翻译的能力外，我们还证明了我们的方法的两个副产品——三维关键点增强和多视图理解——可以帮助实现基于关键点的手语理解。代码和型号将在https://github.com/FangyunWei/SLRT et.al.|[2401.04730](http://arxiv.org/abs/2401.04730)|**[link](https://github.com/FangyunWei/SLRT)**|
|**2024-01-09**|**Morphable Diffusion: 3D-Consistent Diffusion for Single-image Avatar Creation**|生成扩散模型的最新进展已经实现了从单个输入图像或文本提示生成3D资产的先前不可行的能力。在这项工作中，我们的目标是提高这些模型的质量和功能，以完成创建可控、照片真实感的人类化身的任务。我们通过将3D可变形模型集成到最先进的多视角一致扩散方法中来实现这一点。我们证明了生成管道在关节式3D模型上的精确调节增强了基线模型在从单个图像合成新视图任务中的性能。更重要的是，这种集成有助于将面部表情和身体姿势控制无缝准确地结合到生成过程中。据我们所知，我们提出的框架是第一个扩散模型，能够从看不见的物体的单个图像中创建完全3D一致、可动画化和照片真实感的人类化身；大量的定量和定性评估证明了我们的方法在新视角和新表情合成任务上优于现有的最先进的化身创建模型。 et.al.|[2401.04728](http://arxiv.org/abs/2401.04728)|null|
|**2024-01-05**|**Integrating Open-World Shared Control in Immersive Avatars**|远程操作的化身机器人允许人们将他们的操作技能转移到可能难以或危险的工作环境中。目前的系统能够让操作员直接控制机器人的许多组件，使他们沉浸在远程环境中，但操作员仍然难以亲自完成任务。我们提出了一个将开放世界共享控制纳入化身机器人的框架，以结合直接控制和共享控制的好处。该框架通过最大限度地减少对操作员视图的障碍，并使用相同的界面进行直接、共享和完全自主的控制，来保持我们化身界面的流畅性。在一项人类受试者研究（N=19）中，我们发现使用该框架的操作员比不使用该框架者更快、更可靠地完成一系列任务。 et.al.|[2401.03079](http://arxiv.org/abs/2401.03079)|null|
|**2024-01-04**|**Real-and-Present: Investigating the Use of Life-Size 2D Video Avatars in HMD-Based AR Teleconferencing**|增强现实（AR）电话会议允许单独定位的用户在自己的物理环境中通过代理进行3D交互。利用体积捕获和重建的现有方法可以提供高保真度体验，但对于日常使用来说往往过于复杂和昂贵。其他解决方案针对移动设备，在AR头戴式显示器（HMD）上轻松设置电话会议。他们直接将传统的视频会议移植到AR-HMD平台上，或者使用化身来代表远程参与者。然而，它们只能支持高保真度或高水平的共存。此外，HMD有限的视场（FoV）可能会进一步影响用户的沉浸式体验。为了实现保真度和共现性之间的平衡，我们探索在AR电话会议中使用真人大小的基于2D视频的化身（简称视频化身）。具体而言，鉴于FoV对用户感知接近度的潜在影响，我们首先进行了一项试点研究，以探索视频化身在小组AR对话中以本地用户为中心的最佳位置。根据放置结果，我们实现了基于视频化身的电话会议的概念验证原型。我们对原型进行了用户评估，以验证其在平衡保真度和共存性方面的有效性。根据试点研究中的指示，我们通过一项涉及VR模拟环境中更多FoV条件的用户研究，进一步定量探讨了FoV大小对视频化身最佳位置的影响。我们回归放置模型，作为在各种现有AR HMD和未来具有更大FoV的AR HMD上计算确定此类电话会议应用中视频化身放置的参考。 et.al.|[2401.02171](http://arxiv.org/abs/2401.02171)|null|
|**2024-01-01**|**Text2Avatar: Text to 3D Human Avatar Generation with Codebook-Driven Body Controllable Attribute**|直接从文本生成3D人体模型有助于减少角色建模的成本和时间。然而，由于特征耦合和逼真的3D人体化身数据集的稀缺性，实现多属性可控和逼真的三维人体化身生成仍然具有挑战性。为了解决这些问题，我们提出了Text2Avatar，它可以基于耦合的文本提示生成逼真风格的3D化身。Text2Avatar利用离散代码簿作为中间特征，在文本和化身之间建立连接，从而实现特征的解开。此外，为了缓解逼真风格的3D人体化身数据的稀缺性，我们利用预先训练的无条件3D人体化身生成模型来获得大量的3D化身伪数据，这使得Text2Avatar能够实现逼真风格的生成。实验结果表明，我们的方法可以从耦合的文本数据中生成逼真的3D化身，这对该领域的其他现有方法具有挑战性。 et.al.|[2401.00711](http://arxiv.org/abs/2401.00711)|null|
|**2023-12-28**|**Dynamic Appearance Modeling of Clothed 3D Human Avatars using a Single Camera**|穿着衣服的人的外表不仅受姿势的驱动，还受其时间背景（即运动）的驱动。然而，现有的单目人体建模方法在很大程度上忽略了这种背景，由于运动模糊性，神经网络往往难以学习具有大动态的人的视频，即，即使对于相同的姿势，也存在许多依赖于运动背景的衣服几何配置。在本文中，我们介绍了一种使用动态运动的人的视频对穿着衣服的3D人体化身进行高质量建模的方法。主要挑战来自于缺乏几何的3D地面实况数据及其时间对应关系。我们通过引入一种新颖的组合人体建模框架来应对这一挑战，该框架利用了显式和隐式人体建模。对于显式建模，神经网络通过比较其2D渲染结果和原始图像来学习生成3D身体模型的逐点形状残差和外观特征。该显式模型允许通过编码它们的时间对应关系来从UV空间重构有区别的3D运动特征。对于隐式建模，隐式网络将外观和3D运动特征相结合，以解码具有运动相关几何形状和纹理的高保真穿着衣服的3D人类化身。实验表明，我们的方法可以以物理上合理的方式产生大的二次运动变化。 et.al.|[2312.16842](http://arxiv.org/abs/2312.16842)|null|
|**2023-12-22**|**Deformable 3D Gaussian Splatting for Animatable Human Avatars**|神经辐射场的最新进展使得能够在动态设置中对照片真实感图像进行新颖的视图合成，这可以应用于具有人类动画的场景。然而，通常使用的隐式主干来建立准确的模型，需要许多输入视图和额外的注释，如人体遮罩、UV贴图和深度贴图。在这项工作中，我们提出了ParDy Human（参数化动态人类化身），这是一种完全明确的方法，可以从一个单一的单目序列中构建数字化身。ParDy Human在3D高斯飞溅中引入了参数驱动的动力学，其中通过人体姿势模型使3D高斯变形以使化身动画化。我们的方法由两个部分组成：第一个模块根据SMPL顶点使标准3D高斯变形，第二个模块进一步采用其设计的联合编码并预测每高斯变形，以处理SMPL顶点变形之外的动力学。然后通过光栅化器合成图像。ParDy Human构成了逼真动态人类化身的显式模型，其需要显著更少的训练视图和图像。我们的化身学习不需要额外的注释，如掩码，并且可以在可变背景下进行训练，同时即使在消费硬件上也能高效地推断出全分辨率图像。我们提供的实验证据表明，在ZJU MoCap和THUman4.0数据集上，ParDy-Human在数量和视觉上都优于最先进的方法。 et.al.|[2312.15059](http://arxiv.org/abs/2312.15059)|null|
|**2023-12-22**|**MoSAR: Monocular Semi-Supervised Model for Avatar Reconstruction using Differentiable Shading**|从肖像图像重建化身在多媒体中有许多应用，但仍然是一个具有挑战性的研究问题。从一张图像中提取反射率图和几何图形是不合适的：恢复几何图形是一个一对多的映射问题，反射率和光很难解开。可以在光台的受控条件下捕获精确的几何形状和反射率，但以这种方式获取大型数据集的成本很高。此外，仅使用这种类型的数据进行训练会导致野生图像的泛化能力较差。这促使MoSAR的引入，这是一种从单目图像生成3D化身的方法。我们提出了一种半监督训练方案，通过从光阶段和野外数据集学习来提高泛化能力。这是使用一种新颖的可微分着色公式实现的。我们证明，我们的方法有效地解开了固有的人脸参数，产生了可重新点亮的化身。因此，与现有的最先进的方法相比，MoSAR估计了一组更丰富的皮肤反射率图，并生成了更逼真的化身。我们还介绍了一个新的数据集，名为FFHQ UV Intrensics，这是第一个为总共10k名受试者提供大规模内在人脸属性（漫反射、镜面反射、环境遮挡和半透明图）的公共数据集。项目网站和数据集可通过以下链接获得：https://ubisoft-laforge.github.io/character/mosar/ et.al.|[2312.13091](http://arxiv.org/abs/2312.13091)|null|
|**2023-12-20**|**Relightable and Animatable Neural Avatars from Videos**|3D数字化身的轻量级创建是一项非常理想但具有挑战性的任务。在未知照明下，只有稀疏的人的视频，我们提出了一种创建可重新照明和可动画化的神经化身的方法，该方法可用于在新的视角、身体姿势和照明下合成人类的真实感图像。这里的关键挑战是理清几何结构、衣服的材质和照明，由于身体运动引起的复杂几何结构和阴影变化，这变得更加困难。为了解决这个不适定问题，我们提出了新的技术来更好地模拟几何和阴影的变化。对于几何变化建模，我们提出了一个可逆变形场，这有助于解决反向蒙皮问题，并提高几何质量。为了对空间和时间变化的阴影线索进行建模，我们提出了一种姿态感知的部分光可见性网络来估计光遮挡。在合成和真实数据集上进行的大量实验表明，我们的方法重建了高质量的几何体，并在不同的身体姿势下生成了逼真的阴影。代码和数据位于\url{https://wenbin-lin.github.io/RelightableAvatar-page/}. et.al.|[2312.12877](http://arxiv.org/abs/2312.12877)|null|
|**2023-12-20**|**DLCA-Recon: Dynamic Loose Clothing Avatar Reconstruction from Monocular Videos**|用宽松的衣服重建一个充满活力的人是一项重要但困难的任务。为了应对这一挑战，我们提出了一种名为DLCA-Recon的方法，从单眼视频中创建人类化身。当人类自由活动和行动时，从宽松的衣服到下半身的距离在每一帧中都会迅速变化。以前的方法缺乏有效的几何初始化和约束来指导变形的优化，以解释这种急剧的变化，导致重建表面不连续和不完整。为了更准确地对变形建模，我们建议在规范空间中初始化估计的3D穿着衣服的人，因为变形场更容易从穿着衣服的人类学习，而不是从SMPL学习。通过显式网格和隐式SDF的表示，我们利用连续帧之间的物理连接信息，提出了一个动态变形场（DDF）来优化变形场。DDF考虑了宽松衣服上的作用力，以增强变形的可解释性，并有效地捕捉宽松衣服的自由运动。此外，我们将SMPL蒙皮权重传播到每个个体，并在优化过程中细化姿势和蒙皮权重，以改进蒙皮变换。基于更合理的初始化和DDF，我们可以更准确地模拟真实世界的物理。在公共数据集和我们自己的数据集上进行的大量实验验证了，与SOTA方法相比，我们的方法可以为穿着宽松衣服的人产生更好的结果。 et.al.|[2312.12096](http://arxiv.org/abs/2312.12096)|null|
|**2023-12-18**|**GAvatar: Animatable 3D Gaussian Avatars with Implicit Mesh Learning**|高斯飞溅已经成为一种强大的3D表示，它利用了显式（网格）和隐式（NeRF）3D表示的优势。在本文中，我们试图利用高斯飞溅从文本描述中生成逼真的可动画化身，解决基于网格或NeRF的表示所带来的限制（例如灵活性和效率）。然而，高斯飞溅的天真应用无法生成高质量的可动画化身，并且存在学习不稳定性；它也不能捕捉到精细的化身几何形状，并且经常导致退化的身体部位。为了解决这些问题，我们首先提出了一种基于基元的3D高斯表示，其中高斯在姿势驱动的基元内定义，以便于动画制作。其次，为了稳定和摊销数百万高斯人的学习，我们建议使用神经隐式场来预测高斯属性（例如，颜色）。最后，为了捕捉精细的化身几何图形并提取详细的网格，我们提出了一种新的基于SDF的三维高斯隐式网格学习方法，该方法对底层几何图形进行正则化，并提取高度详细的纹理网格。我们提出的方法GAvatar仅使用文本提示就可以大规模生成各种可动画化的化身。GAvatar在外观和几何质量方面显著优于现有方法，并在1K分辨率下实现了极快的渲染（100fps）。 et.al.|[2312.11461](http://arxiv.org/abs/2312.11461)|null|
|**2023-12-15**|**Attention-Based VR Facial Animation with Visual Mouth Camera Guidance for Immersive Telepresence Avatars**|虚拟现实环境中的面部动画对于需要用户面部的清晰可见性和传达情感信号的能力的应用程序至关重要。在我们的场景中，我们为控制机器人阿凡达系统的操作员的脸设置动画。当想要与特定个体而不仅仅是机器人互动时，面部动画的使用尤其有价值。纯关键点驱动的动画方法与面部运动的复杂性作斗争。我们提出了一种混合方法，既使用关键点，又使用口腔摄像头的直接视觉引导。我们的方法适用于看不见的运营商，只需要快速注册一步，即可捕获两个短视频。选择多个源图像以覆盖不同的面部表情。给定HMD的口腔摄像头帧，我们动态构建目标关键点，并应用注意力机制来确定每个源图像的重要性。为了解决关键点模糊性并使更广泛的口腔表情动画化，我们建议将视觉口腔摄像头信息注入潜在空间。我们通过模拟口腔摄像头输入的视角差异和面部变形，实现了在大规模说话头部数据集上的训练。我们的方法在质量、能力和时间一致性方面优于基线。此外，我们还重点介绍了面部动画是如何帮助我们在ANA阿凡达XPRIZE总决赛中获胜的。 et.al.|[2312.09750](http://arxiv.org/abs/2312.09750)|null|
|**2023-12-15**|**3DGS-Avatar: Animatable Avatars via Deformable 3D Gaussian Splatting**|我们介绍了一种使用3D高斯飞溅（3DGS）从单眼视频创建可动画化人类化身的方法。现有的基于神经辐射场（NeRFs）的方法实现了高质量的新视图/新姿态图像合成，但通常需要数天的训练，并且在推理时非常慢。最近，该社区探索了快速网格结构，以有效训练穿着衣服的化身。尽管训练速度极快，但这些方法几乎无法实现约15 FPS的交互式渲染帧速率。在本文中，我们使用3D高斯飞溅并学习非刚性变形网络来重建可动画化的穿着衣服的人类化身，这些化身可以在30分钟内训练并以实时帧速率（50+FPS）渲染。考虑到我们表示的显式性质，我们进一步在高斯均值向量和协方差矩阵上引入尽可能等距的正则化，增强了我们的模型在高度清晰的看不见姿态上的泛化能力。实验结果表明，与最先进的方法相比，我们的方法在从单目输入创建可动画化身方面实现了相当甚至更好的性能，同时在训练和推理方面分别快了400倍和250倍。 et.al.|[2312.09228](http://arxiv.org/abs/2312.09228)|null|
|**2023-12-26**|**SEEAvatar: Photorealistic Text-to-3D Avatar Generation with Constrained Geometry and Appearance**|在大规模文本到图像生成模型的支持下，文本到3D化身生成取得了可喜的进展。然而，由于不精确的几何形状和低质量的外观，大多数方法都无法产生逼真的结果。为了更实用的化身生成，我们提出了SEEAvatar，这是一种从文本中生成照片级真实感3D化身的方法，具有解耦几何和外观的SElf进化约束。对于几何体，我们建议使用模板化身将优化后的化身约束为适当的全局形状。模板化身是用人类先验初始化的，并且可以由优化的化身周期性地更新为演进的模板，这使得能够更灵活地生成形状。此外，在面部和手部等局部区域，几何结构也受到静态人类先验的约束，以保持精细的结构。对于外观生成，我们使用通过提示工程增强的扩散模型来引导基于物理的渲染管道生成逼真的纹理。亮度约束应用于反照率纹理，以抑制不正确的照明效果。实验表明，我们的方法在全局和局部几何以及外观质量方面都大大优于以前的方法。由于我们的方法可以生成高质量的网格和纹理，因此这些资源可以直接应用于经典图形管道中，以便在任何照明条件下进行逼真的渲染。项目页面位于：https://yoxu515.github.io/SEEAvatar/. et.al.|[2312.08889](http://arxiv.org/abs/2312.08889)|null|
|**2023-12-12**|**On the Potential of an Independent Avatar to Augment Metaverse User Socialization Time**|我们提出了一种计算建模方法，旨在捕捉如何通过在元宇宙中使用独立和自主版本的数字表示来虚拟增加元宇宙用户的可用社交时间容量的细节。我们设想了一个以元宇宙为中心的传统化身概念的扩展：当用户不直接控制化身时，化身也可以被编程为独立操作，从而将其变成基于代理的数字人类表示。这样，用户可以虚拟地委托维持现有联系人所需的化身社交时间，以便最终维持空闲的非化身介导的社交时间，该空闲的社交时间可以潜在地投资于额外的社交活动。我们使用社会科学中选定的概念对环境进行建模，并确定特征变量：自我网络、社会存在和社会线索。然后，我们将用户的非化身中介空闲时间最大化问题公式化为线性优化。最后，我们分析了问题的可行区域，并对化身介导的交互的不同参数值可以实现的空闲时间提出了一些初步见解。 et.al.|[2312.07077](http://arxiv.org/abs/2312.07077)|null|
|**2023-12-11**|**Development of the Lifelike Head Unit for a Humanoid Cybernetic Avatar `Yui' and Its Operation Interface**|在以化身为媒介的交流中，面对面对话者通过化身感知操作员的存在和情绪是至关重要的。尽管类似人类的机器人已经被开发成通过外表和动作来传达存在感，但很少有研究优先考虑使用机器人作为化身来加深操作员和对话者的沟通体验。为了解决这一差距，我们推出了“控制论化身Yui”，它具有28个自由度的人形头部单元，能够表达凝视、面部情绪和与言语相关的口腔动作。通过头戴式显示器（HMD）中的眼睛跟踪单元和Yui双眼的自由度，操作员可以自然地控制化身的凝视。此外，Yui耳朵里嵌入的麦克风可以让操作员在三维空间听到周围的声音，使他们能够仅根据听觉信息辨别通话方向。HMD的面部跟踪单元将化身的面部动作与操作员的面部动作同步。这种身临其境的界面，再加上Yui人性化的外表，实现了实时的情感传递和沟通，增强了双方的存在感。我们的实验展示了Yui的面部表情能力，并通过远程操作试验验证了该系统的功效，这表明化身技术有潜在的进步。 et.al.|[2312.06310](http://arxiv.org/abs/2312.06310)|null|
|**2023-12-08**|**360° Volumetric Portrait Avatar**|我们提出了360体积人像（3VP）化身，这是一种仅基于单眼视频输入重建人类受试者360照片逼真人像化身的新方法。最先进的单目化身重建方法依赖于稳定的面部表现捕捉。然而，基于3DMM的面部跟踪的普遍使用有其局限性；侧视图很难被捕获，而且它失败了，尤其是对于后视图，因为缺少面部标志或人类解析掩码等所需输入。这导致了只覆盖前半球的不完整的化身重建。与此相反，我们提出了一种基于模板的躯干、头部和面部表情跟踪，使我们能够从各个方面覆盖人类受试者的外观。因此，给定在单个相机前旋转的对象的序列，我们基于神经辐射场训练神经体积表示。构建这种表示的一个关键挑战是外观变化的建模，尤其是在口腔区域（即嘴唇和牙齿）。因此，我们提出了一种基于变形场的混合基础，它允许我们在不同的外观状态之间进行插值。我们根据捕获的真实世界数据评估我们的方法，并与最先进的单目重建方法进行比较。与此相反，我们的方法是第一种重建整个360度化身的单目技术。 et.al.|[2312.05311](http://arxiv.org/abs/2312.05311)|null|
|**2023-12-08**|**Disentangled Clothed Avatar Generation from Text Descriptions**|在本文中，我们介绍了一种新颖的文本到化身的生成方法，该方法分别生成人体和衣服，并允许在生成的化身上生成高质量的动画。虽然文本到化身生成的最新进展已经从文本提示中产生了不同的人类化身，但这些方法通常将所有元素——衣服、头发和身体——组合成一个单独的3D表示。这种纠缠的方法给编辑或动画等下游任务带来了挑战。为了克服这些限制，我们在SMPL模型的基础上提出了一种新的解纠缠的3D化身表示，称为序列偏移SMPL（SO-SMPL）。SO-SMPL用两个独立的网格表示人体和衣服，但将它们与偏移相关联，以确保身体和衣服之间的物理对齐。然后，我们设计了一个基于分数蒸馏采样（SDS）的蒸馏框架，从文本提示中生成所提出的SO-SMPL表示。与现有的文本到化身方法相比，我们的方法不仅实现了更高的文本和几何质量以及更好的与文本提示的语义对齐，而且显著提高了角色动画、虚拟试穿和化身编辑的视觉质量。我们的项目页面位于https://shanemankiw.github.io/SO-SMPL/. et.al.|[2312.05295](http://arxiv.org/abs/2312.05295)|null|
|**2023-12-08**|**Reality's Canvas, Language's Brush: Crafting 3D Avatars from Monocular Video**|3D化身生成的最新进展擅长于照片真实感模型的多视图监督。然而，尽管具有更广泛的适用性，但单眼对应物在质量上落后。我们建议ReCaLab缩小这一差距。ReCaLab是一个完全可微分的管道，只需从一个RGB视频中学习高保真3D人体化身。对姿势条件可变形NeRF进行了优化，以在体积上以标准T姿势表示人类受试者。然后利用规范表示来使用2D-3D对应有效地关联视点不可知的纹理。这使得能够单独生成反照率和阴影，它们共同构成RGB预测。该设计允许通过文本提示控制人体姿势、体型、纹理和照明的中间结果。图像条件扩散模型从而有助于使3D化身的外观和姿势动画化，以创建具有先前看不见的人类运动的视频序列。大量实验表明，ReCaLab在图像合成任务的图像质量方面优于以前的单目方法。ReCaLab甚至优于多视图方法，这些方法利用高达19倍的同步视频来完成新颖的姿势渲染任务。此外，自然语言为3D人类化身的创造性操作提供了直观的用户界面。 et.al.|[2312.04784](http://arxiv.org/abs/2312.04784)|null|
|**2023-12-07**|**MonoGaussianAvatar: Monocular Gaussian Point-based Head Avatar**|从单眼人像视频序列重建的照片逼真的头部化身的动画化能力代表了弥合虚拟世界和现实世界之间差距的关键一步。这项正在进行的研究利用了头部化身技术的最新进展，包括显式3D可变形网格（3DMM）、点云和神经隐式表示。然而，基于3DMM的方法受到其固定拓扑的约束，基于点的方法由于涉及大量的点而遭受沉重的训练负担，最后一种方法在变形灵活性和渲染效率方面受到限制。为了应对这些挑战，我们提出了MonoGaussianAvatar（基于单目高斯点的头部化身），这是一种利用3D高斯点表示与高斯变形场相结合的新方法，从单目人像视频中学习明确的头部化身。我们用高斯点定义我们的头部化身，高斯点的特征是形状可适应，从而实现灵活的拓扑结构。这些点表现出高斯变形场与人的目标姿势和表情对齐的运动，有助于有效变形。此外，高斯点具有可控的形状、大小、颜色和不透明度，并与高斯飞溅相结合，从而实现高效的训练和渲染。实验证明了我们的方法的优越性能，在以前的方法中取得了最先进的结果。 et.al.|[2312.04558](http://arxiv.org/abs/2312.04558)|null|

<p align=right>(<a href=#updated-on-20240201>back to top</a>)</p>

[contributors-shield]: https://img.shields.io/github/contributors/Vincentqyw/cv-arxiv-daily.svg?style=for-the-badge
[contributors-url]: https://github.com/Vincentqyw/cv-arxiv-daily/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/Vincentqyw/cv-arxiv-daily.svg?style=for-the-badge
[forks-url]: https://github.com/Vincentqyw/cv-arxiv-daily/network/members
[stars-shield]: https://img.shields.io/github/stars/Vincentqyw/cv-arxiv-daily.svg?style=for-the-badge
[stars-url]: https://github.com/Vincentqyw/cv-arxiv-daily/stargazers
[issues-shield]: https://img.shields.io/github/issues/Vincentqyw/cv-arxiv-daily.svg?style=for-the-badge
[issues-url]: https://github.com/Vincentqyw/cv-arxiv-daily/issues

