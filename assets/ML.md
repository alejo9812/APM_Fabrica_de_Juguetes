# Fundamentals of Tiny ML

Tiny ML features:
- Small size
- Low power consumption $<140$ $\mu W$
- Low cost


## Model compression techniques

- _Prunning_

Reduce the size of the network. Sometimes accuracy is lost.

![Alt text](toy1.png)

- _Quantization_

Reduce number of bits used by values.

![](attachments/Pasted%20image%2020240108123207.png)

- _Knowledge Distillation_

The most important information is teached.

![](attachments/Pasted%20image%2020240108123504.png)


---

_Tensorflow_ -> Software framework to write ML code

>[!Note]
>Smartphones use _Tensorflow Lite_


![](attachments/Pasted%20image%2020240108124153.png)

![](attachments/Pasted%20image%2020240108124338.png)


Sample TensorFlow code:

```Python
# Load in the TensorFlow library
import tensorflow as tf

# Define my custom Neural Network model
class MyModel(tf.keras.Model):
    def __init__(self):
        super(MyModel, self).__init__()
        # define Neural Network layer types
        self.conv = tf.keras.layers.Conv2D(32, 3, activation='relu')
        self.flatten = tf.keras.layers.Flatten()
        self.dense1 = tf.keras.layers.Dense(128, activation='relu')
        self.dense2 = tf.keras.layers.Dense(10)

	# Run my Neural Network model by evaluating each layer on my input data
    def call(self, x):
        x = self.conv(x)
        x = self.flatten(x)
        x = self.dense1(x)
        x = self.dense2(x)
        return x

# Create an instance of the model
model = MyModel()

```


---

![](attachments/Pasted%20image%2020240108140426.png)

Given:

```
X = [-1.0, 0.0, 1.0, 2.0, 3.0, 4.0]
Y = [-3.0, -1.0, 1.0, 3.0, 5.0, 7.0]
```

A guess is a function $F:X\to Y$

Error of each guess is quantified using root of mean of squares:

![](attachments/Pasted%20image%2020240108161246.png)

>[!Note]
>In this case we are using _mean squared error_ loss function.
>There are many other loss functions

Size of step of gray ball is _learning rate_ ($\%$).

Each step (_epoch_) is $g\cdot LR$ -> $g$ :  Gradient, $LR$ : Learning rate.

The process is repeated until the gradient is 0 (takes many steps) -> _Gradient descent.

Every point in the curve is a guess.

>[!Note]
>Recommended: $LR < 0.1$
>Increasing $LR$ will make it to converge faster, however, a too high $LR$ will make the loss to diverge

---

![](attachments/Pasted%20image%2020240108171533.png)

_Hidden layers_ -> Middle ones. Nor input or outputs.


![](attachments/Pasted%20image%2020240108173900.png)

Output = (Weight * Input) + Bias








