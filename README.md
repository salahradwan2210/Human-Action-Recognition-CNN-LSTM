# Human Action Recognition using CNN-LSTM

This project implements a human action recognition system using a hybrid CNN-LSTM architecture. The model is capable of recognizing six different human actions: HUGGING, KICKING, PUNCHING, PUSHING, HANDSHAKING, and POINTING.

## Features

- Hybrid CNN-LSTM architecture with attention mechanism
- Real-time video processing capabilities
- Support for multiple video formats
- Advanced feature extraction using optical flow
- Visualization tools for model performance analysis

## Dataset

This project uses the UT-Interaction dataset, which contains videos of human interactions:
- **Dataset Link**: [UT-Interaction Dataset on Kaggle](https://www.kaggle.com/datasets/duynm619/utinteraction)
- Contains 6 classes of human interactions: HUGGING, KICKING, PUNCHING, PUSHING, HANDSHAKING, and POINTING
- Standard benchmark for human action recognition algorithms

## Project Structure

```
Human-Action-Recognition-CNN-LSTM/
├── notebooks/             # Jupyter notebooks
├── output/                # Model outputs and visualizations
│   ├── training_history.png    # Training progress visualization
│   ├── confusion_matrix.png    # Model performance analysis
│   ├── class_distribution.png  # Dataset class distribution
├── model/                 # Model directory
│   └── ut_interaction_model.pth # Pre-trained model for inference (not included in repo)
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

## Output Directory Structure

The `output` directory will contain files generated during training and testing:

### Visualization Files
The following files will be automatically generated when running the model:
- `training_history.png`: Shows training and validation accuracy/loss over epochs
- `confusion_matrix.png`: Displays model's classification performance
- `class_distribution.png`: Shows distribution of samples across classes

### Video Outputs
Processed videos with predictions will be saved as:
- `output_video_name.mp4`: Original video with predictions overlaid
- Format: MP4 with predictions, confidence scores, and action descriptions

## Model Performance

### Training History
![Training History](output/training_history.png)
The training history shows the model's learning progress over epochs, with both training and validation metrics. The final model achieved:
- Training Accuracy: 84.56%
- Validation Accuracy: 92.90%
- Best Validation Accuracy: 93.23%

### Confusion Matrix
![Confusion Matrix](output/confusion_matrix.png)
The confusion matrix shows the model's classification performance across all action classes. Notable results:
- Perfect accuracy (100%) for HUGGING and POINTING actions
- Strong performance (>90%) for PUSHING and HANDSHAKING
- Good discrimination between similar actions

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

## Example Videos
Example processed videos are available in the dataset:
- Download sample videos from the [UT-Interaction Dataset on Kaggle](https://www.kaggle.com/datasets/duynm619/utinteraction)
- Place downloaded videos in the `data/videos` directory to test the model's predictions

## License

This project is licensed under the MIT License - see the LICENSE file for details. 
