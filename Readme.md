<style type="text/css">
.pic{width:90px;height:126px;float:right;margin-right:10px;border:1px solid #ccc}
.cent{float:left;}
</style>

<div class="cent">
  <p>
    <font size=5><strong>刘黄河</strong></font>
  </p>
  <br>电话：173-6539-1767&emsp;<br>邮箱：liuhuanghe@hotmail.com&emsp;<br>微信：Huanghe_946
</div>
<div class="pic"><img src="./17_pic.jpg"  alt=""/></div>

![](./split.png)

#### 教育和工作经历

* 中国科学技术大学&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;2018.09 ~ 至今&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; 软件工程专业-硕士研究生
* 四川大学&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;2013.09 ~ 2017.6&emsp;&emsp;&emsp;&emsp;&emsp;计算机科学与技术专业-本科  
* 深圳云天励飞技术有限公司&emsp;&emsp;&emsp;2017.07 ~ 2017.10 &emsp;&emsp;&emsp;&emsp; C++后端开发工程师




sdad <span style="float:right" face="italic"> September 2018 - present </span>

sdad <front style="float:right" face="italic"> <i>September 2018 - present <i> </front>

![](./split.png)

#### 专业技能

* 熟悉 C++ / Python
* 掌握常见数据结构和基本算法，掌握操作系统、计算机网络等基础知识
* 熟悉 Linux 操作系统和常用命令，熟悉 Git 等工具的使用
* 有 docker 和 Kubernetes 学习和使用经验

![](./split.png)

#### 项目经历

* **寒武纪计算卡深度学习算法移植 &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; 2018.09 - 2019.08**
    **项目概述**：移植 cnn 模型到寒武纪计算卡，并编写相应的示例 demo（目标识别，分类，人脸识别，车辆检测等）。  
    **本人主要工作**： 
      1. 转换预训练 caffe 模型（resnet、vgg、ssd等）到寒武纪私有模型格式；
      2. 编写 c++ 程序对视频文件或图片列表进行识别并将识别目标输出文本和目标框绘制文件，图像处理部分使用 opencv, 采用3个线程分别处理图片读入与预处理、模型推理、结果写回，使用队列进行数据缓冲，并进行板卡内存与主存的数据拷贝。

<br>

* **基于 Nvidia TX2 的目标识别 &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; &emsp; 2018.11 - 2019.06**
    **项目概述**：基于 Nvidia TX2 开发目标识别应用，模型采用 yolov3，减枝并且移植到 TensorRT，目标提高 TX2 车辆识别目标检测速度。 
    **本人主要工作**： 
      1. 使用 pytorch 进行 yolov3 训练并进行减枝，将 yolov3 模型大小缩小到 100MB 以内；
      2. 将模型转换成 caffe 模型格式再转换成 TensorRT 格式；
      3. 对于 yolo 检测层单独编写代码处理，主要包括 anchor 与 nms 实现；
      4. 编写 c++ 程序对视频文件或摄像头输入逐帧识别处理并实时显示识别结果, 图像处理部分使用 opencv。

<br>

* **搭建实验室深度学习服务 &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; 2019.03 - 2019.08**
    **项目概述**：基于 lxd 容器技术实现多卡 GPU 服务器的 GPU 分配和环境隔离，编写 web 服务，实现 web 容器管理，提供多用户深度学习环境。 
    **本人主要工作**：
      1. 部署 lxd 和 cuda 环境，完成基础环境搭建后生成 template 容器镜像；
      2. 编写 python 脚本调用 lxc 命令接口，查询和设置 gpu 绑定与端口绑定，实现更加便捷的容器管理；
      3. 使用 python flask 编写 web 服务，后台调用脚本，实现通过 web 界面查看和管控容器，方便用户申请容器实例，绑定端口，和绑定 gpu。

<br>

* **参与搭建以国产智能计算板卡为核心的分布式平台 &emsp;&emsp;&emsp;&emsp;2019.07 - 至今**
    **项目概述**：40台服务器共160张计算加速卡，通过 Kubernetes 进行集群管理，底层使用 Ceph 作为存储层。
    **本人主要工作**： 
      1. 参考 intel DevicePlugin，开发寒武纪板卡 DevicePlugin，实现 k8s 集群对寒武纪板卡的资源管理；
      2. 使用 envoy + registry-proxy，实现 gcr、quay 仓库的代理服务，避免镜像拉取失败；
      3. 使用 pytorch 对 yolov3/ssd/vgg 等模型进行重训练，并转换模型到寒武纪格式，开发和部署应用 demo，提供 restful api 服务。
      4. Kubernetes 集群部署与维护。
      
![](./split.png)

#### 获奖经历

1. **海量光学摇感数据算法大赛 一等奖 &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; 2019年**
  **比赛简介**：基于寒武纪寒武纪 MLU100 对卫星遥感图像进行目标识别，强调处理速度和限制模型大小，主要目的是及进行CNN网络算法移植和裁剪，主要考验对于 MLU100 的算力利用和模型移植能力；
  **参赛方案**：使用 yolov3 模型，进行模型减枝，最终模型大小为54MB，由于 MLU100 不支持 yolo 检测层，将 yolo 和输出层丢弃，并手动实现 yolo 检测代码和相关过程，考虑到 MLU100 8个处理器一组，4组一共32个核心，将数据分成4份，启动4个线程，每个线程使用8个mlu核心进行并行数据推理；整个方案通过 c++ 实现。

<br>

2. **全国大学生机器人大赛 ROBOMASTERS 南部赛区 三等奖 &emsp;&emsp;&emsp;2016年**
  **比赛简介**：大疆主办的轮式机器人射击比赛，2016年第二届 robomaster 每组队伍包含1个英雄机器人、3个步兵机器人、1个基地机器人、1个空中机器人，一共6个机器人进行设计对抗，红蓝双方装备有红蓝灯装甲板方便队伍机器自动瞄准。
  **参赛方案**：步兵机器人采用官方提供的机器人，队伍设计和实现英雄机器人、基地机器人、空中机器人；参与英雄机器人和基地机器人的上层控制与自动瞄准实现；使用 ros 进行系统通信与控制，采用 kinect 深度相机，使用 opencv 库，采用 滑窗+SVM 识别敌方装甲板并进行跟踪，根据敌方运动进行提前量预估，进行自动射击。

<br>

3. **全国机器人锦标赛仿真 11VS11 机器人足球项目 一等奖 &emsp;&emsp;&emsp;&emsp; 2015年**
  **比赛简介**：在赛方提供的仿真平台上进行 11vs11 的机器人足球对抗
  **参赛方案**：使用平台提供相关接口，实现对11个机器人的动作决策，实现机器人的路径规划与避障，机器人传球，机器人射门，机器人点球的不同策略。

<br>

4. **国家励志奖学金 &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;2015年**

5. **四川大学优秀学生 &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;2015年**

6. **四川大学二等/三等奖学金等  &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&ensp;2014~2017年**