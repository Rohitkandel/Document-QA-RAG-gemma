# Document Q&A System

This project is a Streamlit-based application that allows users to ask questions about documents and receive AI-powered answers. It utilizes document embedding, vector storage, and language models to provide accurate responses based on the content of uploaded PDF files.

## Features

- PDF document loading and processing
- Text embedding using Google's Generative AI
- Vector storage with FAISS for efficient retrieval
- Question answering using the Gemma-7b-it model via Groq
- Interactive Streamlit interface for easy user interaction

## Installation

1. Clone this repository:
2.  Install the required packages
3.  Set up your environment variables:
Create a `.env` file in the root directory and add your API keys:
GROQ_API_KEY=your_groq_api_key
GOOGLE_API_KEY=your_google_api_key

## Usage

1. Place your PDF documents in the `./pdffiles` directory.

2. Run the Streamlit app.

3. Open your web browser and go to the URL provided by Streamlit (usually `http://localhost:8501`).

4. Click the "Documents Embedding" button to process and embed the documents.

5. Enter your question in the text input field and press Enter to get an answer.

## How it Works

1. The system loads PDF documents from the specified directory.
2. It splits the documents into smaller chunks and creates vector embeddings using Google's Generative AI.
3. The embeddings are stored in a FAISS vector database for quick retrieval.
4. When a user asks a question, the system retrieves the most relevant document chunks.
5. The Gemma-7b-it model, accessed via Groq, generates an answer based on the retrieved chunks and the user's question.

## Dependencies

- streamlit
- langchain
- faiss-cpu
- PyPDF2
- python-dotenv
- langchain_groq
- langchain_google_genai

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
