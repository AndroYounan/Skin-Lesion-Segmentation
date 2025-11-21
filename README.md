# Skin-Lesion-Segmentation
Deep learning models for automated skin lesion segmentation, including U-Net from scratch, ResNet34 U-Net, and Attention U-Net with ResNet34.

# Dataset

- The models were trained on publicly available skin lesion segmentation datasets (ISIC Challenge datasets).
- Input images are resized and normalized, with data augmentation including rotations, flips, and color adjustments.

# Models

**1. U-Net (from scratch)**
Standard U-Net architecture with 4 downsampling stages with double convolution blocks, a bottleneck in the center, and four upsampling stages using transposed convolutions.

**2. U-Net (ResNet34 encoder)**
Uses a pre-trained ResNet34 encoder for improved feature extraction and performance.

**3. Attention U-Net (ResNet34 encoder)**
Adds attention gates to the ResNet34 U-Net to focus on relevant regions and capture fine lesion boundaries.

# Results
| Model                              | Dice (F1) | Jaccard (IoU) |
|------------------------------------|-----------|---------------|
| U-Net (from scratch)               |  0.8998   |  0.4499       |
| U-Net (ResNet34 encoder)           |  0.9201   |  0.8536       |
| Attention U-Net (ResNet34 encoder) |  0.9220   |  0.8572       |

# Key insights:

- Baseline U-Net (from scratch) achieved good results but was limited by its lack of pretrained feature extraction.
- Incorporating a ResNet34 encoder significantly improved both Dice and IoU, demonstrating the value of transfer learning for medical imaging tasks.
- The Attention U-Net with ResNet34 achieved the best overall performance, highlighting the benefit of attention mechanisms for capturing fine lesion boundaries and handling challenging artifacts.
- Overall, deeper pretrained encoders and attention modules provide more accurate and reliable lesion segmentation, making them strong candidates for real-world clinical applications.
