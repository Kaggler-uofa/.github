## Kaggle Competition : SenNet + HOA - Hacking the Human Vasculature in 3D

**Team members :** [Hyunji Cha](https://github.com/mochimuchi), [Minjae Jeong](https://github.com/JJalswo), Min Joh, [Jin Yoo](https://github.com/jinyoo1021)


> **Competition Information:**\
> Title: SenNet + HOA - Hacking the Human Vasculature in 3D\
> Host: SenNet + HOA\
> Platform: Kaggle\
> Final Submission Deadline: February 6, 2024\
> Link: https://www.kaggle.com/competitions/blood-vessel-segmentation

### Overview
The goal of this competition is to segment blood vessels. You will create a model trained on 3D Hierarchical Phase-Contrast Tomography (HiP-CT) data from human kidneys to help complete a picture of vasculature throughout a body.

Your work will better researchers' understanding of the size, shape, branching angles, and patterning of blood vessels in human tissue.

---
### Description
Your body's organs and tissues depend on the interaction, spatial organization, and specialization of your cells—all 37 trillion of them. Researchers make sense of cellular functions and relationships with the Vasculature Common Coordinate Framework (VCCF). The VCCF maps cells using the blood vasculature in the human body as the primary navigation system. The framework crosses all scale levels and provides a unique way to identify cellular locations using capillary structures as an address. However, the gaps in what researchers know about the vasculature lead to gaps in the VCCF. If data science could help automatically segment vasculature arrangements, researchers could use the real-world tissue data to fill in those gaps and complete their picture of the vasculature throughout the body.

Currently, human expert annotators manually trace the vascular structures—a slow process. Even with expert annotators, each new dataset takes 6+ months to complete. Machine learning approaches using this manual data do not generalize well to new datasets because of the variability of both human anatomy and to changes in the image quality as HiP-CT technology continues to improve and change.

Competition host the Common Fund’s Cellular Senescence Network (SenNet) Program was established to comprehensively identify and characterize the differences in senescent cells across the body, across various states of human health, and across the lifespan. SenNet provides publicly accessible atlases of senescent cells and develops innovative tools and technologies that build upon previous advances in single-cell analysis.

SenNet is joined by the Human Organ Atlas (HOA) for this competition. HOA is a digital atlas containing 3D multi-resolution imaging datasets, created at the world’s brightest synchrotron (European Synchrotron Radiation Facility), using an imaging technique called Hierarchical Phase-Contrast Tomography (HiP-CT). HiP-CT spans a previously poorly explored scale in researchers’ understanding of human anatomy, from microns to entire intact organs.

Your efforts could ​​​​improve our understanding of the effect of vasculature on different cells in the human body. With better data, researchers could simulate the flow of blood, oxygen, or even drugs through the vessel network. They could also use the available organ images to augment their understanding of how blood vasculature changes as sex, age, and BMI change. Ultimately, you could help pave the way towards a more complete Vascular Common Coordinate Framework (VCCF) and Human Reference Atlas (HRA), which could identify how the relationships between cells affect our health.

---
# Our Performance

### ML Flowchart
<img src="https://github.com/Kaggler-uofa/.github/blob/84863602bcdcacc1cf8da84abed73dd8132cf983/profile/image/ML_Flowchart.drawio.svg" width=40% height=40% title="flowchart">

1. **Data Preparation:** You have gathered a dataset consisting of images and their corresponding masks, which delineate the vascular structures. These images and masks are obtained from specified paths.

2. **Data Augmentation:** To increase the diversity of your dataset and improve the robustness of your model, you have applied augmentation techniques to both the images and their corresponding masks.

3. **Model Training:** An artificial intelligence model is then trained using the augmented images. The model outputs predicted masks, which are estimates of the actual vascular structures.

4. **Loss Calculation:** A loss function is used to calculate the discrepancy between the predicted masks and the actual masks, providing a loss value that quantifies the model's performance.

5. **Optimization:** With the use of a train loader to feed data, an optimizer to adjust the model parameters, and the loss function to guide improvements, your model is trained and subsequently saved, along with the training loss information.

6. **Evaluation:** Finally, the model is evaluated to determine its performance in terms of validation loss, ensuring that it generalizes well to new, unseen data.

---
### Development Environment
- Main :
    - python3, numpy, pandas, skimage, torch
    - <details>
        <summary>All env</summary>
        
            ```txt
            numpy==1.26.3
            pandas==2.1.4
            scikit-image==0.22.0
            tqdm==4.62.2
            albumentations==1.3.1
            matplotlib==3.8.2
            seaborn==0.11.2
            torch==2.1.2
            torchvision==0.16.2
            torchinfo==1.5.2
            ```
    </details>

---
### Visualizing the Dataset


---
### Image Processing
<img src="https://github.com/Kaggler-uofa/.github/blob/main/profile/image/kidney_1_dense_image_0700.jpeg" width=20% height=20% title="kidney_1_700"> <img src="https://github.com/Kaggler-uofa/.github/blob/main/profile/image/kidney_1_dense_label_0700.jpeg" width=20% height=20% title="kidney_1_label_700">

---
---
### Organizers & Sponsors
![organizer](https://www.googleapis.com/download/storage/v1/b/kaggle-user-content/o/inbox%2F1536542%2F8fdef9f263e948c0550ee04f8f41fb14%2Fk4-all-sponsors.png?generation=1699368938207653&alt=media)

---
### Citation
Yashvardhan Jain, Katy Borner, Claire Walsh, Nancy Ruschman, Peter D. Lee, Griffin M. Weber, Ryan Holbrook, Addison Howard. (2023). SenNet + HOA - Hacking the Human Vasculature in 3D. Kaggle. https://kaggle.com/competitions/blood-vessel-segmentation
