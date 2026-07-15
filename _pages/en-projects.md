---
title: "Research & Projects"
permalink: /en/projects/
author_profile: true
lang: en
translation_url: /projects/
translation_label: 中文
excerpt: "Multimodal retrieval, diffusion-model experiments, RoboMaster robotics vision, vision-language models, and Jetson deployment."
---

This page records my research training and engineering projects. For team research, it describes only my confirmed responsibilities in experimental implementation, evaluation, and analysis.

## Research training

<div class="resume-entry">
  <h3>Experimental Study on Multi-turn Multimodal Fashion Image Retrieval</h3>
  <p class="resume-entry__meta">Composed Image Retrieval / Multimodal Retrieval | Mar. 2026 - Present</p>
  <ul>
    <li>Contributing to experimental validation and performance analysis for multi-turn interactive image retrieval in realistic shopping scenarios, covering text-to-image, composed image retrieval, in-shop retrieval, and sketch-to-image tasks.</li>
    <li>Participating in the FashionAM three-stage training and evaluation pipeline, including background-removed image alignment, fashion-caption alignment, MLLM + LoRA multi-turn query modeling, and multi-positive contrastive learning.</li>
    <li>Analyzing R@K and mAP on DIM-Fashion and MT FashionIQ settings, with attention to multi-task, multi-turn-context, and intent-switching behavior.</li>
    <li>Reproducing experiments and ablation studies to analyze the effects of training stages, alignment objectives, and MLLM backbones on retrieval performance.</li>
  </ul>
</div>

<div class="resume-entry">
  <h3>Experimental Study on Diffusion Model Acceleration and Artifact Analysis</h3>
  <p class="resume-entry__meta">Diffusion Model Acceleration | Sep. 2025 - Jan. 2026</p>
  <ul>
    <li>Participated in a RALU-based diffusion-model acceleration study on grid-like artifacts caused by staged latent upsampling in high-frequency image regions.</li>
    <li>Implemented and evaluated FLUX.1-dev experiments with a Stage-3 VAE re-projection comparison pipeline, including VAE decoding, pixel-space upsampling, VAE encoding, patch-coordinate mapping, and re-noising settings.</li>
    <li>Compared FID, CLIP, GenEval, CLIP-IQA, and inference latency on settings including cc12m and COCO2017 to examine quality-efficiency trade-offs.</li>
    <li>Observed that VAE re-projection can reduce high-frequency grid artifacts, but introduces extra encoding-decoding cost and reduced sharpness, so it does not directly preserve the original acceleration advantage.</li>
  </ul>
</div>

## Robotics vision and engineering projects

<div class="resume-entry">
  <h3>RoboMaster Robotics Competition / ARTINX Lab</h3>
  <p class="resume-entry__meta">Vision Group Lead, Advisor | Sep. 2023 - Aug. 2025</p>
  <ul>
    <li>Led model training, inference deployment, and on-robot debugging for the robot vision system across hero, infantry, and sentry platforms.</li>
    <li>Fine-tuned YOLO-series object detectors with PyTorch and deployed them to Jetson Orin NX via TensorRT for armor-plate detection and localization. Data augmentation and model replacement improved overall accuracy by about 15% below 20 Lux while maintaining typical latency within 10 ms.</li>
    <li>Designed a periodic observation and timed-shooting algorithm for the outpost target, supporting stable hits on dynamic targets with average hit efficiency of about 90%.</li>
    <li>Used Extended Kalman Filter-based target-motion observation and control-aware aiming-direction selection. Also contributed to a C++ Actor Framework visualization module and ArtinxHub maintenance.</li>
  </ul>
</div>

<div class="resume-entry">
  <h3>VLM Image Captioning and Component Analysis</h3>
  <p class="resume-entry__meta">Computer Vision course project | Score: 110/110 | <a href="https://github.com/fpjo/LLaVA">GitHub</a></p>
  <ul>
    <li>Implemented an end-to-end LLaVA-style vision-language model with PyTorch and Transformers, integrating ViT/ResNet visual encoders with GPT-2/Qwen language models for image-captioning training and evaluation.</li>
    <li>Built the training, inference, and evaluation pipeline on COCO, using BLEU and CIDEr for quantitative analysis.</li>
    <li>Conducted ablations on the visual encoder, connector, and language model components. An attention connector improved CIDEr by more than 230% over an MLP connector in the experiment.</li>
  </ul>
</div>

<div class="resume-entry">
  <h3>Face Recognition and Expression Interaction System on Jetson Nano</h3>
  <p class="resume-entry__meta">Deep Learning course project | Score: 98/100</p>
  <ul>
    <li>Built a real-time face-detection, face-recognition, and expression-interaction system on a Jetson Nano 4GB board, achieving approximately 30 fps end-to-end.</li>
    <li>Used RetinaFace-500MF with a MobileNet backbone for detection, MobileFaceNet@WebFace600K for recognition, and MobileNetV3 fine-tuned on FER2013 for expression recognition.</li>
    <li>Applied TensorRT and Jetson ecosystem tools for edge inference optimization under limited compute and memory resources.</li>
  </ul>
</div>
