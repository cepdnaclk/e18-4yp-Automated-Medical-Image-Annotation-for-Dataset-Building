---
layout: home
permalink: index.html

# Please update this with your repository name and title
repository-name: e18-4yp-Automated-Medical-Image-Annotation-for-Dataset-Building
title: Automated Medical Image Annotation for Dataset Building
---

[comment]: # "This is the standard layout for the project, but you can clean this and use your own template"

# A Comparative Study on Generalized Automated Medical Image Segmentation for Dataset Building

#### Table of content

1. [Introduction](#introduction)
2. [Approach](#approach)
3. [Results and Analysis](#results-and-analysis)
4. [Conclusion](#conclusion)
5. [Publications](#publications)
6. [Links](#links)

---

## Introduction
Medical image annotation plays a crucial role in building datasets for clinical applications, such as diagnosis, treatment planning, and research. However, the manual annotation process is labor-intensive, time-consuming, costly, and prone to human error, requiring trained experts to handle complex anatomical structures with low contrast, overlapping or blurry boundaries, and irregular regions of interest (ROI). These challenges necessitate the development of automated solutions to enhance the efficiency and scalability of medical image annotation.

Traditional deep learning models, while effective, often require retraining or fine-tuning for novel annotation tasks, which is not feasible for clinical annotators due to the time and expertise required. To address these limitations, few-shot learning approaches have gained popularity for their ability to generalize to unseen annotation tasks involving new anatomies and image modalities using only a limited number of image-label pairs, without the need for additional retraining.

In this work, we comprehensively study the generalizability of state-of-the-art few-shot learning segmentation models for medical images, evaluating their performance across diverse medical datasets and identifying their limitations. Our research aims to identify effective models for generalized automated medical image segmentation, focusing on region annotations (segmentation). By using a small set of support images as references for unseen tasks, these models can automate the annotation process, significantly improving the efficiency and accuracy of medical image annotation, thus supporting various clinical applications more effectively.

## Approach
### Automated Annotation
![image](https://github.com/user-attachments/assets/8b00402e-ea8f-4b57-be67-f35d9cb95cfe)

### Research Objectives
There is need of consistent performance across diverse data & complex domain shifts, No re-training & fine-tuning required for new unseen tasks which saves time & resources, Clinical researchers do not need any expertise.
* Focus on Comparative Study of Generalizable Models for Medical Image Segmentation without re-training or fine-tuning.
* Provide an overview of advantages of Generalizable Models to build a automated medical image annotation system.
![image](https://github.com/user-attachments/assets/8eba089e-5226-4721-bd83-cae270a1aab2)


## Results and Analysis

![image](https://github.com/user-attachments/assets/5f7f5d16-c4aa-4caf-80a4-9f3b5b882790)

In one-shot setting, SegGPT & PerSAM show the high performance where UniverSeg & Painter lag behind. In few-shot setting, UniverSeg followed by SegGPT show high performance. This shows the potential for improvement of model's performance with more support samples. 

![image](https://github.com/user-attachments/assets/4b8fde73-8573-4d29-b265-1c9ab5aa0fe6)


![image](https://github.com/user-attachments/assets/5c85061d-a734-41c9-860a-d2202fec6391)

Increasing the support set size improves the average dice score evaluation of the prediction across different medical image modalities.

![image](https://github.com/user-attachments/assets/4650ee65-8624-4f1b-b919-305bade7d916)

These visual representations of few-shot baselines UniverSeg & SegGPT on the diverse medical image modalities hold evidence for the improvement of prediction performance with the increase of support size by which the predictions closely match the ground truth masks. 

## Conclusion

This work investigates approaches for adapting to new, unseen segmentation tasks by experts without the need for model retraining and fine-tuning on large datasets. The choice of a segmentation model for specific medical image applications depends on the characteristics of the dataset and the required performance level. Our analysis highlights that foundational models like SAM, MedSAM, and Grounding Dino, which are trained on natural image domains, often fall short in medical image segmentation due to domain-specific complexities that these models do not inherently address.

From the comparative results, it is evident that few-shot learning approaches offer a viable solution for medical image segmentation tasks, as they can predict labels without extensive retraining and fine-tuning, even when data is limited. 

Overall, this analysis underscores the efficacy of few-shot learning models in medical image segmentation, particularly for applications requiring rapid adaptation to new tasks without the overhead of retraining. These findings support the broader conclusion that few-shot learning approaches are well-suited for generalizing across unseen image modalities in a single pass during inference, offering a practical and efficient solution for medical image annotation challenges. This adaptability makes few-shot learning models a valuable tool in clinical settings where new and varied segmentation tasks frequently arise.

## Publications
[//]: # "Note: Uncomment each once you uploaded the files to the repository"

 1. [Final Presentation Slides](https://docs.google.com/presentation/d/1qMW0ntk3r72oQNNPejfo2Oda9H3w-_hmxwdWZx57jaI/edit?usp=sharing) 
<!-- 2. [Semester 7 slides](./) -->
<!-- 3. [Semester 8 report](./) -->
<!-- 4. [Semester 8 slides](./) -->
<!-- 5. Author 1, Author 2 and Author 3 "Research paper title" (2021). [PDF](./). -->

#### Team

- E/18/245, Nishani K., [email](mailto:e18245@eng.pdn.ac.lk)
- E/18/340, Vithurshini S., [email](mailto:e18340@eng.pdn.ac.lk)
- E/18/366, Thulasiyan Y., [email](mailto:e18366@eng.pdn.ac.lk)


#### Supervisors

- Prof. Roshan G. Ragel, [email](mailto:roshanr@eng.pdn.ac.lk)
- Dr. Isuru Nawinne, , [email](mailto:isurunawinne@eng.pdn.ac.lk)
- Devindi G.A.I, [email](mailto:e17058@eng.pdn.ac.lk)
- Liyanage S.N, [email](mailto:e17190@eng.pdn.ac.lk)
  
## Links

[//]: # ( NOTE: EDIT THIS LINKS WITH YOUR REPO DETAILS )

- [Project Repository](https://github.com/cepdnaclk/e18-4yp-Automated-Medical-Image-Annotation-for-Dataset-Building)
- [Project Page](https://cepdnaclk.github.io/e18-4yp-Automated-Medical-Image-Annotation-for-Dataset-Building/)
- [Department of Computer Engineering](http://www.ce.pdn.ac.lk/)
- [University of Peradeniya](https://eng.pdn.ac.lk/)

[//]: # "Please refer this to learn more about Markdown syntax"
[//]: # "https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet"
