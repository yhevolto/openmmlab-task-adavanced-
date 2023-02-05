# openmmlab-task-adavanced-
cifar10
数据读入：mmclassification直接能识别cifar数据，所以直接将数据形式'imagenet'改成'CIRAR10'
注意：data = dict()中dict(type='LoadImageFromFile')要删掉，否则在读入时会跳出KeyError: 'img_prefix'这种错误。
但别失手将test=dict()或者val=dict()中的其他列误删掉，导致读入方式出问题，模型可能能跑起来，但是评估的acc top1很低（百分之十几）。

模型精度：2023-02-05 14:15:07,99
7 - mmcls - INFO - Epoch(val) [30][313] accuracy_top-1: 95.2000
