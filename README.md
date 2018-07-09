# Install CUDA-9.0 on Ubuntu 16.04

Ubuntu 16.04 



## Install CUDA Toolkit

Before install CUDA, remove existing ones. 

```
sudo apt-get purge cuda
sudo apt-get purge libcudnn6
sudo apt-get purge libcudnn6-dev
```

Download install files. 

```
wget https://github.com/AndersonJo/cuda-ubuntu/releases/download/9.0/cuda-repo-ubuntu1604_9.0.176-1_amd64.deb
wget https://github.com/AndersonJo/cuda-ubuntu/releases/download/9.0/libcudnn7-dev_7.0.5.15-1.cuda9.0_amd64.deb
wget https://github.com/AndersonJo/cuda-ubuntu/releases/download/9.0/libcudnn7_7.0.5.15-1.cuda9.0_amd64.deb
wget https://github.com/AndersonJo/cuda-ubuntu/releases/download/9.0/libnccl-dev_2.1.4-1.cuda9.0_amd64.deb
wget https://github.com/AndersonJo/cuda-ubuntu/releases/download/9.0/libnccl2_2.1.4-1.cuda9.0_amd64.deb
```

After downloading, install the deb files. 

```
sudo dpkg -i cuda-repo-ubuntu1604_9.0.176-1_amd64.deb
sudo dpkg -i libcudnn7_7.0.5.15-1+cuda9.0_amd64.deb
sudo dpkg -i libcudnn7-dev_7.0.5.15-1+cuda9.0_amd64.deb
sudo dpkg -i libnccl2_2.1.4-1+cuda9.0_amd64.deb
sudo dpkg -i libnccl-dev_2.1.4-1+cuda9.0_amd64.deb
sudo apt-get update
sudo apt-get install cuda=9.0.176-1
sudo apt-get install libcudnn7-dev
sudo apt-get install libnccl-dev
```

You need to hold upgrading CUDA Toolkit versions. 

```
sudo apt-mark hold libcudnn7 libcudnn7-dev
```

To later allow upgrades, you can remove the holds. 

```
sudo apt-mark unhold libcudnn7 libcudnn7-dev
```

# Installing TensorFlow

```
$ pip install tensorflow      # Python 2.7; CPU support (no GPU support)
$ pip3 install tensorflow     # Python 3.n; CPU support (no GPU support)
$ pip install tensorflow-gpu  # Python 2.7;  GPU support
$ pip3 install tensorflow-gpu # Python 3.n; GPU support 
```
