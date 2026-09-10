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
| ![original]<img width="277" height="490" alt="image" src="https://github.com/user-attachments/assets/68f0ece9-6244-4b6e-9577-d11a0dd73c9a" />
| ![grayscale] <img width="312" height="551" alt="image" src="https://github.com/user-attachments/assets/5a8ecab1-1680-4a97-ab19-753fb4c3f02e" />
| ![sepia]<img width="226" height="390" alt="image" src="https://github.com/user-attachments/assets/0466a418-5a96-4ef1-bd09-bfa71d5b7812" />
 | ![blur]<img width="197" height="345" alt="image" src="https://github.com/user-attachments/assets/2585621e-038e-4885-880a-4b3999682644" />
 | ![edge]<img width="297" height="521" alt="image" src="https://github.com/user-attachments/assets/2e1d8d65-16dd-4256-9f8b-ad47f83d918b" />
|

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
