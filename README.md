# AbsVis — Benchmarking How Humans and Vision-Language Models “See” Abstract Concepts in Images - EMNLP 2025 Long Paper (Main)

AbsVis is the dataset accompanying the EMNLP 2025 paper  
**"AbsVis — Benchmarking How Humans and Vision-Language Models 'See' Abstract Concepts in Images."**  
It examines how abstract concepts (e.g., *catastrophe, geography, strategy, mercy*) are visually represented in real images and how humans and vision–language models attribute concepts to those images.


🔗 **ACL Anthology:**  
https://aclanthology.org/2025.emnlp-main.417/

---

## Repository Structure

This repository currently includes:

### `metadata/nouns_list.csv`
This file contains the set of nouns used in the AbsVis dataset.  
Each noun is matched with its concreteness rating and assigned one of three categories based on the rating:

- **abstract**  
- **mid-range**  
- **concrete**

---

### `metadata/image_noun_mapping.csv`
This file lists every **image–noun pair** used in the AbsVis dataset.  
Each row contains a single image name and the noun associated with that image.

**Columns:**
- `image_name`  
- `noun`



---

### `metadata/noun_image_mapping.csv`
This file lists every **noun–image pair**, in the reverse direction of the previous file.  
Each row contains a noun and one of its associated image names.

**Columns:**
- `noun`  
- `image_name`

---

### `metadata/images_list.csv`
This file contains the complete set of **unique image names** used in the AbsVis dataset.  
Each row contains a single image ID.

**Columns:**
- `image_name`

---

### `annotations/` (human & model explanations)

This repository also includes the `annotations/` folder with raw explanations collected from humans and two vision–language models (Qwen, LLaVA). 

Provided annotation CSVs:
- `annotations/annotations_human_raw.csv` — human explanations (one row per human explanation)
- `annotations/annotations_qwen_raw.csv` — Qwen explanations (one row per model output)
- `annotations/annotations_llava_raw.csv` — LLaVA explanations (one row per model output)
- `annotations/annotations_all_raw.csv` — combined, with a `source` column

**Note on human explanation counts (quality control):**  
During annotation quality control we intentionally retained only substantive human explanations. One word responses were excluded from the final CSV in order to keep the dataset focused on meaningful concept–explanation pairs. As a result, a small number of images have fewer than 15 human explanations: 

Distribution of human explanation counts per image:
```
10: 1
13: 7
14: 28
15: 639
```

---



## 📚 Citation

If you use **AbsVis**, please cite:

```bibtex
@inproceedings{tater-etal-2025-absvis,
    title = "{A}bs{V}is {--} Benchmarking How Humans and Vision-Language Models ``See'' Abstract Concepts in Images",
    author = "Tater, Tarun  and
      Frassinelli, Diego  and
      Schulte im Walde, Sabine",
    booktitle = "Proceedings of the 2025 Conference on Empirical Methods in Natural Language Processing",
    month = nov,
    year = "2025",
    address = "Suzhou, China",
    publisher = "Association for Computational Linguistics",
    url = "https://aclanthology.org/2025.emnlp-main.417/",
    doi = "10.18653/v1/2025.emnlp-main.417",
    pages = "8271--8292",
    ISBN = "979-8-89176-332-6",
}