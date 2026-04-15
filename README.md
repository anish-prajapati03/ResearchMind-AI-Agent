# 🔬 ResearchMind — Multi-Agent AI Research Pipeline

> Four specialized AI agents collaborate to deliver a polished research report on any topic — in seconds.

Built by **Anish Prajapati** · Powered by **LangChain** · UI by **Streamlit**

---

## 🚀 What It Does

ResearchMind runs a 4-step autonomous agent pipeline whenever you enter a research topic:

| Step | Agent | Role |
|------|-------|------|
| 01 | **Search Agent** | Gathers recent, reliable web information on the topic |
| 02 | **Reader Agent** | Picks the best URL and deep-scrapes its content |
| 03 | **Writer Chain** | Drafts a full, structured research report |
| 04 | **Critic Chain** | Reviews, scores, and gives feedback on the report |

The final output is a downloadable `.md` research report with critic feedback — all generated autonomously.

---

## 🖥️ Demo

Live: https://researchmindagentanix.streamlit.app/

---

## 🛠️ Tech Stack

- **[LangChain](https://langchain.com/)** — Agent orchestration, chains, and tool use
- **[Streamlit](https://streamlit.io/)** — Frontend UI
- **Python 3.13**
- **MistralAI / Any LLM** — via LangChain's model abstraction

---

## 📁 Project Structure

```
ResearchMind-AI-Agent/
│
├── app.py            # Streamlit UI (blue theme)
├── agent.py          # Agent & chain definitions
├── requirements.txt  # Python dependencies
├── .env.example      # Environment variable template
└── README.md
```

---

## ⚙️ Setup & Installation

### 1. Clone the repo
```bash
git clone https://github.com/YOUR_USERNAME/ResearchMind-AI-Agent.git
cd ResearchMind-AI-Agent
```

### 2. Create a virtual environment
```bash
python -m venv venv
source venv/bin/activate      # On Windows: venv\Scripts\activate
```

### 3. Install dependencies
```bash
pip install -r requirements.txt
```

### 4. Set up environment variables
```bash
cp .env.example .env
```
Then edit `.env` and add your API keys:
```env
OPENAI_API_KEY=your_openai_key_here
# or
GROQ_API_KEY=your_groq_key_here
```

### 5. Run the app
```bash
streamlit run app.py
```

Open your browser at `http://localhost:8501`

---

## 🧠 How the Agents Work

### 🔍 Search Agent
Uses a search tool (e.g. Tavily, SerpAPI, or DuckDuckGo) to find the most recent and relevant web results for the given topic.

### 📄 Reader Agent
Takes the top search result URLs, picks the most relevant one, and scrapes its full content for deeper research material.

### ✍️ Writer Chain
Combines the search results and scraped content, then uses an LLM to draft a well-structured, comprehensive research report in Markdown.

### 🧐 Critic Chain
Reviews the generated report and provides a quality score along with constructive feedback — covering accuracy, depth, clarity, and completeness.

---

## 📦 Requirements

Create a `requirements.txt` with:
```
streamlit
langchain
langchain-openai
langchain-community
python-dotenv
requests
beautifulsoup4
```

> Adjust based on the tools and LLM provider used in your `agent.py`.



## 🙌 Author

**Anish Prajapati**


---

## 📄 License

This project is licensed under the **MIT License** — feel free to use, modify, and distribute.

---

> ⭐ If you found this useful, please consider giving it a star on GitHub!
