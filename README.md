[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]

## Updated on 2024.07.16
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
|**2024-07-13**|**Learning Online Scale Transformation for Talking Head Video Generation**|单镜头说话头视频生成使用源图像和驾驶视频来创建合成视频，其中源人物的面部动作模仿驾驶视频的面部动作。然而，源图像和驱动图像之间的比例差异仍然是面部重现的一个挑战。现有的方法试图在驾驶视频中定位与源图像最对齐的帧，但不精确的对齐可能会导致次优结果。为此，我们引入了一个比例变换模块，该模块可以通过使用源图像和驱动帧的检测关键点中保持的比例差信息，自动调整驱动图像的比例以适应源图像的比例。此外，为了在生成过程中不断感知人脸的尺度信息，我们将从尺度变换模块学习到的尺度信息整合到生成过程的每一层中，以产生具有精确尺度的最终结果。我们的方法可以在没有任何锚帧的情况下在两幅图像之间进行精确的运动传递，这是通过所提出的在线尺度变换面部重现网络的贡献来实现的。大量实验表明，我们提出的方法根据源面部自动调整驱动面部的尺度，并在跨身份面部重现中生成具有精确尺度的高质量面部。 et.al.|[2407.09965](http://arxiv.org/abs/2407.09965)|null|
|**2024-07-08**|**Audio-driven High-resolution Seamless Talking Head Video Editing via StyleGAN**|现有的音频驱动说话头视频编辑方法存在视觉效果差的局限性。本文试图通过基于两个模块无缝编辑不同情绪的说话人脸图像来解决这个问题：（1）音频到地标模块，由交叉重建的情绪解耦和对齐网络模块组成。它通过从语音中预测相应的情感标志来弥合语音和面部动作之间的差距；（2） 基于地标的编辑模块通过StyleGAN编辑面部视频。它的目的是从输入音频中生成由情感和内容组成的无缝编辑视频。大量实验证实，与最先进的方法相比，我们的方法提供了具有高视觉质量的高分辨率视频。 et.al.|[2407.05577](http://arxiv.org/abs/2407.05577)|null|
|**2024-06-20**|**MultiTalk: Enhancing 3D Talking Head Generation Across Languages with Multilingual Video Dataset**|最近在语音驱动的3D说话头生成方面的研究在言语表达方面取得了令人信服的结果。然而，当应用于其他语言的输入语音时，生成准确的嘴唇同步会降低质量，这可能是由于缺乏覆盖跨语言面部运动的广泛数据集。在这项工作中，我们介绍了一项新任务，即从不同语言的语音中生成3D对话头。我们收集了一个新的多语言2D视频数据集，其中包括20种语言的420多个小时的谈话视频。通过我们提出的数据集，我们提出了一个多语言增强模型，该模型结合了特定语言的风格嵌入，使其能够捕捉与每种语言相关的独特嘴部动作。此外，我们还提出了一种在多语言环境中评估唇同步准确性的指标。我们证明，使用我们提出的数据集训练3D说话头模型可以显著提高其多语言性能。代码和数据集可在https://multi-talk.github.io/. et.al.|[2406.14272](http://arxiv.org/abs/2406.14272)|null|
|**2024-06-17**|**NLDF: Neural Light Dynamic Fields for Efficient 3D Talking Head Generation**|基于神经辐射场模型的说话头生成显示出有前景的视觉效果。然而，由于合成一个像素需要数百个采样点的繁重计算过程，NeRF的缓慢渲染速度严重限制了它的应用。在这项工作中，提出了一种新的神经光动态场模型，旨在以显著的速度生成高质量的3D说话面。NLDF表示基于光段的光场，深度网络用于一次学习整个光束的信息。在学习过程中，应用了知识蒸馏，并使用基于NeRF的合成结果来指导NLDF中光段的正确着色。此外，提出了一种新的主动池训练策略，专注于高频运动，特别是说话者的嘴和眉毛。所提出的方法有效地表示了3D谈话视频生成中的面部光动态，与基于NeRF的现有技术方法相比，其速度快了约30倍，生成视觉质量相当。 et.al.|[2406.11259](http://arxiv.org/abs/2406.11259)|null|
|**2024-06-18**|**A Comprehensive Taxonomy and Analysis of Talking Head Synthesis: Techniques for Portrait Generation, Driving Mechanisms, and Editing**|会说话的头部合成是一种从特定内容驱动的静止图像生成肖像视频的先进方法，在虚拟现实、增强现实和游戏制作中引起了广泛关注。最近，随着变压器和扩散模型等新模型的引入，取得了重大突破。当前的方法不仅可以生成新内容，还可以编辑生成的材料。这项调查系统地回顾了这项技术，将其分为三个关键领域：肖像生成、驱动机制和编辑技术。我们总结了里程碑式的研究，并批判性地分析了它们在每个领域的创新和不足。此外，我们组织了大量的数据集，并根据各种评估指标对当前方法进行了全面的性能分析，旨在为未来的研究提供清晰的框架和强有力的数据支持。最后，我们探索了说话头合成的应用场景，用具体案例加以说明，并探讨了未来的潜在方向。 et.al.|[2406.10553](http://arxiv.org/abs/2406.10553)|null|
|**2024-06-13**|**Talking Heads: Understanding Inter-layer Communication in Transformer Language Models**|尽管已知变换器语言模型（LM）将特征从早期层传递到后期层，但尚不清楚模型是如何表示和路由这些信息的。通过分析LM用于实现这一点的特定机制，我们发现它也用于从列表中召回项目，并表明这种机制可以解释模型对提示中项目顺序的任意敏感性。具体来说，我们发现模型写入残差流的低秩子空间来表示特征，然后由特定的后续层读出，在层之间形成低秩通信信道。通过用奇异值分解（SVD）分解注意力头部权重矩阵，我们发现，通过分析其权重矩阵，可以预测先前描述的由一层或多层分隔的头部之间的相互作用。我们表明，可以根据我们发现的机制操纵内部模型表示以及编辑模型权重，以显著提高我们的合成洗衣清单任务的性能，该任务需要从列表中召回，通常可以将任务准确率提高20%以上。我们的分析揭示了从语言模型预训练中学到的一个令人惊讶的复杂可解释结构，并帮助我们理解为什么复杂的LM有时会在简单的领域失败，从而促进未来对更复杂行为的分析。 et.al.|[2406.09519](http://arxiv.org/abs/2406.09519)|null|
|**2024-05-12**|**Listen, Disentangle, and Control: Controllable Speech-Driven Talking Head Generation**|早期关于说话脸生成的大多数研究都集中在嘴唇运动和语音内容的同步上。然而，人的头部姿态和面部情绪是自然人脸同样重要的特征。虽然音频驱动的说话脸生成已经取得了显著的进步，但现有的方法要么忽视了面部情绪，要么仅限于特定的个人，不能应用于任意的受试者。在这篇论文中，我们提出了一种一次性的说话头生成框架（SPEAK），它通过启用情绪和姿势控制来区别于一般的说话脸生成。具体而言，我们引入了重建特征间解耦（IRFD）方法，将人脸特征解耦为三个潜在空间。然后，我们设计了一个面部编辑模块，将语音内容和面部潜码修改为单个潜空间。随后，我们提出了一种新的生成器，该生成器使用从编辑模块导出的修改后的潜码来调节合成面部动画时的情绪表达、头部姿势和语音内容。大量试验表明，我们的方法可以生成具有协调嘴唇动作、真实面部情绪和流畅头部运动的逼真说话头部。演示视频可通过匿名链接获得：https://anonymous.4open.science/r/SPEAK-F56E et.al.|[2405.07257](http://arxiv.org/abs/2405.07257)|null|
|**2024-05-10**|**NeRFFaceSpeech: One-shot Audio-driven 3D Talking Head Synthesis via Generative Prior**|音频驱动的对话头一代正在从2D内容向3D内容发展。值得注意的是，神经辐射场（NeRF）作为合成高质量3D对话头输出的一种手段，备受关注。不幸的是，这种基于NeRF的方法通常需要为每个身份提供大量成对的视听数据，从而限制了该方法的可扩展性。尽管有人试图用单个图像生成音频驱动的3D说话头动画，但由于图像中模糊区域的信息不足，结果往往不令人满意。在本文中，我们主要关注在单镜头音频驱动领域中被忽视的3D一致性方面，在该领域中，面部动画主要是在正面视角中合成的。我们提出了一种新的方法，即NeRFFaceSpeech，它能够产生高质量的3D感知说话头。利用生成模型的先验知识并结合NeRF，我们的方法可以创建一个与单个图像相对应的3D一致的面部特征空间。我们的空间同步方法利用参数化人脸模型的音频相关顶点动力学，通过光线变形将静态图像特征转换为动态视觉效果，确保逼真的3D面部运动。此外，我们引入了LipaintNet，它可以补充口腔内部区域缺乏的信息，这些信息无法从给定的单张图像中获得。该网络通过利用生成能力以自我监督的方式进行训练，而无需额外的数据。综合实验证明，与以前的方法相比，我们的方法在从单个图像生成具有增强3D一致性的音频驱动说话头方面具有优势。此外，我们首次引入了一种定量方法来衡量模型对姿态变化的鲁棒性，这种方法只能定性地实现。 et.al.|[2405.05749](http://arxiv.org/abs/2405.05749)|null|
|**2024-04-25**|**GaussianTalker: Real-Time High-Fidelity Talking Head Synthesis with Audio-Driven 3D Gaussian Splatting**|我们提出了GaussianTalker，这是一种实时生成姿态可控说话头的新框架。它利用了3D高斯散斑（3DGS）的快速渲染功能，同时解决了通过语音音频直接控制3DGS的挑战。GaussianTalker构建了头部的规范3DGS表示，并使其与音频同步变形。一个关键的见解是将3D高斯属性编码为共享的隐式特征表示，在那里它与音频特征合并以操纵每个高斯属性。这种设计利用了空间感知特征，并加强了相邻点之间的交互。然后，特征嵌入被馈送到空间音频注意力模块，该模块预测每个高斯属性的逐帧偏移。它比以前的级联或乘法方法更稳定，可以操纵大量的高斯分布及其复杂的参数。实验结果表明，与之前的方法相比，GaussianTalker在面部保真度、嘴唇同步精度和渲染速度方面具有优势。具体来说，GaussianTalker实现了高达120 FPS的卓越渲染速度，超过了之前的基准测试。我们的代码可在以下网址获得https://github.com/KU-CVLAB/GaussianTalker/ . et.al.|[2404.16012](http://arxiv.org/abs/2404.16012)|**[link](https://github.com/ku-cvlab/gaussiantalker)**|
|**2024-07-05**|**TalkingGaussian: Structure-Persistent 3D Talking Head Synthesis via Gaussian Splatting**|辐射场在合成逼真的3D对话头方面表现出了令人印象深刻的性能。然而，由于难以适应陡峭的外观变化，通过直接修改点外观来呈现面部运动的主流范式可能会导致动态区域的失真。为了应对这一挑战，我们引入了TalkingGaussian，这是一种基于变形的辐射场框架，用于高保真说话头合成。利用基于点的高斯散斑，我们的方法可以通过对持久的高斯基元应用平滑和连续的变形来表示面部运动，而不需要像以前的方法那样学习困难的外观变化。由于这种简化，可以在保持高度完整的面部特征的同时合成精确的面部动作。在这种变形范式下，我们进一步发现了一种面部-嘴部运动不一致，这会影响详细说话动作的学习。为了解决这一冲突，我们将模型分别分解为面部和口腔内部区域的两个分支，从而简化了学习任务，以帮助重建口腔区域更准确的运动和结构。大量实验表明，与之前的方法相比，我们的方法能够渲染出高质量的嘴唇同步说话头视频，具有更好的面部保真度和更高的效率。 et.al.|[2404.15264](http://arxiv.org/abs/2404.15264)|null|
|**2024-04-28**|**GaussianTalker: Speaker-specific Talking Head Synthesis via 3D Gaussian Splatting**|最近使用神经辐射场（NeRF）进行音频驱动的说话头合成的工作取得了令人印象深刻的结果。然而，由于NeRF隐式表示导致的姿势和表情控制不足，这些方法仍然存在一些局限性，例如嘴唇运动不同步或不自然，以及视觉抖动和伪影。本文提出了一种基于3D高斯散斑的音频驱动说话头合成新方法——GaussianTalker。利用三维高斯分布的显式表示特性，通过将高斯分布绑定到三维面部模型，实现了对面部运动的直观控制。GaussianTalker由两个模块组成，特定于说话者的运动翻译器和动态高斯渲染器。特定于说话者的运动翻译器通过通用的音频特征提取和定制的嘴唇运动生成，实现了特定于目标说话者的精确嘴唇运动。动态高斯渲染器引入了特定于说话者的BlendShapes，通过潜在姿势增强面部细节表现，提供稳定逼真的渲染视频。大量的实验结果表明，GaussianTalker在说话头合成方面优于现有的最先进的方法，提供了精确的嘴唇同步和卓越的视觉质量。我们的方法在NVIDIA RTX4090 GPU上实现了130 FPS的渲染速度，大大超过了实时渲染性能的阈值，并有可能部署在其他硬件平台上。 et.al.|[2404.14037](http://arxiv.org/abs/2404.14037)|null|
|**2024-04-13**|**THQA: A Perceptual Quality Assessment Database for Talking Heads**|在媒体技术领域，由于计算机技术的快速发展，数字人已经变得突出。然而，大多数数字人所需的手动建模和控制对高效开发构成了重大障碍。语音驱动方法为操纵数字人类的嘴形和表情提供了一条新途径。尽管驾驶方法激增，但许多生成的说话头（TH）视频的质量仍然是一个问题，影响了用户的视觉体验。为了解决这个问题，本文介绍了Talking Head质量评估（THQA）数据库，该数据库包含通过8种不同的语音驱动方法生成的800个TH视频。大量实验证实了THQA数据库在字符和语音特征方面的丰富性。随后的主观质量评估实验分析了评分结果与语音驱动方法、年龄和性别之间的相关性。此外，实验结果表明，主流图像和视频质量评估方法对THQA数据库存在局限性，强调了进一步研究以提高TH视频质量评估的必要性。THQA数据库可在以下网址公开访问https://github.com/zyj-2000/THQA. et.al.|[2404.09003](http://arxiv.org/abs/2404.09003)|**[link](https://github.com/zyj-2000/thqa)**|
|**2024-04-07**|**GvT: A Graph-based Vision Transformer with Talking-Heads Utilizing Sparsity, Trained from Scratch on Small Datasets**|视觉变换器（ViTs）在大规模图像分类中取得了令人印象深刻的结果。然而，当在小数据集上从头开始训练时，ViT和卷积神经网络（CNN）之间仍然存在显著的性能差距，这归因于缺乏归纳偏差。为了解决这个问题，我们提出了一种基于图的视觉变换器（GvT），它利用了图卷积投影和图池。在每个块中，查询和关键字是通过基于空间邻接矩阵的图卷积投影来计算的，而点积注意力则用于另一个图卷积来生成值。当使用更多的注意力头时，查询和键的维数会降低，使它们的点积成为一个无信息的匹配函数。为了克服注意力低阶瓶颈，我们采用了基于双线性混合特征和稀疏选择注意力张量的说话头技术。这允许过滤后的注意力得分之间的交互，并使每个注意力机制都依赖于所有查询和关键字。此外，我们在两个中间块之间应用图池，以减少令牌数量并更有效地聚合语义信息。我们的实验结果表明，GvT产生了与深度卷积网络相当或更优的结果，并且在没有对大型数据集进行预训练的情况下超越了视觉变换器。我们提出的模型的代码可以在网站上公开获得。 et.al.|[2404.04924](http://arxiv.org/abs/2404.04924)|null|
|**2024-04-02**|**EDTalk: Efficient Disentanglement for Emotional Talking Head Synthesis**|实现对多个面部动作的解耦控制并适应不同的输入方式，大大增强了会说话的一代的应用和娱乐性。这需要深入探索面部特征的解耦空间，确保它们a）独立运行而不相互干扰，b）可以保留以与不同的模态输入共享，这两个方面在现有方法中经常被忽视。为了解决这一差距，本文提出了一种新的用于说话头生成的高效去纠缠框架（EDTalk）。我们的框架允许根据视频或音频输入对嘴形、头部姿势和情绪表达进行单独操纵。具体来说，我们使用三个轻量级模块将面部动态分解为三个不同的潜在空间，分别表示嘴巴、姿势和表情。每个空间都有一组可学习的基，其线性组合定义了特定的运动。为了确保独立性并加快训练速度，我们加强了基地之间的正交性，并设计了一种有效的训练策略，在不依赖外部知识的情况下将运动责任分配给每个空间。然后将学习到的库存储在相应的库中，从而实现具有音频输入的共享视觉先验。此外，考虑到每个空间的特性，我们提出了一种用于音频驱动的说话头合成的音频到运动模块。实验证明了EDTalk的有效性。我们建议您查看项目网站：https://tanshuai0219.github.io/EDTalk/ et.al.|[2404.01647](http://arxiv.org/abs/2404.01647)|null|
|**2024-03-28**|**MoDiTalker: Motion-Disentangled Diffusion Model for High-Fidelity Talking Head Generation**|传统的基于GAN的说话头生成模型往往质量有限，训练不稳定。最近基于扩散模型的方法旨在解决这些局限性并提高保真度。然而，它们仍然面临着挑战，包括广泛的采样时间和由于扩散模型的高度随机性而难以保持时间一致性。为了克服这些挑战，我们提出了一种新的用于高质量说话头生成的运动解纠缠扩散模型，称为MoDiTalker。我们介绍了两个模块：音频到运动（AToM），旨在从音频生成同步的嘴唇运动，以及运动到视频（MToV），设计用于根据生成的运动生成高质量的头部视频。AToM擅长通过利用音频注意力机制捕捉微妙的嘴唇动作。此外，MToV通过利用高效的三平面表示来增强时间一致性。我们在标准基准上进行的实验表明，与现有模型相比，我们的模型具有更优的性能。我们还提供全面的消融研究和用户研究结果。 et.al.|[2403.19144](http://arxiv.org/abs/2403.19144)|**[link](https://github.com/KU-CVLAB/MoDiTalker)**|
|**2024-03-23**|**Adaptive Super Resolution For One-Shot Talking-Head Generation**|单镜头说话头生成学习在相同或不同身份视频的驱动下，将说话头视频与一个源肖像图像合成。通常，这些方法需要通过雅可比矩阵或面部图像扭曲进行基于平面的像素变换，以生成新的姿势。使用单个图像源和像素位移的限制通常会影响合成图像的清晰度。一些方法试图通过引入额外的超分辨率模块来提高合成视频的质量，但这无疑会增加计算消耗并破坏原始数据分布。在这项工作中，我们提出了一种自适应的高质量说话头视频生成方法，该方法在没有额外预训练模块的情况下合成高分辨率视频。具体来说，受现有超分辨率方法的启发，我们对单镜头源图像进行下采样，然后通过编码器-解码器模块自适应地重建高频细节，从而提高了视频清晰度。我们的方法通过一种简单而有效的策略，不断提高生成视频的质量，并得到定量和定性评估的证实。代码和演示视频可在以下网址获得：\url{https://github.com/Songluchuan/AdaSR-TalkingHead/}. et.al.|[2403.15944](http://arxiv.org/abs/2403.15944)|**[link](https://github.com/songluchuan/adasr-talkinghead)**|
|**2024-03-19**|**EmoVOCA: Speech-Driven Emotional 3D Talking Heads**|近年来，3D对话头生成领域取得了重大进展。该领域的一个显著挑战在于将语音相关运动与表情动态相结合，这主要是由于缺乏将口语句子的多样性与各种面部表情相结合的全面3D数据集造成的。尽管文献工作试图利用2D视频数据和参数化3D模型作为解决方法，但在联合建模这两种运动时，这些方法仍然存在局限性。在这项工作中，我们从不同的角度解决了这个问题，并提出了一种创新的数据驱动技术，用于创建一个名为EmoVOCA的合成数据集，该数据集是通过组合一组无表情的3D说话头和一组3D表情序列获得的。为了展示这种方法的优点和数据集的质量，我们设计并训练了一个情感3D说话头生成器，该生成器接受3D面部、音频文件、情感标签和强度值作为输入，并学习用面部的表现特征来动画化音频同步的嘴唇动作。与文献中表现最佳的方法相比，使用我们的数据和生成器证据进行定量和定性综合实验，在合成令人信服的动画方面具有更高的能力。我们的代码和预训练模型将可用。 et.al.|[2403.12886](http://arxiv.org/abs/2403.12886)|null|
|**2024-03-19**|**ScanTalk: 3D Talking Heads from Unregistered Scans**|语音驱动的3D对话头生成已成为研究人员感兴趣的一个重要领域，带来了许多挑战。现有的方法受到具有固定拓扑的面动画的约束，其中建立了逐点对应关系，并且点的数量和顺序在模型可以动画化的所有身份中保持一致。在这项工作中，我们提出了ScanTalk，这是一个能够在包括扫描数据在内的任意拓扑中为3D人脸制作动画的新框架。我们的方法依赖于DiffusionNet架构来克服固定的拓扑约束，为更灵活、更逼真的3D动画提供了有前景的途径。通过利用DiffusionNet的强大功能，ScanTalk不仅可以适应不同的面部结构，而且在处理扫描数据时还可以保持保真度，从而增强生成的3D对话头的真实性和多功能性。通过与最先进的方法进行全面比较，我们验证了我们的方法的有效性，证明了它能够产生与现有技术相当的真实对话头。虽然我们的主要目标是开发一种不受拓扑约束的通用方法，但所有最先进的方法都受到这些限制的约束。用于复制我们结果的代码和预训练模型将可用。 et.al.|[2403.10942](http://arxiv.org/abs/2403.10942)|null|
|**2024-03-11**|**A Comparative Study of Perceptual Quality Metrics for Audio-driven Talking Head Videos**|人工智能生成内容（AIGC）技术的快速发展推动了音频驱动的对话头生成，在实际应用中引起了相当大的研究关注。然而，性能评估研究滞后于说话头生成技术的发展。现有文献依赖于启发式定量指标，没有经过人工验证，阻碍了准确的进度评估。为了弥补这一差距，我们收集了四种生成方法生成的会说话的头部视频，并对视觉质量、嘴唇音频同步和头部运动自然性进行了受控的心理物理学实验。我们的实验验证了模型预测和人类注释之间的一致性，确定了比广泛使用的度量更符合人类观点的度量。我们相信，我们的工作将促进绩效评估和模型开发，在更广泛的背景下提供对AIGC的见解。代码和数据将在https://github.com/zwx8981/ADTH-QA. et.al.|[2403.06421](http://arxiv.org/abs/2403.06421)|**[link](https://github.com/zwx8981/adth-qa)**|
|**2024-03-12**|**Style2Talker: High-Resolution Talking Head Generation with Emotion Style and Art Style**|尽管最近人们对自动动画音频驱动的说话头越来越感兴趣，但之前的努力主要集中在实现嘴唇与音频的同步，忽略了生成富有表现力的视频的两个关键要素：情感风格和艺术风格。本文提出了一种创新的音频驱动说话人脸生成方法，称为Style2Talker。它包括两个风格化阶段，即Style-E和Style-A，将文本控制的情感风格和图片控制的艺术风格整合到最终输出中。为了准备与视频相对应的稀缺情感文本描述，我们提出了一种无需人工的范式，该范式采用大规模预训练模型来自动注释现有视听数据集的情感文本标签。结合合成情感文本，Style-E阶段利用大规模CLIP模型提取情感表示，并将其与音频相结合，作为高效潜在扩散模型的条件，该模型旨在产生3DMM模型的情感运动系数。进入Style-A阶段，我们开发了一个系数驱动的运动生成器和一个嵌入在著名的StyleGAN中的艺术特定风格路径。这使我们能够使用生成的情感运动系数和艺术风格的源图片来合成高分辨率的艺术风格化的说话头视频。此外，为了更好地保留图像细节并避免伪影，我们为StyleGAN提供了从身份图像中提取的多尺度内容特征，并分别通过设计的内容编码器和细化网络细化其中间特征图。大量的实验结果表明，我们的方法在音频嘴唇同步以及情感风格和艺术风格的表现方面优于现有的最先进的方法。 et.al.|[2403.06365](http://arxiv.org/abs/2403.06365)|null|
|**2024-02-27**|**Learning Dynamic Tetrahedra for High-Quality Talking Head Synthesis**|最近在隐式表示方面的工作，如神经辐射场（NeRF），已经推进了从视频序列中生成逼真和可动画化的头部化身。这些隐式方法仍然面临着视觉伪影和抖动，因为缺乏显式的几何约束对精确建模复杂的面部变形构成了根本性的挑战。在本文中，我们介绍了动态四面体（DynTet），这是一种新的混合表示，它通过神经网络对显式动态网格进行编码，以确保各种运动和视点之间的几何一致性。DynTet由基于坐标的网络参数化，该网络学习带符号距离、变形和材料纹理，将训练数据锚定到预定义的四面体网格中。利用Marching tetrahedra，DynTet有效地解码具有一致拓扑的纹理网格，通过可微光栅化器实现快速渲染，并通过像素损失进行监控。 由于DynTet中采用了有效的几何表示，这些优点很容易实现。与之前的工作相比，DynTet根据各种指标在保真度、唇形同步和实时性能方面都有显著提高。除了生成稳定且视觉上吸引人的合成视频外，我们的方法还输出动态网格，这有望实现许多新兴应用。 et.al.|[2402.17364](http://arxiv.org/abs/2402.17364)|**[link](https://github.com/zhangzc21/dyntet)**|
|**2024-01-11**|**Jump Cut Smoothing for Talking Heads**|跳跃式剪辑为观看体验带来了突然的、有时是不必要的变化。我们提出了一种新的框架，用于在对话头视频的背景下平滑这些跳跃。我们利用视频中其他源帧的主体外观，将其与DensePose关键点和面部地标驱动的中级表示融合。为了实现运动，我们在切割周围的结束帧之间插值关键点和界标。然后，我们使用来自关键点和源帧的图像翻译网络来合成像素。由于关键点可能包含错误，我们提出了一种跨模态注意力方案，从每个关键点的多个选项中选择最合适的来源。通过利用这种中级表示，我们的方法可以获得比强视频插值基线更强的结果。我们在会说话的头部视频中的各种跳跃剪切上演示了我们的方法，例如剪切填充词、停顿，甚至随机剪切。我们的实验表明，我们可以实现无缝过渡，即使在具有挑战性的情况下，说话的头在跳投中旋转或剧烈移动。 et.al.|[2401.04718](http://arxiv.org/abs/2401.04718)|null|
|**2023-12-23**|**TransFace: Unit-Based Audio-Visual Speech Synthesizer for Talking Head Translation**|直接语音到语音翻译通过引入从自监督学习中获得的离散单元来实现高质量的结果。这种方法避免了与模型级联相关的延迟和级联错误。然而，与音频语音相比，将视听语音（即说话头视频）从一种语言转换为另一种语言的说话头翻译仍然面临着几个挑战：（1）现有的方法总是依赖于级联，通过音频和文本进行合成，导致延迟和级联错误。（2） 有声翻译的参考系有限。如果生成的翻译超过了原始语音的长度，则需要通过重复帧来补充视频序列，从而导致视频过渡不协调。在这项工作中，我们提出了一个说话头翻译模型\textbf{TransFace}，它可以直接将视听语音翻译成其他语言的视听语音。它由一个将音频语音转换为离散单元的语音到单元转换模型和一个基于单元的视听语音合成器Unit2Lip组成，用于并行地从离散单元重新合成同步的视听语音。此外，我们引入了一个有界持续时间预测器，确保等距说话头平移并防止重复参考系。实验证明，我们提出的Unit2Lip模型显著提高了同步性（在LSE-C上，原始和生成的音频语音分别为1.601和0.982），并将LRS2上的推理速度提高了4.35倍。此外，TransFace在LRS3-T和100%等时翻译上的Es-En和Fr-En的BLEU得分分别为61.93和47.55，令人印象深刻。 et.al.|[2312.15197](http://arxiv.org/abs/2312.15197)|null|
|**2023-12-18**|**AE-NeRF: Audio Enhanced Neural Radiance Field for Few Shot Talking Head Synthesis**|音频驱动的说话头合成是一个有前景的话题，在数字人类、电影制作和虚拟现实中有着广泛的应用。与之前的研究相比，最近基于NeRF的方法在质量和保真度方面显示出优越性。然而，当涉及到少镜头说话头生成时，一个身份只有几秒钟的说话视频，出现了两个局限性：1）它们要么没有基础模型，作为快速收敛的面部先验，要么在构建先验时忽略了音频的重要性；2） 他们中的大多数人忽视了不同面部区域与音频之间的相关性，例如，嘴与音频相关，而耳朵与音频无关。本文中，我们提出了音频增强神经辐射场（AE-NeRF）来解决上述问题，它可以用较少的数据集生成新说话者的逼真肖像。具体来说，我们在参考方案的特征融合阶段引入了一个音频感知聚合模块，其中权重由参考图像和目标图像之间的音频相似性决定。然后，提出了一种音频对齐人脸生成策略，利用双NeRF框架分别对音频相关和音频无关区域进行建模。大量实验表明，AE NeRF在图像保真度、音频嘴唇同步和泛化能力方面超越了最先进的技术，即使在有限的训练集或训练迭代中也是如此。 et.al.|[2312.10921](http://arxiv.org/abs/2312.10921)|null|
|**2023-12-15**|**DreamTalk: When Expressive Talking Head Generation Meets Diffusion Probabilistic Models**|扩散模型在各种下游生成任务中取得了显著的成功，但在重要且具有挑战性的表达性说话头生成中仍未得到充分探索。在这项工作中，我们提出了一个DreamTalk框架来填补这一空白，该框架采用细致的设计来释放扩散模型在生成富有表现力的对话头方面的潜力。具体来说，DreamTalk由三个关键组成部分组成：去噪网络、风格感知唇专家和风格预测器。基于扩散的去噪网络能够跨不同表情一致地合成高质量的音频驱动面部运动。为了提高嘴唇动作的表现力和准确性，我们引入了一位具有风格意识的嘴唇专家，他可以在注意说话风格的同时指导嘴唇同步。为了消除对表情参考视频或文本的需要，利用额外的基于扩散的风格预测器直接从音频中预测目标表情。通过这种方式，DreamTalk可以利用强大的扩散模型有效地生成富有表现力的面部，并减少对昂贵的风格参考的依赖。实验结果表明，DreamTalk能够生成具有不同说话风格的照片般逼真的说话面孔，并实现准确的嘴唇动作，超越了现有的最先进的同行。 et.al.|[2312.09767](http://arxiv.org/abs/2312.09767)|null|
|**2023-12-11**|**DiT-Head: High-Resolution Talking Head Synthesis using Diffusion Transformers**|我们提出了一种名为“DiT-head”的新型说话头合成流水线，该流水线基于扩散变换器，并使用音频作为条件来驱动扩散模型的去噪过程。我们的方法是可扩展的，可以推广到多个身份，同时产生高质量的结果。我们训练和评估了我们提出的方法，并将其与现有的说话头合成方法进行了比较。我们证明，我们的模型在视觉质量和唇形同步精度方面可以与这些方法竞争。我们的研究结果突出了我们提出的方法在广泛应用中的潜力，包括虚拟助手、娱乐和教育。有关结果和我们的用户研究的视频演示，请参阅我们的补充材料。 et.al.|[2312.06400](http://arxiv.org/abs/2312.06400)|null|
|**2023-12-09**|**R2-Talker: Realistic Real-Time Talking Head Synthesis with Hash Grid Landmarks Encoding and Progressive Multilayer Conditioning**|动态NeRF最近在3D谈话肖像合成方面引起了越来越多的关注。尽管在渲染速度和视觉质量方面取得了进步，但在提高效率和有效性方面仍然存在挑战。我们提出了R2 Talker，这是一个高效且有效的框架，能够实现逼真的实时说话头合成。具体来说，我们使用多分辨率哈希网格，介绍了一种将面部地标编码为条件特征的新方法。该方法通过将任意地标映射到统一的特征空间，将地标结构无损编码为条件特征，解耦输入多样性和条件空间。我们进一步提出了一种在NeRF渲染管道中进行渐进式多层条件处理的方案，以实现有效的条件特征融合。与最先进的作品相比，我们的新方法具有以下优势：1）无损输入编码能够获得更精确的特征，从而产生卓越的视觉质量。输入和条件空间的解耦提高了泛化能力。2） 在每个MLP层融合条件特征和MLP输出增强了条件影响，从而实现了更准确的嘴唇合成和更好的视觉质量。3） 它紧凑地构建了条件特征的融合，显著提高了计算效率。 et.al.|[2312.05572](http://arxiv.org/abs/2312.05572)|null|
|**2023-12-07**|**VividTalk: One-Shot Audio-Driven Talking Head Generation Based on 3D Hybrid Prior**|近年来，音频驱动的说话头生成引起了人们的广泛关注，在嘴唇同步、富有表现力的面部表情、自然的头部姿势生成和高视频质量方面做出了许多努力。然而，由于音频和运动之间的一对多映射，还没有一个模型能够引领或捆绑所有这些指标。在本文中，我们提出了VividTalk，这是一个两阶段通用框架，支持生成具有上述所有属性的高视觉质量说话头视频。具体来说，在第一阶段，我们通过学习两种运动将音频映射到网格，包括非刚性表情运动和刚性头部运动。对于表情运动，采用混合形状和顶点作为中间表示，以最大限度地提高模型的表示能力。针对自然头部运动，提出了一种具有两阶段训练机制的可学习头部姿态码本。在第二阶段，我们提出了一种双分支运动矢量和一个生成器，将网格转换为密集运动，并逐帧合成高质量的视频。大量实验表明，所提出的VividTalk可以生成具有唇形同步和逼真度大幅增强的高视觉质量的说话头视频，并且在客观和主观比较方面优于之前最先进的作品。 et.al.|[2312.01841](http://arxiv.org/abs/2312.01841)|null|
|**2024-04-28**|**SyncTalk: The Devil is in the Synchronization for Talking Head Synthesis**|在合成逼真的、语音驱动的说话头视频时实现高同步是一个重大挑战。传统的生成对抗网络（GAN）难以保持一致的面部身份，而神经辐射场（NeRF）方法虽然可以解决这个问题，但通常会产生不匹配的嘴唇动作、不充分的面部表情和不稳定的头部姿势。一个栩栩如生的会说话的头需要主体身份、嘴唇动作、面部表情和头部姿势的同步协调。缺乏这些同步是一个根本缺陷，导致不切实际和人为的结果。为了解决同步这一关键问题，我们引入了SyncTalk，它被认为是创造逼真对话头的“魔鬼”。这种基于NeRF的方法有效地保持了主体身份，增强了说话头合成的同步性和真实性。SyncTalk采用面部同步控制器将嘴唇动作与语音对齐，并创新性地使用3D面部混合形状模型来捕捉准确的面部表情。我们的头部同步稳定器优化了头部姿势，实现了更自然的头部运动。肖像同步生成器恢复头发细节，并将生成的头部与躯干融合在一起，以获得无缝的视觉体验。大量的实验和用户研究表明，SyncTalk在同步和真实性方面优于最先进的方法。我们建议您观看补充视频：https://ziqiaopeng.github.io/synctalk et.al.|[2311.17590](http://arxiv.org/abs/2311.17590)|**[link](https://github.com/ZiqiaoPeng/SyncTalk)**|
|**2023-11-30**|**Talking Head(?) Anime from a Single Image 4: Improved Model and Its Distillation**|我们研究了创建一个可以从动漫角色的单个图像实时控制的角色模型的问题。这个问题的解决方案将大大降低创建化身、电脑游戏和其他交互式应用程序的成本。Talking Head Anime 3（THA3）是一个开源项目，试图直接解决这个问题。它接收（1）动漫角色上半身的图像和（2）45维姿势向量作为输入，并输出采取指定姿势的同一角色的新图像。可能的动作范围足以表达个人化身和某些类型的游戏角色。然而，该系统速度太慢，无法在普通PC上实时生成动画，其图像质量可以提高。本文从两个方面对THA3进行了改进。首先，我们提出了基于U-Nets的组成网络的新架构，该网络基于在现代生成模型中广泛使用的注意旋转角色的头部和身体。新架构始终比THA3基线产生更好的图像质量。然而，它们也使整个系统慢得多：生成一帧需要150毫秒。其次，我们提出了一种技术，将系统提炼成一个小网络（小于2 MB），该网络可以使用消费类游戏GPU实时生成512x512个动画帧（低于30 FPS），同时保持图像质量接近整个系统的图像质量。这一改进使整个系统适用于实时应用。 et.al.|[2311.17409](http://arxiv.org/abs/2311.17409)|null|

<p align=right>(<a href=#updated-on-20240716>back to top</a>)</p>

[contributors-shield]: https://img.shields.io/github/contributors/Vincentqyw/cv-arxiv-daily.svg?style=for-the-badge
[contributors-url]: https://github.com/Vincentqyw/cv-arxiv-daily/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/Vincentqyw/cv-arxiv-daily.svg?style=for-the-badge
[forks-url]: https://github.com/Vincentqyw/cv-arxiv-daily/network/members
[stars-shield]: https://img.shields.io/github/stars/Vincentqyw/cv-arxiv-daily.svg?style=for-the-badge
[stars-url]: https://github.com/Vincentqyw/cv-arxiv-daily/stargazers
[issues-shield]: https://img.shields.io/github/issues/Vincentqyw/cv-arxiv-daily.svg?style=for-the-badge
[issues-url]: https://github.com/Vincentqyw/cv-arxiv-daily/issues

