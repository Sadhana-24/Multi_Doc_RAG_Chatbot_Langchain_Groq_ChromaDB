# Multi-Document RAG Chatbot

This project is a Multi-Document Retrieval-Augmented Generation (RAG) Chatbot built with Streamlit, LangChain, and Groq using Llama 3.3-70b Versatile as the LLM. It answers questions based on uploaded documents and maintains chat history for contextual follow-up questions.

---

## Features

- Multi-Document Retrieval with Chroma Vector Store
- Conversational Memory for contextual Q&A
- Powered by Llama 3.3-70b Versatile via Groq
- Streamlit UI for interactive chat

---

## Requirements

- Python 3.8 or higher
- libmagic (for file type detection)

---

## Installation

1. Clone the Repository:
    ```bash
    git clone https://github.com/your-username/multi-doc-chatbot.git
    cd multi-doc-chatbot
    ```

2. Create Virtual Environment (Optional):
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows: venv\Scripts\activate
    ```

3. Install Dependencies:
    ```bash
    pip install -r requirements.txt
    ```

4. Install libmagic:
    - On Ubuntu/Debian:
        ```bash
        sudo apt install libmagic1
        ```
    - On MacOS:
        ```bash
        brew install libmagic
        ```
    - On Windows:
        - Install via [GnuWin32](http://gnuwin32.sourceforge.net/packages/file.htm) or use Windows Subsystem for Linux (WSL).

---

## Configuration

1. Get Groq API Key from [Groq Console](https://console.groq.com).
2. Add API Key to `config.json`:
    ```json
    {
      "GROQ_API_KEY": "your_groq_api_key_here"
    }
    ```

---

## Vectorize Documents

1. Place documents in the `data` directory.
2. Run the vectorization script:
    ```bash
    python vectorize_documents.py
    ```

---

## Run the Chatbot

```bash
streamlit run main.py
