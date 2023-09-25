[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]

## Updated on 2023.09.25
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
|**2023-09-22**|**NeRRF: 3D Reconstruction and View Synthesis for Transparent and Specular Objects with Neural Refractive-Reflective Fields**|神经辐射场（NeRF）已经彻底改变了基于图像的视图合成领域。然而，NeRF使用直线光线，无法处理由折射和反射引起的复杂光路变化。这阻碍了NeRF成功合成透明或镜面物体，而这些物体在现实世界的机器人和A/VR应用中无处不在。本文介绍了折射反射场。以物体轮廓为输入，我们首先利用渐进编码的行进四面体来重建非朗伯物体的几何结构，然后使用菲涅耳项在统一的框架中对物体的折射和反射效应进行建模。同时，为了实现高效、有效的抗混叠，我们提出了一种虚拟锥超采样技术。我们在真实世界和合成数据集的不同形状、背景和菲涅耳项上对我们的方法进行了基准测试。我们还对各种编辑应用程序的渲染结果进行了定性和定量的基准测试，包括材质编辑、对象替换/插入和环境照明估计。代码和数据可在https://github.com/dawning77/NeRRF. et.al.|[2309.13039](http://arxiv.org/abs/2309.13039)|**[link](https://github.com/dawning77/nerrf)**|
|**2023-09-21**|**ORTexME: Occlusion-Robust Human Shape and Pose via Temporal Average Texture and Mesh Encoding**|在单目视频的3D人体形状和姿势估计中，用有限的标记数据训练的模型不能很好地推广到具有遮挡的视频，这在野生视频中很常见。最近的人类神经渲染方法专注于由现成的人形和姿势方法初始化的新颖视图合成，具有校正初始人形的潜力。然而，现有的方法存在一些缺点，例如，在处理遮挡时出错，对不准确的人体分割敏感，以及由于非正则化的不透明度场而导致的无效损失计算。为了解决这些问题，我们引入了ORTexME，这是一种遮挡鲁棒的时间方法，它利用来自输入视频的时间信息来更好地正则化被遮挡的身体部位。虽然我们的ORTexME是基于NeRF的，但为了确定NeRF射线采样的可靠区域，我们利用我们新颖的平均纹理学习方法来学习人的平均外观，并基于平均纹理推断面具。此外，为了指导NeRF中的不透明度场更新以抑制模糊和噪声，我们建议使用人体网格。定量评估表明，我们的方法在具有挑战性的多人3DPW数据集上实现了显著的改进，其中我们的方法实现了1.8P-MPJPE的误差降低。基于SOTA渲染的方法失败了，并在同一数据集上将错误扩大到5.6。 et.al.|[2309.12183](http://arxiv.org/abs/2309.12183)|null|
|**2023-09-21**|**Fast Satellite Tensorial Radiance Field for Multi-date Satellite Imagery of Large Size**|现有的卫星图像NeRF模型速度较慢，必须输入太阳信息，并且在处理大型卫星图像方面存在局限性。作为回应，我们提出了SatensoRF，它显著加快了整个过程，同时为大尺寸卫星图像使用了更少的参数。此外，我们观察到，在神经辐射场中，朗伯表面的普遍假设不符合植物和水生元素。与传统的基于分层MLP的场景表示相比，我们选择了一种针对颜色、体积密度和辅助变量的多尺度张量分解方法来对具有镜面颜色的光场进行建模。此外，为了纠正多日期图像中的不一致性，我们结合了总变化损失来恢复密度张量场，并将该问题视为去噪任务。为了验证我们的方法，我们使用空间网多视图数据集的子集对SatensoRF进行了评估，该数据集包括多日期和单日期多视图RGB图像。我们的结果清楚地表明，SatensoRF在新颖的视图合成性能方面超过了最先进的Sat-NeRF系列。值得注意的是，SatensoRF需要更少的参数进行训练，从而提高训练和推理速度，降低计算需求。 et.al.|[2309.11767](http://arxiv.org/abs/2309.11767)|null|
|**2023-09-20**|**GenLayNeRF: Generalizable Layered Representations with 3D Model Alignment for Multi-Human View Synthesis**|由于复杂的人与人之间的遮挡，多人场景的新视图合成（NVS）带来了挑战。分层表示通过将场景划分为多层辐射场来处理复杂性，然而，它们主要局限于逐场景优化，因此效率低下。可泛化的人体视图合成方法将预先拟合的三维人体网格与图像特征相结合以达到泛化，但它们主要是针对单个人体场景设计的。另一个缺点是依赖于用于3D身体模型的参数预拟合的多步骤优化技术，该3D身体模型在稀疏视图设置中与图像不对准，从而导致合成视图中的幻觉。在这项工作中，我们提出了GenLayNeRF，这是一种可推广的分层场景表示，用于多个人类主体的自由视点渲染，不需要每场景优化和非常稀疏的视图作为输入。我们将场景划分为由3D身体网格锚定的多个人体层。然后，我们通过一个新颖的端到端可训练模块确保身体模型与输入视图的像素级对齐，该模块执行迭代参数校正，并结合多视图特征融合，以产生对齐的3D模型。对于NVS，我们提取逐点图像对齐和人锚定的特征，这些特征使用自注意和交叉注意模块进行关联和融合。我们使用基于注意力的RGB融合模块将低级别的RGB值增强到特征中。为了评估我们的方法，我们构建了两个多人视角合成数据集；DeepMultiSyn和ZJU MultiHuman。结果表明，在没有测试时间优化的情况下，我们提出的方法优于可推广的和非人类的每场景NeRF方法，同时与分层的每场景方法不相上下。 et.al.|[2309.11627](http://arxiv.org/abs/2309.11627)|null|
|**2023-09-20**|**Light Field Diffusion for Single-View Novel View Synthesis**|单视图新视图合成，即基于单个参考图像从新视点生成图像的任务，是计算机视觉中一项重要但具有挑战性的任务。近年来，去噪扩散概率模型（DDPM）由于其强大的高保真度图像生成能力而在该领域流行起来。然而，当前基于扩散的方法直接依赖于相机姿态矩阵作为观看条件，全局地和隐含地引入3D约束。这些方法可能存在从不同角度生成的图像之间的不一致性，特别是在具有复杂纹理和结构的区域中。在这项工作中，我们提出了光场扩散（LFD），这是一种基于条件扩散的单视图新视图合成模型。与以前使用相机姿态矩阵的方法不同，LFD将相机视图信息转换为光场编码，并将其与参考图像相结合。这种设计在扩散模型中引入了局部像素约束，从而促进了更好的多视图一致性。在几个数据集上的实验表明，我们的LFD可以有效地生成高保真图像，即使在复杂的区域也能保持更好的3D一致性。我们的方法可以生成比基于NeRF的模型质量更高的图像，并且我们获得的样本质量与其他基于扩散的模型类似，但只有模型大小的三分之一。 et.al.|[2309.11525](http://arxiv.org/abs/2309.11525)|null|
|**2023-09-21**|**Controllable Dynamic Appearance for Neural 3D Portraits**|神经辐射场（NeRF）的最新进展使得通过控制头部姿势、面部表情和观看方向来重建和恢复动态人像场景成为可能。然而，训练这样的模型假设变形区域的光度一致性，例如，随着头部姿势和面部表情的变化，面部变形时必须均匀照明。即使在工作室环境中，视频各帧之间的这种光度一致性也很难保持，因此，创建的可重影神经肖像在重影过程中容易出现伪影。在这项工作中，我们提出了CoDyNeRF，这是一种能够在真实世界的捕捉条件下创建完全可控的3D肖像的系统。CoDyNeRF通过规范空间中的动态外观模型来学习近似照明相关效果，该模型以预测的表面法线、面部表情和头部姿势变形为条件。表面法线预测是使用3DMM法线来指导的，3DMM法线充当人类头部法线的粗略先验，其中由于头部姿势和面部表情变化引起的刚性和非刚性变形，很难直接预测法线。仅使用智能手机拍摄的受试者短视频进行训练，我们就展示了我们的方法在具有明确的头部姿势和表情控制以及逼真照明效果的人像场景的自由视图合成方面的有效性。项目页面可在此处找到：http://shahrukhathar.github.io/2023/08/22/CoDyNeRF.html et.al.|[2309.11009](http://arxiv.org/abs/2309.11009)|null|
|**2023-09-19**|**ReShader: View-Dependent Highlights for Single Image View-Synthesis**|近年来，由于3D场景表示和图像修复技术的快速发展，从单个图像进行的新颖视图合成已经取得了重大进展。虽然目前的方法能够合成几何一致的新视图，但它们往往不能正确处理视图相关的效果。具体来说，他们合成图像中的高光通常看起来粘在表面上，这使得新颖的视图不切实际。为了解决这个主要问题，我们进行了一项关键观察，即合成新视图的过程需要改变基于新相机的像素的阴影，并将它们移动到适当的位置。因此，我们建议将视图合成过程拆分为两个独立的任务，即像素重新加载和重新定位。在重影过程中，我们以单个图像为输入，并基于新型相机调整其明暗度。然后将该重新加载的图像用作现有视图合成方法的输入，以重新定位像素并产生最终的新颖视图图像。我们建议使用神经网络来执行重新加载，并生成一大组合成输入重新加载对来训练我们的网络。我们证明，我们的方法在各种现实世界场景中产生了具有逼真运动亮点的看似新颖的视图图像。 et.al.|[2309.10689](http://arxiv.org/abs/2309.10689)|null|
|**2023-09-19**|**Locally Stylized Neural Radiance Fields**|近年来，人们对将风格化应用于参考风格图像的3D场景，特别是应用于神经辐射场（NeRF）越来越感兴趣。虽然直接在NeRF上执行风格化可以保证在任意新颖视图上的外观一致性，但引导图案从风格图像转移到NeRF场景的不同部分是一个具有挑战性的问题。在这项工作中，我们提出了一个基于局部风格转移的NeRF风格化框架。特别是，我们使用哈希网格编码来学习外观和几何组件的嵌入，并表明哈希表定义的映射允许我们在一定程度上控制风格化。然后通过优化外观分支同时保持几何体分支固定来实现样式化。为了支持局部风格转移，我们提出了一种新的损失函数，该函数利用分割网络和二分匹配来建立风格图像和从体绘制中获得的内容图像之间的区域对应关系。我们的实验表明，我们的方法通过新的视图合成产生了合理的风格化结果，同时通过操纵和定制区域对应关系具有灵活的可控性。 et.al.|[2309.10684](http://arxiv.org/abs/2309.10684)|null|
|**2023-09-19**|**Anti-Aliased Neural Implicit Surfaces with Encoding Level of Detail**|我们提出了LoD-NeuS，这是一种用于高频几何细节恢复和抗锯齿新视图渲染的有效神经表示。从具有细节水平（LoD）的基于体素的表示中汲取灵感，我们引入了一种基于多尺度三平面的场景表示，该表示能够捕捉符号距离函数（SDF）的LoD和空间辐射。我们的表示聚合了来自圆锥台内沿射线的多重卷积特征的空间特征，并通过可微分渲染优化了LoD特征体积。此外，我们提出了一种误差引导采样策略，以在优化过程中引导SDF的增长。定性和定量评估都表明，与最先进的方法相比，我们的方法实现了卓越的表面重建和真实感视图合成。 et.al.|[2309.10336](http://arxiv.org/abs/2309.10336)|null|
|**2023-09-21**|**ExBluRF: Efficient Radiance Fields for Extreme Motion Blurred Images**|我们提出了ExBluRF，这是一种基于有效辐射场优化的极端运动模糊图像的新视图合成方法。我们的方法由两个主要组成部分组成：基于6自由度相机轨迹的运动模糊公式和基于体素的辐射场。从极其模糊的图像中，我们通过联合估计生成模糊图像的相机轨迹来优化清晰的辐射场。在训练中，沿着相机轨迹的多条光线被累积以重建单个模糊的颜色，这相当于物理运动模糊操作。我们最小化了模糊图像空间上的照片一致性损失，并获得了具有相机轨迹的清晰辐射场，这些轨迹解释了所有图像的模糊。模糊图像空间上的联合优化需要与模糊大小成比例地痛苦地增加计算和资源。我们的方法通过将基于MLP的框架替换为低维6自由度相机姿态和基于体素的辐射场来解决这个问题。与现有作品相比，我们的方法从具有挑战性的运动模糊视图中恢复了更清晰的3D场景，训练时间和GPU内存消耗减少了10倍。 et.al.|[2309.08957](http://arxiv.org/abs/2309.08957)|null|

<p align=right>(<a href=#updated-on-20230925>back to top</a>)</p>

## 3D Reconstruction

|Publish Date|Title|Abstract|PDF|Code|
|---|---|---|---|---|
|**2023-09-22**|**NeRRF: 3D Reconstruction and View Synthesis for Transparent and Specular Objects with Neural Refractive-Reflective Fields**|神经辐射场（NeRF）已经彻底改变了基于图像的视图合成领域。然而，NeRF使用直线光线，无法处理由折射和反射引起的复杂光路变化。这阻碍了NeRF成功合成透明或镜面物体，而这些物体在现实世界的机器人和A/VR应用中无处不在。本文介绍了折射反射场。以物体轮廓为输入，我们首先利用渐进编码的行进四面体来重建非朗伯物体的几何结构，然后使用菲涅耳项在统一的框架中对物体的折射和反射效应进行建模。同时，为了实现高效、有效的抗混叠，我们提出了一种虚拟锥超采样技术。我们在真实世界和合成数据集的不同形状、背景和菲涅耳项上对我们的方法进行了基准测试。我们还对各种编辑应用程序的渲染结果进行了定性和定量的基准测试，包括材质编辑、对象替换/插入和环境照明估计。代码和数据可在https://github.com/dawning77/NeRRF. et.al.|[2309.13039](http://arxiv.org/abs/2309.13039)|**[link](https://github.com/dawning77/nerrf)**|
|**2023-09-22**|**Deep3DSketch+: Rapid 3D Modeling from Single Free-hand Sketches**|AR/VR的快速发展给3D内容带来了巨大的需求。虽然广泛使用的计算机辅助设计（CAD）方法需要耗时且劳动密集的建模过程，但基于草图的三维建模作为计算机与人交互的自然形式提供了一种潜在的解决方案。然而，草图的稀疏性和模糊性使得生成反映创作者想法的高保真度内容具有挑战性。通常需要从多个视图精确绘制或战略性分步绘制来应对挑战，但对新手用户来说并不友好。在这项工作中，我们介绍了一种新的端到端方法Deep3DSketch+，该方法只使用一个徒手草图进行三维建模，而无需输入多个草图或视图信息。具体而言，我们介绍了一种用于实时高效推理的轻量级生成网络，以及一种具有结构感知的对抗性训练方法，该方法使用笔划增强模块（SEM）来捕获结构信息，以便于学习逼真和精细的形状结构，从而实现高保真性能。大量的实验证明了我们的方法在合成和真实数据集上具有最先进的（SOTA）性能的有效性。 et.al.|[2309.13006](http://arxiv.org/abs/2309.13006)|null|
|**2023-09-20**|**Language-driven Object Fusion into Neural Radiance Fields with Pose-Conditioned Dataset Updates**|神经辐射场是一种新兴的渲染方法，它通过神经场景表示和体积渲染生成高质量的多视图一致图像。尽管基于神经辐射场的技术对于场景重建是稳健的，但它们添加或移除对象的能力仍然有限。本文提出了一种新的语言驱动方法，通过数据集更新实现具有神经辐射场的对象操作。具体而言，为了将由一组多视图图像表示的新前景对象插入背景辐射场，我们使用文本到图像的扩散模型来学习并生成组合图像，该组合图像将感兴趣的对象融合到视图之间的给定背景中。然后，这些组合图像用于细化背景辐射场，以便我们可以渲染包含对象和背景的视图一致的图像。为了确保视图的一致性，我们提出了一种数据集更新策略，该策略在将训练传播到剩余视图之前，优先考虑与已训练视图接近的相机视图的辐射场训练。我们表明，在相同的数据集更新策略下，我们可以使用文本到三维模型的数据以及对象移除来轻松地调整我们的对象插入方法。实验结果表明，我们的方法可以生成编辑场景的真实感图像，在三维重建和神经辐射场混合方面优于现有技术。 et.al.|[2309.11281](http://arxiv.org/abs/2309.11281)|**[link](https://github.com/kcshum/pose-conditioned-NeRF-object-fusion)**|
|**2023-09-19**|**PLVS: A SLAM System with Points, Lines, Volumetric Mapping, and 3D Incremental Segmentation**|本文介绍了PLVS：一个利用稀疏SLAM、体积映射和3D无监督增量分割的实时系统。PLVS代表点、线、体积映射和分割。它支持RGB-D和立体声相机，这些相机可以选择配备IMU。SLAM模块基于关键帧，提取并跟踪稀疏点和线段作为特征。体积映射相对于SLAM前端并行运行，并通过融合从关键帧反向投影的点云来生成探索环境的3D重建。PLVS支持并集成了不同的体积映射方法。我们使用一种新的重投影误差来对调整线段进行集束。该误差利用可用的深度信息来稳定线段端点的位置估计。在PLVS框架下，为RGB-D相机实现并集成了一种基于几何的增量分割方法。我们在一些公开的数据集上对PLVS框架进行了定性和定量评估。附录详细介绍了所采用的立体线三角测量方法，并对我们用于线误差项的雅可比矩阵进行了推导。该软件是开源的。 et.al.|[2309.10896](http://arxiv.org/abs/2309.10896)|**[link](https://github.com/luigifreda/plvs)**|
|**2023-09-19**|**SHOWMe: Benchmarking Object-agnostic Hand-Object 3D Reconstruction**|最近的手-物体交互数据集显示出有限的真实物体可变性，并且依赖于拟合MANO参数模型来获得真实的手形状。为了超越这些限制并推动进一步的研究，我们引入了SHOWMe数据集，该数据集由96个视频组成，用真实和详细的手对象3D纹理网格进行注释。根据最近的工作，我们考虑了一个刚性手对象场景，其中手相对于对象的姿势在整个视频序列中保持不变。这一假设使我们能够将亚毫米精度的地面实况3D扫描注册到SHOWMe中的图像序列中。尽管更简单，但这一假设在所需精度和细节水平很重要的应用中是有意义的，例如，人机协作中的对象移交、对象扫描或操作和接触点分析。重要的是，手对象系统的刚性允许使用由刚性配准步骤和多视图重建（MVR）部分组成的两阶段流水线来处理未知手持对象的基于视频的3D重建。我们仔细评估了这两个阶段的一组非平凡基线，并表明使用SfM工具箱或手部姿态估计器来恢复刚性变换和现成的MVR算法，可以实现有前景的对象不可知的3D手部对象重建。然而，这些方法对最初的相机姿态估计仍然敏感，由于物体上缺乏纹理或手的严重遮挡，这些估计可能不精确，这为重建留下了改进的空间。代码和数据集可在https://europe.naverlabs.com/research/showme et.al.|[2309.10748](http://arxiv.org/abs/2309.10748)|null|
|**2023-09-18**|**Improving Neural Indoor Surface Reconstruction with Mask-Guided Adaptive Consistency Constraints**|从2D图像重建3D场景一直是一项长期任务。最近的研究利用神经隐式表面作为3D重建的统一表示，而不是估计每帧深度图并将其融合到3D中。这些方法配备了数据驱动的预训练几何线索，表现出了良好的性能。然而，不准确的先验估计（这通常是不可避免的）可能导致次优重建质量，特别是在一些几何复杂的区域。在本文中，我们提出了一个两阶段的训练过程，解耦视图相关和视图无关的颜色，并利用两个新的一致性约束来提高细节重建性能，而不需要额外的先验。此外，我们引入了一个基本的掩码方案来自适应地影响监督约束的选择，从而提高自监督范式中的性能。在合成数据集和真实世界数据集上的实验表明，该方法能够减少先验估计误差的干扰，并实现具有丰富几何细节的高质量场景重建。 et.al.|[2309.09739](http://arxiv.org/abs/2309.09739)|null|
|**2023-09-18**|**Robust Geometry-Preserving Depth Estimation Using Differentiable Rendering**|在这项研究中，我们解决了从单目深度估计中恢复3D场景结构的挑战。虽然传统的深度估计方法利用标记的数据集来直接预测绝对深度，但最近的进展提倡混合数据集训练，增强了在不同场景中的泛化能力。然而，这种混合数据集训练只能产生未知规模和偏移的深度预测，阻碍了精确的3D重建。现有的解决方案需要额外的3D数据集或几何体完整的深度注释，这些限制了它们的通用性。在本文中，我们提出了一种学习框架，该框架训练模型来预测几何保持深度，而不需要额外的数据或注释。为了产生逼真的3D结构，我们渲染重建场景的新颖视图，并设计损失函数，以提高不同视图之间的深度估计一致性。全面的实验强调了我们框架卓越的泛化能力，在几个基准数据集上超越了现有的最先进的方法，而不需要利用额外的训练信息。此外，我们创新的损失函数使模型能够仅使用未标记的图像自主恢复特定领域的尺度和偏移系数。 et.al.|[2309.09724](http://arxiv.org/abs/2309.09724)|null|
|**2023-09-18**|**Self-supervised Multi-view Clustering in Computer Vision: A Survey**|近年来，多视图聚类（MVC）在跨模态表示学习和数据驱动决策中具有重要意义。它通过利用多个视图之间的一致性和互补信息将样本聚类到不同的组中来实现这一点。然而，随着对比学习在计算机视觉领域的不断发展，自监督学习也取得了实质性的研究进展，并逐渐在MVC方法中占据主导地位。它通过设计代理任务来指导聚类过程，以挖掘图像和视频数据本身作为监督信息的表示。尽管自监督MVC发展迅速，但目前还没有一个全面的调查来分析和总结研究进展的现状。因此，本文探讨了自监督MVC出现的原因和优势，并讨论了常见数据集的内部联系和分类、数据问题、表示学习方法和自监督学习方法。本文不仅介绍了每一类方法的机制，还举例说明了如何使用这些技术。最后指出了一些有待进一步研究和发展的问题。 et.al.|[2309.09473](http://arxiv.org/abs/2309.09473)|null|
|**2023-09-17**|**Uncertainty-aware 3D Object-Level Mapping with Deep Shape Priors**|三维对象级映射是机器人技术中的一个基本问题，当推理过程中对象CAD模型不可用时，这一问题尤其具有挑战性。在这项工作中，我们提出了一个框架，可以为未知对象重建高质量的对象级映射。我们的方法以多个RGB-D图像作为输入，并为检测到的对象输出密集的3D形状和9-DoF姿势（包括3个比例参数）。我们方法的核心思想是利用形状类别的学习生成模型作为先验，并为3D重建制定概率、不确定性感知的优化框架。我们推导了一个概率公式，该公式通过两个新的损失函数传播形状并带来不确定性。与当前最先进的方法不同，我们在优化过程中明确地对对象形状和姿态的不确定性进行建模，从而产生高质量的对象级映射系统。此外，我们证明，由此产生的形状和姿态不确定性可以准确地反映我们物体地图的真实误差，也可以用于下游机器人任务，如主动视觉。我们对室内和室外真实世界的数据集进行了广泛的评估，实现了对最先进方法的实质性改进。我们的代码将在https://github.com/TRAILab/UncertainShapePose. et.al.|[2309.09118](http://arxiv.org/abs/2309.09118)|null|
|**2023-09-15**|**Uncertainty-Aware Multi-View Visual Semantic Embedding**|图像文本检索的关键挑战是有效地利用语义信息来测量视觉和语言数据之间的相似性。然而，使用实例级二进制标签，即每个图像与单个文本配对，无法捕捉不同语义单元之间的多个对应关系，导致多模态语义理解的不确定性。尽管最近的研究通过更复杂的模型结构或预训练技术捕获了细粒度的信息，但很少有研究直接建模对应关系的不确定性，以充分利用二进制标签。为了解决这个问题，我们提出了一个不确定性感知的多视图视觉语义嵌入（UAMVSE）}框架，该框架将整个图像-文本匹配分解为多视图-文本匹配。我们的框架引入了一个不确定性感知损失函数（UALoss），通过自适应地建模每个视图文本对应关系中的不确定性来计算每个视图文本损失的权重。不同的权重引导模型关注不同的语义信息，增强了模型理解图像和文本对应关系的能力。我们还通过对相似度矩阵进行归一化，设计了一种优化的图像-文本匹配策略，以提高模型性能。在Flicker30k和MS-COCO数据集上的实验结果表明，UAMVSE的性能优于最先进的模型。 et.al.|[2309.08154](http://arxiv.org/abs/2309.08154)|null|

<p align=right>(<a href=#updated-on-20230925>back to top</a>)</p>

## Diffusion

|Publish Date|Title|Abstract|PDF|Code|
|---|---|---|---|---|
|**2023-09-22**|**MosaicFusion: Diffusion Models as Data Augmenters for Large Vocabulary Instance Segmentation**|我们提出了MosaicFusion，这是一种简单而有效的基于扩散的数据增强方法，用于大型词汇实例分割。我们的方法是免费培训，不依赖任何标签监督。两个关键设计使我们能够使用现成的文本到图像扩散模型作为对象实例和掩码注释的有用数据集生成器。首先，我们将图像画布划分为多个区域，并执行单轮扩散过程，以根据不同的文本提示同时生成多个实例。其次，我们通过跨层和扩散时间步长聚合与对象提示相关的交叉注意力图，然后进行简单的阈值处理和边缘感知细化处理，来获得相应的实例掩码。在没有铃声和口哨声的情况下，我们的MosaicFusion可以为罕见和新颖的类别产生大量的合成标记数据。在具有挑战性的LVIS长尾和开放词汇基准上的实验结果表明，MosaicFusion可以显著提高现有实例分割模型的性能，尤其是对于罕见和新颖的类别。代码将在发布https://github.com/Jiahao000/MosaicFusion. et.al.|[2309.13042](http://arxiv.org/abs/2309.13042)|**[link](https://github.com/jiahao000/mosaicfusion)**|
|**2023-09-22**|**Free fermions with dephasing and boundary driving: Bethe Ansatz results**|通过使用Lindblad方程，我们导出了长度为 $L$的自由费米子链在体相移和边界损耗的作用下两点相关器的演化。我们使用Bethe ansatz对控制相关器动力学的Liouvillian$｛\mathcal L｝^｛\scriptscriptstyle（2）｝$进行对角化。它的大部分能级是复杂的。准确地说，$L（L-1）/2$复能不依赖于去相位，除了一个微不足道的偏移。对于大的$L$ ，剩余的复杂能级与非相位无关的能级扰动相关。长期动力学是由一个包含大量能级的实能量带控制的。它们在可以忽略边界的中间时间产生扩散缩放。此外，它们对渐近长时间扩散的破坏进行了编码。有趣的是，对于大损耗率，频谱中出现了两种边界模式。实能量对应于Bethe方程的弦解，并且可以有效地处理大链。这使我们能够导出费米子密度动力学的紧凑公式。我们对照精确对角化来检验我们的结果，发现完全一致。 et.al.|[2309.12978](http://arxiv.org/abs/2309.12978)|null|
|**2023-09-22**|**Diffusion Augmentation for Sequential Recommendation**|序列推荐（SRS）已成为最近许多应用程序的技术基础，旨在根据用户的历史交互来推荐下一个项目。然而，序列推荐经常面临数据稀疏的问题，这在推荐系统中广泛存在。此外，大多数用户只与少数项目进行交互，但现有的SRS模型往往不如这些用户。这样一个被称为长尾用户问题的问题还有待解决。数据扩充是缓解这两个问题的一种独特方式，但它们通常需要捏造的训练策略，或者受到低质量生成的交互的阻碍。为了解决这些问题，我们提出了一种用于更高质量生成的序列推荐的扩散增强（DiffuASR）。DiffuASR的增强数据集可以直接用于训练序列推荐模型，而不需要复杂的训练过程。为了充分利用扩散模型的生成能力，我们首先提出了一种基于扩散的伪序列生成框架，以填补图像生成和序列生成之间的空白。然后，设计了一个序列U-Net，以使扩散噪声预测模型U-Net适应离散序列生成任务。最后，我们提出了两种引导策略来同化生成序列和起源序列之间的偏好。为了验证所提出的DiffuASR，我们在三个具有三个顺序推荐模型的真实世界数据集上进行了大量实验。实验结果验证了DiffuASR的有效性。据我们所知，DiffuASR是将扩散模型引入推荐的先驱之一。 et.al.|[2309.12858](http://arxiv.org/abs/2309.12858)|null|
|**2023-09-22**|**Accuracy and stability analysis of horizontal discretizations used in unstructured grid ocean models**|我们用来评估全球环流模型（GCM）稳健性的一个重要工具是了解浅水近似下动力核心的水平离散化。在这里，我们评估了在考虑浅水模型的非结构化海洋模型中使用或适用的不同方法的准确性和稳定性。我们的结果表明，这两种方案具有不同的精度能力，A-（NICAM）和B-网格（FeSOM 2.0）方案在大多数算子和时间积分变量中至少提供了一阶精度，而两种C-网格（ICON和MPAS）方案在充分近似水平动力学方面表现出更大的困难。此外，规则网格上的惯性重力波表示理论可以扩展到我们基于非结构化的方案，其中从最小到最精确分别为：A-、B和C-网格。仅考虑C网格方案，MPAS方案显示出比ICON更准确的惯性重力波表示。在稳定性方面，我们发现A和C网格MPAS方案都表现出最好的稳定性，但A网格方案依赖于人工扩散，而C网格方案则不依赖。同时，B网格和C网格ICON方案在最不稳定的范围内。最后，为了理解ICON中潜在不稳定性的影响，我们注意到，没有过滤项的完整3D模型不会随着时间的推移而不稳定。然而，杂散振荡是降低洋流动能的原因。此外，还观察到洋流的湍流动能进一步下降，产生了虚假的混合，这也在这些洋流强度下降中发挥了作用。 et.al.|[2309.12832](http://arxiv.org/abs/2309.12832)|null|
|**2023-09-22**|**Synthetic Boost: Leveraging Synthetic Data for Enhanced Vision-Language Segmentation in Echocardiography**|准确的分割对于基于超声心动图的心血管疾病（CVD）评估至关重要。然而，超声医师之间的可变性和超声图像的固有挑战阻碍了精确分割。通过利用图像和文本模态的联合表示，视觉语言分割模型（VLSM）可以包含丰富的上下文信息，有助于准确和可解释的分割。然而，超声心动图缺乏现成的数据，阻碍了VLSM的训练。在本研究中，我们探索使用语义扩散模型（SDM）的合成数据集来增强VLSM用于超声心动图分割。我们使用七种不同类型的语言提示来评估两种流行VLSM（CLIPSeg和CRIS）的结果，这些语言提示来自于从超声心动图图像、分割掩码及其元数据中自动提取的几个属性。我们的结果表明，在对真实图像进行微调之前，在SDM生成的合成图像上预训练VLSM时，改进了度量并加快了收敛速度。代码、配置和提示可在https://github.com/naamiinepal/synthetic-boost. et.al.|[2309.12829](http://arxiv.org/abs/2309.12829)|**[link](https://github.com/naamiinepal/synthetic-boost)**|
|**2023-09-22**|**DurIAN-E: Duration Informed Attention Network For Expressive Text-to-Speech Synthesis**|本文介绍了一种改进的持续时间知情注意神经网络（DurIAN-E），用于表达性和高保真度的文本到语音（TTS）合成。继承了原始的DurIAN模型，采用了自回归模型结构，其中从持续时间模型推断输入语言信息和输出声学特征之间的对齐。同时，所提出的DurIAN-E利用多个堆叠的基于SwishRNN的Transformer块作为语言编码器。风格自适应实例规范化（SAIN）层被用于帧级编码器，以提高表达性的建模能力。结合mel声谱图的去噪扩散概率模型（DDPM）和SAIN模块，进行了一种去噪器，以进一步提高合成语音的质量和表现力。实验结果证明，本文提出的表达型TTS模型在主观平均意见得分（MOS）和偏好测试中都比现有方法具有更好的性能。 et.al.|[2309.12792](http://arxiv.org/abs/2309.12792)|null|
|**2023-09-22**|**Semantic Change Driven Generative Semantic Communication Framework**|新兴的生成人工智能技术为语义通信（SemCom）框架的发展提供了新的见解。这些框架有可能解决与现有SemCom框架的现有端到端训练方式中固有的黑匣子性质相关的挑战，以及基于深度学习的语义通信中不可避免的错误下限导致的用户体验恶化。在本文中，我们关注广泛的远程监控场景，并提出了一个语义变化驱动的生成SemCom框架。其中，语义编码器和语义解码器可以独立地进行优化。具体来说，我们开发了一个具有基于信息值的语义采样功能的模块化语义编码器。此外，我们提出了一种条件去噪扩散概率模式辅助语义解码器，该解码器依赖于从源接收的语义信息，即语义图和局部静态场景信息来远程再生场景。此外，我们通过仿真证明了所提出的语义编码器和解码器的有效性，以及在降低能耗方面的巨大潜力。代码可在https://github.com/wty2011jl/SCDGSC.git et.al.|[2309.12775](http://arxiv.org/abs/2309.12775)|null|
|**2023-09-22**|**Coverage Dependent H $_2$ Desorption Energy: a Quantitative Explanation Based on Encounter Desorption Mechanism**|最近的实验表明，H$_2$在类金刚石碳（DLC）表面的解吸能取决于表面的H$_2$。我们的目的是定量解释实验测量的与覆盖率相关的H$_2$解吸能。基于相遇-解吸机制，导出了计算有效H$_2$解吸能的数学公式。有效的H$_2$解吸能取决于两个关键参数，即H$_2$~（2+）在H$_2$1衬底上的解吸能和H$_2$2扩散势垒与其解吸能的比值。如果在计算中使用文献中这两个参数的值，则计算的有效H$_2$解吸能与实验测量的与覆盖相关的H$_2$解吸能定性一致。我们认为，有效H$_2$ 解吸能与实验结果之间的差异是由于缺乏对这两个参数的了解。因此，我们根据实验数据重新计算这两个参数。如果在计算中使用这两个更新的参数，可以在理论和实验结果之间获得良好的一致性。 et.al.|[2309.12587](http://arxiv.org/abs/2309.12587)|null|
|**2023-09-21**|**A Diffusion-Model of Joint Interactive Navigation**|自动驾驶汽车系统的模拟要求模拟的交通参与者表现出多样化和现实的行为。在模拟中使用预先录制的真实世界交通场景确保了真实性，但安全关键事件的罕见性使得大规模收集驾驶场景的成本高昂。在本文中，我们提出了一种基于扩散的交通场景生成方法DJINN。我们的方法以过去、现在或未来的一组灵活的状态观测为条件，共同扩散所有主体的轨迹。在流行的轨迹预测数据集上，我们报告了联合轨迹度量的最新性能。此外，我们还演示了DJNN如何灵活地从各种有价值的条件分布中实现直接测试时间采样，包括基于目标的采样、行为类采样和场景编辑。 et.al.|[2309.12508](http://arxiv.org/abs/2309.12508)|null|
|**2023-09-21**|**License Plate Super-Resolution Using Diffusion Models**|在监控中，车牌的质量低、尺寸小，影响了识别精度，从而阻碍了准确识别车牌。尽管在基于人工智能的图像超分辨率方面取得了进步，但卷积神经网络（CNNs）和生成对抗性网络（GANs）等方法在增强车牌图像方面仍然存在不足。这项研究利用了尖端的扩散模型，该模型在图像恢复方面一直优于其他深度学习技术。通过使用沙特车牌的精选数据集以低分辨率和高分辨率对该模型进行训练，我们发现了扩散模型的优越性。与SwinIR和ESRGAN相比，该方法的峰值信噪比分别提高了12.55%和37.32%。此外，我们的方法在结构相似性指数（SSIM）方面超过了这些技术，分别比SwinIR和ESRGAN提高了4.89%和17.66%。此外，92%的人类评估者更喜欢我们的图像，而不是其他算法的图像。从本质上讲，这项研究为车牌超分辨率提供了一个开创性的解决方案，在监控系统中具有明显的潜力。 et.al.|[2309.12506](http://arxiv.org/abs/2309.12506)|null|

<p align=right>(<a href=#updated-on-20230925>back to top</a>)</p>

## NeRF

|Publish Date|Title|Abstract|PDF|Code|
|---|---|---|---|---|
|**2023-09-22**|**NOC: High-Quality Neural Object Cloning with 3D Lifting of Segment Anything**|随着神经领域的发展，从多视图输入重建目标物体的3D模型最近越来越受到社会的关注。现有的方法通常学习整个场景的神经场，而如何在飞行中重建用户指示的特定对象仍在探索之中。考虑到分段任意模型（SAM）在分割任何2D图像方面都显示出了有效性，本文提出了一种新的高质量3D对象重建方法——神经对象克隆（NOC），它从两个方面利用了神经场和SAM的优点。首先，为了将目标对象从场景中分离出来，我们提出了一种新的策略，将SAM的多视图2D分割掩模提升到一个统一的3D变化场中。然后，3D变化场被投影到2D空间中，并生成SAM的新提示。这个过程是迭代的，直到收敛，以将目标对象从场景中分离出来。然后，除了2D掩模之外，我们进一步将SAM编码器的2D特征提升到3D SAM场中，以提高目标对象的重建质量。NOC将SAM的2D掩模和特征提升到3D神经场中，用于高质量的目标对象重建。我们在几个基准数据集上进行了详细的实验，以证明我们的方法的优势。代码将被发布。 et.al.|[2309.12790](http://arxiv.org/abs/2309.12790)|null|
|**2023-09-15**|**Breathing New Life into 3D Assets with Generative Repainting**|基于扩散的文本到图像模型引发了视觉社区、艺术家和内容创作者的巨大关注。这些模型的广泛采用是由于世代质量的显著提高以及对各种模式的有效调节，而不仅仅是文本。然而，将这些2D模型的丰富生成先验提升到3D中是具有挑战性的。最近的工作提出了由扩散模型和神经场的纠缠提供动力的各种管道。我们探索了预训练的2D扩散模型和标准3D神经辐射场作为独立工具的威力，并展示了它们以非学习方式协同工作的能力。这种模块化具有易于部分升级的内在优势，这在这样一个快节奏的领域中成为了一个重要的特性。我们的管道接受任何遗留的可渲染几何体，如纹理或无纹理网格，协调2D生成细化和3D一致性强制工具之间的交互，并以多种格式输出绘制的输入几何体。我们对ShapeNetSem数据集中的广泛对象和类别进行了大规模研究，并从定性和定量两个方面展示了我们方法的优势。项目页面：https://www.obukhov.ai/repainting_3d_assets et.al.|[2309.08523](http://arxiv.org/abs/2309.08523)|**[link](https://github.com/kongdai123/repainting_3d_assets)**|
|**2023-09-14**|**Neural Field Representations of Articulated Objects for Robotic Manipulation Planning**|传统的操作规划方法依赖于环境的显式几何模型来将给定任务公式化为优化问题。然而，从原始传感器输入推断准确的模型本身就是一个难题，尤其是对于铰接物体（例如壁橱、抽屉）。在本文中，我们提出了一种关节对象的神经场表示（NFR），可以直接从图像中进行操作规划。具体来说，在拍摄了一个新的关节物体的几张照片后，我们可以向前模拟它可能的运动，因此，可以直接使用该神经模型进行轨迹优化规划。此外，这种表示可以用于形状重建、语义分割和图像渲染，这在训练和泛化过程中提供了强大的监督信号。我们表明，我们的模型仅在合成图像上训练，能够在模拟和真实图像中为同类看不见的物体提取有意义的表示。此外，我们证明了该表示能够直接从图像中对现实世界中的关节物体进行机器人操作。 et.al.|[2309.07620](http://arxiv.org/abs/2309.07620)|null|
|**2023-09-13**|**Generalizable Neural Fields as Partially Observed Neural Processes**|神经场将信号表示为由神经网络参数化的函数，是传统离散矢量或基于网格的表示的一种很有前途的替代方案。与离散表示相比，神经表示既能很好地扩展分辨率，又是连续的，并且可以是多次可微的。然而，给定我们想要表示的信号数据集，必须为每个信号优化单独的神经场是低效的，并且不能利用信号之间的共享信息或结构。现有的泛化方法将其视为元学习问题，并采用基于梯度的元学习来学习初始化，然后通过测试时间优化对初始化进行微调，或者学习超网络来产生神经场的权重。相反，我们提出了一种新的范式，将神经表征的大规模训练视为部分观察到的神经过程框架的一部分，并利用神经过程算法来解决这一任务。我们证明，这种方法优于最先进的基于梯度的元学习方法和超网络方法。 et.al.|[2309.06660](http://arxiv.org/abs/2309.06660)|null|
|**2023-09-08**|**Single View Refractive Index Tomography with Neural Fields**|折射率层析成像是一个反问题，我们试图从2D投影图像测量中重建场景的3D折射场。折射场本身是不可见的，而是影响光线在空间中传播时路径的连续弯曲。折射场出现在各种各样的科学应用中，从显微镜中的半透明细胞样本到弯曲来自遥远星系的光的暗物质场。这个问题带来了一个独特的挑战，因为折射场直接影响光的路径，使其恢复成为一个非线性问题。此外，与传统的层析成像相比，我们试图通过利用散射在整个介质中的光源的知识，仅从单个视点使用投影图像来恢复折射场。在这项工作中，我们介绍了一种使用基于坐标的神经网络对场景中潜在的连续折射场进行建模的方法。然后，我们使用射线三维空间曲率的显式建模来优化该网络的参数，通过综合分析方法重建折射场。通过在模拟中恢复折射场，并分析光源分布对恢复的影响，证明了我们方法的有效性。然后，我们在模拟暗物质映射问题上测试了我们的方法，在该问题中，我们恢复了真实模拟暗物质分布下的折射场。 et.al.|[2309.04437](http://arxiv.org/abs/2309.04437)|null|
|**2023-09-07**|**BluNF: Blueprint Neural Field**|神经辐射场（NeRF）彻底改变了场景新颖的视图合成，提供了视觉逼真、精确和稳健的隐式重建。虽然最近的方法允许NeRF编辑，例如对象删除、3D形状修改或材料特性操纵，但在这种编辑之前的手动注释使该过程变得乏味。此外，传统的2D交互工具缺乏对3D空间的准确感知，阻碍了对场景的精确操作和编辑。在本文中，我们介绍了一种新的方法，称为蓝图神经场（BluNF），以解决这些编辑问题。BluNF提供了一个强大且用户友好的2D蓝图，实现了直观的场景编辑。通过利用隐式神经表示，BluNF使用先前的语义和深度信息构建场景的蓝图。生成的蓝图可以轻松编辑和操作NeRF表示。我们通过直观的点击和更改机制展示了BluNF的可编辑性，实现了3D操作，如遮罩、外观修改和对象移除。我们的方法对视觉内容创作做出了重大贡献，为该领域的进一步研究铺平了道路。 et.al.|[2309.03933](http://arxiv.org/abs/2309.03933)|null|
|**2023-09-07**|**SimNP: Learning Self-Similarity Priors Between Neural Points**|用于3D对象重建的现有神经场表示要么（1）利用对象级表示，但由于对全局潜在代码的限制而遭受低质量细节，要么（2）能够完美地重建观测，但未能利用对象级先验知识来推断未观察到的区域。我们提出了一种学习类别级自相似性的方法SimNP，它通过将神经点辐射场与类别级自类似性表示相连接，结合了两个世界的优点。我们的贡献是双重的。（1） 我们利用相干点云的概念设计了第一个类别级别的神经点表示。由此产生的神经点辐射场为局部支持的对象区域存储了高级别的细节。（2） 我们了解了如何以无约束和无监督的方式在神经点之间共享信息，这允许在重建过程中根据给定的观测值导出对象的未观察区域。我们表明，SimNP在重建对称的看不见物体区域方面优于以前的方法，超过了建立在类别级或像素对齐辐射场上的方法，同时提供了实例之间的语义对应 et.al.|[2309.03809](http://arxiv.org/abs/2309.03809)|null|
|**2023-09-06**|**CoNeS: Conditional neural fields with shift modulation for multi-sequence MRI translation**|多序列磁共振成像（MRI）在现代临床研究和深度学习研究中都有广泛的应用。然而，在临床实践中，由于患者的不同图像采集协议或造影剂禁忌症，经常会出现一个或多个MRI序列缺失的情况，这限制了在多序列数据上训练的深度学习模型的使用。一种很有前途的方法是利用生成模型来合成缺失的序列，这可以作为替代获取。解决这一问题的最先进方法是基于卷积神经网络（CNN），该网络通常存在频谱偏差，导致高频精细细节的重建较差。在本文中，我们提出了具有移位调制的条件神经场（CoNeS），这是一种以体素坐标为输入并学习用于多序列MRI平移的目标图像的表示的模型。所提出的模型使用多层感知器（MLP）代替CNN作为像素到像素映射的解码器。因此，每个目标图像被表示为神经场，该神经场通过利用学习的潜码的移位调制而被调节在源图像上。在BraTS 2018和前庭神经鞘瘤患者的内部临床数据集上进行的实验表明，所提出的方法在视觉和定量上都优于最先进的多序列MRI翻译方法。此外，我们进行了光谱分析，表明CoNeS能够克服传统CNN模型中常见的光谱偏差问题。为了进一步评估合成图像在临床下游任务中的使用，我们在推理时使用合成图像测试了分割网络。 et.al.|[2309.03320](http://arxiv.org/abs/2309.03320)|**[link](https://github.com/cyjdswx/cones)**|
|**2023-09-06**|**ResFields: Residual Neural Fields for Spatiotemporal Signals**|神经场是一类被训练来表示高频信号的神经网络，近年来由于其在复杂三维数据建模方面的出色性能，特别是通过单个多层感知器（MLP）的大神经符号距离（SDFs）或辐射场（NeRFs），而受到了极大的关注。然而，尽管用MLP表示信号的能力和简单性很强，但由于MLP的容量有限，这些方法在建模大而复杂的时间信号时仍然面临挑战。在本文中，我们提出了一种有效的方法来解决这一限制，将时间残差层纳入神经场，称为ResFields，这是一类专门设计用于有效表示复杂时间信号的新型网络。我们对ResFields的性质进行了全面的分析，并提出了一种矩阵分解技术来减少可训练参数的数量并增强泛化能力。重要的是，我们的公式与现有技术无缝集成，并在各种具有挑战性的任务中持续改进结果：2D视频近似、通过时间SDF的动态形状建模和动态NeRF重建。最后，我们通过展示ResFields在从轻量级捕捉系统的稀疏感官输入捕捉动态3D场景方面的有效性，展示了它的实用性。 et.al.|[2309.03160](http://arxiv.org/abs/2309.03160)|**[link](https://github.com/markomih/ResFields)**|
|**2023-09-01**|**GNFactor: Multi-Task Real Robot Learning with Generalizable Neural Feature Fields**|开发能够在非结构化现实世界环境中通过视觉观察执行各种操作任务的代理是机器人技术中的一个长期问题。为了实现这一目标，机器人需要对场景的3D结构和语义有全面的了解。在这项工作中，我们提出了 $\textbf｛GNFactor｝$，一种用于多任务机器人操作的视觉行为克隆代理，具有$\textbf｛G｝$通用$\textbf｛N｝$eural功能$\textbf｛F｝$字段。GNFactor联合优化了作为重建模块的可推广神经场（GNF）和作为决策模块的感知转换器，利用了共享的深度3D体素表示。为了在3D中结合语义，重建模块利用视觉语言基础模型（$\textit｛例如｝$ ，Stable Diffusion）将丰富的语义信息提取到深度3D体素中。我们在3个真实机器人任务中评估了GNFactor，并在10个RLBench任务中进行了详细的消融，演示次数有限。我们观察到GNFactor在可见和不可见任务中比当前最先进的方法有了实质性的改进，证明了GNFactor强大的泛化能力。我们的项目网站是https://yanjieze.com/GNFactor/。 et.al.|[2308.16891](http://arxiv.org/abs/2308.16891)|**[link](https://github.com/YanjieZe/GNFactor)**|

<p align=right>(<a href=#updated-on-20230925>back to top</a>)</p>

[contributors-shield]: https://img.shields.io/github/contributors/Vincentqyw/cv-arxiv-daily.svg?style=for-the-badge
[contributors-url]: https://github.com/Vincentqyw/cv-arxiv-daily/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/Vincentqyw/cv-arxiv-daily.svg?style=for-the-badge
[forks-url]: https://github.com/Vincentqyw/cv-arxiv-daily/network/members
[stars-shield]: https://img.shields.io/github/stars/Vincentqyw/cv-arxiv-daily.svg?style=for-the-badge
[stars-url]: https://github.com/Vincentqyw/cv-arxiv-daily/stargazers
[issues-shield]: https://img.shields.io/github/issues/Vincentqyw/cv-arxiv-daily.svg?style=for-the-badge
[issues-url]: https://github.com/Vincentqyw/cv-arxiv-daily/issues

