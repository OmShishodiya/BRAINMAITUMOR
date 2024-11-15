
# Brain Tumor Type Detection Using AI/ML

This repository contains a project for detecting different types of brain tumors using AI/ML. It leverages several Python libraries for machine learning and data processing and a Flask-based backend to connect the model with a web frontend.

---

## Table of Contents

- [Project Overview](#project-overview)
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Usage](#usage)
- [Model Training](#model-training)
- [Contributing](#contributing)
- [License](#license)

---

## Project Overview

This AI/ML project is designed to classify brain tumor images into types using a convolutional neural network (CNN) implemented in TensorFlow. The project includes a web-based interface for users to upload MRI images, which are then processed by the trained model to detect and identify the type of tumor.

Supported tumor types include:

- Glioma
- Meningioma
- No Tumor
- Pituitary Tumor

The goal of this project is to aid in quick and accurate diagnosis of brain tumors.

---

## Features

- **Tumor Type Detection**: Classifies uploaded MRI images into tumor types.
- **User-Friendly Interface**: A web-based frontend allows users to upload images easily.
- **Real-Time Detection**: After uploading, the system provides immediate results for tumor type.
- **Model Training Pipeline**: Allows retraining the model with additional datasets.
- **Visualizations**: Displays relevant metrics and visualizations of model performance.

---

## Technologies Used

**Backend**:
- **TensorFlow**: For building and training the neural network model.
- **OpenCV**: For image processing and pre-processing tasks.
- **Pandas** and **NumPy**: For data manipulation and handling.
- **Flask**: For connecting the model with the frontend.

**Frontend**:
- **HTML**, **CSS**, **JavaScript**: For creating a responsive and user-friendly interface.

---

## Project Structure

```plaintext
├── app.py                    # Main Flask app
├── model/
│   ├── model.h5              # Trained model file
│   ├── training_data/        # Dataset used for training
├── static/
│   ├── css/                  # Stylesheets
│   ├── js/                   # JavaScript files
├── templates/
│   ├── index.html            # Homepage
├── uploads/                  # Folder for storing uploaded images
├── trainset/                 # Folder for storing training dataset with subfolders for each tumor type
├── requirements.txt          # List of dependencies
└── README.md                 # Project documentation
```

---

## Installation

To set up this project locally:

1. **Clone the Repository**  
   ```bash
   git clone https://github.com/OmShishodiya/Brain-Tumor-Detection.git
   cd Brain-Tumor-Detection
   ```

2. **Create and Activate a Virtual Environment**  
   ```bash
   python -m venv venv
   source venv/bin/activate   # On Windows, use 'venv\Scripts\activate'
   ```

3. **Install Dependencies**  
   ```bash
   pip install -r requirements.txt
   ```

4. **Run the Flask Application**  
   ```bash
   python app.py
   ```

5. **Open in Browser**  
   Go to `http://127.0.0.1:5000` to use the app.

---

## Usage

1. **Upload an Image**: On the homepage, upload an MRI image.
2. **Detection**: The uploaded image is processed, and the detected tumor type is displayed.
3. **Result**: The result displays the predicted tumor type, with options to upload another image or retrain the model with new data.

---

## Model Training

The model is a CNN built with TensorFlow. The dataset used for training includes labeled MRI images categorized by tumor types. You can train the model with additional data by adding images to the `trainset/` folder, organized in subfolders by tumor type.

To retrain the model, run the training script (if available) or modify `app.py` to initiate training when new data is added.

### Training Example (for a custom script)

```bash
python train_model.py
```

---

## Contributing

Contributions are welcome! Please open an issue or submit a pull request with your improvements.

1. Fork the repository
2. Create a new branch for your feature (`git checkout -b feature-branch`)
3. Commit your changes (`git commit -m 'Add some feature'`)
4. Push to the branch (`git push origin feature-branch`)
5. Open a pull request

---

## License

This project is licensed under the MIT License.
