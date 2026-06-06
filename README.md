<div align="center">

# MaskAlign
### Mask-Guided Multi-Granularity Contrastive Learning for Fine-Grained Vision–Language Alignment

[![arXiv](https://img.shields.io/badge/arXiv-Paper-red)](https://arxiv.org/abs/xxxx.xxxxx)
[![ModelScope Model](https://img.shields.io/badge/🤗%20Model-Collection-purple)](https://modelscope.cn/models/Chenjg02/MaskAlign-Base)
[![ModelScope Data](https://img.shields.io/badge/📦%20Dataset-Collection-purple)](https://modelscope.cn/datasets/Chenjg02/MG-Data)
[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](./LICENSE)

**Jiangeng Chen**, **Hongtao Yu**, **Pandeng Li**, **Chen-Wei Xie**, **Yuxin Peng**, **Xiu-Shen Wei**

</div>

---

## 📑 Table of Contents
- [Highlights](#-highlights)
- [News](#-news)
- [Installation](#-installation)
- [Data Preparation](#-data-preparation)
- [Training & Evaluation](#-training--evaluation)
- [License](#-license)
- [Citation](#-citation)
- [Related Projects](#-related-projects)

---

## 🔥 Highlights
- 🔥 **Pixel-Level Multi-Granularity Supervision** — Fine-grained alignment at pixel level across multiple granularities.
- 🔥 **Intra-Granularity Alignment** — Cross-modal contrastive learning within each granularity layer.
- 🔥 **Mask Feature Aggregation Strategy** — Aggregating region features via learnable mask tokens for more precise vision–language matching.

---

## 📰 News
| Date | Event |
|------|-------|
| **2026/06/15** | 🚀 [Paper](https://arxiv.org/abs/2403.15378), [model](https://modelscope.cn/models/Chenjg02/MaskAlign-Base), and [MG-Data](https://modelscope.cn/datasets/Chenjg02/MG-Data) released! |

---

## ⚙️ Installation

```shell
git clone https://github.com/Chenjg02/MaskAlign.git
conda create -n maskalign python=3.10 -y
conda activate maskalign
cd FG-CLIP && pip install -e .
```

---

## 📦 Data Preparation

### Training Data
| Dataset | Description | Link |
|---------|-------------|------|
| MG-Data | Multi-granularity training dataset | [Download](https://modelscope.cn/datasets/Chenjg02/MG-Data) |

### Evaluation Data

#### Holistic Image Understanding
| Dataset | Notes | Link |
|---------|-------|------|
| ShareGPT4V | Image captions (1246K) | [Download](https://huggingface.co/datasets/Lin-Chen/ShareGPT4V/blob/main/share-captioner_coco_lcs_sam_1246k_1107.json) |
| COCO Captions | Annotations → `data/coco/annotations/` | [Download](https://github.com/tylin/coco-caption) |
| COCO | Images → `data/coco/` | [Download](https://cocodataset.org/dataset) |
| DCI | → `data/densely_captioned_images/` | [Download](https://github.com/facebookresearch/DCI) |
| ImageNet-1K | Validation set → `data/IN1K_val/` | [Download](https://image-net.org/) |
| ImageNet-v2 | Matched-frequency format → `data/imagenetv2-matched-frequency-format-val/` | [Download](https://opendatalab.com/OpenDataLab/ImageNetV2/tree/main) |

---

## 🚀 Training & Evaluation

### Holistic Image Understanding Tasks
```bash
bash scripts/overall.sh
```

### Bbox / Mask Classification and Semantic Segmentation
Refer to [ClearCLIP](https://github.com/mc-lan/ClearCLIP) for detailed instructions.

---

## 📄 License

This project utilizes certain datasets and checkpoints that are subject to their respective original licenses. Users must comply with all terms and conditions of these original licenses.

The content of this project itself is licensed under the [Apache License 2.0](./LICENSE).

---

## 📖 Citation

If you find our work helpful for your research, please consider citing:

```bibtex
@article{chen2026maskalign,
  title   = {Mask-Guided Multi-Granularity Contrastive Learning for
             Fine-Grained Vision–Language Alignment},
  author  = {Jiangeng Chen and Hongtao Yu and Pandeng Li and
             Chen-Wei Xie and Yuxin Peng and Xiu-Shen Wei},
  journal = {arXiv preprint arXiv:2026.},
  year    = {2026}
}
```

---

## 🙏 Related Projects

This work builds upon the incredible open-source contributions of:

- [FG-CLIP](https://github.com/360CVGroup/FG-CLIP.git)
- [ClearCLIP](https://github.com/mc-lan/ClearCLIP.git)
- [LLaVA](https://github.com/haotian-liu/LLaVA.git)
- [LongCLIP](https://github.com/beichenzbc/Long-CLIP.git)
- [SigLIP](https://github.com/merveenoyan/siglip.git)

---

<div align="center">
  <sub>Made with ❤️ by the MaskAlign team</sub>
</div>
