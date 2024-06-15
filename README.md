实验结果介绍：
本实验使用的是CIFAR-10数据集，这是一个常用的图像样本数据集。
本实验采用的是EDM框架（这一设计框架统一了diffusion-based model），将Heun2阶求解方法、unipc框架、dpm-solver++和dpm-solver-V3这三种采样方法进行了对比。
用这四种方法分别对图像进行采样，并且对比了在不同NFE(numbers of function evaluations)之下的四种方法的图像采样结果，采用FID衡量了这些结果的好坏。

实验复现过程：
创建虚拟环境后安装了所需的库，在sample.bash脚本中需要加入
source C:/Users/sjc/anaconda3/etc/profile.d/conda.sh 
conda activate env-DPM1 set 
-ex
三条语句，以在脚本中启用对应的环境。
在gitbash里输入指令bash sample.sh即可进行图像处理。
实验过程进行了1天左右，生成的结果存储在samples文件夹中的emd-cifar10-32x32-uncond-vp中。
接下来通过compute_fid.py计算生成结果的fid，结果存储在output.txt中。
