# COD - Camouflaged Object Detection

A web-based application for detecting camouflaged objects in images using SINet V2 (Search and Identification Network Version 2) deep learning model.

## Features

- **Real-time Detection**: Upload images and get instant camouflaged object detection results
- **Multiple Visualizations**: View detection results as bounding boxes, segmentation masks, and heatmaps
- **Web Interface**: User-friendly web interface built with HTML, CSS, and JavaScript
- **FastAPI Backend**: High-performance API backend with async processing
- **SINet V2 Model**: State-of-the-art deep learning model for camouflaged object detection

## Project Structure

```
COD/
├── app.py                    # Main FastAPI application
├── Architecture/             # Model architecture files
│   ├── lib/                 # Network libraries
│   ├── MyTesting.py         # Testing utilities
│   └── MyTrain_Val.py       # Training and validation
├── Back End/                # Backend components
│   ├── sinetv2_model.py     # SINet V2 model implementation
│   ├── main.py              # Backend main file
│   └── requirements.txt     # Backend dependencies
├── Front End/               # Web interface
│   ├── index.html           # Main HTML page
│   ├── style.css            # Styling
│   ├── script.js            # Frontend JavaScript
│   └── serve.py             # Frontend server
├── COD10K Trained model/    # Pre-trained model weights
└── uploads/                 # Uploaded images storage
```

## Installation

### Prerequisites

- Python 3.8 or higher
- CUDA-compatible GPU (optional, for faster inference)

### Setup

1. Clone the repository:
```bash
git clone https://github.com/yourusername/COD.git
cd COD
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

3. Download pre-trained model weights (if not included):
   - Place model files in `COD10K Trained model/` directory

## Usage

### Running the Application

1. Start the FastAPI server:
```bash
python app.py
```

2. Open your web browser and navigate to:
```
http://localhost:8000
```

3. Upload an image and view the detection results in three different visualizations:
   - **Detection View**: Bounding boxes around detected objects
   - **Segmentation View**: Mask overlays showing object boundaries
   - **Heatmap View**: Confidence heatmaps highlighting detection areas

### API Endpoints

- `GET /` - Main web interface
- `POST /upload` - Upload image for detection
- `GET /health` - Health check endpoint

## Model Information

This project uses SINet V2 (Search and Identification Network Version 2), a deep learning model specifically designed for camouflaged object detection. The model is trained on the COD10K dataset and can detect various types of camouflaged objects including:

- Aquatic creatures (fish, octopus, crabs)
- Terrestrial animals (chameleons, spiders, snakes)
- Flying creatures (birds, insects)
- Other camouflaged objects

## Technical Details

- **Framework**: FastAPI for backend, vanilla HTML/CSS/JS for frontend
- **Deep Learning**: PyTorch with SINet V2 architecture
- **Image Processing**: OpenCV and PIL
- **Model**: Pre-trained on COD10K dataset

## Requirements

```
fastapi>=0.104.1
uvicorn>=0.24.0
python-multipart>=0.0.6
torch>=2.1.0
torchvision>=0.16.0
opencv-python>=4.8.0
pillow>=10.2.0
numpy>=1.24.0
```

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- SINet V2 model architecture
- COD10K dataset for training
- FastAPI framework
- PyTorch deep learning library

## Contact

For questions or support, please open an issue on GitHub.