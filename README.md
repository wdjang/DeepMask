# DeepMask
A Keras implementation of DeepMask based on NIPS 2015 paper [Learning to Segment Object Candidates](https://arxiv.org/abs/1506.06204).

## Requirements
ANACONDA、Keras、OpenCV3、mscoco

Here is the instructions to install them all:
* Download [ANACONDA](https://www.continuum.io/downloads) and then install it, I suggest you to install the Python 3.6 version.
* Install [Keras](https://keras.io) by the following steps:
  
  `sudo pip install -U --pre pip setuptools wheel`
  
  `sudo pip install -U --pre numpy scipy matplotlib scikit-learn scikit-image`
  
  `sudo pip install -U --pre tensorflow`
  
     >If your computer supports CUDA, you could install tensorflow-gpu by 
     
     >`sudo pip install -U --pre tensorflow-gpu`
     
     > Make sure you have installed [CUDA](https://developer.nvidia.com/cuda-downloads) and [cuDNN](https://developer.nvidia.com/cudnn) first.
  
  `sudo pip install -U --pre keras`

* Install [OpenCV3](http://opencv.org) by the following steps:

  `brew tap homebrew/science`
  
  `brew install opencv3 --with-python3 --without-python --without-numpy`
  
  `cd ~/anaconda/lib/python3.6/site-packages/`
  
  `ln -s /usr/local/Cellar/opencv3/3.2.0/lib/python3.6/site-packages/cv2.cpython-36m-darwin.so cv2.so`
  
  If your computer system aren't macOS Sierra, you should download [OpenCV3.2.0](https://github.com/opencv/opencv/archive/3.2.0.zip) 
  and then install it from source.
  
  Make sure the compile setting 'with-python3' is on, you could do that by using [cmake-gui](https://cmake.org).
  
  When you have installed OpenCV3, make sure the cv2.so is in '~/anaconda/lib/python3.6/site-packages/'.

* Install [MS COCO API](https://github.com/pdollar/coco) by the following steps:
  
  Download [coco](https://codeload.github.com/pdollar/coco/zip/master) and unzip it.
  
  `cd coco-master/PythonAPI/`
  
  `python setup.py build_ext install`

## Usage
Download the [mscoco datasets](http://mscoco.org/dataset/#download) first, you should only download '2014 Training images' and '2014 Train/Val object instances'.

Make a dir named 'coco', go inside and make two dir named 'images' and 'annotations'.

Unzip '2014 Training images' to dir 'images', '2014 Train/Val object instances' to dir 'annotations'.

`cd DeepMask\`

`python main.py`



