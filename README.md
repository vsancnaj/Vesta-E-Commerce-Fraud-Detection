# Vesta-E-Commerce-Fraud-Detection

In the realm of e-commerce, navigating the fine line between security and convenience is crucial, and it's the adept implementation of fraud prevention systems that make it possible. As you face the inconvenience of a declined card at checkout, remember that these systems are the unsung heroes guarding against unauthorized transactions. Vesta Corporation, in partnership with IEEE-CIS, is at the forefront of refining these systems. They leverage a vast dataset from real-world transactions to benchmark machine learning models, ensuring your transactions are secure and seamless.

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
