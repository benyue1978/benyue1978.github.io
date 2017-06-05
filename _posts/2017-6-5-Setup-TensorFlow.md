---
layout: post
title: Setup TensorFlow
---
I decided to learn the artificial intelligence using TensorFlow.  

I followed [the steps for Mac OS X](https://www.tensorflow.org/install/install_mac).  

Because my laptop is inside the corporate network, I always need to setup HTTP_PROXY and HTTPS_PROXY environment variables. And when I uses sudo, I need to use 'sudo -E' to preserve the environment variables in sudo.  

### Install virtualenv  
`$ sudo -E easy_install pip`  
`$ sudo pip install --upgrade virtualenv`

### Create a virutalenv  
`$ virtualenv --system-site-package ~/tensorflow` 

### Enter the virtual environment   
`$ source ~/tensorflow/bin/activate`

### Install TensorFlow   
I don't know if my GPU is fit for use, so I simply choose the non-GPU version of TensorFlow.     
`$ pip install --upgrade tensorflow` 

## Validate the Installation  
### Enter the virtual environment
`source ~/tensorflow/bin/activate`

### Ivnoke Python and run a short TensorFlow program
```
$python
>>> import tensorflow as tf
>>> hello = tf.constant('Hello, TensorFlow!')
>>> sess = tf.Session()
>>> print(sess.run(hello))
```
The result looks like   
`Hello, TensorFlow!`
