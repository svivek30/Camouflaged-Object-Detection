# Setup Guide

## Quick Start

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/COD.git
   cd COD
   ```

2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Run the application**
   ```bash
   cd COD
   python app.py
   ```

4. **Open your browser**
   Navigate to `http://localhost:8000`

## Project Structure

```
COD/
├── COD/                      # Main application directory
│   ├── app.py               # FastAPI main application
│   ├── inference.py         # Standalone inference script
│   ├── Architecture/        # Model architecture files
│   ├── Back End/           # Backend components
│   ├── Front End/          # Web interface files
│   ├── COD10K Trained model/ # Pre-trained model weights
│   └── uploads/            # Runtime upload directory
├── requirements.txt        # Python dependencies
├── README.md              # Project documentation
├── LICENSE                # MIT License
└── .gitignore            # Git ignore rules
```

## Model Files

The pre-trained model files are included in the `COD10K Trained model/` directory:
- `Net_epoch_best.pth` - Main SINet V2 model weights
- `res2net50_v1b_26w_4s-3cf99910.pth` - ResNet backbone weights

## Usage

### Web Interface
1. Start the application with `python app.py`
2. Upload an image through the web interface
3. View detection results in three formats:
   - Bounding boxes
   - Segmentation masks
   - Confidence heatmaps

### Standalone Inference
```bash
python inference.py
# Enter image path when prompted
```

## Requirements

- Python 3.8+
- PyTorch 2.1.0+
- CUDA (optional, for GPU acceleration)
- 4GB+ RAM recommended
- 2GB+ disk space for model files

## Troubleshooting

1. **CUDA out of memory**: Reduce image size or use CPU
2. **Model loading errors**: Ensure model files are in correct directory
3. **Port already in use**: Change port in `app.py` or kill existing process