# 🤖 AI / ML Engineer Portfolio — Stephen Gashoka

> LLM pipelines, model training, and AI systems built for real-world deployment. Focused on African language models and accessibility — bringing AI to underserved communities in East Africa.

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![HuggingFace](https://img.shields.io/badge/HuggingFace-FFD21E?style=flat-square&logo=huggingface&logoColor=black)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)

---

## Projects

### 1. Multilingual Voice Agent for Public Services 🇰🇪
**Problem:** Millions of Kenyans cannot access government information digitally because services are only available in English.

**Solution:** A voice assistant serving Swahili, Luo, Kikuyu, and Somali speakers.

**Architecture:**
- Speech-to-text: **OpenAI Whisper** (multilingual, fine-tuned on Kenyan accent data)
- Translation layer: **NLLB (No Language Left Behind)** by Meta
- Knowledge retrieval: **RAG pipeline with LlamaIndex** over government FAQ corpus
- TTS output: **Coqui TTS** (supports Swahili synthesis)
- Delivery: **Twilio Voice** or WhatsApp Business API

**Why this matters:** This is a genuine unmet need — Kenya has 68 languages and English-only digital services exclude most rural citizens.

**Stack:** Python · Whisper · NLLB · LlamaIndex · LangChain · Coqui TTS · FastAPI · Twilio

---

### 2. African News Summarizer & Bias Detector
**Problem:** East African news consumers lack tools to identify media bias or access multilingual summaries.

**Architecture:**
- Fine-tuned **T5** on East African news corpus (sourced from Daily Nation, The Standard, NTV)
- Bias classification model trained on annotated political, regional, and tonal bias labels
- React frontend: paste URL → get summary + bias breakdown + counterpoint suggestions
- **Hugging Face Transformers + LangChain** for the inference pipeline

**Key ML decisions:**
- Used LoRA fine-tuning to adapt T5 efficiently on limited GPU budget
- Built a custom annotation schema for Kenyan political bias (regional + ethnic dimensions not present in Western bias datasets)

**Stack:** Python · PyTorch · HuggingFace Transformers · T5 · LangChain · React · FastAPI

---

### 3. Medical Imaging Assistant for Understaffed Clinics
**Problem:** Rural Kenyan clinics have X-ray machines but no radiologists to interpret results.

**Architecture:**
- Object detection: **YOLOv8** fine-tuned on NIH ChestX-ray14 + VinDr-CXR datasets
- Training pipeline with **fastai** for transfer learning
- Deployed via **Gradio** (mobile-friendly image upload interface)
- Generates PDF diagnostic summary reports

**Ethical framing:** This is a decision-support tool, not a replacement for clinicians. All outputs are clearly labelled as AI-assisted suggestions requiring clinical review.

**Stack:** Python · YOLOv8 · fastai · PyTorch · Gradio · ReportLab

---

## MLOps & deployment practices
- Model versioning with **MLflow**
- Notebook testing with **nbmake** in CI
- Model serving via **FastAPI + Docker**
- Experiment tracking on **Weights & Biases**

---

## Skills demonstrated
| Area | Technologies |
|---|---|
| LLMs & RAG | LangChain, LlamaIndex, OpenAI API, Hugging Face |
| Model training | PyTorch, fastai, LoRA fine-tuning |
| Speech/NLP | Whisper, NLLB, spaCy, T5 |
| Computer Vision | YOLOv8, OpenCV |
| MLOps | MLflow, W&B, nbmake, Docker |
| Serving | FastAPI, Gradio, Streamlit |

---

📧 stephengachoka57@gmail.com | 🌐 [stephengachoka.co.ke](https://stephengachoka.co.ke) | 📍 Nairobi, Kenya
