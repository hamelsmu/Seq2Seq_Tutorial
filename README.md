[![GitHub license](https://img.shields.io/github/license/hamelsmu/Seq2Seq_Tutorial.svg)](https://github.com/hamelsmu/Seq2Seq_Tutorial/blob/master/LICENSE)

## Sequence-to-Sequence Tutorial with Github Issues Data
Code For Medium Article: ["How To Create Data Products That Are Magical Using Sequence-to-Sequence Models"](https://medium.com/@hamelhusain/how-to-create-data-products-that-are-magical-using-sequence-to-sequence-models-703f86a231f8)

## Installation

`pip install -r requirements.txt`

If you are using the AWS Deep Learning Ubuntu AMI, many of the required dependencies will already be installed,
so you only need to run:

```
source activate tensorflow_p36
pip install ktext annoy nltk pydot
```

See #4 below if you wish to run this tutorial using Docker.


## Resources:

1. [Tutorial Notebook](https://nbviewer.jupyter.org/github/hamelsmu/Seq2Seq_Tutorial/blob/master/notebooks/Tutorial.ipynb):  The Jupyter notebook that coincides with the Medium post.

2. [seq2seq_utils.py](./notebooks/seq2seq_utils.py):  convenience functions that are used in the tutorial notebook to make predictions.

3. [ktext](https://github.com/hamelsmu/ktext): this library is used in the tutorial to clean data.  This library can be installed with `pip`.  

4. [Nvidia Docker Container](https://hub.docker.com/r/hamelsmu/seq2seq_tutorial/): contains all libraries that are required to run the tutorial.  This container is built with Nvidia-Docker v1.0.  You can install Nvidia-Docker and run this container like so:


```
curl -s -L https://nvidia.github.io/nvidia-docker/gpgkey |   sudo apt-key add -
distribution=$(. /etc/os-release;echo $ID$VERSION_ID)
curl -s -L https://nvidia.github.io/nvidia-docker/$distribution/nvidia-docker.list |   sudo tee /etc/apt/sources.list.d/nvidia-docker.list
sudo apt-get update
sudo apt-get install nvidia-docker

sudo nvidia-docker run hamelsmu/seq2seq_tutorial

```

This should work with both Nvidia-Docker v1.0 and v2.0.