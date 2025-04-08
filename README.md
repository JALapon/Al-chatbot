🍕 Pizza Restaurant Q&A Chatbot

This project is an interactive command-line chatbot that answers questions about a fictional pizza restaurant using real-looking review data. It leverages vector embeddings and a local LLM via LangChain and Ollama to retrieve relevant context from restaurant reviews and generate accurate responses.
🧠 How It Works

    Vector Store Initialization:

        Reads a dataset of realistic restaurant reviews from a CSV.

        Converts each review into an embedding using mxbai-embed-large.

        Stores these in a Chroma vector database for efficient retrieval.

    Interactive Q&A:

        Users type in a question.

        The app retrieves the most relevant reviews using vector similarity.

        It uses llama3.2 from Ollama to generate a context-aware answer.

📁 Project Structure

.
├── main.py                      # Main script for the interactive chatbot
├── vector.py                    # Loads the data and sets up the vector store and retriever
├── realistic_restaurant_reviews.csv  # Dataset of fake but realistic reviews
├── requirements.txt             # Required Python packages

🛠 Requirements

Install dependencies with:

pip install -r requirements.txt

You must also have Ollama installed and the models llama3.2 and mxbai-embed-large available locally. Install them via:

ollama pull llama3:2
ollama pull mxbai-embed-large

🚀 Usage

Run the chatbot:

python main.py

Type your question (like "What do people think about the crust?") and get a response. Type q to quit.
📌 Notes

    The vector store is only created on the first run. It will be reused in subsequent runs unless deleted.

    Reviews are stored and searched using langchain-chroma for fast similarity retrieval.

📄 Example Questions

    "Is the service good at the restaurant?"

    "What do reviewers say about the pizza sauce?"

    "Are there any complaints about the wait time?"
