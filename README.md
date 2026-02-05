# BlockVote — Online Voting on Blockchain
<img src="https://capsule-render.vercel.app/api?type=waving&color=2e7d32&height=120&section=header&text=BlockVote&fontColor=ffffff&fontSize=40&animation=twinkling" alt="BlockVote" />

[![Python](https://img.shields.io/badge/Python-3.x-3776AB?logo=python&logoColor=white)](https://www.python.org/)
[![Flask](https://img.shields.io/badge/Flask-Web-000000?logo=flask&logoColor=white)](https://flask.palletsprojects.com/)
[![Blockchain](https://img.shields.io/badge/Topic-Blockchain-2e7d32?logo=polymerproject&logoColor=white)](#)
[![UI](https://img.shields.io/badge/UI-HTML%2FCSS-E34F26?logo=html5&logoColor=white)](#)

> 🔐 Secure, tamper-evident voting built with a minimal blockchain, Flask, and a simple web UI.

## What It Is
- 🧪 A lightweight demo of blockchain-backed electronic voting (educational proof of concept).
- ⛓️ Each vote is recorded as a transaction, grouped into mined blocks with Proof of Work.
- 🌐 Flask-powered web app with separate flows for admins (miners) and voters.

## Features
- 🗳️ Double-vote prevention using in-memory voter ledgers during a session.
- 👨‍💼 Admin/miner flow to mine recent votes into the chain and review past records.
- 🧑‍⚖️ Voter flow to cast a ballot via styled HTML forms; optional chain inspection endpoint.
- ⚙️ Simple Proof-of-Work consensus with chain validation hooks for multi-node expansion.
- 📡 JSON APIs for mining, submitting votes, and retrieving the full chain.

## Tech Stack
- 🐍 Languages: Python 3, HTML5, CSS3 (inline + standalone stylesheet).
- 🔧 Frameworks/Libraries: Flask, requests, matplotlib (planned/optional), uuid, hashlib, time.
- 🖥️ Runtime: Any recent Python 3 environment (developed on Windows; works cross-platform).

## Project Structure
- 📁 `main.py` — Flask app, routes for voters/miners, transaction handling, mining trigger, chain viewer.
- 📦 `backend.py` — `Blockchain` class (genesis block, PoW, transaction pool, hashing, consensus hook).
- 🎨 `templates/` — HTML pages for landing, voter entry, ballot forms, repeat-vote notice; includes one legacy Wix-exported page and a basic CSS file.
- 🧰 `venv/` — Local virtual environment (not required if you create your own).

## Getting Started
1) Clone
```
git clone https://github.com/<your-org>/Online-Voting-Using-Blockchain.git
cd Online-Voting-Using-Blockchain-main/Online-Voting-Using-Blockchain-main
```

2) Create & activate a virtual environment
```
python -m venv .venv
./.venv/Scripts/activate   # Windows
# source .venv/bin/activate   # macOS/Linux
```

3) Install dependencies
```
pip install flask requests matplotlib pymysql
```

4) Run the app
```
python main.py
# App defaults: host=localhost, port=5500, debug=True
```

5) Open in your browser
- Admin/miner & voter landing: http://localhost:5500/
- Voter entry page: http://localhost:5500/voter
- Full chain (JSON): http://localhost:5500/chain/

## Usage Notes
- Sample voter IDs and miner IDs are hard-coded for demo purposes; adjust for real deployments.
- Votes are kept in memory; restarting the server resets the chain and voter ledgers.
- Proof-of-Work difficulty is low (four leading zeros) to keep demos fast.
- Security, authentication, persistence, and audit features are intentionally minimal for clarity.

## Publication
This project is published in the **Springer Nature** proceedings:

📖 **"Ensuring Security and Transparency in E-Voting Systems Through Blockchain Technology"**
- **Authors:** Siddhartha Roy, Abhijay Dutta, Surjyakamal Saha, Tanmoy Saha & Suvaditya Roy
- **Conference:** International Conference On Data Mining And Information Security (ICDMIS 2024)
- **Published:** October 01, 2025
- **Series:** Lecture Notes in Networks and Systems (LNNS, volume 1387)
- **DOI/Link:** https://link.springer.com/chapter/10.1007/978-981-96-6060-5_33

<img src="https://capsule-render.vercel.app/api?type=waving&color=2e7d32&height=100&section=footer" alt="footer" />
