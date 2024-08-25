
# LLaVA Model Setup and Installation Guide

This README provides detailed instructions for setting up and configuring the environment necessary to run the LLaVA model with optimal settings for performance and testing.

## System Requirements
- **RAM:** 32 GB or higher

###  Clone the Repository
Before setting up the environment, clone the LLaVA repository to your local machine. Use the following command in your terminal:

```bash
git clone https://github.com/shijithm7/LLaVA_integration.git
cd LLaVA_integration
```


## Installation Steps

### Step 1: Create and Activate Conda Environment
First, you need to create a dedicated Conda environment for the LLaVA project. Use the following commands in your terminal:


```bash

conda create --name LLaVA_env python=3.10.12
conda activate LLaVA_env

```

### Step 2: Install Required Libraries
Install the necessary Python libraries in your Conda environment. Run the following commands:

```bash
# Install Pillow for image processing
pip install pillow

# Install specific version of Transformers and Gradio for creating web UIs
pip install transformers==4.31.0
pip install -q gradio

# Install BitsAndBytes for optimized training
pip install bitsandbytes

# Install Accelerate for distributed training
pip install accelerate
```

### Step 3: Install PyTorch
Ensure you have the correct version of PyTorch installed that is compatible with your CUDA version. For CUDA 12.4, use the following command:

```bash
pip3 install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu124
```

## Verification
After installation, verify that all components are installed correctly by checking the versions of the installed packages:

```bash
conda list
```

Ensure that the versions match the requirements specified in the installation steps.

## Usage
Once the installation is complete, you can start developing and testing with the LLaVA model within the `LLaVA_env` environment. Make sure to activate the Conda environment every time you work on the project:

```bash
conda activate LLaVA_env
cd LLaVA
```
Run the notebook  [LLaVA_13b_4bit_vanilla_inference_code.ipynb](https://github.com/shijithm7/LLaVA_integration/blob/main/LLaVA/LLaVA_13b_4bit_vanilla_inference_code.ipynb)    with kernal ``` LLaVA_env ```


[LLaVA_13b_4bit_vanilla_google_colab_code.ipynb](https://github.com/shijithm7/LLaVA_integration/blob/main/LLaVA/LLaVA_13b_4bit_vanilla_google_colab_code.ipynb) This notebook demonstrates how to quickly set up and test the LLaVA model with 4-bit quantization in Google Colab. This setup is optimized for rapid testing and inference vision models, leveraging Colab's GPUs.



For model Training and Evaluation [Refere Here](https://github.com/shijithm7/LLaVA_integration/blob/main/LLaVA/README.md)


## Troubleshooting
If you encounter any issues during the installation, make sure to check the compatibility of the installed packages with your system specifications. Revisit the installation commands to ensure they were entered correctly.

For more detailed guidance or support, refer to the official documentation of each package or reach out to their respective support forums.
