# 📘 Automative Teaching Using RAG

This repository contains the evaluation notebook for our capstone project:  
**"Automatic Teaching via Vision Language Retrieval Augmented Generation."**

The goal of this work is to compare how different language models—specifically FLAN-T5, BART-Large, and a Hybrid Retriever—perform on academic question answering when grounded in course content.

🔗 **Run the notebook here →**  
[Colab Link: RAG_Evaluation_Colab.ipynb](https://colab.research.google.com/drive/1cllFgi0dszfPW1dU2tq8VZfhqFfSQgfC?pli=1)

---

## 🧪 Notebook Features

- Loads structured academic Q&A dataset  
- Generates context-aware answers using:
  - `google/flan-t5-base`
  - `facebook/bart-large`
  - Hybrid retrieval (non-generative baseline)  
- Computes and compares results across metrics:
  - **BLEU**, **ROUGE**, **F1 Score**
  - **METEOR**, **Cosine Similarity**, **CIDEr**, **Exact Match**

---

## 📊 Sample Output

| Model           | BLEU | ROUGE-1 | F1 Score | Cosine Sim |
|------------------|------|---------|----------|------------|
| FLAN-T5          | 0.000 | 0.0364 | 0.0476   | 0.2403     |
| BART-Large       | 0.0038| 0.2329 | 0.2105   | 0.4555     |
| Hybrid-Retriever | 0.0035| 0.1333 | 0.1017   | 0.3497     |

---

## 📦 Dependencies

You can run this notebook in Colab without any local setup.  
If running locally, install:

```bash
pip install pandas numpy torch sentence-transformers transformers nltk rouge-score scikit-learn
