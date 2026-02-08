# 🦁 Awal-LM (Version 1.0 - Izem)

**Awal-LM** is the first specialized Large Language Model (LLM) designed specifically for the **Tamazight language** using the **Tifinagh script**. 

The name **"Awal"** means *"Word"* or *"Speech"* in Tamazight, reflecting our goal to give the Amazigh language a powerful digital voice in the era of Artificial Intelligence.

---

## 🌟 Overview
- **Architecture:** Based on GPT-2.
- **Training Data:** Fine-tuned on 19,000+ sentences from the IRCAM corpus and Amazigh literature.
- **Version:** 1.0 (Codename: **Izem** - Lion)
- **Format:** Optimized for CPU inference (approx. 318MB).

## 🚀 Key Features
- **Creative Generation:** Capable of writing stories and folk tales in Tifinagh.
- **Grammatical Accuracy:** High understanding of Tamazight sentence structure.
- **Lightweight:** Runs smoothly on standard servers (4 Cores / 4GB RAM).

## 🛠️ Quick Start

To use **Awal-LM**, you will need the `transformers` library installed:

```python
from transformers import pipeline

# Load the model
pipe = pipeline("text-generation", model="rachidnichan/Awal-LM")

# Generate text
prompt = "ⴰⵣⵓⵍ"
result = pipe(prompt, max_new_tokens=50, temperature=0.7, repetition_penalty=1.2)

print(result[0]['generated_text'])
```

---

## 🌍 Vision
Awal-LM is an open-source project dedicated to preserving the Amazigh heritage. We believe that language is the heart of identity, and AI is the bridge to the future.

## 🤝 Contributing
We welcome contributions! Whether it's:
* Adding more high-quality training data.
* Improving the Tifinagh tokenizer.
* Building applications on top of Awal-LM.

## 📄 License
This project is licensed under the **MIT License**.

---
**Developed with ❤️ by [Rachid Nichan](https://huggingface.co/rachidnichan)**
```
