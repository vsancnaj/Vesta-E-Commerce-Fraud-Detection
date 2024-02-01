# Vesta-E-Commerce-Fraud-Detection
In the realm of e-commerce, the fine line between security and convenience is navigated through the adept implementation of fraud prevention systems. 
As you face the inconvenience of a declined card at the checkout, it's these systems that are the unsung heroes guarding against unauthorized transactions. Partnering with IEEE-CIS, Vesta Corporation is on the forefront of refining these systems, leveraging a vast dataset from real-world transactions to benchmark machine learning models. 

## Getting Started

### Dependencies


These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites

What things you need to install the software and how to install them.

```markdown
- A Google account (for Google Colab)
- A local or cloud environment that can run Jupyter notebooks if not using Google Colab
```
### Setting Up the Kaggle API and Downloading the Dataset

To utilize datasets from Kaggle for your project, you'll need to configure the Kaggle API on your system. Follow these clear steps to get started:

1. **Create or Log Into Kaggle Account:**
   - If you're new to Kaggle, [create an account](https://www.kaggle.com/).
   - If you already have an account, simply [log in](https://www.kaggle.com/account/login).

2. **API Token Generation:**
   - Navigate to your account settings by clicking on your profile picture in the top right corner and selecting 'Account'.
   - Scroll to the 'API' section.
   - Click the 'Create New API Token' button. This action downloads a file named `kaggle.json`, which contains your API credentials.

3. **Setup API Token on Your System:**
   - Place the downloaded `kaggle.json` file into the directory specified in your notebook. The standard location is `~/.kaggle/` for Unix-like systems.

4. **Explore the Dataset:**
   - Visit the [IEEE Fraud Detection Kaggle Competition](https://www.kaggle.com/competitions/ieee-fraud-detection/data) page to explore and understand the dataset you'll be working with.

5. **Dataset Download and Setup:**
   - Use the following commands in your notebook to set up the Kaggle API and download the dataset:
   
     ```bash
     # Create the necessary Kaggle directory
     !mkdir ~/.kaggle

     # Copy the kaggle.json file into this directory
     !cp /content/drive/MyDrive/Springboard/kaggle.json ~/.kaggle/

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
vsanchezn.cs@gmail.com


## Acknowledgments

[Kaggle Dataset](https://www.kaggle.com/competitions/ieee-fraud-detection/data?select=train_identity.csv) <br /> from IEEE COMPUTATIONAL INTELLIGENCE SOCIETY

