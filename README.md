# CRADLE Bench

**Content Warning:** This project addresses sensitive topics including suicide ideation, self-harm, rape, domestic violence, and child abuse.

---

## Hugging Face Resources

### CRADLE Bench

[![Dataset](https://img.shields.io/badge/🤗%20Dataset-Cradle--Bench-FFD21E?labelColor=FFD21E&color=FFD21E&style=flat)](https://huggingface.co/datasets/SungJoo/Cradle-Bench)

Fine-tuned models (trained on consensus vs. unanimous subsets of the ensemble-labeled training corpus):

[![Model](https://img.shields.io/badge/🤗%20Model-LLaMA--3.3--70B%20·%20unanimous-4B91F1?style=flat)](https://huggingface.co/SungJoo/llama3.3-70b-CRADLE-unanimous)
[![Model](https://img.shields.io/badge/🤗%20Model-LLaMA--3.3--70B%20·%20consensus-7FB3F5?style=flat)](https://huggingface.co/SungJoo/llama3.3-70b-CRADLE-consensus)
[![Model](https://img.shields.io/badge/🤗%20Model-Qwen2.5--72B%20·%20unanimous-4B91F1?style=flat)](https://huggingface.co/SungJoo/Qwen2.5-72b-CRADLE-unanimous)
[![Model](https://img.shields.io/badge/🤗%20Model-Qwen2.5--72B%20·%20consensus-7FB3F5?style=flat)](https://huggingface.co/SungJoo/Qwen2.5-72b-CRADLE-consensus)

### CRADLE Dialogue

[![Dataset](https://img.shields.io/badge/🤗%20Dataset-Cradle--Dialogue-FFD21E?labelColor=FFD21E&color=FFD21E&style=flat)](https://huggingface.co/datasets/SungJoo/Cradle-Dialogue)
[![Model](https://img.shields.io/badge/🤗%20Model-Qwen3--32B%20·%202epoch-3DBE8A?style=flat)](https://huggingface.co/SungJoo/cradle-dialogue-qwen3-32b-2epoch)

---

## Dataset Overview

CRADLE BENCH is constructed from Reddit posts spanning crisis-related and general mental health subreddits, with annotations provided by licensed clinical psychologists and social workers. Each post is labeled with one or more of the following crisis categories, along with a temporal dimension (ongoing vs. past).

### Crisis Categories

| Category | Description |
|---|---|
| Suicide Ideation (Active) | Explicit intent, method, or preparation for suicide (C-SSRS levels 4–5) |
| Suicide Ideation (Passive) | Wish to die without a plan or active intent (C-SSRS levels 1–3) |
| Self-Harm | Intentional non-suicidal self-injury or urges, without suicidal intent |
| Domestic Violence | Abuse between intimate partners — physical, emotional, financial, or coercive |
| Rape | Non-consensual sexual acts involving penetration, by force or coercion |
| Sexual Harassment | Unwanted sexual advances or contact not involving penetration |
| Child Abuse / Endangerment | Physical/sexual abuse or neglect of minors by an adult |

### Data Statistics

| Split | Posts | Labels | Avg. labels/post |
|---|---|---|---|
| Dev | 420 | 443 | 1.05 |
| Test | 600 | 670 | 1.12 |
| Train (Consensus) | 4,181 | 4,649 | 1.11 |
| Train (Unanimous) | 3,058 | 3,257 | 1.07 |

The dev and test sets are manually annotated by clinicians. Training labels are automatically generated via majority-vote ensemble of GPT-5, Claude-4-Sonnet, and Gemini-2.5-Pro. The **Unanimous** subset includes only instances where all three models agree; the **Consensus** subset includes cases where at least two agree.

---

## Citation

If you use our data or models, please cite the EACL 2026 paper below.

**CRADLE Bench: A Clinician-Annotated Benchmark for Multi-Faceted Mental Health Crisis and Safety Risk Detection**  
Grace Byun, Rebecca Lipschutz, Sean T. Minton, Abigail Powers, Jinho D. Choi  
*EACL 2026 (Long Papers)* · [ACL Anthology](https://aclanthology.org/2026.eacl-long.73/)

<details>
<summary>BibTeX</summary>

```bibtex
@inproceedings{byun-etal-2026-cradle,
    title = "{CRADLE} Bench: A Clinician-Annotated Benchmark for Multi-Faceted Mental Health Crisis and Safety Risk Detection",
    author = "Byun, Grace  and
      Lipschutz, Rebecca  and
      Minton, Sean T.  and
      Powers, Abigail  and
      Choi, Jinho D.",
    editor = "Demberg, Vera  and
      Inui, Kentaro  and
      Marquez, Llu{\'i}s",
    booktitle = "Proceedings of the 19th Conference of the {E}uropean Chapter of the {A}ssociation for {C}omputational {L}inguistics (Volume 1: Long Papers)",
    month = mar,
    year = "2026",
    address = "Rabat, Morocco",
    publisher = "Association for Computational Linguistics",
    url = "https://aclanthology.org/2026.eacl-long.73/",
    doi = "10.18653/v1/2026.eacl-long.73",
    pages = "1572--1590",
    ISBN = "979-8-89176-380-7",
    abstract = "Detecting mental health crisis situations such as suicide ideation, rape, domestic violence, child abuse, and sexual harassment is a critical yet underexplored challenge for language models. When such situations arise during user{--}model interactions, models must reliably flag them, as failure to do so can have serious consequences. In this work, we introduce CRADLE BENCH, a benchmark for multi-faceted crisis detection. Unlike previous efforts that focus on a limited set of crisis types, our benchmark covers seven types defined in line with clinical standards and is the first to incorporate temporal labels. Our benchmark provides 600 clinician-annotated evaluation examples and 420 development examples, together with a training corpus of around 4K examples automatically labeled using a majority-vote ensemble of multiple language models, which significantly outperforms single-model annotation. We further fine-tune six crisis detection models on subsets defined by consensus and unanimous ensemble agreement, providing complementary models trained under different agreement criteria. Content warning: This paper discusses sensitive topics such as suicide ideation, self-harm, rape, domestic violence, and child abuse."
}
```
</details>

---
