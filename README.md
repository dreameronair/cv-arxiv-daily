[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]

## Updated on 2023.09.11
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
|**2023-09-07**|**SyncDreamer: Generating Multiview-consistent Images from a Single-view Image**|在本文中，我们提出了一种新的扩散模型，称为，从单视图图像生成多视图一致图像。最近的工作Zero123使用预先训练的大规模2D扩散模型，展示了从物体的单视图图像生成看似新颖的视图的能力。然而，为生成的图像保持几何图形和颜色的一致性仍然是一个挑战。为了解决这个问题，我们提出了一种同步多视点扩散模型，该模型对多视点图像的联合概率分布进行建模，从而能够在单个反向过程中生成多视点一致图像。SyncDreamer通过3D感知特征注意力机制在反向过程的每一步同步所有生成图像的中间状态，该机制将不同视图中的相应特征关联起来。实验表明，SyncDreamer生成的图像在不同视图之间具有高度一致性，因此非常适合各种3D生成任务，如新颖的视图合成、文本到3D和图像到3D。 et.al.|[2309.03453](http://arxiv.org/abs/2309.03453)|null|
|**2023-09-06**|**Bayes' Rays: Uncertainty Quantification for Neural Radiance Fields**|神经辐射场（NeRF）在视图合成和深度估计等应用中显示出了前景，但从多视图图像中学习面临着固有的不确定性。目前量化它们的方法要么是启发式的，要么是计算要求很高的。我们引入了BayesRays，这是一个事后框架，用于在不修改训练过程的情况下评估任何预先训练的NeRF中的不确定性。我们的方法使用空间扰动和贝叶斯拉普拉斯近似来建立体积不确定性场。我们从统计角度推导了我们的算法，并在关键指标和应用中展示了其卓越的性能。其他结果可在：https://bayesrays.github.io. et.al.|[2309.03185](http://arxiv.org/abs/2309.03185)|null|
|**2023-09-05**|**TiAVox: Time-aware Attenuation Voxels for Sparse-view 4D DSA Reconstruction**|四维数字减影血管造影（4D DSA）在许多医学疾病的诊断中起着至关重要的作用，如动静脉畸形（AVM）和动静脉瘘（AVF）。尽管4D DSA的重建具有重要的应用价值，但它需要大量的视图来有效地模拟复杂的血管和放射造影流，从而意味着显著的辐射剂量。为了解决这个高辐射问题，我们提出了一种用于稀疏视图4D DSA重建的时间感知衰减体素（TiAVox）方法，为高质量的4D成像铺平了道路。此外，可以从重建的4D DSA图像生成2D和3D DSA成像结果。TiAVox引入了4D衰减体素网格，从空间和时间维度反映衰减特性。它通过最小化渲染图像和稀疏2D DSA图像之间的差异来进行优化。在没有任何神经网络参与的情况下，TiAVox享有特定的物理可解释性。每个可学习体素的参数表示衰减系数。我们在临床和模拟数据集上验证了TiAVox方法，在临床来源的数据集上仅使用30个视图，就实现了31.23的新视图合成峰值信噪比（PSNR），而传统的Feldkamp-Davis-Kress方法需要133个视图。类似地，在合成数据集中只有10个视图的情况下，TiAVox对于新视图合成产生了34.32的PSNR，对于3D重建产生了41.40的PSNR。我们还进行了消融研究，以证实TiAVox的主要成分。该代码将公开提供。 et.al.|[2309.02318](http://arxiv.org/abs/2309.02318)|null|
|**2023-09-06**|**Instant Continual Learning of Neural Radiance Fields**|神经辐射场（NeRFs）已成为一种有效的视图合成和三维场景重建方法。然而，传统的训练方法需要在场景优化期间访问所有训练视图。在连续学习场景中，这种假设可能是禁止的，在这种场景中，以顺序的方式获取新数据，并且需要NeRF的连续更新，如在汽车或遥感应用中。当在这样一个持续的环境中天真地训练时，传统的场景表示框架会遭受灾难性的遗忘，在对新数据进行训练后，先前学习的知识会被破坏。先前使用NeRF缓解遗忘的工作存在重建质量低和延迟高的问题，这使得它们在现实世界中的应用不切实际。我们提出了一个用于训练NeRF的持续学习框架，该框架利用了基于回放的方法与显-隐混合场景表示相结合。当在连续环境中训练时，我们的方法在重建质量方面优于以前的方法，同时具有更快一个数量级的额外好处。 et.al.|[2309.01811](http://arxiv.org/abs/2309.01811)|null|
|**2023-09-04**|**EMR-MSF: Self-Supervised Recurrent Monocular Scene Flow Exploiting Ego-Motion Rigidity**|自监督单目场景流估计旨在从两个时间连续的单目图像中理解3D结构和3D运动，由于其简单经济的传感器设置而受到越来越多的关注。然而，当前方法的准确性受到网络架构效率较低和缺乏正则化运动刚度的瓶颈的影响。在本文中，我们借鉴了监督学习范围下网络架构设计的优势，提出了一个名为EMR-MSF的高级模型。我们通过精心构建的自我运动聚合模块进一步施加了显式和鲁棒的几何约束，其中提出了刚性软掩模来过滤动态区域，以便使用静态区域进行稳定的自我运动估计。此外，我们提出了运动一致性损失和掩码正则化损失，以充分利用静态区域。集成了几种有效的训练策略，包括梯度分离技术和增强的视图合成过程，以获得更好的表现。我们提出的方法在很大程度上优于以前的自监督工作，并赶上了监督方法的性能。在KITTI场景流基准上，我们的方法将最先进的自监督单目方法的SF all指标提高了44%，并在包括深度和视觉里程计在内的子任务以及其他自监督单任务或多任务方法中表现出优异的性能。 et.al.|[2309.01296](http://arxiv.org/abs/2309.01296)|null|
|**2023-09-03**|**Turn Fake into Real: Adversarial Head Turn Attacks Against Deepfake Detection**|恶意使用deepfakes会引起公众的严重关注，并降低人们对数字媒体的信任。尽管已经提出了有效的深度伪造检测器，但它们在很大程度上容易受到对抗性攻击。为了评估检测器的鲁棒性，最近的研究探索了各种攻击。然而，所有现有的攻击都局限于2D图像扰动，很难转化为现实世界中的面部变化。在本文中，我们提出了对抗性头转向（AdvHeat），这是针对深度伪造检测器的3D对抗性人脸视图的首次尝试，基于从单视图伪造图像中合成人脸视图。大量实验验证了各种探测器在现实的黑盒场景中对AdvHeat的脆弱性。例如，基于简单随机搜索的AdvHeat在360个搜索步骤中获得了96.8%的高攻击成功率。当允许额外的查询访问时，我们可以进一步将步骤预算减少到50。额外的分析表明，AdvHeat在交叉检测器的可转移性和对防御的鲁棒性方面都优于传统攻击。AdvHeat生成的对抗性图像也显示出自然的外观。我们的代码，包括为FaceForensics++的1000个ID中的每个ID生成由360个合成视图组成的多视图数据集的代码，可在https://github.com/twowwj/AdvHeaT. et.al.|[2309.01104](http://arxiv.org/abs/2309.01104)|null|
|**2023-08-29**|**Pose-Free Neural Radiance Fields via Implicit Pose Regularization**|无姿态神经辐射场（NeRF）旨在用未经处理的多视图图像训练NeRF，近年来取得了令人印象深刻的成功。大多数现有工作共享一个管道，首先用渲染图像训练粗略的姿态估计器，然后联合优化估计的姿态和神经辐射场。然而，由于姿态估计器仅用渲染图像进行训练，由于真实图像和渲染图像之间的域间隙，姿态估计通常对真实图像有偏差或不准确，导致真实图像的姿态估计鲁棒性差，并且在联合优化中存在进一步的局部最小值。我们设计了IR NeRF，这是一种创新的无姿态NeRF，它引入了隐式姿态正则化来改进未聚焦真实图像的姿态估计器，并提高了真实图像姿态估计的鲁棒性。通过特定场景的2D图像的集合，IR NeRF构建了一个场景码本，该场景码本存储场景特征，并隐式地捕捉特定场景的姿势分布作为先验。因此，根据只有当2D真实图像的估计姿势位于姿势分布内时才可以从场景码本很好地重建2D真实图像这一原理，可以利用场景先验来提高姿势估计的鲁棒性。大量实验表明，IR NeRF实现了卓越的新视图合成，并在多个合成和真实数据集上始终优于最先进的视图合成。 et.al.|[2308.15049](http://arxiv.org/abs/2308.15049)|null|
|**2023-08-28**|**CLNeRF: Continual Learning Meets NeRF**|新颖的视图合成旨在呈现给定一组校准图像的看不见的视图。在实际应用中，场景的覆盖范围、外观或几何结构可能会随着时间的推移而变化，不断捕捉新的图像。有效地整合这种持续的变化是一个公开的挑战。标准NeRF基准测试仅涉及场景覆盖范围的扩展。为了研究其他实际的场景变化，我们提出了一个新的数据集，即跨时间世界（WAT），由外观和几何结构随时间变化的场景组成。我们还提出了一种简单而有效的方法CLNeRF，它将连续学习（CL）引入到神经辐射场（NeRF）中。CLNeRF结合了生成回放和即时神经图形原件（NGP）架构，以有效防止灾难性遗忘，并在新数据到达时有效更新模型。我们还向NGP添加了可训练的外观和几何嵌入，允许单个紧凑模型处理复杂的场景变化。在不需要存储历史图像的情况下，在变化场景的多次扫描上顺序训练的CLNeRF与在一次所有扫描上训练的上界模型性能相当。与其他CL基线相比，CLNeRF在标准基准和WAT上的表现要好得多。源代码和WAT数据集可在https://github.com/IntelLabs/CLNeRF.视频演示可在以下网址获得：https://youtu.be/nLRt6OoDGq0?si=8yD6k-8MMBJInQP et.al.|[2308.14816](http://arxiv.org/abs/2308.14816)|**[link](https://github.com/intellabs/clnerf)**|
|**2023-08-28**|**Flexible Techniques for Differentiable Rendering with 3D Gaussians**|快速、可靠的形状重建是许多计算机视觉应用中的重要组成部分。Neural Radiance Fields证明，真实感的新视图合成是触手可及的，但受到真实场景和对象快速重建性能要求的限制。最近的一些方法建立在替代形状表示的基础上，特别是3D高斯。我们开发了这些渲染器的扩展，例如集成可微分光流、导出防水网格和渲染每光线法线。此外，我们还展示了最近的两种方法是如何相互操作的。这些重建快速、稳健，并且可以在GPU或CPU上轻松执行。有关代码和可视化示例，请参见https://leonidk.github.io/fmb-plus et.al.|[2308.14737](http://arxiv.org/abs/2308.14737)|null|
|**2023-08-27**|**Depth self-supervision for single image novel view synthesis**|在本文中，我们解决了在给定单个帧作为输入的情况下从任意视点生成新图像的问题。虽然在这种设置中操作的现有方法旨在预测目标视图深度图以指导合成，但在没有明确监督此类任务的情况下，我们共同优化了新视图合成和深度估计的框架，以最大限度地释放两者之间的协同作用。具体地，以自监督的方式训练共享深度解码器，以预测在源视图和目标视图中一致的深度图。我们的结果证明了我们的方法在解决这两项任务的挑战方面的有效性，这两项工作允许生成更高质量的图像，并为目标视点提供更准确的深度。 et.al.|[2308.14108](http://arxiv.org/abs/2308.14108)|**[link](https://github.com/johnminelli/twowaysynth)**|

<p align=right>(<a href=#updated-on-20230911>back to top</a>)</p>

## 3D Reconstruction

|Publish Date|Title|Abstract|PDF|Code|
|---|---|---|---|---|
|**2023-09-07**|**A Food Package Recognition and Sorting System Based on Structured Light and Deep Learning**|基于视觉算法的机械臂抓取系统是一种可以应用于各种场景的机械臂系统。它使用算法自动识别目标的位置，并引导机械臂抓取目标，这比可教的机械臂抓取系统具有更灵活的特点。然而，对于一些食品包装来说，其透明包装或反射材料给视觉算法的识别带来了挑战，传统的视觉算法无法实现这些包装的高精度。此外，在机械臂抓取过程中，在z轴高度上的定位仍然需要手动设置参数，这可能会导致错误。基于上述两个问题，我们使用深度学习算法和结构光三维重建技术设计了一个食品包装分拣系统。使用预先训练好的MASK-R-CNN模型识别图像中物体的类别并获得其二维坐标，然后使用结构光三维重建技术计算其三维坐标，最后经过坐标系转换来引导机械臂进行抓取。经过测试表明，该方法可以实现对不同种类食品包装的全自动识别和抓取，具有较高的精度。使用这种方法，可以帮助食品制造商降低生产成本，提高生产效率。 et.al.|[2309.03704](http://arxiv.org/abs/2309.03704)|null|
|**2023-09-06**|**SADIR: Shape-Aware Diffusion Models for 3D Image Reconstruction**|从有限数量的2D图像重建3D图像一直是计算机视觉和图像分析中的一个长期挑战。虽然基于深度学习的方法在这一领域取得了令人印象深刻的性能，但现有的深度网络往往无法有效利用图像中呈现的对象的形状结构。因此，重建对象的拓扑结构可能无法很好地保存，导致不同部分之间存在诸如不连续性、孔洞或不匹配连接之类的伪影。在本文中，我们提出了一种基于扩散模型的三维图像重建形状感知网络，称为SADIR，以解决这些问题。与之前主要依赖图像强度的空间相关性进行3D重建的方法不同，我们的模型利用从训练数据中学习的形状先验来指导重建过程。为了实现这一点，我们开发了一个联合学习网络，该网络可以同时学习变形模型下的平均形状。然后，每个重建的图像被认为是平均形状的变形变体。我们在大脑和心脏磁共振成像（MRI）上验证了我们的模型SADIR。实验结果表明，我们的方法优于基线，具有更低的重建误差和更好地保留图像中物体的形状结构。 et.al.|[2309.03335](http://arxiv.org/abs/2309.03335)|null|
|**2023-09-06**|**Sparse 3D Reconstruction via Object-Centric Ray Sampling**|我们提出了一种新的方法，用于从360度校准的摄像机设备捕获的稀疏视图集重建3D对象。我们通过使用基于MLP的神经表示和三角形网格的混合模型来表示物体表面。我们工作中的一个关键贡献是一种新的以对象为中心的神经表示采样方案，其中光线在所有视图中共享。这有效地集中并减少了在每次迭代时用于更新神经模型的样本数量。此采样方案依赖于网格表示，以确保样本沿其法线良好分布。然后通过可微分渲染器有效地执行渲染。我们证明，这种采样方案可以更有效地训练神经表示，不需要对分割掩模进行额外监督，可以进行最先进的3D重建，并且可以在谷歌的扫描对象、坦克和寺庙以及MVMC汽车数据集上使用稀疏视图。 et.al.|[2309.03008](http://arxiv.org/abs/2309.03008)|null|
|**2023-09-06**|**Multi-log grasping using reinforcement learning and virtual visual servoing**|我们探索了使用强化学习和虚拟视觉伺服进行自动转发的多日志抓取。森林过程的自动化是一个重大挑战，由于非结构化和恶劣的户外环境，许多关于机器人控制的技术带来了不同的挑战。抓取多个原木涉及动力学和路径规划问题，其中抓斗、原木、地形和障碍物之间的交互需要视觉信息。为了解决这些挑战，我们将图像分割与起重机控制分离，并利用虚拟相机从3D重建数据中提供图像流。我们使用笛卡尔控制来简化域转移。由于原木桩是静态的，使用桩及其周围环境的3D重建进行视觉伺服相当于使用真实的相机数据直到抓取点。这放宽了图像分割挑战的计算资源和时间限制，并允许在原木堆未被遮挡的情况下收集数据。缺点是在抓取过程中缺乏信息。我们证明了这个问题是可以控制的，并且提供了一种代理，该代理在从具有挑战性的2-5根原木堆中挑选一根或几根原木时成功率为95%。 et.al.|[2309.02997](http://arxiv.org/abs/2309.02997)|null|
|**2023-09-06**|**Designing Situated Dashboards: Challenges and Opportunities**|情境可视化是一个新兴领域，它将可视化、增强现实、人机交互和物联网等多个领域结合在一起，以支持无处不在的世界中的人类数据活动。同样，仪表板广泛用于通过多个视图简化复杂数据。然而，仪表板仅适用于桌面设置，并且需要视觉策略来支持情境性。我们提出了基于AR的定位仪表盘的概念，并介绍了在与专家的访谈中提出的设计考虑因素和挑战。这些挑战旨在为促进定位仪表板的有效设计和创作提供方向和机会。 et.al.|[2309.02945](http://arxiv.org/abs/2309.02945)|null|
|**2023-09-06**|**LightNeuS: Neural Surface Reconstruction in Endoscopy using Illumination Decline**|我们提出了一种从单目内窥镜获取的图像序列进行3D重建的新方法。它基于两个关键的见解。首先，腔内腔是不透水的，这一特性是通过用符号距离函数对其进行建模而自然实现的。其次，场景照明是可变的。它来自内窥镜的光源，并随着与表面距离平方的倒数而衰减。为了利用这些见解，我们建立在NeuS之上，NeuS是一种神经隐式表面重建技术，具有从多个视图学习外观和SDF表面模型的卓越能力，但目前仅限于具有静态照明的场景。为了消除这一限制并利用像素亮度和深度之间的关系，我们修改了NeuS架构以明确说明这一点，并引入了内窥镜相机和光源的校准光度模型。我们的方法是第一个产生完整结肠切片的防水重建。我们在幻影图像上展示了卓越的准确性。值得注意的是，防水先验与光照下降相结合，可以以可接受的精度完成表面看不见部分的重建，为癌症筛查探索的自动质量评估铺平道路，测量观察到的粘膜的全球百分比。 et.al.|[2309.02777](http://arxiv.org/abs/2309.02777)|null|
|**2023-09-05**|**GO-SLAM: Global Optimization for Consistent 3D Instant Reconstruction**|最近，神经隐式表示在密集同时定位和映射（SLAM）方面取得了令人信服的结果，但在相机跟踪和重建中存在误差积累和失真。有目的地，我们提出了GO-SLAM，这是一种基于深度学习的密集视觉SLAM框架，用于实时全局优化姿态和三维重建。鲁棒姿态估计是其核心，由有效的闭环和在线全束调整支持，通过利用输入帧完整历史的学习全局几何来优化每帧。同时，我们动态更新隐式和连续曲面表示，以确保三维重建的全局一致性。在各种合成和真实世界数据集上的结果表明，GO-SLAM在跟踪鲁棒性和重建精度方面优于最先进的方法。此外，GO-SLAM是通用的，可以与单眼、立体声和RGB-D输入一起运行。 et.al.|[2309.02436](http://arxiv.org/abs/2309.02436)|null|
|**2023-09-05**|**Doppelgangers: Learning to Disambiguate Images of Similar Structures**|我们考虑的视觉消歧任务是确定一对视觉相似的图像是否描绘了相同或不同的3D表面（例如，对称建筑的相同或相反侧）。两张图像观察到不同但在视觉上相似的3D表面，这对人类来说可能很难区分，也可能导致3D重建算法产生错误的结果。我们提出了一种基于学习的视觉消歧方法，将其表述为图像对的二元分类任务。为此，我们为这个问题引入了一个新的数据集，即Doppelgangers，它包括具有基本事实标签的相似结构的图像对。我们还设计了一种网络架构，将局部关键点和匹配的空间分布作为输入，从而能够更好地对局部和全局线索进行推理。我们的评估表明，我们的方法可以在困难的情况下区分虚幻的匹配，并可以集成到SfM管道中，以产生正确的、消除歧义的3D重建。有关我们的代码、数据集和更多结果，请参阅我们的项目页面：http://doppelgangers-3d.github.io/. et.al.|[2309.02420](http://arxiv.org/abs/2309.02420)|**[link](https://github.com/RuojinCai/Doppelgangers)**|
|**2023-09-05**|**TiAVox: Time-aware Attenuation Voxels for Sparse-view 4D DSA Reconstruction**|四维数字减影血管造影（4D DSA）在许多医学疾病的诊断中起着至关重要的作用，如动静脉畸形（AVM）和动静脉瘘（AVF）。尽管4D DSA的重建具有重要的应用价值，但它需要大量的视图来有效地模拟复杂的血管和放射造影流，从而意味着显著的辐射剂量。为了解决这个高辐射问题，我们提出了一种用于稀疏视图4D DSA重建的时间感知衰减体素（TiAVox）方法，为高质量的4D成像铺平了道路。此外，可以从重建的4D DSA图像生成2D和3D DSA成像结果。TiAVox引入了4D衰减体素网格，从空间和时间维度反映衰减特性。它通过最小化渲染图像和稀疏2D DSA图像之间的差异来进行优化。在没有任何神经网络参与的情况下，TiAVox享有特定的物理可解释性。每个可学习体素的参数表示衰减系数。我们在临床和模拟数据集上验证了TiAVox方法，在临床来源的数据集上仅使用30个视图，就实现了31.23的新视图合成峰值信噪比（PSNR），而传统的Feldkamp-Davis-Kress方法需要133个视图。类似地，在合成数据集中只有10个视图的情况下，TiAVox对于新视图合成产生了34.32的PSNR，对于3D重建产生了41.40的PSNR。我们还进行了消融研究，以证实TiAVox的主要成分。该代码将公开提供。 et.al.|[2309.02318](http://arxiv.org/abs/2309.02318)|null|
|**2023-09-05**|**Iterative Superquadric Recomposition of 3D Objects from Multiple Views**|人类善于重组新物体，即他们可以识别未知物体之间的共性，从一般结构到更精细的细节，这是机器难以复制的能力。我们提出了一个框架ISCO，在不训练使用3D监督的模型的情况下，直接从2D视图使用3D超二次曲面作为语义部分来重新组合对象。为了实现这一点，我们优化了组成对象特定实例的超二次曲面参数，比较了其渲染的3D视图和2D图像轮廓。我们的ISCO框架在重建误差高的地方迭代地添加新的超二次曲面，首先提取目标对象的粗略区域，然后提取目标对象更精细的细节。通过这种简单的从粗到细的归纳偏差，ISCO为相关的对象部分提供了一致的超二次曲面，尽管没有任何语义监督。由于ISCO不训练任何神经网络，因此它对分布外的对象也具有固有的鲁棒性。实验表明，与最近的单实例超二次曲面重建方法相比，ISCO提供了持续更准确的3D重建，即使是从野外图像中也是如此。代码可在https://github.com/ExplainableML/ISCO。 et.al.|[2309.02102](http://arxiv.org/abs/2309.02102)|null|

<p align=right>(<a href=#updated-on-20230911>back to top</a>)</p>

## Diffusion

|Publish Date|Title|Abstract|PDF|Code|
|---|---|---|---|---|
|**2023-09-07**|**InstructDiffusion: A Generalist Modeling Interface for Vision Tasks**|我们介绍了InstructionDiffusion，这是一个统一的通用框架，用于将计算机视觉任务与人类指令相协调。与现有的集成先验知识并预先定义每个视觉任务的输出空间（例如，类别和坐标）的方法不同，我们将不同的视觉任务投射到人类直观的图像操作过程中，其输出空间是灵活和交互式的像素空间。具体来说，该模型建立在扩散过程的基础上，并根据用户指令进行训练以预测像素，例如用红色包围男子的左肩或在左车上戴蓝色口罩。InstructionDiffusion可以处理各种视觉任务，包括理解任务（如分割和关键点检测）和生成任务（如编辑和增强）。它甚至表现出处理看不见的任务的能力，并在新的数据集上优于先前的方法。这代表着向视觉任务的广义建模界面迈出了重要一步，推动了计算机视觉领域的人工通用智能。 et.al.|[2309.03895](http://arxiv.org/abs/2309.03895)|null|
|**2023-09-07**|**DiffusionEngine: Diffusion Model is Scalable Data Engine for Object Detection**|数据是深度学习的基石。本文揭示了最近开发的扩散模型是一个可扩展的对象检测数据引擎。现有的用于放大面向检测的数据的方法通常需要手动收集或生成模型来获得目标图像，然后进行数据扩充和标记以产生训练对，这是昂贵的、复杂的或缺乏多样性的。为了解决这些问题，我们提出了DiffusionEngine（DE），这是一个数据扩展引擎，可以在单个阶段提供高质量的面向检测的训练对。DE由预先训练的扩散模型和有效的检测适配器组成，有助于以即插即用的方式生成可扩展、多样和可推广的检测数据。检测适配器被学习来将现成的扩散模型中的隐含语义和位置知识与检测感知信号对齐，以做出更好的边界框预测。此外，我们贡献了两个数据集，即COCO-DE和VOC-DE，以扩大现有的检测基准，促进后续研究。大量实验表明，通过DE扩展数据可以在各种场景中实现显著改进，如各种检测算法、自监督预训练、数据稀疏、标签稀缺、跨域和半监督学习。例如，当使用DE和基于DINO的适配器来放大数据时，COCO的mAP提高了3.1%，VOC提高了7.6%，Clipart提高了11.5%。 et.al.|[2309.03893](http://arxiv.org/abs/2309.03893)|null|
|**2023-09-07**|**Text-to-feature diffusion for audio-visual few-shot learning**|从视听数据中训练用于视频分类的深度学习模型通常需要通过昂贵的过程收集大量的标记训练数据。一个具有挑战性且未被充分探索，但成本低得多的设置是从视频数据中很少拍摄学习。特别地，具有声音和视觉信息的视频数据的固有多模态特性尚未被广泛用于少镜头视频分类任务。因此，我们在VGGSound FSL、UCF-FSL、ActivityNet FSL三个数据集上引入了一个统一的视听少镜头视频分类基准，并对十种方法进行了调整和比较。此外，我们提出了AV-DIFF，一种文本到特征的扩散框架，它首先通过跨模态注意力融合时间和视听特征，然后为新类生成多模态特征。我们表明，AV-DIFF在我们提出的视听（广义）少镜头学习基准上获得了最先进的性能。当只有有限的标记数据可用时，我们的基准为有效的视听分类铺平了道路。代码和数据可在https://github.com/ExplainableML/AVDIFF-GFSL. et.al.|[2309.03869](http://arxiv.org/abs/2309.03869)|null|
|**2023-09-07**|**Early warning via transitions in latent stochastic dynamical systems**|在许多现实世界的应用中，如基因突变、脑疾病、自然灾害、金融危机和工程可靠性，对复杂系统或高维观测数据中的动态转变的早期预警至关重要。为了有效地提取预警信号，我们开发了一种新的方法：定向各向异性扩散图，它捕捉了低维流形中潜在的进化动力学。将该方法应用于真实的脑电图数据，我们成功地找到了合适的有效坐标，并导出了能够检测状态转换过程中临界点的预警信号。我们的方法将潜在的动力学与原始数据集联系起来。通过数值实验，从密度和跃迁概率方面验证了该框架的准确性和有效性。结果表明，第二坐标为各种评价指标中的临界转变提供了有意义的信息。 et.al.|[2309.03842](http://arxiv.org/abs/2309.03842)|null|
|**2023-09-07**|**Phasic Content Fusing Diffusion Model with Directional Distribution Consistency for Few-Shot Model Adaption**|用有限数量的样本训练生成模型是一项具有挑战性的任务。目前的方法主要依靠少镜头模型自适应来训练网络。然而，在数据极其有限（小于10）的情况下，生成网络往往会过度拟合，并遭受内容退化。为了解决这些问题，我们提出了一种新的阶段性内容融合的具有方向分布一致性损失的少镜头扩散模型，该模型在扩散模型的不同训练阶段针对不同的学习目标。具体而言，我们设计了一种具有阶段性内容融合的阶段性训练策略，以帮助我们的模型在t较大时学习内容和风格信息，在t较小时学习目标域的局部细节，从而提高对内容、风格和局部细节的捕获。此外，我们引入了一种新的方向分布一致性损失，它比现有方法更有效、更稳定地确保了生成分布和源分布之间的一致性，防止了我们的模型过拟合。最后，我们提出了一种跨领域结构指导策略，以增强领域自适应过程中的结构一致性。理论分析、定性和定量实验表明，与最先进的方法相比，我们的方法在少数镜头生成模型自适应任务中具有优势。源代码位于：https://github.com/sjtuplayer/few-shot-diffusion. et.al.|[2309.03729](http://arxiv.org/abs/2309.03729)|null|
|**2023-09-07**|**Prospects for $γ$-ray observations of the Perseus galaxy cluster with the Cherenkov Telescope Array**|星系团预计将是暗物质（DM）的储存库和宇宙射线质子（CRp）的储藏室，这些质子在星系团的形成过程中积累。因此，它们是在伽马射线能量下搜索DM湮灭和衰变信号的极好目标，并且由于团簇内介质中的强子相互作用，被预测为大规模伽马射线发射的来源。我们估计了切伦科夫望远镜阵列（CTA）探测英仙座星系团散射伽马射线发射的灵敏度。我们对DM和CRp分量的预期信号进行了详细的空间和频谱建模。对于每种情况，我们计算预期的CTA灵敏度。文中还讨论了珀尔修斯的观测策略。在没有扩散信号（未检测）的情况下，CTA应将半径$R_{500}$内的CRp与热能之比限制为约$X_{500}<3\乘以10^{-3}$，对于遵循热气体的空间CRp分布和CRp光谱指数$\alpha_｛\rm CRp｝=2.3$。在英仙座射电微晕纯强子起源的乐观假设下，根据假设的磁场剖面，CTA应测量$\alpha｛\rmCRp｝$至约$\Delta\alpha_｛\RMCRp｝\simeq 0.1$和CRp空间分布，精度为10%。关于DM，CTA应根据DM晕子结构的建模，将速度平均湮灭截面上集群观测的当前地面伽马射线DM极限提高高达$\sim 5$的因子。在DM粒子衰变的情况下，CTA将探索参数空间的一个新区域，对于1TeV以上的DM质量，达到$\tau_{\chi}>10^{27}$ 的模型。这些约束将对团簇尺度下的CRp加速和传输的物理特性以及TeV DM粒子模型提供前所未有的敏感性，尤其是在衰变场景中。 et.al.|[2309.03712](http://arxiv.org/abs/2309.03712)|null|
|**2023-09-07**|**DiffDefense: Defending against Adversarial Attacks via Diffusion Models**|本文提出了一种新的重建方法，该方法利用扩散模型来保护机器学习分类器免受对抗性攻击，而不需要对分类器本身进行任何修改。机器学习模型对微小输入扰动的敏感性使其容易受到对抗性攻击。虽然基于扩散的方法由于其缓慢的反向过程而通常被忽略用于对抗性防御，但本文证明了我们提出的方法在保持干净的准确性、速度和即插即用兼容性的同时，提供了对抗性威胁的鲁棒性。代码位于：https://github.com/HondamunigePrasannaSilva/DiffDefence. et.al.|[2309.03702](http://arxiv.org/abs/2309.03702)|null|
|**2023-09-07**|**Electric Analog of Magnons in Order-Disorder Ferroelectrics**|我们分析“ferron”微观伪自旋模型对有序无序铁电体的激发。我们证明，与磁振子类似，磁振子是磁性材料中自旋波的量子，它同时携带静态和振荡电偶极矩，表现出斯塔克效应，并可能受到太赫兹辐射的参数激发方向和施加的静电场。我们预测铁离子的扩散长度可以达到厘米，这意味着通过温度梯度有效地传输电极化。这些特性表明，铁电材料可能对数据存储应用之外的信息技术有用。 et.al.|[2309.03691](http://arxiv.org/abs/2309.03691)|null|
|**2023-09-07**|**Diffuse gamma-ray emission around the Rosette Nebula**|玫瑰星云是一个年轻的星团和分子云复合体，位于中年SNR Monoceros环（G205.5+0.5）的南壳边缘。我们使用超过13年的费米LAT数据重新研究了玫瑰星云的GeV伽马射线发射。我们测试了几个空间模型，发现与仅使用CO气体模板的结果相比，包含HII气体模板可以显著提高似然拟合。我们使用新的空间模板进行了光谱分析。利用伽马射线观测和CO+HII气体数据，我们导出了玫瑰星云附近不同成分的宇宙射线光谱。我们发现玫瑰星云的伽马射线发射比之前报道的要困难得多，这可能意味着玫瑰星云是另一个发射伽马射线的年轻大质量星团的例子。 et.al.|[2309.03577](http://arxiv.org/abs/2309.03577)|null|
|**2023-09-07**|**Text2Control3D: Controllable 3D Avatar Generation in Neural Radiance Fields using Geometry-Guided Text-to-Image Diffusion Model**|ControlNet等扩散模型的最新进展使几何可控、高保真的文本到图像生成成为可能。然而，它们都没有解决将这种可控性添加到文本到三维生成中的问题。作为回应，我们提出了Text2Control3D，这是一种可控的文本到3D化身生成方法，在手持相机随意拍摄的单眼视频中，其面部表情是可控的。我们的主要策略是在神经辐射场（NeRF）中构建3D化身，该神经辐射场使用我们从ControlNet生成的一组可控视点感知图像进行优化，ControlNet的条件输入是从输入视频中提取的深度图。在生成视点感知图像时，我们利用交叉注意力通过交叉注意力注入控制良好的、参考性的面部表情和外观。我们还对扩散模型的高斯潜像进行低通滤波，以改善我们从经验分析中观察到的视点不可知的纹理问题，其中视点感知图像在相同的像素位置上包含在3D中无法理解的相同纹理。最后，为了使用视点感知但在几何结构上不严格一致的图像来训练NeRF，我们的方法将每个图像的几何变化视为来自共享3D规范空间的变形视图。因此，我们通过经由变形字段表学习一组每图像变形来在可变形NeRF的规范空间中构造3D化身。我们展示了实证结果，并讨论了我们的方法的有效性。 et.al.|[2309.03550](http://arxiv.org/abs/2309.03550)|null|

<p align=right>(<a href=#updated-on-20230911>back to top</a>)</p>

## NeRF

|Publish Date|Title|Abstract|PDF|Code|
|---|---|---|---|---|
|**2023-09-07**|**SimNP: Learning Self-Similarity Priors Between Neural Points**|用于3D对象重建的现有神经场表示要么（1）利用对象级表示，但由于对全局潜在代码的限制而遭受低质量细节，要么（2）能够完美地重建观测，但未能利用对象级先验知识来推断未观察到的区域。我们提出了一种学习类别级自相似性的方法SimNP，它通过将神经点辐射场与类别级自类似性表示相连接，结合了两个世界的优点。我们的贡献是双重的。（1） 我们利用相干点云的概念设计了第一个类别级别的神经点表示。由此产生的神经点辐射场为局部支持的对象区域存储了高级别的细节。（2） 我们了解了如何以无约束和无监督的方式在神经点之间共享信息，这允许在重建过程中根据给定的观测值导出对象的未观察区域。我们表明，SimNP在重建对称的看不见物体区域方面优于以前的方法，超过了建立在类别级或像素对齐辐射场上的方法，同时提供了实例之间的语义对应 et.al.|[2309.03809](http://arxiv.org/abs/2309.03809)|null|
|**2023-09-06**|**CoNeS: Conditional neural fields with shift modulation for multi-sequence MRI translation**|多序列磁共振成像（MRI）在现代临床研究和深度学习研究中都有广泛的应用。然而，在临床实践中，由于患者的不同图像采集协议或造影剂禁忌症，经常会出现一个或多个MRI序列缺失的情况，这限制了在多序列数据上训练的深度学习模型的使用。一种很有前途的方法是利用生成模型来合成缺失的序列，这可以作为替代获取。解决这一问题的最先进方法是基于卷积神经网络（CNN），该网络通常存在频谱偏差，导致高频精细细节的重建较差。在本文中，我们提出了具有移位调制的条件神经场（CoNeS），这是一种以体素坐标为输入并学习用于多序列MRI平移的目标图像的表示的模型。所提出的模型使用多层感知器（MLP）代替CNN作为像素到像素映射的解码器。因此，每个目标图像被表示为神经场，该神经场通过利用学习的潜码的移位调制而被调节在源图像上。在BraTS 2018和前庭神经鞘瘤患者的内部临床数据集上进行的实验表明，所提出的方法在视觉和定量上都优于最先进的多序列MRI翻译方法。此外，我们进行了光谱分析，表明CoNeS能够克服传统CNN模型中常见的光谱偏差问题。为了进一步评估合成图像在临床下游任务中的使用，我们在推理时使用合成图像测试了分割网络。 et.al.|[2309.03320](http://arxiv.org/abs/2309.03320)|null|
|**2023-09-06**|**ResFields: Residual Neural Fields for Spatiotemporal Signals**|神经场是一类被训练来表示高频信号的神经网络，近年来由于其在复杂三维数据建模方面的出色性能，特别是通过单个多层感知器（MLP）的大神经符号距离（SDFs）或辐射场（NeRFs），而受到了极大的关注。然而，尽管用MLP表示信号的能力和简单性很强，但由于MLP的容量有限，这些方法在建模大而复杂的时间信号时仍然面临挑战。在本文中，我们提出了一种有效的方法来解决这一限制，将时间残差层纳入神经场，称为ResFields，这是一类专门设计用于有效表示复杂时间信号的新型网络。我们对ResFields的性质进行了全面的分析，并提出了一种矩阵分解技术来减少可训练参数的数量并增强泛化能力。重要的是，我们的公式与现有技术无缝集成，并在各种具有挑战性的任务中持续改进结果：2D视频近似、通过时间SDF的动态形状建模和动态NeRF重建。最后，我们通过展示ResFields在从轻量级捕捉系统的稀疏感官输入捕捉动态3D场景方面的有效性，展示了它的实用性。 et.al.|[2309.03160](http://arxiv.org/abs/2309.03160)|**[link](https://github.com/markomih/ResFields)**|
|**2023-09-01**|**GNFactor: Multi-Task Real Robot Learning with Generalizable Neural Feature Fields**|开发能够在非结构化现实世界环境中通过视觉观察执行各种操作任务的代理是机器人技术中的一个长期问题。为了实现这一目标，机器人需要对场景的3D结构和语义有全面的了解。在这项工作中，我们提出了 $\textbf｛GNFactor｝$，一种用于多任务机器人操作的视觉行为克隆代理，具有$\textbf｛G｝$通用$\textbf｛N｝$eural功能$\textbf｛F｝$字段。GNFactor联合优化了作为重建模块的可推广神经场（GNF）和作为决策模块的感知转换器，利用了共享的深度3D体素表示。为了在3D中结合语义，重建模块利用视觉语言基础模型（$\textit｛例如｝$ ，Stable Diffusion）将丰富的语义信息提取到深度3D体素中。我们在3个真实机器人任务中评估了GNFactor，并在10个RLBench任务中进行了详细的消融，演示次数有限。我们观察到GNFactor在可见和不可见任务中比当前最先进的方法有了实质性的改进，证明了GNFactor强大的泛化能力。我们的项目网站是https://yanjieze.com/GNFactor/。 et.al.|[2308.16891](http://arxiv.org/abs/2308.16891)|**[link](https://github.com/YanjieZe/GNFactor)**|
|**2023-08-30**|**Active Neural Mapping**|我们用不断学习的神经场景表示来解决主动映射的问题，即主动神经映射。关键在于通过有效的代理移动积极找到要探索的目标空间，从而最大限度地减少在以前看不见的环境中飞行中的地图不确定性。在本文中，我们检验了连续学习神经场的权重空间，并从经验上表明，神经变异性，即对随机权重扰动的预测鲁棒性，可以直接用于测量神经映射的瞬时不确定性。结合神经映射中继承的连续几何信息，可以引导agent找到一条可遍历的路径，以逐渐获得环境知识。我们首次提出了一种用于在线场景重建的具有基于坐标的隐式神经表示的主动映射系统。在视觉逼真的Gibson和Matterport3D环境中的实验证明了所提出方法的有效性。 et.al.|[2308.16246](http://arxiv.org/abs/2308.16246)|null|
|**2023-08-29**|**Canonical Factors for Hybrid Neural Fields**|因子特征量提供了一种简单的方法来构建更紧凑、高效和可积分的神经场，但也引入了对真实世界数据不一定有益的偏差。在这项工作中，我们（1）描述了这些架构对轴对准信号的不希望有的偏差——它们可能导致高达2 PSNR的辐射场重建差异——以及（2）探索了学习一组规范化变换如何通过消除这些偏差来改进表示。我们在二维模型问题中证明，同时学习这些变换和场景外观是成功的，效率大大提高。我们使用图像、符号距离和辐射场重建任务验证了最终的架构，我们称之为TILTED，在这些任务中，我们观察到了质量、稳健性、紧凑性和运行时间方面的改进。结果表明，TILTED可以实现比基线大2倍的能力，同时突出神经场评估程序的弱点。 et.al.|[2308.15461](http://arxiv.org/abs/2308.15461)|null|
|**2023-08-30**|**NSF: Neural Surface Fields for Human Modeling from Monocular Depth**|从单眼相机获得个性化的3D可动画化化身在游戏、虚拟试穿、动画和VR/XR等领域有几个现实世界的应用。然而，从这种稀疏的数据中建模动态和细粒度的服装变形是非常具有挑战性的。现有的从深度数据建模3D人类的方法在计算效率、网格一致性以及分辨率和拓扑结构的灵活性方面具有局限性。例如，使用隐式函数重建形状和每帧提取显式网格在计算上是昂贵的，并且不能确保跨帧的连贯网格。此外，在具有离散表面的预先设计的人类模板上预测每个顶点的变形在分辨率和拓扑结构上缺乏灵活性。为了克服这些局限性，我们提出了一种新的方法“关键特征：神经表面场”，用于从单目深度对穿着3D衣服的人类进行建模。NSF仅在基面上定义了一个神经场，该神经场对连续和灵活的位移场进行建模。NSF可以适应不同分辨率和拓扑结构的基面，而无需在推理时进行重新训练。与现有方法相比，我们的方法在保持网格一致性的同时消除了昂贵的每帧表面提取，并且能够在不重新训练的情况下重建任意分辨率的网格。为了促进这方面的研究，我们在项目页面上发布了我们的代码：https://yuxuan-xue.com/nsf. et.al.|[2308.14847](http://arxiv.org/abs/2308.14847)|null|
|**2023-08-28**|**A Transformer-Conditioned Neural Fields Pipeline with Polar Coordinate Representation for Astronomical Radio Interferometric Data Reconstruction**|在射电天文学中，能见度数据是对射电望远镜波信号的测量，被转换成图像，用于观测遥远的天体。然而，由于信号稀疏性和其他因素，这些结果图像通常包含真实源和伪影。获得更干净图像的一种方法是在成像之前将样本重建成致密的形式。不幸的是，现有的可见性重建方法可能会错过频率数据的一些分量，因此模糊的对象边缘和持久的伪影仍然存在于图像中。此外，由于数据偏斜，在不规则可见性样本上的计算开销很高。为了解决这些问题，我们提出了PolarRec，这是一种干涉能见度数据的重建方法，它由具有极坐标表示的变压器条件神经场管道组成。这种表示与望远镜在地球自转时观察天体区域的方式相匹配。我们进一步提出了径向频率损失函数，使用极坐标系中的径向坐标与频率信息进行关联，以帮助重建完整的可见性。我们还根据极坐标系中的角坐标对可见性采样点进行分组，并使用分组作为随后使用Transformer编码器进行编码的粒度。因此，我们的方法可以有效地捕捉可见性数据的固有特征。我们的实验表明，PolarRec通过忠实地重建可见性域中的所有频率分量，显著提高了成像结果，同时显著降低了计算成本。 et.al.|[2308.14610](http://arxiv.org/abs/2308.14610)|null|
|**2023-08-24**|**NeO 360: Neural Fields for Sparse View Synthesis of Outdoor Scenes**|最近的隐式神经表示在新的视图合成中显示出了很好的结果。然而，现有的方法需要从许多视图进行昂贵的每场景优化，因此限制了它们在真实世界的无边界城市环境中的应用，在这些环境中，从极少数视图观察到感兴趣的对象或背景。为了缓解这一挑战，我们引入了一种名为NeO360的新方法，用于户外场景稀疏视图合成的神经场。NeO 360是一种可推广的方法，它从单个或几个摆出姿势的RGB图像重建360｛\deg｝场景。我们方法的本质是捕捉复杂的真实世界户外3D场景的分布，并使用可以从任何世界点查询的混合图像条件三平面表示。我们的表示结合了基于体素和鸟瞰图（BEV）的最佳表示，比每种表示都更有效、更具表现力。NeO 360的表示使我们能够从大量无界3D场景中学习，同时在推理过程中从一张图像中提供对新视图和新场景的可推广性。我们在所提出的具有挑战性的360｛\deg｝无界数据集NeRDS 360上演示了我们的方法，并表明NeO 360在新视图合成方面优于最先进的可推广方法，同时还提供编辑和合成功能。项目页面：https://zubair-irshad.github.io/projects/neo360.html et.al.|[2308.12967](http://arxiv.org/abs/2308.12967)|**[link](https://github.com/zubair-irshad/NeO-360)**|
|**2023-08-23**|**Semantic-Aware Implicit Template Learning via Part Deformation Consistency**|学习隐式模板作为神经场最近在无监督形状对应方面表现出了令人印象深刻的性能。尽管取得了成功，但我们观察到，目前仅依赖几何信息的方法往往会在具有高结构可变性的通用物体形状中学习次优变形。在本文中，我们强调了零件变形一致性的重要性，并提出了一个语义感知的隐式模板学习框架，以实现语义上合理的变形。通过利用自监督特征提取器的语义先验，我们建议使用新的语义感知变形代码进行局部条件调节，并对零件变形、全局变形和全局缩放进行变形一致性正则化。我们的大量实验证明了所提出的方法在各种任务中优于基线：关键点转移、零件标签转移和纹理转移。更有趣的是，我们的框架在更具挑战性的环境下显示出更大的性能提升。我们还提供了定性分析来验证语义感知变形的有效性。代码可在https://github.com/mlvlab/PDC. et.al.|[2308.11916](http://arxiv.org/abs/2308.11916)|null|

<p align=right>(<a href=#updated-on-20230911>back to top</a>)</p>

[contributors-shield]: https://img.shields.io/github/contributors/Vincentqyw/cv-arxiv-daily.svg?style=for-the-badge
[contributors-url]: https://github.com/Vincentqyw/cv-arxiv-daily/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/Vincentqyw/cv-arxiv-daily.svg?style=for-the-badge
[forks-url]: https://github.com/Vincentqyw/cv-arxiv-daily/network/members
[stars-shield]: https://img.shields.io/github/stars/Vincentqyw/cv-arxiv-daily.svg?style=for-the-badge
[stars-url]: https://github.com/Vincentqyw/cv-arxiv-daily/stargazers
[issues-shield]: https://img.shields.io/github/issues/Vincentqyw/cv-arxiv-daily.svg?style=for-the-badge
[issues-url]: https://github.com/Vincentqyw/cv-arxiv-daily/issues

