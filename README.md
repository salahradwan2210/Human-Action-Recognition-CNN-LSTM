# Human Action Recognition using CNN-LSTM

This project implements a human action recognition system using a hybrid CNN-LSTM architecture. The model is capable of recognizing six different human actions: HUGGING, KICKING, PUNCHING, PUSHING, HANDSHAKING, and POINTING.

## Features

- Hybrid CNN-LSTM architecture with attention mechanism
- Real-time video processing capabilities
- Support for multiple video formats
- Advanced feature extraction using optical flow
- Visualization tools for model performance analysis

## Project Structure

```
Human-Action-Recognition-CNN-LSTM/
├── src/                    # Source code
├── notebooks/             # Jupyter notebooks
├── outputs/               # Model outputs and visualizations
├── data/                  # Data directory
│   ├── videos/           # Video files
│   └── csv/              # CSV files
└── requirements.txt       # Project dependencies
```

## Setup and Installation

1. Clone the repository:
```bash
git clone https://github.com/salahradwan2210/Human-Action-Recognition-CNN-LSTM.git
cd Human-Action-Recognition-CNN-LSTM
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

## Usage

1. Place your video files in the `data/videos` directory
2. Run the main script:
```bash
python src/main.py
```

## Model Architecture

The model uses a hybrid architecture combining:
- CNN layers for spatial feature extraction
- Bidirectional GRU for temporal feature processing
- Attention mechanism for focusing on important features
- Deep classifier with skip connections

## Results

The model achieves significant accuracy in recognizing human actions, with detailed performance metrics available in the outputs directory:
- Training history plots
- Confusion matrix
- Class distribution analysis

## License

This project is licensed under the MIT License - see the LICENSE file for details. 