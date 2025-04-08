# 🧠 Violence-Instigating Bangla Text Identification System

This repository contains the implementation of a deep learning-based system for detecting **violence-inciting Bangla text**, developed as part of the Deep Learning course for the **M.Sc. (Engg.)** degree in Computer Science and Engineering (CSE) at Rangamati Science and Technology University. The project leverages the **Vio-Lens dataset** from **BLP Shared Task 1: Violence Inciting Text Detection (VITD)**.

---


## 📘 Introduction

With the increasing misuse of social media to spread communal hatred and violence, this project focuses on building automated systems to detect violence-inciting text in Bangla. The model classifies YouTube comments into three classes — Direct Violence, Passive Violence, and Non-Violence — using a variety of deep learning and transformer-based models.

---

## 📊 Dataset

- **Name**: Vio-Lens Dataset (BLP Shared Task 1: VITD)
- **Source**: YouTube comments from top 9 violent incidents in Bengal Region (Bangladesh and West Bengal)
- **Samples**:
  - Train: 2700
  - Dev: 1330
  - Test: 2016
- **Languages**: Bangla


### 🔖 Label Definitions

| Label | Category         |
|-------|------------------|
| 0     | Non-Violence     |
| 1     | Passive Violence |
| 2     | Direct Violence  |

### 📉 Class Distribution

**Train Set**:
- Direct Violence: 15%
- Passive Violence: 34%
- Non-Violence: 51%

**Dev Set**:
- Direct Violence: 15%
- Passive Violence: 31%
- Non-Violence: 54%

**Test Set**:
- Direct Violence: 9.97%
- Passive Violence: 35.66%
- Non-Violence: 54.37%

---

## 📌 Task Description

The goal is to classify Bangla text into:
1. **Direct Violence** – Explicit threats (e.g., killing, rape, forceful conversion)
2. **Passive Violence** – Derogatory/abusive language, slang, or justification of violence
3. **Non-Violence** – General or non-violent content

This is a **multi-class classification task**.

---

## 🧹 Data Preprocessing


- Removal of:
  - Emojis
  - Special characters
  - Non-Bangla text
  - Repeated punctuation
- Tokenization using SentencePiece for transformer-based models

---

## 🔁 Data Augmentation

To address class imbalance, we used:
- **Back Translation** (Bangla → English → Bangla) for minority classes (Direct & Passive Violence)

---

## 🏗️ Models Explored

### 🔹 Deep Learning Architectures

- CNN
- LSTM
- BiLSTM
- BiGRU
- CNN + LSTM
- CNN + BiLSTM
- CNN + BiGRU
- LSTM + CNN
- BiLSTM + CNN
- BiGRU + CNN

These hybrid architectures combine the strengths of convolutional and recurrent layers for sequential and spatial feature extraction.

---

## 🤖 Transformer-Based Models

- **BERT Multilingual (Cased)**
- **XLM-RoBERTa (Base)**
- **BanglaBERT (Base)**
- **BanglaBERT**
- **BanglaBERT with MLP**



---

## 🧠 Final Model: BanglaBERT + MLP

The final and best-performing model combines **BanglaBERT** with an extra **Multi-Layer Perceptron (MLP)** classification head.

**Performance**:
- **Macro-F1 (Development Set)**: 0.76
- **Macro-F1 (Test Set)**: 0.75

---

## 🧠 Final Model Architecture

It will be Updated Soon...

---

## 📈 Evaluation

It will be Updated Soon...

---

## 📊 Results

It will be Updated Soon...

---

## 📊 Acknowledgement 

I would like to sincerely thank **Md. Mynoddin, Assistant Professor, Department of Computer Science and Engineering, Rangamati Science and Technology University (RMSTU)**, for his invaluable guidance and support during the Deep Learning course of the 2nd Semester in the M.Sc. (Engineering) program. His encouragement was crucial to the completion of this work.

---

## 📖 Citation

If you use this dataset or task in your work, please cite the following:

### 📚 Dataset Paper

```bibtex
@inproceedings{SahaAndJunaed,
  title = "Vio-Lens: A Novel Dataset of Annotated Social Network Posts Leading to Different Forms of Communal Violence and its Evaluation",
  author= "Saha, Sourav and Junaed, Jahedul Alam  and Saleki, Maryam and Sharma, Arnab Sen and Rifat, Mohammad Rashidujjaman and Rahout, Mohamed and Ahmed, Syed Ishtiaque and Mohammad, Nabeel and Amin, Mohammad Ruhul",
  booktitle =  "Proceedings of the 1st International Workshop on Bangla Language Processing (BLP-2023)",
  month = "Dec",
  year = "2023",
  publisher = "Association for Computational Linguistics",
  address = "Singapore",
}

``` 

### 📌 Task Description Paper

```bibtex

@inproceedings{blp2023-overview-task1,
  title = "BLP-2023 Task 1: Violence Inciting Text Detection (VITD)",
  author= "Saha, Sourav and Junaed, Jahedul Alam and Saleki, Maryam and Rahouti, Mohamed and Mohammed, Nabeel and Amin, Mohammad Ruhul",
  booktitle =  "Proceedings of the 1st International Workshop on Bangla Language Processing (BLP-2023)",
  month = "Dec",
  year = "2023",
  publisher = "Association for Computational Linguistics",
  address = "Singapore",
}
```



## 📚 References

- [BLP Shared Task Website](https://github.com/blp-workshop/blp_task1)
- [BanglaBERT Paper on arXiv](https://aclanthology.org/2022.findings-naacl.98/)
- [BanglaBERT Paper on arXiv](https://aclanthology.org/2020.emnlp-main.207/)

---

## 📬 Contact

For questions or collaborations, feel free to reach out to:

- Prosenjit Chakraborty
- Dept. of CSE
- Rangamati Science and Technology University
- [Connect With Me](https://prosenjit-ch.github.io/Prosenjit-Chakraborty/#)
