# DCGAN Human Face Generation

*a bittersweeet relic from my grad school days.*

## Overview

Synthetic human-face generation using a Deep Convolutional Generative Adversarial Network (DCGAN), implemented with TensorFlow and Keras and trained on the CelebA dataset.

The project explores adversarial learning, convolutional network architectures, dataset balancing, and hyperparameter optimization to generate realistic 128 × 128 facial images.

## Methodology

- **Data Preparation:** Preprocessed the CelebA dataset and explored attribute balancing to improve the representation of facial characteristics.
- **Model Architecture:** Implemented convolutional generator and discriminator networks for adversarial image generation.
- **Hyperparameter Optimization:** Applied Bayesian optimization using Keras Tuner to explore convolutional filters, kernel sizes, learning rates, and batch sizes.
- **Adversarial Training:** Trained the generator and discriminator iteratively to improve image synthesis quality.
- **Model Evaluation:** Examined generated image quality and diversity through visual inspection and quantitative metrics, including Inception Score (IS) and Fréchet Inception Distance (FID).

## Model Architecture

The DCGAN consists of two adversarial components:

| Component | Function |
|---|---|
| Generator | Transforms random latent vectors into synthetic facial images using transposed convolutional layers. |
| Discriminator | Uses convolutional layers to distinguish generated images from real CelebA samples. |

Through adversarial training, the generator learns to produce increasingly realistic facial features, while the discriminator learns to identify differences between real and synthetic images.

## Training Progression

![DCGAN Training Progression](artifacts/timelapse.gif)

The animation illustrates the progressive development of facial features throughout training, demonstrating improvements in image structure, clarity, and visual realism.

## Model Development

- [Jupyter Notebook](artifacts/model_development.ipynb)
- [Rendered Notebook](https://mirabelleding.github.io/DCGAN-Human-Face/)

*Note: Due to its large file size, the original Jupyter notebook cannot be rendered directly on GitHub. The rendered version preserves the code, training progression, and saved outputs for viewing.*