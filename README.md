
# Multimodal AI POC with Agentic Orchestration

##  Overview
This is a proof-of-concept (POC) demo showcasing multimodal AI capabilities (text → image, audio, video) with agentic orchestration.

- **Input:** A text prompt  
- **Planner:** Flan-T5-small generates a structured JSON plan  
- **Orchestration:** The agent interprets the plan and calls tools  
- **Tools:**
  - Image → Stable Diffusion (`runwayml/stable-diffusion-v1-5`)
  - Audio → gTTS (text-to-speech)
  - Video → ffmpeg (combines image + audio)
- **Output:** `.png`, `.wav`, `.mp4` files  

Built fully with **open-source models** and **free infra** (Google Colab + Hugging Face).

## 🚀 How to Run (Colab)
1. Open `Multimodel_AI_.ipynb` in Google Colab.  
2. Runtime → Change runtime type → **GPU**.  
3. Install dependencies:
```bash
pip install -q diffusers[torch] transformers accelerate safetensors huggingface_hub ffmpeg-python gTTS
