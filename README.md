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
│   ├── training_history.png    # Training progress visualization
│   ├── confusion_matrix.png    # Model performance analysis
│   ├── class_distribution.png  # Dataset class distribution
│   └── output_videos/          # Processed video outputs
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

3. Download pre-trained model:
   - Download `ut_interaction_model.pth` (274MB) from [Google Drive](https://drive.google.com/file/YOUR_FILE_ID)
   - Place the downloaded file in the `outputs` directory

## Model Performance

### Training History
![Training History](outputs/training_history.png)
The training history shows the model's learning progress over epochs, with both training and validation metrics. The final model achieved:
- Training Accuracy: 84.56%
- Validation Accuracy: 92.90%
- Best Validation Accuracy: 93.23%

### Confusion Matrix
![Confusion Matrix](outputs/confusion_matrix.png)
The confusion matrix shows the model's classification performance across all action classes. Notable results:
- Perfect accuracy (100%) for HUGGING and POINTING actions
- Strong performance (>90%) for PUSHING and HANDSHAKING
- Good discrimination between similar actions

### Class Distribution
![Class Distribution](outputs/class_distribution.png)
The class distribution plot shows the balance of samples across different action classes in both training and testing sets.

## Model Architecture

The model uses a hybrid architecture combining:
- CNN layers for spatial feature extraction
- Bidirectional GRU for temporal feature processing
- Attention mechanism for focusing on important features
- Deep classifier with skip connections

## Results

The model achieves significant accuracy in recognizing human actions:
- Overall Accuracy: 93%
- Macro Average F1-Score: 0.93
- Perfect Recognition (100%) for HUGGING and POINTING actions
- Strong Performance (>90%) for most other actions

### Per-Class Performance:
```
              precision    recall  f1-score   support
     HUGGING       1.00      1.00      1.00        50
     KICKING       0.79      0.94      0.86        52
    PUNCHING       0.93      0.75      0.83        52
     PUSHING       0.91      0.98      0.94        52
 HANDSHAKING       0.98      0.91      0.94        55
    POINTING       1.00      1.00      1.00        49
```

## Model Weights

The trained model weights (`ut_interaction_model.pth`, 274MB) are available for download:
- [Download from Google Drive](https://drive.google.com/file/YOUR_FILE_ID)
- Place the downloaded file in the `outputs` directory
- File contains complete model state including:
  - CNN layers weights
  - GRU parameters
  - Attention mechanism weights
  - Classifier layers

## Video Processing Examples

The model processes videos and generates output files with predictions overlaid:
- Input videos are analyzed frame by frame
- Real-time action recognition is performed
- Confidence scores are displayed
- Action descriptions are shown on the video

Example outputs can be found in the `outputs` directory:
- `output_10_2_1.mp4`: Original processed video
- `output_output_10_2_1.mp4`: Secondary processing example

## License

This project is licensed under the MIT License - see the LICENSE file for details. 