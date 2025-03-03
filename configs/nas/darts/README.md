# DARTS
> [DARTS: Differentiable Architecture Search](https://arxiv.org/abs/1806.09055)

## Abstract

This paper addresses the scalability challenge of architecture search by formulating the task in a differentiable manner. Unlike conventional approaches of applying evolution or reinforcement learning over a discrete and non-differentiable search space, our method is based on the continuous relaxation of the architecture representation, allowing efficient search of the architecture using gradient descent. Extensive experiments on CIFAR-10, ImageNet, Penn Treebank and WikiText-2 show that our algorithm excels in discovering high-performance convolutional architectures for image classification and recurrent architectures for language modeling, while being orders of magnitude faster than state-of-the-art non-differentiable techniques. Our implementation has been made publicly available to facilitate further research on efficient architecture search algorithms.

![pipeline](/docs/en/imgs/model_zoo/darts/pipeline.png)



## Results and models

### Supernet
Dataset|Unroll|Config|Download|
|:---------:|:---------:|:------:|:------:|
|Cifar10|True|[config](./darts_supernet_unroll_1xb64_cifar10.py) |[model](https://openmmlab-share.oss-cn-hangzhou.aliyuncs.com/mmrazor/v0.1/nas/darts/darts_supernet_unroll_1xb64_cifar10/darts_supernet_unroll_1xb64_cifar10_20211222-a923a040.pth?versionId=CAEQHxiBgID6mLuL7xciIDhjYzA2NGViNzY5ZDQxODk5MTY3ZjBiMGUyMGNlYzlk) &#124; [log](https://openmmlab-share.oss-cn-hangzhou.aliyuncs.com/mmrazor/v0.1/nas/darts/darts_supernet_unroll_1xb64_cifar10/darts_supernet_unroll_1xb64_cifar10_20211220_133123.log.json?versionId=CAEQHxiBgIDmmLuL7xciIGQwN2RlZWUwNmZkYjQwMzU4MGRiMTA3NGY4NTU5N2Nm)|


### Subnet

Dataset|Params(M)|Flops(G)|Top-1 Acc|Top-5 Acc|Subnet|Config|Download|Remarks|
|:---------:|:---------:|:---------:|:---------:|:---------:|:---------:|:------:|:------:|:------:|
|Cifar10|3.42 | 0.48 | 97.32 |99.94|[mutable](https://openmmlab-share.oss-cn-hangzhou.aliyuncs.com/mmrazor/v0.1/nas/darts/darts_subnetnet_1xb96_cifar10/darts_subnetnet_1xb96_cifar10_acc-97.32_20211222-e5727921_mutable_cfg.yaml?versionId=CAEQHxiBgMDn0ICL7xciIDAwNzUzZTU3ZjE4OTQ0MDg5YmZiMmYzYzExZTQ3YTRm)|[config](./darts_subnetnet_1xb96_cifar10.py)| [model](https://openmmlab-share.oss-cn-hangzhou.aliyuncs.com/mmrazor/v0.1/nas/darts/darts_subnetnet_1xb96_cifar10/darts_subnetnet_1xb96_cifar10_acc-97.32_20211222-e5727921.pth?versionId=CAEQHxiBgID20ICL7xciIDllOWZmNTliMzkwNzQ5YzdhODk2MzY1MWEyOTQ1Yjlk) &#124; [log](https://openmmlab-share.oss-cn-hangzhou.aliyuncs.com/mmrazor/v0.1/nas/darts/darts_subnetnet_1xb96_cifar10/darts_subnetnet_1xb96_cifar10_20211222-e5727921.log.json?versionId=CAEQHxiBgMDz0ICL7xciIGRhMjk0NDU0OTVhZjQwMDg4N2ZkMDAzZDM1ZWU4N2Ri)|MMRazor searched
|Cifar10|3.83 | 0.55 | 97.27 |99.98|[mutable](https://openmmlab-share.oss-cn-hangzhou.aliyuncs.com/mmrazor/v0.1/nas/darts/darts_subnetnet_1xb96_cifar10/darts_subnetnet_1xb96_cifar10_acc-97.27_20211222-17e42600_mutable_cfg.yaml?versionId=CAEQHxiBgICrnpmL7xciIGFmYzUxYjdmYWM1YzQ3N2I5NGU1MDE2ZjIxYmJhY2E0)|[config](./darts_subnetnet_1xb96_cifar10.py)| [model](https://openmmlab-share.oss-cn-hangzhou.aliyuncs.com/mmrazor/v0.1/nas/darts/darts_subnetnet_1xb96_cifar10/darts_subnetnet_1xb96_cifar10_acc-97.27_20211222-17e42600.pth?versionId=CAEQHxiBgIDQnpmL7xciIGQzOTRkMTViMDgzNzQ2MWI5MmUyNzIxZDk4OTUzZDgz) &#124; [log](https://openmmlab-share.oss-cn-hangzhou.aliyuncs.com/mmrazor/v0.1/nas/darts/darts_subnetnet_1xb96_cifar10/darts_subnetnet_1xb96_cifar10_20211222-17e42600.log.json?versionId=CAEQHxiBgMDPnpmL7xciIDViYTVlYTIyYmQ2OTQ1ZDZhNTNhMjVkODA2NDRlMTI1)|official


## Citation

```latex
@inproceedings{liu2018darts,
  title={DARTS: Differentiable Architecture Search},
  author={Liu, Hanxiao and Simonyan, Karen and Yang, Yiming},
  booktitle={International Conference on Learning Representations},
  year={2018}
}
```
