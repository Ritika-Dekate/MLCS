# 🔐 Real-Time Phishing URL Detection Using ML on User Browsing Data

## 📌 Problem Overview
The domain of cybersecurity focuses on protecting users from online threats such as phishing, malware, and identity theft.  
Phishing attacks involve creating fake websites that mimic legitimate services (e.g., banking, email, e-commerce) to steal sensitive user information like login credentials and financial details.

These phishing websites are often short-lived and frequently change their URL structures, making traditional blacklist-based detection systems ineffective.  
Therefore, an adaptive machine learning–based approach is required to analyze URL patterns and detect phishing websites in real time as users access them on a normal personal computer.

---

## 🎯 Problem Statement
**Develop a machine learning model that classifies URLs as phishing or legitimate in real time with high accuracy, using URL-based features and continuously collected data from user inputs and synthetic phishing URL generation, to provide early warnings and reduce user exposure to fraudulent websites.**

### This Statement:
- Defines the task: Binary classification of URLs (phishing vs legitimate)  
- Outlines the success criteria: High accuracy and low false positives  
- Links to goals: User safety, automated phishing detection, real-time protection  

---

## 📥 Input Data Requirements

### 🔹 Data Needed
- URL-based lexical features:
  - URL length  
  - Number of dots  
  - Presence of IP address  
  - Special characters  
  - Suspicious keywords (e.g., "login", "verify", "secure")  
- Structural features:
  - Number of subdomains  
  - Use of HTTPS  
- Optional behavioral features:
  - Frequency of similar URL patterns over time  

### 🔹 Data Format
- CSV file with columns:

### 🔹 Data Sources (Own Dataset Creation)
- Real-time URLs collected from user input on a normal PC  
- Synthetic phishing-like URLs generated using predefined phishing patterns and non-existent domains (.test, .example)  
- Legitimate URLs collected from normal browsing activity  

### 🔹 Bias & Privacy Considerations
- Ensure balanced data between phishing and legitimate URLs  
- Avoid collecting any personal information other than the URL string  
- Generate diverse synthetic URLs using multiple brand names, keywords, and domain patterns to reduce bias  

---

## 📤 Output Requirements

### 🔹 Output Format
- Binary classification:
- `1 → Phishing`  
- `0 → Legitimate`  

### 🔹 Evaluation Metrics
- Accuracy  
- Precision (to reduce false positives)  
- Recall (to detect phishing effectively)  
- F1-score  

### 🔹 Interpretability
- Feature importance scores from tree-based models  
- Explanation of key URL patterns contributing to phishing detection  

### 🔹 Real-Time Performance
- Fast prediction time (< 1 second per URL)  
- Immediate user feedback (Safe / Phishing warning)  

---

## ⚙️ Constraints, Assumptions & Ethics

### 🔹 Constraints
- Real-time prediction required on a normal PC  
- Limited availability of real phishing URLs initially  
- No heavy web scraping or website content analysis  
- No interaction with real phishing websites  

### 🔹 Assumptions
- URL lexical patterns are sufficient for phishing detection  
- User-provided URLs represent real-world browsing behavior  
- Synthetic phishing URLs mimic realistic phishing patterns  

### 🔹 Ethical Considerations
- All synthetic URLs use non-existent domains  
- False positives are minimized to avoid blocking legitimate websites  
- No personal or sensitive user data is collected  

---

## ✅ Feasibility and Impact

### 🔹 Feasibility
- Lightweight ML models (Logistic Regression, Random Forest) can run on a normal PC or Google Colab  
- Synthetic dataset generation allows controlled expansion of training data  
- Real-time URL input requires minimal system resources  

### 🔹 Impact
- Helps users avoid phishing websites in real time  
- Reduces dependency on static blacklists  
- Demonstrates practical ML application in cybersecurity  
- Can be extended to browser extensions or email filtering systems  

---

## 🧠 Machine Learning Approach
- Type: Supervised Learning (Binary Classification)  
- Models:
- Logistic Regression (baseline)
- Random Forest (primary model)

---

## 🚀 Future Scope
- Integration with browser extensions  
- Online learning with continuous retraining  
- Support for email phishing detection  
- Addition of content-based features (HTML analysis)

---
