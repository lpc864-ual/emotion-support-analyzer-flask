# Emotional Support Analyzer

A deep learning-based analyzer that classifies customer messages in Spanish to determine their intention and prioritize customer service.

## Features

- Spanish text analysis to classify customer messages
- Intuitive web interface
- Feedback system for model improvement
- Automatic retraining with new data
- Natural Language Processing with NLTK
- LSTM neural network using TensorFlow/Keras
- Classification into three categories:
  - **A**: Customer praises the product
  - **B**: Customer needs additional information about the product for operation
  - **C**: Customer needs urgent technical support

## Installation

1. Clone the repository:
```bash
git clone https://github.com/[username]/emotion-support-analyzer-flask.git
cd emotion-support-analyzer-flask
```

2. Create a virtual environment (recommended):
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

4. Initialize NLTK:
```python
import nltk
nltk.download('stopwords')
```

## Usage

1. Start the application:
```bash
python app.py
```

2. Open your browser and visit `http://localhost:5000`

3. Enter the text you want to analyze and click "Analyze"

4. Provide feedback to help improve the model

## Project Structure

```
.
├── app.py                 # Main Flask application
├── sentiment_model.py     # Sentiment analysis model
├── data/
│   └── training_data.py   # Training data
├── model/                 # Saved model files
├── static/
│   └── style.css          # CSS styles
├── templates/             # HTML templates
│   ├── index.html
│   ├── result.html
│   └── training.html
├── requirements.txt       # Project dependencies
├── LICENSE.md             # License information
└── README.md              # This file
```

## Model

The system uses an LSTM (Long Short-Term Memory) neural network architecture implemented with TensorFlow/Keras. Key features:

- Text preprocessing with NLTK
- Spanish negation handling
- 100-dimensional word embeddings
- LSTM layers with 64 and 32 units
- Dense layer with ReLU activation
- Dropout for overfitting prevention

## Contributing

Contributions are welcome. Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/new-feature`)
3. Make your changes and commit (`git commit -am 'Add new feature'`)
4. Push to the branch (`git push origin feature/new-feature`)
5. Create a Pull Request

## Main Dependencies

- Flask
- TensorFlow
- NLTK
- NumPy
- scikit-learn
- Keras

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.

## Acknowledgments

- Thanks to all contributors who have helped improve the model
- Special thanks to the Spanish NLP community for providing resources and guidance
- Built with Flask and TensorFlow

## Contact

For questions or suggestions, please open an issue in the GitHub repository.