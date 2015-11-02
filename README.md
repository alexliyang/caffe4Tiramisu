# Caffe4Tiramisu

This projects extends Caffe for the Tiramisu project.
Mostly it modifies the feature extraction code for easier interaction.

## GoogLeNet models

The GoogLeNet models needed to run feature extraction are added in this repository. This is done for the sake of simplicity. Instructions on how to get them can be found on the original caffe site.

## Before running

Two parameters need to be modified in the prototxt file (e.g., ~/gits/caffe4Tiramisu/models/bvlc_googlenet/feat_extract.prototxt):
- the location of the mean_file shold be set to your local imagenet_mean.binaryproto (e.g., /your/local/path/caffe4Tiramisu/data/ilsvrc12)
- the file_list.txt, by default set to /tmp/file_list.txt. This two column file of the form "image_path.jpg 0" defines the image (SINGULAR) to process

## Calling feature extraction (example)
/your/local/path/caffe4Tiramisu/build/tools/extract_featuresTiramisu /your/local/path/caffe4Tiramisu/models/bvlc_googlenet/bvlc_googlenet.caffemodel /your/local/path/caffe4Tiramisu/models/bvlc_googlenet/feat_extract.prototxt inception_4e/output /tmp/tst 

the target directory (/tmp/tst in the example) must exist!
the layers to extract (inception_4e/output) can be multiple, separated by commas
only one image is process per call

# Caffe

[![Build Status](https://travis-ci.org/BVLC/caffe.svg?branch=master)](https://travis-ci.org/BVLC/caffe)
[![License](https://img.shields.io/badge/license-BSD-blue.svg)](LICENSE)

Caffe is a deep learning framework made with expression, speed, and modularity in mind.
It is developed by the Berkeley Vision and Learning Center ([BVLC](http://bvlc.eecs.berkeley.edu)) and community contributors.

Check out the [project site](http://caffe.berkeleyvision.org) for all the details like

- [DIY Deep Learning for Vision with Caffe](https://docs.google.com/presentation/d/1UeKXVgRvvxg9OUdh_UiC5G71UMscNPlvArsWER41PsU/edit#slide=id.p)
- [Tutorial Documentation](http://caffe.berkeleyvision.org/tutorial/)
- [BVLC reference models](http://caffe.berkeleyvision.org/model_zoo.html) and the [community model zoo](https://github.com/BVLC/caffe/wiki/Model-Zoo)
- [Installation instructions](http://caffe.berkeleyvision.org/installation.html)

and step-by-step examples.

[![Join the chat at https://gitter.im/BVLC/caffe](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/BVLC/caffe?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

Please join the [caffe-users group](https://groups.google.com/forum/#!forum/caffe-users) or [gitter chat](https://gitter.im/BVLC/caffe) to ask questions and talk about methods and models.
Framework development discussions and thorough bug reports are collected on [Issues](https://github.com/BVLC/caffe/issues).

Happy brewing!

## License and Citation

Caffe is released under the [BSD 2-Clause license](https://github.com/BVLC/caffe/blob/master/LICENSE).
The BVLC reference models are released for unrestricted use.

Please cite Caffe in your publications if it helps your research:

    @article{jia2014caffe,
      Author = {Jia, Yangqing and Shelhamer, Evan and Donahue, Jeff and Karayev, Sergey and Long, Jonathan and Girshick, Ross and Guadarrama, Sergio and Darrell, Trevor},
      Journal = {arXiv preprint arXiv:1408.5093},
      Title = {Caffe: Convolutional Architecture for Fast Feature Embedding},
      Year = {2014}
    }
