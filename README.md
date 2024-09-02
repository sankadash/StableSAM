# StableSAM
## Image Inpainting with Gradio and Stable Diffusion

StableSAM is an advanced image inpainting tool that combines the power of the Stable Diffusion model with Meta Research FAIR's Segment Anything Model (SAM). This project allows users to perform intuitive and creative image editing based on natural language prompts, providing an innovative solution for image inpainting tasks.

## Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Example](#example)

## Overview

StableSAM leverages state-of-the-art AI models to allow users to select specific regions of an image and apply modifications based on user-provided prompts. The tool provides a seamless and interactive experience for creative professionals and enthusiasts looking to enhance or completely transform images.

### How It Works

1. **User Input:**
   - Users can upload one or two images via a Gradio-based web interface.
   - Users select a region of interest within the image that they wish to modify or blend with another image.
   - Users provide a textual prompt describing the desired transformation or adaptation.

2. **Processing:**
   - A binary mask is generated for the selected region using the Segment Anything Model (SAM).
   - The binary mask, along with the input image and user prompt, is passed to the Stable Diffusion Inpainting model.
   - The model performs image inpainting around the selected region based on the prompt, generating a modified output image.

## Features

- **User-Friendly Interface:** Intuitive Gradio interface for easy interaction.
- **Flexible Image Editing:** Supports multiple image uploads and region-based editing.
- **Natural Language Prompts:** Allows users to specify image transformations using simple text prompts.
- **High-Quality Inpainting:** Utilizes the Stable Diffusion model for high-fidelity image generation.

## Installation

To run StableSAM, ensure you have the following prerequisites:

- Python 3.8 or higher
- CUDA-compatible GPU (optional but recommended for faster processing)
- Required Python libraries (specified in `requirements.txt`)

### Step-by-Step Installation

1. **Clone the Repository:**

   ```bash
   git clone https://github.com/sankadash/StableSAM.git
   cd StableSAM
   ```

2. **Install the Dependencies:**

   Install the required Python libraries:

   ```bash
   pip install -r requirements.txt
   ```

3. **Download Model Weights:**

   Ensure you have the required model weights for SAM and Stable Diffusion. Place the SAM model weights in the `weights` directory as specified:

   ```bash
   mkdir weights
   # Place your SAM model weights file in the weights directory
   ```

## Usage

Run the application locally using the following command:

```bash
python app.py
```

This will launch the Gradio interface in your default web browser. Follow these steps to use the application:

1. Upload your image(s).
2. Select the region of interest on the image(s) using the interactive tool.
3. Enter a textual prompt describing the desired modification.
4. Click "Submit" to generate the output image with the inpainting applied.

### Example
Upload an image of a landscape, select an area you wish to modify (e.g., the sky), and provide a prompt like "Replace the sky with a sunset." The tool will generate a new image with the specified modification.


## Acknowledgments

- [Hugging Face](https://huggingface.co/) for the Stable Diffusion model.
- [Meta Research FAIR](https://github.com/facebookresearch/segment-anything) for the Segment Anything Model (SAM).

