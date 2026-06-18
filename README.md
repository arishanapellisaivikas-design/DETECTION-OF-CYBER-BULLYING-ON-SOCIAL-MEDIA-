# Detection of Cyberbullying on Social Media Using Machine Learning & NLP

A Machine Learning and Natural Language Processing (NLP) based web application that detects offensive and cyberbullying content on social media posts. The system analyzes user text using trained ML models and classifies content as offensive or non-offensive.

---

## Features

* Cyberbullying and offensive text detection
* NLP-based text preprocessing
* TF-IDF feature extraction
* Multiple ML model comparison
* Sentiment classification system
* User registration and login
* Offensive user monitoring
* Django-based web interface
* MySQL database integration

---

## Technologies Used

### Programming & Frameworks

* Python
* Django 2.1.7

### Machine Learning & NLP

* Scikit-learn
* NLTK
* TF-IDF Vectorization

### Database

* MySQL

### ML Algorithms

* Support Vector Machine (SVM)
* AdaBoost Classifier
* SGD Classifier
* Naive Bayes

---

## Project Architecture

```text
User Input
    |
    v
Text Preprocessing (NLP)
    |
    v
TF-IDF Vectorization
    |
    v
ML Classification Models
    |
    v
Cyberbullying Detection Result
```

---

## NLP Processing Pipeline

The system performs:

* Tokenization
* Stopword removal
* Punctuation removal
* Stemming
* Lemmatization
* TF-IDF vectorization

---

## Installation

### Clone Repository

```bash
git clone https://github.com/YOUR_USERNAME/cyberbullying-detection.git
cd cyberbullying-detection
```

---

## Install Dependencies

```bash
pip install numpy==1.19.2
pip install pandas==0.25.3
pip install matplotlib==3.1.1
pip install PyMySQL==0.9.3
pip install nltk==3.4.5
pip install scikit-learn==0.22.2.post1
pip install Django==2.1.7
```

---

## Database Setup

### MySQL Configuration

```sql
drop database bullying;

create database bullying;
use bullying;

create table register(
    username varchar(30) primary key,
    password varchar(30),
    contact varchar(12),
    email varchar(30),
    address varchar(40),
    status varchar(200)
);

create table post(
    username varchar(30),
    msg_id varchar(50),
    message varchar(300),
    image_name varchar(100),
    sentiment varchar(100),
    message_type varchar(100),
    msg_date varchar(50)
);

create table userstatus(
    username varchar(50),
    offensive_count int
);
```

---

## Run the Project

### Start Django Server

```bash
python manage.py runserver
```

Open in browser:

```text
http://127.0.0.1:8000
```

---

## Dataset

The project uses labeled social media datasets containing:

* Offensive posts
* Non-offensive posts
* Social media text samples

Datasets are processed using NLP techniques before training ML models.

---

## Machine Learning Models

The following models were trained and evaluated:

| Model          | Purpose                      |
| -------------- | ---------------------------- |
| AdaBoost       | Classification               |
| SGD Classifier | Linear classification        |
| Naive Bayes    | Probabilistic classification |
| SVM            | Offensive content detection  |

---

## Sample Prediction

Input:

```text
you bitch go to hell
```

Output:

```text
Offensive Content Detected
```

---

## Future Enhancements

* Deep Learning integration
* Real-time social media monitoring
* Toxicity severity scoring
* Image-based cyberbullying detection
* Admin analytics dashboard
* Live sentiment tracking

---

## Author

**Yashwanth Guvva**

* GitHub: [https://github.com/yashwanth-kiran89](https://github.com/yashwanth-kiran89)
* Email: [guvvayeshwanth@gmail.com](mailto:guvvayeshwanth@gmail.com)

---

## License

This project is developed for educational and research purposes.
