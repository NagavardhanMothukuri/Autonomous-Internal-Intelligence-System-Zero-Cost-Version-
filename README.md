# Autonomous-Internal-Intelligence-System-Zero-Cost-Version-



# 📁 Project Folder Structure

shadowai/
├── backend/
│   ├── main.py               # FastAPI backend server
│   ├── agents/
│   │   ├── watcher_agent.py  # Observes company data
│   │   ├── planner_agent.py  # Decides next actions
│   │   └── executor_agent.py # Executes actions (PRs, emails, tasks)
│   ├── data/
│   │   └── mock_data.json    # Simulated company logs (Slack, GitHub, etc.)
│   ├── memory/
│   │   └── chromadb/         # Local vector store for RAG
│   └── utils/
│       ├── parser.py         # GitHub/Slack/Drive parsers
│       └── summarizer.py     # Summarizes events using local LLM
│
├── models/
│   ├── phi3_loader.py        # Load Phi-3-mini model (recommended lightweight LLM)
│   └── gemma_loader.py       # Optional: Load Gemma 2B for more structured reasoning
│
├── frontend/
│   ├── public/
│   ├── src/
│   │   ├── components/       # React components (Card, Chart, RiskItem)
│   │   ├── pages/
│   │   │   ├── Dashboard.jsx # Main dashboard UI
│   │   │   └── AgentLog.jsx  # Agent activity log view
│   │   └── App.jsx
│   └── tailwind.config.js
│
├── scripts/
│   └── generate_mock_data.py # Generates fake Slack, GitHub, Jira logs for testing
│
├── requirements.txt          # Python dependencies (FastAPI, ChromaDB, CrewAI, LangChain)
├── README.md
└── .env                      # Local config for dev keys (GitHub, Firebase)

# ✅ Phase 1 Plan (MVP)
# - [ ] Set up FastAPI backend
# - [ ] Ingest mock JSON data from /data/
# - [ ] Load Phi-3 via Ollama and use for summarization
# - [ ] Build a simple WatcherAgent using CrewAI
# - [ ] Store task summaries in ChromaDB
# - [ ] Display risk items on React dashboard

# 🧠 Tip: Use `scripts/generate_mock_data.py` to simulate a company
