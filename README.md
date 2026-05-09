# Cartoonify Image

A deep learning project that converts real images into cartoon-style artwork using neural networks and image processing techniques.

## Features

- **Image Cartoonification**: Transform regular photos into cartoon-style images
- **Black Outlines**: Creates strong black edge outlines for classic cartoon appearance
- **Flat Color Reduction**: Uses K-means clustering to reduce colors for a stylized look
- **Webcam Support**: Real-time cartoonification from webcam feed
- **Pre-trained Models**: Includes pre-trained Keras models for quick inference

## Project Structure

```
cartoonify image/
├── CARTOON.ipynb            
├── bestcartoon.keras         
├── cartoonmmm.keras          
├── requirements.txt          
├── README.md                  
└── dataset/
    ├── train/
    │   ├── cartoon/          
    │   └── real/            
    └── val/
        ├── cartoon/         
        └── real/            
```
## imp
create model by run test.py
gives a cartoonify model named "bestcartoon.keras"

## Installation

1. **Clone or download this project**

2. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```


### Parameters

- **line_thickness**: Thickness of black outlines (default: 2)
- **n_colors**: Number of flat colors for quantization (default: 8)

### Real-time Webcam Cartoonification

Run the notebook cells that use `cv2.VideoCapture(0)` to enable live webcam processing. Press 'q' to quit.

### Capture Photo from Webcam

Use the photo capture cells in the notebook to capture a single frame from your webcam and cartoonify it.

## Models

- **bestcartoon.keras**: Primary trained model with optimized performance
- **cartoonmmm.keras**: Alternative model for comparison

## Dependencies

- numpy
- matplotlib
- tensorflow >= 2.10.0
- opencv-python
- Pillow

See `requirements.txt` for complete list.

## Key Functions

### `cartoon_simple_black_outline_flat_colors()`
Main cartoonification function that:
1. Reduces colors using K-means clustering
2. Detects edges using Canny edge detection
3. Creates thick black outlines
4. Combines edges with flat colors for cartoon effect

## Dataset

The project includes training and validation datasets with:
- **Real images**: Original photographs
- **Cartoon images**: Target cartoon-style outputs

Used for training the neural network model.

## Examples

Multiple example cells in the notebook demonstrate:
- Static image cartoonification
- Webcam streaming
- Photo capture and cartoonification
- Parameter tuning (line thickness and color counts)

## License

This project is provided as-is for educational and personal use.

## Notes

- For better results, experiment with different `line_thickness` and `n_colors` parameters
- Higher color counts produce more detailed results but less stylization
- Thicker lines create stronger cartoon outlines
- GPU acceleration is recommended for faster processing with TensorFlow

---
example outputs
<img width="997" height="447" alt="image" src="https://github.com/user-attachments/assets/cc51be23-c788-4117-813b-6e09dc60f4f2" />
<img width="993" height="355" alt="image" src="https://github.com/user-attachments/assets/cbe924d2-9cc2-4178-8188-f0b315a971c5" />
<img width="995" height="350" alt="image" src="https://github.com/user-attachments/assets/75b47c84-557b-40e8-8993-ff8472266f1e" />
<img width="995" height="571" alt="image" src="https://github.com/user-attachments/assets/50b3b763-b02a-4e60-bdfc-96d82b73db3b" />



data set made myself by converting real image to catroon image using gemini
link of dataset is below
https://drive.google.com/file/d/1lGR48ZhNL-td6qEDbjBDaU6BThpMk0sj/view?usp=drive_link


For more details, see the `CARTOON.ipynb` notebook.
