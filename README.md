# 🧠 MCP Research Server

A research assistant server powered by the [Model Context Protocol (MCP)](https://modelcontextprotocol.org), this tool lets AI models interact with academic research papers from [arXiv.org](https://arxiv.org) using callable tools and resources.

## 🚀 Features

- 🔍 Search arXiv for academic papers using keywords
- 📝 Extract and store metadata from papers
- 📁 Organize paper info by topic in local folders
- 📚 Retrieve papers and summaries as Markdown resources
- 🎯 Use prompt templates to guide LLM-based exploration

## 📦 Requirements

- Python 3.8+
- [arxiv](https://pypi.org/project/arxiv/) package
- [mcp](https://pypi.org/project/mcp/) (`fastmcp`)
- File system write access


## ⚙️ Installation

Install dependencies using uv:

```bash
uv add mcp arxiv
```

## ▶️ Running the Server

```bash
python research_server.py
```
By default, this runs on port 8001 with SSE transport.

## 🛠 Tools

#### 🔍 search_papers(topic: str, max_results: int = 5)

Search arXiv for papers on a topic and save their metadata.
Returns: List of paper IDs

#### 📑 extract_info(paper_id: str)

Extracts saved metadata about a specific paper from local storage.
Returns: JSON string or error message

## 📚 Resources

#### 📂 papers://folders
Lists all available research topics that have been saved locally.

#### 🧾 papers://{topic}
Returns a structured Markdown summary of all papers stored under a topic.

## 🧠 Prompts

✨ generate_search_prompt(topic: str, num_papers: int = 5)
Generates a Claude-compatible prompt to analyze academic literature in a structured, insightful way.

#### 📝 Example Usage

```python
search_papers("reinforcement learning", 5)
get_available_folders()
get_topic_papers("reinforcement_learning")
```

## 👤 Author

Sanjay Mehta


