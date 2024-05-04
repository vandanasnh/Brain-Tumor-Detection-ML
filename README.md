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

**Building the Brain Tumor Fighter:**

We opted for a custom-designed neural network architecture, considering the data size and computational limitations. 

**Why Not Go Pre-Built?**

We experimented with pre-trained models like ResNet50 and VGG-16, but they proved too complex for our data size. Our custom model, trained from scratch, achieved impressive results while keeping things efficient.

**The Champion Emerges!**

After 24 rounds of training, we identified the best performing model, achieving:

* **88.7% Accuracy** on identifying brain tumors in unseen test data.
* **0.88 F1 Score** indicating a strong balance between precision and recall.

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
