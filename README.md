# Photovoltaic pose estimation dataset
A 3D dataset for PV station parts like transformers and gears features 10 categories and 14,000 images, suitable for pose estimation. Captured with a RealSense D435i, the dataset is processed on a powerful system and includes Aruco QR codes for 3D reconstruction. It's optimized for robustness with color and noise enhancements.

运行环境Operating environment
1. 环境配置
安装Miniconda（Linux系统）：
访问Miniconda的官方网站找到最新的安装脚本链接，：https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh。
使用wget命令下载安装脚本，并执行安装脚本。
安装过程中，阅读并同意许可协议，选择安装位置（默认安装在用户home目录下）。
安装完成后，激活Miniconda环境。
创建并激活虚拟环境：
根据ObjectDatasetTools的要求，建议使用Python 3.6版本（Python 2.7版本可能存在较多bug）。
使用conda create命令创建一个名为odt的虚拟环境，并指定Python版本为3.6。
激活该虚拟环境。
安装依赖：
使用sudo apt-get命令更新和升级系统软件包。
安装必要的依赖，如build-essential、cmake、git、pkg-config、libssl-dev、libgl1-mesa-glx等。
安装meshlab，一个用于处理3D网格的开源系统。
使用pip命令安装Python依赖包，如numpy、pypng、scipy、scikit-learn、open3d（推荐版本为0.9.0.0）、scikit-image、tqdm、pykdtree、opencv-python（推荐版本为4.6.0.66）、opencv-contrib-python（推荐版本为4.6.0.66）等。
2. 数据集处理
加载数据集：
使用ObjectDatasetTools的API加载数据集，例如：dataset = ObjectDataset('path/to/dataset')。
数据预处理：
使用ObjectDatasetTools提供的方法对数据进行预处理，如随机裁剪、水平翻转、缩放等。
数据可视化：
使用ObjectDatasetTools的可视化功能查看图像与标注框。
数据集评估：
使用ObjectDatasetTools提供的方法计算平均精度（mAP）等指标，评估模型性能。
