# disaster-response
A zero-shot learning (ZSL) based disaster response system that classifies disaster types using multimodal inputs (images and text) without requiring task-specific training.

## Overview
This project leverages OpenAI's **CLIP** model to classify disaster types (e.g., floods, wildfires, earthquakes, hurricanes) from images using zero-shot learning. It combines visual and textual embeddings to make predictions without needing labeled disaster datasets.

## Features
- Zero-shot classification of disaster types
- Multimodal input (images + text prompts)
- Pre-trained CLIP model (ViT-B/32)
- Customizable disaster classes and prompts
- Real-time inference with GPU acceleration

## Installation
1. Clone the repository:
```bash
git clone https://github.com/mariam-gad232/disaster-response.git
```

## Install dependencies:

```
pip install torch torchvision clip ftfy requests matplotlib
```
## Download pre-trained CLIP model:

```
python -c "import clip; clip.load('ViT-B/32')"
```

## Customizing Disaster Classes
Edit disaster_classes.json to add or modify disaster types and their associated text prompts:

```
{
    "flood": [
        "a photo of a flood with water covering streets",
        "an image of submerged houses due to heavy rainfall"
    ],
    "wildfire": [
        "a photo of a forest fire with smoke and flames",
        "burning trees in a wildfire"
    ]
}
```

## Dataset
Uses zero-shot learning, so no specific dataset is required. However, you can test with:

-Disaster images from public datasets (e.g., NOAA, ReliefWeb)
-Custom images of floods, wildfires, earthquakes, etc.

## Results
Disaster Type	Accuracy (Sample)
Flood	85%
Wildfire	90%
Earthquake	75%
Hurricane	80%


## Acknowledgments
OpenAI for the CLIP model
Public disaster image datasets for testing
