---
title: Slime Chunk Counter
date: 2024-05-30
summary: 计算Minecraft指定区域中的史莱姆区块数量
---

计算 Minecraft 指定区域中的史莱姆区块数量(找出足够多区块的史莱姆农场)

# 用法

1. 克隆存储库

```shell
git clone https://github.com/dunxuan/SlimeChunkCounter.git
cd SlimeChunkCounter
```

2. 创建 Conda 环境

```shell
conda create --prefix .conda python=3.11
conda activate "/path/to/.conda"
```

3. 安装依赖包

```shell
conda install cudatoolkit=11.8 cudnn pytorch torchvision torchaudio pytorch-cuda=11.8  -c pytorch -c nvidia
pip install 'git+https://github.com/MostAwesomeDude/java-random.git'
```

4. 运行

```shell
.conda/python run.py
```
