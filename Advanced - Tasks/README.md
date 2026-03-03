# Language Model Deployment & Analysis - GPT-2

An Advanced task for the **ShadowFox AIML Internship** program. This project demonstrates loading, fine-tuning, evaluating, and visualising the GPT-2 language model using HuggingFace Transformers and PyTorch.

---

## Table of Contents

1. [Project Description](#project-description)
2. [Model Architecture](#model-architecture)
3. [Installation](#installation)
4. [Usage](#usage)
5. [Project Structure](#project-structure)
6. [Key Findings](#key-findings)
7. [Technologies](#technologies)
8. [References](#references)
9. [Author](#author)

---

## Project Description

This project covers the complete lifecycle of working with a pre-trained large language model:

- Loading and exploring GPT-2 from HuggingFace Hub
- Generating text with multiple decoding strategies (greedy, beam search, top-k, top-p, temperature scaling)
- Fine-tuning GPT-2 on the WikiText-2 dataset
- Evaluating the model using perplexity and BLEU score
- Visualising attention weights and token probability distributions

---

## Model Architecture

| Property           | Value                         |
|--------------------|-------------------------------|
| Model              | GPT-2 (small)                 |
| Layers             | 12 transformer blocks         |
| Hidden size        | 768                           |
| Attention heads    | 12                            |
| Parameters         | ~117 M                        |
| Context window     | 1 024 tokens                  |
| Architecture type  | Transformer-based, autoregressive |

---

## Installation

```bash
pip install -r requirements.txt
```

---

## Usage

### Jupyter / Google Colab

1. Open `Language_Model_GPT2.ipynb` in Jupyter Lab, Jupyter Notebook, or upload it to [Google Colab](https://colab.research.google.com/).
2. Run all cells from top to bottom (`Runtime → Run all` in Colab).
3. A GPU runtime is recommended for the fine-tuning section but not required.

---

## Project Structure

```
Advanced - Tasks/
├── README.md                   # This file
├── requirements.txt            # Python dependencies
└── Language_Model_GPT2.ipynb   # Main Jupyter notebook
```

---

## Key Findings

> _Results below are placeholder values; actual numbers will appear after running the notebook._

| Metric                      | Base GPT-2 | Fine-tuned GPT-2 |
|-----------------------------|-----------|-----------------|
| Perplexity (WikiText-2 val) | ~29.4     | ~24.1           |
| BLEU score (sample)         | 0.18      | 0.23            |
| Type-token ratio            | 0.62      | 0.67            |

**Decoding strategy comparison (qualitative)**

| Strategy      | Diversity | Coherence |
|---------------|-----------|-----------|
| Greedy        | Low       | High      |
| Beam search   | Medium    | Very High |
| Top-k (k=50)  | High      | Medium    |
| Top-p (p=0.95)| High      | Medium    |
| Temperature   | Variable  | Variable  |

---

## Technologies

- **Python 3.9+**
- **PyTorch** – model training and inference
- **HuggingFace Transformers** – GPT-2 model and tokenizer
- **HuggingFace Datasets** – WikiText-2 dataset loading
- **NLTK** – BLEU score computation
- **Matplotlib / Seaborn** – visualisations
- **NumPy / Pandas** – numerical processing and result tables
- **scikit-learn** – supplementary ML utilities

---

## References

- Radford, A. et al. (2019). *Language Models are Unsupervised Multitask Learners*. OpenAI.  
  [https://cdn.openai.com/better-language-models/language_models_are_unsupervised_multitask_learners.pdf](https://cdn.openai.com/better-language-models/language_models_are_unsupervised_multitask_learners.pdf)
- HuggingFace Transformers documentation: [https://huggingface.co/docs/transformers](https://huggingface.co/docs/transformers)
- HuggingFace Datasets documentation: [https://huggingface.co/docs/datasets](https://huggingface.co/docs/datasets)

---

## Author

**ShadowFox AIML Intern**  
ShadowFox Internship Programme – Advanced Track
