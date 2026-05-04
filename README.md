# CRADLE Bench

**Content Warning:** This project addresses sensitive topics including suicide ideation, self-harm, rape, domestic violence, and child abuse.

---


## Hugging Face Resources

### CRADLE Bench

Dataset and fine-tuned models for crisis detection in social media text (Reddit), covering seven crisis types with clinician annotations.

- Dataset: [SungJoo/Cradle-Bench](https://huggingface.co/datasets/SungJoo/Cradle-Bench)

Fine-tuned models (trained on consensus vs. unanimous subsets of the ensemble-labeled training corpus):

| Model | Training Set | Link |
|---|---|---|
| LLaMA-3.3-70B | Unanimous | [SungJoo/llama3.3-70b-CRADLE-unanimous](https://huggingface.co/SungJoo/llama3.3-70b-CRADLE-unanimous) |
| LLaMA-3.3-70B | Consensus | [SungJoo/llama3.3-70b-CRADLE-consensus](https://huggingface.co/SungJoo/llama3.3-70b-CRADLE-consensus) |
| Qwen2.5-72B | Unanimous | [SungJoo/Qwen2.5-72b-CRADLE-unanimous](https://huggingface.co/SungJoo/Qwen2.5-72b-CRADLE-unanimous) |
| Qwen2.5-72B | Consensus | [SungJoo/Qwen2.5-72b-CRADLE-consensus](https://huggingface.co/SungJoo/Qwen2.5-72b-CRADLE-consensus) |

### CRADLE Dialogue

Extension to multi-turn dialogue, with turn-level crisis detection annotations over synthetic clinical conversations.

- Dataset: [SungJoo/Cradle-Dialogue](https://huggingface.co/datasets/SungJoo/Cradle-Dialogue)
- Model: [SungJoo/cradle-dialogue-qwen3-32b-2epoch](https://huggingface.co/SungJoo/cradle-dialogue-qwen3-32b-2epoch)

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
