# Multi-CSV AI Data Assistant

## Overview

Multi-CSV AI Data Assistant is a Python application that leverages **LangChain**, **OpenAI GPT-4o Mini**, and **Pandas** to answer natural language questions across multiple CSV datasets.

The application automatically downloads sample datasets from Google Drive, loads them into Pandas DataFrames, and creates a LangChain Pandas Agent capable of selecting the appropriate dataset to answer user queries.

Instead of manually searching spreadsheets, users can simply ask questions in plain English.

---

## Features

* Automatic dataset download from Google Drive
* Supports multiple CSV files simultaneously
* Natural language question answering
* Powered by OpenAI GPT-4o Mini
* Uses LangChain Pandas DataFrame Agent
* Interactive command-line chat interface
* Secure API key input using `getpass`
* Modular and beginner-friendly implementation

---

## Datasets Included

The project automatically downloads four datasets:

* SaaS Documentation
* Credit Card Terms
* Hospital Policy
* E-commerce FAQs

The AI agent determines which dataset contains the information needed to answer each question.

---

## Technologies Used

* Python 3
* Pandas
* LangChain
* LangChain Experimental
* OpenAI GPT-4o Mini
* gdown
* Requests

---

## Installation

Clone the repository:

```bash
git clone https://github.com/yourusername/multi-csv-ai-data-assistant.git
cd multi-csv-ai-data-assistant
```

Install dependencies:

```bash
pip install langchain-experimental
pip install langchain-openai
pip install pandas
pip install gdown
pip install requests==2.32.4
```

Or install everything together:

```bash
pip install langchain-experimental langchain-openai pandas gdown requests==2.32.4
```

---

## Usage

Run the Python script:

```bash
python app.py
```

Enter your OpenAI API Key when prompted.

Once initialized, ask questions such as:

```
What are the hospital visiting hours?

What is the API rate limit?

What is the annual fee for the Platinum Credit Card?

How can I return an item purchased online?
```

Type:

```
exit
```

to quit the application.

---

## Project Workflow

1. Download CSV datasets from Google Drive.
2. Load each dataset into a Pandas DataFrame.
3. Initialize the OpenAI language model.
4. Create a LangChain Pandas DataFrame Agent.
5. Accept user questions.
6. Determine the most relevant dataset.
7. Generate an answer using only the CSV data.

---

## Project Structure

```
project/
│
├── app.py
├── saas_docs.csv
├── credit_card_terms.csv
├── hospital_policy.csv
├── ecommerce_faqs.csv
├── README.md
└── requirements.txt
```

---

## Example Session

```
You:
What is the hospital visiting hour?

AI:
General visiting hours are from 10:00 AM to 8:00 PM.

------------------------------

You:
What is the API request limit?

AI:
The SaaS platform allows up to 1000 API requests per hour.
```

---

## Future Improvements

* Add PDF document support
* Support Excel and Word documents
* Add Retrieval-Augmented Generation (RAG)
* Build a Streamlit or Gradio web interface
* Integrate vector databases for semantic search
* Enable conversation memory
* Support local LLMs such as Llama and Mistral

---

## Requirements

* Python 3.10+
* OpenAI API Key
* Internet connection (for downloading datasets)

---

## License

This project is intended for educational and learning purposes. You may modify and extend it for personal or academic use.

---

## Author

Developed as a demonstration of building AI-powered data assistants using LangChain, OpenAI, and Pandas.
