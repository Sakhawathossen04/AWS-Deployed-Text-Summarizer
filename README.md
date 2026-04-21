# End-to-End Text Summarization System (PEGASUS + FastAPI + AWS)

## Project Overview

This project presents a production-ready End-to-End Natural Language Processing system for Text Summarization. The objective is to transform long textual content such as articles, documents, or dialogues into concise summaries while preserving the essential meaning and context.

The system utilizes the PEGASUS Transformer model (`google/pegasus-cnn_dailymail`) from Hugging Face and is fine-tuned on the SAMSum dataset to generate high-quality abstractive summaries.

---

## Key Features

* Modular and scalable architecture for clean code management
* Automated training and inference pipelines
* FastAPI-based web application for real-time summarization
* Containerized deployment using Docker
* CI/CD pipeline using GitHub Actions
* Cloud deployment on AWS (EC2 and ECR)

---

## Model Details

* Model: PEGASUS (Google)
* Framework: Hugging Face Transformers
* Dataset: SAMSum (Dialogue Summarization)
* Task: Abstractive Text Summarization

---

## Tech Stack

### Programming Language

* Python 3.8

### Libraries and Frameworks

* Hugging Face Transformers
* PyTorch
* NLTK
* Pandas
* FastAPI
* LangChain

### Cloud and DevOps

* AWS (EC2, ECR)
* Docker
* GitHub Actions

---

## Project Architecture

```
├── config/
├── src/
│   ├── components/
│   ├── pipeline/
│   ├── config/
│   └── entity/
├── app.py
├── main.py
├── params.yaml
├── config.yaml
```

---

## Project Workflow

To maintain a structured and scalable development process, the following order is followed:

1. Update `config.yaml`
2. Update `params.yaml`
3. Define Entity
4. Configure Configuration Manager
5. Develop Components
6. Build Pipeline
7. Execute `main.py`
8. Launch `app.py`

---

## Installation and Setup

### 1. Clone the Repository

```
git clone https://github.com/Sakhawathossen04/aws-deployed-text-summarizer
cd aws-deployed-text-summarizer
```

### 2. Create Virtual Environment

```
conda create -n text-summarizer python=3.8 -y
conda activate text-summarizer
```

### 3. Install Dependencies

```
pip install -r requirements.txt
```

### 4. Run the Application

```
python app.py
```

Access the application at:

```
http://localhost:8080
```

---

## AWS CI/CD Deployment

### Step 1: AWS Setup

* Create an IAM user with the following permissions:

  * AmazonEC2FullAccess
  * AmazonEC2ContainerRegistryFullAccess
* Create an ECR repository
* Launch an EC2 instance (recommended: t2.large)

---

### Step 2: EC2 Configuration

* Install Docker
* Configure the EC2 instance as a GitHub self-hosted runner

---

### Step 3: GitHub Secrets

Add the following secrets in the repository settings:

```
AWS_ACCESS_KEY_ID
AWS_SECRET_ACCESS_KEY
AWS_REGION
AWS_ECR_LOGIN_URI
ECR_REPOSITORY_NAME
```

---

## Use Cases

* News summarization
* Dialogue and chat summarization
* Research paper summarization
* Document compression systems

---

## Future Improvements

* Multilingual summarization support
* Integration with custom fine-tuned large language models
* Advanced evaluation metrics such as ROUGE and BLEU
* Scalable microservices deployment

---

## Acknowledgements

* Model: Google PEGASUS
* Dataset: SAMSum
---

## Contact

For feedback, collaboration, or contributions, feel free to connect and open issues or pull requests.
