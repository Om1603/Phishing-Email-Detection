# Phishing Email Detection System

This project is a machine learning-based system designed to detect phishing emails by analyzing email content. The model is trained using a logistic regression algorithm and can classify emails as either "Phishing" or "Safe." The project is intended for use within Google Colab, and the trained model is provided as a `.pkl` file for easy reuse.

## Features

- **Email Content Analysis:** Automatically detects phishing attempts based on email content.
- **Machine Learning Model:** Trained with logistic regression for high accuracy.
- **Model Reusability:** Includes pre-trained `.pkl` files for quick deployment.

## Getting Started

### Prerequisites

- Google Colab
- Basic knowledge of Python and machine learning

### Installation

1. Clone this repository:
    ```bash
    git clone https://github.com/yourusername/phishing-email-detection.git
    ```
2. Open the `phishing_email_detection.ipynb` notebook in Google Colab.

### Usage

1. Load the provided `.pkl` file to use the pre-trained model:
    ```python
    import joblib
    model = joblib.load('phishing_model.pkl')
    vectorizer = joblib.load('vectorizer.pkl')
    ```
2. Transform new email data using the vectorizer:
    ```python
    new_email = ["Your account has been compromised. Please click here to verify."]
    new_email_transformed = vectorizer.transform(new_email)
    ```
3. Predict if the email is phishing:
    ```python
    prediction = model.predict(new_email_transformed)
    print("Predicted class:", prediction)
    ```

### Project Structure

- **`phishing_email_detection.ipynb`:** The main notebook containing data loading, model training, and evaluation.
- **`phishing_model.pkl`:** The trained logistic regression model.
- **`vectorizer.pkl`:** The vectorizer used to transform email text into features.

### Screenshots

- ![image](https://github.com/user-attachments/assets/3007f773-c309-4da4-b990-95785f022129)
- ![image](https://github.com/user-attachments/assets/c179ac31-7989-4be5-8c6c-dd92ee31f000)



### Contributing

Feel free to fork this repository and submit pull requests. Contributions are welcome!

### License

This project is licensed under the MIT License.

