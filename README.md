# Classificação de Imagens Médicas: Diagnóstico da "Doença de Sauron"

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![TensorFlow](https://img.shields.io/badge/TensorFlow-%23FF6F00.svg?style=for-the-badge&logo=TensorFlow&logoColor=white)
![Keras](https://img.shields.io/badge/Keras-%23D00000.svg?style=for-the-badge&logo=Keras&logoColor=white)
![Google Colab](https://img.shields.io/badge/Google%20Colab-F9AB00?style=for-the-badge&logo=googlecolab&logoColor=white)

Este repositório contém o projeto final desenvolvido para a pós-graduação em **Machine Learning (SENAI)**, focado na classificação binária de imagens de lâminas de sangue para detecção automatizada de patologias.

## 📝 O Desafio
Proposto pela ONG fictícia **"Elfos Muito Legais"**, o objetivo é automatizar o diagnóstico da **"Doença de Sauron"**. O projeto utiliza técnicas de Visão Computacional para identificar a presença de parasitas em células sanguíneas, visando aumentar a velocidade e a precisão dos laudos médicos.

## 📊 O Dataset
* **Volume:** 27.558 imagens de células de sangue.
* **Classes:** 
  * `Parasitized`: Células infectadas (Positivo).
  * `Uninfected`: Células saudáveis (Negativo).
* **Pré-processamento:** As imagens passaram por redimensionamento, normalização e técnicas de *Data Augmentation* (rotação, zoom, flip) para aumentar a capacidade de generalização dos modelos.

## 🚀 Metodologia

Foram implementadas e comparadas duas abordagens principais:

### 1. CNN Customizada (Deep Learning do Zero)
Desenvolvimento de uma rede neural convolucional própria. Focada em extrair características morfológicas específicas das células através de camadas de `Conv2D`, `MaxPooling` e `Dropout` para evitar overfitting.
* **Arquivo:** `Projeto_CNN_Classificacao_da_Doença_Sauron.ipynb`

### 2. Transfer Learning & Fine-Tuning
Utilização do modelo DenseNet121. Esta abordagem foca em adaptar o conhecimento prévio do modelo para a especificidade das imagens médicas.
* **Arquivo:** `Projeto_TL_FT_Classificacao_da_Doença_Sauron.ipynb`

## 📈 Performance Comparativa
Abaixo, a comparação dos resultados obtidos nos dados de teste:

| Modelo | Acurácia | Loss |
| :--- | :---: | :---: |
| **CNN Customizada** | 0.9598 | 0.1335 |
| **Transfer Learning** | 0.9472 | 0.1711 |

## Observações
O modelo de TL não chegou a convergência, ele parou o treinamento devido ao número máximo de épocas predeterminado devido ao tempo de entrega do projeto. 
Acredito que caso ele fosse treinado até convergir em um mínimo local de perda ele iria superar a CNN.

Outro fator a ser levado em conta é a métrica escolhida, devido aos requisitos do projeto utilizei acurácia, mas acredito que pelo contexto médico seria melhor utilizar o F1-Score ou o Recall.

## 🛠️ Tecnologias Utilizadas
* **Linguagem:** Python 3.x
* **Frameworks:** TensorFlow / Keras
* **Manipulação de Dados:** NumPy, Pandas, Scikit-learn
* **Visualização:** Matplotlib, Seaborn
* **Infraestrutura:** Google Colab (Aceleração por GPU)

## 📂 Organização do Repositório
* `Classificacao-de-Imagens-Medicas-...pdf`: Documentação técnica e relatório final do projeto.
* `Projeto_CNN_...ipynb`: Notebook com a implementação da rede neural do zero.
* `Projeto_TL_FT_...ipynb`: Notebook com a implementação de Transfer Learning.

---
**Desenvolvido por:** [Gabriel](https://github.com/Gabriel4210)
*Pós-Graduação em Machine Learning - SENAI*
