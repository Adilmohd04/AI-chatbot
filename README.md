
# 🔥 AI Movie Character Chatbot 🚀

## 🎯 Overview
This project designed to progressively build and scale an AI-powered chatbot that mimics movie characters. The chatbot integrates **LLMs, real movie dialogues, RAG-based vector search, caching, and high-performance optimizations**. The goal is to develop a scalable, real-time backend chatbot capable of handling high traffic and providing character-accurate responses.

## 🏆 Features
- **Character-Accurate Responses** – AI mimics personalities using LLMs & movie dialogues.
- **Retrieval-Augmented Generation (RAG)** – Enhances accuracy with semantic search for more relevant dialogue retrieval.
- **High-Performance Optimization** – Redis caching, async processing, rate limiting for handling large traffic volumes.
- **Scalability & Deployment** – Handles high traffic, deployed with WebSockets for real-time interaction, and includes performance monitoring.

## 🏗 Tech Stack
- **Backend:** FastAPI, Python
- **AI Models:** OpenAI GPT API / Llama2
- **Database:** MongoDB, Redis, Vector DB (FAISS/Pinecone/ChromaDB)
- **Deployment:** Vercel
- **Monitoring:** Prometheus, Grafana
- **Additional Tools:** WebSockets for real-time communication

## 🚀 Installation & Setup

### 1. **Clone the Repository**  
   Clone this repository to your local machine:
   ```bash
   git clone https://github.com/your-repo-link.git
   cd ai-movie-chatbot
   ```

### 2. **Install Dependencies**  
   Install all the required dependencies using pip:
   ```bash
   pip install -r requirements.txt
   ```

### 3. **Set Up Environment Variables**  
   Create a `.env` file in the root directory and add the following environment variables:
   ```env
   OPENAI_API_KEY=your_openai_api_key
   DATABASE_URL=your_database_url
   REDIS_URL=your_redis_url
   ```

### 4. **Run the Server**  
   Start the development server using Uvicorn:
   ```bash
   uvicorn main:app --reload
   ```

## 📌 API Endpoints  
Here are the available API endpoints:

### `POST /chat`
- **Description**: Sends user messages and returns the chatbot's response based on the chosen movie character.
- **Request Body**:
  ```json
  {
    "character": "CharacterName",
    "user_message": "User's message"
  }
  ```
- **Response**: Returns a message mimicking the character's personality.
  
### `POST /store-script`
- **Description**: Stores movie dialogues in the database for later retrieval.
- **Request Body**:
  ```json
  {
    "movie_name": "Movie Title",
    "character": "Character Name",
    "dialogue": "Character's dialogue"
  }
  ```

### `GET /status`
- **Description**: Health check endpoint to verify that the API is running properly.

## 📚 Movie Script Sources
For this project, movie scripts can be sourced from:
- [IMSDb (Internet Movie Script Database)](https://www.imsdb.com/)
- [SimplyScripts](https://www.simplyscripts.com/)
- [The Script Lab](https://thescriptlab.com/)
