Dataset
CelebA is a large-scale face attributes dataset with more than 200K celebrity images, each with 40 attribute annotations. The images in this dataset cover large pose variations and background clutter.

Download the data from Sucourse and upload it to your Google Drive. You must upload both CelebA30k.zip and CelebA30k.csv to your Drive without renaming them. CelebA30k is a smaller version of the original CelebA dataset, containing 30,000 images, to reduce computation time during training. Split the data as follows: reserve 10% of the samples for validation and 10% for testing (i.e., 3,000 samples). The remaining 80% should be used for training. Important: The test set (3,000 samples) must be used only for final evaluation and not for model selection or hyperparameter tuning.

Task
The task in this homework is to perform binary smiling classification on a subset of the CelebA dataset using transfer learning.

A pretrained VGG-16 model will be adapted to the task, and its performance will be evaluated under several settings. You will replace the classification head with a binary output layer and train the model for a fixed number of 10 epochs per configuration.

You must:

Freeze appropriate parts of the pretrained model according to the strategy you choose and only modify the classification head.
Evaluate your models using the following hyperparameters:
10 epochs
Learning rate: 0.0001
Fine-tuning strategies:
Freeze all convolutional layers and train only the classifier head.
Freeze all weights except the last convolutional block and the classifier head, and fine-tune those parameters.
Apply Random Horizontal Flip and a light Color Jitter during training, then discuss how these augmentations affect the smiling classification performance.
Dataset: CelebA
Model: VGG-16
Library: PyTorch

Software
You will use the PyTorch framework for this homework. PyTorch offers flexible tools for deep learning, including pretrained models, custom training loops, and GPU acceleration.
