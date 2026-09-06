---
title: "CV"
permalink: /cv/
redirect_from:
  - /resume
---

<a class="btn btn--primary" href="{{ '/files/yuansheng-zhou-cv.tex' | relative_url }}" download>Download CV (LaTeX source)</a>

The CV is available as LaTeX source. A PDF version is not yet available.

## Profile

MSc graduate in Autonomous Systems from DTU, with project experience in machine learning, signal processing, intelligent sensing, and robotics and automation. My work spans acoustic and biomedical signal analysis, generative models, and robot and vision integration.

## Education

{% include education.md %}

At DTU, my study areas included artificial intelligence, embedded systems, data analysis, optimization, information technology, and systems engineering. At EPFL, my coursework covered medical image processing and data analysis. My undergraduate average was **88/100**, ranking in the **top three of the cohort**.

## Research experience

**[Music-Driven Binaural Ear-Acoustic Authentication]({{ '/research/acoustic-authentication/' | relative_url }})**<br>
Master's thesis, Technical University of Denmark · Oct 2025 – Mar 2026

Built an acoustic-authentication pipeline using OpenEarable 2.0 recordings from 50 participants, including preprocessing, MFCC extraction, identity recognition, binaural fusion comparisons, and replay-attack evaluation.

**[EEG Analysis of Neural Responses to Taste Stimuli]({{ '/research/taste-eeg/' | relative_url }})**<br>
Bachelor's research, Biomedical Engineering Laboratory · Oct 2022 – Jun 2023

Processed scalp EEG responses to five basic tastes and a tasteless control, with feature selection and spectral and temporal comparisons across brain regions. Contributed to conceptualization and formal analysis of the published study.

## Selected technical projects

- **[Medical Image Generation with Diffusion Models]({{ '/research/medical-image-generation/' | relative_url }})** · DTU Compute · Feb 2025 – May 2025. Fine-tuned Stable Diffusion 2.1 with LoRA on ISIC 2019 melanoma and nevus images; studied text-embedding interpolation and evaluated class consistency with ResNet18.
- **[GMP-Oriented Pharmaceutical Automation]({{ '/research/pharmaceutical-automation/' | relative_url }})** · NNE and DTU · Jan 2025. Integrated a UR3e robot and two SICK 3D cameras for cartridge inspection and sorting; implemented control, safety configuration, HMI functionality, testing, and documentation in Siemens TIA Portal.
- **[Action Classification and Joint-Angle Estimation from EMG]({{ '/research/emg-movement-estimation/' | relative_url }})** · Machine learning project · Nov 2024 – Dec 2024. Processed NinaPro signals and developed classification and regression models for movement-intention estimation.

## Publication

{% for publication in site.publications %}
{% include publication-citation.html publication=publication %}
{% endfor %}

**Contribution:** conceptualization and formal analysis.

## Technical skills

- **Programming and modelling:** Python; C/C++; machine-learning classification and regression; diffusion-model fine-tuning with LoRA; data analysis and experimental evaluation.
- **Signal processing:** audio preprocessing; MFCC and time-frequency features; binaural feature fusion; EEG and EMG processing; spectral analysis and feature selection.
- **Sensors, robotics and automation:** OpenEarable 2.0; UR3e; SICK 3D cameras; FANUC; PLC/HMI development; Siemens TIA Portal; GX Works2; servo-motor control.

## Honors

- President's Special Award · 2023
- Scholarship for Outstanding Students · 2020, 2022
- Second Prize, Metallographic Skills Competition of ZJNU · 2021

## Languages

- **Mandarin:** native
- **English:** BEng and MSc completed in English
- **Danish:** Danskuddannelse 3, Module 2
