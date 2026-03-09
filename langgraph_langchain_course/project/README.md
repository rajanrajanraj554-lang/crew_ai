# 🤖 AI Research Assistant - Final Project

A multi-agent research assistant built with LangGraph and LangChain.

## Features

- **Router Agent**: Classifies queries and routes to specialists
- **Research Agent**: Searches web and academic papers
- **Math Agent**: Solves mathematical problems
- **Code Agent**: Executes and debugs code
- **Synthesizer**: Combines results from all agents
- **Human-in-the-Loop**: Optional approval step

## Installation

```bash
pip install -r requirements.txt
cp .env.example .env
# Edit .env with your API keys
python src/main.py
```

## Usage

```python
from src.graph import create_research_graph

app = create_research_graph()
result = app.invoke({
    "messages": [("human", "What is the time complexity of quicksort?")],
    "query": "What is the time complexity of quicksort?",
})
print(result["synthesis"])
```
