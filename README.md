# Neural Nets Are Reversible

This project is intended to validate the ideas presented in the paper 
"Deep Neural Networks are Surprisingly Reversible: A Baseline for Zero-Shot Inversion", 
where authors demonstrate that, contrary to popular belief, neural nets are not
the black boxes we thought they were. 

I am working on this project to validate my understanding of the paper on simpler
problems like MNIST.

# Results so far:
Generated images from an inverted network of 2 dense layer NN (inverse-of-network-mnist.ipynb)- top row has original, bottom row has generated images:

<img src="https://github.com/nayash/neural-nets-are-reversible/blob/95fa99ff05f7e8473a479c5889365dc7369fe0a6/assets/2-layer-Screenshot%20from%202021-11-21%2013-01-50.png" width=600 height=200/>

Generated images from a inverted network of convolutional NN (inverse-of-network-mnist-cnn.ipynb)- 3rd and 4th row show the output of target models CNN and input to inverted models CNN (should be very similar):

<img src="https://github.com/nayash/neural-nets-are-reversible/blob/master/assets/3layer_upsample_1conv_progressive_lecunNormalInit_selu_1637508546.0172439.png" width=700 height=400/>
** as you can see here, the outputs are not good, most probably because target model used 
for this experiment had MaxPool layer but inverted model didn't. Check samples from next experiment below!

Generated images from a reversed model which attempts to reverse a 4 layered (2 Conv2d + 2 Dense) network with no maxpool:

<img src="https://github.com/nayash/neural-nets-are-reversible/blob/master/assets/newProgressive_noPoolInTgt_4layer_nonProgsv_1638011097.0101573.png" width=700 height=400/>

<img src="https://github.com/nayash/neural-nets-are-reversible/blob/master/assets/newProgressive_noPoolInTgt_4layer_nonProgsv_1638020844.1275597.png" width=700 height=400/>

** This seems to be much more clearer than other conv based models. The above model was still improving, so generated image quality can still be improved.

TODO: train a model with MaxPool


