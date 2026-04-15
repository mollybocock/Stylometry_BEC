# Stylography_BEC
ipeline for BEC detection using the Enron corpus. XGBoost + Sentence Transformer + GPT-4o red team
# Stylometry_BEC
### Authorship Verification and Adversarial Attack Pipeline

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/mollybocock/Stylography_BEC/blob/main/v2BEC_Stylometric_Verifier_Clean%20(1).ipynb)

Stylometric authorship verification as a method of defense against Business Email Compromise (BEC). Trains on the Enron Email Corpus to build per-user writing fingerprints, then evaluates whether LLM-generated impersonation emails can evade detection.

## Models
- **XGBoost** — 638 stylometric features (138 handcrafted + 500 character n-grams)
- **Sentence Transformer** — all-MiniLM-L6-v2 + Logistic Regression head

## Red Team Pipeline
| Condition | Strategy | Result |
|---|---|---|
| B — Statistical Brief | GPT-4o prompted with plain-English feature summary | Low evasion |
| C — Few-Shot | GPT-4o prompted with 5 real emails as exemplars | Higher evasion |

## Files
- `v2BEC_Stylometric_Verifier_Clean.ipynb` — full annotated pipeline
- `bec_stylometric_verifier.py` — AI-generated code artifact (see Attribution)

## Attribution
`bec_stylometric_verifier.py` generated using Claude claude-sonnet-4-6 (Anthropic, 2025).

**Citation (IEEE):** M. Bocock, "BEC Stylometric Verifier," generated using Claude claude-sonnet-4-6 (Anthropic, 2025), CYBERSEC520, Duke University, 2025.

## Dataset
Enron Email Corpus — Klimt & Yang (2004), via [Kaggle](https://www.kaggle.com/datasets/wcukierski/enron-email-dataset)
