# ⵣ Awal-LM (Version 1.8 - Gemma-2)

<p align="center">
  <img src="awal-logo.png" width="250" alt="Awal-LM Logo">
</p>

**Awal-LM** is the first specialized Large Language Model (LLM) designed specifically for the **Tamazight language** using the **Tifinagh script**. 

The name **"Awal"** means *"Word"* or *"Speech"* in Tamazight, reflecting our goal to give the Amazigh language a powerful digital voice in the era of Artificial Intelligence.

---

## 🌟 Overview (Latest Update)
- **Architecture:** Based on **Google Gemma-2-2B** (Upgraded from GPT-2).
- **Fine-tuning:** Optimized using **Unsloth** for 2x faster inference and better memory efficiency.
- **Training Data:** Fine-tuned on a curated Tamazight dataset (IRCAM corpus, literature, and custom instructions).
- **Format:** Hugging Face LoRA Adapters (approx. 7.24GB).
- **Deployment:** Live at [awallm.com](https://awallm.com)

## 🚀 Key Features
- **Advanced Generation:** Powered by Gemma-2, providing much higher fluency and logical coherence in Tifinagh.
- **Instruct-Ready:** Can follow simple instructions and answer questions in Tamazight.
- **Cultural Identity:** Deeply integrated with Amazigh linguistic structures.
- **State-of-the-Art:** Uses the latest Transformer technology (2024/2025).

## 🛠️ Usage

To use the new **Awal-LM v1.8**, we recommend using the `unsloth` or `transformers` library:

```python
from transformers import AutoModelForCausalLM, AutoTokenizer

model_name = "rachidnichan/Awal-LM"

# Load the model and tokenizer
tokenizer = AutoTokenizer.from_pretrained(model_name)
model = AutoModelForCausalLM.from_pretrained(model_name)

# Generate text
prompt = "<start_of_turn>user\nⴰⵣⵓⵍ, ⵎⴰⵏⵉⴽ ⵜⴳⴰⴷ? <end_of_turn>\n<start_of_turn>model\n"
inputs = tokenizer(prompt, return_tensors="pt")
outputs = model.generate(**inputs, max_new_tokens=100, temperature=0.7)

print(tokenizer.decode(outputs[0], skip_special_tokens=True))
```

## 🌍 Vision
Awal-LM is an open-source project dedicated to preserving Amazigh heritage. By moving to Gemma-2, we are ensuring that Tamazight is represented in the latest generation of AI models.

## 🤝 Contributing
We welcome contributions to improve Awal-LM:
- **Dataset Expansion:** Help us gather more high-quality Tamazight texts and instructions.
- **RLHF:** Human feedback to improve the model's chat capabilities.
- **Applications:** Building mobile and web apps using the Awal-LM API.

## 📄 License
This project follows the Gemma License and is open for community research.

---
Developed with ❤️ by **Rachid Nichan**
