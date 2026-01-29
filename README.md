# Hi there, I'm Ivan Olivera 👋

### High-Performance Software Engineer | Low Latency & Distributed Systems

I am a Backend Engineer with 4 years of experience in critical financial systems, specializing in **High-Frequency Trading (HFT)** infrastructure, Cloud-Native Banking architectures, and **Zero-Allocation** system design.

My engineering focus is on pushing the boundaries of the JVM, optimizing for nanosecond-level latency, and architecting secure, cost-efficient distributed platforms.

---

### 🚀 Engineering Highlights & Featured Projects

#### 1. [CudaQuantEngine: HFT-Grade Option Pricer](https://github.com/ivanoliveraprofesional-code/cuda-quant-engine)
> **C++20 | CUDA 12.x | Compute-Bound Architecture**

A GPU-accelerated Monte Carlo pricing engine for path-dependent derivatives. Optimized to physical hardware limits using **Philox RNG** (Stateless) and Warp-Level Primitives to eliminate Global Memory traffic.

* **⚡ Throughput:** `138 Million paths/sec` on RTX 3050.
* **⏱️ Latency:** `7.22 ms` end-to-end (1M paths, 252 steps).
* **🧠 Key Tech:** Warp Shuffle (`__shfl_down_sync`), Constant Memory Broadcasting, Zero-Copy.

#### 2. [Ultra-Low Latency HFT Trading Engine](https://github.com/ivanoliveraprofesional-code/high-performance-zero-gc-logger)
> **Java 21 (Preview) | Project Panama | Zero-GC**

A proof-of-concept HFT Data Ingestion Engine utilizing **Mechanical Sympathy**. It simulates the full lifecycle from UDP Multicast capture to Off-Heap persistence with **zero garbage collection** on the critical path.

* **⚡ Throughput:** `16.3 Million msg/sec` (UDP -> RingBuffer -> Disk).
* **⏱️ Latency:** `< 600 ns` (Network Stack + App Logic).
* **🧠 Key Tech:** LMAX Disruptor Pattern, Kernel Bypass (Busy Spin), MemorySegments (FFM API).

#### 3. [FinOps Distributed Banking Platform](https://github.com/ivanoliveraprofesional-code/finops-bank-platform)
> **Cloud-Native | Kubernetes | Zero Trust Security**

A production-grade Tier-3 banking simulation focusing on Cost Optimization (FinOps) and Security. Bridges the gap between Software Development and Platform Engineering using a hybrid DB strategy.

* **☁️ Infrastructure:** AWS Emulation via **LocalStack** (S3, KMS, DynamoDB).
* **🛡️ Security:** **Istio Service Mesh** for mTLS & JWT Validation.
* **🧠 Key Tech:** Hexagonal Architecture, Terraform (IaC), GitOps.

---

### 🛠 Technology Stack

| Domain | Stack |
| :--- | :--- |
| **Low Latency & Systems** | Java 21 (Project Panama/Loom), C++20, CUDA, Rust |
| **Concurrency & Perf** | LMAX Disruptor, Agrona, Lock-Free Algos, JMH, SIMD/AVX |
| **Cloud & Architecture** | Kubernetes, AWS, Terraform, Istio, Kafka, LocalStack |

---

### 🔭 Current Focus

* **Micro-optimizations:** Exploring CPU affinity and kernel bypass (**Solarflare**) for Linux environments.
* **Systems Programming:** Porting critical paths to **Rust** for hybrid architectures.
