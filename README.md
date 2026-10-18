# Smile Classification on CelebA with Transfer Learning (VGG-16)

CS412 Machine Learning (Sabancı University) — Homework 3.

Binary smiling / not-smiling classification on a 30,000-image subset of **CelebA**, by adapting an ImageNet-pretrained **VGG-16** in PyTorch.

## Setup
- **Data split:** 80% train, 10% validation, 10% test; the test set is used only for the final evaluation.
- **Training:** 10 epochs per configuration, learning rate 1e-4, binary classification head replacing the original classifier.

## Experiments
| Strategy | What is trained |
|---|---|
| 1. Frozen backbone | Only the classification head |
| 2. Partial fine-tuning | Last convolutional block + head |
| Augmentation | Strategy runs repeated with random horizontal flip and light color jitter |

**Best validation accuracy: 92.3%** (partial fine-tuning of the last convolutional block).

The notebook reports training/validation loss and accuracy curves, training time per configuration and a discussion of how the augmentations affect performance.

## Files
- `CS412_HW3_Umut_Can_Çubukçu_32453.ipynb` — full pipeline, experiments and discussion
