AMD-Powered LLM Stack on AWS EC2 (g4ad.16xlarge)

This project demonstrates a high-performance, production-ready LLM deployment running on AWS EC2 g4ad.16xlarge, powered by AMD EPYC CPUs and Radeon Pro GPUs, optimized for running multiple local LLMs efficiently via Ollama and Open WebUI.

⚡ Instance Overview

The g4ad.16xlarge instance delivers a powerful balance of CPU, GPU, and memory:

CPU: AMD EPYC (2nd Gen “Rome” architecture)
vCPUs: 64
Memory: 256 GB RAM
GPU: 4× AMD Radeon Pro V520
Storage: High-throughput NVMe SSD

This architecture is designed for parallel workloads, high memory bandwidth, and GPU-accelerated inference, making it ideal for multi-model LLM environments.

🧠 Multi-LLM Execution (6 Models Concurrently)

This setup runs multiple LLMs simultaneously using Ollama:

llama3.2
qwen2.5
mistral
phi3
gemma3
lightweight models (1b–7b) for fast inference
Key Advantages:
Model switching without reload delays
Efficient memory utilization via dynamic loading
Parallel request handling across sessions
Optimized CPU-bound inference performance

Even without GPU acceleration, the EPYC CPU’s high core count allows:

fast token generation
low latency for smaller models
stable multi-user workloads via Open WebUI
🔥 Performance Characteristics
On AMD EPYC CPU:
Strong multi-threaded inference
Reliable for 1B–7B models
Scales well with concurrent users
Ideal for development, testing, and lightweight production
Bottlenecks:
Larger models (13B–14B+) introduce latency
CPU-only inference limits peak throughput
🚀 What Changes with AMD Instinct GPUs?

If this stack is deployed on AMD Instinct GPUs (MI210 / MI250 / MI300):

Massive Gains:
⚡ 10–50× faster inference
🧠 Efficient handling of large models (13B–70B+)
🔄 Real-time streaming across multiple users
📈 Higher throughput and lower latency
Why:
ROCm-accelerated tensor operations
High-bandwidth memory (HBM)
Parallel GPU compute optimized for AI workloads
🏗️ Architecture
Users (WebUI)
     ↓
Open WebUI (Docker, port 3000)
     ↓
Ollama Runtime
     ↓
LLM Models (CPU/GPU execution)
🌐 Key Outcomes
Fully self-hosted LLM stack on AMD infrastructure
Multi-model orchestration with dynamic loading
Scalable across CPU-only and GPU-accelerated environments
Accessible via browser (multi-session, multi-user)
Portable and reproducible via Docker
💡 Summary

The g4ad.16xlarge instance proves that AMD EPYC CPUs can effectively power a multi-LLM environment, delivering strong performance for small-to-medium models with excellent scalability.

When combined with AMD Instinct GPUs, this architecture transforms into a high-throughput AI inference platform, capable of serving large-scale LLM workloads with enterprise-grade performance.

One of the references:

https://www.amd.com/en/developer/resources/technical-articles/running-llms-locally-on-amd-gpus-with-ollama.html
