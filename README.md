# pytorch-ssd-forked

This program is a merge of <https://github.com/qfgaohao/pytorch-ssd> and <https://github.com/dusty-nv/pytorch-ssd>.
It also includes other bug fixes.

## Installation

### Docker

<https://github.com/fa0311/ichigo-compose/blob/main/ichigo2025/mobilenet/Dockerfile>

### Manual

```sh
git clone https://github.com/fa0311/pytorch-ssd-forked
cd pytorch-ssd-forked
pip install -r requirements.txt

wget https://github.com/fa0311/pytorch-ssd-archive-model/releases/download/v0.0.1/mobilenet-v1-ssd-mp-0_675.pth -O models/mobilenet-v1-ssd-mp-0_675.pth
wget https://github.com/fa0311/pytorch-ssd-archive-model/releases/download/v0.0.1/mb2-ssd-lite-mp-0_686.pth -O models/mb2-ssd-lite-mp-0_686.pth
```

## Changes

- Enable `mb3-small-ssd-lite` and `mb3-large-ssd-lite` on Jetson
- Fix `requirements.txt`
- Support the latest `1.x` version of `numpy`
- Add argument `--no-augment` to disable data augmentation
- Add sample script `run_ssd_camera.py` for evaluating the model with a camera
- Add new scheduler, `--scheduler=cosine-warmup`
- Add learning rate tensorboard summary
- Add `eta_min` to `CosineAnnealingLR` scheduler

## Blog

<https://zenn.dev/fa0311/articles/fbad7b20aa1422>
