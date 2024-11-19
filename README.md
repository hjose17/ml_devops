# Breast Cancer Machine Learning Project

This project uses machine learning to classify breast cancer tumors as malignant or benign based on the Breast Cancer dataset from sklearn. The goal of this project is to demonstrate the entire machine learning lifecycle, including model training, saving the model, configuration management, and integration into a DevOps pipeline using Jenkins, Docker, and AWS.

---

## Table of Contents

- [Project Overview](#project-overview)
- [Technologies Used](#technologies-used)
- [Installation](#installation)
- [Usage](#usage)
- [Model Details](#model-details)
- [DevOps Pipeline](#devops-pipeline)
- [Contributing](#contributing)
- [License](#license)

---

## Project Overview

The Breast Cancer Machine Learning Project aims to classify breast cancer tumors as malignant or benign using the RandomForestClassifier from scikit-learn. The dataset is split into training and testing sets, and the model is evaluated based on accuracy.

Key functionalities:
- Load and preprocess the Breast Cancer dataset.
- Train a RandomForest model.
- Save the trained model and configuration to files (`model.pkl` and `config.yaml`).
- Integrate the model with Jenkins for testing, Docker for containerization, and AWS for deployment.

---

## Technologies Used

- **Python 3** – Main programming language.
- **scikit-learn** – For training the machine learning model.
- **pandas** – For data manipulation.
- **yaml** – For configuration management.
- **pickle** – For saving the trained model.
- **Jenkins** – For continuous integration and testing.
- **Docker** – For containerization of the application.
- **AWS** – For deployment.

---

## Installation

Follow these steps to set up the project on your local machine or in a cloud environment like Google Colab.

1. Clone the repository:
    ```bash
    git clone https://github.com/your-username/breast-cancer-ml.git
    cd breast-cancer-ml
    ```

2. Install required Python libraries:
    ```bash
    pip install -r requirements.txt
    ```

---

## Usage

1. **Train the Model**: To train the model and save it along with the configuration, run `train.py`:
    ```bash
    python train.py
    ```

    This will:
    - Train the model using the Breast Cancer dataset.
    - Save the model to `model.pkl`.
    - Save the configuration to `config.yaml`.

2. **Test the Model**: To test the model or evaluate the performance, run the `test_model.py` script:
    ```bash
    python test_model.py
    ```

---

## Model Details

The machine learning model used is a **RandomForestClassifier**. The model is trained on the Breast Cancer dataset provided by **scikit-learn**.

- **Model Parameters**:
    - `n_estimators=100` (Number of trees in the forest)
    - `max_depth=5` (Maximum depth of the trees)
    - `random_state=42` (Seed for reproducibility)

The model is evaluated on accuracy, which is printed after the evaluation.

---

## DevOps Pipeline

This project integrates with the following DevOps tools:
1. **Jenkins**: To run unit tests and trigger training on each code change.
2. **Docker**: The project is containerized so that it can be deployed in any environment with Docker.
3. **AWS**: Once Dockerized, the application is ready for deployment on AWS using services like EC2 or Elastic Beanstalk.

---

## Contributing

Contributions are welcome! To contribute to this project:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Make your changes and commit them (`git commit -am 'Add new feature'`).
4. Push to the branch (`git push origin feature-branch`).
5. Open a pull request with a description of your changes.

---

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
