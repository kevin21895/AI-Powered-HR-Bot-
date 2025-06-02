# 🤖 AI-Powered HR Assistant for Nestlé

A user-friendly chatbot that answers HR-related queries from Nestlé employees by referencing information extracted from official HR policy PDF documents.

---

## 🔧 Tools & Technologies

- **[LangChain](https://python.langchain.com/)** – for managing documents, embeddings, and retrieval chains  
- **[OpenAI GPT-3.5 Turbo](https://platform.openai.com/)** – for generating human-like responses  
- **[Gradio](https://gradio.app/)** – to create an interactive web-based chat interface  
- **[PyPDFLoader](https://python.langchain.com/docs/modules/data_connection/document_loaders/pdf/)** – to load and extract text from PDFs  
- **[FAISS](https://github.com/facebookresearch/faiss)** / **Chroma** – for fast vector similarity search

---

## 🧠 How It Works

1. **Load PDF**  
   Nestlé’s HR policy document is loaded using PyPDFLoader.

2. **Text Chunking and Embedding**  
   The document is split into manageable chunks using `RecursiveCharacterTextSplitter`, and vector embeddings are created using OpenAI Embeddings.

3. **Question Answering Chain**  
   A retrieval-based QA chain uses the GPT-3.5 Turbo model and returns answers based on the most relevant document chunks using FAISS or Chroma vector search.

4. **Prompt Engineering**  
   Prompts are crafted to instruct GPT to respond professionally in English, strictly using the retrieved document context.

5. **Chatbot Interface with Gradio**  
   The chatbot interface allows users to enter queries and get responses in real time. The session maintains chat history and times out after 10 minutes of inactivity.

---

## 🚀 Features

- Welcomes users with:  
  `"Welcome to Nestlé’s HR BOT. Ask me anything."`
- Retrieves relevant HR document snippets based on questions
- Generates accurate, professional answers using GPT-3.5 Turbo
- Maintains chat history during each session
- User-friendly and accessible via web browser

---

## 📁 Project Structure

```plaintext
nestle_hr_chatbot/
├── the_nestle_hr_policy.pdf
├── chatbot.ipynb
├── README.md
└── requirements.txt
```

---

## ✅ Getting Started

1. **Clone the repository**
   ```bash
   git clone https://github.com/your-username/nestle-hr-chatbot.git
   cd nestle-hr-chatbot
   ```

2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Set up your OpenAI API key**
   ```python
   import openai
   openai.api_key = "your_api_key"
   ```

4. **Run the notebook**  
   Launch the Jupyter Notebook and run `chatbot.ipynb`

---

## 📃 License

This project is for educational and demonstration purposes.
