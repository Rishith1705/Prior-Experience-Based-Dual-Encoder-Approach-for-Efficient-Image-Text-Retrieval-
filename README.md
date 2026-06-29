# 🌍 Prior-Experience-Based Unified Encoder Approach for Efficient Image-Text Retrieval

A deep learning project for **Remote Sensing Image-Text Retrieval (RSITR)** using a **single CLIP-based unified encoder**. The project simplifies traditional dual-encoder architectures by mapping both images and text into a shared embedding space for efficient cross-modal retrieval.

---

## 📖 Overview

Remote Sensing Image-Text Retrieval (RSITR) aims to retrieve the most relevant **text description** for a given remote sensing image and the most relevant **image** for a given text query.

Traditional RSITR models use **two separate encoders**:

- Swin Transformer → Image Encoder
- BERT → Text Encoder

This project proposes a **unified encoder architecture** using **CLIP (Contrastive Language–Image Pretraining)**, which processes both image and text within the same embedding space.

Using a single encoder:

- Simplifies the architecture
- Reduces computational complexity
- Improves retrieval efficiency
- Supports both Image-to-Text and Text-to-Image retrieval

---

# 🎯 Objectives

- Perform Image-to-Text Retrieval.
- Perform Text-to-Image Retrieval.
- Replace dual encoders with a unified CLIP encoder.
- Reduce model complexity.
- Improve retrieval efficiency.
- Utilize RemoteCLIP pretrained models for Remote Sensing images.

---

# 🏗 Proposed Architecture

```
                 Text Query
                      │
                      ▼
              CLIP Tokenizer
                      │
                      ▼
              Unified CLIP Encoder
                      │
                      │
Image ──► Image Processor ──► Unified CLIP Encoder
                      │
                      ▼
            Shared Embedding Space
                      │
              Cosine Similarity
                      │
        ┌─────────────┴─────────────┐
        ▼                           ▼
 Image-to-Text Retrieval     Text-to-Image Retrieval
```

---

# 🚀 Features

- Remote Sensing Image Retrieval
- Image Caption Retrieval
- Text-to-Image Search
- Image-to-Text Search
- Unified CLIP Encoder
- RemoteCLIP pretrained weights
- Multiple CLIP Backbones
- Stable Diffusion Image Generation

---

# 📂 Repository Structure

```
Prior-Experience-Based-Unified-Encoder-Approach/
│
├── image_to_text.py          # Image → Text Retrieval
├── text_to_image.py          # Text → Image Generation
├── README.md
```

---

# 🛠 Technologies Used

- Python
- PyTorch
- HuggingFace Hub
- OpenCLIP
- RemoteCLIP
- Stable Diffusion
- Diffusers
- Transformers
- Google Colab

---

# 📚 Libraries Used

```python
torch
open_clip_torch
huggingface_hub
diffusers
transformers
Pillow
matplotlib
gradio
accelerate
```

---

# 🤖 Models Used

## RemoteCLIP

Pretrained models:

- RN50
- ViT-B-32
- ViT-L-14

RemoteCLIP is specifically trained for **Remote Sensing Vision-Language tasks**.

---

## Stable Diffusion

Model Used

```
dreamlike-art/dreamlike-diffusion-1.0
```

Used for:

- Text-to-Image Generation
- Satellite Image Synthesis

---

# ⚙ Workflow

## Image → Text Retrieval

```
Input Satellite Image
          │
          ▼
Image Preprocessing
          │
          ▼
RemoteCLIP Image Encoder
          │
          ▼
Image Embedding
          │
          ▼
Text Embedding
          │
          ▼
Cosine Similarity
          │
          ▼
Best Matching Caption
```

---

## Text → Image Generation

```
Text Prompt
      │
      ▼
Stable Diffusion Pipeline
      │
      ▼
Latent Diffusion
      │
      ▼
Generated Satellite Image
```

---

# 🔍 Methodology

### Image-to-Text

- Load RemoteCLIP pretrained model.
- Encode satellite image.
- Encode predefined text captions.
- Generate embeddings.
- Compute cosine similarity.
- Retrieve the most relevant caption.

---

### Text-to-Image

- Load Stable Diffusion model.
- Accept text prompt.
- Generate multiple satellite images.
- Display generated outputs.

---

# 📊 Example Text Queries

```
A busy airport with many aeroplanes.

Satellite view of Sydney.

Satellite view of Hohai University.

A building next to a lake.

Many people in a stadium.
```

---

# 📈 Output

### Image-to-Text

Input:

```
Airport Satellite Image
```

Output:

```
A busy airport with many aeroplanes.
```

---

### Text-to-Image

Input:

```
Satellite view of a busy airport with many aeroplanes.
```

Output:

```
Generated Remote Sensing Images
```

---

# 💡 Advantages

- Single Encoder Architecture
- Lower Computational Cost
- Shared Embedding Space
- Faster Retrieval
- Improved Efficiency
- Supports Bidirectional Retrieval
- Better Remote Sensing Understanding

---

# 📌 Applications

- Satellite Image Retrieval
- GIS Systems
- Urban Planning
- Disaster Monitoring
- Agriculture Monitoring
- Environmental Analysis
- Military Surveillance
- Smart Cities

---

# 🔮 Future Improvements

- Fine-tune RemoteCLIP on RSICD Dataset
- Integrate BLIP-2
- Use SigLIP
- Deploy using Streamlit
- Build REST API
- Support Natural Language Search
- Add Interactive Web Interface

---

# 📚 References

- CLIP: Contrastive Language–Image Pretraining
- RemoteCLIP
- Stable Diffusion
- HuggingFace Transformers
- OpenCLIP

---

# 👨‍💻 Author

**Rishith Reddy**

GitHub: https://github.com/Rishith1705

---

## ⭐ If you found this project useful, consider giving it a Star!
