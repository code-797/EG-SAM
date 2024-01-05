## RC-SAM:Refine the Contour of complex objects with SAM and Boundary Guidance

### Pipeline

![pipeline](figs/pipeline.png)

### Environment

Python 3.8

CUDA 11.7

PyTorch 1.13.1

TorchVision 0.14.1

### Train

python -m torch.distributed.launch --nproc_per_node=<num_gpus> train.py --checkpoint <your checkpoint path> --model-type <model_type> --output <your output path>

### Evaluation

python -m torch.distributed.launch --nproc_per_node=<num_gpus> train.py --checkpoint <your checkpoint path> --model-type <model_type> --output <your output path> --eval --restore-model <your training_checkpoint path>

### Visualization

![Vis1](figs/Vis1.png)

Visual comparison with **nine state-of-the-art COD methods**. EC-SAM demonstrates superior accuracy in delineating the boundaries of camouflaged objects.

![cam](figs/cam.jpg)
![sort](figs/sort.png)

### Results on DIS，COIFT and ThinObject

![result1](figs/result1.jpg)

### Results on CODs

![result2](figs/result2.jpg)

