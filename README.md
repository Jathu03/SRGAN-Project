# SRGAN-Project: Super-Resolution Image Generation

![GAN](https://img.shields.io/badge/Deep%20Learning-SRGAN-orange)

This repository is dedicated to the implementation of the **Super-Resolution Generative Adversarial Network (SRGAN)** architecture. The project's primary goal is to perform super-resolution by taking low-resolution (LR) input images and generating corresponding high-resolution (HR) images, significantly enhancing image detail and quality.

## 🧠 Core Methodology

The project utilizes the **SRGAN** variant of Generative Adversarial Networks (GANs). This is a crucial deep learning technique for image processing where:
1.  **Generator:** Creates high-resolution details from low-res inputs.
2.  **Discriminator:** Distinguishes between the generated images and real high-resolution images, forcing the Generator to create more realistic textures.

## 📂 Project Structure

The entire project codebase is written in **Python (100.0%)**. The implementation is modularized across several files:

| File Name | Role in the SRGAN Pipeline |
| :--- | :--- |
| **`model.py`** | Contains the definition of the two primary network architectures: the **Generator** (upscaling) and the **Discriminator** (judging realism). |
| **`train.py`** | The main script that orchestrates the training process, including running the GAN loop, updating weights, and saving checkpoints. |
| **`dataset.py`** | Handles the creation of LR and HR image pairs, performs data augmentation, and manages data loading for efficient batch processing. |
| **`loss.py`** | Implements the specific loss functions critical to SRGAN training, including **Perceptual Loss (VGG loss)** and **Adversarial Loss**. |
| `config.py` | Defines global variables, hyperparameters (e.g., learning rates, batch size), and file paths necessary for managing the training environment. |
| `utils.py` | Provides helper functions for metric calculation, visualization, image saving, and checkpoint loading. |
| `.gitignore` | Specifies files and directories (like compiled files or data outputs) to be ignored by Git. |

## 🚀 Getting Started

### Prerequisites
*   Python 3.x
*   PyTorch (Recommended)
*   Numpy, Matplotlib, Pillow

### Installation
1.  Clone the repository:
    ```bash
    git clone https://github.com/YourUsername/SRGAN-Project.git
    cd SRGAN-Project
    ```

2.  Install dependencies:
    ```bash
    pip install -r requirements.txt
    ```

### Usage
1.  **Configure:** Open `config.py` to set your dataset paths and hyperparameters.
2.  **Train:** Run the training script:
    ```bash
    python train.py
    ```

## 🛠️ Tech Stack

*   **Language:** Python (100.0%)
*   **Domain:** Computer Vision / Deep Learning
