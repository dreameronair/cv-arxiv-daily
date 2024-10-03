[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]

## Updated on 2024.10.03
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
|**2024-10-01**|**LaDTalk: Latent Denoising for Synthesizing Talking Head Videos with High Frequency Details**|音频驱动的说话头生成是电影制作和虚拟现实中的一个关键领域。尽管现有的方法在遵循端到端范式方面取得了重大进展，但由于在该领域的表现力有限，它们在制作具有高频细节的视频方面仍然遇到了挑战。这种局限性促使我们探索一种有效的后处理方法来合成逼真的说话头视频。具体来说，我们采用预训练的Wav2Lip模型作为我们的基础模型，利用其强大的音频唇对齐功能。基于Lipschitz连续性理论，我们从理论上建立了矢量量化自编码器（VQAE）的噪声鲁棒性。我们的实验进一步证明，我们引入的空间优化矢量量化自动编码器（SOVQAE）可以在时间上一致地恢复基础模型的高频纹理缺陷，从而有助于创建逼真的说话头视频。我们在传统数据集和我们策划的高频TalKing头部（HFTK）数据集上进行了实验。结果表明，我们的方法LaDTalk实现了最新的视频质量和域外唇形同步性能。 et.al.|[2410.00990](http://arxiv.org/abs/2410.00990)|null|
|**2024-09-29**|**Learning Frame-Wise Emotion Intensity for Audio-Driven Talking-Head Generation**|人类的情感表达本质上是动态的、复杂的和流动的，其特征是在整个言语交流中强度的平稳过渡。然而，这种强度波动的建模在很大程度上被之前的音频驱动的说话头生成方法所忽视，这通常会导致静态的情绪输出。本文探讨了言语过程中情绪强度的波动，提出了一种捕捉和生成这些微妙变化的方法，用于生成说话的头部。具体来说，我们开发了一个说话头框架，能够通过精确控制强度水平来产生各种情绪。这是通过学习一个连续的情绪潜在空间来实现的，在这个空间里，情绪类型被编码在潜在的取向中，情绪强度被反映在潜在的规范中。此外，为了捕捉动态强度波动，我们通过考虑反映强度的说话语调来采用音频强度预测器。该预测器的训练信号是通过我们的情绪无关强度伪标记方法获得的，不需要逐帧强度标记。大量的实验和分析验证了我们提出的方法在准确捕捉和再现说话头生成中的情绪强度波动方面的有效性，从而显著提高了生成输出的表现力和真实感。 et.al.|[2409.19501](http://arxiv.org/abs/2409.19501)|null|
|**2024-09-16**|**DreamHead: Learning Spatial-Temporal Correspondence via Hierarchical Diffusion for Audio-driven Talking Head Synthesis**|音频驱动的说话头合成努力从提供的音频中生成逼真的视频肖像。扩散模型因其卓越的质量和鲁棒的泛化能力而受到认可，已被探索用于这项任务。然而，利用扩散模型在时间音频线索和相应的空间面部表情之间建立鲁棒的对应关系仍然是说话头部生成的一个重大挑战。为了弥合这一差距，我们提出了DreamHead，这是一个分层扩散框架，可以在不损害模型内在质量和适应性的情况下学习说话头合成中的时空对应关系~DreamHead学习从音频中预测密集的面部标志作为中间信号，以模拟空间和时间的对应关系~具体而言，首先设计音频到地标扩散的第一层次，以在给定音频序列信号的情况下预测时间平滑和准确的地标序列。然后，进一步提出了第二层次的地标到图像扩散，通过建模密集的面部地标和外观之间的空间对应关系，产生空间一致的面部肖像视频。大量实验表明，所提出的DreamHead可以通过设计的分层扩散有效地学习时空一致性，并为多个身份生成高保真音频驱动的说话头视频。 et.al.|[2409.10281](http://arxiv.org/abs/2409.10281)|null|
|**2024-09-14**|**StyleTalk++: A Unified Framework for Controlling the Speaking Styles of Talking Heads**|个人有独特的面部表情和头部姿势风格，反映了他们的个性化说话风格。现有的单镜头说话头方法无法捕捉到这种个性化特征，因此无法在最终视频中产生多样化的说话风格。为了应对这一挑战，我们提出了一种单镜头风格可控的说话脸生成方法，该方法可以从参考说话视频中获取说话风格，并驱动单镜头肖像与参考说话风格和另一段音频一起说话。我们的方法旨在在一个统一的框架内合成3D可变形模型（3DMM）的风格可控系数，包括面部表情和头部运动。具体来说，所提出的框架首先利用风格编码器从参考视频中提取所需的说话风格，并将其转换为风格代码。然后，该框架使用风格感知解码器从音频输入和风格代码中合成3DMM的系数。在解码过程中，我们的框架采用了一种双分支架构，分别生成风格化的面部表情系数和风格化的头部运动系数。在获得3DMM的系数后，图像渲染器将表情系数渲染成特定人的说话头视频。大量实验表明，我们的方法仅从一张肖像图像和一段音频片段中生成具有不同说话风格的视觉真实的说话头视频。 et.al.|[2409.09292](http://arxiv.org/abs/2409.09292)|null|
|**2024-09-11**|**EMOdiffhead: Continuously Emotional Control in Talking Head Generation via Diffusion**|音频驱动的肖像动画的任务涉及使用身份图像和语音音轨生成会说话的头部视频。虽然许多现有的方法侧重于嘴唇同步和视频质量，但很少有方法能够解决生成情绪驱动的说话头视频的挑战。控制和编辑情绪的能力对于制作富有表现力和逼真的动画至关重要。为了应对这一挑战，我们提出了EMOdiffhead，这是一种用于情感对话头视频生成的新方法，不仅可以精细控制情感类别和强度，还可以生成单镜头视频。考虑到FLAME 3D模型在表情建模中的线性，我们利用DECA方法提取表情向量，并将其与音频相结合，以指导扩散模型生成具有精确嘴唇同步和丰富情感表现力的视频。这种方法不仅可以从与情绪无关的数据中学习丰富的面部信息，还可以促进情绪视频的生成。它有效地克服了情绪数据的局限性，例如面部和背景信息缺乏多样性，并解决了情绪无关数据中缺乏情绪细节的问题。大量的实验和用户研究表明，与其他情感肖像动画方法相比，我们的方法实现了最先进的性能。 et.al.|[2409.07255](http://arxiv.org/abs/2409.07255)|null|
|**2024-09-05**|**SVP: Style-Enhanced Vivid Portrait Talking Head Diffusion Model**|通常由音频驱动的Talking Head Generation（THG）是一项重要而具有挑战性的任务，在数字人类、电影制作和虚拟现实等各个领域具有广阔的应用前景。虽然基于扩散模型的THG方法提供了高质量和稳定的内容生成，但它们往往忽视了包含个性化特征的内在风格，如视频的说话习惯和面部表情。因此，生成的视频内容缺乏多样性和生动性，因此在现实生活场景中受到限制。为了解决这些问题，我们提出了一个名为风格增强生动肖像（SVP）的新框架，该框架充分利用了THG中与风格相关的信息。具体来说，我们首先引入了新的概率风格先验学习，使用面部表情和音频嵌入将内在风格建模为高斯分布。通过“被戳”的对比目标来学习分布，有效地捕捉到每个视频中的动态风格信息。然后，我们对预训练的稳定扩散（SD）模型进行微调，通过交叉注意注入学习到的内在风格作为控制信号。实验表明，我们的模型能够生成多样化、生动、高质量的视频，对内在风格有灵活的控制，优于现有的最先进的方法。 et.al.|[2409.03270](http://arxiv.org/abs/2409.03270)|null|
|**2024-09-04**|**PoseTalk: Text-and-Audio-based Pose Control and Motion Refinement for One-Shot Talking Head Generation**|虽然之前的音频驱动的说话头生成（THG）方法从驾驶音频中生成头部姿势，但生成的姿势或嘴唇不能很好地匹配音频或不可编辑。在这项研究中，我们提出了\textbf{PoseTalk}，这是一个THG系统，可以自由生成嘴唇同步的会说话的头部视频，其头部姿势以文本提示和音频为条件。我们方法的核心见解是使用头部姿势来连接视觉、语言和音频信号。首先，我们建议从音频和文本提示中生成姿势，其中音频提供头部运动的短期变化和节奏对应，文本提示描述头部运动的长期语义。为了实现这一目标，我们设计了一个姿势潜在扩散（PLD）模型，在姿势潜在空间中从文本提示和音频线索中生成运动潜在。其次，我们观察到一个损失不平衡问题：嘴唇区域的损失占姿势和嘴唇造成的总重建损失的不到4%，这使得优化更倾向于头部运动而不是嘴唇形状。为了解决这个问题，我们提出了一种基于细化的学习策略，使用两个级联网络（即CoarseNet和RefineNet）合成自然的谈话视频。CoarseNet估计粗略运动以生成新姿势的动画图像，RefineNet侧重于通过从低分辨率到高分辨率逐步估计嘴唇运动来学习更精细的嘴唇运动，从而提高嘴唇同步性能。实验证明，与仅文本或仅音频相比，我们的姿势预测策略实现了更好的姿势多样性和真实性，我们的视频生成器模型在合成具有自然头部运动的说话视频方面优于最先进的方法。项目：https://junleen.github.io/projects/posetalk. et.al.|[2409.02657](http://arxiv.org/abs/2409.02657)|null|
|**2024-08-18**|**FD2Talk: Towards Generalized Talking Head Generation with Facial Decoupled Diffusion Model**|会说话的头部生成是一个重要的研究课题，仍然面临着许多挑战。以往的研究往往采用生成对抗网络或回归模型，这些模型受到生成质量和平均面部形状问题的困扰。尽管扩散模型显示出令人印象深刻的生成能力，但它们在说话头生成方面的探索仍然不尽如人意。这是因为他们要么只使用扩散模型来获得中间表示，然后使用另一个预训练的渲染器，要么忽略了复杂面部细节的特征解耦，如表情、头部姿势和外观纹理。因此，我们提出了一种用于说话头生成的面部解耦扩散模型，称为FD2Talk，它充分利用了扩散模型的优点，通过多阶段将复杂的面部细节解耦。具体来说，我们将面部细节分为运动和外观。在初始阶段，我们设计了扩散变换器，以从原始音频中准确预测运动系数。这些运动与外观高度解耦，与高维RGB图像相比，使网络更容易学习。随后，在第二阶段，我们对参考图像进行编码以捕获外观纹理。然后，预测的面部和头部运动以及编码的外观作为扩散UNet的条件，指导帧生成。得益于面部细节的解耦和充分利用扩散模型，大量实验证实，与以前最先进的方法相比，我们的方法在提高图像质量和生成更准确、更多样化的结果方面表现出色。 et.al.|[2408.09384](http://arxiv.org/abs/2408.09384)|null|
|**2024-08-18**|**S^3D-NeRF: Single-Shot Speech-Driven Neural Radiance Field for High Fidelity Talking Head Synthesis**|说话头合成是一种应用广泛的实用技术。目前基于神经辐射场（NeRF）的方法在用视频或从音频中回归的信号驱动单镜头说话头方面显示出了优越性。然而，他们中的大多数人没有直接将音频作为驱动信息，无法享受语音的灵活性和可用性。由于将音频信号映射到面部变形是不平凡的，本文设计了一种单镜头语音驱动神经辐射场（S^3D NeRF）方法来解决以下三个困难：学习每个身份的代表性外观特征，用音频模拟不同面部区域的运动，以及保持嘴唇区域的时间一致性。为此，我们引入了一种分层面部外观编码器来学习多尺度表示，以捕捉不同说话者的外观，并根据音频信号与不同面部区域之间的关系，精心设计了一个跨模态面部变形场来执行语音动画。此外，为了提高重要嘴唇区域的时间一致性，我们引入了一个嘴唇同步鉴别器来惩罚不同步的视听序列。大量实验表明，我们的S^3D NeRF在视频保真度和音频唇形同步方面都超越了以前的技术。 et.al.|[2408.09347](http://arxiv.org/abs/2408.09347)|null|
|**2024-08-03**|**Landmark-guided Diffusion Model for High-fidelity and Temporally Coherent Talking Head Generation**|音频驱动的对话头生成是一项重要而具有挑战性的任务，适用于虚拟化身、电影制作和在线会议等各个领域。然而，现有的基于GAN的模型强调生成同步良好的嘴唇形状，但忽视了生成帧的视觉质量，而基于扩散的模型则优先生成高质量的帧，但忽略了嘴唇形状匹配，导致嘴部运动不稳定。为了解决上述问题，我们引入了一个基于两阶段扩散的模型。第一阶段涉及基于给定的语音生成同步的面部标志。在第二阶段，这些生成的界标作为去噪过程中的一个条件，旨在优化嘴部抖动问题，并生成高保真、同步良好、时间连贯的说话头视频。大量实验表明，我们的模型具有最佳性能。 et.al.|[2408.01732](http://arxiv.org/abs/2408.01732)|null|
|**2024-08-03**|**JambaTalk: Speech-Driven 3D Talking Head Generation Based on Hybrid Transformer-Mamba Model**|近年来，会说话的一代已经成为研究人员关注的焦点。人们正在大力改进嘴唇同步运动，捕捉富有表现力的面部表情，生成自然的头部姿势，并实现高视频质量。然而，还没有一个模型在所有这些指标上实现了等效性。本文旨在使用混合变形金刚曼巴模型Jamba制作3D人脸动画。Mamba是一种开创性的结构化状态空间模型（SSM）架构，旨在解决传统Transformer架构的限制。然而，它有几个缺点。Jamba融合了Transformer和Mamba方法的优点，提供了一个整体解决方案。基于Jamba的基础模块，我们提出了JambaTalk，通过多模态集成来提高运动的多样性和速度。广泛的实验表明，我们的方法实现了与最先进的模型相当或更优的性能。 et.al.|[2408.01627](http://arxiv.org/abs/2408.01627)|null|
|**2024-08-01**|**EmoTalk3D: High-Fidelity Free-View Synthesis of Emotional 3D Talking Head**|我们提出了一种合成具有可控情绪的3D对话头的新方法，该方法具有增强的嘴唇同步和渲染质量。尽管在该领域取得了重大进展，但现有方法仍然存在多视图一致性和缺乏情感表达的问题。为了解决这些问题，我们收集了带有校准的多视图视频、情感注释和每帧3D几何的EmoTalk3D数据集。通过在EmoTalk3D数据集上进行训练，我们提出了一个\textit{“语音到几何到外观”}映射框架，该框架首先从音频特征预测忠实的3D几何序列，然后从预测的几何中合成由4D高斯表示的3D说话头的外观。该外观进一步被分解为规范高斯和动态高斯，从多视图视频中学习，并融合以渲染自由视图说话的头部动画。此外，我们的模型能够在生成的说话头中实现可控的情绪，并且可以在宽范围的视图中呈现。我们的方法在嘴唇运动生成中表现出改进的渲染质量和稳定性，同时捕获了动态面部细节，如皱纹和微妙的表情。实验证明了我们的方法在生成高保真度和情绪可控的3D对话头方面的有效性。代码和EmoTalk3D数据集发布于https://nju-3dv.github.io/projects/EmoTalk3D. et.al.|[2408.00297](http://arxiv.org/abs/2408.00297)|null|
|**2024-07-13**|**Learning Online Scale Transformation for Talking Head Video Generation**|单镜头说话头视频生成使用源图像和驾驶视频来创建合成视频，其中源人物的面部动作模仿驾驶视频的面部动作。然而，源图像和驱动图像之间的比例差异仍然是面部重现的一个挑战。现有的方法试图在驾驶视频中定位与源图像最对齐的帧，但不精确的对齐可能会导致次优结果。为此，我们引入了一个比例变换模块，该模块可以通过使用源图像和驱动帧的检测关键点中保持的比例差信息，自动调整驱动图像的比例以适应源图像的比例。此外，为了在生成过程中不断感知人脸的尺度信息，我们将从尺度变换模块学习到的尺度信息整合到生成过程的每一层中，以产生具有精确尺度的最终结果。我们的方法可以在没有任何锚帧的情况下在两幅图像之间进行精确的运动传递，这是通过所提出的在线尺度变换面部重现网络的贡献来实现的。大量实验表明，我们提出的方法根据源面部自动调整驱动面部的尺度，并在跨身份面部重现中生成具有精确尺度的高质量面部。 et.al.|[2407.09965](http://arxiv.org/abs/2407.09965)|null|
|**2024-07-08**|**Audio-driven High-resolution Seamless Talking Head Video Editing via StyleGAN**|现有的音频驱动说话头视频编辑方法存在视觉效果差的局限性。本文试图通过基于两个模块无缝编辑不同情绪的说话人脸图像来解决这个问题：（1）音频到地标模块，由交叉重建的情绪解耦和对齐网络模块组成。它通过从语音中预测相应的情感标志来弥合语音和面部动作之间的差距；（2） 基于地标的编辑模块通过StyleGAN编辑面部视频。它的目的是从输入音频中生成由情感和内容组成的无缝编辑视频。大量实验证实，与最先进的方法相比，我们的方法提供了具有高视觉质量的高分辨率视频。 et.al.|[2407.05577](http://arxiv.org/abs/2407.05577)|null|
|**2024-06-20**|**MultiTalk: Enhancing 3D Talking Head Generation Across Languages with Multilingual Video Dataset**|最近在语音驱动的3D说话头生成方面的研究在言语表达方面取得了令人信服的结果。然而，当应用于其他语言的输入语音时，生成准确的嘴唇同步会降低质量，这可能是由于缺乏覆盖跨语言面部运动的广泛数据集。在这项工作中，我们介绍了一项新任务，即从不同语言的语音中生成3D对话头。我们收集了一个新的多语言2D视频数据集，其中包括20种语言的420多个小时的谈话视频。通过我们提出的数据集，我们提出了一个多语言增强模型，该模型结合了特定语言的风格嵌入，使其能够捕捉与每种语言相关的独特嘴部动作。此外，我们还提出了一种在多语言环境中评估唇同步准确性的指标。我们证明，使用我们提出的数据集训练3D说话头模型可以显著提高其多语言性能。代码和数据集可在https://multi-talk.github.io/. et.al.|[2406.14272](http://arxiv.org/abs/2406.14272)|null|
|**2024-06-17**|**NLDF: Neural Light Dynamic Fields for Efficient 3D Talking Head Generation**|基于神经辐射场模型的说话头生成显示出有前景的视觉效果。然而，由于合成一个像素需要数百个采样点的繁重计算过程，NeRF的缓慢渲染速度严重限制了它的应用。在这项工作中，提出了一种新的神经光动态场模型，旨在以显著的速度生成高质量的3D说话面。NLDF表示基于光段的光场，深度网络用于一次学习整个光束的信息。在学习过程中，应用了知识蒸馏，并使用基于NeRF的合成结果来指导NLDF中光段的正确着色。此外，提出了一种新的主动池训练策略，专注于高频运动，特别是说话者的嘴和眉毛。所提出的方法有效地表示了3D谈话视频生成中的面部光动态，与基于NeRF的现有技术方法相比，其速度快了约30倍，生成视觉质量相当。 et.al.|[2406.11259](http://arxiv.org/abs/2406.11259)|null|
|**2024-06-18**|**A Comprehensive Taxonomy and Analysis of Talking Head Synthesis: Techniques for Portrait Generation, Driving Mechanisms, and Editing**|会说话的头部合成是一种从特定内容驱动的静止图像生成肖像视频的先进方法，在虚拟现实、增强现实和游戏制作中引起了广泛关注。最近，随着变压器和扩散模型等新模型的引入，取得了重大突破。当前的方法不仅可以生成新内容，还可以编辑生成的材料。这项调查系统地回顾了这项技术，将其分为三个关键领域：肖像生成、驱动机制和编辑技术。我们总结了里程碑式的研究，并批判性地分析了它们在每个领域的创新和不足。此外，我们组织了大量的数据集，并根据各种评估指标对当前方法进行了全面的性能分析，旨在为未来的研究提供清晰的框架和强有力的数据支持。最后，我们探索了说话头合成的应用场景，用具体案例加以说明，并探讨了未来的潜在方向。 et.al.|[2406.10553](http://arxiv.org/abs/2406.10553)|null|
|**2024-06-13**|**Talking Heads: Understanding Inter-layer Communication in Transformer Language Models**|尽管已知变换器语言模型（LM）将特征从早期层传递到后期层，但尚不清楚模型是如何表示和路由这些信息的。通过分析LM用于实现这一点的特定机制，我们发现它也用于从列表中召回项目，并表明这种机制可以解释模型对提示中项目顺序的任意敏感性。具体来说，我们发现模型写入残差流的低秩子空间来表示特征，然后由特定的后续层读出，在层之间形成低秩通信信道。通过用奇异值分解（SVD）分解注意力头部权重矩阵，我们发现，通过分析其权重矩阵，可以预测先前描述的由一层或多层分隔的头部之间的相互作用。我们表明，可以根据我们发现的机制操纵内部模型表示以及编辑模型权重，以显著提高我们的合成洗衣清单任务的性能，该任务需要从列表中召回，通常可以将任务准确率提高20%以上。我们的分析揭示了从语言模型预训练中学到的一个令人惊讶的复杂可解释结构，并帮助我们理解为什么复杂的LM有时会在简单的领域失败，从而促进未来对更复杂行为的分析。 et.al.|[2406.09519](http://arxiv.org/abs/2406.09519)|null|
|**2024-08-27**|**Listen, Disentangle, and Control: Controllable Speech-Driven Talking Head Generation**|早期关于说话脸生成的大多数研究都集中在嘴唇运动和语音内容的同步上。然而，人的头部姿态和面部情绪是自然人脸同样重要的特征。虽然音频驱动的说话脸生成已经取得了显著的进步，但现有的方法要么忽视了面部情绪，要么仅限于特定的个人，不能应用于任意的受试者。在这篇论文中，我们提出了一种一次性的说话头生成框架（SPEAK），它通过启用情绪和姿势控制来区别于一般的说话脸生成。具体而言，我们引入了重建特征间解耦（IRFD）方法，将人脸特征解耦为三个潜在空间。然后，我们设计了一个面部编辑模块，将语音内容和面部潜码修改为单个潜空间。随后，我们提出了一种新的生成器，该生成器使用从编辑模块导出的修改后的潜码来调节情绪表达、头部姿势和语音内容，以合成面部动画。大量试验表明，我们的方法可以生成具有协调嘴唇动作、真实面部情绪和流畅头部运动的逼真说话头部。演示视频可通过匿名链接获得：https://anonymous.4open.science/r/SPEAK-F56E et.al.|[2405.07257](http://arxiv.org/abs/2405.07257)|null|
|**2024-05-10**|**NeRFFaceSpeech: One-shot Audio-driven 3D Talking Head Synthesis via Generative Prior**|音频驱动的对话头一代正在从2D内容向3D内容发展。值得注意的是，神经辐射场（NeRF）作为合成高质量3D对话头输出的一种手段，备受关注。不幸的是，这种基于NeRF的方法通常需要为每个身份提供大量成对的视听数据，从而限制了该方法的可扩展性。尽管有人试图用单个图像生成音频驱动的3D说话头动画，但由于图像中模糊区域的信息不足，结果往往不令人满意。在本文中，我们主要关注在单镜头音频驱动领域中被忽视的3D一致性方面，在该领域中，面部动画主要是在正面视角中合成的。我们提出了一种新的方法，即NeRFFaceSpeech，它能够产生高质量的3D感知说话头。利用生成模型的先验知识并结合NeRF，我们的方法可以创建一个与单个图像相对应的3D一致的面部特征空间。我们的空间同步方法利用参数化人脸模型的音频相关顶点动力学，通过光线变形将静态图像特征转换为动态视觉效果，确保逼真的3D面部运动。此外，我们引入了LipaintNet，它可以补充口腔内部区域缺乏的信息，这些信息无法从给定的单张图像中获得。该网络通过利用生成能力以自我监督的方式进行训练，而无需额外的数据。综合实验证明，与以前的方法相比，我们的方法在从单个图像生成具有增强3D一致性的音频驱动说话头方面具有优势。此外，我们首次引入了一种定量方法来衡量模型对姿态变化的鲁棒性，这种方法只能定性地实现。 et.al.|[2405.05749](http://arxiv.org/abs/2405.05749)|null|
|**2024-04-25**|**GaussianTalker: Real-Time High-Fidelity Talking Head Synthesis with Audio-Driven 3D Gaussian Splatting**|我们提出了GaussianTalker，这是一种实时生成姿态可控说话头的新框架。它利用了3D高斯散斑（3DGS）的快速渲染功能，同时解决了通过语音音频直接控制3DGS的挑战。GaussianTalker构建了头部的规范3DGS表示，并使其与音频同步变形。一个关键的见解是将3D高斯属性编码为共享的隐式特征表示，在那里它与音频特征合并以操纵每个高斯属性。这种设计利用了空间感知特征，并加强了相邻点之间的交互。然后，特征嵌入被馈送到空间音频注意力模块，该模块预测每个高斯属性的逐帧偏移。它比以前的级联或乘法方法更稳定，可以操纵大量的高斯分布及其复杂的参数。实验结果表明，与之前的方法相比，GaussianTalker在面部保真度、嘴唇同步精度和渲染速度方面具有优势。具体来说，GaussianTalker实现了高达120 FPS的卓越渲染速度，超过了之前的基准测试。我们的代码可在以下网址获得https://github.com/KU-CVLAB/GaussianTalker/ . et.al.|[2404.16012](http://arxiv.org/abs/2404.16012)|**[link](https://github.com/ku-cvlab/gaussiantalker)**|
|**2024-07-05**|**TalkingGaussian: Structure-Persistent 3D Talking Head Synthesis via Gaussian Splatting**|辐射场在合成逼真的3D对话头方面表现出了令人印象深刻的性能。然而，由于难以适应陡峭的外观变化，通过直接修改点外观来呈现面部运动的主流范式可能会导致动态区域的失真。为了应对这一挑战，我们引入了TalkingGaussian，这是一种基于变形的辐射场框架，用于高保真说话头合成。利用基于点的高斯散斑，我们的方法可以通过对持久的高斯基元应用平滑和连续的变形来表示面部运动，而不需要像以前的方法那样学习困难的外观变化。由于这种简化，可以在保持高度完整的面部特征的同时合成精确的面部动作。在这种变形范式下，我们进一步发现了一种面部-嘴部运动不一致，这会影响详细说话动作的学习。为了解决这一冲突，我们将模型分别分解为面部和口腔内部区域的两个分支，从而简化了学习任务，以帮助重建口腔区域更准确的运动和结构。大量实验表明，与之前的方法相比，我们的方法能够渲染出高质量的嘴唇同步说话头视频，具有更好的面部保真度和更高的效率。 et.al.|[2404.15264](http://arxiv.org/abs/2404.15264)|null|
|**2024-08-09**|**GaussianTalker: Speaker-specific Talking Head Synthesis via 3D Gaussian Splatting**|最近使用神经辐射场（NeRF）进行音频驱动的说话头合成的工作取得了令人印象深刻的结果。然而，由于NeRF隐式表示导致的姿势和表情控制不足，这些方法仍然存在一些局限性，例如嘴唇运动不同步或不自然，以及视觉抖动和伪影。本文提出了一种基于3D高斯散斑的音频驱动说话头合成新方法——GaussianTalker。利用三维高斯分布的显式表示特性，通过将高斯分布绑定到三维面部模型，实现了对面部运动的直观控制。GaussianTalker由两个模块组成，特定于说话者的运动翻译器和动态高斯渲染器。特定于说话者的运动翻译器通过通用的音频特征提取和定制的嘴唇运动生成，实现了特定于目标说话者的精确嘴唇运动。动态高斯渲染器引入了特定于说话者的BlendShapes，通过潜在姿势增强面部细节表现，提供稳定逼真的渲染视频。大量的实验结果表明，GaussianTalker在说话头合成方面优于现有的最先进的方法，提供了精确的嘴唇同步和卓越的视觉质量。我们的方法在NVIDIA RTX4090 GPU上实现了130 FPS的渲染速度，大大超过了实时渲染性能的阈值，并有可能部署在其他硬件平台上。 et.al.|[2404.14037](http://arxiv.org/abs/2404.14037)|null|
|**2024-04-13**|**THQA: A Perceptual Quality Assessment Database for Talking Heads**|在媒体技术领域，由于计算机技术的快速发展，数字人已经变得突出。然而，大多数数字人所需的手动建模和控制对高效开发构成了重大障碍。语音驱动方法为操纵数字人类的嘴形和表情提供了一条新途径。尽管驾驶方法激增，但许多生成的说话头（TH）视频的质量仍然是一个问题，影响了用户的视觉体验。为了解决这个问题，本文介绍了Talking Head质量评估（THQA）数据库，该数据库包含通过8种不同的语音驱动方法生成的800个TH视频。大量实验证实了THQA数据库在字符和语音特征方面的丰富性。随后的主观质量评估实验分析了评分结果与语音驱动方法、年龄和性别之间的相关性。此外，实验结果表明，主流图像和视频质量评估方法对THQA数据库存在局限性，强调了进一步研究以提高TH视频质量评估的必要性。THQA数据库可在以下网址公开访问https://github.com/zyj-2000/THQA. et.al.|[2404.09003](http://arxiv.org/abs/2404.09003)|**[link](https://github.com/zyj-2000/thqa)**|
|**2024-04-07**|**GvT: A Graph-based Vision Transformer with Talking-Heads Utilizing Sparsity, Trained from Scratch on Small Datasets**|视觉变换器（ViTs）在大规模图像分类中取得了令人印象深刻的结果。然而，当在小数据集上从头开始训练时，ViT和卷积神经网络（CNN）之间仍然存在显著的性能差距，这归因于缺乏归纳偏差。为了解决这个问题，我们提出了一种基于图的视觉变换器（GvT），它利用了图卷积投影和图池。在每个块中，查询和关键字是通过基于空间邻接矩阵的图卷积投影来计算的，而点积注意力则用于另一个图卷积来生成值。当使用更多的注意力头时，查询和键的维数会降低，使它们的点积成为一个无信息的匹配函数。为了克服注意力低阶瓶颈，我们采用了基于双线性混合特征和稀疏选择注意力张量的说话头技术。这允许过滤后的注意力得分之间的交互，并使每个注意力机制都依赖于所有查询和关键字。此外，我们在两个中间块之间应用图池，以减少令牌数量并更有效地聚合语义信息。我们的实验结果表明，GvT产生了与深度卷积网络相当或更优的结果，并且在没有对大型数据集进行预训练的情况下超越了视觉变换器。我们提出的模型的代码可以在网站上公开获得。 et.al.|[2404.04924](http://arxiv.org/abs/2404.04924)|null|
|**2024-04-02**|**EDTalk: Efficient Disentanglement for Emotional Talking Head Synthesis**|实现对多个面部动作的解耦控制并适应不同的输入方式，大大增强了会说话的一代的应用和娱乐性。这需要深入探索面部特征的解耦空间，确保它们a）独立运行而不相互干扰，b）可以保留以与不同的模态输入共享，这两个方面在现有方法中经常被忽视。为了解决这一差距，本文提出了一种新的用于说话头生成的高效去纠缠框架（EDTalk）。我们的框架允许根据视频或音频输入对嘴形、头部姿势和情绪表达进行单独操纵。具体来说，我们使用三个轻量级模块将面部动态分解为三个不同的潜在空间，分别表示嘴巴、姿势和表情。每个空间都有一组可学习的基，其线性组合定义了特定的运动。为了确保独立性并加快训练速度，我们加强了基地之间的正交性，并设计了一种有效的训练策略，在不依赖外部知识的情况下将运动责任分配给每个空间。然后将学习到的库存储在相应的库中，从而实现具有音频输入的共享视觉先验。此外，考虑到每个空间的特性，我们提出了一种用于音频驱动的说话头合成的音频到运动模块。实验证明了EDTalk的有效性。我们建议您查看项目网站：https://tanshuai0219.github.io/EDTalk/ et.al.|[2404.01647](http://arxiv.org/abs/2404.01647)|null|
|**2024-03-28**|**MoDiTalker: Motion-Disentangled Diffusion Model for High-Fidelity Talking Head Generation**|传统的基于GAN的说话头生成模型往往质量有限，训练不稳定。最近基于扩散模型的方法旨在解决这些局限性并提高保真度。然而，它们仍然面临着挑战，包括广泛的采样时间和由于扩散模型的高度随机性而难以保持时间一致性。为了克服这些挑战，我们提出了一种新的用于高质量说话头生成的运动解纠缠扩散模型，称为MoDiTalker。我们介绍了两个模块：音频到运动（AToM），旨在从音频生成同步的嘴唇运动，以及运动到视频（MToV），设计用于根据生成的运动生成高质量的头部视频。AToM擅长通过利用音频注意力机制捕捉微妙的嘴唇动作。此外，MToV通过利用高效的三平面表示来增强时间一致性。我们在标准基准上进行的实验表明，与现有模型相比，我们的模型具有更优的性能。我们还提供全面的消融研究和用户研究结果。 et.al.|[2403.19144](http://arxiv.org/abs/2403.19144)|**[link](https://github.com/KU-CVLAB/MoDiTalker)**|
|**2024-03-23**|**Adaptive Super Resolution For One-Shot Talking-Head Generation**|单镜头说话头生成学习在相同或不同身份视频的驱动下，将说话头视频与一个源肖像图像合成。通常，这些方法需要通过雅可比矩阵或面部图像扭曲进行基于平面的像素变换，以生成新的姿势。使用单个图像源和像素位移的限制通常会影响合成图像的清晰度。一些方法试图通过引入额外的超分辨率模块来提高合成视频的质量，但这无疑会增加计算消耗并破坏原始数据分布。在这项工作中，我们提出了一种自适应的高质量说话头视频生成方法，该方法在没有额外预训练模块的情况下合成高分辨率视频。具体来说，受现有超分辨率方法的启发，我们对单镜头源图像进行下采样，然后通过编码器-解码器模块自适应地重建高频细节，从而提高了视频清晰度。我们的方法通过一种简单而有效的策略，不断提高生成视频的质量，并得到定量和定性评估的证实。代码和演示视频可在以下网址获得：\url{https://github.com/Songluchuan/AdaSR-TalkingHead/}. et.al.|[2403.15944](http://arxiv.org/abs/2403.15944)|**[link](https://github.com/songluchuan/adasr-talkinghead)**|
|**2024-09-11**|**EmoVOCA: Speech-Driven Emotional 3D Talking Heads**|近年来，3D对话头生成领域取得了重大进展。该领域的一个显著挑战在于将语音相关运动与表情动态相结合，这主要是由于缺乏将口语句子的多样性与各种面部表情相结合的全面3D数据集造成的。尽管文献工作试图利用2D视频数据和参数化3D模型作为解决方法，但在联合建模这两种运动时，这些方法仍然存在局限性。在这项工作中，我们从不同的角度解决了这个问题，并提出了一种创新的数据驱动技术，用于创建一个名为EmoVOCA的合成数据集，该数据集是通过组合一组无表情的3D说话头和一组3D表情序列获得的。为了展示这种方法的优点和数据集的质量，我们设计并训练了一个情感3D说话头生成器，该生成器接受3D面部、音频文件、情感标签和强度值作为输入，并学习用面部的表现特征来动画化音频同步的嘴唇动作。与文献中表现最佳的方法相比，使用我们的数据和生成器证据进行定量和定性综合实验，在合成令人信服的动画方面具有更高的能力。我们的代码和预训练模型将可用。 et.al.|[2403.12886](http://arxiv.org/abs/2403.12886)|null|
|**2024-09-25**|**ScanTalk: 3D Talking Heads from Unregistered Scans**|语音驱动的3D对话头生成已成为研究人员感兴趣的一个重要领域，带来了许多挑战。现有的方法受到具有固定拓扑的面动画的约束，其中建立了逐点对应关系，并且点的数量和顺序在模型可以动画化的所有身份中保持一致。在这项工作中，我们提出了\textbf{ScanTalk}，这是一个能够在包括扫描数据在内的任意拓扑中为3D人脸设置动画的新框架。我们的方法依赖于DiffusionNet架构来克服固定的拓扑约束，为更灵活、更逼真的3D动画提供了有前景的途径。通过利用DiffusionNet的强大功能，ScanTalk不仅可以适应不同的面部结构，而且在处理扫描数据时还可以保持保真度，从而增强生成的3D对话头的真实性和多功能性。通过与最先进的方法进行全面比较，我们验证了我们的方法的有效性，证明了它能够产生与现有技术相当的真实对话头。虽然我们的主要目标是开发一种不受拓扑约束的通用方法，但所有最先进的方法都受到这些限制的约束。用于复制我们结果的代码和预训练模型可在以下网址获得https://github.com/miccunifi/ScanTalk . et.al.|[2403.10942](http://arxiv.org/abs/2403.10942)|**[link](https://github.com/miccunifi/scantalk)**|

<p align=right>(<a href=#updated-on-20241003>back to top</a>)</p>

[contributors-shield]: https://img.shields.io/github/contributors/Vincentqyw/cv-arxiv-daily.svg?style=for-the-badge
[contributors-url]: https://github.com/Vincentqyw/cv-arxiv-daily/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/Vincentqyw/cv-arxiv-daily.svg?style=for-the-badge
[forks-url]: https://github.com/Vincentqyw/cv-arxiv-daily/network/members
[stars-shield]: https://img.shields.io/github/stars/Vincentqyw/cv-arxiv-daily.svg?style=for-the-badge
[stars-url]: https://github.com/Vincentqyw/cv-arxiv-daily/stargazers
[issues-shield]: https://img.shields.io/github/issues/Vincentqyw/cv-arxiv-daily.svg?style=for-the-badge
[issues-url]: https://github.com/Vincentqyw/cv-arxiv-daily/issues

