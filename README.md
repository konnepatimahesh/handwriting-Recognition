# handwriting-Recognition

WriteID is a handwriting verification system that leverages deep learning to match and verify handwriting samples. This project includes a Flask-based backend for model inference and a frontend interface for user interaction.

# Features

1.Handwriting Matching: Compares two handwriting samples to determine similarity.

2.Handwriting Verification: Authenticates handwriting against stored records.

3.Preprocessing Module: Cleans and prepares handwriting images for model input.

4.Deep Learning Model: Trained for handwriting verification.

5.Web-Based UI: Frontend for users to upload and verify handwriting samples

# Project Structure

WriteID/
│── backend/
│   ├── models/               # Trained models
│   ├── uploads/              # Folder to store uploaded images
│   ├── app.py                # Flask server for API
│   ├── handwriting_match.py  # Handwriting matching logic
│   ├── model_train.py        # Model training script
│   ├── preprocess.py         # Preprocessing module
│   ├── requirements.txt      # Required dependencies
│   ├── verify.py             # Handwriting verification module
│
│── datasets/
│   ├── train/                # Training dataset
│   ├── test/                 # Test dataset
│   ├── labels.csv            # Labels for dataset
│
│── frontend/
│   ├── first.html            # Landing page
│   ├── home.html             # Main UI
│   ├── second.html           # Additional page
│   ├── upload.html           # File upload interface
│   ├── script.js             # JavaScript for API calls
│   ├── style.css             # Stylesheet for UI
│
│── saved_model/              # Stored model files
│── uploads/                  # Temporary file storage
│
│── venv/                     # Python virtual environment
│── label_map.pkl             # Label mapping for classification
│── preprocessed_data.pkl      # Preprocessed dataset
│── writeid_model.h5           # Trained deep learning model
│── pyenv.cfg                  # Virtual environment config
│
└── README.md                 # Project documentation
# Installation & Setup
Prerequisites
Ensure you have Python 3.8+ installed.

# Steps

1.Clone the repository:
   git clone https://github.com/yourusername/WriteID.git
   cd WriteID  
2.Set up a virtual environment:
   python -m venv venv
   source venv/bin/activate  # For Linux/Mac
   venv\Scripts\activate     # For Windows
3.install dependencies
  pip install -r requirements.txt
4.Run the Flask server
  python backend/app.py
5.Open the frontend in a browser:
  http://127.0.0.1:5000

# Usage

Upload a handwriting sample via the web UI.

The system preprocesses and verifies the handwriting.

The result is displayed with similarity scores.

Model Training

To train the model on new handwriting data:

python backend/model_train.py

Ensure the datasets/train/ directory contains labeled handwriting samples.

