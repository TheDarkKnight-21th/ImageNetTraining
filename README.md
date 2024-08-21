# dataset download link
```
ImageNet homepage : https://www.image-net.org/
```

# Data Path
```
* 아래는 데이터 경로 입니다. 
```
dataset/
├─ imagenet21k/
│  └─ train
├─ imagenet21k_resized/
│  ├─ imagenet21k_small_classes 
│  ├─ imagenet21k_train  
│  └─ imagenet21k_val
└─ imagenet1k/
    └─ data
        ├─ train
        ├─ val
        └─ test
```

# Pretraining stage

```
# multi-gpu 

bash ./run_hyperpram_ddp.sh IN1k-PATH DATASET LR WARMUP_LR GPU_NUMBER THE_NUMBER_OF_GPU BATCHSIZE

default ex) bash ./run_hyperparam_ddp.sh /home/dataset/imagenet1k/data/train default 1e-3 1e-5 0,1,2,3,4,5,6,7 8 128
wds     ex) bash ./run_hyperparam_ddp.sh /home/dataset/imagenet-w21-wds wds/ 1e-3 1e-5 0,1,2,3,4,5,6,7 8 128
```
```
# sigle-gpu

bash ./run_hyperparam_single.sh IN21k-PATH DATASETLR WARMUP_LR GPU_NUMBER BATCHSIZE

default ex) bash ./run_hyperparam_single.sh /home/dataset/imagenet21k_train/train default  1e-3 1e-5 0 1024
wds     ex) bash ./run_hyperparam_single.sh /home/dataset/imagenet-w21-wds wds/  1e-3 1e-5 0 1024
```
