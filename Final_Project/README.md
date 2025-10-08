# 🏀 FIBA Rules Chatbot

Welcome to the FIBA Rules Chatbot, this project lets you ask questions about basketball rules from the official FIBA 2024 rulebook and get accurate.

It’s like having a friendly basketball expert on your computer ready to explain the rules whenever you want.

## ✨ Features

- Ask questions naturally, the chatbot understands queries like “What are the rules of dribbling?”

- Accurate answers from official FIBA documents, the AI reads the PDF and gives factual responses.

- Source clarity, see which page and document chunk the answer came from.

- Interactive interface built with Gradio, so it feels like chatting with a human.

## 🛠 How It Works

- PDF Loading: The official FIBA 2024 rules PDF is downloaded and loaded.

- Text Splitting: Long pages are split into smaller chunks to fit the AI’s context window.

- Embeddings: Each chunk is converted into a vector that represents its meaning.

- Vector Store: Chroma stores all embeddings so we can quickly find relevant text for a query.

- Retriever: Finds the top relevant chunks based on your question.

- LLM (Groq LLaMA 3.1): Reads the retrieved chunks and generates a friendly, concise answer.

## 🎯 Example Usage

- Ask the bot questions like:

  - “What are the rules of dribbling?”

  - “How many fouls can a player commit?”

  - “What are the dimensions of a basketball court?”

## 🧑‍💻 Installation

### Clone the repository:

```bash
git clone https://github.com/TonyMakhoul1/LLMs.git
cd LLMs
```

### Create a virtual environment and install dependencies:
```bash
python -m venv venv
source venv/bin/activate  # Linux/macOS
venv\Scripts\activate     # Windows
pip install -r requirements.txt
```
### Configure Environment Variables

Create a .env file in the project root and add:
```bash
GROQ_API_KEY=your_api_key_here
```

Run the cells

Open the Gradio interface in your browser and start chatting!

## 💡 Tips

- Use specific questions for best answers.

- If the bot says it can’t find the answer, check the source PDF.

## ⚡ Tech Stack

- Python: main programming language

- LangChain: for connecting LLM with retrieval

- Hugging Face Embeddings: for converting text into vectors

- Chroma: local vector database

- Groq LLaMA 3.1: LLM for generating answers

- Gradio: for building the interactive chatbot
