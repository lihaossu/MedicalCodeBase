# MedicalCodeBase
## 初衷
···
主要是 研究开发的模型代码，项目不同代码不同。复现各个领域的论文往往也是在原始论文基础上受原始代码影响，结构限制。 不利于 抽象编程和滚雪球，也不利于研究成果转化和可视化。不能抽象，提取，进化的代码只能成为越积越多的垃圾堆。
化繁为简， 化具体为抽象，提高代码能力，以及开发代码的适应性
consistly diving into mywork, working for myself

* 第一 以前各个项目中训练，推理模型的代码 规范化提取(抽象)到 codebase, 然后codebase（具体化 instance）项目代码。
* 项目进行的范式：
    * 范式配置：
        * tensorboradX or wandb
        * pytorch dp, ddp or others
        * config 管理 --》  Hydra
        * experiment 管理
            * 每次运行到的必要脚本备份
            * 运行环境信息保存
            * 训练过程记录
            * 训练时间和硬件效率分析及优化
* 这里不是 pilot 开发 或者 demo, 或者 first-reproduce 的地方。而是在快速复现，pilot 开发，或者各个项目里开发完成后 对这些开发完成的代码 进行整理，泛化处理的地方。
Todo list
* hydra config-style model pipeline building
···
## 关于推理
    * 验证集和测试集推理
    * end2end 推理
## 关于医疗影像数据
## 关于数据集处理
* 数据集EDA & EDA 可视化
* 训练数据 分段式处理 还是 一段式 ？
    * 比如 nnUNet 就是分段式
    * 有的项目就是一段式，所有的数据增强，处理都包含在训练过程中 比如 Lung ImPulSe
* vessel_data&mask_process
    * centerline and node process
    * stl visualization
    * 
* training & valid & test
## 关于结果分析
* 定量分析 & 可视化
* 定性分析 & 可视化
## 关于模型训练
* 训练配置及监督
    * train & valid split （specified list）  
    * wandb & tensorboardX
    * optimal
    * loss function
    * iteration, epoch,
* nnunet 训练模式
    * LN_seg_2D --> classification header 
    * MedNeXt
        * slab_wise training(z_axis)
    * Swintransformer
    * STUnet
        * slab_wise training(z_axis) 
* stomach_artery 训练模式
    * densenet
    * train radom crop & valid whole roi resample
* vesselFM 训练模式
* ImPulSe 训练模式
* lung respiratory motion simulation

## 关于docker
## 关于package或者requirement,或者发布
## 关于项目
## 代码提升
* 资源使用率分析（时间优化）
* 代码结构优化分析
* 面向抽象编程
* 测试代码片段
* 文档补全和注释
## debug log