# Braille to Text Converter

![Braille to Text Converter](https://img.shields.io/badge/Project-Braille%20to%20Text-blue)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-orange)
![Python](https://img.shields.io/badge/Python-3.8%2B-green)
![License](https://img.shields.io/badge/License-MIT-yellow)

A web application that converts braille patterns in images to readable text using computer vision and deep learning.

## 🌟 Features

- **Image Upload**: Upload images containing braille patterns
- **Automatic Detection**: Identifies braille dots and patterns in images
- **Text Conversion**: Translates detected braille patterns to English text
- **Visual Feedback**: Displays processed image with detected braille highlighted
- **Responsive Design**: Works on desktop and mobile devices

## 🖼️ Demo

![Demo of Braille to Text Converter](demo_screenshot.png)

Try the live demo: [Braille to Text Converter](https://braille-to-text-cnn.onrender.com/)

## 🔧 Technology Stack

- **Frontend**: HTML, CSS, JavaScript
- **Backend**: Flask (Python)
- **Machine Learning**: TensorFlow/Keras CNN model
- **Image Processing**: OpenCV
- **Deployment**: Render

## 📋 How It Works

1. **Image Preprocessing**:
   - Converts image to grayscale
   - Applies thresholding to isolate braille dots
   - Detects light direction for better dot recognition

2. **Segmentation**:
   - Identifies individual braille cells
   - Groups cells into words and sentences
   - Prepares segments for model input

3. **Prediction**:
   - Feeds preprocessed segments to a trained CNN model
   - Model classifies each braille pattern to corresponding letter
   - Combines predictions to form complete text

4. **Visualization**:
   - Highlights detected braille patterns
   - Overlays predicted text on the original image
   - Returns processed image with text conversion

## 🚀 Getting Started

### Prerequisites

- Python 3.8 or higher
- pip (Python package manager)

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/braille-to-text.git
   cd braille-to-text
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Run the application:
   ```bash
   python predict_app.py
   ```

4. Open your browser and navigate to:
   ```
   http://localhost:10000
   ```

### Docker Deployment

```bash
docker build -t braille-to-text .
docker run -p 10000:10000 braille-to-text
```

## 📊 Model Training

The CNN model was trained on a dataset of braille patterns with the following characteristics:

- **Dataset**: Custom dataset of braille characters (a-z)
- **Architecture**: Convolutional Neural Network with 3 convolutional layers
- **Training**: Trained for 50 epochs with data augmentation
- **Accuracy**: 95% accuracy on test set

## 📝 Usage Guidelines

For best results:

- Use well-lit images with good contrast
- Ensure braille dots are clearly visible
- Avoid shadows across the braille text
- Position camera perpendicular to the braille surface
- Maintain consistent lighting across the image

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgements

- [TensorFlow](https://www.tensorflow.org/) for the machine learning framework
- [OpenCV](https://opencv.org/) for image processing capabilities
- [Flask](https://flask.palletsprojects.com/) for the web framework
- [Render](https://render.com/) for hosting the application

## 📞 Contact

Your Name - [your.email@example.com](mailto:your.email@example.com)

Project Link: [https://github.com/yourusername/braille-to-text
