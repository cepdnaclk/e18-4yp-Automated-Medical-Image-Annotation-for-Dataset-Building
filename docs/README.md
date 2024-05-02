---
layout: home
permalink: index.html

# Please update this with your repository name and title
repository-name: e18-4yp-Automated-Medical-Image-Annotation-for-Dataset-Building
title: Automated Medical Image Annotation for Dataset Building
---

[comment]: # "This is the standard layout for the project, but you can clean this and use your own template"

# Automated Medical Image Annotation for Dataset Building

#### Table of content

1. [Abstract](#abstract)
2. [Related works](#related-works)
3. [Pipeline](#pipeline)
4. [Results and Analysis](#results-and-analysis)
5. [Conclusion](#conclusion)
6. [Publications](#publications)
7. [Links](#links)

---

## Abstract
Medical image annotation to build datasets leverages in many clinical applications such as diagnosis and treatment planning. Automated medical image annotation shows an efficient solution over manual annotation in dataset building. In this work, we focus on automated user-interactive oral image annotation that could perform automated annotations with assistance of user prompts such as text,points and bounding boxes. Meta AI’s Segment Anything Model (SAM) , a vision foundation model trained on the largest segmentation dataset for interactive promptable segmentation with impressive zero-shot performance has increased the potential for medical image segmentation. However, SAM shows limited performance with the images that differ from the trained dataset or images with challenging conditions like irregular regions and boundaries and text-to-mask task seems exploratory.

In this work, we explore a comprehensive study on automating oral image annotation and related work using the foundation models such as SAM, Dino, Grounding Dino,Grounded SAM addressing the above limitations. At the end, we discuss the potential research gaps in automating medical image annotation and propose our methodology to address the identified gaps.

## Related works
### Object Detection Foundation model 
Grounding DINO
- State-of-the-art zero-shot object-set detection model.
- Support (image,text) input.
- Trained on natural images.
  
![image](https://github.com/vithurshiniS/e18-4yp-Automated-Medical-Image-Annotation-for-Dataset-Building/assets/95094083/1c17c7f1-18f7-4d9d-839e-668ea2c582de)

### Object Segmentation Foundation model 
1) SAM
- A promptable segmentation foundation model
- Support points,box,text annotation input.
- Trained on natural images.
- Leverages zero-shot generalization capability to unseen image distributions and tasks

![image](https://github.com/vithurshiniS/e18-4yp-Automated-Medical-Image-Annotation-for-Dataset-Building/assets/95094083/565cc65c-88fb-44f2-a2fa-3c0ce32888b7)

2) MedSAM
- Based on SAM model specified for medical images

### Models used for Detection and Segmentation
1) Grounded-SAM
- Combines Grounding DINO and SAM : detect and segment anything with text.
- Integrates object detection and segmentation for open-vocabulary tasks for natural images.
  
2) TongueSAM
- Integrates object detection and segmentation for open-vocabulary tasks for natural images.
- Trained only for specific task.

![image](https://github.com/vithurshiniS/e18-4yp-Automated-Medical-Image-Annotation-for-Dataset-Building/assets/95094083/6675638c-b1c1-4dd3-82ac-dff5ba190e35)

### Few-shot paradigm
- Aimed at learning from limited labeled data.
- Leverages the existing knowledge to learn new tasks efficiently. 

### Few-shot keypoint detection
- Predict the keypoints with uncertainty in a query image given the support keypoints.
- N-way-K-shot detection. N: support keypoints K: support images

### Few-shot Segmentation
1) UniverSeg :  Universal Medical Image Segmentation
- Enables solving new segmentation tasks without retraining.
- A novel flexible CrossBlock mechanism that transfers information from the example set to the new image.
- Tasks are dynamically assigned during inference. 

## Pipeline
![image](https://github.com/vithurshiniS/e18-4yp-Automated-Medical-Image-Annotation-for-Dataset-Building/assets/95094083/939791ae-7f67-4c2c-815c-3361f33b6779)

## Results and Analysis
### MedSAM Results
![image](https://github.com/cepdnaclk/e18-4yp-Automated-Medical-Image-Annotation-for-Dataset-Building/assets/95094083/802bbc32-5e73-43cc-8c07-bcef0d72181e)
![image](https://github.com/cepdnaclk/e18-4yp-Automated-Medical-Image-Annotation-for-Dataset-Building/assets/95094083/f6c93172-4523-4f38-93e7-6f7b08339b72)

### MedSAM Finetune (Flare 22 CT dataset)
![image](https://github.com/cepdnaclk/e18-4yp-Automated-Medical-Image-Annotation-for-Dataset-Building/assets/95094083/d7e28671-758e-414a-b68c-dba95218d921)
![image](https://github.com/cepdnaclk/e18-4yp-Automated-Medical-Image-Annotation-for-Dataset-Building/assets/95094083/298e5b6c-6bf4-422d-9b03-bff948a381ea)

### MedSAM Finetune (Tufts Teeth dataset with training)
![image](https://github.com/cepdnaclk/e18-4yp-Automated-Medical-Image-Annotation-for-Dataset-Building/assets/95094083/c85c4dae-6a9e-4d04-9f84-6491ad242510)

### MedSAM Finetune (Tufts Teeth dataset with validation)
![image](https://github.com/cepdnaclk/e18-4yp-Automated-Medical-Image-Annotation-for-Dataset-Building/assets/95094083/b64bba08-6a32-4545-a35e-0720ad6c7e55)
![image](https://github.com/cepdnaclk/e18-4yp-Automated-Medical-Image-Annotation-for-Dataset-Building/assets/95094083/092909c1-9d55-4d37-a691-e6e2d8f7fe83)

### Few-shot keypoint detection Results

Episodic Attention Maps

![image](https://github.com/cepdnaclk/e18-4yp-Automated-Medical-Image-Annotation-for-Dataset-Building/assets/95094083/decc59ec-19ef-45dc-b8e8-294bdb3cf1ef)

Support Images

![image](https://github.com/cepdnaclk/e18-4yp-Automated-Medical-Image-Annotation-for-Dataset-Building/assets/95094083/c823ef59-bc52-4c96-8396-cd96ee18b1de)

Query

![image](https://github.com/cepdnaclk/e18-4yp-Automated-Medical-Image-Annotation-for-Dataset-Building/assets/95094083/7bd5de4f-26e7-4b89-9921-0c1e059d7dea)

Query Prediction

![image](https://github.com/cepdnaclk/e18-4yp-Automated-Medical-Image-Annotation-for-Dataset-Building/assets/95094083/15b142b9-052d-4332-9873-125265a89419)

### UniverSeg Results
![image](https://github.com/cepdnaclk/e18-4yp-Automated-Medical-Image-Annotation-for-Dataset-Building/assets/95094083/a6ce0bec-29e6-48b5-9a27-0aa4c2871ecf)

Increasing the support set size improves the Dice score evaluation of the prediction.

### Visualizations
1) WBC dataset
   Support set samples
   
   ![image](https://github.com/cepdnaclk/e18-4yp-Automated-Medical-Image-Annotation-for-Dataset-Building/assets/95094083/c49f3fc1-5ebf-4860-a6b2-9aa76242539b)

   Test Predictions for varying Support Set Size N
   
   ![image](https://github.com/cepdnaclk/e18-4yp-Automated-Medical-Image-Annotation-for-Dataset-Building/assets/95094083/4fc4efc1-e2e7-4778-97e9-bacd49660c9f)

3) OASIS dataset
   Support set samples
   
   ![image](https://github.com/cepdnaclk/e18-4yp-Automated-Medical-Image-Annotation-for-Dataset-Building/assets/95094083/eec45461-5d3e-4cda-a4a1-839c63d4c8aa)

5) Tufts dataset
   Support set samples
   
   ![image](https://github.com/cepdnaclk/e18-4yp-Automated-Medical-Image-Annotation-for-Dataset-Building/assets/95094083/7d12abab-2ec0-430e-87fa-4d710b634b1f)

   Test Predictions for varying Support Set Size N
   
   ![image](https://github.com/cepdnaclk/e18-4yp-Automated-Medical-Image-Annotation-for-Dataset-Building/assets/95094083/76f630cd-1c03-45f3-a0d6-85857ae7fddc)

6) ISIC2018 dataset
   Support set samples
   
   ![image](https://github.com/cepdnaclk/e18-4yp-Automated-Medical-Image-Annotation-for-Dataset-Building/assets/95094083/3e7dfbc6-789a-4fdb-b22e-8292edb990f0)

   Test Predictions for varying Support Set Size N
   
   ![image](https://github.com/cepdnaclk/e18-4yp-Automated-Medical-Image-Annotation-for-Dataset-Building/assets/95094083/b7613cb5-cb23-4339-b40c-6d019ddecfbb)

## Conclusion

## Publications
[//]: # "Note: Uncomment each once you uploaded the files to the repository"

<!-- 1. [Semester 7 report](./) -->
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
