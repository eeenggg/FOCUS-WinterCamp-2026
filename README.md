# \# 👁️ FOCUS Winter Camp 2026 - 视觉与云端 AI 赛道

# 

# > \*\*eeenggg

# > \*\*生医2503

# 

# \## 📖 项目简介

# 本项目是 2026 FOCUS 冬令营视觉赛道的结项仓库。我基于 \*\*YOLOv11\*\* 实现了从环境搭建、自定义数据集采集、模型训练到端侧推理的全流程闭环。

# 

# \*\*核心成果：\*\*

# 1\.  \*\*二次元角色识别 (MyGO!!!!!)\*\*：解决了画风差异与相似角色混淆问题，训练出高精度识别模型。

# 2\.  \*\*日常生活物品检测\*\*：自制数据集（手表、鼠标、杯子、纸巾），成功训练并部署。

# 3\.  \*\*智能计数系统\*\*：开发了能够实时统计画面人数/物体数量的 Python 脚本。

# 

# ---

# 

# \## 📂 目录结构说明

# 

# ```text

# FOCUS-WinterCamp-2026/

# ├── docs/                   # 项目文档与资源

# │   └── assets/             # \[核心] 存放项目展示图片与验收截图

# ├── runs/                   # 训练结果 (模型权重与日志)

# │   └── detect/

# │       ├── train9/         # \[MyGO模型] 最佳权重 (best.pt)

# │       └── train\_common2/  # \[物品模型] 最佳权重 (best.pt)

# ├── src/                    # 源代码

# │   ├── scripts/            # 核心脚本

# │   │   ├── predict\_mygo.py    # MyGO 预测脚本

# │   │   ├── count\_image.py     # 图片计数脚本

# │   │   ├── count\_video.py     # 视频计数脚本

# │   │   └── train\_common.py    # 物品训练脚本

# │   ├── config/             # YOLO 模型配置文件

# │   └── datasets/           # 数据集

# └── README.md               # 项目主页



---



\## 🏆 任务验收成果展示



\### ✅ 验收点 1：环境搭建与基础任务

成功配置 Anaconda + PyTorch 环境，完成 CNN 手写数字识别与官方数据集跑通测试。



\*\*1. GitHub Pages 个人主页生成：\*\*

!\[GitHub Page](docs/assets/page界面.png)



\*\*2. 官方数据集训练与检测结果：\*\*

!\[Official Training](docs/assets/官方数据集YOLOv11训练过程和生成的目标检测结果.png)



\*\*3. CNN 手写数字识别 Loss 曲线：\*\*

!\[CNN Loss](docs/assets/CNN于手写数字识别损失函数下降曲线.png)



---



\### ✅ 验收点 2：MyGO 角色识别 (自定义训练)

\* \*\*模型路径：\*\* `runs/detect/train9/weights/best.pt`

\* \*\*任务难点：\*\* 克服了 2D/3D 画风差异，实现了对素世、爱音等角色的精准区分。



\*\*识别效果展示：\*\*

!\[MyGO Prediction](docs/assets/预测3.jpg)

\*(更多预测结果请见 docs/assets 文件夹下的 预测1.jpg - 预测4.jpg)\*



---



\### ✅ 验收点 3：日常生活物品检测与计数

\* \*\*模型路径：\*\* `runs/detect/train\_common2/weights/best.pt`

\* \*\*功能：\*\* 编写了自定义脚本，能够自动统计画面中的人数或特定物品数量。



\*\*人数统计脚本运行结果：\*\*

> 脚本自动在画面左上角标记出统计数量 "Count: X"。



!\[People Counting](docs/assets/识别图像中的人.png)



---



\## 快速开始



\### 1. 环境依赖

首先，请确保安装了必要的依赖库：

```bash

pip install ultralytics opencv-python

```



\### 2. 运行 MyGO 识别

执行以下命令进行识别任务：

```bash

python src/scripts/predict\_mygo.py

```



\### 3. 运行计算图像人数

对图像文件进行计数演示：

```bash

python src/scripts/count\_image.py

```



\### 4. 运行计算视频人数

对视频进行计数演示：

```bash

python src/scripts/count\_video.py

```



