# Uzbek-Sentiment-Analysis
# 🇺🇿 O'zbek tili uchun Sentiment Analysis (XLM-RoBERTa)

Ushbu loyiha o'zbek tilidagi matnlarning kayfiyatini (ijobiy/salbiy) aniqlash uchun **XLM-RoBERTa** modelini qo'llaydi. mBERT modeliga qaraganda, XLM-R o'zbek tili uchun ancha yuqori aniqlikni ta'minlaydi.

---

## 🚀 Nega XLM-RoBERTa?
mBERT (Multilingual BERT) ko'p tillarni bilsa-da, **XLM-RoBERTa** o'zbek tili kabi kam resursli tillarda (low-resource languages) yaxshiroq natija ko'rsatadi. Bu model matndagi o'zbekcha so'zlarning nozik ma'no va kontekstlarini chuqurroq tushunadi.

---

## 🛠 Texnologiyalar
* ![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
* ![PyTorch](https://img.shields.io/badge/PyTorch-%23EE4C2C.svg?style=for-the-badge&logo=PyTorch&logoColor=white)
* ![HuggingFace](https://img.shields.io/badge/%F0%9F%A4%97-Hugging%20Face-yellow?style=for-the-badge)

---

## 📊 Dataset va Model
* **Model:** `xlm-roberta-base`
* **Dataset:** [kaffash/uzbek-sentiment](https://huggingface.co/datasets/kaffash/uzbek-sentiment) (10k+ qator)
* **Maqsad:** Mijozlar fikrini avtomatik klassifikatsiya qilish.

---

## 📈 Erishilgan natijalar
Modelni o'qitish davomida (Fine-tuning) quyidagi ko'rsatkichlar qayd etildi:
- **Test Accuracy:** 88%
- **Training Time:** NVIDIA T4 GPU yordamida ~15 daqiqa.

---

## 💻 Ishga tushirish (Inference)

```python
from transformers import pipeline

# Modelni yuklash
classifier = pipeline("sentiment-analysis", model="sizning_username/uzbek-xlmr-sentiment")

# Test qilib ko'rish
print(classifier("Sizlarning xizmat ko'rsatishingiz juda yomon!"))
# Natija: [{'label': 'LABEL_0', 'score': 0.98}]
👨‍💻 Muallif
Sizning Ismingiz - Javohirxon

⭐ Loyihani qo'llab-quvvatlash uchun Star bosishni unutmang!

