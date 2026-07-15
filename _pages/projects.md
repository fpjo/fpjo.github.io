---
title: "研究与项目"
permalink: /projects/
author_profile: true
lang: zh
translation_url: /en/projects/
translation_label: English
excerpt: "多模态检索, 扩散模型实验, RoboMaster 机器人视觉, VLM 与 Jetson 部署项目."
---

这里记录我参与的科研训练与工程项目. 对团队研究工作, 页面仅描述本人已确认的实验实现, 评估和分析职责.

## 科研训练

<div class="resume-entry">
  <h3>多轮多模态时尚图像检索实验研究</h3>
  <p class="resume-entry__meta">Composed Image Retrieval / Multimodal Retrieval | 2026.03 - 至今</p>
  <ul>
    <li>围绕真实购物场景下的多轮交互式图像检索, 参与多模态检索模型的实验验证与性能分析, 覆盖 text-to-image, composed image retrieval, in-shop retrieval 和 sketch-to-image 等任务形式.</li>
    <li>参与 FashionAM 三阶段框架的训练与评估流程, 涉及背景去除图像对齐, 服饰语义 caption 对齐, MLLM + LoRA 多轮查询建模与多正样本对比学习目标.</li>
    <li>基于 DIM-Fashion 与 MT FashionIQ 等设置分析 R@K 和 mAP 在多任务, 多轮上下文与意图切换场景中的变化.</li>
    <li>通过实验复现与 ablation study 分析训练阶段, alignment objective 和 MLLM backbone 对检索性能的影响.</li>
  </ul>
</div>

<div class="resume-entry">
  <h3>扩散模型推理加速与伪影分析实验研究</h3>
  <p class="resume-entry__meta">Diffusion Model Acceleration | 2025.09 - 2026.01</p>
  <ul>
    <li>参与基于 RALU 的扩散模型推理加速实验, 聚焦分阶段 latent upsampling 在高频细节区域引入网格状伪影的问题.</li>
    <li>负责 FLUX.1-dev 相关实验实现与评估分析, 在 Stage 3 引入 VAE 重投影对比流程, 包括 VAE decode, 像素级上采样, VAE encode, patch 坐标映射与 re-noising 设置.</li>
    <li>在 cc12m 与 COCO2017 等设置下比较 FID, CLIP, GenEval, CLIP-IQA 与推理耗时, 分析图像质量改善和效率损失的权衡.</li>
    <li>实验观察到 VAE 重投影可缓解高频网格伪影, 但会带来额外编解码开销和清晰度下降, 因而不适合作为直接保留原加速优势的最终方案.</li>
  </ul>
</div>

## 机器人视觉与工程项目

<div class="resume-entry">
  <h3>RoboMaster 机器人比赛 / ARTINX 实验室</h3>
  <p class="resume-entry__meta">视觉组组长, 顾问 | 2023.09 - 2025.08</p>
  <ul>
    <li>负责比赛机器人视觉系统的模型训练, 推理部署与实车调试, 覆盖英雄, 步兵和哨兵机器人平台.</li>
    <li>使用 PyTorch 微调 YOLO 系列目标检测模型, 并基于 TensorRT 部署至 Jetson Orin NX 完成装甲板检测与定位. 通过数据增强和模型替换, 在低于 20 Lux 的昏暗环境中将整体精度提升约 15%, 常态推理耗时控制在 10 ms 内.</li>
    <li>设计前哨站周期观测估计与定时击打算法, 支持稳定击打动态目标, 前哨站平均击打效率约 90%.</li>
    <li>基于扩展卡尔曼滤波观测目标运动状态, 结合操控因素优化枪口方向选择. 参与 C++ Actor Framework 视觉算法可视化模块优化与 ArtinxHub 视觉框架维护.</li>
  </ul>
</div>

<div class="resume-entry">
  <h3>VLM 图像字幕生成与组件分析</h3>
  <p class="resume-entry__meta">计算机视觉课程项目 | 得分: 110/110 | <a href="https://github.com/fpjo/LLaVA">GitHub</a></p>
  <ul>
    <li>基于 PyTorch 与 Transformers 端到端实现 LLaVA 架构视觉语言模型, 集成 ViT/ResNet 视觉编码器与 GPT-2/Qwen 语言模型, 完成图像字幕生成训练与评估流程.</li>
    <li>搭建 COCO 数据集上的训练, 推理和评估流程, 使用 BLEU, CIDEr 等指标进行量化分析.</li>
    <li>完成视觉编码器, 连接器与语言模型组件的消融实验, 观察到 Attention 连接器相较 MLP 使 CIDEr 提升超过 230%, 并对关键组件进行性能归因.</li>
  </ul>
</div>

<div class="resume-entry">
  <h3>基于 Jetson Nano 的人脸识别与表情交互系统</h3>
  <p class="resume-entry__meta">深度学习课程项目 | 得分: 98/100</p>
  <ul>
    <li>在 Jetson Nano 4GB 开发板上实现实时人脸检测, 人脸识别与表情交互系统, 端到端运行速度约 30 fps.</li>
    <li>基于 RetinaFace-500MF (MobileNet Backbone) 完成人脸检测, 基于 MobileFaceNet@WebFace600K 完成人脸识别, 并基于 FER2013 微调 MobileNetV3 实现表情识别.</li>
    <li>使用 TensorRT 与 Jetson 生态组件进行边缘端推理优化, 在算力和内存受限环境下完成模型选型, 部署和性能调试.</li>
  </ul>
</div>
