### RC-SAM:Refine the Contour of complex objects with SAM and Boundary Guidance

#### Pipeline

![pipeline](C:\Users\Administrator-PC\OneDrive\桌面\FormattingGuidelines-IJCAI-23\pipeline.png)

#### Environment

Python 3.8

CUDA 11.7

PyTorch 1.13.1

TorchVision 0.14.1

#### Train

python -m torch.distributed.launch --nproc_per_node=<num_gpus> train.py --checkpoint <your checkpoint path> --model-type <model_type> --output <your output path>

#### Evaluation

python -m torch.distributed.launch --nproc_per_node=<num_gpus> train.py --checkpoint <your checkpoint path> --model-type <model_type> --output <your output path> --eval --restore-model <your training_checkpoint path>

#### **Visualization**

![Vis1](C:\Users\Administrator-PC\OneDrive\桌面\FormattingGuidelines-IJCAI-23\Vis1.png)

Visual comparison with **nine state-of-the-art COD methods**. EC-SAM demonstrates superior accuracy in delineating the boundaries of camouflaged objects.

![cam](C:\Users\Administrator-PC\OneDrive\桌面\FormattingGuidelines-IJCAI-23\cam.jpg)

#### Results on DIS，COIFT and ThinObject

![image-20240105112644171](C:\Users\Administrator-PC\AppData\Roaming\Typora\typora-user-images\image-20240105112644171.png)

#### Results on CODs

![image-20240105112749688](C:\Users\Administrator-PC\AppData\Roaming\Typora\typora-user-images\image-20240105112749688.png)

