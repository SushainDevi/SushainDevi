<p align="center">
  <a href="https://github.com/SushainDevi">
    <img src="https://readme-typing-svg.demolab.com?font=Georgia&size=18&duration=2000&pause=100&multiline=true&width=600&height=80&lines=Sushain+Devi;Geometric+Interpretability+%26+Neuro-Symbolic+AI;NIKA+%7C+GWM-Pilot" alt="Typing SVG" />
  </a>
  <br/>
  <a href="https://sushaindevi.netlify.app/">
    <img src="https://img.shields.io/badge/Website-red?style=flat-square">
  </a>
  <a href="https://sushain-devi-resume.tiiny.site/">
    <img src="https://img.shields.io/badge/PDF-Resume-red?style=flat-square&logo=adobe">
  </a>
  <a href="https://www.linkedin.com/in/sushaindevi/">
    <img src="https://img.shields.io/badge/-LinkedIn-blue?style=flat-square&logo=linkedin">
  </a>
  <a href="mailto:devisushain@gmail.com">
    <img src="https://img.shields.io/badge/-Email-red?style=flat-square&logo=gmail&logoColor=white">
  </a>
  <a href="https://scholar.google.com/">
    <img src="https://img.shields.io/badge/-Scholar-4285F4?style=flat-square&logo=google-scholar&logoColor=white">
  </a>
</p>

## What I work on

I study **the geometry of reasoning in neural networks** — how truth, logic, and knowledge
are encoded as geometric structure inside large language models, and how that structure
can be measured, intervened upon, and engineered. This has two branches:

**NIKA** — an interpretability research program on how large language models represent
truth, where that representation breaks down, and how geometric interventions can steer
model behavior. Five iterations (V1–V5), 32B-scale models, published findings on truth
manifolds, dead zones, and surgical layer modification.

**GWM-Pilot** — a reversible Yang-Mills stack for geometric deep learning. An
architecture that composes Clifford multivector fields, a learned so(10) gauge
connection, symplectic integration, and reversible autograd — with a specific
architectural limit characterized under three independent control regimes.

Both projects share the same thesis: **the geometry is the mechanism**.

---

## NIKA — Neuro-Interpretive Knowledge Architecture

A geometric interpretability framework for large language models. Treats the residual
stream of a transformer as a principal fiber bundle over the sequence of layers, extracts
a low-dimensional truth subspace, transports it via connection matrices in so(K), and uses
the resulting geometry to detect holonomy, localize reasoning circuits, and steer
generation.

**Model:** Qwen-2.5-32B / DeepSeek-R1-Distill-Qwen-32B (D=5120, L=64)
**Scale:** ~30 hours of experimental runtime, 500 samples per condition, 4-bit NF4 quantization

### Key findings across the program

| Version | Contribution | Headline Result |
|---|---|---|
| **V1** | Neuro-symbolic critic-pivot architecture for epistemic agency | 100% pivot rate on toxic axioms; DeepSeek-R1 fails the "Odd Prime Fallacy" |
| **V2** | Causal steering of truth circuits with train/test validated probes | +18% overall steering improvement; 15D truth subspace (**99.7% compression**) |
| **V3** | Substrate Observer — real-time visualization of truth circuit formation | Truth compresses to **2–3 intrinsic dimensions**; Layer 16–32 "dead zone" identified |
| **V4** | Surgical layer intervention — domino effect through downstream layers | Layer 19 keystone: **+41.8%** truth improvement propagated through 17 layers |
| **V5** | Full parallel transport, holonomy detection, and domain manifold discovery | Universal truth direction at Layer 47: **86.5% cross-domain accuracy** across 12 scientific domains |

### Selected technical achievements

- **Truth bundle is orientable.** Holonomy determinant = 1.0000 across all 64 layers; 5 active canonical rotation planes in SO(10); mean geodesic distance 2.387 rad between consecutive layers.
- **Peak reasoning layer convergence.** Layer 47 identified independently by three separate methodologies (Block 1A probe accuracy, Block 1D calibration, Block 2D Fisher sweep).
- **Surgical causality.** Single-layer LoRA modification at Layer 19 propagates through the entire network; Layer 32 acts as grand integrator (peaks in 50% of prompts).
- **Behavioral emergence.** Level-1 "confused seeking" on false axioms ("Wait… Hmm… Let me think…") — first evidence of truth circuits inhibiting false confidence at the token level.
- **Distributed architecture.** Contradiction detection (Layers 19–22), integration zone (23–28), construction reasoning (29–32), universal input (16–18).

### Papers

- **NIKA V1** — *A Neuro-Symbolic Architecture for Induced Epistemic Agency and System-2 Reasoning in Quantized Large Language Models.* SSRN. [Link](https://ssrn.com/abstract=6100046)
- **NIKA V2** — *Causal Steering of Truth Circuits via Geometric Intervention in 32B Transformers.* TechRxiv.
- **NIKA V3** — *A Substrate Observer Study of Geometric Reasoning in DeepSeek-R1-Qwen-32B.* Zenodo. [Link](https://zenodo.org/records/18957019)
- **NIKA V4** — *The Keystone and the Domino: Mapping and Modifying the Distributed Architecture of Truth in Large Language Models.*
- **NIKA V5** — *Mapping the Geometry of Truth via Parallel Transport, Holonomy Detection, and Domain Manifold Discovery.*

---

## GWM-Pilot — Reversible Yang-Mills Stack

A geometric deep learning architecture where information flows through a learned
non-abelian gauge field. Composes Clifford multivector fields over a sparse voxel
grid, an so(10) connection, a symplectic leapfrog integrator, and a reversible
autograd stack with O(1) memory in depth.

**Repository:** [github.com/SushainDevi/GWM-Pilot](https://github.com/SushainDevi/GWM-Pilot)

### Verified properties

| Property | Measured |
|---|---|
| O(1) memory in depth | Peak grows **0.7%** from 2→8 layers |
| Exact reversibility | **1.3×10⁻⁸** reconstruction error, fp32, 8 layers |
| Symplectic energy conservation | **0.002%** drift over 200 steps |
| Gauge covariance (Wu-Yang) | Residual **< 10⁻⁷** |
| Full-stack gradcheck | Passes at float64, 8 layers |

### The finding

The A-update rule is **strictly local in voxel space** — no term allows one voxel's
A-field to influence a neighbor's. This defines a precise architectural envelope:
tasks requiring only per-voxel A-processing succeed (FDTD, 5.27× over trivial
baseline); tasks requiring A to carry information across space fail (torque transport
ratio = **0.0000**, bit-identical under every control regime).

The finding is established under three independent control regimes (naive, gradient-
patched, frozen-decoder) and documented with a full technical write-up, verification
protocols, configs, and trained model weights.

---

## Research direction

The next chapter of NIKA extends the surgical methodology from single-layer to full
16-layer modification of the dead zone — targeting the 0.73 truth emergence that
currently requires external steering.

The next version of GWM adds spatial coupling to the A-update (discrete Laplacian),
which re-derives every primitive and re-runs every downstream task. The current v1
release is frozen at the pre-coupling version so the architectural finding remains
reproducible.

Both directions are documented, verifiable, and open.

---

## Tools & Technologies

### Languages
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![C++](https://img.shields.io/badge/C++-00599C?style=flat-square&logo=c%2B%2B&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-336791?style=flat-square&logo=postgresql&logoColor=white)
![HTML](https://img.shields.io/badge/HTML-E34F26?style=flat-square&logo=html5&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)

### ML Frameworks
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![Hugging Face](https://img.shields.io/badge/Hugging%20Face-FFD500?style=flat-square&logo=huggingface&logoColor=white)
![Transformers](https://img.shields.io/badge/Transformers-FF6F00?style=flat-square)
![bitsandbytes](https://img.shields.io/badge/bitsandbytes-4--bit%20quantization-8E44AD?style=flat-square)

### Scientific Stack
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat-square&logo=numpy)
![SciPy](https://img.shields.io/badge/SciPy-8CAAE6?style=flat-square&logo=scipy&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikit-learn&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?style=flat-square)

### Research Focus Areas
![Geometric Interpretability](https://img.shields.io/badge/Geometric%20Interpretability-8E44AD?style=flat-square)
![Mechanistic Interpretability](https://img.shields.io/badge/Mechanistic%20Interpretability-007ACC?style=flat-square)
![Neuro-Symbolic AI](https://img.shields.io/badge/Neuro--Symbolic%20AI-007ACC?style=flat-square)
![Gauge Theory](https://img.shields.io/badge/Gauge%20Theory-D35400?style=flat-square)
![Clifford Algebra](https://img.shields.io/badge/Clifford%20Algebra-FF4081?style=flat-square)
![Symplectic Integration](https://img.shields.io/badge/Symplectic%20Integration-00BFFF?style=flat-square)
![LLM Reasoning](https://img.shields.io/badge/LLM%20Reasoning-8E44AD?style=flat-square)
![Reversible Networks](https://img.shields.io/badge/Reversible%20Networks-FF8C00?style=flat-square)

---

## Selected repositories

| Repository | Description |
|---|---|
| [**NIKA**](https://github.com/SushainDevi/NIKA) | Geometric interpretability of truth circuits in large language models (V1–V5) |
| [**GWM-Pilot**](https://github.com/SushainDevi/GWM-Pilot) | Reversible Yang-Mills stack for geometric deep learning — full pilot release |
| [**LLaMA-3-Like-Transformer**](https://github.com/SushainDevi/LLaMA-3-Like-Transformer-Model-Implementation) | Transformer implementation from scratch (RoPE, attention, FFN) |
| [**DocChat**](https://github.com/SushainDevi/DocChat) | Document summarization and retrieval chatbot |

---

## Education

**B.Tech Computer Science & Engineering** — MIT WPU, Pune
Independent researcher on geometric interpretability and neuro-symbolic architectures.

---

<music>
  <br>
  Currently coding & listening to:
  <br>
  <a href="https://open.spotify.com/playlist/6FuPRHeFZi0fvPTd2iKBrc" target="_blank">
      <img src="https://cdn.dribbble.com/users/441326/screenshots/3165191/media/45c2723efdf8be2140ff43913cbe8a3f.gif" alt="Spotify Logo" width="100">
  </a>
</music>
