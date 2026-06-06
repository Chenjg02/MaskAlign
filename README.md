<div align="center">
  
# MaskAlign
### Mask-Guided Multi-Granularity Contrastive Learning </br>for Fine-Grained Vision–Language Alignment

[![arXiv](https://img.shields.io/badge/arXiv-Paper-red?style=flat-square&logo=arxiv&logoColor=white)](https://arxiv.org/abs/xxxx.xxxxx)
[![ModelScope Model](https://img.shields.io/badge/🤗%20Model-Collection-purple?style=flat-square)](https://modelscope.cn/models/Chenjg02/MaskAlign-Base)
[![ModelScope Data](https://img.shields.io/badge/📦%20Dataset-Collection-purple?style=flat-square)](https://modelscope.cn/datasets/Chenjg02/MG-Data)
[![License](https://img.shields.io/badge/License-Apache%202.0-blue?style=flat-square)](./LICENSE)

<br>

*Jiangeng Chen* · *Hongtao Yu* · *Pandeng Li* · *Chen-Wei Xie* · *Yuxin Peng* · *Xiu-Shen Wei*

</div>

<br>

<p align="center">
  <img width="80%" src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=18&duration=3000&pause=1000&color=2EA44F&center=true&vCenter=true&width=600&lines=Pixel-Level+Multi-Granularity+Supervision;Intra-Granularity+Contrastive+Alignment;Mask+Feature+Aggregation+Strategy" alt="features">
</p>

---

## 📑 Table of Contents

<details open>
<summary><b>Click to expand</b></summary>

&nbsp;&nbsp;🔹 [Highlights](#-highlights)<br>
&nbsp;&nbsp;🔹 [News](#-news)<br>
&nbsp;&nbsp;🔹 [Installation](#-installation)<br>
&nbsp;&nbsp;🔹 [Data Preparation](#-data-preparation)<br>
&nbsp;&nbsp;🔹 [Training & Evaluation](#-training--evaluation)<br>
&nbsp;&nbsp;🔹 [License](#-license)<br>
&nbsp;&nbsp;🔹 [Citation](#-citation)<br>
&nbsp;&nbsp;🔹 [Related Projects](#-related-projects)

</details>

---

## 🔥 Highlights

<table>
<tr>
<td width="50%">

> **Pixel-Level Multi-Granularity Supervision**
>
> Fine-grained alignment at pixel level across multiple granularities, enabling precise region-level vision–language correspondence.

</td>
<td width="50%">

> **Intra-Granularity Alignment**
>
> Cross-modal contrastive learning within each granularity layer, ensuring consistent feature matching at every scale.

</td>
</tr>
<tr>
<td width="50%">

> **Mask Feature Aggregation Strategy**
>
> Aggregating region features via learnable mask tokens for more precise vision–language matching, surpassing global-pooling baselines.

</td>
<td width="50%">

> **Strong Open-Vocabulary Performance**
>
> Competitive results on holistic understanding, bbox/mask classification, and semantic segmentation benchmarks.

</td>
</tr>
</table>

---

## 📰 News

<table>
<tr>
<td align="center" width="120"><b>2026/06/15</b></td>
<td>
🚀 Paper, model, and dataset released!
&nbsp;
<a href="https://arxiv.org/abs/2403.15378"><img src="https://img.shields.io/badge/Paper-arXiv-red?style=flat-square&logo=arxiv"></a>
<a href="https://modelscope.cn/models/Chenjg02/MaskAlign-Base"><img src="https://img.shields.io/badge/Model-ModelScope-purple?style=flat-square"></a>
<a href="https://modelscope.cn/datasets/Chenjg02/MG-Data"><img src="https://img.shields.io/badge/Data-ModelScope-purple?style=flat-square"></a>
</td>
</tr>
</table>

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

<details open>
<summary><b>🔹 Training Data</b></summary>
<br>

| Dataset | Description | Link |
|:--------|:------------|:-----|
| **MG-Data** | Multi-granularity training dataset with pixel-level annotations | [🤗 ModelScope](https://modelscope.cn/datasets/Chenjg02/MG-Data) |

</details>

<details open>
<summary><b>🔹 Evaluation Data — Holistic Image Understanding</b></summary>
<br>

| Dataset | Target Directory | Link |
|:--------|:-----------------|:-----|
| **ShareGPT4V** | — | [🤗 HuggingFace](https://huggingface.co/datasets/Lin-Chen/ShareGPT4V/blob/main/share-captioner_coco_lcs_sam_1246k_1107.json) |
| **COCO Captions** | `data/coco/annotations/` | [🌐 Official](https://github.com/tylin/coco-caption) |
| **COCO** (images) | `data/coco/` | [🌐 Official](https://cocodataset.org/dataset) |
| **DCI** | `data/densely_captioned_images/` | [🌐 Official](https://github.com/facebookresearch/DCI) |
| **ImageNet-1K** (val) | `data/IN1K_val/` | [🌐 Official](https://image-net.org/) |
| **ImageNet-v2** | `data/imagenetv2-matched-frequency-format-val/` | [🌐 OpenDataLab](https://opendatalab.com/OpenDataLab/ImageNetV2/tree/main) |

</details>

---

## 🚀 Training & Evaluation

### Holistic Image Understanding
```bash
bash scripts/overall.sh
```

### Bbox / Mask Classification & Semantic Segmentation

See [**ClearCLIP**](https://github.com/mc-lan/ClearCLIP) for full pipeline details.

---

## 📄 License

> [!IMPORTANT]
> This project uses datasets and checkpoints subject to their respective original licenses. Users must comply with all terms and conditions of those licenses.

The project itself is licensed under [Apache License 2.0](./LICENSE).

---

## 📖 Citation

If you find MaskAlign useful, please cite:

```bibtex
@article{chen2026maskalign,
        title={Mask-Guided Multi-Granularity Contrastive Learning for Fine-Grained Vision–Language Alignment},
        author={Jiangeng Chen, Hongtao Yu, Pandeng Li, Chen-Wei Xie, Yuxin Peng and Xiu-Shen Wei},
        journal={arXiv preprint arXiv:2026.},
        year={2026}
}
```

---

## 🙏 Related Projects

We stand on the shoulders of these excellent open-source works:

<p align="center">
  <a href="https://github.com/360CVGroup/FG-CLIP.git"><img src="https://img.shields.io/badge/FG--CLIP-181717?style=for-the-badge&logo=github&logoColor=white"></a>
  &nbsp;
  <a href="https://github.com/mc-lan/ClearCLIP.git"><img src="https://img.shields.io/badge/ClearCLIP-181717?style=for-the-badge&logo=github&logoColor=white"></a>
  &nbsp;
  <a href="https://github.com/haotian-liu/LLaVA.git"><img src="https://img.shields.io/badge/LLaVA-181717?style=for-the-badge&logo=github&logoColor=white"></a>
  &nbsp;
  <a href="https://github.com/beichenzbc/Long-CLIP.git"><img src="https://img.shields.io/badge/LongCLIP-181717?style=for-the-badge&logo=github&logoColor=white"></a>
  &nbsp;
  <a href="https://github.com/merveenoyan/siglip.git"><img src="https://img.shields.io/badge/SigLIP-181717?style=for-the-badge&logo=github&logoColor=white"></a>
</p>

<br>

<div align="center">
  <sub>© 2026 MaskAlign · All links preserved from original</sub>
</div>

