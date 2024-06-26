### Assignment: gan
#### Date: Deadline: Jun 28, 22:00
#### Points: 2 points
#### Tests: gan_tests
#### Examples: gan_examples

In this assignment you will implement a simple Generative Adversarion Network
for three datasets in the MNIST format. Your goal is to modify the
[gan.py](https://github.com/ufal/npfl138/tree/master/labs/13/gan.py)
template and implement a GAN.

After submitting the assignment to ReCodEx, you can experiment with the three
available datasets (`mnist`, `mnist-fashion`, and `mnist-cifarcars`) and
maybe try different latent variable dimensionality. The generated images are
available in TensorBoard logs, and the images generated by the reference
solution can be also seen in the Examples.

You can also continue with `dcgan` assignment.

#### Tests Start: gan_tests
_Note that your results may be slightly different, depending on your CPU type and whether you use a GPU._

1. `python3 gan.py --dataset=mnist --train_size=490 --epochs=5 --z_dim=2`
```
Epoch 1/5 discriminator_accuracy: 0.8389 - discriminator_loss: 0.3185 - generator_loss: 3.8554 - loss: 3.7265
Epoch 2/5 discriminator_accuracy: 1.0000 - discriminator_loss: 0.0163 - generator_loss: 5.5732 - loss: 5.3607
Epoch 3/5 discriminator_accuracy: 0.9991 - discriminator_loss: 0.0137 - generator_loss: 6.6932 - loss: 6.4308
Epoch 4/5 discriminator_accuracy: 0.9995 - discriminator_loss: 0.0130 - generator_loss: 8.6689 - loss: 8.4075
Epoch 5/5 discriminator_accuracy: 0.9980 - discriminator_loss: 0.0203 - generator_loss: 10.1508 - loss: 9.8099
```

2. `python3 gan.py --dataset=mnist --train_size=490 --epochs=5 --z_dim=100`
```
Epoch 1/5 discriminator_accuracy: 0.8422 - discriminator_loss: 0.3254 - generator_loss: 3.3758 - loss: 3.4330
Epoch 2/5 discriminator_accuracy: 1.0000 - discriminator_loss: 0.0297 - generator_loss: 4.7812 - loss: 4.6822
Epoch 3/5 discriminator_accuracy: 1.0000 - discriminator_loss: 0.0296 - generator_loss: 5.9973 - loss: 5.7049
Epoch 4/5 discriminator_accuracy: 0.9954 - discriminator_loss: 0.0590 - generator_loss: 5.9659 - loss: 5.9170
Epoch 5/5 discriminator_accuracy: 0.9879 - discriminator_loss: 0.0903 - generator_loss: 5.6847 - loss: 5.9416
```
#### Tests End:
#### Examples Start: gan_examples
_Note that your results may be slightly different, depending on your CPU type and whether you use a GPU._
- `python3 gan.py --dataset=mnist --z_dim=2`
![mnist samples with z_dim 2](https://ufal.mff.cuni.cz/~straka/courses/npfl138/2324/demos/gan_mnist_z2.png)
- `python3 gan.py --dataset=mnist --z_dim=100`
![mnist samples with z_dim 100](https://ufal.mff.cuni.cz/~straka/courses/npfl138/2324/demos/gan_mnist_z100.png)
- `python3 gan.py --dataset=mnist-fashion --z_dim=2`
![mnist-fasion samples with z_dim 2](https://ufal.mff.cuni.cz/~straka/courses/npfl138/2324/demos/gan_mnist-fashion_z2.png)
- `python3 gan.py --dataset=mnist-fashion --z_dim=100`
![mnist-fasion samples with z_dim 100](https://ufal.mff.cuni.cz/~straka/courses/npfl138/2324/demos/gan_mnist-fashion_z100.png)
- `python3 gan.py --dataset=mnist-cifarcars --z_dim=2`
![mnist-cifarcars samples with z_dim 2](https://ufal.mff.cuni.cz/~straka/courses/npfl138/2324/demos/gan_mnist-cifarcars_z2.png)
- `python3 gan.py --dataset=mnist-cifarcars --z_dim=100`
![mnist-cifarcars samples with z_dim 100](https://ufal.mff.cuni.cz/~straka/courses/npfl138/2324/demos/gan_mnist-cifarcars_z100.png)
#### Examples End:
