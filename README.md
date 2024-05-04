## Brain Tumor Fighter: Using AI to Detect Brain Tumors

This project tackles a critical challenge in healthcare: detecting brain tumors. We've built a powerful AI model using a Convolutional Neural Network (CNN) in TensorFlow & Keras to identify brain tumors in MRI images.

**Why It Matters:**

Early detection of brain tumors is crucial for successful treatment. This project brings the power of AI to assist medical professionals in this fight.

**Unleashing the Power of Data:**

We used a dataset of brain MRI images from Kaggle [link here](https://www.kaggle.com/navoneel/brain-mri-images-for-brain-tumor-detection), but there wasn't quite enough data to train our AI effectively. 

**Data Augmentation to the Rescue!**

To address the limited data, we employed a special technique called data augmentation. This essentially creates more training examples from the existing data, making our AI model more robust. 

**Training Our Champion:**

The data went through a rigorous training process, including:

* **Brain Extractor:** We cropped each image to focus solely on the brain, the vital area of interest.
* **Standardization:** Images were resized and normalized to ensure consistency for the AI model.
* **Data Split:** The data was divided strategically for training, validation, and testing purposes.
* **Neural Network Architecture**

![Neural Network Architecture](convnet_architecture.jpg)

**Understanding the architecture:**<br>
Each input x (image) has a shape of (240, 240, 3) and is fed into the neural network. And, it goes through the following layers:<br>

1. A Zero Padding layer with a pool size of (2, 2).
2. A convolutional layer with 32 filters, with a filter size of (7, 7) and a stride equal to 1.
3. A batch normalization layer to normalize pixel values to speed up computation.
4. A ReLU activation layer.
5. A Max Pooling layer with f=4 and s=4.
6. A Max Pooling layer with f=4 and s=4, same as before.
7. A flatten layer in order to flatten the 3-dimensional matrix into a one-dimensional vector.
8. A Dense (output unit) fully connected layer with one neuron with a sigmoid activation (since this is a binary classification task).

**Why this architecture?**<br>

Firstly, I applied transfer learning using a ResNet50 and vgg-16, but these models were too complex to the data size and were overfitting. Of course, you may get good results applying transfer learning with these models using data augmentation. But, I'm using training on a computer with 6th generation Intel i7 CPU and 8 GB memory. So, I had to take into consideration computational complexity and memory limitations.<br>

So why not try a simpler architecture and train it from scratch. And it worked :)

# Training the model
The model was trained for 24 epochs and these are the loss & accuracy plots:


![Loss plot](Loss.PNG)


![Accuracy plot](Accuracy.PNG)

The best validation accuracy was achieved on the 23rd iteration.

# Results

Now, the best model (the one with the best validation accuracy) detects brain tumor with:<br>

**88.7%** accuracy on the **test set**.<br>
**0.88** f1 score on the **test set**.<br>
These resutls are very good considering that the data is balanced.


**Performance Breakdown:**

| Metric | Validation Set | Test Set |
|---|---|---|
| Accuracy | 91% | 89% |
| F1 Score | 0.91 | 0.88 |

**What's Here for You?**

* IPython notebooks containing the code.
* Pre-trained model weights, with the best model clearly labeled.
* Original and augmented data for reference.

**Join the Fight!**

We welcome contributions to this project. Together, let's keep pushing the boundaries of AI in healthcare.

**Thank you!**

This  README highlights the project's purpose, the challenges addressed, and the achieved results. 
