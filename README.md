[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]

## Updated on 2023.12.01
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
|**2023-11-29**|**HUGS: Human Gaussian Splats**|神经渲染的最新进展已经将训练和渲染时间提高了几个数量级。虽然这些方法展示了最先进的质量和速度，但它们是为静态场景的摄影测量而设计的，不能很好地推广到环境中自由移动的人类。在这项工作中，我们介绍了人类高斯飞溅（HUGS），它表示可动画化的人类以及使用3D高斯飞溅（3DGS）的场景。我们的方法只拍摄一个具有少量（50-100）帧的单眼视频，它会自动学习在30分钟内解开静态场景和完全可动画化的人类化身。我们利用SMPL身体模型来初始化人类高斯。为了捕捉SMPL未建模的细节（如布料、头发），我们允许3D高斯与人体模型偏离。为动画人类使用3D高斯带来了新的挑战，包括在表达高斯时产生的人工制品。我们建议联合优化线性混合蒙皮权重，以协调动画过程中各个高斯人的运动。我们的方法实现了人类的新颖姿势合成和人类和场景的新颖视角合成。我们以60 FPS的渲染速度实现了最先进的渲染质量，同时比之前的工作快了约100倍。我们的代码将在此处公布：https://github.com/apple/ml-hugs et.al.|[2311.17910](http://arxiv.org/abs/2311.17910)|null|
|**2023-11-29**|**SODA: Bottleneck Diffusion Models for Representation Learning**|我们介绍了SODA，一种自监督扩散模型，用于表示学习。该模型包含一个图像编码器，该编码器将源视图提取为紧凑的表示，进而指导相关新视图的生成。我们表明，通过在编码器和去噪解码器之间施加严格的瓶颈，并利用新颖的视图合成作为自监督目标，我们可以将扩散模型转变为强表示学习器，能够以无监督的方式捕获视觉语义。据我们所知，SODA是第一个成功进行ImageNet线性探针分类的扩散模型，同时，它可以在广泛的数据集上完成重建、编辑和合成任务。进一步的研究揭示了其涌现的潜在空间的非纠缠性质，它是控制和操纵模型生成图像的有效接口。总之，我们的目标是揭示扩散模型令人兴奋和有前景的潜力，不仅用于图像生成，而且用于学习丰富和稳健的表示。 et.al.|[2311.17901](http://arxiv.org/abs/2311.17901)|null|
|**2023-11-29**|**Erasing the Ephemeral: Joint Camera Refinement and Transient Object Removal for Street View Synthesis**|综合城市环境的新颖视图对于自动驾驶和虚拟旅游等任务至关重要。与物体级或室内情况相比，室外设置带来了独特的挑战，例如由于移动的车辆和长序列中的相机姿态漂移而导致的帧间不一致。在本文中，我们介绍了一种方法来解决户外场景的视图合成方面的这些挑战。我们使用神经点光场场景表示，并战略性地检测和屏蔽动态对象，以重建没有伪影的新场景。此外，我们同时优化相机姿势和视图合成过程，因此，我们同时细化了这两个元素。通过在真实世界的城市数据集上进行验证，我们展示了合成城市场景新视图的最先进结果。 et.al.|[2311.17634](http://arxiv.org/abs/2311.17634)|null|
|**2023-11-28**|**ConTex-Human: Free-View Rendering of Human from a Single Image with Texture-Consistent Synthesis**|在这项工作中，我们提出了一种方法来解决以自由视图方式从单个图像渲染3D人体的挑战。一些现有的方法可以通过使用可推广的像素对齐隐式场来重建人类的纹理网格，或者通过使用2D扩散模型作为分数蒸馏采样（SDS）方法的指导，将2D图像提升到3D空间来实现这一点。然而，可推广的隐式场往往会导致纹理场过于平滑，而SDS方法往往会导致与输入图像的纹理不一致的新视图。在本文中，我们介绍了一个纹理一致的后视图合成模块，该模块可以通过深度和文本引导的注意力注入将参考图像内容转移到后视图。此外，为了减轻侧面区域中出现的颜色失真，我们提出了一种可见性感知的补丁一致性正则化方法，用于纹理映射和细化，并与合成的后视图纹理相结合。通过上述技术，我们可以从单个图像中实现高保真度和纹理一致的人类渲染。在真实数据和合成数据上进行的实验证明了我们方法的有效性，并表明我们的方法优于以前的基线方法。 et.al.|[2311.17123](http://arxiv.org/abs/2311.17123)|null|
|**2023-11-28**|**UC-NeRF: Neural Radiance Field for Under-Calibrated multi-view cameras in autonomous driving**|多摄像头设置广泛应用于各种应用，如自动驾驶，因为它们极大地扩展了传感功能。尽管神经辐射场（NeRF）技术发展迅速，并在室内和室外场景中得到了广泛应用，但将NeRF应用于多摄像机系统仍然极具挑战性。这主要是由于多摄像头设置中固有的校准不足问题，包括不同摄像头中单独校准的图像信号处理单元产生的不一致成像效果，以及驱动过程中影响相对摄像头姿态的机械振动产生的系统误差。在本文中，我们提出了UC-NeRF，这是一种新的方法，适用于校准不足的多视图相机系统中的新视图合成。首先，我们提出了一种基于层的颜色校正来校正不同图像区域中的颜色不一致。其次，我们提出了虚拟扭曲，以生成更多视点多样但颜色一致的虚拟视图，用于颜色校正和3D恢复。最后，设计了一种时空约束的姿态精化方法，用于多摄像机系统中更稳健、更准确的姿态校准。我们的方法不仅在多摄像机设置中实现了最先进的新视图合成性能，而且有效地促进了在具有合成新视图的大型户外场景中的深度估计。 et.al.|[2311.16945](http://arxiv.org/abs/2311.16945)|null|
|**2023-11-29**|**LiveNVS: Neural View Synthesis on Live RGB-D Streams**|现有的实时RGB-D重建方法，如Kinect Fusion，缺乏实时照片逼真的可视化。这是由于不完美的深度图和相机姿势融合了嘈杂、过度平滑或不完整的几何体和模糊的纹理。最近的神经渲染方法可以克服许多这样的伪影，但大多是针对离线使用进行优化的，这阻碍了集成到实时重建管道中。在本文中，我们介绍了LiveNVS，这是一个允许在实时RGB-D输入流上进行神经新视图合成的系统，具有非常低的延迟和实时渲染。基于RGB-D输入流，通过经由密集融合的深度图将神经特征投影到目标视图中并将图像空间中的特征聚合到目标特征图来渲染新视图。然后，可推广的神经网络将目标特征图转换为高质量的RGB图像。LiveNVS在捕捉过程中实现了未知场景的最先进的神经渲染质量，允许用户虚拟探索场景并实时评估重建质量。 et.al.|[2311.16668](http://arxiv.org/abs/2311.16668)|null|
|**2023-11-28**|**Rethinking Directional Integration in Neural Radiance Fields**|最近的工作使用神经辐射场（NeRF）进行多视图3D重建，在渲染真实感场景方面有了重大飞跃。然而，尽管NeRF具有功效，但与光场渲染或基于图像的视图合成相比，其学习视图相关效果的能力有限。为此，我们对NeRF渲染方程进行了修改，对于任何NeRF变化，只要更改几行代码即可，同时大大提高了视图相关效果的渲染质量。通过交换积分算子和方向解码器网络，我们只积分沿射线的位置特征，并将方向项移出积分，导致视图相关和独立分量的解纠缠。修正后的方程等效于理想情况下在具有狄拉克密度的物体表面上的经典体积渲染。此外，我们证明了在网络近似和数值积分引起的误差的情况下，与经典的NeRF相比，我们的渲染方程表现出更好的收敛性和更低的误差累积。我们还表明，修改后的方程可以解释为具有学习的光线嵌入的光场渲染。对不同NeRF变化的实验表明，通过我们的简单修改，视图相关效果的质量得到了一致的改善。 et.al.|[2311.16504](http://arxiv.org/abs/2311.16504)|null|
|**2023-11-27**|**Mip-Splatting: Alias-free 3D Gaussian Splatting**|最近，3D高斯散射已经展示了令人印象深刻的新颖视图合成结果，达到了高保真度和效率。然而，当改变采样率时，可以观察到强烈的伪影，例如通过改变焦距或相机距离。我们发现，这种现象的来源可以归因于缺乏3D频率约束和使用2D膨胀滤波器。为了解决这个问题，我们引入了一种3D平滑滤波器，该滤波器基于输入视图引起的最大采样频率来约束3D高斯基元的大小，消除放大时的高频伪影。此外，用模拟2D盒滤波器的2D Mip滤波器代替2D膨胀，有效地缓解了混叠和膨胀问题。我们的评估，包括在单尺度图像上的训练和在多尺度上的测试等场景，验证了我们方法的有效性。 et.al.|[2311.16493](http://arxiv.org/abs/2311.16493)|null|
|**2023-11-29**|**Animatable 3D Gaussian: Fast and High-Quality Reconstruction of Multiple Human Avatars**|神经辐射场能够重建高质量的可驾驶人类化身，但训练和渲染成本高昂。为了减少消耗，我们提出了可动画化的3D高斯，它从输入图像和姿势中学习人类化身。我们通过在规范空间中建模一组蒙皮的3D高斯和相应的骨架，并根据输入的姿势将3D高斯变形到姿势空间，将3D高斯扩展到动态人类场景。我们引入了哈希编码的形状和外观来加快训练，并提出了与时间相关的环境遮挡，以在包含复杂运动和动态阴影的场景中实现高质量的重建。在新的视图合成和新的姿态合成任务上，我们的方法在训练时间、渲染速度和重建质量方面都优于现有方法。我们的方法可以很容易地扩展到多人场景，并且只需25秒的训练就可以在10人的场景中获得可比的新颖视图合成结果。 et.al.|[2311.16482](http://arxiv.org/abs/2311.16482)|**[link](https://github.com/jimmyYliu/Animatable-3D-Gaussian)**|
|**2023-11-27**|**AerialBooth: Mutual Information Guidance for Text Controlled Aerial View Synthesis from a Single Image**|我们提出了一种新的方法，AerialBooth，用于使用其文本描述从单个输入图像合成鸟瞰图。我们利用预训练的文本到2D图像的稳定扩散模型作为3D世界的先验知识。该模型分两步进行微调，分别针对重建输入图像及其逆透视映射的文本嵌入和UNet进行优化。反向透视映射在扩散模型的文本图像空间内产生方差，同时为鸟瞰图合成提供弱指导。在推断时，我们使用新的相互信息引导将生成的图像的内容引向输入图像，该相互信息引导使两个图像的概率分布之间的信息内容最大化。我们在广泛的真实和合成数据上评估了我们的方法，包括自然场景、室内场景、人类行为等。通过广泛的实验和消融研究，我们证明了AerialBooth的有效性，以及它对其他文本控制视图的可推广性。我们还表明，AerialBooth通过对分析输入图像的视点和保真度的7个指标进行定量评估，实现了最佳的视点保真度权衡。代码和数据可在https://github.com/divyakraman/aerialbooth2023. et.al.|[2311.15478](http://arxiv.org/abs/2311.15478)|null|

<p align=right>(<a href=#updated-on-20231201>back to top</a>)</p>

## 3D Reconstruction

|Publish Date|Title|Abstract|PDF|Code|
|---|---|---|---|---|
|**2023-11-29**|**Volumetric Cloud Field Reconstruction**|云和雾等体积现象由于其半透明性质及其与光的复杂相互作用，给3D重建系统带来了重大挑战。重建散射体积的传统技术依赖于受控设置，限制了实际应用。本文介绍了一种从几个输入立体声对重建体积的方法。我们提出了一种新的深度学习框架，该框架将深度立体模型与3D卷积神经网络（3D CNN）和平流模块集成在一起，能够捕捉体积的形状和动力学。立体深度用于在体积周围雕刻空白空间，为3D CNN提供了应对输入视图不足的先验知识。对我们的输出进行细化后，平流模块利用了介质的时间演变，提供了一种推断运动和提高时间一致性的机制。我们的系统通过其从一组稀疏的立体图像对中估计大规模体积（在这种情况下是云）的密度和速度场的能力来证明其有效性。 et.al.|[2311.17657](http://arxiv.org/abs/2311.17657)|null|
|**2023-11-28**|**REF $^2$ -NeRF: Reflection and Refraction aware Neural Radiance Field**|最近，在研究使用隐式神经表示从多个图像进行3D重建的方法方面取得了重大进展，例如神经辐射场（NeRF）方法。这种基于体绘制的方法可以对各种光现象进行建模，并且已经提出了各种扩展方法来适应不同的场景和情况。然而，当处理具有多个玻璃对象的场景时，例如玻璃陈列柜中的对象，由于存在多重反射和折射效果，因此对目标场景进行准确建模一直是一项挑战。因此，本文提出了一种基于NeRF的玻璃外壳场景建模方法。在所提出的方法中，折射和反射是使用依赖和独立于观察者视角的元素来建模的。这种方法使我们能够估计发生折射的表面，即玻璃表面，并能够分离和建模直射光和反射光分量。与现有方法相比，所提出的方法能够对玻璃折射和整个场景进行更准确的建模。 et.al.|[2311.17116](http://arxiv.org/abs/2311.17116)|null|
|**2023-11-28**|**Improved Prototypical Semi-Supervised Learning with Foundation Models: Prototype Selection, Parametric vMF-SNE Pretraining and Multi-view Pseudolabelling**|在本文中，我们提出了一种改进的计算机视觉原型半监督学习方法，将冻结基础模型作为神经网络的主干。作为一种通用工具，我们提出了参数von Mises-Fisher随机邻域嵌入（vMF-SNE），以在保持局部结构的高维潜在空间之间创建具有神经网络的映射。这使我们能够使用vMF-SNE的基础模型的高质量嵌入来预训练网络的投影头。我们还提出了软多视图伪标签，其中与一致性或交换分配方法相比，跨多个视图的预测被组合以提供更可靠的监督信号。我们证明了这些想法在一系列基准数据集上改进了P｝预测支持样本视图分配（PAWS）（一种当前最先进的半监督学习方法）以及鲁棒PAWS（RoPAWS）。我们还介绍了简单的 $k$ -意味着原型选择，在这种情况下，这种技术比其他无监督标签选择方法提供了优越的性能。对于每类有四个标签的CIFAR-10和CIFAR-100，这些变化对PAWS的平均改善幅度分别为+2.9%和+5.7%，而DeepWeeds是一个对半监督学习特别具有挑战性的数据集，其改善幅度为+15.2%。在这种小标签制度下，我们在半监督学习中也取得了新的最先进的结果，CIFAR-10为95.8%（+0.7%），CIFAR-100为76.6%（+12.0%）。 et.al.|[2311.17093](http://arxiv.org/abs/2311.17093)|null|
|**2023-11-28**|**Multi-Scale 3D Gaussian Splatting for Anti-Aliased Rendering**|3D高斯最近已经成为3D重建和渲染的高效表示。尽管在高分辨率下渲染质量和速度都很高，但在较低分辨率或远离相机位置渲染时，它们都会急剧恶化。在低分辨率或远距离渲染期间，与每个飞溅的3D高斯的屏幕大小相比，图像的像素大小可能低于奈奎斯特频率，并导致混叠效应。渲染速度也会因每个像素上更多飞溅的高斯数的顺序alpha混合而大幅减慢。为了解决这些问题，我们提出了一种多尺度的3D高斯飞溅算法，该算法将高斯保持在不同的尺度来表示同一场景。使用更多的小高斯渲染高分辨率图像，使用更少的大高斯渲染低分辨率图像。在相似的训练时间下，与单尺度3D高斯飞溅相比，我们的算法在Mip-NeRF360数据集上以4 $\times$-128$\times$ 的尺度渲染可以实现13\%-66\%PSNR和160\%-240O\%的渲染速度提高。 et.al.|[2311.17089](http://arxiv.org/abs/2311.17089)|null|
|**2023-11-28**|**Surf-D: High-Quality Surface Generation for Arbitrary Topologies using Diffusion Models**|在本文中，我们提出了Surf-D，这是一种使用扩散模型将高质量的三维形状生成为具有任意拓扑的曲面的新方法。具体来说，我们采用无符号距离域（UDF）作为曲面表示，因为它擅长处理任意拓扑，从而能够生成复杂的形状。虽然先前的方法探索了使用不同表示的形状生成，但它们受到拓扑和几何细节的限制。此外，直接将先验扩散模型扩展到UDF是不平凡的，因为它们由于离散的体积结构而缺乏空间连续性。然而，UDF需要用于网格提取和学习的精确梯度。为了解决这些问题，我们首先利用基于点的自动编码器来学习紧凑的潜在空间，该空间支持通过微分对任何输入点进行梯度查询，以高分辨率有效地捕捉复杂的几何图形。由于各种形状的学习难度可能不同，因此采用课程学习策略来有效嵌入各种表面，从而增强整个嵌入过程。利用预先训练的形状潜在空间，我们采用潜在扩散模型来获取各种形状的分布。我们的方法在多个模态的形状生成方面表现出卓越的性能，并在无条件生成、类别条件生成、图像三维重建和文本到形状任务中进行了广泛的实验。 et.al.|[2311.17050](http://arxiv.org/abs/2311.17050)|null|
|**2023-11-28**|**Gradient-based Local Next-best-view Planning for Improved Perception of Targeted Plant Nodes**|机器人越来越多地被用于番茄温室，以自动化劳动密集型任务，如选择性收割和落叶。为了执行这些任务，机器人必须能够准确有效地感知需要切割的植物节点，尽管与其他植物部分的遮挡程度很高。我们将这个问题表述为局部次优视图（NBV）规划任务，其中机器人必须规划一组有效的相机视点，以克服遮挡并提高感知质量。我们的公式侧重于快速提高单个目标节点的感知准确性，以最大限度地提高其被切割的机会。以前的NBV规划方法大多侧重于全局视图规划，并使用候选视点的随机采样进行探索，这可能会导致计算成本高、候选较差导致的视图选择无效或采样效率低导致的轨迹不平滑。我们提出了一种使用差分射线采样的基于梯度的NBV规划器，该规划器直接估计视点规划的局部梯度方向，以克服遮挡并改善感知。通过仿真实验，我们表明，我们的规划器可以处理遮挡，并与基于采样的NBV规划器一样好地改进节点的3D重建和位置估计，同时减少10倍的计算，生成效率高出28%的轨迹。 et.al.|[2311.16759](http://arxiv.org/abs/2311.16759)|null|
|**2023-11-28**|**MultiCBR: Multi-view Contrastive Learning for Bundle Recommendation**|捆绑推荐旨在向用户推荐一系列相关项目，以提高用户体验和平台利润。现有的捆绑包推荐模型已经从只捕获用户捆绑包交互发展到对用户、捆绑包和项目之间的多个关系进行建模。特别是，CrossCBR将跨视角对比学习纳入了双视角偏好学习框架，显著提高了SOTA的性能。然而，它确实有两个局限性：1）两种观点的表述并没有充分利用用户、捆绑包和项目之间的所有异构关系；2）“早对比晚融合”框架在捕捉用户偏好方面效果较差，难以推广到多个视图。在本文中，我们提出了一种新的多视角对比学习框架MultiCBR，用于捆绑推荐。首先，我们设计了一个多视图表示学习框架，能够捕获所有的用户捆绑、用户项目和捆绑项目关系，特别是更好地利用捆绑项目隶属关系来增强稀疏捆绑的表示。其次，我们创新性地采用了“早期融合和后期对比”的设计，在进行自我监督的对比学习之前，首先融合多视图表示。与现有方法相比，我们的框架颠倒了融合和对比的顺序，引入了以下优势：1）我们的框架能够对跨视图和自我视图偏好进行建模，使我们能够实现增强的用户偏好建模；2）我们只需要两个自监督的对比损失，而不需要二次交叉视角对比损失，从而使额外成本最小化。在三个公共数据集上的实验结果表明，我们的方法优于SOTA方法。 et.al.|[2311.16751](http://arxiv.org/abs/2311.16751)|**[link](https://github.com/happypointer/multicbr)**|
|**2023-11-28**|**RGBGrasp: Image-based Object Grasping by Capturing Multiple Views during Robot Arm Movement with Neural Radiance Fields**|当涉及到抓取各种形状、材料和纹理的物体的复杂任务时，机器人研究遇到了一个重大障碍。与之前的许多研究严重依赖于专门的点云相机或丰富的RGB视觉数据来收集物体抓取任务的3D见解不同，本文引入了一种称为RGBGrasp的开创性方法。这种方法依赖于一组有限的RGB视图来感知包含透明和镜面对象的3D环境，并实现准确的抓取。我们的方法利用预先训练的深度预测模型来建立几何约束，即使在有限的视图条件下也能进行精确的3D结构估计。最后，我们集成了哈希编码和提议采样器策略，以显著加快3D重建过程。这些创新显著增强了我们的算法在现实场景中的适应性和有效性。通过全面的实验验证，我们证明RGBGrasp在广泛的物体抓取场景中取得了显著的成功，使其成为现实世界机器人操纵任务的一个有前途的解决方案。我们的方法演示可以在以下网站上找到：https://sites.google.com/view/rgbgrasp et.al.|[2311.16592](http://arxiv.org/abs/2311.16592)|null|
|**2023-11-28**|**Rethinking Directional Integration in Neural Radiance Fields**|最近的工作使用神经辐射场（NeRF）进行多视图3D重建，在渲染真实感场景方面有了重大飞跃。然而，尽管NeRF具有功效，但与光场渲染或基于图像的视图合成相比，其学习视图相关效果的能力有限。为此，我们对NeRF渲染方程进行了修改，对于任何NeRF变化，只要更改几行代码即可，同时大大提高了视图相关效果的渲染质量。通过交换积分算子和方向解码器网络，我们只积分沿射线的位置特征，并将方向项移出积分，导致视图相关和独立分量的解纠缠。修正后的方程等效于理想情况下在具有狄拉克密度的物体表面上的经典体积渲染。此外，我们证明了在网络近似和数值积分引起的误差的情况下，与经典的NeRF相比，我们的渲染方程表现出更好的收敛性和更低的误差累积。我们还表明，修改后的方程可以解释为具有学习的光线嵌入的光场渲染。对不同NeRF变化的实验表明，通过我们的简单修改，视图相关效果的质量得到了一致的改善。 et.al.|[2311.16504](http://arxiv.org/abs/2311.16504)|null|
|**2023-11-27**|**Weakly-Supervised 3D Reconstruction of Clothed Humans via Normal Maps**|我们提出了一种新的基于深度学习的方法，通过2D法线图使用弱监督对穿着衣服的人进行3D重建。给定单个RGB图像或多视图图像，我们的网络推断出在静止姿势下身体周围的四面体网格上离散的有符号距离函数（SDF）。随后，使用推断的姿势和相机参数从SDF生成法线贴图。我们方法的一个关键方面是使用Marching四面体从四面体网格上的SDF（唯一地）计算三角化表面，便于直接微分（从而反向传播）。因此，仅给定地面实况法线图（没有体积信息地面实况信息），我们可以训练网络从相应的RGB图像中产生SDF值。可选地，额外的多视角损失导致改善的结果。我们展示了我们的方法在网络推理和三维重建方面的有效性。 et.al.|[2311.16042](http://arxiv.org/abs/2311.16042)|null|

<p align=right>(<a href=#updated-on-20231201>back to top</a>)</p>

## Diffusion

|Publish Date|Title|Abstract|PDF|Code|
|---|---|---|---|---|
|**2023-11-30**|**Do text-free diffusion models learn discriminative visual representations?**|虽然许多无监督学习模型专注于一组任务，无论是生成性的还是判别性的，但我们探索了统一表示学习器的可能性：一个同时处理两组任务的模型。我们将扩散模型（一种最先进的生成任务方法）确定为主要候选者。这样的模型包括训练U-Net以迭代地预测和去除噪声，并且所得到的模型可以合成高保真、多样、新颖的图像。我们发现U-Net的中间特征图是多样的、有区别的特征表示。我们提出了一种新的用于汇集特征图的注意力机制，并进一步利用该机制作为DifFormer，这是来自不同扩散U-Net块和噪声步长的特征的变换特征融合。我们还开发了DifFeed，这是一种针对扩散量身定制的新型反馈机制。我们发现，扩散模型比GANs更好，并且通过我们的融合和反馈机制，可以在判别任务方面与最先进的无监督图像表示学习方法竞争——具有全监督和半监督的图像分类、细粒度分类的转移、对象检测和分割以及语义分割。我们的项目网站(https://mgwillia.github.io/diffssl/)和代码(https://github.com/soumik-kanad/diffssl)可公开获取。 et.al.|[2311.17921](http://arxiv.org/abs/2311.17921)|null|
|**2023-11-29**|**Visual Anagrams: Generating Multi-View Optical Illusions with Diffusion Models**|我们解决了合成多视图视错觉的问题：图像在变换（如翻转或旋转）时会改变外观。我们提出了一种简单的零样本方法，用于从离线文本到图像的扩散模型中获得这些错觉。在反向扩散过程中，我们从噪声图像的不同视图中估计噪声。然后，我们将这些噪声估计组合在一起，并对图像进行去噪。理论分析表明，这种方法正好适用于可以写成正交变换的视图，其中排列是正交变换的子集。这就产生了视觉变位符号的想法——一种在像素重新排列的情况下改变外观的图像。这包括旋转和翻转，但也包括更奇特的像素排列，如拼图重排。我们的方法也自然地延伸到具有两种以上观点的幻觉。我们提供了定性和定量结果，证明了我们方法的有效性和灵活性。有关其他可视化效果和结果，请参阅我们的项目网页：https://dangeng.github.io/visual_anagrams/ et.al.|[2311.17919](http://arxiv.org/abs/2311.17919)|null|
|**2023-11-29**|**AvatarStudio: High-fidelity and Animatable 3D Avatar Creation from Text**|我们研究仅从文本描述创建高保真度和可动画化的3D化身的问题。现有的文本到化身的方法要么局限于不能被动画化的静态化身，要么难以生成具有良好质量和精确姿势控制的可动画化化身。为了解决这些限制，我们提出了AvatarStudio，这是一个从粗到细的生成模型，用于为可动画化的人类化身生成显式纹理3D网格。具体而言，AvatarStudio从基于低分辨率NeRF的粗略生成表示开始，然后将SMPL引导的关节运动合并到显式网格表示中，以支持化身动画和高分辨率渲染。为了确保生成的化身的视图一致性和姿势可控性，我们引入了一个以DensePose为条件的二维扩散模型，用于分数蒸馏采样监督。通过有效利用铰接网格表示和DensePose条件扩散模型之间的协同作用，AvatarStudio可以从准备好动画的文本中创建高质量的化身，显著优于以前的方法。此外，它适用于许多应用，例如，多模式化身动画和风格引导的化身创建。有关更多结果，请参阅我们的项目页面：http://jeff95.me/projects/avatarstudio.html et.al.|[2311.17917](http://arxiv.org/abs/2311.17917)|null|
|**2023-11-29**|**CG3D: Compositional Generation for Text-to-3D via Gaussian Splatting**|随着基于扩散的生成模型的出现及其生成文本条件图像的能力，内容生成受到了极大的启发。最近，这些模型已被证明为3D图形资产的生成提供了有用的指导。然而，现有的基于文本的3D生成工作面临着基本的限制：（i）无法生成详细的多对象场景，（ii）无法从文本上控制多对象配置，以及（iii）物理逼真的场景合成。在这项工作中，我们提出了CG3D，这是一种用于合成生成可扩展3D资产的方法，可以解决这些约束。我们发现，明确的高斯辐射场，参数化以允许物体的组成，具有实现语义和物理一致场景的能力。通过利用围绕这一明确表示构建的制导框架，我们展示了最先进的结果，甚至能够在物体组合和物理精度方面超过制导扩散模型。 et.al.|[2311.17907](http://arxiv.org/abs/2311.17907)|null|
|**2023-11-29**|**SODA: Bottleneck Diffusion Models for Representation Learning**|我们介绍了SODA，一种自监督扩散模型，用于表示学习。该模型包含一个图像编码器，该编码器将源视图提取为紧凑的表示，进而指导相关新视图的生成。我们表明，通过在编码器和去噪解码器之间施加严格的瓶颈，并利用新颖的视图合成作为自监督目标，我们可以将扩散模型转变为强表示学习器，能够以无监督的方式捕获视觉语义。据我们所知，SODA是第一个成功进行ImageNet线性探针分类的扩散模型，同时，它可以在广泛的数据集上完成重建、编辑和合成任务。进一步的研究揭示了其涌现的潜在空间的非纠缠性质，它是控制和操纵模型生成图像的有效接口。总之，我们的目标是揭示扩散模型令人兴奋和有前景的潜力，不仅用于图像生成，而且用于学习丰富和稳健的表示。 et.al.|[2311.17901](http://arxiv.org/abs/2311.17901)|null|
|**2023-11-29**|**S 308 and other X-ray emitting bubbles around Wolf-Rayet stars**|S308是一个X射线发射气泡，围绕着沃尔夫-拉叶星WR6。这种结构在光学上也很闪耀，因此被称为海豚星云。由于它的角度范围很大，在过去的XMM-Newton观测中，它只被覆盖了90%。由于SRG/eROSITA在X射线中进行的全天空调查提供了独特的数据集，我们可以首次显示气泡在该波段的整个范围的图像及其光谱特征。此外，我们还试图将同样的程序应用于在光学/IR中检测到的其他风吹气泡，并在它们周围寻找X射线扩展发射。我们首先分析了S308的漫发射，提供了详细的光谱分析。然后，我们考虑了之前基于WISE数据的研究中22个光学/IR选择的风吹气泡的样本，首次提供了X射线通量的估计值。我们获得了S308的最佳拟合，其中两个温度非平衡等离子体模型（kT $_{1}=0.8_{-0.3}^{+0.8}$keV和kT$_{2}=2-{-1}^{+3}$keV）显示出超太阳氮丰度和低吸收。我们没有在X射线中检测到22个光学/IR发射气泡中的任何一个，但使用我们的最佳拟合模型，我们估计了每个气泡的3$\sigma$ 通量上限。我们展示了SRG/eROSITA提供的研究已知风吹气泡并寻找其他气泡的新可能性。双温度等离子体描述似乎与S308的数据非常吻合。由于SRG/eROSITA仍然没有检测到所研究的所有22个气泡，因此吸收效应和空间紧凑性很可能是阻碍在软X射线中检测这些气泡的挑战的原因。 et.al.|[2311.17879](http://arxiv.org/abs/2311.17879)|null|
|**2023-11-29**|**Leveraging Graph Diffusion Models for Network Refinement Tasks**|大多数真实世界的网络都是来自未知目标分布的噪声和不完整样本。通过校正损坏或推断未观察到的区域来细化它们通常可以提高下游性能。受用于纠正图像中损坏的令人印象深刻的生成能力的启发，以及“在画”和填充以观察到的图为条件的缺失节点和边之间的相似性，我们提出了一种新的基于子图扩散的图生成框架SGDM。我们的框架不仅提高了图扩散模型的可扩展性和保真度，而且还利用反向过程来执行新的条件生成任务。特别是，通过广泛的经验分析和一组新的度量，我们证明了我们提出的模型有效地支持部分可观测网络的以下细化任务：T1：去噪无关子图，T2：扩展现有的子图，T3：通过重新生成特定的子图以匹配不同节点或子图的特性来执行“样式”转移。 et.al.|[2311.17856](http://arxiv.org/abs/2311.17856)|null|
|**2023-11-30**|**SPiC-E : Structural Priors in 3D Diffusion Models using Cross-Entity Attention**|由于预训练的文本图像扩散模型的可用性，我们正在见证自动生成和操作3D资产的快速进展。然而，合成每个样本都需要耗时的优化程序，这阻碍了它们民主化3D内容创建的潜力。相反，3D扩散模型现在在百万规模的3D数据集上训练，在几秒钟内产生高质量的文本条件3D样本。在这项工作中，我们介绍了SPiC-E——一种为3D扩散模型添加结构指导的神经网络，将其使用范围扩展到文本条件生成之外。其核心是，我们的框架引入了一种跨实体注意力机制，允许多个实体（特别是成对的输入和引导3D形状）通过其在去噪网络内的内部表示进行交互。我们利用这种机制从辅助制导形状学习3D扩散模型中的任务特定结构先验。我们展示了我们的方法支持各种应用程序，包括3D风格化、语义形状编辑和文本条件抽象到3D，它将基于原始的抽象转换为高度表达的形状。大量实验表明，SPiC-E在这些任务中实现了SOTA性能，同时通常比其他方法快得多。重要的是，这是在没有针对任何特定任务调整我们的方法的情况下完成的。 et.al.|[2311.17834](http://arxiv.org/abs/2311.17834)|null|
|**2023-11-29**|**Analyzing and Explaining Image Classifiers via Diffusion Guidance**|虽然深度学习在ImageNet等复杂的图像分类任务中取得了巨大进展，但意外的失败模式，例如通过虚假特征，让人质疑这些分类器在野外工作的可靠性。此外，对于安全关键任务，其决策的黑匣子性质是有问题的，迫切需要解释或至少需要使决策合理的方法。在本文中，我们通过使用引导图像生成框架生成优化分类器导出目标的图像来解决这些问题。我们通过视觉反事实解释（VCE）分析图像分类器的行为和决策，通过分析分类器最大程度不一致的图像检测系统错误，以及可视化神经元以验证潜在的虚假特征。通过这种方式，我们验证了现有的观察结果，例如对抗性鲁棒模型的形状偏差，以及新的故障模式，例如零样本CLIP分类器的系统误差，或识别有害的虚假特征。此外，我们的VCE在更通用的同时，也优于以前的工作。 et.al.|[2311.17833](http://arxiv.org/abs/2311.17833)|null|
|**2023-11-29**|**An Algorithm Based on a Cable-Nernst Planck Model Predicting Synaptic Activity throughout the Dendritic Arbor with Micron Specificity**|最近的技术进步使得能够以高的空间和时间分辨率记录完整电路中的神经元，这就需要以同样的精度进行建模。特别是，结合基于荧光的遗传编码Ca2+-指示剂的超快双光子显微镜的发展，可以捕获与突触输入和动作电位输出相关的完整树突轴和体细胞反应。树枝状乔木结构和随时间分布的活动模式的复杂性导致了极其丰富的4D数据集的生成，这些数据集很难分析（Sakaki，2020）。由于影响细胞内钙离子浓度及其与传感器结合的几个因素之间的非线性相互作用，包括由扩散、电梯度和电压门控电导驱动的离子动力学，从基于荧光的Ca2+生物传感器解释神经活动是具有挑战性的。为了研究这些动力学，我们设计了一个基于类Cable方程的模型，该方程与电解质中离子通量的能斯特-普朗克方程相耦合。我们使用这个模型来模拟信号在树枝状心轴上的传播和离子电扩散。利用这些模拟结果，我们设计了一种从Ca2+成像数据集中检测突触的算法。我们最终将该算法应用于表达jGCaMP7s的神经元的实验性Ca2+-指标数据集（Dana et al.，2019），使用快速随机存取双光子显微镜在非洲爪蟾视顶盖体内进行全树突乔木采样。我们的模型再现了实验观察到的视觉刺激诱发的jGCaMP7s介导的钙信号的动力学，由此产生的算法可以预测突触在树突轴上的位置。我们的研究提供了一种方法，根据完整和清醒发育的脊椎动物大脑中记录的神经元完整树突轴的荧光数据来预测树突轴上的突触活动和位置。 et.al.|[2311.17785](http://arxiv.org/abs/2311.17785)|null|

<p align=right>(<a href=#updated-on-20231201>back to top</a>)</p>

## NeRF

|Publish Date|Title|Abstract|PDF|Code|
|---|---|---|---|---|
|**2023-11-29**|**Neural Fields with Thermal Activations for Arbitrary-Scale Super-Resolution**|最近的任意尺度单图像超分辨率（ASSR）方法已经使用局部神经场来表示可以以不同速率采样的连续信号。然而，在这样的公式中，场值的逐点查询并不自然地与给定像素的点扩散函数（PSF）匹配。在这项工作中，我们提出了一种设计神经场的新方法，使得可以使用高斯PSF来查询点，该函数在ASSR的分辨率之间移动时起到抗混叠的作用。我们使用从傅立叶理论和热方程导出的新激活函数来实现这一点。这不需要额外的成本：与图像域中的滤波不同，在我们的框架中使用高斯PSF查询点不会影响计算成本。与超网络相结合，我们的方法不仅提供了理论上有保证的抗混叠，而且为ASSR设置了一个新的标准，同时也比以前的方法更具参数效率。 et.al.|[2311.17643](http://arxiv.org/abs/2311.17643)|null|
|**2023-11-28**|**In Search of a Data Transformation That Accelerates Neural Field Training**|神经场是数据表示中一种新兴的范式，它训练神经网络来逼近给定的信号。阻碍其广泛采用的一个关键障碍是编码速度——生成神经场需要神经网络的过拟合，这可能需要大量的SGD步骤才能达到所需的保真度水平。在本文中，我们深入研究了数据转换对神经场训练速度的影响，特别是关注像素位置的排列如何影响SGD的收敛速度。与直觉相反，我们发现随机排列像素位置可以显著加速训练。为了解释这一现象，我们通过PSNR曲线、损失景观和误差模式来检验神经场训练。我们的分析表明，随机像素排列去除了易于拟合的模式，这有助于在早期阶段进行简单的优化，但阻碍了捕捉信号的精细细节。 et.al.|[2311.17094](http://arxiv.org/abs/2311.17094)|null|
|**2023-11-28**|**HumanGaussian: Text-Driven 3D Human Generation with Gaussian Splatting**|根据文本提示生成逼真的三维人体是一项理想但具有挑战性的任务。现有的方法通过分数蒸馏采样（SDS）优化3D表示，如网格或神经场，其存在细节不足或训练时间过长的问题。在本文中，我们提出了一个高效而有效的框架HumanGaussian，它可以生成具有细粒度几何结构和逼真外观的高质量3D人。我们的关键见解是，3D高斯飞溅是一种具有周期性高斯收缩或增长的高效渲染器，其中这种自适应密度控制可以由内在的人体结构自然引导。具体而言，1）我们首先提出了一种结构感知SDS，它可以同时优化人体外观和几何形状。利用RGB和深度空间的多模态得分函数来提取高斯致密化和修剪过程。2） 此外，我们通过将SDS分解为更嘈杂的生成分数和更干净的分类器分数，设计了一种退火的负提示引导，很好地解决了过饱和问题。在仅修剪阶段中，基于高斯大小进一步消除浮动伪影，以增强生成平滑度。大量实验证明了我们的框架具有卓越的效率和竞争力，在不同的场景下呈现了生动的3D人类。项目页面：https://alvinliu0.github.io/projects/humangaussian et.al.|[2311.17061](http://arxiv.org/abs/2311.17061)|null|
|**2023-11-28**|**SplitNeRF: Split Sum Approximation Neural Field for Joint Geometry, Illumination, and Material Estimation**|我们提出了一种新的方法，通过从一组具有固定照明的姿势图像中估计真实世界物体的几何结构、材料特性和环境照明来数字化它们。我们的方法将分割和近似与基于图像的照明结合到神经辐射场（NeRF）管道中，用于基于物理的实时渲染。我们建议使用单个场景特定的MLP来建模场景的照明，该MLP表示任意分辨率的预集成的基于图像的照明。我们通过开发一种基于有效蒙特卡罗采样的新型正则化子来实现预集成照明的精确建模。此外，我们还提出了一种新的方法，通过利用基于蒙特卡罗采样的类似正则化子来监督自遮挡预测。实验结果证明了我们的方法在估计场景几何、材料特性和照明方面的效率和有效性。我们的方法能够在单个NVIDIA A100 GPU中仅经过 ${\sim}1$ 小时的训练后就获得最先进的重新照明质量。 et.al.|[2311.16671](http://arxiv.org/abs/2311.16671)|null|
|**2023-11-27**|**MeshGPT: Generating Triangle Meshes with Decoder-Only Transformers**|我们介绍了MeshGPT，这是一种生成三角形网格的新方法，它反映了艺术家创建的网格的典型紧凑性，而不是通过等表面方法从神经场中提取的密集三角形网格。受强大的大型语言模型最近进展的启发，我们采用了一种基于序列的方法来自回归生成三角形网格作为三角形序列。我们首先使用图卷积来学习潜在量化嵌入的词汇表，图卷积为这些嵌入提供了局部网格几何和拓扑的信息。这些嵌入被解码器排序并解码为三角形，确保它们能够有效地重建网格。然后在这个学习的词汇表上训练转换器，以在给定先前嵌入的情况下预测下一个嵌入的索引。一旦训练好，我们的模型就可以进行自回归采样以生成新的三角形网格，直接生成具有尖锐边缘的紧凑网格，更接近于模仿手工网格的有效三角测量模式。与最先进的网格生成方法相比，MeshGPT有了显著的改进，形状覆盖率提高了9%，各种类别的FID得分提高了30分。 et.al.|[2311.15475](http://arxiv.org/abs/2311.15475)|null|
|**2023-11-26**|**Distributed Delay and Desynchronization in a Brain Network Model**|我们考虑一个神经场模型，该模型由任意数量的Wilson Cowan节点的网络组成，该网络具有抑制性耦合强度和延时兴奋性耦合的稳态调节。我们扩展了以前对该模型的研究，将具有常用核分布的分布式时延包括在内：德尔塔函数、均匀分布和伽玛分布。重点讨论满足常行和条件的网络，我们展示了连通矩阵的每个特征值如何与Hopf分支相关，并且特征值决定了分支是导致同步还是去同步的振荡行为。我们考虑两个示例网络，一个具有所有实特征值（双向环），另一个具有一些复特征值（单向环）。在双向环中，Hopf曲线被组织起来，使得只有同步的Hopf才会导致渐近稳定的行为。因此，网络中的行为总是同步的。然而，在单向环网络中，异步和同步Hopf曲线的交点可能会出现双Hopf分岔点。因此，可以出现渐近稳定的同步和异步极限环，以及结合同步和异步行为的类环面解。增加网络的大小或平均时延会使这些交叉点和相关的异步行为更有可能发生。数值方法用于证实这一发现，并使用Wolfram Mathematica绘制了Hopf分岔曲线。这些见解提供了对大型振荡器网络中去同步机制的更深入理解。 et.al.|[2311.15329](http://arxiv.org/abs/2311.15329)|null|
|**2023-11-25**|**Coordinate-Aware Modulation for Neural Fields**|将低维输入坐标映射到相应信号的神经场在表示各种信号方面显示出了有希望的结果。已经提出了许多方法，并且使用MLP和网格表示的技术已经取得了实质性的成功。MLP允许紧凑和高表达性，但经常受到光谱偏差和缓慢收敛速度的影响。另一方面，使用网格的方法不受光谱偏差的影响，并且以高空间复杂度为代价实现了快速的训练速度。在这项工作中，我们提出了一种在神经领域中利用MLP和网格表示的新方法。与顺序组合它们（首先从网格中提取特征并将其提供给MLP）的流行方法不同，我们将无光谱偏差的网格表示注入MLP中的中间特征。更具体地说，我们提出了一种坐标感知调制（CAM），它使用从网格表示中提取的比例和偏移参数来调制中间特征。这可以保持MLP的优势，同时减轻任何剩余的潜在偏差，促进高频成分的快速学习。此外，我们根据经验发现，在神经领域文献中尚未成功的特征归一化，在与所提出的CAM结合应用时被证明是有效的。实验结果表明，CAM增强了神经表示的性能，并提高了一系列信号的学习稳定性。特别是在新颖的视图合成任务中，我们以最少的参数数量和快速的训练速度实现了最先进的动态场景性能，并在1MB内存下实现了静态场景的最佳性能。CAM的性能也大大优于使用神经场的最佳视频压缩方法。 et.al.|[2311.14993](http://arxiv.org/abs/2311.14993)|null|
|**2023-11-22**|**Compact 3D Gaussian Representation for Radiance Field**|神经辐射场（NeRFs）在高保真度捕捉复杂三维场景方面显示出非凡的潜力。然而，阻碍NeRFs广泛采用的一个持续挑战是体积绘制造成的计算瓶颈。另一方面，3D高斯飞溅（3DGS）最近作为一种替代表示出现，它利用了基于3D高斯的表示，并采用光栅化流水线来渲染图像，而不是体积渲染，实现了非常快的渲染速度和有希望的图像质量。然而，一个显著的缺点出现了，因为3DGS需要大量的3D高斯来维持渲染图像的高保真度，这需要大量的存储器和存储。为了解决这一关键问题，我们特别强调两个关键目标：在不牺牲性能的情况下减少高斯点的数量，以及压缩高斯属性，如与视图相关的颜色和协方差。为此，我们提出了一种可学习的掩码策略，该策略在保持高性能的同时显著减少高斯数。此外，我们通过使用基于网格的神经场而不是依赖于球面谐波，提出了一种紧凑但有效的视图相关颜色表示。最后，我们学习码本，通过矢量量化来紧凑地表示高斯的几何属性。在我们广泛的实验中，我们一致表明，与3DGS相比，存储空间减少了10美元，渲染速度提高，同时保持了场景表示的质量。我们的工作为3D场景表示提供了一个全面的框架，实现了高性能、快速训练、紧凑性和实时渲染。我们的项目页面位于https://maincold2.github.io/c3dgs/. et.al.|[2311.13681](http://arxiv.org/abs/2311.13681)|null|
|**2023-11-21**|**3D Compression Using Neural Fields**|神经场（NFs）作为一种压缩各种数据模式（如图像和视频）的工具，已经获得了发展势头。这项工作利用了先前的进展，并提出了一种新的基于NF的3D数据压缩算法。我们推导出了两个版本的方法——一个是基于有符号距离域（SDF）的水密形状，更一般地说，一个是使用无符号距离场（UDF）的任意非水密形状。我们证明了我们的方法在三维点云和网格上的几何压缩方面表现出色。此外，我们表明，由于NF公式，可以直接扩展我们的压缩算法来压缩3D数据的几何结构和属性（例如颜色）。 et.al.|[2311.13009](http://arxiv.org/abs/2311.13009)|null|
|**2023-11-20**|**NePF: Neural Photon Field for Single-Stage Inverse Rendering**|我们提出了一种新的单级框架——神经光子场（NePF），以解决多视图图像的不适定逆绘制问题。与以前在多个阶段恢复几何、材料和照明并从不同神经场的各种多层感知器中提取特性的方法相反，我们质疑这种复杂性，并介绍了我们的方法-一个统一恢复所有特性的单阶段框架。NePF通过充分利用神经隐式曲面的权重函数背后的物理含义和与视图相关的辐射来实现这种统一。此外，我们还介绍了一种创新的基于坐标的照明模型，用于基于体积物理的快速渲染。为了正则化这种照明，我们实现了用于散射估计的次表面散射模型。我们在真实数据集和合成数据集上评估我们的方法。结果证明了我们的方法在恢复高保真几何和视觉上合理的材料属性方面的优越性。 et.al.|[2311.11555](http://arxiv.org/abs/2311.11555)|null|

<p align=right>(<a href=#updated-on-20231201>back to top</a>)</p>

[contributors-shield]: https://img.shields.io/github/contributors/Vincentqyw/cv-arxiv-daily.svg?style=for-the-badge
[contributors-url]: https://github.com/Vincentqyw/cv-arxiv-daily/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/Vincentqyw/cv-arxiv-daily.svg?style=for-the-badge
[forks-url]: https://github.com/Vincentqyw/cv-arxiv-daily/network/members
[stars-shield]: https://img.shields.io/github/stars/Vincentqyw/cv-arxiv-daily.svg?style=for-the-badge
[stars-url]: https://github.com/Vincentqyw/cv-arxiv-daily/stargazers
[issues-shield]: https://img.shields.io/github/issues/Vincentqyw/cv-arxiv-daily.svg?style=for-the-badge
[issues-url]: https://github.com/Vincentqyw/cv-arxiv-daily/issues

