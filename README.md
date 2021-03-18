# Pruned-YOLO
Using model pruning method to obtain compact models, namely Pruned-YOLOv5, based on YOLOv5.

## NOTICE:

1.This project is based on [ultralytics/yolov5](https://github.com/ultralytics/yolov5). Place install it first. Then, use the model configuration file ( *coco_yolov5l.yaml* ) and network module definition file ( *common.py* ) provided here to replace the original corresponding files.

2.Referring to [SlimYOLOv3](https://github.com/PengyiZhang/SlimYOLOv3), we also use the subgradient method for sparsity training ( *sparsity.py* ). Besides, sparsity training and fine tuning are combined to simplify the pruning pipeline. We introduce the soft mask strategy and sparse factor cosine decay in the training process.

3.Use the *train.py* for sparsity train, pruning can be done directly without fine-tuning.

4.Please place *prune_channel_v5_weightingByKernel.py* and *prune_layer_v5_weightingByKernel.py* in the home directory ( */yolov5/* ). The former is used for channel pruning and the latter for layer pruning. The model pruning can be done by them.

5.These two steps are iteratively applied until the compression model reaches the budget target.
