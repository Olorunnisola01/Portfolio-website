---
title: "A comparative case study on the impact of architecture, loss function, and augmentation on CNN robustness using the NEU-CLS dataset"

# Authors
# If you created a profile for a user (e.g. the default `admin` user), write the username (folder name) here 
# and it will be replaced with their full name and linked to their profile.
authors:
- Adeleke Olorunnisola Oyeyemi
- Oluwajire Oluwatimilehin

# Author notes (optional)
author_notes:
- "First Author"
- "Second Author"

# Schedule page publish date (NOT publication's date).
# publishDate: "2017-01-01T00:00:00Z"

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["2"]

# Publication name and optional abbreviated publication name.
publication: In *The International Journal of Advanced Manufacturing Technology*, vol. 143, pp. 2545-2558
publication_short: In *IJAMT*

date: "2026-02-23T00:00:00Z"

abstract: Convolutional Neural Network (CNN) models often report high accuracy on controlled, curated datasets, such as the NEU steel surface defect dataset; however, this performance frequently fails to translate to robust real-world applications. This study investigates this gap by conducting a comprehensive comparative study of 36 model configurations, spanning six distinct architectures (VGG19, ResNet50, DenseNet121, InceptionV3, EfficientNetB0, and MobileNetV3Small). We examined the interplay between these backbones and hybrid combinations of three loss functions -- Sparse Categorical Cross-Entropy (SCCEL), Focal Loss (FL), and Supervised Contrastive Loss (SCL). The models were evaluated for robustness against synthetic corruptions (noise, blur, illumination), cross-domain generalization to an out-of-distribution (OOD) dataset, and deployment efficiency. Our results challenge the validity of clean accuracy as a sole performance metric -- while ResNet50 achieved perfect in-distribution accuracy (100%), it exhibited severe fragility under distributional shifts, highlighting the tendency of standard Cross-Entropy minimization to induce overfitting in high-capacity models. In contrast, EfficientNetB0 configurations demonstrated the highest resilience to environmental corruptions (mCE of 0.043). Critically, we found that loss function design is a primary driver of generalization. The VGG19 architecture, when trained with a hybrid SCL+FL loss, achieved superior cross-domain generalization (F1-score of 0.92) on the target OOD class. This study provides empirical evidence that for small-data industrial tasks, combining modern efficient architectures or simpler networks with contrastive-hybrid loss mechanisms offers the optimal pathway to industrial robustness.

# Summary. An optional shortened abstract.
summary: "A 36-configuration comparative study of CNN architectures and loss functions for steel surface defect detection, showing that robustness under distributional shift and cross-domain generalization diverge sharply from clean in-distribution accuracy."

tags:
- Machine Learning
- Computer Vision
- Smart Manufacturing

# Display this page in the Featured widget?
featured: false


links:
    - icon: "link"
      icon_pack: "fas"
      name: "DOI"
      url: "https://doi.org/10.1007/s00170-026-17729-y"
    - icon: "kaggle"
      icon_pack: "fab"
      name: "Dataset"
      url: "https://www.kaggle.com/datasets/adelekeolorunnisola/surface-defect"

# Custom links (uncomment lines below)


# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
image:
  caption: ""
  focal_point: ""
  preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
projects:
- Material_Defect_Detection


# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
slides: ""
---
