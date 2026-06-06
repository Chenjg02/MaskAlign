# [MaskAlign : Mask-Guided Multi-Granularity Contrastive Learning for Fine-Grained Vision–Language Alignment]()
</br>
Jiangeng Chen, Hongtao Yu, Pandeng Li, Chen-Wei Xie, Yuxin Peng, Xiu-Shen Wei
</br>
[![arXiv](https://img.shields.io/badge/arXiv.svg)](xxx)
[![ModelScope-model](https://img.shields.io/badge/Model-Collection🤖-purple.svg)](https://modelscope.cn/models/Chenjg02/MaskAlign-Base)
[![ModelScope-data](https://img.shields.io/badge/Benchmark-Collection🤖-purple.svg)](https://modelscope.cn/datasets/Chenjg02/MG-Data)

## 💡 Highlights
- 🔥 **Pixel-Level Multi-Granularity Supervision**
- 🔥 **Intra Granularity Alignment**
- 🔥 **Mask Feature Aggregation Strategy**

## 🔥 News
- 🚀 **[2026/06/15]** [Paper](https://arxiv.org/abs/2403.15378), [model](https://modelscope.cn/models/Chenjg02/MaskAlign-Base) and [MG-Data](https://modelscope.cn/datasets/Chenjg02/MG-Data) is released!

## 🛠️ Usage

### Installation
```shell
git clone https://github.com/Chenjg02/MaskAlign.git
conda create -n maskalign python=3.10 -y
conda activate maskalign
cd FG-CLIP && pip install -e .
```
### Training and Evaluation
Dataset for training:
Download [MG-Data](https://modelscope.cn/datasets/Chenjg02/MG-Data).

Dataset for evaluation(holistic image understanding tasks):

Download the [share-captioner_coco_lcs_sam_1246k_1107.json](https://huggingface.co/datasets/Lin-Chen/ShareGPT4V/blob/main/share-captioner_coco_lcs_sam_1246k_1107.json) from the following link 

Download the [CocoCaptions](https://github.com/tylin/coco-caption) from the following link nd put them into data/coco/annotations/

Download the [COCO](https://cocodataset.org/dataset) from the following link and put them into data/coco

Download the [DCI](https://github.com/facebookresearch/DCI) from the following links and put them into data/densely_captioned_images

Download the [ImageNet-1K](https://image-net.org/) from the following links and put them into data/IN1K_val

Download the [ImageNet-v2](https://opendatalab.com/OpenDataLab/ImageNetV2/tree/main) from the following links and put them into data/imagenetv2-matched-frequency-format-val

```
bash scripts/overall.sh
```
For Bbox/Mask Classification and Semantic Segmentation:

Refer to [ClearCLIP](https://github.com/mc-lan/ClearCLIP)

## License

This project utilizes certain datasets and checkpoints that are subject to their respective original licenses. Users must comply with all terms and conditions of these original licenses.
The content of this project itself is licensed under the [Apache license 2.0](./LICENSE).

## Citation
If you find our work helpful for your research, please consider giving a citation:
```
@article{chen2026maskalign,
        title={Mask-Guided Multi-Granularity Contrastive Learning for Fine-Grained Vision–Language Alignment},
        author={Jiangeng Chen, Hongtao Yu, Pandeng Li, Chen-Wei Xie, Yuxin Peng and Xiu-Shen Wei},
        journal={arXiv preprint arXiv:2026.},
        year={2026}
}
```
## Related Projects
This work wouldn't be possible without the incredible open-source code of these projects. Huge thanks!
- [FG-CLIP](https://github.com/360CVGroup/FG-CLIP.git)
- [ClearCLIP](https://github.com/mc-lan/ClearCLIP.git)
- [LLAVA](https://github.com/haotian-liu/LLaVA.git)
- [LongCLIP](https://github.com/beichenzbc/Long-CLIP.git)
- [SigLIP](https://github.com/merveenoyan/siglip.git)

