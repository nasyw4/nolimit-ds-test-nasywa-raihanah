# 🚀 NoLimit Data Scientist Test — NLP Sentiment Analysis  
NLP Sentiment Analysis on E-Commerce Product & Service Reviews  
*(By: Nasywa Raihanah)*

---

## 📌 Overview
Project ini dibuat sebagai bagian dari NoLimit Data Scientist Technical Test.  
Tujuan utama proyek ini adalah membangun model **sentiment analysis** menggunakan **Hugging Face Transformers** dan **embeddings**, dengan dataset review produk/jasa dari berbagai sumber.

Model akan mengklasifikasikan sentiment menjadi:
- **positive**
- **neutral**
- **negative**

Selain itu, proyek ini dilengkapi dengan:
- EDA,
- preprocessing,
- model training & evaluation,

---

## 📁 Repository Structure

`nolimit-ds-test/`
├── `data/`
│   ├── `raw/`
│   ├── `processed/`
│   └── `sample/`
├── `notebooks/`
│   ├── `EDA & Preprocessing.ipynb`
│   └── `Train Test Split & Modeling & Evaluation.ipynb`
├── `src/`
├── `flowchart/`
│   └── `pipeline.png`
├── `requirements.txt`
└── `README.md`


---

## 📊 Dataset
Dataset yang digunakan merupakan gabungan dari beberapa dataset review publik Kaggle (e-commerce & online services), yang memiliki:

| Column        | Description |
|---------------|-------------|
| `review_text` | Teks ulasan customer |
| `rating`      | Rating 1–5 |
| `sentiment`   | Label hasil mapping rating → sentiment |

(Dataset tidak bisa di upload ke github karena size yang besar)
Link Dataset:
1. https://www.kaggle.com/datasets/farhan999/tokopedia-product-reviews?resource=download
2. https://www.kaggle.com/datasets/satyaahb/ecommerce-ratings-and-reviews-in-bahasa-indonesia
3. https://www.kaggle.com/datasets/satyaahb/e-commerce-sampled-reviews-in-bahasa-indonesia
4. https://drive.google.com/drive/folders/1zpL6veYJJUyKfpK1mx2X0vD0gVXUZcpy?usp=sharing (data selama proses preprocessing dan training model)

### 🔄 Rating to Sentiment Mapping
- **1–2** → negative  
- **3** → neutral  
- **4–5** → positive  

Dataset sudah melalui proses:
- Standar kolom  
- Drop kolom tidak relevan  
- Cleaning  
- Remove duplicates  
- Remove missing values  

---

## 🔍 EDA Highlights
EDA dilakukan untuk:
- Mengecek distribusi rating & sentiment  
- Menganalisis panjang review (karakter & kata)  
- Memvalidasi kualitas teks  
- Mendeteksi imbalance dataset  

Detail EDA terdapat pada notebook: `notebook/EDA & Preprocessing.ipynb`

---

## 🧹 Text Preprocessing
Preprocessing minimal dilakukan untuk menjaga kualitas input bagi model Transformer:
- Remove URLs  
- Remove punctuation  
- Remove extra whitespace  
- Lowercase  
- Remove emoji  

Hasilnya disimpan di `data/processed/`.

---

## 🤖 Modeling
Model yang digunakan:
- **Hugging Face Transformer** (`AutoModelForSequenceClassification`)
- Pretrained model:  
  `w11wo/indonesian-roberta-base-sentiment-classifier` *(or XLM-R / mBERT)*

Langkah-langkah modeling:
1. Train-test split  
2. Tokenization  
3. Fine-tuning model  
4. Evaluation (Accuracy, F1-score)  
5. Save model  

Notebook: `notebooks/Train Test Split & Modeling & Evaluation.ipynb`
(Terdapat versi .py karena versi .ipynb terdapat error di previewnya)

---

## 📈 Evaluation
Model dievaluasi menggunakan dataset test dengan hasil sebagai berikut:
- Accuracy: 85.8%
- F1-Score: 0.84
- Eval Loss: 0.3975

---

## 🧪 Requirements
Daftar dependency tersedia di: `requirements.txt`

## 📬 Contact
Untuk pertanyaan lebih lanjut:  
**NASYWA RAIHANAH**  
Email: *nasywaraihanah@gmail.com*

