# 🤖 Multi-Tool AI Research Chatbot

An AI-powered research assistant built using **LangChain, LangGraph, and Groq LLM** that can interact with multiple external tools to retrieve academic research papers, access knowledge from Wikipedia, and search the web for recent information.

The chatbot uses an LLM with tool-calling capabilities to understand user queries and decide when external tools are needed to generate relevant responses.

## 🚀 Project Overview

This project demonstrates how to build an intelligent, tool-using AI chatbot by integrating multiple information sources into a single conversational workflow.

Instead of relying only on the knowledge stored in an LLM, the chatbot can use external tools to retrieve relevant and up-to-date information.

## ✨ Features

- **Arxiv Research Search:** Retrieves academic research papers and related information from Arxiv.
- **Wikipedia Integration:** Fetches information and explanations on different topics using Wikipedia.
- **Tavily Web Search:** Searches the web for recent information, AI news, and other current topics.
- **Groq LLM Integration:** Uses Groq-powered LLM inference for natural language understanding and tool calling.
- **LangGraph Workflow:** Implements a graph-based architecture to manage chatbot execution and tool routing.
- **Tool Calling:** Allows the LLM to select appropriate external tools based on the user's query.
- **Conversational Interaction:** Accepts natural-language questions and displays chatbot responses.

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| Python | Core programming language |
| LangChain | LLM and tool integration |
| LangGraph | Workflow orchestration |
| Groq | LLM inference |
| Arxiv API | Academic research retrieval |
| Wikipedia API | Knowledge retrieval |
| Tavily | Web search |
| Jupyter Notebook | Development and experimentation |

## 🏗️ Architecture

The chatbot follows a graph-based tool-calling workflow.

1. **User Input:** The user submits a question.
2. **LLM Processing:** The Groq-powered LLM processes the query and determines whether a tool is required.
3. **Tool Selection:** The LLM can select Arxiv, Wikipedia, or Tavily.
4. **Tool Execution:** LangGraph's ToolNode executes the selected tool.
5. **Response:** The chatbot returns the available result to the user.

### Workflow Diagram

```text
          User Query
               |
               v
        Groq LLM (Agent)
               |
               v
        Tool Selection
               |
        +------+------+
        |      |      |
        v      v      v
      Arxiv  Wikipedia Tavily
        |      |      |
        +------+------+
               |
               v
         Tool Execution
               |
               v
          Final Output
```

## 📂 Project Structure

```text
multi-tool-ai-research-chatbot/
│
├── chatboot_multiple_tools.ipynb
├── .env
├── .gitignore
└── README.md
```

## ⚙️ Installation and Setup

### 1. Clone the Repository

```bash
git clone https://github.com/YOUR_USERNAME/multi-tool-ai-research-chatbot.git
```

### 2. Navigate to the Project Directory

```bash
cd multi-tool-ai-research-chatbot
```

### 3. Install Dependencies

```bash
pip install -U langchain-community
pip install arxiv==1.4.8 wikipedia
pip install -U langchain-groq
pip install -U langgraph
pip install -U python-dotenv
pip install -U tavily-python
```

### 4. Configure API Keys

Create a `.env` file in the project directory:

```env
GROQ_API_KEY=your_groq_api_key
TAVILY_API_KEY=your_tavily_api_key
```

Get your API keys from:

- Groq: https://console.groq.com/keys
- Tavily: https://app.tavily.com/

**Important:** Never upload your `.env` file or expose your API keys on GitHub.

### 5. Run the Notebook

Launch Jupyter Notebook:

```bash
jupyter notebook
```

Open `chatboot_multiple_tools.ipynb` and execute the cells.

## 💡 Example Queries

Try asking the chatbot:

- What is Artificial Intelligence?
- Find research papers on Quantum Computing.
- Explain the research paper "Attention Is All You Need".
- What are the latest AI news updates?
- Find recent research papers on Machine Learning.
- Search for recent AI news and quantum computing research papers.

## 🎯 Learning Outcomes

Through this project, I explored:

- Building LLM-powered applications using LangChain.
- Integrating multiple external tools with an LLM.
- Implementing tool calling and function execution.
- Designing graph-based workflows using LangGraph.
- Working with external APIs for information retrieval.
- Managing API credentials using environment variables.
