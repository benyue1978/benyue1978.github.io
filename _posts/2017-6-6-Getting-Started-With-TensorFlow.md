---
layout: post
title: Getting Started with TensorFlow
---
Reading through [this article](https://www.tensorflow.org/get_started/get_started). The most important concept is the Computational Graph. The TensorFlow programming basically consists two steps:
1. Build the computational graph
2. Run the computational graph

### Importing TensorFlow  
```
import tensorflow as tf
```

### Constant, placeholder and variable
```
node1 = tf.constant(3.0, tf.float32)
a = tf.placeholder(tf.float32)
b = tf.Variable([.3], tf.float32)
```

### tf session
```
sess = tf.Session()
sess.run(node1)
```

### print
```
print(node1)
print(sess.run(node1))
```
