---
title: Aerial Image Segmentation with U-Net for Autonomous UAV Vision
summary: "Benchmarking U-Net and DeepLabV3+ across five encoder backbones to semantically segment low-altitude drone imagery into 12 classes"

authors:
- "Adeleke Olorunnisola Oyeyemi"

tags:
- Deep Learning
- Computer vision
- Robotics

date: "2023-02-13T00:00:00Z"

# Internal link to another page within the Hugo site
internal_link: "project/Aerial_Image_Segmentation/"

# Links to additional resources (like code, demo videos, etc.)
links:
    - icon: "github"
      icon_pack: "fab"
      name: "Source code"
      url: "https://github.com/Olorunnisola01/Aerial-image-segmentation-with-unet"

slides: ""
---
#### Project motivation

The usability of an autonomous drone is determined by how reliably it can
fly, navigate and land. Most low-altitude UAVs still lean almost entirely
on GPS and inertial sensing for self-navigation — signals that are of low
semantic intelligence and are prone to failure in exactly the complex,
dynamic, human-designed environments drones are increasingly asked to
operate in. Vision is what closes that gap: a drone that can label the
pixels beneath it as *road*, *vegetation*, *construction*, *person* or
*obstacle* can reason about where it is safe to descend. This project
therefore segments real aerial imagery collected by UAVs using
state-of-the-art deep learning segmentation architectures, as a basis for
further work in autonomous drone vision.

#### Method

3,269 pre-labelled aerial images, shot between roughly 5 and 50 metres
above ground, were used for the experiments. Every pixel is classified
into one of **12 classes** — person, bike, car, drone, boat, animal,
obstacle, construction, vegetation, road, sky and background.

The study ran in two stages:

1. **Architecture selection.** **U-Net** and **DeepLabV3+** were trained
   and evaluated on a shared MobileNetV2 encoder, so the comparison
   isolates the decoder architecture rather than the backbone.
2. **Encoder selection.** The winning architecture was then re-trained
   with four further backbones — **DenseNet121, EfficientNetB0, ResNet50
   and VGG19** — to test whether MobileNetV2's computational efficiency is
   also justifiable on accuracy grounds.

Mean intersection-over-union (mIoU) was the optimising metric; parameter
count, pixel accuracy, precision and F1-score were tracked as satisficing
metrics. The segmentation models themselves (U-Net, FCN-8, LinkNet,
DeepLabV3+) are implemented from scratch as a reusable TensorFlow/Keras
module in the repository rather than pulled from an off-the-shelf library.

#### Results

After 50 epochs, **U-Net reached 45% mIoU against DeepLabV3+'s 37%** on
the shared MobileNetV2 encoder. Re-training U-Net across the remaining
backbones gave **64% (DenseNet121), 64% (ResNet50), 62% (VGG19) and 57%
(EfficientNetB0)** — a substantial jump over MobileNetV2, showing that the
lightweight backbone's efficiency does come at a real accuracy cost here.
**U-Net + DenseNet121** was the best overall choice, combining the top
mIoU with a fair parameter count.

These numbers are a floor rather than a ceiling: training was capped at 50
epochs by Google Colaboratory's limited and time-regulated GPU allocation,
and class weighting — which would help the model resolve the classes that
occupy very few pixels — was left out for the same reason. Additional
data, deeper training and class weighting are the obvious next steps,
followed by deploying the model on a UAV to test in-flight classification
and decision-making.

See the [GitHub repository](https://github.com/Olorunnisola01/Aerial-image-segmentation-with-unet)
for the full implementation, the segmentation-model module, and the
training notebooks for every architecture and encoder combination.
