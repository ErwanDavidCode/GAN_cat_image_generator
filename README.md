# GAN_cat_image_generator
# Presentation
This Python project uses the PyTorch library to generate a unique cat image using GAN technology.

# Installation
- Install Python libraries
```sh
pip install -r requirements.txt
```
When the program is run locally, the following files are downloaded locally into the cloned directory : 
- dataset.zip
- dataset

They represent training and test data. They don't weigh much more than 50MB each. They can be easily deleted after training.

However, I recommend running this code in Google Colab to benefit from the computing power of their CPU and/or GPU. What's more, no files will be downloaded locally if the code is run on Google Colab.

# Algorithm configuration
The internal values used for the algorithm can be modified in the `TP_GAN_cat_image_generator` file.
To name just a few important ones:

```python
BATCH_SIZE = 64
EPOCHS = 20
lr=2e-4
LATENT_DIM = 100
```

|argument|type|description|
|-|-|-|
|BATCH_SIZE|int|The size of the data batch used for training|
|EPOCHS|int|The number of epochs used to train the model|
|lr|float|The learning rate of the optimizer (“Adam” here)|
|lr|int|The size of the latent vector from which the generator starts an image generation|


**Notes**: All values must be modified with full knowledge of the facts. No check is made on the consistency of values.
Execution time can be quite long (less than an hour on Colab for several weeks of epochs).

# Examples
Here are some images of cats generated with 20 EPOCHS:
![Screenshot of cat for a 20 EPOCHS training](/pictures/chats_20_epochs.png)