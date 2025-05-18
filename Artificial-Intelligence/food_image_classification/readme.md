# 🍕 Food Image Classification with Hugging Face Transformers

This project is a computer vision application that classifies food images using a pre-trained Vision Transformer model from Hugging Face 🤖. It was built for a hypothetical social media platform that wants to auto-tag food photos uploaded by users — making search, organization, and recommendations more powerful and delicious 🍲✨.

---

## 🚀 Project Goal

Build a **robust food classification system** that can:
- Automatically identify food categories in user-uploaded images
- Display top predictions with confidence scores
- Enhance user engagement on food-centric platforms (like Instagram for foodies)

---

## 🔍 How It Works

### 🛠️ Tech Stack
- [x] Python 🐍
- [x] Hugging Face `transformers` library 🤗
- [x] `nateraw/food` model (Vision Transformer trained on Food101)
- [x] `PIL` for image loading and formatting
- [x] `matplotlib` for optional visualization

---

### 📦 Model Used

[`nateraw/food`](https://huggingface.co/nateraw/food)  
A Vision Transformer (`ViT-base`) trained on [Food101](https://data.vision.ee.ethz.ch/cvl/datasets_extra/food-101/) — a dataset containing 101 food categories and 101k images.  
Achieves ~89% validation accuracy.

---

### 🧪 Sample Output

```python
[{'label': 'pizza', 'score': 0.874},
 {'label': 'cheeseburger', 'score': 0.064},
 {'label': 'risotto', 'score': 0.023}]
