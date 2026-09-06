---
title: "Medical Image Generation with Diffusion Models"
permalink: /research/medical-image-generation/
order: 2
period: "Feb 2025 – May 2025"
context: "DTU Compute"
excerpt: "Stable Diffusion 2.1 fine-tuning with LoRA to generate dermatological lesions and study transitions between melanoma and nevus images."
---

<p class="project-meta">{{ page.period }} · {{ page.context }} · Kongens Lyngby, Denmark</p>

## Background

This project explored synthetic dermatological image generation and transitions between benign and malignant lesion classes.

## My work and methods

I fine-tuned Stable Diffusion 2.1 with low-rank adaptation (LoRA) on melanoma and nevus images from ISIC 2019. I used text-embedding interpolation to study transitions between the two classes and a ResNet18 classifier to evaluate class consistency.

## Outcome

The project produced synthetic dermatological lesions and an evaluation of class consistency using the classifier, alongside exploration of class transitions through text-embedding interpolation.

[All research and projects]({{ '/research/' | relative_url }})
