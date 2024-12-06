# Tomato Plant Disease Classification Based On Symptomps

## Project Description
This project focuses on multiclass classification of tomato plant diseases using images of their leaves. By leveraging EfficientNetB3 and TensorFlow, it identifies and classifies tomato leaf images into specific disease categories or as healthy.

The project aims to assist farmers, agricultural experts, and hobbyists in diagnosing tomato plant diseases efficiently and accurately, reducing the risk of crop failure and promoting better farming practices.

![image](https://github.com/user-attachments/assets/26cc8fc2-a24b-423c-826e-477e275e6813)

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
- keras==2.12.0


### Environment
| | |
| --- | --- |
| CPU | Standard Google Colab VM Processor |
| GPU | Tesla T4 |
| ROM | 100 GB of temporary storage |
| RAM | 12 GB |
| OS | Ubuntu 18.04.6 LTS (Linux-based system) |

## Dataset
The dataset used in this project is obtained from [Kaggle](kaggle.com). It is titled Plant Disease Expert Dataset and provides images of various plant leaves categorized into different classes based on their health or diseases. For this project, we focus exclusively on the data related to tomato plants.
- Link to datasets: https://www.kaggle.com/datasets/sadmansakibmahi/plant-disease-expert
![download (29)](https://github.com/user-attachments/assets/2226a82a-8128-4706-952e-9c53a982beff)

## Results
### Model Performance

#### 1. Metrics

| Model | Epoch | Learning Rate | Batch size | Optimizer | Accuracy | Loss | Validation Accuracy | Validation Loss |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| EfficientNetB3 | 10 |  0.0001 | 32 | Adam | 99.50% | 0.0160 | 99.33% | 0.0221 |
| DenseNet121 | 10 |  0.0001 | 32 | Adam | 98.86% | 0.0328 | 97.21% | 0.0763 |
| ResNet50 | 10 |  0.0001 | 32 | Adam | 99.29% | 0.0208 | 98.55% | 0.0577 |
| InceptionV3 | 10 |  0.0001 | 32 | Adam | 98.98% | 0.0279 | 98.33% | 0.0557 |
| MobileNetV2 | 10 |  0.0001 | 32 | Adam | 99.12% | 0.0290 | 91.29% | 0.4089 |

#### 2. Ablation Study

| Model | Base Model Trainable | Learning Rate | Added Layers | Dropout Rate | Output Layer | Accuracy | Loss | Validation Accuracy | Validation Loss | Test Accuracy | Test Loss |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| EfficientNetB3 (Base) | Frozen | 0.001 | GlobalAveragePooling2D | 0.0 | Dense(9, softmax) | 91.60% | 0.3026 | 91.74% | 0.2630 | 91.26% | 0.285 |
| EfficientNetB3 (Modified 1) | Trainable | 0.0001 | GlobalAveragePooling2D | 0.0 | Dense(9, softmax) | 99.85% | 0.0065 | 99.22% | 0.0271 | 98.67% | 0.0328 |
| EfficientNetB3 (Modified 2) | Frozen | 0.001 | Dense(512, relu), GlobalAveragePooling2D | 0.4 | Dense(9, softmax) | 86.69% | 0.4104 | 91.07% | 0.2892 | 90.92% | 0.3024 |
| EfficientNetB3 (Modified 3) | Trainable | 0.0001 | Dense(512, relu), GlobalAveragePooling2D | 0.4 | Dense(9, softmax) | 99.61% | 0.0133 | 99.11% | 0.0223 | 99.51% | 0.0177 |
| EfficientNetB3 (Modified 4) | Trainable | 0.0001 | Dense(1024, relu), GlobalAveragePooling2D | 0.3 | Dense(9, softmax) | 99.63% | 0.0121 | 98.88% | 0.0341 | 99.68% | 0.0175% |
| EfficientNetB3 (Final) | Trainable | 0.0001 | Dense(512, relu), GlobalAveragePooling2D | 0.5 | Dense(9, softmax) | 99.50% | 0.0160 | 99.33% | 0.0221 | 99.00% | 0.0388 |

#### 3. Training/Validation Curve

![Graph Accuracy](https://github.com/user-attachments/assets/f6cfb9a4-88e6-4cec-a90b-f788ccd37059)
![Graph Loss](https://github.com/user-attachments/assets/c322cc01-c036-4430-9783-a5eb0083bb3c)

### Testing

![tenimage](https://github.com/user-attachments/assets/6ab1bdca-2c9c-4474-b93d-b92d3bccac3d)

### Deployment
We have deployed this product using Streamlit to build the website to be interactive and Ngrok for tunneling from local to internet using Public URL.
Link to our project: https://equipped-oarfish-sharp.ngrok-free.app/

## Supporting Documents
### Presentation Deck
- Link: https://drive.google.com/file/d/1JOzANyhUWw8FcSIBrYdbj7ukkeJLFRKL/view?usp=drive_link

### Business Model Canvas
![Tim 1 SCAI (1)](https://github.com/user-attachments/assets/375fac2d-1af9-4f78-902a-c1ea4a0bddf1)

### Short Video
- Link: https://...

## References
- Link: https://github.com/Sukanyasingh3/AgroAid.git

## Additional Comments
No additional comment at this moment

## How to Cite
If you find this project useful, we'd grateful if you cite this repository:
```
@article{FinalProjectStartupCampusTim1,
  author    = {Team 1, Startup Campus},
  title     = {Tomato Plant Classification Based on Symptoms},
  journal   = {GitHub Repository},
  year      = {2024},
  url       = {https://github.com/abdanrafii/Final-Project-Startup-Campus-Tim-1},
  note      = {Accessed: 2024-12-06}
}

```

## License
For academic and non-commercial use only.

## Acknowledgement
This project entitled <b>"Tomato Plant Disease Classification Based On Symptomps"</b> is supported and funded by Startup Campus Indonesia and Indonesian Ministry of Education and Culture through the "**Kampus Merdeka: Magang dan Studi Independen Bersertifikasi (MSIB)**" program.
