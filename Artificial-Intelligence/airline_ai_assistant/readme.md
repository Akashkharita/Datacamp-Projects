
## 📦 Dataset

The dataset used is the **Bitext Travel LLM Chatbot Training Dataset**.

### 🔑 Key Columns

- **`instruction`**: User query from the travel domain  
- **`category`**: High-level semantic intent (e.g., Booking, Info)  
- **`intent`**: Specific intent (e.g., BookFlight, BaggageStatus)  
- **`response`**: Ideal assistant reply  

---

## ⚡ Usage

### 1. Clone the repository

```bash
git clone https://github.com/Akashkharita/airline-chatbot-tinyllama.git
cd airline-chatbot-tinyllama
```

### 2. Launch the notebook

```bash
jupyter notebook notebook.ipynb
```

> ✅ Run all cells to fine-tune the model and test it on sample travel-related queries.

---

## 🛠️ Methods

- **🧠 Model**: [`TinyLlama/TinyLlama-1.1B-Chat`](https://huggingface.co/TinyLlama/TinyLlama-1.1B-Chat-v0.1)  
- **🧩 LoRA Fine-Tuning**: Used `peft.LoraConfig` for low-rank adaptation  
- **🔧 Supervised Training**: Leveraged `SFTTrainer` from Hugging Face TRL  
- **🧪 Testing**: Performed inference using `.generate()` with tokenized input  

---

## 🧪 Example Output

```text
Input: Query: I'm trying to book a flight

Output: Sure! Where are you flying from and what is your destination?
```

---

## 🔧 Key Configurations

### 💾 LoRA Configuration

```python
from peft import LoraConfig

lora_config = LoraConfig(    
    r=4,    
    lora_alpha=16,    
    lora_dropout=0.05,    
    bias="none",    
    task_type="CAUSAL_LM",    
    target_modules=["q_proj", "v_proj"]
)
```

### ⚙️ Training Configuration

```python
from trl import SFTConfig

sftConfig = SFTConfig(
    max_steps=10,
    per_device_train_batch_size=1,
    gradient_accumulation_steps=1,
    learning_rate=5e-4,
    max_grad_norm=0.3,
    dataset_text_field="instruction",
    output_dir="./outputs",
    packing=False
)
```

---

## 📊 Results

- ✅ Learned to understand diverse airline-related intents  
- ✍️ Generates accurate, helpful, human-like responses  
- 🔧 Successfully fine-tuned TinyLlama on a small, balanced subset of travel queries  

---

## 🤝 Contributing

Contributions and suggestions are welcome!  
Feel free to fork this repo and open a pull request.

---

## 📄 License

This project is licensed under the **MIT License**.

---

## 🙏 Acknowledgments

- 🤗 **Hugging Face** – For Transformers, TRL, PEFT, and Datasets libraries  
- ✈️ **Bitext** – For the travel chatbot dataset  
- 🦙 **TinyLlama** – For the compact, open-source language model  
- 🎓 **DataCamp** – For project structure and inspiration  

---

## 🤝 Let's Connect

Made with ❤️ by **Akash Kharita**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-blue?style=flat&logo=linkedin)](https://www.linkedin.com/in/akash-k-609b12361/)  
[![GitHub](https://img.shields.io/badge/GitHub-black?style=flat&logo=github)](https://github.com/Akashkharita)

