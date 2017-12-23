# Face Scoring - Score Face by CNN Model based on TensorFlow
 
## A little more details
 * http://blog.csdn.net/roguesir/article/details/77164578

## Dataset
* Download: http://www.hcii-lab.net/data/SCUT-FBP/EN/download.html

![Result Pic](https://github.com/roguesir/DL-project/blob/master/Face-Scoring/web_image.jpg)

After downloading, we need match the labels and images.

![Result Pic](https://github.com/roguesir/DL-project/blob/master/Face-Scoring/face_image.jpg)

``` 
python rename.py
```

## Run

There are three train scripts about the train model. 

* python3 train.py
* python3 train_alex.py
* python3 train_vgg.py

## Test

![Result Pic](https://github.com/roguesir/DL-project/blob/master/Face-Scoring/test_image.jpg)

## Model Downloading

I train three models with different architectures: one is with three convolutional layers and two fully connected layers; another is with five convolutional layers and three fully connected layers like AlexNet; the last one is with 13 convolutional layers and three fully connected layers like VGG-16.

### Download link:

First model: http://pan.baidu.com/s/1bp8gqfH

AlexNet model: http://pan.baidu.com/s/1mhM0Jkk

## Deploy

### Offcial Tutorial
https://www.tensorflow.org/serving/

### Install Bazel
```
$ wget https://github.com/bazelbuild/bazel/releases/download/0.9.0/bazel-0.9.0-installer-linux-x86_64.sh
$ chmod u+x bazel-0.9.0-installer-linux-x86_64.sh
$ ./bazel-0.9.0-installer-linux-x86_64.sh
```

### Install gRPC
```
$ pip install grpcio
```

### TensorFlow Serving Python API PIP package
```
$ pip install tensorflow-serving-api
```
### Installing the ModelServer
1. Add TensorFlow Serving distribution URI as a package source (one time setup)
```
echo "deb [arch=amd64] http://storage.googleapis.com/tensorflow-serving-apt stable tensorflow-model-server tensorflow-model-server-universal" | sudo tee /etc/apt/sources.list.d/tensorflow-serving.list

curl https://storage.googleapis.com/tensorflow-serving-apt/tensorflow-serving.release.pub.gpg | sudo apt-key add -

```
2. Install and update TensorFlow ModelServer

```
git clone --recurse-submodules https://github.com/tensorflow/serving
```











