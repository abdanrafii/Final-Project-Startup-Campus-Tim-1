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
| Nicholas Dominic | Startup Campus, AI Track | nic.dominic@icloud.com | [link](https://linkedin.com/in/nicholas-dominic) | Supervisor |

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

| model | epoch | learning_rate | batch_size | optimizer | val_loss | val_precision | val_recall | ... |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| vit_b_16 | 1000 |  0.0001 | 32 | Adam | 0.093 | 88.34% | 84.15% | ... |
| vit_l_32 | 2500 | 0.00001 | 128 | SGD | 0.041 | 90.19% | 87.55% | ... |
| ... | ... | ... | ... | ... | ... | ... | ... | ... | 

#### 2. Ablation Study
Any improvements or modifications of your base model, should be summarized in this table. Feel free to adjust the columns in the table below.

| model | layer_A | layer_B | layer_C | ... | top1_acc | top5_acc |
| --- | --- | --- | --- | --- | --- | --- |
| vit_b_16 | Conv(3x3, 64) x2 | Conv(3x3, 512) x3 | Conv(1x1, 2048) x3 | ... | 77.43% | 80.08% |
| vit_b_16 | Conv(3x3, 32) x3 | Conv(3x3, 128) x3 | Conv(1x1, 1028) x2 | ... | 72.11% | 76.84% |
| ... | ... | ... | ... | ... | ... | ... |

#### 3. Training/Validation Curve
Insert an image regarding your training and evaluation performances (especially their losses). The aim is to assess whether your model is fit, overfit, or underfit.

![graph accuracy](https://github.com/user-attachments/assets/977179f6-bfd4-423f-8eb7-49bd168ee9db)
![graph loss](https://github.com/user-attachments/assets/59f3a76b-09df-4e69-8a35-157d6eb27d99)

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
