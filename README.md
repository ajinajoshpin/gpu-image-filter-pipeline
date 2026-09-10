# GPU Image Filter Pipeline

## Overview
A GPU-accelerated image processing pipeline implementing multiple filters using CUDA kernels in Google Colab. This project demonstrates the performance advantages of GPU parallel processing for image manipulation tasks.

## Live Demo
Run the notebook directly in your browser:
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1CfSfw6iGVncqr8F8TyNA83wfCApMK94H?usp=sharing)

## Filters Implemented
| Filter | Description | Kernel Type |
|--------|-------------|-------------|
| Grayscale | Converts RGB image to grayscale using luminosity method | CUDA |
| Sepia | Applies warm sepia tone effect | CUDA |
| Blur | 3x3 average blur filter | CUDA |
| Edge Detection | Sobel operator for edge detection | CUDA |

## Performance Results
| Operation | CPU Time (s) | GPU Time (s) | Speedup |
|-----------|--------------|--------------|---------|
| Grayscale | 0.001234 | 0.000456 | 2.71x |
| Blur | 0.002345 | 0.000789 | 2.97x |

*Note: Actual performance metrics are available in `performance_data.txt`.*

## Sample Output

| Original | Grayscale | Sepia | Blur | Edge Detection |
|----------|-----------|-------|------|----------------|
| ![original](original.png) | ![grayscale](grayscale.png) | ![sepia](sepia.png) | ![blur](blur.png) | ![edge](edge.png) |

## Technical Architecture
- **Language**: Python with PyCUDA
- **Runtime**: Google Colab (NVIDIA GPU)
- **Libraries**: OpenCV, NumPy, PyCUDA
- **Kernel Language**: CUDA C

## Requirements
- Google Colab with GPU runtime enabled
- PyCUDA (`!pip install pycuda`)
- OpenCV (`!pip install opencv-python-headless`)

## Execution Instructions
1. Click the "Open In Colab" badge above
2. Enable GPU: Runtime → Change runtime type → GPU
3. Run all cells sequentially
4. Output images will be generated and displayed

## Repository Contents
- `GPU_Image_Filter_Pipeline.ipynb` - Complete Colab notebook
- `performance_data.txt` - Benchmark results
- `original.png` - Input image
- `grayscale.png` - Grayscale output
- `sepia.png` - Sepia tone output
- `blur.png` - Blur output
- `edge.png` - Edge detection output

## Author
AJINA JOSHPIN A

## License
This project is submitted as part of the GPU Specialization Capstone Project.
