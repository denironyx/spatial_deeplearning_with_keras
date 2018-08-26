# Deep Neural Network with keras-R (TensorFlow GPU backend): Satellite-Image Classification

This tutorial  will show how to implement [Deep Neural Network](https://en.wikipedia.org/wiki/Deep_learning) for [pixel based](https://gis.stackexchange.com/questions/237461/distinction-between-pixel-based-and-object-based-classification) [supervised classification ](https://articles.extension.org/pages/40214/whats-the-difference-between-a-supervised-and-unsupervised-image-classification) of [Sentinel-2 multispectral images](https://sentinel.esa.int/web/sentinel/missions/sentinel-2) using [keras](https://keras.rstudio.com/) package in [R](https://cloud.r-project.org/) under [Windows 10](https://www.microsoft.com/en-us/software-download/windows10).

[keras](https://keras.rstudio.com/) is a popular Python package for deep neural networks with multiple backends, including [TensorFlow](https://www.tensorflow.org/), [Microsoft Cognitive Toolkit (CNTK)](https://docs.microsoft.com/en-us/cognitive-toolkit/), and [Theano](http://deeplearning.net/software/theano/). Two R packages allow you  to use [Keras[(https://keras.rstudio.com/)] from R:  [keras](https://keras.rstudio.com/) and  [kerasR](https://github.com/statsmaths/kerasR). The keras package is able to provide a flexible and feature-rich API and can run both [CPU and GUP version of TensorFlow](https://www.tensorflow.org/install/install_windows) in both Windows and Linux.  If you want to run this tutorial with [GUP version of TensorFlow](https://www.tensorflow.org/install/install_windows) you need following prerequisites in your system:   


*[CUDA Toolkit v9.0](https://developer.nvidia.com/cuda-90-download-archive?target_os=Windows&target_arch=x86_64&target_version=10&target_type=exelocal): If you have an NVIDIAÂ® GPU in your system, you need to download and install [CUDA Toolkit  v9.0](https://developer.nvidia.com/cuda-90-download-archive?target_os=Windows&target_arch=x86_64&target_version=10&target_type=exelocal). Detail installation steps can be found [here](http://nvidia.custhelp.com/app/answers/detail/a_id/2040/~/identifying-the-graphics-card-model-and-device-id-in-a-pc).



Detail installation steps of Keras backend GPU or CUP version of Tensorflow can be found [here](https://tensorflow.rstudio.com/keras/reference/install_keras.html).

First, we will split "point_data" into a training set (75% of the data), a validation set (12%) and a test set (13%) data.The validation data set will be used to optimize the model parameters during training process.The model's performance will be tested with the test data set and then we will predict landuse clasess on grid data set. The point and grid data can be download as [rar](https://www.dropbox.com/s/l94zhzwjrc3lkk7/Point_Grid_Data.rar?dl=0), [7z](https://www.dropbox.com/s/77qk7raj48z0151/Point_Grid_Data.7z?dl=0) and [zip](https://www.dropbox.com/s/007vd9vayn60c2s/Point_Grid_Data.zip?dl=0) format. 
