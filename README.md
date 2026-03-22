# Self-Verifying AI Tutors

**Reducing Hallucinations and Improving Reliability in Educational LLM Systems**

---

## 📌 Overview

This repository accompanies the research paper:

> **Self-Verifying AI Tutors: Reducing Hallucinations and Improving Educational Reliability through Verification Loops**

It provides a complete, reproducible framework for benchmarking and improving the reliability of AI-driven tutoring systems based on Large Language Models (LLMs).

The repository includes:
- 📊 Benchmark datasets for educational QA
- 📓 Google Colab notebooks (v1, v2, and Self-Verifying Tutor)
- 📈 Figures and tables used in the paper
- 🧪 Evaluation pipelines for hallucination and calibration
- 🧠 Student learning simulation

---

## 🚨 Motivation

While LLM-based tutors offer scalable and personalized learning, they suffer from:

- ❌ Hallucinations (incorrect but plausible answers)
- ⚠️ Overconfident errors
- 📉 Poor calibration of confidence
- 🎓 Negative impact on student learning

This project introduces a **Self-Verifying Tutor (SVT)** framework that integrates:

- Retrieval (RAG)
- Verification
- Self-correction loops

to significantly improve reliability and educational outcomes.

---

## 🧠 Key Contributions

- ✅ Novel **Self-Verification Score (SVS)** for evaluating tutor reliability
- 🔁 Self-verifying architecture with iterative correction
- 📊 Multi-metric benchmark:
  - Accuracy
  - Hallucination rate
  - Overconfident errors
  - Calibration (ECE)
- 🎓 Student learning simulation
- ⚖️ Comparative analysis of:
  - Naive tutor
  - Baseline tutor
  - RAG-only tutor
  - Self-verifying tutor

---

## 📂 Repository Structure

```
self-verifying-ai-tutors/
│
├── notebooks/
│   ├── ai_tutor_hallucination_benchmark.ipynb
│   ├── ai_tutor_hallucination_benchmark_v2.ipynb
│   └── self_verifying_tutor.ipynb
│
├── data/
│   ├── benchmark_dataset.csv
│   └── generated_results.csv
│
├── figures/
│   ├── accuracy_comparison.png
│   ├── hallucination_rates.png
│   ├── reliability_diagrams.png
│   └── svs_comparison.png
│
├── tables/
│   ├── model_comparison.csv
│   ├── calibration_bins.csv
│   └── student_impact.csv
│
└── README.md
```

---

## ⚙️ Installation

Clone the repository:

```bash
git clone https://github.com/hamamh66/self-verifying-ai-tutors.git
cd self-verifying-ai-tutors
```

Install dependencies:

```bash
pip install -r requirements.txt
```

---

## 🚀 Usage

### 1. Run Benchmark (Colab recommended)

Open in Google Colab:

- `ai_tutor_hallucination_benchmark.ipynb`
- `ai_tutor_hallucination_benchmark_v2.ipynb`
- `self_verifying_tutor.ipynb`

All notebooks:
- Mount Google Drive
- Save outputs automatically
- Generate figures and tables

---

### 2. Run with Real LLMs

Edit configuration:

```python
SIMULATION_MODE = False
```

Set API keys:

```python
OPENAI_API_KEY=...
GOOGLE_API_KEY=...
HF_TOKEN=...
```

---

### 3. Outputs

The notebooks generate:

- 📊 Figures (PNG)
- 📋 Tables (CSV)
- 📈 Evaluation metrics

Saved to:

```
MyDrive/Self_Verifying_Tutor_Benchmark/
```

---

## 📊 Evaluation Metrics

| Metric | Description |
|------|-------------|
| Accuracy | Correct answers |
| Hallucination Rate | Incorrect + high confidence |
| Overconfident Error | High-risk errors |
| ECE | Calibration error |
| SVS | Self-Verification Score |

---

## 🧪 Self-Verifying Tutor (SVT)

### Pipeline

```
Question → Retrieval → Answer → Verification → Correction → Final Answer
```

### Key Idea

Instead of trusting a single generation, the model:
1. Retrieves evidence
2. Verifies its own output
3. Corrects inconsistencies

---

## 📈 Main Results

| Model | Accuracy | SVS ↓ | Mastery ↑ |
|------|--------|------|-----------|
| Self-Verifying Tutor | **0.87** | **0.04** | **0.99** |
| RAG-only | 0.65 | 0.105 | 0.93 |
| Baseline | 0.60 | 0.175 | 0.86 |
| Naive | 0.55 | 0.33 | 0.66 |

---

## 🎓 Educational Impact

- 📉 Hallucination reduction: **80–90%**
- 📉 Misinformation reduction: **~10×**
- 📈 Student mastery improvement: **+13–33%**

---

## 🔬 Reproducibility

- Fully self-contained notebooks
- Synthetic + structured dataset
- Deterministic simulation mode
- Compatible with:
  - OpenAI
  - LLaMA
  - Mistral
  - Gemini

---

## 📄 Citation

```bibtex
@article{hamam2026svt,
  title={Self-Verifying AI Tutors: Reducing Hallucinations and Improving Educational Reliability},
  author={Hamam, Habib and others},
  journal={Computers and Education: Artificial Intelligence},
  year={2026}
}
```

---

## 🤝 Contributing

Contributions are welcome! Please open:
- issues
- pull requests
- suggestions for datasets or evaluation

---

## 📜 License

MIT License

---

## 👨‍🏫 Author

**Habib Hamam**  
Professor of Electrical and Computer Engineering  
Université de Moncton  

---

## ⭐ Acknowledgment

This work contributes to advancing **trustworthy AI in education**, aligning with global efforts toward safe and reliable AI systems.

---

## 🌍 Keywords

AI Tutors, LLM, Hallucination, Explainable AI, RAG, Education AI, Trustworthy AI
