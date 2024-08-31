# Custom Network Intrusion Detection System (NIDS)

## Project Overview
This project aims to create a custom Network Intrusion Detection System (NIDS) that can detect various types of network attacks, such as Denial of Service (DoS), port scanning, and unauthorized access, by analyzing network traffic data. The system uses a machine learning model trained on a dataset of labeled network traffic to identify suspicious patterns.

## Installation

### Steps to Set Up the Project Locally

1. Clone the repository and navigate to the project directory.
2. Create a virtual environment:
   ```bash
   python -m venv venv
## Activate it:

bash
Copy code
.\venv\Scripts\activate
## Install the required Python libraries using the requirements.txt file:

bash
Copy code
pip install -r requirements.txt
## If you encounter activation issues, use PowerShell to give access with the following commands:

powershell
Copy code
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned
powershell
Copy code
Unblock-File V:\Github\Custom_NIDS_with_ML.\venv\Scripts\Activate.ps1
powershell
Copy code
Invoke-Command -ScriptBlock {V:\Github\Custom_NIDS_with_ML.\venv\Scripts\activate}
powershell
Copy code
V:\Github\Custom_NIDS_with_ML.\venv\Scripts\activate.bat
Add a database CSV file to your project.

## Setting Up the Dataset
To get started, you'll need to download the dataset and place it in a data/ folder within your project directory. Follow these steps:

### For the NSL-KDD dataset:

Download the NSL-KDD dataset from the Kaggle website.
Extract the downloaded zip file to a folder named data within your project directory.
Rename the dataset file to NSL-KDD.csv for simplicity.

### For the CICIDS2017 dataset:

Download the CICIDS2017 dataset from the Canadian Institute for Cybersecurity website.
Extract the downloaded zip file to a folder named data within your project directory.
Rename the dataset file to CICIDS2017.csv for simplicity.
Once you've downloaded and placed the dataset in the data/ folder, you can modify the load_data function to load the dataset correctly.

## Model Details
Details about the machine learning model, including the training process and evaluation metrics, will be documented here.

## Limitations
Any known limitations or potential future improvements can be noted in this section.

Note: VS Code needs to run in admin mode for some features to function correctly.

## Real-Time Intrusion Detection
### Network Traffic Capture
scapy requires access to network interfaces, which might require administrative privileges.
Ensure no other process is using the network interface that could interfere with packet capture.
### Simulating Network Traffic
You can use tools like nmap to generate traffic for testing your NIDS.
For example, in a separate terminal window, you can run:
nmap -sS <your_local_ip>
This will simulate a SYN scan, and your NIDS should detect it as a potential intrusion.
### Thank you for using this NIDS project!
