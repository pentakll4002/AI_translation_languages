# 🌐 AI Translation Languages

This project provides a simple and efficient API for translating text between languages using FastAPI, LangChain, and Groq's large language model (`Qwen-Qwq-32b`).

---

## 🚀 Technologies Used

- [FastAPI](https://fastapi.tiangolo.com/) – high-performance web framework for building APIs with Python
- [LangChain](https://www.langchain.com/) – framework for building language model-powered applications
- [Groq (ChatGroq)](https://groq.com/) – LLM provider powering high-speed model inference
- [LangServe](https://github.com/langchain-ai/langserve) – easily expose LangChain chains as APIs
- [Dotenv](https://pypi.org/project/python-dotenv/) – for loading environment variables

---

## 📦 Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/ai-translation-languages.git
cd ai-translation-languages
```

### 2. Create a .env File
```venv
GROQ_API_KEY=your_groq_api_key
```

### 3. Install Dependencies
```bash
pip install -r requirements.txt
```

### 4. Run the API Server
```bash
uvicorn main:app --reload
```
Server will be available at: http://127.0.0.1:8000

## 🧠 How It Works
- A translation prompt is built using ChatPromptTemplate

- The model (Qwen-Qwq-32b) processes the input and returns a translated version

- The result is returned as plain text using StrOutputParser

## 🌐 Example API Route
If you're using LangServe, the API will expose a route like:

```http
POST /langchain/predict
```
With a JSON body:

```json
{
  "input": {
    "text": "Hello, how are you?",
    "target_language": "Vietnamese"
  }
}
```

## 🛡️ CORS Support
The API is CORS-enabled, so it can be consumed from frontend applications (React, Vue, etc.).

## 📄 License
MIT License

```yaml
---
Let me know if you also want a `requirements.txt` or sample `main.py` for the FastAPI app setup!
```







