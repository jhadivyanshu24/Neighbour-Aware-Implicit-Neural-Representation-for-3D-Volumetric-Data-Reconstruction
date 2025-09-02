# Neighbour-Aware Implicit Neural Representation for 3D Volumetric Data Reconstruction

A spatially-aware SIREN architecture with 18-neighbor consistency for high-fidelity 3D scientific volume reconstruction and uncertainty quantification.

## Description

This project implements a novel neural implicit field system that predicts central values, uncertainty estimates, and 18 neighboring field values simultaneously. The approach ensures spatially coherent 3D volumetric reconstructions by learning spatial relationships between adjacent voxels. The architecture combines SIREN networks with residual connections and achieves 48+ dB PSNR on scientific datasets.

## Key Features

- Neighbor-aware SIREN architecture with 18-neighbor spatial consistency
- Uncertainty quantification via negative log-likelihood estimation
- Residual connections for improved gradient flow
- VTK integration for 3D scientific data processing
- Real-time inference with GPU acceleration
- Automatic model checkpointing during training

## Quick Start on Kaggle

### Step 1: Upload Your Dataset

1. Go to kaggle.com and sign in to your account
2. Navigate to kaggle.com/datasets
3. Click Create New Dataset button
4. Upload your VTI file (example: Isabel_3D.vti)
5. Set dataset title as "Isabel 3D Hurricane Data" or similar
6. Make the dataset public
7. Note your dataset path: yourusername/dataset-name

### Step 2: Create Training Notebook

1. Go to kaggle.com/code
2. Click New Notebook
3. Select Notebook type
4. In the right panel, click Add data
5. Search for your uploaded dataset and add it
6. Copy and paste the training code from neighbor_aware_neural_fields_training_v1.ipynb
7. Update the file path: input_data_file = '/kaggle/input/your-dataset-name/Isabel_3D.vti'

### Step 3: Configure GPU and Run Training

1. Go to Settings in your notebook
2. Under Accelerator, select GPU T4 x2
3. Click Run All or execute cells one by one
4. Training will take 4-6 hours for 300 epochs
5. Model checkpoints save automatically to /kaggle/working/

### Step 4: Run Inference

1. Create a new notebook for inference
2. Add your dataset and the trained model as data sources
3. Copy inference code from neighbor_aware_neural_fields_inference_v1.ipynb
4. Update model checkpoint path to point to your trained model
5. Execute to generate reconstructed volumes

### Step 5: Download Results

1. After training/inference completes, go to Output tab
2. Download .pth model files and .vti reconstruction files
3. VTI files can be visualized in ParaView or other 3D visualization tools


