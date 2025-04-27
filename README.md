# 🎨 Anime Style Image Generation Web Application

A full-stack Generative AI application that generates anime-style images from user prompts, fine-tuned using a curated Naruto dataset.  
The system uses Stable Diffusion with LoRA optimization for efficient fine-tuning and provides image generation through a backend API and an interactive frontend interface.  
Model performance is evaluated using CLIP Score for semantic alignment between prompts and generated images.

---

## 🚀 Project Objective

> To develop a full-stack text-to-image Generative AI application using Stable Diffusion, fine-tuned on a Naruto anime-style dataset with LoRA-based U-Net adaptation for efficiency.  
> The application enables stylized image generation based on user prompts and evaluates semantic relevance using CLIP Score.

---

## 🛠️ Tech Stack

| Component          | Technology Used                     |
|--------------------|--------------------------------------|
| Base Model         | Stable Diffusion v1.5                |
| Fine-Tuning        | LoRA (Low-Rank Adaptation) with PEFT |
| Backend            | FastAPI                              |
| Frontend           | Streamlit                            |
| Evaluation Metric  | CLIP Score (semantic alignment)     |
| Deployment Utility | pyngrok (for tunneling FastAPI server) |

---

## 📚 Step-by-Step Process

### 1. Data Preparation
- Utilized a Naruto anime-style dataset.
- Preprocessing steps included resizing images to 256x256 resolution and normalizing pixel values.
- Captions were tokenized using a CLIP tokenizer for text encoding.

### 2. Model Fine-Tuning
- Fine-tuned only the U-Net component of the Stable Diffusion model using LoRA for parameter-efficient training.
- The VAE encoder, VAE decoder, and text encoder remained frozen during training to maintain semantic integrity.

### 3. Backend Development
- Developed RESTful APIs using FastAPI to serve the base Stable Diffusion model and the fine-tuned model separately.
- Enabled easy switching between models for comparative inference.

### 4. Frontend Development
- Built an interactive user interface using Streamlit to collect user prompts and display generated images.
- Integrated API endpoints to allow users to select between the base and fine-tuned models for generation.

### 5. Evaluation
- Computed CLIP Scores for generated images relative to input prompts.
- Visualized semantic alignment through batch evaluations and comparative plots.

---

## 📈 System Architecture

```
Streamlit Frontend
        ↓
FastAPI Backend APIs
    ↙️             ↘️
Base Model     Fine-Tuned Model (LoRA)
(Stable Diffusion v1.5)
```

---

## 🎯 Future Improvements

- Enhance frontend capabilities to allow custom user-uploaded prompts and prompt history.
- Deploy APIs and frontend on cloud services for broader accessibility and scalability.

---

