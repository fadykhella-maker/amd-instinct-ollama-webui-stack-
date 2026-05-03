# 🚀 AMD LLM Stack on AWS (EPYC + Ollama + WebUI)

![AWS](https://img.shields.io/badge/AWS-EC2-orange)
![AMD](https://img.shields.io/badge/CPU-AMD%20EPYC-red)
![LLM](https://img.shields.io/badge/LLMs-6%20Models-blue)
![Docker](https://img.shields.io/badge/Docker-Enabled-blue)

---

## ⚡ Overview

This project runs a **multi-LLM stack (6 models)** on an  
**AWS EC2 g4ad.16xlarge instance**, powered by:

- 🧠 **AMD EPYC (Rome) CPU**
- 🎮 **AMD Radeon Pro V520 GPUs**
- 🐳 Docker-based deployment
- 🌐 Open WebUI for multi-user access

---

## 🖥️ Instance Specs

| Component | Details |
|----------|--------|
| Instance | `g4ad.16xlarge` |
| CPU | AMD EPYC (2nd Gen - Rome) |
| vCPUs | 64 |
| RAM | 256 GB |
| GPU | 4× AMD Radeon Pro V520 |

---

## 🧠 LLM Stack

Running via **Ollama**:

- `llama3.2`
- `qwen2.5`
- `mistral`
- `phi3`
- `gemma3`
- lightweight models (`1B–7B`) for speed

---

## ⚡ Performance

### ✅ CPU (EPYC)
- Fast inference for **1B–7B models**
- Handles **multiple users simultaneously**
- Stable and scalable

### ⚠️ Limitations
- Larger models (13B+) slower on CPU
- GPU not fully utilized in this setup

---

## 🚀 With AMD Instinct GPUs

Switching to **AMD Instinct (MI250 / MI300)** would:

- ⚡ 10–50× faster inference
- 🧠 Run large models (30B–70B+)
- 🔥 Real-time multi-user performance

---

## 🏗️ Architecture

Browser (Users)
↓
Open WebUI (Docker :3000)
↓
Ollama Runtime
↓
LLM Models (CPU / GPU)


---

## 🌐 Features

- Multi-model switching
- Multi-user WebUI access
- Dockerized deployment
- Fully self-hosted LLM stack

---

## 💡 Why This Matters

This setup proves:

👉 AMD EPYC can **reliably power multi-LLM workloads**  
👉 Scales from **CPU-only → GPU-accelerated AI**  
👉 Ready for real-world inference environments  

---

## 🔥 Next Steps

- Add AMD Instinct GPU support (ROCm)
- Benchmark token/sec performance
- Automate deployment (Terraform / scripts)

---
