# 🚀 English-to-Hindi Neural Machine Translation (NMT) with MarianMT

This project explores **fine-tuning a transformer-based LLM (MarianMT)** for **English-to-Hindi translation** using the **IIT Bombay Parallel Corpus (1.6M bilingual sentence pairs)**. The goal is to evaluate how fine-tuning improves translation fluency, contextual accuracy, and overall performance compared to off-the-shelf pre-trained models.

---

## 📌 Project Overview
- Implemented **Neural Machine Translation (NMT)** with the MarianMT (Helsinki-NLP/opus-mt-en-hi) model.  
- Fine-tuned the model on a **large-scale bilingual dataset** to improve domain-specific translation.  
- Applied **subword tokenization (SentencePiece/BPE)**, normalization, padding, and truncation for preprocessing.  
- Evaluated performance using **BLEU, ROUGE, and METEOR scores**.  
- Compared **pre-trained vs. fine-tuned models** to demonstrate the impact of fine-tuning on real-world translation tasks.  

---

## 🛠️ Methodology
1. **Dataset Preparation**  
   - Used the [IIT Bombay English-Hindi Parallel Corpus](https://www.cfilt.iitb.ac.in/iitb_parallel/).  
   - Preprocessed with tokenization, normalization, padding, and truncation.  

2. **Model Fine-Tuning**  
   - Base model: `Helsinki-NLP/opus-mt-en-hi` (MarianMT).  
   - Fine-tuned with Hugging Face Transformers using **transfer learning**.  
   - Hyperparameters:  
     - Batch size: `16`  
     - Learning rate: `3e-5`  
     - Weight decay: `0.01`  
     - Epochs: `2` (≈ 5-6 hrs on NVIDIA RTX A7000 GPU).  

3. **Evaluation**  
   - Metrics: **BLEU, ROUGE, METEOR** via Hugging Face `evaluate` library.  
   - Comparative study of baseline vs. fine-tuned model.  

---

## 📊 Results
- Fine-tuned model outperformed the baseline across all metrics.  
- Clear improvements in **fluency, contextual grounding, and handling of unseen data**.  

| Metric  | Pre-trained | Fine-tuned |
|---------|-------------|------------|
| BLEU    | Lower       | Higher ✅  |
| ROUGE   | Lower       | Higher ✅  |
| METEOR  | Lower       | Higher ✅  |

(*Exact values depend on test set evaluation*)  

---

## 🔑 Key Takeaways
- Fine-tuning significantly enhances the **adaptability of LLMs** to domain-specific tasks.  
- Subword tokenization improves handling of **rare words and morphology-rich languages** like Hindi.  
- Demonstrates the value of **transfer learning** in achieving better generalization with limited compute.  

---

## 📂 Project Structure
