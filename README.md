# 📚 RAG Q&A Conversation With PDF Uploads and Chat History

This project is an **end-to-end Conversational Retrieval-Augmented Generation (RAG)** system that allows users to upload **PDF documents** and ask questions based on the document content. The system remembers past interactions using **chat history**, improving multi-turn dialogue accuracy.

Built using **LangChain**, **Streamlit**, **Groq LLMs**, and **ChromaDB**, it showcases how to implement a document-aware, session-based chatbot using modern LLM infrastructure.

## 📁 Project Structure

```
RAG-Q-A-Conversation.../           # ✅ Main RAG Q&A Project
├── .env                           # HuggingFace token (environment variables)
├── .gitignore                     # Git ignore file
├── app.py                         # Main Streamlit app for RAG Q&A with chat history
├── README.md                      # 📘 Project documentation
└── requirements.txt               # Required Python libraries
```

## 🚀 Features

* 🗂️ Upload one or multiple PDF files
* 🔍 Ask questions about the content in natural language
* 🧠 Uses Retrieval-Augmented Generation for accurate context-based answers
* 💬 Maintains **session-based chat history** using `RunnableWithMessageHistory`
* 📚 Reformulates questions based on chat history (history-aware retriever)
* 🤖 Powered by **Groq LLM (Gemma-2-9b-IT)** and **MiniLM embeddings**
* 🌐 Simple and interactive UI built using **Streamlit**

## 🛠️ Tech Stack & Tools

| Tool / Library | Purpose |
|---|---|
| `Streamlit` | Frontend UI |
| `LangChain` | RAG pipeline, prompts, history |
| `Groq` + `ChatGroq` | Fast LLM inference (Gemma 2 9B) |
| `HuggingFaceEmbeddings` | Embeddings via MiniLM |
| `Chroma` | In-memory vector database |
| `PyPDFLoader` | Load PDFs as LangChain docs |
| `RecursiveCharacterTextSplitter` | Chunking long documents |
| `dotenv` | API key management |

## 🧪 How It Works

1. **User uploads PDF(s)**
2. Documents are loaded and split into chunks
3. Embeddings are created using `all-MiniLM-L6-v2`
4. Chunks are stored in a Chroma vector store
5. Questions are reformulated using chat history (`history-aware retriever`)
6. Final answers are generated using the RAG pipeline
7. Chat history is saved session-wise

## 🖼️ Screenshots

*Add screenshots of the following:*

* 💬 Asking a question
* 📜 Displaying answer and chat history
* 📊 Displaying langsmith results

You can add images like this:

```markdown
![Chat Interface](screenshots/1.png)
![Chat Interface](screenshots/3.png)
![Chat Interface](screenshots/2.png)


```

## 🔐 Environment Setup

1. Clone the repo:

```bash
git clone https://github.com/yourusername/your-repo-name.git
cd your-repo-name
```

2. Install dependencies:

```bash
pip install -r requirements.txt
```

3. Create a `.env` file with your Hugging Face token:

```env
HF_TOKEN=your_huggingface_token
```

4. Run the app:

```bash
streamlit run app.py
```

## 📌 Requirements

* Python 3.8+
* Streamlit
* LangChain
* Groq API Key (you will input it in the app)
* HuggingFace Token for embeddings

## 📈 Example Use Cases

* Ask questions from academic research papers
* Query legal documents or contracts
* Summarize multi-page policy documents
* Interactive reading assistant for students

## 🧠 Future Improvements

* Add source document references with answers
* Allow multiple session management
* Integrate other LLM providers (OpenAI, Anthropic, etc.)
* UI enhancements for chat layout

## 👨‍💻 Author

Built with ❤️ using modern LLM and RAG technologies.