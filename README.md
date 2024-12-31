# SegKAN

This is the code repository for the paper:
> **SegKAN: High-Resolution Medical Image Segmentation with Long-Distance Dependencies**
>
> [Shengbo Tan](https://github.com/goblin327), [Rundong Xue](https://github.com/Yizhao-dong),[Shipeng Luo], [Zeyu Zhang](https://steve-zeyu-zhang.github.io/), [Xinran Wang],[Lei Zhang],[ Daji Ergu],[Zhang Yi],[Yang Zhao] and [Ying Cai] 
> 
> **ICME 2025 [[[arXiv](https://arxiv.org/html/2412.19990v1)]]**

![](./pictures/dynamic_depth_result.gif)

If you use any content of this repo for your work, please cite the following our paper:
```
@article{***,
  title={SegKAN: High-Resolution Medical Image Segmentation with Long-Distance Dependencies},
  author={***},
  journal={***},
  year={2024}
}
```



## Introduction
Hepatic vessels in computed tomography scans often suffer from image fragmentation and noise interference, making it difficult to maintain vessel integrity and posing significant challenges for vessel segmentation. To address this issue, we propose an innovative model: SegKAN. First, we improve the conventional embedding module by adopting a novel convolutional network structure for image embedding, which smooths out image noise and prevents issues such as gradient explosion in subsequent stages. Next, we transform the spatial relationships between Patch blocks into temporal relationships to solve the problem of capturing positional relationships between Patch blocks in traditional Vision Transformer models. We conducted experiments on a Hepatic vessel dataset, and compared to the existing state-of-the-art model, the Dice score improved by 1.78\%. These results demonstrate that the proposed new structure effectively enhances the segmentation performance of high-resolution extended objects.
<div align="center">
<img src="pictures/overview.jpg" width="95%">

The core algorithm framework of SegKAN, illustrates the 3D image slices and encoding of 3D patches, as well as the learning of spatial relationships between 3D patches. The unique elongated structure of Hepatic blood vessels is highlighted in the top-left corner. The bottom-right image shows the impact of different split quantities on the model's segmentation results. The model performs best when the split quantity reaches 16, indicating that an appropriate number of splits can significantly improve segmentation performance in the SegKAN model.
</div>
