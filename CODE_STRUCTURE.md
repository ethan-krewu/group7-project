\#Source code structure This document explains the structure of our
chatbot web app.

---

\##Project folder layout

\## 📁 Source Code Structure

\`\`\` 📦 chatbot-webapp/ ├── 📁 Data\_Ivanti/ \# Ivanti data batch
folders │ ├── documents\_batches/ │ ├── error\_messages\_batches/ │ ├──
incidents\_batches/ │ ├── knowledges\_batches/ │ ├── problems\_batches/
│ ├── references\_batches/ │ ├── resolution\_actions\_batches/ │ ├──
service\_requests\_batches/ │ ├── sources\_batches/ │ └──
workarounds\_batches/

├── 📁 scripts/ \# Python scripts for handling Ivanti datasets │ ├──
Documents.py │ ├── Error\_messages.py │ ├── Incidents.py │ ├──
Knowledges.py │ ├── Problems.py │ ├── References.py │ ├──
Resolution\_actions.py │ ├── Service\_requests.py │ ├── Sources.py │ └──
Workarounds.py

├── 📁 backend/ \# Backend logic (e.g., API routes, processing) │ └──
\_\_init\_\_.py

├── 📁 frontend/ \# Frontend UI (from thinktank-chat-ui-main) │ └──
thinktank-chat-ui-main/ │ ├── public/ │ ├── src/ │ └── package.json

├── 📁 config/ \# Config files & environment │ └── .env

├── 📁 docs/ \# Project documentation │ ├── README.md │ └──
README\_ThinkTank\_AI\_Assistant.md

├── .gitignore \# Ignore rules for Git ├── app.py \# Main Python app
entry point ├── requirements.txt \# Python dependencies \`\`\`

\## How The flow of the web app chatbot works 1. The user logs into the
chatbot through a login page made with Supabase 2. User types a query,
the frontend sends the question to the backend. 3. The Backend then uses
Azure/OpenAI and cognitive search to generate a response. 4. Response is
taken from the backend to the frontend and is shown to the user.

--- \##Technologies used

-\*\*Frontend\*\*: React.js -\*\*Backend\*\*: FastAPI
-\*\*Authentication\*\*: Supabase -\*\*Storage\*\*: Azure Blob Storage
-\*\*AI\*\*: GPT via Azure/OpenAI

---
