# MooIn
무인점포 이상상황 대응 및 예방 웹 서비스 (2025-1 숙명여대 it공학전공 졸업프로젝트)
<br>
<img src='https://i.ifh.cc/yHzGZf.png' width=400>

> This project builds upon the **CLIP4Clip** architecture proposed in [ArrowLuo/CLIP4Clip](https://github.com/ArrowLuo/CLIP4Clip),  
and leverages pretrained weights from [Searchium-ai/clip4clip-webvid150k](https://huggingface.co/Searchium-ai/clip4clip-webvid150k).


### Base Architecture
- **Repository:** [ArrowLuo/CLIP4Clip](https://github.com/ArrowLuo/CLIP4Clip)  
- **Description:** Original PyTorch implementation of CLIP4Clip, a vision-language model for video–text retrieval.  
- **License:** MIT License  
- **Usage:** The architecture was used as a *baseline backbone* for our fine-tuning task.

### Pretrained Weights
- **Model:** [`Searchium-ai/clip4clip-webvid150k`](https://huggingface.co/Searchium-ai/clip4clip-webvid150k)  
- **Dataset:** WebVid-150k  
- **Purpose:** Used as initialization weights for domain-specific fine-tuning on in-store human action datasets (AI-Hub).  
- **Modifications:**  
  - Re-trained for 50 epochs with custom multimodal contrastive loss.  
  - Adapted to detect context-aware abnormal behaviors in unmanned store environments.

### Fine-tuning & Serving
- **H/w:** NVIDIA RTX 3060 (local environment)  
- **Frameworks:** PyTorch, FastAPI  
<br>

> ⚠️ **Note:**  
> This project does **not** claim authorship of the original CLIP4Clip architecture.  
> All rights of the base model remain with the respective authors.  
> Our contribution lies in adapting and fine-tuning the pretrained model for real-time multimodal anomaly detection in retail environments.

---

## 📄 Citation

If you use or build upon this work, please cite both the original CLIP4Clip and the Searchium-ai pretrained model:

```bibtex
@inproceedings{luo2021clip4clip,
  title={CLIP4Clip: An Empirical Study of CLIP for End to End Video Clip Retrieval},
  author={Luo, Hao and others},
  booktitle={ACM International Conference on Multimedia (MM)},
  year={2021}
}

@misc{searchiumai2023clip4clipwebvid150k,
  title={Searchium-ai/clip4clip-webvid150k},
  author={Searchium.ai},
  howpublished={\url{https://huggingface.co/Searchium-ai/clip4clip-webvid150k}},
  year={2023}
}
