# SCC0270


---

### Projeto Multimodal de Redes Neurais para Detecção e Análise de Tumores Cerebrais (CT + MRI)

---

## Descrição Geral

Este projeto tem como objetivo o desenvolvimento de um modelo de **aprendizado profundo multimodal**, utilizando imagens de **Tomografia Computadorizada (CT)** e **Ressonância Magnética (MRI)** para **detecção, classificação e análise de tumores cerebrais**.

O uso de múltiplas modalidades de imagem permite ao modelo combinar informações complementares:

* **CT:** Estruturas ósseas e calcificações.
* **MRI:** Detalhes de tecidos moles.

Essa abordagem busca auxiliar no **diagnóstico precoce**, na **classificação de tipos de tumores** e como suporte a decisões clínicas.

---

## Sobre o Conjunto de Dados

O dataset foi construído a partir de diferentes fontes públicas e privadas.

* **Modalidades:** CT e MRI.
* **Tipos de Tumores:** Glioma, Meningioma, Pituitário, entre outros.
* **Tamanhos das Imagens:** Diversos (256x256, 512x512).
* **Anotações:** Tipo de tumor, localização (em alguns casos), modalidade da imagem.

---

## Fontes do Conjunto de Dados

### Imagens de Tomografia Computadorizada (CT):

* [CT Brain Segmentation - Roboflow](https://universe.roboflow.com/joshua-zgc7b/ct-brain-segmentation)
* [CT to MRI cGAN - Kaggle](https://www.kaggle.com/datasets/darren2020/ct-to-mri-cgan)
* [CT Head Scans - Kaggle](https://www.kaggle.com/datasets/clarksaben/ct-head-scans)
* [Head CT Images for Classification - Kaggle](https://www.kaggle.com/datasets/nipaanjum/head-ct-images-for-classification)
* Dados privados (Cérebro Anônimo)
* [CT e MRI não pareados - Mendeley Data](https://data.mendeley.com/datasets/z4wc364g79/1)

### Imagens de Ressonância Magnética (MRI):

* [Brain Tumor MRI Scans - Kaggle](https://www.kaggle.com/datasets/rm1000/brain-tumor-mri-scans)
* [Brain Tumor MRIs - Kaggle](https://www.kaggle.com/datasets/vinayjayanti/brain-tumor-mris)
* [Siardataset - Kaggle](https://www.kaggle.com/datasets/masoumehsiar/siardataset)
* [Brain Tumors 256x256 - Kaggle](https://www.kaggle.com/datasets/thomasdubail/brain-tumors-256x256)
* [MRI Image Classification - Kaggle](https://www.kaggle.com/datasets/iashiqul/brain-tumor-mri-image-classification-dataset)
* [Brain Tumor MRI Yes or No - Kaggle](https://www.kaggle.com/datasets/mohamada2274/brain-tumor-mri-yes-or-no)
* [Brain Tumor Class Class - Roboflow](https://universe.roboflow.com/college-sf5ih/brain-tumor-class-class)
* [Brain Tumor Detection - Roboflow](https://universe.roboflow.com/tuan-nur-afrina-zahira/brain-tumor-detection-bmmqz)
* [Tumor Detection - Roboflow](https://universe.roboflow.com/brain-tumor-detection-wsera/tumor-detection-ko5jp)

---

## Objetivos do Projeto

* Classificação de Tumores
* Segmentação de Áreas Tumorais
* Detecção Binária (Tumor / Sem Tumor)
* Fusão de Modalidades (CT + MRI)
* Tradução entre Modalidades (ex.: geração de MRI a partir de CT)

---

## Importância Clínica e Científica

* Diagnóstico precoce
* Apoio à decisão clínica
* Pesquisa em fusão multimodal de imagens médicas
* Desenvolvimento de sistemas CAD (Computer-Aided Diagnosis)

---

## Modelos

### Classificação

* CNNs (ResNet, VGG, EfficientNet)
* Vision Transformers (ViT)
* Modelos multimodais com Early e Late Fusion

### Segmentação

* U-Net, U-Net++
* 3D U-Net
* SegNet
* Mask R-CNN para imagens médicas

### Tradução entre Modalidades / Geração de Imagens

* CycleGAN
* pix2pix GAN

---

## Estratégias de Fusão Multimodal

| Estratégia      | Descrição                                             |
| --------------- | ----------------------------------------------------- |
| Early Fusion    | CT e MRI como múltiplos canais na entrada             |
| Late Fusion     | Processamento separado + fusão posterior das features |
| Cross-Attention | Mecanismo de atenção cruzada entre as features        |

---

## Métricas de Avaliação

### Para Classificação:

* Accuracy
* Precision / Recall / F1-score
* AUC-ROC

### Para Segmentação:

* Dice Coefficient
* IoU (Intersection over Union)
* Hausdorff Distance

---

## Possíveis Aplicações

* Ferramentas clínicas com IA
* Suporte à radiologia e neurocirurgia
* Pesquisa em aprendizado multimodal
* Sistemas hospitalares de diagnóstico

---

## Referências Científicas

* Isensee, F. et al. (2021). nnU-Net: A self-configuring method for deep learning-based biomedical image segmentation. *Nature Methods*.
* Zhou, Z. et al. (2018). UNet++: A Nested U-Net Architecture for Medical Image Segmentation. *Springer*.
* Zhou, T., Ruan, S., Canu, S. (2019). Deep Learning for Medical Image Segmentation Using Multi-Modality Fusion. *Array*.
* Ronneberger, O. et al. (2015). U-Net: Convolutional Networks for Biomedical Image Segmentation. *MICCAI*.

---
