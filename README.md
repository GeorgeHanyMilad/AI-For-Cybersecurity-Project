<h1 align="center">
    <img src="https://readme-typing-svg.herokuapp.com/?font=Righteous&size=35&color=00BFFF&center=true&vCenter=true&width=700&height=100&duration=7000&lines=Hello+Everyone+👋;I+hope+this+project+is+useful+to+you+❤;" />
</h1>

<p align="center">
  <img src="https://adcy.io/wp-content/uploads/2020/04/anti-hacking.gif" alt="Anti Hacking GIF" width="600" />
</p>
<br>

# Malicious URLs Detection Model

This project involves creating a machine learning model to detect malicious URLs based on various features extracted from the URLs. The model classifies URLs into four categories: benign, defacement, phishing, and malware.

## Table of Contents
1. [Project Overview](#project-overview)
2. [Steps Involved](#steps-involved)
3. [Technologies Used](#technologies-used)

## Project Overview
This project focuses on detecting malicious URLs by analyzing various URL features. The URL types include:
- **Benign**: Safe and legitimate URLs.
- **Defacement**: URLs pointing to defaced websites.
- **Phishing**: URLs used for phishing attacks.
- **Malware**: URLs leading to sites containing malicious software.
<br>

## Steps Involved

### 1. Data Loading and Understanding
- Import necessary libraries (e.g., Pandas, Scikit-learn, etc.) for data manipulation and visualization.
- Load the dataset and inspect it for missing values, data types, and structure.

### 2. Data Cleaning
- Remove the "www." prefix from the URLs for uniformity.
- Handle missing values by removing rows with missing data.

### 3. Feature Engineering
Several features are extracted from the URLs, including:
- **URL length**: The total number of characters in the URL.
- **Count of special characters**: The number of special characters in the URL.
- **Number of words**: The number of words in the URL.
- **Presence of suspicious words**: Such as 'login', 'admin', etc.
- **Presence of abnormal URLs**: URLs with uncommon patterns.
- **Protocol security**: HTTP or HTTPS.
- **Count of digits and letters**: The number of digits and alphabetic characters.
- **Count the number of characters**: This can be a separate feature to count all the characters, including letters, digits, and special characters.
- **URL shortening services**: Identifying URLs from shortening services (e.g., bit.ly).
- **Check for IP address in the link**: Determine if the URL contains an IP address instead of a domain name.

### 4. Data Visualization
- Visualize the distribution of different URL types (benign, defacement, phishing, malware).
- Visualize suspicious words, abnormal URLs, and protocol security using pie charts.

### 5. Encoding Labels
- Convert the target labels (type) into numerical values using label encoding:
  - **benign = 0**
  - **defacement = 1**
  - **phishing = 2**
  - **malware = 3**

### 6. Model Training and Evaluation
- Split the dataset into training and testing sets.
- Train a machine learning model (e.g., Random Forest or Gradient Boosting) to classify URLs into one of the four types.
- Evaluate the model using various metrics such as accuracy, confusion matrix, precision, recall, and F1 score.

### 7. Model Saving
- Save the trained model using **joblib** for future use in detecting malicious URLs.

## Technologies Used
- Python
- Pandas
- Scikit-learn
- Matplotlib
- Seaborn
- Joblib
