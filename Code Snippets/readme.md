

# ${Code \space Snippets}$

The Code Snippets are provided here. The code snippets for the ***three different models*** are provided. This folder must be opened when the person wants to have an 
***abstract knowledge*** of the project and the Models developed.

### ${First \space Model}$

```java
classes = 2    # Since we have two animals cats and dogs thus, the number of classes is two...

ConvolutionalNeuralNetwork = Sequential([
    Conv2D(filters=36, input_shape=(360, 360, 3), kernel_size=3, padding="same", activation="relu", name="conv1"),   
    # Input shape is (360, 360, 3)...
    MaxPooling2D((3, 3)),      # Pooling size is 3 x 3 matrix...
    Conv2D(filters=28, kernel_size=4, strides=(2,2), padding="same", activation="relu", name="conv2"),
    MaxPooling2D((3, 3)),      # Pooling size is 3 x 3 matrix...
    Conv2D(filters=24, kernel_size=3, strides=(1,1), padding="same", activation="relu", name="conv3"),
    MaxPooling2D((3, 3)),      # Pooling size is 3 x 3 matrix...
    Flatten(name="Flattening"),      # Flattening layer...
    Dense(128, activation="relu"),   # Output layer = 128 neurons, Input layer = 24 neurons...
    Dense(classes)                   # Output layer = 2 neurons, Input layer = 128 neurons...
])
```

    Accuracy Score = 0.5009
    Loss = 0.6931

----

### ${Second \space Model}$

```java
CNN1 = Sequential([
    Conv2D(filters=64, kernel_size=3, input_shape=(360, 360, 3), activation="relu", padding="same", name="conv1"),   
    # Input shape same as that of the resized Images...
    MaxPooling2D(pool_size=(2, 2)),    # Pooling size is 2 x 2 matrix...
    Conv2D(filters=32, kernel_size=3, activation="relu", padding="same", name="conv2"),
    MaxPooling2D(pool_size=(2, 2)),    # Pooling size is 2 x 2 matrix...
    Flatten(name="Flattening"),      # Flattening layer...
    Dense(32, activation="relu", name="dense1"),      # Output layer = 32 neurons, Input layer = 32 neurons...
    Dense(16, activation="relu", name="dense2"),      # Output layer = 16 neurons, Input layer = 32 neurons...
    Dense(2, activation="sigmoid", name="dense3")    # Output layer = 2 neurons, Input layer = 16 neurons...
])
```

    Accuracy Score = 0.9856
    Loss = 0.0791


----


### ${Third \space Model}$

```java
CNN2 = Sequential([
    Conv2D(filters=64, kernel_size=3, input_shape=(360, 360, 3), activation="relu", padding="same", name="conv1"),     
    # Input shape same as the resized Images...
    MaxPooling2D(pool_size=(2, 2)),     # Pooling size of 2 x 2 matrix...
    Conv2D(filters=48, kernel_size=3, activation="relu", padding="same", name="conv2"),
    MaxPooling2D(pool_size=(2, 2)),     # Pooling size of 2 x 2 matrix...
    Conv2D(filters=32, kernel_size=3, activation="relu", padding="same", name="conv3"),
    MaxPooling2D(pool_size=(2, 2)),     # Pooling size of 2 x 2 matrix...
    Flatten(name="Flattening"),      # Flattening layer = 32 neurons...
    Dense(32, activation="softmax", name="dense1"), # Output layer = 32 neurons, Input layer = 32 neurons...
    Dense(16, activation="relu", name="dense2"),    # Output layer = 16 neurons, Input layer = 32 neurons...
    Dense(8, activation="softmax", name="dense3"),  # Output layer = 8 neurons, Input layer = 16 neurons...
    Dense(2, activation="sigmoid", name="dense4")   # Output layer = 2 neurons, Input layer = 8 neurons...
])
```

    Accuracy Score = 0.4560
    Loss = 0.6936
    
----

## ${Ciphered \space By}$
***Vishu Kalier***





