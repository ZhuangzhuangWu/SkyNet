This part of code was adapted from [offical release of SiamMask](https://github.com/foolwood/SiamMask). Please refer to this repo before use.

You may follow the **Environment setup** or run
```
$ conda env create -f environment.yml
$ conda activate sky
$ bash make.sh
```
```
$ conda env list

$ conda create -n sky python=3.6
$ source activate sky
$ pip install -r requirements.txt
$ pip install Cython

$ bash make.sh
```



to setup the environment.

```
- install
  $ pip install opencv-contrib-python
  $ pip install torch torchvision  
  $ pip install tensorboardX
  $ pip install torchsummary
  $ pip install utils

  (check version of CUDA)
  $ nvcc -V
  (install pytorch for cuda 7.5)
  $ conda install pytorch=0.4.1 cuda75 -c pytorch
  (install pytorch for NON-GPU)
  $ conda install pytorch torchvision cpuonly -c pytorch
```


Follow the original code to setup datasets  
[Youtube-VOS](https://youtube-vos.org/dataset/),
[install YouTube-VOS](https://github.com/maxpark/SkyNet/tree/master/Tracking/data/ytb_vos)

```

```

[COCO](http://cocodataset.org/#download),  
[ImageNet-DET](http://image-net.org/challenges/LSVRC/2015/),  
and [ImageNet-VID](http://image-net.org/challenges/LSVRC/2015/) and train/test on them.  

An example to train SkyNet on Youtube-VOS:
```
python tools/train_siammask.py --config=config_skynet.json -b 32 -j 16 --epochs 60 --log logs/log.txt --save_dir=snapshot_sky
```
To test on [GOT-10k](http://got-10k.aitestunion.com/) dataset, refer [test_got10k.py](./test_got10k.py).  


## License
Licensed under an MIT license.

