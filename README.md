[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]

## Updated on 2024.03.17
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
|**2023-11-29**|**SyncTalk: The Devil is in the Synchronization for Talking Head Synthesis**|在逼真的、语音驱动的谈话头部视频的合成中实现高度同步是一个重大挑战。传统的生成对抗性网络（GAN）难以保持一致的面部身份，而神经辐射场（NeRF）方法虽然可以解决这个问题，但往往会产生不匹配的嘴唇动作、不恰当的面部表情和不稳定的头部姿势。一个栩栩如生的会说话的头需要主体身份、嘴唇动作、面部表情和头部姿势的同步协调。缺乏这些同步是一个根本缺陷，导致了不切实际和人为的结果。为了解决同步这一关键问题，我们引入了SyncTalk，它被认为是创建逼真谈话头的“魔鬼”。这种基于NeRF的方法有效地保持了主体身份，增强了说话头部合成的同步性和真实性。SyncTalk采用面部同步控制器将嘴唇运动与语音对齐，并创新性地使用3D面部混合形状模型来捕捉准确的面部表情。我们的头部同步稳定器可优化头部姿势，实现更自然的头部运动。肖像同步生成器恢复头发细节，并将生成的头部与躯干融合，以获得无缝的视觉体验。大量的实验和用户研究表明，SyncTalk在同步和逼真度方面优于最先进的方法。我们建议观看补充视频：https://ziqiaopeng.github.io/synctalk et.al.|[2311.17590](http://arxiv.org/abs/2311.17590)|**[link](https://github.com/ZiqiaoPeng/SyncTalk)**|
|**2023-11-30**|**Talking Head(?) Anime from a Single Image 4: Improved Model and Its Distillation**|我们研究了创建一个可以从动画角色的单个图像实时控制的角色模型的问题。这个问题的解决方案将大大降低创建化身、计算机游戏和其他交互式应用程序的成本。Talking Head Anime 3（THA3）是一个开源项目，试图直接解决这个问题。它采用（1）动画角色上身的图像和（2）45维姿势矢量作为输入，并输出采用指定姿势的同一角色的新图像。可能的动作范围对于个人化身和某些类型的游戏角色来说足够有表现力。然而，该系统太慢，无法在普通PC上实时生成动画，并且其图像质量可以提高。在本文中，我们从两个方面改进THA3。首先，我们提出了新的组成网络架构，该架构基于U-Nets旋转角色的头部和身体，并在现代生成模型中广泛使用。新的架构始终产生比THA3基线更好的图像质量。尽管如此，它们也会使整个系统慢得多：生成一帧需要150毫秒。其次，我们提出了一种技术，将系统提取到一个小型网络（小于2MB）中，该网络可以使用消费者游戏GPU实时生成512x512个动画帧（低于30FPS），同时保持接近整个系统的图像质量。这一改进使整个系统在实时应用中具有实用性。 et.al.|[2311.17409](http://arxiv.org/abs/2311.17409)|null|
|**2023-11-28**|**THInImg: Cross-modal Steganography for Presenting Talking Heads in Images**|跨模态隐写术是在公开可用的覆盖信号（不同于秘密信号的模态）中不引人注目地隐藏秘密信号的实践。虽然以前的方法主要集中在隐藏相对少量的信息，但我们提出了THInImg，它通过利用人脸的特性，成功地将冗长的音频数据隐藏在身份图像中（并随后解码会说话的头部视频），可以有效地用于秘密通信、传输和版权保护。THInImg由两部分组成：编码器和解码器。在编码器-解码器流水线内部，我们引入了一种新的架构，该架构大大提高了在图像中隐藏音频的能力。此外，我们的框架可以扩展到迭代地将多个音频片段隐藏到身份图像中，从而提供对权限的多级控制。我们进行了广泛的实验来证明我们的方法的有效性，证明THInImg可以在160x160分辨率的身份图像中呈现长达80秒的高质量谈话头部视频（包括音频）。 et.al.|[2311.17177](http://arxiv.org/abs/2311.17177)|null|
|**2023-11-05**|**3D-Aware Talking-Head Video Motion Transfer**|会说话的头部视频的运动转移涉及生成具有主题视频的外观和驾驶视频的运动模式的新视频。当前的方法主要依赖于有限数量的主题图像和2D表示，从而忽略了充分利用主题视频中固有的多视图外观特征。在本文中，我们提出了一种新的3D感知会说话的头部视频运动传输网络Head3D，该网络通过递归网络从2D主题帧生成可视觉解释的3D规范头部，充分利用主题外观信息。我们方法的一个关键组成部分是自监督的3D头部几何学习模块，设计用于从2D主题视频帧预测头部姿势和深度图。该模块便于在规范空间中估计3D头部，然后可以对其进行变换以与驱动视频帧对准。此外，我们使用基于注意力的融合网络将主题帧的背景和其他细节与3D主题头部相结合，以产生合成目标视频。我们在两个公开演讲的头部视频数据集上进行的广泛实验表明，Head3D在实际的交叉身份设置中优于2D和3D现有技术，有证据表明它可以很容易地适应姿势可控的新型视图合成任务。 et.al.|[2311.02549](http://arxiv.org/abs/2311.02549)|null|
|**2023-11-02**|**LaughTalk: Expressive 3D Talking Head Generation with Laughter**|笑是一种独特的表达方式，对人类积极的社会互动至关重要。尽管目前的3D会说话的头部生成方法产生了令人信服的语言表达，但它们往往无法捕捉到笑声和微笑的活力和微妙之处，尽管它们在社会环境中很重要。在本文中，我们介绍了一项新任务，即生成既能清晰表达语音又能真实大笑的3D会说话的头。我们新策划的数据集包括2D大笑视频，以及伪注释和人工验证的3D FLAME参数和顶点。给定我们提出的数据集，我们提出了一个具有两阶段训练方案的强基线：模型首先学习说话，然后获得表达笑声的能力。大量实验表明，与现有方法相比，我们的方法在说话头部生成和表达笑声信号方面都表现良好。在我们提出的装配逼真化身的方法的基础上，我们进一步探索了潜在的应用。 et.al.|[2311.00994](http://arxiv.org/abs/2311.00994)|null|
|**2023-10-08**|**GestSync: Determining who is speaking without a talking head**|在本文中，我们介绍了一种新的同步任务，手势同步：确定一个人的手势是否与他们的语音相关。与嘴唇同步相比，手势同步更具挑战性，因为声音和身体运动之间的关系远比声音和嘴唇运动之间的松散。我们为这项任务引入了一个双编码器模型，并比较了许多输入表示，包括RGB帧、关键点图像和关键点矢量，评估了它们的性能和优势。我们证明了该模型可以单独使用自监督学习进行训练，并在LRS3数据集上评估其性能。最后，我们展示了手势同步在视听同步中的应用，以及在不看脸的情况下确定谁是人群中的演讲者。代码、数据集和预训练模型可在以下位置找到：\url{https://www.robots.ox.ac.uk/~vgg/research/gestsync}。 et.al.|[2310.05304](http://arxiv.org/abs/2310.05304)|**[link](https://github.com/Sindhu-Hegde/gestsync)**|
|**2023-09-28**|**OSM-Net: One-to-Many One-shot Talking Head Generation with Spontaneous Head Motions**|一次性会说话的头部生成没有明确的头部运动参考，因此很难生成具有头部运动的会说话的头。现有的一些作品只对嘴部区域进行编辑，生成静止的会说话的头，导致会说话的头部表现不真实。其他作品在音频信号和头部运动序列之间构建了一对一的映射，将模糊对应引入到映射中，因为当人们说出相同的内容时，头部运动中的行为可能不同。这种不合理的映射形式无法对多样性进行建模，并产生几乎静态甚至夸张的头部运动，这是不自然和奇怪的。因此，一次性会说话的头部生成任务实际上是一个一对多的不适定问题，人们在说话时会出现不同的头部运动。基于上述观察，我们提出了OSM-Net，这是一个具有自然头部运动的一对多的一次性谈话头部生成网络。OSM-Net构建了一个包含丰富多样的剪辑级头部运动特征的运动空间。空间的每个基础都代表了剪辑中有意义的头部运动的特征，而不仅仅是一帧，从而在说话的头部中提供了更连贯、更自然的运动变化。将驾驶音频映射到运动空间中，可以在合理的范围内对运动空间周围的各种运动特征进行采样，以实现一对多映射。此外，地标约束和时间窗口特征输入提高了表情特征提取和视频生成的准确性。大量实验表明，与其他方法相比，OSM-Net在合理的一对多映射范式下生成了更自然、逼真的头部运动。 et.al.|[2309.16148](http://arxiv.org/abs/2309.16148)|null|
|**2023-10-12**|**Efficient Emotional Adaptation for Audio-Driven Talking-Head Generation**|音频驱动的会说话的头部合成是虚拟人相关应用的热门研究课题。然而，现有方法的灵活性和低效性是显著的局限性，需要昂贵的端到端训练来将情绪从指导视频转移到会说话的头部预测。在这项工作中，我们提出了音频驱动的谈话头部的情绪自适应（EAT）方法，该方法通过参数有效自适应，以经济高效的方式将情绪不可知的谈话头部模型转换为情绪可控的模型。我们的方法利用了一个预先训练的与情绪无关的谈话头部转换器，并从不同的角度引入了三种轻量级的适应（深度情绪提示、情绪变形网络和情绪适应模块），以实现精确而现实的情绪控制。我们的实验表明，我们的方法在广泛使用的基准测试上实现了最先进的性能，包括LRW和MEAD。此外，即使在情感训练视频稀少或不存在的情况下，我们的参数有效自适应也表现出显著的泛化能力。项目网站：https://yuangan.github.io/eat/ et.al.|[2309.04946](http://arxiv.org/abs/2309.04946)|**[link](https://github.com/yuangan/eat_code)**|
|**2023-08-30**|**From Pixels to Portraits: A Comprehensive Survey of Talking Head Generation Techniques and Applications**|深度学习和计算机视觉的最新进展导致了人们对生成逼真的会说话的大脑的兴趣激增。本文对最先进的谈话头生成方法进行了全面的综述。我们系统地将其分为四种主要方法：图像驱动、音频驱动、视频驱动和其他方法（包括神经辐射场（NeRF）和基于3D的方法）。我们对每种方法进行了深入分析，强调了它们的独特贡献、优势和局限性。此外，我们彻底比较了公开可用的模型，并在关键方面对其进行了评估，如推理时间和生成输出的人工评分质量。我们的目标是对当前谈话型头部生成的前景进行清晰简洁的概述，阐明不同方法之间的关系，并为未来的研究确定有希望的方向。这项调查将为对这一快速发展的领域感兴趣的研究人员和从业者提供宝贵的参考。 et.al.|[2308.16041](http://arxiv.org/abs/2308.16041)|null|
|**2023-08-12**|**Text-to-Video: a Two-stage Framework for Zero-shot Identity-agnostic Talking-head Generation**|ChatGPT的出现引入了信息收集和分析的创新方法。然而，ChatGPT提供的信息仅限于文本，这些信息的可视化仍然受到限制。先前的研究探索了将文本转换为视频的零样本文本到视频（TTV）方法。然而，这些方法缺乏对生成音频的身份的控制，即不是身份不可知的，阻碍了它们的有效性。为了解决这一限制，我们提出了一个新的两阶段框架，用于不可知人的视频克隆，特别关注TTV的生成。在第一阶段，我们利用预先训练的零样本模型来实现文本到速度（TTS）的转换。在第二阶段中，采用音频驱动的谈话头生成方法来生成具有第一阶段中生成的音频特权的引人注目的视频。本文对不同的TTS和音频驱动的谈话头生成方法进行了比较分析，确定了未来最有前途的研究和开发方法。可以在以下链接中找到一些音频和视频示例：https://github.com/ZhichaoWang970201/Text-to-Video/tree/main. et.al.|[2308.06457](http://arxiv.org/abs/2308.06457)|**[link](https://github.com/zhichaowang970201/text-to-video)**|
|**2023-09-20**|**Context-Aware Talking-Head Video Editing**|Talking head视频编辑旨在通过文本转录编辑器有效地插入、删除和替换预先录制的视频中的单词。这项任务的关键挑战是获得一种编辑模型，该模型生成新的会说话的头部视频片段，该视频片段同时具有精确的嘴唇同步和运动平滑度。以前的方法，包括基于3DMM的（3D变形模型）方法和基于NeRF的（神经辐射场）方法，都是次优的，因为它们要么需要几分钟的源视频和几天的训练时间，要么缺乏对视频剪辑插入的语言（如嘴唇运动）和非语言（如头部姿势和表情）表示的复杂控制。在这项工作中，我们充分利用视频上下文来设计一种新的谈话式头部视频编辑框架，该框架实现了效率、解纠缠的运动控制和顺序平滑。具体来说，我们将该框架分解为运动预测和运动条件渲染：（1）我们首先设计了一个动画预测模块，该模块可以有效地获得基于驱动语音的平滑和唇同步运动序列。该模块采用非自回归网络来获取上下文先验，提高预测效率，并从多身份视频数据集中学习具有更好泛化能力的语音动画映射先验。（2） 然后，在给定预测的运动序列的情况下，我们引入了一个神经渲染模块来合成照片逼真度和全头视频帧。该模块采用预先训练的头部拓扑，仅使用少量帧进行有效微调，以获得特定于个人的渲染模型。大量实验表明，与以前的方法相比，我们的方法使用更少的数据，以更高的图像质量和嘴唇精度有效地实现了更平滑的编辑结果。 et.al.|[2308.00462](http://arxiv.org/abs/2308.00462)|null|
|**2023-08-18**|**Implicit Identity Representation Conditioned Memory Compensation Network for Talking Head video Generation**|Talking head视频生成旨在使用从目标驾驶视频中获得的运动信息，在静止图像中以动态姿势和表情对人脸进行动画化，同时在源图像中保持人的身份。然而，驾驶视频中剧烈而复杂的运动会导致模糊的生成，因为静止源图像无法为遮挡区域或微妙的表情变化提供足够的外观信息，这会产生严重的伪影并显著降低生成质量。为了解决这个问题，我们建议学习一个全局面部表示空间，并设计一个新的隐式身份表示条件记忆补偿网络，称为MCNet，用于高保真谈话头部生成~具体来说，我们设计了一个网络模块，从所有训练样本中学习统一的空间面部元记忆库，该模块可以提供丰富的面部结构和外观先验，以补偿生成时扭曲的源面部特征。此外，我们提出了一种基于从源图像的离散关键点学习的隐式身份表示的有效查询机制。它可以极大地促进从存储器库中检索更多相关信息以进行补偿。大量实验表明，MCNet可以学习具有代表性和互补性的面部记忆，并且在VoxCeleb1和CelebV数据集上明显优于以前最先进的会说话的头部生成方法。请查看我们的\href{https://github.com/harlanhong/ICCV2023-MCNET项目 et.al.|[2307.09906](http://arxiv.org/abs/2307.09906)|**[link](https://github.com/harlanhong/iccv2023-mcnet)**|
|**2023-07-04**|**A Comprehensive Multi-scale Approach for Speech and Dynamics Synchrony in Talking Head Generation**|使用语音输入信号用深度生成模型对静止人脸图像进行动画制作是一个活跃的研究课题，并且最近取得了重要进展。然而，大部分精力都放在了假唱和渲染质量上，而自然头部运动的产生，更不用说头部运动和语音之间的视听相关性了，却经常被忽视。在这项工作中，我们提出了多尺度视听同步损失和多尺度自回归GAN，以更好地处理语音与头部和嘴唇动态之间的短期和长期相关性。特别是，我们在多模式输入金字塔上训练一堆同步器模型，并在多尺度生成器网络中使用这些模型作为指导，以产生在不同时间尺度上展开的音频对齐运动。我们的生成器在面部标志域中运行，这是一种标准的低维头部表示。实验表明，在标志域和图像域中，头部运动动力学质量和多尺度视听同步性都比现有技术有了显著改进。 et.al.|[2307.03270](http://arxiv.org/abs/2307.03270)|**[link](https://github.com/louisbearing/hmo-audio)**|
|**2023-06-06**|**Emotional Talking Head Generation based on Memory-Sharing and Attention-Augmented Networks**|给定音频片段和参考人脸图像，会说话的头部生成的目标是生成高保真度的会说话的头视频。尽管一些音频驱动的头部视频生成方法在过去已经取得了一些成就，但它们大多只关注嘴唇和音频同步，缺乏再现目标人物面部表情的能力。为此，我们提出了一种由记忆共享情感特征提取器（MSEF）和基于U-net的注意力增强翻译器（AATU）组成的谈话头生成模型。首先，MSEF可以从音频中提取隐含的情感辅助特征，以估计更准确的情感人脸标志~其次，AATU充当估计的地标和照片逼真视频帧之间的翻译器。大量的定性和定量实验表明，该方法优于以往的工作。代码将公开。 et.al.|[2306.03594](http://arxiv.org/abs/2306.03594)|null|
|**2023-07-26**|**Learning Landmarks Motion from Speech for Speaker-Agnostic 3D Talking Heads Generation**|本文提出了一种从原始音频输入生成3D谈话头的新方法。我们的方法基于这样一种想法，即语音相关的运动可以通过位于面部可移动部分（即地标）上的几个控制点的运动来全面有效地描述。下面的肌肉骨骼结构使我们能够了解它们的运动如何影响整个面部的几何变形。为此，所提出的方法采用了两个不同的模型：第一个模型学习从给定的音频中生成稀疏的地标集的运动。第二个模型将这样的地标运动扩展到密集运动场，该密集运动场用于在中性状态下对给定的3D网格进行动画制作。此外，我们引入了一种新的损失函数，称为余弦损失，它使生成的运动矢量和地面实况矢量之间的角度最小化。在3D谈话头生成中使用地标提供了各种优势，如一致性、可靠性和无需手动注释。我们的方法是不受身份限制的，为任何用户提供高质量的面部动画，而无需额外的数据或培训。 et.al.|[2306.01415](http://arxiv.org/abs/2306.01415)|**[link](https://github.com/fedenoce/s2l-s2d)**|
|**2023-05-17**|**LPMM: Intuitive Pose Control for Neural Talking-Head Model via Landmark-Parameter Morphable Model**|虽然目前的会说话的头部模型能够生成逼真的会说话视频，但它们提供的姿势可控性有限。大多数方法都需要特定的视频序列，这些视频序列应该准确地包含所需的头部姿势，而不是用户友好的姿势控制。三维可变形模型（3DMM）提供语义姿势控制，但无法捕捉某些表情。我们提出了一种新的方法，该方法在预先训练的神经会说话的头部模型上利用头部方向和面部表情的参数控制。为了实现这一点，我们引入了一个地标参数可变形模型（LPMM），该模型通过一组语义参数提供对面部地标域的控制。使用LPMM，可以调整特定的头部姿势因素，而不会扭曲其他面部属性。结果表明，我们的方法对神经会说话的头部模型提供了直观的钻机式控制，允许基于参数和图像的输入。 et.al.|[2305.10456](http://arxiv.org/abs/2305.10456)|null|
|**2023-12-10**|**DaGAN++: Depth-Aware Generative Adversarial Network for Talking Head Video Generation**|在会说话的头部生成方面的主要技术在很大程度上取决于2D信息，包括来自输入面部图像的面部外观和运动。然而，密集的3D面部几何结构，如逐像素深度，在构建准确的3D面部结构和抑制复杂的背景噪声以进行生成方面发挥着关键作用。然而，面部视频的密集3D注释的获取成本高得令人望而却步。在这项工作中，首先，我们提出了一种新的自监督方法，用于从人脸视频中学习密集的3D人脸几何（即深度），而不需要在训练中使用相机参数和3D几何注释。我们进一步提出了一种学习像素级不确定性的策略，以感知用于几何学习的更可靠的刚性运动像素。其次，我们设计了一个有效的几何引导的面部关键点估计模块，为生成运动场提供了准确的关键点。最后，我们开发了一种3D感知的跨模态（即外观和深度）注意力机制，该机制可以应用于每个生成层，以从粗到细的方式捕捉面部几何形状。在三个具有挑战性的基准（即VoxCeleb1、VoxCeleb2和HDTF）上进行了广泛的实验。结果表明，我们提出的框架可以生成看起来高度逼真的重演谈话视频，并在这些基准上建立新的最先进的性能。代码和经过训练的模型可在GitHub项目页面上公开获取，网址为https://github.com/harlanhong/CVPR2022-DaGAN et.al.|[2305.06225](http://arxiv.org/abs/2305.06225)|**[link](https://github.com/harlanhong/cvpr2022-dagan)**|
|**2023-09-12**|**Avatar Fingerprinting for Authorized Use of Synthetic Talking-Head Videos**|现代生成器以令人印象深刻的真实感渲染会说话的头部视频，在带宽预算有限的情况下带来新的用户体验，如视频会议。然而，它们的安全采用需要一种机制来验证渲染的视频是否可信。例如，对于视频会议，我们必须确定合成视频肖像未经个人同意使用其外观的情况。我们将此任务称为“化身指纹”。具体来说，我们学习了一种嵌入，其中一个身份的运动特征被分组在一起，并被推离其他身份的运动签名。这使我们能够将合成视频与驱动视频中表情的身份联系起来，而不管所显示的面部外观如何。随着会说话的头部生成器变得越来越普遍，而且还没有大规模的数据集来完成这项新任务，头像指纹识别算法将是至关重要的。因此，我们贡献了一个庞大的数据集，由人们提供脚本化和即兴创作的短独白，并配以合成视频，在合成视频中，我们使用另一个人的面部表情来渲染一个人的视频。项目页面：https://research.nvidia.com/labs/nxp/avatar-fingerprinting/. et.al.|[2305.03713](http://arxiv.org/abs/2305.03713)|null|
|**2023-04-25**|**AudioGPT: Understanding and Generating Speech, Music, Sound, and Talking Head**|大型语言模型（LLM）在各种领域和任务中表现出了非凡的能力，挑战了我们对学习和认知的理解。尽管最近取得了成功，但目前的LLM无法处理复杂的音频信息或进行口语对话（如Siri或Alexa）。在这项工作中，我们提出了一个名为AudioGPT的多模式人工智能系统，它用1）基础模型来补充LLM（即ChatGPT），以处理复杂的音频信息并解决大量的理解和生成任务；以及2）支持口语对话的输入/输出接口（ASR、TTS）。随着对评估人类意图理解和与基础模型合作的多模式LLM的需求不断增加，我们概述了原理和过程，并测试了AudioGPT的一致性、能力和稳健性。实验结果证明了AudioGPT在多轮对话中通过语音、音乐、声音和会说话的头部理解和生成来解决人工智能任务的能力，这使人类能够以前所未有的轻松创建丰富多样的音频内容。我们的系统可在\url上公开获取{https://github.com/AIGC-Audio/AudioGPT}. et.al.|[2304.12995](http://arxiv.org/abs/2304.12995)|**[link](https://github.com/aigc-audio/audiogpt)**|
|**2023-11-02**|**High-Fidelity and Freely Controllable Talking Head Video Generation**|会说话的头部生成是基于给定的源身份和目标运动来生成视频。然而，当前的方法面临着一些挑战，这些挑战限制了所生成视频的质量和可控性。首先，生成的面通常会出现意外变形和严重扭曲。其次，驾驶图像没有明确地分解运动相关信息，如姿势和表情，这限制了在生成过程中对不同属性的操作。第三，由于相邻帧之间提取的地标的不一致性，生成的视频往往具有闪烁的伪影。在本文中，我们提出了一种新的模型，该模型可以生成高保真的会说话的头部视频，并可以自由控制头部姿势和表情。我们的方法利用自监督学习的地标和基于3D人脸模型的地标来对运动进行建模。我们还引入了一种新的运动感知多尺度特征对齐模块，以在没有人脸失真的情况下有效地传递运动。此外，我们还通过特征上下文自适应和传播模块来增强合成的头部视频的平滑度。我们在具有挑战性的数据集上评估我们的模型，并展示其最先进的性能。 et.al.|[2304.10168](http://arxiv.org/abs/2304.10168)|null|

<p align=right>(<a href=#updated-on-20240317>back to top</a>)</p>

[contributors-shield]: https://img.shields.io/github/contributors/Vincentqyw/cv-arxiv-daily.svg?style=for-the-badge
[contributors-url]: https://github.com/Vincentqyw/cv-arxiv-daily/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/Vincentqyw/cv-arxiv-daily.svg?style=for-the-badge
[forks-url]: https://github.com/Vincentqyw/cv-arxiv-daily/network/members
[stars-shield]: https://img.shields.io/github/stars/Vincentqyw/cv-arxiv-daily.svg?style=for-the-badge
[stars-url]: https://github.com/Vincentqyw/cv-arxiv-daily/stargazers
[issues-shield]: https://img.shields.io/github/issues/Vincentqyw/cv-arxiv-daily.svg?style=for-the-badge
[issues-url]: https://github.com/Vincentqyw/cv-arxiv-daily/issues

