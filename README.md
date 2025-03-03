# Keypoint RCNN training code

Training:
```
python train.py \
    --dataset coco_kp \
    --data-path path/to/coco2017/dataset \
    --model keypointrcnn_resnet50_fpn \
    --data-path /path/to/coco \
    --epochs 46 \
    --lr-steps 36 43 \
    --aspect-ratio-group-factor 3 \
    --batch-size 4 \
    --lr 0.02 \
```

Your data should be in the COCO2017 dataset format.
```
coco2017/
├── annotations/
│   ├── person_keypoints_train2017.json
│   ├── person_keypoints_val2017.json
├── train2017/
│   ├── 000000000009.jpg
│   ├── 000000000025.jpg
│   └── ... # All training images
├── val2017/
│   ├── 000000000139.jpg
│   ├── 000000000285.jpg
│   └── ... # All validation images
└── test2017/  # Optional
```
