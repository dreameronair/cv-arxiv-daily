[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]

## Updated on 2024.06.08
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
|**2024-05-12**|**Listen, Disentangle, and Control: Controllable Speech-Driven Talking Head Generation**|大多数早期关于会说话的人脸生成的研究都集中在嘴唇运动和语音内容的同步上。然而，人类的头部姿势和面部情绪是自然人脸同样重要的特征。虽然音频驱动的谈话人脸生成已经取得了显著的进步，但现有的方法要么忽略了面部情绪，要么仅限于特定的个人，不能应用于任意的对象。在本文中，我们提出了一种一次性的会说话的头部生成框架（SPEAK），该框架通过实现情绪和姿势控制来区别于一般的会说话面部生成。具体来说，我们引入了互重构特征去纠缠（IRFD）方法，将人脸特征解耦到三个潜在空间中。然后，我们设计了一个人脸编辑模块，将语音内容和面部潜在代码修改到一个单一的潜在空间中。随后，我们提出了一种新的生成器，该生成器使用从编辑模块导出的修改后的潜在代码来调节面部动画合成中的情绪表达、头部姿势和语音内容。大量试验表明，我们的方法可以生成逼真的会说话的头部，嘴唇动作协调，面部情绪真实，头部动作流畅。演示视频可通过匿名链接获得：https://anonymous.4open.science/r/SPEAK-F56E et.al.|[2405.07257](http://arxiv.org/abs/2405.07257)|null|
|**2024-05-10**|**NeRFFaceSpeech: One-shot Audio-driven 3D Talking Head Synthesis via Generative Prior**|音频驱动的谈话头生成正在从2D内容向3D内容发展。值得注意的是，神经辐射场（NeRF）作为一种合成高质量3D谈话头输出的手段而备受关注。不幸的是，这种基于NeRF的方法通常需要针对每个身份的大量成对视听数据，从而限制了该方法的可扩展性。尽管已经尝试用单个图像生成音频驱动的3D会说话的头部动画，但由于图像中被遮挡区域的信息不足，结果往往不令人满意。在本文中，我们主要致力于解决在一次拍摄、音频驱动领域中被忽视的3D一致性方面，在该领域中，面部动画主要以正面视角合成。我们提出了一种新的方法，即NeRFFaceSpeech，它能够产生高质量的3D感知谈话头。利用生成模型的先验知识与NeRF相结合，我们的方法可以创建与单个图像相对应的3D一致的面部特征空间。我们的空间同步方法采用参数人脸模型的音频相关顶点动力学，通过光线变形将静态图像特征转换为动态视觉，确保逼真的三维人脸运动。此外，我们还介绍了LipaintNet，它可以补充口腔内部区域缺乏的信息，而这些信息是无法从给定的单个图像中获得的。通过在没有额外数据的情况下利用生成能力，以自监督的方式训练网络。综合实验表明，与以前的方法相比，我们的方法在从单个图像生成音频驱动的谈话头方面具有优越性，并增强了3D一致性。此外，我们首次引入了一种定量的方法来测量模型对姿态变化的鲁棒性，这只能在定性上实现。 et.al.|[2405.05749](http://arxiv.org/abs/2405.05749)|null|
|**2024-04-25**|**GaussianTalker: Real-Time High-Fidelity Talking Head Synthesis with Audio-Driven 3D Gaussian Splatting**|我们提出了GaussianTalker，这是一种用于实时生成姿态可控谈话头的新框架。它利用了3D高斯飞溅（3DGS）的快速渲染功能，同时解决了用语音音频直接控制3DGS的挑战。GaussianTalker构建了头部的标准3DGS表示，并使其与音频同步变形。一个关键的见解是将3D高斯属性编码为共享的隐式特征表示，在其中它与音频特征合并以操纵每个高斯属性。这种设计利用了空间感知特征，并加强了相邻点之间的交互。然后，将特征嵌入馈送到空间音频注意力模块，该模块预测每个高斯属性的逐帧偏移。它比以前的级联或乘法方法更稳定，可以操作大量的高斯及其复杂的参数。实验结果表明，与以前的方法相比，GaussianTalker在面部保真度、嘴唇同步精度和渲染速度方面具有优势。具体来说，GaussianTalker实现了高达120 FPS的卓越渲染速度，超过了以前的基准。我们的代码可在https://github.com/KU-CVLAB/GaussianTalker/ . et.al.|[2404.16012](http://arxiv.org/abs/2404.16012)|**[link](https://github.com/ku-cvlab/gaussiantalker)**|
|**2024-04-23**|**TalkingGaussian: Structure-Persistent 3D Talking Head Synthesis via Gaussian Splatting**|辐射场在合成逼真的3D会说话的头方面表现出了令人印象深刻的性能。然而，由于难以拟合陡峭的外观变化，通过直接修改点外观来呈现面部运动的主流范式可能会导致动态区域的失真。为了应对这一挑战，我们引入了TalkingGaussian，这是一种用于高保真谈话头合成的基于变形的辐射场框架。利用基于点的高斯飞溅，在我们的方法中，可以通过对持久的高斯基元应用平滑和连续的变形来表示面部运动，而不需要像以前的方法那样学习困难的外观变化。由于这种简化，可以合成精确的面部运动，同时保持高度完整的面部特征。在这种变形范式下，我们进一步确定了会影响详细说话动作学习的脸-嘴动作不一致。为了解决这一冲突，我们将模型分解为面部和口腔内部区域的两个分支，从而简化了学习任务，以帮助重建口腔区域更准确的运动和结构。大量实验表明，与以前的方法相比，我们的方法可以渲染高质量的唇同步谈话头部视频，具有更好的面部保真度和更高的效率。 et.al.|[2404.15264](http://arxiv.org/abs/2404.15264)|null|
|**2024-04-28**|**GaussianTalker: Speaker-specific Talking Head Synthesis via 3D Gaussian Splatting**|最近，使用神经辐射场（NeRF）进行音频驱动的谈话头合成的工作取得了令人印象深刻的结果。然而，由于NeRF隐式表示导致姿势和表情控制不足，这些方法仍然存在一些局限性，如嘴唇运动不同步或不自然，以及视觉抖动和伪影。在本文中，我们提出了GaussianTalker，这是一种基于3D高斯飞溅的音频驱动谈话头合成的新方法。利用3D高斯的显式表示特性，通过将高斯绑定到3D面部模型来实现对面部运动的直观控制。GaussianTalker由两个模块组成，扬声器专用运动转换器和动态高斯渲染器。扬声器专用运动翻译器通过通用音频特征提取和自定义嘴唇运动生成，实现特定于目标扬声器的精确嘴唇运动。动态高斯渲染器引入了特定于说话者的BlendShapes，通过潜在姿势增强面部细节表示，提供稳定逼真的渲染视频。大量的实验结果表明，GaussianTalker在说话头合成方面优于现有的最先进的方法，提供了精确的嘴唇同步和卓越的视觉质量。我们的方法在NVIDIA RTX4090 GPU上实现了130 FPS的渲染速度，大大超过了实时渲染性能的阈值，并有可能部署在其他硬件平台上。 et.al.|[2404.14037](http://arxiv.org/abs/2404.14037)|null|
|**2024-04-13**|**THQA: A Perceptual Quality Assessment Database for Talking Heads**|在媒体技术领域，由于计算机技术的快速发展，数字人已经崭露头角。然而，大多数数字人类所需的手动建模和控制对高效开发构成了重大障碍。语音驱动的方法为操纵数字人类的口型和表情提供了一种新的途径。尽管驾驶方法激增，但许多生成的会说话的头部（TH）视频的质量仍然令人担忧，影响了用户的视觉体验。为了解决这个问题，本文介绍了Talking Head Quality Assessment（THQA）数据库，该数据库通过8种不同的语音驱动方法生成了800个TH视频。大量实验证实了THQA数据库在字符和语音特征方面的丰富性。随后的主观质量评估实验分析了评分结果与语音驱动方法、年龄和性别之间的相关性。此外，实验结果表明，主流的图像和视频质量评估方法对THQA数据库有局限性，这突出了进一步研究加强TH视频质量评估的必要性。THQA数据库可在https://github.com/zyj-2000/THQA. et.al.|[2404.09003](http://arxiv.org/abs/2404.09003)|**[link](https://github.com/zyj-2000/thqa)**|
|**2024-04-07**|**GvT: A Graph-based Vision Transformer with Talking-Heads Utilizing Sparsity, Trained from Scratch on Small Datasets**|视觉转换器（ViTs）在大规模图像分类方面取得了令人印象深刻的成果。然而，当在小数据集上从头开始训练时，ViTs和卷积神经网络（CNNs）之间仍然存在显著的性能差距，这归因于缺乏归纳偏差。为了解决这个问题，我们提出了一种基于图的视觉转换器（GvT），它利用了图卷积投影和图池。在每个块中，通过基于空间邻接矩阵的图卷积投影来计算查询和密钥，而在另一个图卷积中使用点积注意力来生成值。当使用更多的注意力头时，查询和键的维度会变低，使它们的点积成为一个无信息的匹配函数。为了克服注意力头中的低秩瓶颈，我们采用了基于双线性池特征和注意力张量稀疏选择的谈话头技术。这允许过滤后的注意力分数之间的交互，并使每个注意力机制能够依赖于所有查询和键。此外，我们在两个中间块之间应用图池，以减少令牌的数量并更有效地聚合语义信息。我们的实验结果表明，GvT在没有大型数据集预训练的情况下，产生了与深度卷积网络相当或优越的结果，并超过了视觉转换器。我们提出的模型的代码可在网站上公开获取。 et.al.|[2404.04924](http://arxiv.org/abs/2404.04924)|null|
|**2024-04-02**|**EDTalk: Efficient Disentanglement for Emotional Talking Head Synthesis**|实现对多个面部动作的解开控制并适应不同的输入模式，大大增强了会说话的头部生成的应用和娱乐性。这就需要深入探索面部特征的解耦空间，确保它们a）在没有相互干扰的情况下独立操作，b）可以保留为与不同的模态输入共享，这两个方面在现有方法中经常被忽视。为了解决这一差距，本文提出了一种新的用于Talking头生成（EDTalk）的高效解纠缠框架。我们的框架能够根据视频或音频输入对口型、头部姿势和情绪表达进行个性化操作。具体来说，我们使用三个轻量级模块将面部动力学分解为三个不同的潜在空间，分别代表嘴、姿势和表情。每个空间都由一组可学习的基来表征，这些基的线性组合定义了特定的运动。为了确保独立性和加速训练，我们加强了基地之间的正交性，并设计了一种有效的训练策略，在不依赖外部知识的情况下将运动责任分配给每个空间。然后将学习到的基础存储在相应的库中，从而实现具有音频输入的共享视觉先验。此外，考虑到每个空间的性质，我们提出了一个用于音频驱动的谈话头合成的音频到运动模块。实验证明了EDTalk的有效性。我们建议观看项目网站：https://tanshuai0219.github.io/EDTalk/ et.al.|[2404.01647](http://arxiv.org/abs/2404.01647)|null|
|**2024-03-28**|**MoDiTalker: Motion-Disentangled Diffusion Model for High-Fidelity Talking Head Generation**|用于谈话头生成的传统的基于GAN的模型经常受到质量有限和训练不稳定的影响。最近基于扩散模型的方法旨在解决这些限制并提高保真度。然而，它们仍然面临挑战，包括大量的采样时间和由于扩散模型的高度随机性而难以保持时间一致性。为了克服这些挑战，我们提出了一种用于高质量谈话头生成的新的运动解纠缠扩散模型，称为MoDiTalker。我们介绍了两个模块：音频到运动（AToM）和运动到视频（MToV），前者旨在从音频中生成同步嘴唇运动，后者旨在根据生成的运动生成高质量的头部视频。AToM擅长利用音频注意力机制捕捉微妙的嘴唇动作。此外，MToV通过利用高效的三平面表示来增强时间一致性。我们在标准基准上进行的实验表明，与现有模型相比，我们的模型实现了卓越的性能。我们还提供全面的消融研究和用户研究结果。 et.al.|[2403.19144](http://arxiv.org/abs/2403.19144)|**[link](https://github.com/KU-CVLAB/MoDiTalker)**|
|**2024-03-23**|**Adaptive Super Resolution For One-Shot Talking-Head Generation**|一次拍摄会说话的头部生成学习在相同或不同身份视频的驱动下，将会说话的头视频与一个源肖像图像合成。通常，这些方法需要通过雅可比矩阵或面部图像扭曲进行基于平面的像素变换，以生成新的姿态。使用单个图像源和像素位移的约束常常损害合成图像的清晰度。一些方法试图通过引入额外的超分辨率模块来提高合成视频的质量，但这无疑会增加计算消耗并破坏原始数据分布。在这项工作中，我们提出了一种自适应的高质量会说话的头部视频生成方法，该方法在没有额外预训练模块的情况下合成高分辨率视频。具体来说，受现有超分辨率方法的启发，我们对单镜头源图像进行下采样，然后通过编码器-解码器模块自适应地重建高频细节，从而提高视频清晰度。我们的方法通过一种简单有效的策略，通过定量和定性评估不断提高生成视频的质量。代码和演示视频可在以下网址获得：\url{https://github.com/Songluchuan/AdaSR-TalkingHead/}. et.al.|[2403.15944](http://arxiv.org/abs/2403.15944)|**[link](https://github.com/songluchuan/adasr-talkinghead)**|
|**2024-03-19**|**EmoVOCA: Speech-Driven Emotional 3D Talking Heads**|近年来，3D会说话的头部生成领域取得了重大进展。该领域的一个显著挑战是将语音相关运动与表情动力学相结合，这主要是由于缺乏将口语句子的多样性与各种面部表情相结合的综合3D数据集。尽管文献工作试图利用2D视频数据和参数化3D模型作为一种变通方法，但当联合建模这两个运动时，这些仍然显示出局限性。在这项工作中，我们从不同的角度解决了这个问题，并提出了一种创新的数据驱动技术，我们用于创建一个名为EmoVOCA的合成数据集，该数据集是通过将一组无法表达的3D说话头和一组3D表达序列相结合而获得的。为了证明这种方法的优势和数据集的质量，我们设计并训练了一个情绪化的3D会说话的头部生成器，该生成器接受3D人脸、音频文件、情绪标签和强度值作为输入，并学习将音频同步的嘴唇运动与人脸的表达特征相结合。与文献中表现最好的方法相比，使用我们的数据和生成器进行的定量和定性的综合实验证明了其在合成令人信服的动画方面的卓越能力。我们的代码和预先训练的模型将可用。 et.al.|[2403.12886](http://arxiv.org/abs/2403.12886)|null|
|**2024-03-19**|**ScanTalk: 3D Talking Heads from Unregistered Scans**|语音驱动的3D会说话的头生成已经成为研究人员感兴趣的一个重要领域，这带来了许多挑战。现有方法通过使用固定拓扑设置面的动画来约束，其中建立逐点对应关系，并且点的数量和顺序在模型可以设置动画的所有身份中保持一致。在这项工作中，我们介绍了ScanTalk，这是一种新颖的框架，能够在包括扫描数据在内的任意拓扑中为3D人脸设置动画。我们的方法依赖于DiffusionNet架构来克服固定的拓扑约束，为更灵活、更逼真的3D动画提供了有希望的途径。通过利用DiffusionNet的强大功能，ScanTalk不仅能够适应不同的面部结构，而且在处理扫描数据时保持保真度，从而增强生成的3D谈话头的真实性和多功能性。通过与最先进的方法进行全面比较，我们验证了我们的方法的有效性，证明了其产生与现有技术相当的逼真谈话头脑的能力。虽然我们的主要目标是开发一种不受拓扑约束的通用方法，但所有最先进的方法都受到这些限制的约束。用于复制我们的结果的代码和预训练的模型将可用。 et.al.|[2403.10942](http://arxiv.org/abs/2403.10942)|null|
|**2024-03-11**|**A Comparative Study of Perceptual Quality Metrics for Audio-driven Talking Head Videos**|人工智能生成内容（AIGC）技术的快速发展推动了音频驱动的谈话头生成，在实际应用中获得了相当大的研究关注。然而，绩效评估研究滞后于会说话的头部生成技术的发展。现有文献依赖于启发式定量指标，而没有人为验证，阻碍了准确的进度评估。为了解决这一差距，我们收集了由四种生成方法生成的会说话的头部视频，并对视觉质量、嘴唇音频同步和头部运动的自然度进行了受控的心理物理实验。我们的实验验证了模型预测和人类注释之间的一致性，确定了比广泛使用的指标更符合人类意见的指标。我们相信，我们的工作将促进绩效评估和模型开发，在更广泛的背景下深入了解AIGC。代码和数据将在https://github.com/zwx8981/ADTH-QA. et.al.|[2403.06421](http://arxiv.org/abs/2403.06421)|**[link](https://github.com/zwx8981/adth-qa)**|
|**2024-03-12**|**Style2Talker: High-Resolution Talking Head Generation with Emotion Style and Art Style**|尽管最近对音频驱动的说话头进行自动动画制作越来越感兴趣，但之前的工作主要集中在实现与音频的嘴唇同步，忽略了生成富有表现力的视频的两个关键元素：情感风格和艺术风格。在本文中，我们提出了一种创新的音频驱动的谈话人脸生成方法，称为Style2Taker。它涉及两个风格化阶段，即风格E和风格A，将文本控制的情感风格和图片控制的艺术风格融入最终输出中。为了准备与视频相对应的稀缺情感文本描述，我们提出了一种无需人工的范式，该范式使用大规模的预训练模型来自动注释现有视听数据集的情感文本标签。结合合成的情感文本，Style-E阶段利用大规模的CLIP模型来提取情感表示，这些情感表示与音频相结合，作为设计用于产生3DMM模型的情感运动系数的有效潜在扩散模型的条件。进入Style-A阶段，我们开发了一个系数驱动的运动生成器和嵌入到著名StyleGAN中的特定艺术风格路径。这使我们能够使用生成的情感运动系数和艺术风格的源图片来合成高分辨率艺术风格化的谈话头部视频。此外，为了更好地保留图像细节并避免伪影，我们向StyleGAN提供了从身份图像中提取的多尺度内容特征，并分别通过设计的内容编码器和细化网络细化其中间特征图。大量的实验结果表明，我们的方法在音频嘴唇同步以及情感风格和艺术风格的表现方面优于现有的最先进的方法。 et.al.|[2403.06365](http://arxiv.org/abs/2403.06365)|null|
|**2024-02-27**|**Learning Dynamic Tetrahedra for High-Quality Talking Head Synthesis**|最近在隐式表示方面的工作，如神经辐射场（NeRF），已经推动了从视频序列中生成逼真和可动画化的头部化身。这些隐式方法仍然面临视觉伪影和抖动，因为缺乏明确的几何约束对精确建模复杂的面部变形构成了根本挑战。在本文中，我们介绍了动态四面体（DynTet），这是一种新的混合表示，通过神经网络对显式动态网格进行编码，以确保各种运动和视点的几何一致性。DynTet通过基于坐标的网络进行参数化，该网络学习符号距离、变形和材料纹理，将训练数据锚定到预定义的四面体网格中。利用Marching四面体，DynTet有效地解码具有一致拓扑的纹理网格，通过可微光栅化器实现快速渲染，并通过像素丢失进行监督。为了提高训练效率，我们结合了经典的3D变形模型来促进几何学习，并定义了一个规范空间来简化纹理学习。由于DynTet中采用了有效的几何表示，这些优点很容易实现。与之前的工作相比，DynTet在保真度、唇同步和实时性能方面根据各种指标进行了显著改进。除了生成稳定且具有视觉吸引力的合成视频外，我们的方法还输出动态网格，这有望实现许多新兴应用。 et.al.|[2402.17364](http://arxiv.org/abs/2402.17364)|**[link](https://github.com/zhangzc21/dyntet)**|
|**2024-01-11**|**Jump Cut Smoothing for Talking Heads**|跳跃式剪裁给观看体验带来了一种突然的、有时是不必要的变化。我们提出了一个新颖的框架来平滑这些跳跃剪辑，在谈话头部视频的背景下。我们利用视频中其他源帧中受试者的外观，将其与由DensePose关键点和面部标志驱动的中级表示融合。为了实现运动，我们在切割周围的结束帧之间插入关键点和地标。然后，我们使用来自关键点和源帧的图像翻译网络来合成像素。由于关键点可能包含错误，我们提出了一种跨模态注意力方案，以在每个关键点的多个选项中选择最合适的来源。通过利用这种中级表示，我们的方法可以获得比强大的视频插值基线更强的结果。我们在会说话的头部视频中演示了我们的方法，如剪切填充词、停顿，甚至随机剪切。我们的实验表明，即使在有挑战性的情况下，我们也可以实现无缝转换，其中会说话的头部在跳跃切割中旋转或剧烈移动。 et.al.|[2401.04718](http://arxiv.org/abs/2401.04718)|null|
|**2023-12-23**|**TransFace: Unit-Based Audio-Visual Speech Synthesizer for Talking Head Translation**|直接语音到语音翻译通过引入自监督学习中获得的离散单元来实现高质量的结果。这种方法避免了与模型级联相关的延迟和级联错误。然而，与音频语音相比，有声头翻译，即将视听语音（即有声头视频）从一种语言转换为另一种语言，仍然面临着几个挑战：（1）现有方法总是依赖于级联，通过音频和文本进行合成，导致延迟和级联错误。（2） 会说话的头翻译有一套有限的参考框架。如果生成的翻译超过了原始语音的长度，则需要通过重复帧来补充视频序列，从而导致不和谐的视频转换。在这项工作中，我们提出了一个有声头翻译模型\textbf{TransFace}，它可以直接将视听语音翻译成其他语言的视听语音。它由一个语音到单元的翻译模型和一个基于单元的视听语音合成器Unit2Lip组成，前者将音频语音转换为离散单元，后者并行地从离散单元重新合成同步的视听语音。此外，我们还引入了一个有界持续时间预测器，确保等轴测头的平移并防止重复的参考帧。实验表明，我们提出的Unit2Lip模型显著提高了同步性（原始和生成的音频语音在LSE-C上分别为1.601和0.982），并将LRS2上的推理速度提高了4.35倍。此外，TransFace在LRS3-T和100%等时翻译上的Es-En和Fr-En的BLEU得分分别为61.93和47.55。 et.al.|[2312.15197](http://arxiv.org/abs/2312.15197)|null|
|**2023-12-18**|**AE-NeRF: Audio Enhanced Neural Radiance Field for Few Shot Talking Head Synthesis**|音频驱动的会说话的头部合成是一个很有前途的课题，在数字人、电影制作和虚拟现实等领域有着广泛的应用。与之前的研究相比，最近基于NeRF的方法在质量和保真度方面显示出优势。然而，当涉及到少镜头会说话的头部生成时，在一个身份只有几秒钟会说话的视频的实际场景中，出现了两个限制：1）它们要么没有基本模型，作为快速收敛的面部先验，要么在构建先验时忽略了音频的重要性；2） 它们大多忽略了不同面部区域与音频之间的相关性，例如，嘴与音频相关，而耳朵与音频无关。在本文中，我们提出了音频增强神经辐射场（AE NeRF）来解决上述问题，它可以用最少的镜头数据集生成新扬声器的逼真肖像。具体来说，我们在参考方案的特征融合阶段引入了音频感知聚合模块，其中权重由参考图像和目标图像之间音频的相似性决定。然后，提出了一种基于双NeRF框架的音频对齐人脸生成策略，分别对音频相关和音频无关区域进行建模。大量实验表明，即使在有限的训练集或训练迭代中，AE NeRF在图像保真度、音频嘴唇同步和泛化能力方面也超过了最先进的技术。 et.al.|[2312.10921](http://arxiv.org/abs/2312.10921)|null|
|**2023-12-15**|**DreamTalk: When Expressive Talking Head Generation Meets Diffusion Probabilistic Models**|扩散模型在各种下游生成任务中取得了显著的成功，但在重要且具有挑战性的表达型会说话的头部生成中仍有待探索。在这项工作中，我们提出了一个DreamTalk框架来填补这一空白，该框架采用了细致的设计来释放扩散模型在生成富有表现力的谈话头方面的潜力。具体来说，DreamTalk由三个关键组成部分组成：去噪网络、风格感知嘴唇专家和风格预测器。基于扩散的去噪网络能够在不同的表情中一致地合成高质量的音频驱动的面部运动。为了提高嘴唇动作的表现力和准确性，我们引入了一位风格敏感的嘴唇专家，他可以在注意说话风格的同时指导嘴唇同步。为了消除对表达参考视频或文本的需要，利用额外的基于扩散的风格预测器来直接从音频预测目标表达。通过这种方式，DreamTalk可以利用强大的扩散模型有效地生成富有表情的人脸，并减少对昂贵风格参考的依赖。实验结果表明，DreamTalk能够生成具有不同说话风格的照片逼真的说话脸，并实现准确的嘴唇运动，超过了现有的最先进的同类产品。 et.al.|[2312.09767](http://arxiv.org/abs/2312.09767)|null|
|**2023-12-11**|**DiT-Head: High-Resolution Talking Head Synthesis using Diffusion Transformers**|我们提出了一种新的谈话头部合成管道，称为“DiT头部”，它基于扩散变换器，并使用音频作为条件来驱动扩散模型的去噪过程。我们的方法是可扩展的，可以推广到多个身份，同时产生高质量的结果。我们训练和评估我们提出的方法，并将其与现有的谈话头部合成方法进行比较。我们证明，我们的模型在视觉质量和唇同步精度方面可以与这些方法竞争。我们的研究结果突出了我们提出的方法在广泛应用中的潜力，包括虚拟助理、娱乐和教育。有关结果的视频演示和我们的用户研究，请参阅我们的补充材料。 et.al.|[2312.06400](http://arxiv.org/abs/2312.06400)|null|
|**2023-12-09**|**R2-Talker: Realistic Real-Time Talking Head Synthesis with Hash Grid Landmarks Encoding and Progressive Multilayer Conditioning**|动态NeRF最近在3D说话肖像合成方面引起了越来越多的关注。尽管在渲染速度和视觉质量方面取得了进步，但在提高效率和有效性方面仍然存在挑战。我们提出了R2 Talker，这是一个高效有效的框架，能够实现逼真的实时谈话头部合成。具体来说，使用多分辨率哈希网格，我们介绍了一种将面部地标编码为条件特征的新方法。该方法通过将任意地标映射到统一的特征空间，将地标结构无损地编码为条件特征、解耦输入分集和条件空间。我们进一步提出了一种在NeRF渲染管道中进行渐进多层条件处理的方案，用于有效的条件特征融合。与现有技术相比，我们的新方法具有以下优势：1）无损输入编码能够获得更精确的特征，产生卓越的视觉质量。输入和条件空间的解耦提高了可推广性。2） 条件特征和MLP输出在每个MLP层的融合增强了条件影响，从而实现更准确的嘴唇合成和更好的视觉质量。3） 它紧凑地构造了条件特征的融合，显著提高了计算效率。 et.al.|[2312.05572](http://arxiv.org/abs/2312.05572)|null|
|**2023-12-07**|**VividTalk: One-Shot Audio-Driven Talking Head Generation Based on 3D Hybrid Prior**|近年来，音频驱动的会说话的头部生成引起了人们的广泛关注，并在嘴唇同步、富有表情的面部表情、自然的头部姿势生成和高视频质量方面做出了许多努力。然而，由于音频和运动之间的一对多映射，尚未有任何模型在所有这些指标上领先或捆绑。在本文中，我们提出了VividTalk，这是一个两阶段的通用框架，支持生成具有所有上述属性的高视觉质量的头部谈话视频。具体来说，在第一阶段，我们通过学习两个运动将音频映射到网格，包括非刚性表情运动和刚性头部运动。对于表达式运动，采用混合形状和顶点作为中间表示，以最大限度地提高模型的表示能力。针对自然头部运动，提出了一种新的具有两阶段训练机制的可学习头部姿态码本。在第二阶段，我们提出了一个双分支运动vae和一个生成器来将网格转换为密集运动，并逐帧合成高质量的视频。大量实验表明，所提出的VividTalk可以生成具有唇同步和逼真度的高视觉质量的谈话头部视频，并在客观和主观比较方面优于以往最先进的作品。 et.al.|[2312.01841](http://arxiv.org/abs/2312.01841)|null|
|**2024-04-28**|**SyncTalk: The Devil is in the Synchronization for Talking Head Synthesis**|在逼真的、语音驱动的谈话头部视频的合成中实现高度同步是一个重大挑战。传统的生成对抗性网络（GAN）难以保持一致的面部身份，而神经辐射场（NeRF）方法虽然可以解决这个问题，但往往会产生不匹配的嘴唇动作、不恰当的面部表情和不稳定的头部姿势。一个栩栩如生的会说话的头需要主体身份、嘴唇动作、面部表情和头部姿势的同步协调。缺乏这些同步是一个根本缺陷，导致了不切实际和人为的结果。为了解决同步这一关键问题，我们引入了SyncTalk，它被认为是创建逼真谈话头的“魔鬼”。这种基于NeRF的方法有效地保持了主体身份，增强了说话头部合成的同步性和真实性。SyncTalk采用面部同步控制器将嘴唇运动与语音对齐，并创新性地使用3D面部混合形状模型来捕捉准确的面部表情。我们的头部同步稳定器可优化头部姿势，实现更自然的头部运动。肖像同步生成器恢复头发细节，并将生成的头部与躯干融合，以获得无缝的视觉体验。大量的实验和用户研究表明，SyncTalk在同步和逼真度方面优于最先进的方法。我们建议观看补充视频：https://ziqiaopeng.github.io/synctalk et.al.|[2311.17590](http://arxiv.org/abs/2311.17590)|**[link](https://github.com/ZiqiaoPeng/SyncTalk)**|
|**2023-11-30**|**Talking Head(?) Anime from a Single Image 4: Improved Model and Its Distillation**|我们研究了创建一个可以从动画角色的单个图像实时控制的角色模型的问题。这个问题的解决方案将大大降低创建化身、计算机游戏和其他交互式应用程序的成本。Talking Head Anime 3（THA3）是一个开源项目，试图直接解决这个问题。它采用（1）动画角色上身的图像和（2）45维姿势矢量作为输入，并输出采用指定姿势的同一角色的新图像。可能的动作范围对于个人化身和某些类型的游戏角色来说足够有表现力。然而，该系统太慢，无法在普通PC上实时生成动画，并且其图像质量可以提高。在本文中，我们从两个方面改进THA3。首先，我们提出了新的组成网络架构，该架构基于U-Nets旋转角色的头部和身体，并在现代生成模型中广泛使用。新的架构始终产生比THA3基线更好的图像质量。尽管如此，它们也会使整个系统慢得多：生成一帧需要150毫秒。其次，我们提出了一种技术，将系统提取到一个小型网络（小于2MB）中，该网络可以使用消费者游戏GPU实时生成512x512个动画帧（低于30FPS），同时保持接近整个系统的图像质量。这一改进使整个系统在实时应用中具有实用性。 et.al.|[2311.17409](http://arxiv.org/abs/2311.17409)|null|
|**2023-11-28**|**THInImg: Cross-modal Steganography for Presenting Talking Heads in Images**|跨模态隐写术是在公开可用的覆盖信号（不同于秘密信号的模态）中不引人注目地隐藏秘密信号的实践。虽然以前的方法主要集中在隐藏相对少量的信息，但我们提出了THInImg，它通过利用人脸的特性，成功地将冗长的音频数据隐藏在身份图像中（并随后解码会说话的头部视频），可以有效地用于秘密通信、传输和版权保护。THInImg由两部分组成：编码器和解码器。在编码器-解码器流水线内部，我们引入了一种新的架构，该架构大大提高了在图像中隐藏音频的能力。此外，我们的框架可以扩展到迭代地将多个音频片段隐藏到身份图像中，从而提供对权限的多级控制。我们进行了广泛的实验来证明我们的方法的有效性，证明THInImg可以在160x160分辨率的身份图像中呈现长达80秒的高质量谈话头部视频（包括音频）。 et.al.|[2311.17177](http://arxiv.org/abs/2311.17177)|null|
|**2023-11-05**|**3D-Aware Talking-Head Video Motion Transfer**|会说话的头部视频的运动转移涉及生成具有主题视频的外观和驾驶视频的运动模式的新视频。当前的方法主要依赖于有限数量的主题图像和2D表示，从而忽略了充分利用主题视频中固有的多视图外观特征。在本文中，我们提出了一种新的3D感知会说话的头部视频运动传输网络Head3D，该网络通过递归网络从2D主题帧中生成可视觉解释的3D规范头部，从而充分利用主题外观信息。该方法的一个关键组成部分是自监督的3D头部几何学习模块，用于从2D主题视频帧中预测头部姿态和深度图。该模块便于在规范空间中估计3D头部，然后可以对其进行变换以与驱动视频帧对准。此外，我们使用基于注意力的融合网络将主题帧的背景和其他细节与3D主题头部相结合，以产生合成目标视频。我们在两个公开演讲的头部视频数据集上进行的广泛实验表明，Head3D在实际的交叉身份设置中优于2D和3D现有技术，有证据表明它可以很容易地适应姿势可控的新型视图合成任务。 et.al.|[2311.02549](http://arxiv.org/abs/2311.02549)|null|
|**2023-11-02**|**LaughTalk: Expressive 3D Talking Head Generation with Laughter**|笑是一种独特的表达方式，对人类积极的社会互动至关重要。尽管目前的3D会说话的头部生成方法产生了令人信服的语言表达，但它们往往无法捕捉到笑声和微笑的活力和微妙之处，尽管它们在社会环境中很重要。在本文中，我们介绍了一项新任务，即生成既能清晰表达语音又能真实大笑的3D会说话的头。我们新策划的数据集包括2D大笑视频，以及伪注释和人工验证的3D FLAME参数和顶点。给定我们提出的数据集，我们提出了一个具有两阶段训练方案的强基线：模型首先学习说话，然后获得表达笑声的能力。大量实验表明，与现有方法相比，我们的方法在说话头部生成和表达笑声信号方面都表现良好。在我们提出的装配逼真化身的方法的基础上，我们进一步探索了潜在的应用。 et.al.|[2311.00994](http://arxiv.org/abs/2311.00994)|null|
|**2023-10-08**|**GestSync: Determining who is speaking without a talking head**|在本文中，我们介绍了一种新的同步任务，手势同步：确定一个人的手势是否与他们的语音相关。与嘴唇同步相比，手势同步更具挑战性，因为声音和身体运动之间的关系远比声音和嘴唇运动之间的松散。我们为这项任务引入了一个双编码器模型，并比较了许多输入表示，包括RGB帧、关键点图像和关键点矢量，评估了它们的性能和优势。我们证明了该模型可以单独使用自监督学习进行训练，并在LRS3数据集上评估其性能。最后，我们展示了手势同步在视听同步中的应用，以及在不看脸的情况下确定谁是人群中的演讲者。代码、数据集和预训练模型可在以下位置找到：\url{https://www.robots.ox.ac.uk/~vgg/research/gestsync}。 et.al.|[2310.05304](http://arxiv.org/abs/2310.05304)|**[link](https://github.com/Sindhu-Hegde/gestsync)**|
|**2023-09-28**|**OSM-Net: One-to-Many One-shot Talking Head Generation with Spontaneous Head Motions**|一次性会说话的头部生成没有明确的头部运动参考，因此很难生成具有头部运动的会说话的头。现有的一些作品只对嘴部区域进行编辑，生成静止的会说话的头，导致会说话的头部表现不真实。其他作品在音频信号和头部运动序列之间构建了一对一的映射，将模糊对应引入到映射中，因为当人们说出相同的内容时，头部运动中的行为可能不同。这种不合理的映射形式无法对多样性进行建模，并产生几乎静态甚至夸张的头部运动，这是不自然和奇怪的。因此，一次性会说话的头部生成任务实际上是一个一对多的不适定问题，人们在说话时会出现不同的头部运动。基于上述观察，我们提出了OSM-Net，这是一个具有自然头部运动的一对多的一次性谈话头部生成网络。OSM-Net构建了一个包含丰富多样的剪辑级头部运动特征的运动空间。空间的每个基础都代表了剪辑中有意义的头部运动的特征，而不仅仅是一帧，从而在说话的头部中提供了更连贯、更自然的运动变化。将驾驶音频映射到运动空间中，可以在合理的范围内对运动空间周围的各种运动特征进行采样，以实现一对多映射。此外，地标约束和时间窗口特征输入提高了表情特征提取和视频生成的准确性。大量实验表明，与其他方法相比，OSM-Net在合理的一对多映射范式下生成了更自然、逼真的头部运动。 et.al.|[2309.16148](http://arxiv.org/abs/2309.16148)|null|
|**2023-10-12**|**Efficient Emotional Adaptation for Audio-Driven Talking-Head Generation**|音频驱动的会说话的头部合成是虚拟人相关应用的热门研究课题。然而，现有方法的灵活性和低效性是显著的局限性，需要昂贵的端到端训练来将情绪从指导视频转移到会说话的头部预测。在这项工作中，我们提出了音频驱动的谈话头部的情绪自适应（EAT）方法，该方法通过参数有效自适应，以经济高效的方式将情绪不可知的谈话头部模型转换为情绪可控的模型。我们的方法利用了一个预先训练的与情绪无关的谈话头部转换器，并从不同的角度引入了三种轻量级的适应（深度情绪提示、情绪变形网络和情绪适应模块），以实现精确而现实的情绪控制。我们的实验表明，我们的方法在广泛使用的基准测试上实现了最先进的性能，包括LRW和MEAD。此外，即使在情感训练视频稀少或不存在的情况下，我们的参数有效自适应也表现出显著的泛化能力。项目网站：https://yuangan.github.io/eat/ et.al.|[2309.04946](http://arxiv.org/abs/2309.04946)|**[link](https://github.com/yuangan/eat_code)**|

<p align=right>(<a href=#updated-on-20240608>back to top</a>)</p>

[contributors-shield]: https://img.shields.io/github/contributors/Vincentqyw/cv-arxiv-daily.svg?style=for-the-badge
[contributors-url]: https://github.com/Vincentqyw/cv-arxiv-daily/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/Vincentqyw/cv-arxiv-daily.svg?style=for-the-badge
[forks-url]: https://github.com/Vincentqyw/cv-arxiv-daily/network/members
[stars-shield]: https://img.shields.io/github/stars/Vincentqyw/cv-arxiv-daily.svg?style=for-the-badge
[stars-url]: https://github.com/Vincentqyw/cv-arxiv-daily/stargazers
[issues-shield]: https://img.shields.io/github/issues/Vincentqyw/cv-arxiv-daily.svg?style=for-the-badge
[issues-url]: https://github.com/Vincentqyw/cv-arxiv-daily/issues

