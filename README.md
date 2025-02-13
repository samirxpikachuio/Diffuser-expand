# Diffuser-Expand

Expand Image using Stable Diffusion XL Outpainting

### 🖼️ Output Examples

These examples showcase the image expansion capabilities:

![jmwknt](https://github.com/user-attachments/assets/a1d9b593-a90b-4ea2-87f5-91f018b23d95)
![oqij2v](https://github.com/user-attachments/assets/6469a926-56a2-491f-9d09-c85465e4f027)

## Overview

This project provides a tool to expand existing images using Stable Diffusion XL outpainting techniques.  It leverages a ControlNet-guided diffusion process to seamlessly blend generated content with the original image, extending its borders in a coherent and visually appealing manner.

**Key Features:**

*   **Image Expansion:**  Extend the boundaries of an image beyond its original dimensions.
*   **ControlNet Guidance:**  Utilizes ControlNet to maintain consistency and coherence between the original image and the generated content.
*   **Stable Diffusion XL:** Built on the powerful Stable Diffusion XL model for high-quality image generation.
*   **Gradio Interface:** User-friendly interface for easy interaction and parameter adjustment.

## Requirements

*   **Minimum VRAM:**  Approximately 6 GB with a 1280x720 image using the following configuration: RTX 3060, `RealVisXL_V5.0_Lightning` model, `sdxl-vae-fp16-fix` VAE, `controlnet-union-sdxl-promax` ControlNet, and `sequential_cpu_offload` enabled.  Otherwise, expect to require around 8.3 GB of VRAM.

## Usage ( Adjust accordingly!)


1.  **Installation:** Follow the instructions in the code comments to install the necessary dependencies (using `pip install -r requirements.txt`). Also, please make sure to download and configure any custom models.

2.  **Running the App:** Execute the Python script (`app.py`). This will launch this

3.  **How to use it**

    *   **Upload Image:** Upload the image you want to expand.
    *   **Set Parameters:**
        *   **Width & Height:**  Specify the desired dimensions for the expanded image.
        *   **Prompt:**  Provide a text prompt to guide the image generation process (optional).
        *   **Aspect Ratio:**  Choose a preset aspect ratio or customize the width and height.
        *   **Alignment:** Control the positioning of the original image within the expanded canvas.
        *   **Overlap:** Adjust the overlap between the original image and the outpainted regions.
        *   **Resize:** Choose how the image is resized.

    *   **Generate:**  Click the "Generate" button to start the outpainting process.

## VRAM Optimization (If not applicable directly. More for the underlying code).

*   **Sequential CPU Offload:** Reduces VRAM usage by offloading parts of the model to the CPU.
