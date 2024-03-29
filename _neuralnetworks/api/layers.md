---
layout: document
title: "Layers"
grand_upper_section: index
upper_section: api/apitoc
previous_section: api/models
next_section: api/losses
---
Overview
-------

- **namespace**: Rindow\NeuralNetworks\Builder
- **classname**: Layers

Create new layer instances.

Create an instance of each layer by calling method with the same name as the class name of the layer.
Refer to the constructor of each layer for details.

Layers
------

- [**Dense**](dense.html): Regular densely-connected Neural Networks layer.
- [**Flatten**](flatten.html): Flattens the input.
- [**ExpandDims**](expanddims.html): ExpandDims the input.
- [**Concatenate**](concatenate.html): Concatenate the input.
- [**Embedding**](embedding.html): Embedding the input.
- [**RepeatVector**](repeatvector.html): RepeatVector the input.
- [**Gather**](gather.html): Gather the input.
- [**Max**](max.html): Max the input.
- [**Dropout**](dropout.html): Applies Dropout to the input.
- [**BatchNormalization**](batchnormalization.html): Normalize the previous activation function layer at each batch.
- [**Conv1D**](conv1d.html): 1D convolution layer.
- [**Conv2D**](conv2d.html): 2D convolution layer.
- [**Conv3D**](conv3d.html): 3D convolution layer.
- [**MaxPooling1D**](maxpooling1d.html): Max pooling operation for 1D temporal data.
- [**MaxPooling2D**](maxpooling2d.html): Max pooling operation for 2D temporal data.
- [**MaxPooling3D**](maxpooling3d.html): Max pooling operation for 3D temporal data.
- [**AveragePooling1D**](averagepooling1d.html): Average pooling operation for 1D temporal data.
- [**AveragePooling2D**](averagepooling2d.html): Average pooling operation for 2D temporal data.
- [**AveragePooling3D**](averagepooling3d.html): Average pooling operation for 3D temporal data.
- [**GlobalMaxPooling1D**](globalmaxpooling1d.html)
- [**GlobalMaxPooling2D**](globalmaxpooling2d.html)
- [**GlobalMaxPooling3D**](globalmaxpooling3d.html)
- [**GlobalAveragePooling1D**](globalaveragepooling1d.html)
- [**GlobalAveragePooling2D**](globalaveragepooling2d.html)
- [**GlobalAveragePooling3D**](globalaveragepooling3d.html)
- [**SimpleRNN**](simplernn.html)
- [**LSTM**](lstm.html)
- [**GRU**](gru.html)
- [**Attention**](attention.html)

Activations
-----------

- [**relu**](relu.html): Rectified Linear Unit activation function.
- [**sigmoid**](sigmoid.html): Sigmoid activation function.
- [**softmax**](softmax.html): Softmax activation function.
- [**tanh**](tanh.html): Tanh activation function.
- **linear**: Pass through

Examples
--------

```php
use Rindow\Math\Matrix\MatrixOperator;
use Rindow\NeuralNetworks\Builder\NeuralNetworks;

$mo = new MatrixOperator();
$nn = new NeuralNetworks($mo);
$model = $nn->models()->Sequential([
    $nn->layers()->Dense(128,input_shape:[10],activation='sigmoid');
    $nn->layers()->Dense(1);
    $nn->layers()->Activation('sigmoid');
]);
```
