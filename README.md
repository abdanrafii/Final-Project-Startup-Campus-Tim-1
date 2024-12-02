# Tomato Plant Disease Classification Based On Symptomps

## Project Description
Please describe your Startup Campus final project here. You may should your <b>model architecture</b> in JPEG or GIF.

## Contributor
| Full Name | Affiliation | Email | LinkedIn | Role |
| --- | --- | --- | --- | --- |
| Adelia Virnanda Putri Suhadi | Universitas Muhammadiyah Surabaya | adeliavirnandaps@gmail.com | [link](https://www.linkedin.com/in/adelia-virnanda-putri-suhadi-218972218?utm_source=share&utm_campaign=share_via&utm_content=profile&utm_medium=android_app) | Treasurer |
| Muhammad Abdan Rafi'i | Universitas Sebelas Maret | abdanrafii@student.uns.ac.id | [link](https://www.linkedin.com/in/muhammad-abdan-rafii/) | Team Lead |
| A'yun Fa'yuni | Universitas Nahdlatul Ulama Sunan Giri Bojonegoro | ayunfayunii@gmail.com | [link](https://www.linkedin.com/in/a-yun-fa-yuni-686a56246?utm_source=share&utm_campaign=share_via&utm_content=profile&utm_medium=android_app) | Team Member |
| Al Hafiz Defriansyah | Politeknik Negeri Sriwijaya | alhafizdefriansyah41@gmail.com | [link](https://www.linkedin.com/in/alhafizdefriansyah?utm_source=share&utm_campaign=share_via&utm_content=profile&utm_medium=android_app) |Team Member |
| Ardhya Xeonanda Pradipta | Universitas Sebelas Maret | ardhya@student.uns.ac.id | [link](https://www.linkedin.com/in/ardhya-xeonanda/) | Team Member |
| Edgar Hafizh Alfarizi | Universitas Negeri Surabaya | edgar.21003@mhs.unesa.ac.id | [link](https://www.linkedin.com/in/edgarhafizh002?utm_source=share&utm_campaign=share_via&utm_content=profile&utm_medium=ios_app) | Team Member |
| Aries Fitriawan | Startup Campus, AI Track | aries.fitriawan@ioh.co.id | [link](https://www.linkedin.com/in/ariesfitriawan/) | Mentor |

## Setup
### Prerequisite Packages (Dependencies)
- numpy==1.23.5
- matplotlib==3.6.2
- tensorflow==2.12.0
- ...
- ...

### Environment
| | |
| --- | --- |
| CPU | Example: Apple M3 Pro 12-core CPU |
| GPU | Example: Tesla T4 (x1) |
| ROM | Example: 1 TB SSD |
| RAM | Example: 36 GB |
| OS | Example: macOS Sonoma v14.1.1 |

## Dataset
The dataset used in this project is obtained from [Kaggle](kaggle.com). It is titled Plant Disease Expert Dataset and provides images of various plant leaves categorized into different classes based on their health or diseases. For this project, we focus exclusively on the data related to tomato plants.
- Link to datasets: https://www.kaggle.com/datasets/sadmansakibmahi/plant-disease-expert
![download (29)](https://github.com/user-attachments/assets/2226a82a-8128-4706-952e-9c53a982beff)

## Results
### Model Performance
Describe all results found in your final project experiments, including hyperparameters tuning and architecture modification performances. Put it into table format. Please show pictures (of model accuracy, loss, etc.) for more clarity.

#### 1. Metrics
Inform your model validation performances, as follows:
- For classification tasks, use **Precision and Recall**.
- For object detection tasks, use **Precision and Recall**. Additionaly, you may also use **Intersection over Union (IoU)**.
- For image retrieval tasks, use **Precision and Recall**.
- For optical character recognition (OCR) tasks, use **Word Error Rate (WER) and Character Error Rate (CER)**.
- For adversarial-based generative tasks, use **Peak Signal-to-Noise Ratio (PNSR)**. Additionally, for specific GAN tasks,
  - For single-image super resolution (SISR) tasks, use **Structural Similarity Index Measure (SSIM)**.
  - For conditional image-to-image translation tasks (e.g., Pix2Pix), use **Inception Score**.

Feel free to adjust the columns in the table below.

| Model | Epoch | Learning Rate | Batch size | Optimizer | Accuracy | Loss | Validation Accuracy | Validation Loss |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| EfficientNetB3 | 10 |  0.0001 | 32 | Adam | 99.50% | 0.0160 | 99.33% | 0.0221 |
| DenseNet121 | 10 |  0.0001 | 32 | Adam | 98.86% | 0.0328 | 97.21% | 0.0763 |
| ResNet50 | 10 |  0.0001 | 32 | Adam | 99.29% | 0.0208 | 98.55% | 0.0577 |
| InceptionV3 | 10 |  0.0001 | 32 | Adam | 98.98% | 0.0279 | 98.33% | 0.0557 |
| MobileNetV2 | 10 |  0.0001 | 32 | Adam | 99.12% | 0.0290 | 91.29% | 0.4089 |

#### 2. Ablation Study
Any improvements or modifications of your base model, should be summarized in this table. Feel free to adjust the columns in the table below.

| Model | Base Model Trainable | Learning Rate | Added Layers | Dropout Rate | Output Layer | Accuray | Loss | Validation Accuracy | Validation Loss | Test Accuracy | Test Loss |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| EfficientNetB3 (Base) | Frozen | 0.001 | GlobalAveragePooling2D | 0.0 | Dense(9, softmax) | 91.60% | 0.3026 | 91.74% | 0.2630 | 91.26% | 0.285 |
| EfficientNetB3 (Modified 1) | Trainable | 0.0001 | GlobalAveragePooling2D | 0.0 | Dense(9, softmax) | 99.85% | 0.0065 | 99.22% | 0.0271 | 98.67% | 0.0328 |
| EfficientNetB3 (Modified 2) | Frozen | 0.001 | Dense(512, relu), GlobalAveragePooling2D | 0.4 | Dense(9, softmax) | 86.69% | 0.4104 | 91.07% | 0.2892 | 90.92% | 0.3024 |
| EfficientNetB3 (Modified 3) | Trainable | 0.0001 | Dense(512, relu), GlobalAveragePooling2D | 0.4 | Dense(9, softmax) | 99.61% | 0.0133 | 99.11% | 0.0223 | 99.51% | 0.0177 |
| EfficientNetB3 (Modified 4) | Trainable | 0.0001 | Dense(1024, relu), GlobalAveragePooling2D | 0.3 | Dense(9, softmax) | 99.63% | 0.0121 | 98.88% | 0.0341 | 99.68% | 0.0175% |
| EfficientNetB3 (Final) | Trainable | 0.0001 | Dense(512, relu), GlobalAveragePooling2D | 0.5 | Dense(9, softmax) | 99.50% | 0.0160 | 99.33% | 0.0221 | 99.00% | 0.0388 |

#### 3. Training/Validation Curve
Insert an image regarding your training and evaluation performances (especially their losses). The aim is to assess whether your model is fit, overfit, or underfit.

![Graph Accuracy](https://github.com/user-attachments/assets/f6cfb9a4-88e6-4cec-a90b-f788ccd37059)
![Graph Loss](https://github.com/user-attachments/assets/c322cc01-c036-4430-9783-a5eb0083bb3c)

### Testing
Show some implementations (demos) of this model. Show **at least 10 images** of how your model performs on the testing data.

![tenimage](https://github.com/user-attachments/assets/6ab1bdca-2c9c-4474-b93d-b92d3bccac3d)

### Deployment (Optional)
Describe and show how you deploy this project (e.g., using Streamlit or Flask), if any.

## Supporting Documents
### Presentation Deck
- Link: https://...

### Business Model Canvas
Provide a screenshot of your Business Model Canvas (BMC). Give some explanations, if necessary.

### Short Video
Provide a link to your short video, that should includes the project background and how it works.
- Link: https://...

## References
Provide all links that support this final project, i.e., papers, GitHub repositories, websites, etc.
- Link: https://github.com/Sukanyasingh3/AgroAid.git
- Link: https://...
- Link: https://...

## Additional Comments
Provide your team's additional comments or final remarks for this project. For example,
1. ...
2. ...
3. ...

## How to Cite
If you find this project useful, we'd grateful if you cite this repository:
```
@article{
...
}
```

## License
For academic and non-commercial use only.

## Acknowledgement
This project entitled <b>"Tomato Plant Disease Classification Based On Symptomps"</b> is supported and funded by Startup Campus Indonesia and Indonesian Ministry of Education and Culture through the "**Kampus Merdeka: Magang dan Studi Independen Bersertifikasi (MSIB)**" program.
