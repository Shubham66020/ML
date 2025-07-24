# 🎭 Emotion Detection AI

A real-time emotion detection web application powered by TensorFlow.js and Teachable Machine. This project uses machine learning to analyze facial expressions through your webcam and identify emotions in real-time.

## ✨ Features

- 🎥 **Real-time webcam emotion detection**
- 🎨 **Beautiful modern UI** with gradient backgrounds and glassmorphism design
- 😊 **Emoji indicators** for each detected emotion
- 📊 **Percentage-based confidence scores**
- ⚡ **Instant predictions** with smooth animations
- 🎯 **High-confidence highlighting** with pulsing effects
- 📱 **Responsive design** that works on all devices

## 🚀 Demo

The application detects the following emotions:

- 😊 Happy
- 😢 Sad
- 😠 Angry
- 😲 Surprised
- 😐 Neutral
- 😨 Fear
- 🤢 Disgust

## 🛠️ Technology Stack

- **Frontend**: HTML5, CSS3, JavaScript (ES6+)
- **Machine Learning**: TensorFlow.js, Teachable Machine
- **Webcam Integration**: WebRTC API
- **Styling**: CSS Grid, Flexbox, CSS Animations

## 📁 Project Structure

```
emotion_detect/
├── index.html          # Main application file
├── model/              # Trained ML model files
│   ├── model.json      # Model architecture
│   ├── metadata.json   # Model metadata
│   └── weights.bin     # Model weights
└── README.md          # Project documentation
```

## 🏗️ Installation & Setup

1. **Clone or download** this repository to your local machine

2. **Ensure you have the model files** in the `model/` directory:

   - `model.json`
   - `metadata.json`
   - `weights.bin`

3. **Start a local server** (required for webcam access):

   **Option A: Using Python**

   ```bash
   # Python 3
   python -m http.server 8000

   # Python 2
   python -SimpleHTTPServer 8000
   ```

   **Option B: Using Node.js**

   ```bash
   npx serve .
   ```

   **Option C: Using Live Server (VS Code)**

   - Install the "Live Server" extension
   - Right-click on `index.html` and select "Open with Live Server"

4. **Open your browser** and navigate to `http://localhost:8000`

5. **Click "🚀 Start Detection"** and allow webcam access when prompted

## 🎯 How It Works

1. **Model Loading**: The application loads a pre-trained TensorFlow.js model created with Google's Teachable Machine
2. **Webcam Setup**: Initializes webcam feed with 200x200 pixel resolution
3. **Real-time Analysis**: Continuously captures frames and runs them through the emotion detection model
4. **Results Display**: Shows confidence percentages for each emotion with corresponding emojis
5. **Visual Feedback**: Highlights high-confidence predictions (>70%) with pulsing animations

## 🔧 Customization

### Modifying Emotions

To add or modify emotions, update the `emotionEmojis` object in the JavaScript code:

```javascript
const emotionEmojis = {
  happy: "😊",
  sad: "😢",
  angry: "😠",
  surprised: "😲",
  neutral: "😐",
  fear: "😨",
  disgust: "🤢",
  custom_emotion: "🤔", // Add your custom emotion
};
```

### Changing Webcam Resolution

Modify the webcam initialization parameters:

```javascript
webcam = new tmImage.Webcam(width, height, flip);
```

### Adjusting Confidence Threshold

Change the pulsing effect threshold:

```javascript
if (prediction[i].probability > 0.7) {
  // Change 0.7 to your desired threshold
  predictionElement.classList.add("pulse");
}
```

## 🎨 Styling

The application features a modern design with:

- **Gradient backgrounds** for visual appeal
- **Glassmorphism effects** with backdrop blur
- **Smooth animations** and hover effects
- **Card-based layouts** for predictions
- **Responsive design** for all screen sizes

## 🔐 Privacy & Security

- **Local Processing**: All emotion detection happens locally in your browser
- **No Data Storage**: No images or data are stored or transmitted
- **Webcam Access**: Only used for real-time analysis, not recording

## 🌐 Browser Compatibility

- ✅ Chrome (recommended)
- ✅ Firefox
- ✅ Safari
- ✅ Edge
- ⚠️ Requires HTTPS or localhost for webcam access

## 📝 Requirements

- Modern web browser with WebRTC support
- Webcam access permission
- Local server (for file protocol restrictions)

## 🤝 Contributing

Feel free to contribute to this project by:

1. Forking the repository
2. Creating a feature branch
3. Making your changes
4. Submitting a pull request

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

## 🙏 Acknowledgments

- **Google Teachable Machine** for the easy-to-use ML model training platform
- **TensorFlow.js** for enabling machine learning in the browser
- **WebRTC** for webcam access capabilities

## 📞 Support

If you encounter any issues or have questions:

1. Check that your webcam is working properly
2. Ensure you're running the app on a local server (not file://)
3. Verify that all model files are present in the `model/` directory
4. Make sure your browser supports WebRTC and has webcam permissions

---

**Made with ❤️ and JavaScript**
