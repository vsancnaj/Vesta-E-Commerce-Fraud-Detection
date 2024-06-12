# Vesta E-Commerce Fraud Detection

## Project Summary

### Introduction
This project aims to improve fraud detection systems in e-commerce, partnering with IEEE-CIS and Vesta Corporation to analyze a large dataset of real-world transactions.

### Dataset
- **Size**: 590,540 transactions, 434 features.
- **Key Features**: Transaction amount, transaction time, card details, address, distance, email domains, and various anonymized features.

### Exploratory Data Analysis
- **Transaction Amounts**: Log transformation revealed clear distinctions between fraudulent and non-fraudulent transactions.
- **Timing Patterns**: Fraudulent transactions often occurred at irregular hours.
- **Feature Importance**: PCA reduced multicollinearity, highlighting key features like 'TransactionAmt' and 'TransactionDT'.

### Challenges
- **Imbalanced Data**: The dataset exhibited a significant imbalance between fraudulent and non-fraudulent transactions, posing challenges for effective model training. Due to the many anonymous or encoded features, techniques like SMOTE were not applicable since they require knowledge of the feature meanings. Consequently, we relied heavily on comprehensive feature selection techniques and specific models capable of handling imbalanced data.
- **Feature Selection**: Choosing the most relevant features from a large set of 434 features required extensive visual analysis and dimensionality reduction techniques like PCA and Random Forest feature importance.


### Model Selection
- **Objective**: Balance recall and precision to minimize false positives and maximize fraud detection.
- **Hyperparameter Tuning**: Grid search for Random Forest, Logistic Regression, and XGBoost.
  - **Random Forest**: ROC-AUC 0.89
  - **Logistic Regression**: ROC-AUC 0.51
  - **XGBoost**: ROC-AUC 0.88

### Precision-Recall Analysis
- **Threshold Experimentation**: XGBoost maintained better stability and performance across different thresholds, chosen as the final model.

### Final Model Choice
- **Model**: XGBoost
- **Performance**: Balanced precision and recall, F1-score 0.76, overall accuracy 81%.

### Further Work
1. **Model Integration**: Explore ensembling Random Forest and XGBoost.
2. **Real-Time Deployment**: Evaluate the model in a live environment for real-time fraud detection.

This project enhances fraud detection accuracy, ensuring robust protection and minimizing disruptions for genuine users.



## Getting Started

These instructions will guide you in getting a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites

Ensure you have the following prerequisites installed and set up:

- **Python Version**: Python 3.10.12 (recommended: 3.8 or higher)
- **Libraries and Dependencies**: Ensure all necessary libraries and dependencies are installed as listed in `requirements.txt`.
- **Google Account**: Required for Google Colab.
- **Local or Cloud Environment**: Capable of running Jupyter notebooks if not using Google Colab.

### Installation

Follow these steps to set up the project environment:

1. **Clone the repository**:
    ```bash
    git clone <repository-url>
    cd <repository-name>
    ```
2. **Install required Python packages**:
    ```bash
    pip install -r requirements.txt
    ```

### Running the Notebook

#### Google Colab

If you are using Google Colab, follow these instructions:

1. Open [Google Colab](https://colab.research.google.com/).
2. Click on `File` > `Open notebook` > `GitHub tab` and paste the URL of your notebook.
3. Alternatively, click on `File` > `Upload notebook` to upload the notebook file from your local machine.
4. Follow the instructions within the notebook to mount your Google Drive if required for data access or file storage.

#### Local Jupyter Installation

If you are running the notebook locally:

1. Launch Jupyter Notebook in your environment:
    ```bash
    jupyter notebook
    ```
2. Navigate to the notebook file in the Jupyter interface that opens in your web browser and open it.
3. Run the cells in the notebook sequentially to replicate the analysis.

### Setting Up the Kaggle API and Downloading the Dataset

To utilize datasets from Kaggle for your project, you'll need to configure the Kaggle API on your system. Follow these steps:

1. **Create or Log Into Your Kaggle Account**:
    - New users can [create an account](https://www.kaggle.com/).
    - Existing users can [log in](https://www.kaggle.com/account/login).

2. **API Token Generation**:
    - Navigate to your account settings by clicking on your profile picture in the top right corner and selecting 'Account'.
    - Scroll to the 'API' section and click the 'Create New API Token' button. This downloads a file named `kaggle.json`, containing your API credentials.

3. **Setup API Token on Your System**:
    - Place the downloaded `kaggle.json` file into the directory specified in your notebook. The standard location is `~/.kaggle/` for Unix-like systems.

4. **Explore the Dataset**:
    - Visit the [IEEE Fraud Detection Kaggle Competition](https://www.kaggle.com/competitions/ieee-fraud-detection/data) page to explore and understand the dataset you'll be working with.

5. **Dataset Download and Setup**:
    - Execute the following commands in your notebook to set up the Kaggle API and download the dataset:

    ```bash
    # Create the necessary Kaggle directory
    !mkdir ~/.kaggle

    # Copy the kaggle.json file into this directory
    !cp /your/drive/kaggle.json ~/.kaggle/

    # Secure the API token by updating its permissions
    !chmod 600 ~/.kaggle/kaggle.json

    # Download the dataset from the Kaggle competition
    !kaggle competitions download -c ieee-fraud-detection

    # Unzip the downloaded dataset into the specified directory
    !unzip /content/ieee-fraud-detection.zip
    ```

By following these steps, you'll be able to securely set up the Kaggle API on your system and access the datasets required for your project.

## Authors

Valentina Sanchez <br />
[vsanchezn.cs@gmail.com](mailto:vsanchezn.cs@gmail.com)

## Acknowledgments

Inspiration, datasets, and code snippets for this project were provided by:

- [IEEE Computational Intelligence Society](https://www.kaggle.com/competitions/ieee-fraud-detection/data?select=train_identity.csv) - Source of the Kaggle dataset.
