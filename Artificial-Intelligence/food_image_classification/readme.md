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

### Sample input
**Input Image:**  
`Food Pictures/food_1.png`

![Sample Food Image](Food%20Pictures/food_1.png)

### 🧪 Sample Output

```python
[{'score': 0.992975115776062, 'label': 'spaghetti_bolognese'}, {'score': 0.0026719518937170506, 'label': 'spaghetti_carbonara'}, {'score': 0.0002339343773201108, 'label': 'ravioli'}, {'score': 0.00018298211216460913, 'label': 'pad_thai'}, {'score': 9.571584814693779e-05, 'label': 'ramen'}]
```


### Project structure
```
├── food_classification.py      # Main script
├── Food Pictures/              # Sample image(s)
├── README.md                   # This file
```


###  ▶️ How to Run
1. Install the dependencies

```
pip install transformers torch pillow matplotlib
```

2. Run the notebook
```
Jupyter Notebook --> notebook.ipynb
```

### 💡 Future Improvements

- Add drag-and-drop image upload UI with Gradio or Streamlit
- Fine-tune on Indian food (khichdi deserves better 😄)
- Deploy as a REST API or integrate into a mobile app



## 🤝 Let's Connect
Made with ❤️ by [Akash Kharita]

🔗 [![LinkedIn](https://img.shields.io/badge/LinkedIn-blue?style=flat&logo=linkedin)](https://www.linkedin.com/in/akash-k-609b12361/)

🐙 [![GitHub](https://img.shields.io/badge/GitHub-black?style=flat&logo=github)](https://github.com/Akashkharita)
