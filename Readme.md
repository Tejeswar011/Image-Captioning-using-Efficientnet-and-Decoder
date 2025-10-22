# Image Captioner: Transformer-based Automatic Caption Generation from Images

This project implements an **end-to-end deep learning pipeline** for automatic image captioning. It combines an EfficientNet-based CNN encoder for visual feature extraction with a custom multi-head Transformer decoder for sequential caption generation. Designed for both research and deployment, this solution offers robust data handling, modular training workflows, and flexible inference routines. The model is trained on the Kaggle *Flickr8k* dataset, and all steps are automated in a Google Colab environment for easy reproduction and extensibility.

- **Image Encoder:** EfficientNet-B0 (pretrained, frozen feature extractor)
- **Caption Decoder:** Transformer architecture (multi-head attention, custom embedding)
- **Training Data:** Kaggle Flickr8k image-caption dataset
- **Platform:** Google Colab
- **Key Features:** Modular data preprocessing, efficient training, reproducible inference, extensibility for experimentation

*Ready for quick experimentation, benchmarking, and real-world deployment with clean, maintainable code!*

---

## Model Architechture

![Model architechture](https://github.com/user-attachments/assets/fbf08084-adf5-4339-937d-1c737fdef109)

---

## Overview

The **Image Captioner** project builds a smart system that looks at an image and writes a simple sentence describing what it sees. It uses deep learning, mixing computer vision and natural language processing, so you get captions that make real sense—even for new images. Designed for easy use and quick experiments, everything runs in Google Colab to speed up development.

---

## Dataset & Preparation

We use the **Flickr8k dataset** from Kaggle, which has thousands of images and captions. The notebook loads the images, cleans up the captions, splits the data for training and testing, and gets everything ready for the model—all in just a few steps.

---

## Environment Setup

Everything runs on **Google Colab** for maximum convenience—just hit "Run All"!  
Major libraries: `PyTorch` for deep learning, `timm` for image models, and a few handy tools for image and text processing. You only need basic setup—no hassle with local installs.

---

## Model Architecture

The heart of the project is a combo:  
- **EfficientNet-B0 encoder** grabs features from your images (the "eyes" of the system).
- **Transformer decoder** turns those features into readable captions (the "brain" and "mouth" of the system).

It's a smooth pipeline—so images quickly become meaningful words.

---

## Data Processing

First, captions get cleaned up and broken into individual words.  
Images get resized and normalized.  
The project then pairs images with captions, builds a vocab, and creates fast PyTorch DataLoaders—so everything’s smooth and ready for training.

---

## Training

With one command, you start training—the model learns to connect image patterns to real words.  
It tracks the loss for you and adjusts its brain (weights) every step, using the AdamW optimizer and standard loss metrics so you know when it’s getting smarter.

---

## Evaluation & Results

- **Training Loss:** Dropped from **11.1** to below **0.1**—model learned fast and well.
- **Caption Quality:** Outputs are mostly relevant and clear for new images.
- **Verdict:** The system creates sensible captions; quick loss drop shows good learning on this dataset.

---

## Evaluation Metrics

- **BLEU Score:** 0.6059
- **BLEU-1:** 0.6456
- **BLEU-2:** 0.6333
- **BLEU-3:** 0.6231
- **BLEU-4:** 0.6059
- **METEOR:** 0.9323
- **CIDEr:** 4.2625

**Bottom line:** The model delivers strong scores for caption generation tasks, with BLEU and METEOR showing it captures meaning and structure well, and CIDEr confirming high relevance to ground-truth captions.[1]

---

## Model Saving & Inference

Finished training? Just save your model and vocab files.  
You can reload and instantly caption any new image—no need to retrain. It’s plug-and-play for demos or batch predictions.

---

