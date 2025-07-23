# Rick AI 🧠🛠️

Rick is a text-based personal coding assistant you run over SSH on a remote Debian machine.  
He helps you **read, write, and reason about code** — especially Python, FastAPI, Docker, and PostgreSQL.

## 🔧 What Rick Can Do -- NOTHING!!!!

- Read and summarize Python code files
- Generate or refactor code on request
- Help debug FastAPI/Docker/PostgreSQL issues
- Store simple memories (like project structure or configs)
- Respond conversationally via terminal

## 💻 How It Works

Rick is built as a CLI REPL (Read-Eval-Print Loop).  
He uses a local LLM (via [Ollama](https://ollama.com) or similar) to generate responses.

## 🗃️ Project Structure

```
rick-ai/
├── rick.py               # Main CLI runner
├── core/
│   ├── brain.py          # Prompt formatting + LLM logic
│   └── context.py        # File reading and input prep
├── model/
│   └── local_llm.py      # Model interface (e.g., Ollama)
├── memory/
│   └── memory.json       # Flat memory file (key-value)
├── requirements.txt
└── README.md
```

## 🚀 Usage

```bash
# SSH into your Rick box
ssh you@your-debian-box

# Run Rick
python3 rick.py
```

Then type things like:

```
Rick > Read src/main.py and explain what it does.
Rick > Write a Dockerfile for a FastAPI app with Postgres.
Rick > What does this error mean: psycopg2.OperationalError...
```

## 📦 Requirements

- Python 3.9+
- A local LLM (recommended: [Ollama](https://ollama.com))
- Optionally: [ChromaDB](https://www.trychroma.com/) or SQLite for memory

## 📍 Notes

- Rick does **not** require an internet connection.
- Everything runs **locally** on your Debian server.
- You can extend Rick with plugins (e.g., search the web, run tests).

## 📜 License

MIT License
