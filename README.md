<div align="center">
  <h1>Emotion Detection Application using Watson NLP</h1>
</div>

An AI-powered Emotion Detection application built using the Watson NLP Library. This project analyzes text input and predicts emotions such as joy, sadness, anger, fear, and disgust using IBM Watson NLP services.

<img src="https://github.com/AnderMendoza/AnderMendoza/raw/main/assets/line-neon.gif" width="100%">


# 🚀 Project Overview

This application uses the Emotion Predict function from the Watson NLP library to analyze text and detect emotions.

The application sends a POST request to the Watson NLP endpoint and receives emotional analysis results in JSON format.

---

# 🧠 Watson NLP Emotion Predict API

## Endpoint

```python
https://sn-watson-emotion.labs.skills.network/v1/watson.runtime.nlp.v1/NlpService/EmotionPredict
```

## Headers

```python
{
  "grpc-metadata-mm-model-id": "emotion_aggregated-workflow_lang_en_stock"
}
```

## Input JSON Format

```python
{
  "raw_document": {
    "text": text_to_analyze
  }
}
```

---

# 📂 Project Structure

```bash
final_project/
│
├── emotion_detection.py
├── README.md
└── requirements.txt
```

---

# ⚙️ Requirements

Install the required Python library before running the project.

## Install Requests Library

```bash
python3 -m pip install requests
```

Or:

```bash
pip install requests
```

---

# 🧩 emotion_detection.py

```python
import requests
import json

def emotion_detector(text_to_analyze):

    url = 'https://sn-watson-emotion.labs.skills.network/v1/watson.runtime.nlp.v1/NlpService/EmotionPredict'

    headers = {
        "grpc-metadata-mm-model-id":
        "emotion_aggregated-workflow_lang_en_stock"
    }

    input_json = {
        "raw_document": {
            "text": text_to_analyze
        }
    }

    response = requests.post(url, json=input_json, headers=headers)

    return response.text
```

---

# ▶️ How to Run

## Step 1 — Open Python Shell

```bash
python3
```

---

## Step 2 — Import the Application

```python
from emotion_detection import emotion_detector
```

---

## Step 3 — Test the Application

```python
emotion_detector("I love this new technology.")
```

---

# ✅ Example Output

```json
{
  "emotionPredictions": [
    {
      "emotion": {
        "joy": 0.969,
        "sadness": 0.002,
        "anger": 0.001,
        "fear": 0.003,
        "disgust": 0.001
      },
      "target": ""
    }
  ],
  "producerId": {
    "name": "Watson NLP",
    "version": "0.0.1"
  }
}
```

---

# 📌 Features

- Real-time emotion detection
- Watson NLP integration
- REST API communication
- JSON-based response handling
- Beginner-friendly Python project

---

# 🛠 Technologies Used

- Python 3
- Requests Library
- IBM Watson NLP
- REST APIs
- JSON

---

# 📖 Learning Outcomes

Through this project, you will learn:

- How to consume REST APIs in Python
- How NLP emotion analysis works
- How to send POST requests
- JSON request and response handling
- Modular Python programming

---

# 🔥 Sample Test Cases

```python
emotion_detector("I am very happy today!")
emotion_detector("This is absolutely terrible.")
emotion_detector("I feel nervous about tomorrow.")
emotion_detector("I hate this product.")
```

---

# 📷 Assessment Deliverables

## Option 1 — AI Graded Submission

Required files:

- `2a_emotion_detection`
- `2b_application_creation`

---

## Option 2 — Peer-Graded Submission

Required screenshots:

- `2a_emotion_detection.png`
- `2b_application_creation.png`

---

# 🤝 Contributing

Contributions are welcome.

Feel free to fork this repository and improve the application.

---

# 📄 License

This project is created for educational and learning purposes.

---

# 👨‍💻 Author

Developed as part of the IBM Watson NLP Emotion Detection Project.

<p align="center">
  <img 
    src="https://capsule-render.vercel.app/api?type=waving&color=0:FFB347,25:FF8C00,50:FF6200,75:FF4D00,100:FF2D00&height=100&section=footer&animation=fadeIn" 
    width="100%" 
  />
</p>


