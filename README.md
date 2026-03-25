<div align="center">

# Agent-47

**Advanced Developer Tools Research Agent**

[![Python](https://img.shields.io/badge/Python-3.13%2B-blue?style=for-the-badge&logo=python&logoColor=white)](https://python.org)
[![FireCrawl](https://img.shields.io/badge/Powered%20By-FireCrawl-orange?style=for-the-badge&logo=fire)](https://firecrawl.dev)
[![LangChain](https://img.shields.io/badge/Built%20With-LangChain-green?style=for-the-badge&logo=langchain)](https://langchain.com)
[![License](https://img.shields.io/badge/License-MIT-purple?style=for-the-badge)](LICENSE)

</div>

---

## Overview

**Agent-47** is a sophisticated automated research agent designed to help developers find and analyze tools, libraries, and platforms. By leveraging **FireCrawl** for web access and **LangChain/LangGraph** for cognitive processing, it autonomously searches for companies, analyzes their offerings, and provides structured insights into pricing, tech stacks, and integration capabilities.

## Features

- **Automated Research**: Intelligent search for developer tools and companies based on natural language queries.
- **Structured Data Extraction**: Automatically extracts key information including:
  - Company/Product Name & Website
  - Pricing Models
  - Open Source Status
  - Tech Stack & Language Support
  - API Availability & Integrations
- **AI-Powered Analysis**: Uses OpenAI's GPT models to synthesize findings into actionable recommendations.
- **Robust Workflow**: Built on LangGraph for reliable, state-aware agent execution.

## Tech Stack

- **Python 3.13+**
- **[FireCrawl](https://firecrawl.dev)** - For web searching and scraping.
- **[LangChain](https://www.langchain.com/)** & **[LangGraph](https://langchain-ai.github.io/langgraph/)** - For agentic workflow and orchestration.
- **OpenAI GPT-4o-mini** - For intelligent processing and summarization.
- **[uv](https://github.com/astral-sh/uv)** - For fast and modern Python package management.

## Getting Started

### Prerequisites

- Python 3.13 or higher.
- **[uv](https://docs.astral.sh/uv/)** installed on your system.
- API Keys for:
  - **OpenAI** (`OPENAI_API_KEY`)
  - **FireCrawl** (`FIRECRAWL_API_KEY`)

### Installation

1.  **Clone the repository:**

    ```bash
    git clone https://github.com/KeneanDita/Agent-47.git
    cd Agent-47
    ```

2.  **Install dependencies using uv:**

    ```bash
    uv sync
    ```

3.  **Configure Environment Variables:**

    Create a `.env` file in the root directory and add your API keys:

    ```ini
    OPENAI_API_KEY=your_openai_api_key_here
    FIRECRAWL_API_KEY=your_firecrawl_api_key_here
    ```

### Usage

Run the agent using `uv`:

```bash
uv run main.py
```

Once started, the agent will prompt you for a query.

**Example Queries:**
- *"Find open source vector databases for Python"*
- *"What are the best monitoring tools for Kubernetes?"*
- *"Search for authentication providers with free tiers"*

### Output Example

```text
Developer Tools Query: vector databases

Results for: vector databases
============================================================

1. Pinecone
   Website: https://www.pinecone.io
   Pricing: Freemium
   Open Source: No
   API: Available
   ...
```

## Project Structure

```
Agent-47/
├── src/
│   ├── __init__.py
│   ├── firecrawl.py    # FireCrawl API integration
│   ├── models.py       # Pydantic data models
│   ├── prompts.py      # LLM prompts
│   └── workflow.py     # LangGraph workflow definition
├── main.py             # Entry point
├── pyproject.toml      # Project configuration & dependencies
└── README.md           # Documentation
```

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
