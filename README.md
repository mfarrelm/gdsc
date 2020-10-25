## This repo is used for DSC member recruitment
# Tensorflow

Muhammad Farrel Mahendra
13317027

- Tensorflow is open-source Deep Learning library
- With Tensorflow, we can create DL model for production scale
- It is very easy to build Deep Learning model on Tensorflow with its high-level API which is Keras

for example this is the code to build DL model using Keras for MNIST Image Recognition (Sequential API)
```python
model = tf.keras.models.Sequential([
  tf.keras.layers.Flatten(input_shape=(28, 28, 1)),
  tf.keras.layers.Dense(128,activation='relu'),
  tf.keras.layers.Dense(10, activation='softmax')
])

model.compile(
    loss='sparse_categorical_crossentropy',
    optimizer=tf.keras.optimizers.Adam(0.001),
    metrics=['accuracy'],
)
```

-This is the same model using Functional API
```python
input_ = tf.keras.Input(input_shape = (28, 28, 1))
X = tf.keras.layers.Flatten(input_shape=(28, 28, 1))(input_)
X = tf.keras.layers.Dense(128,activation='relu')(X)
output = tf.keras.layers.Dense(10, activation='softmax')(X)
model = tf.keras.Model(inputs = input_, outputs = output)

model.compile(
    loss='sparse_categorical_crossentropy',
    optimizer=tf.keras.optimizers.Adam(0.001),
    metrics=['accuracy'],
)
```

- Basically Functional API give us more low-level than Sequential API so it gives more freedom to us to build model architecture (example skip-connection NN cannot be implemented with Sequential API)

- [This Project](https://github.com/Yustira/crowd-counting) is an example of using Tensorflow for Crowd Counting System. It is my team Google Bangkit Final Project
- Google also provides certification for Tensorflow. The detail about certification is [here](https://www.tensorflow.org/certificate). This is my [Tensorflow Developer Certificate](https://www.credential.net/f42e4d1a-9d1a-443c-8294-8ba25c2a4be2)


