# n8n Workflows • Automation Library

A curated collection of production-ready **n8n** automations I use across real projects. Each workflow is designed for **reusability**, **clarity**, and **easy import** into any n8n instance.

> **How to use this repo**
>
> 1. Pick a workflow from the list below.
> 2. **Import** it into n8n (File → *Import from File* or *Import from URL* using the raw JSON link).
> 3. Map credentials (Google, LinkedIn, OpenAI/Groq, Pinecone, Supabase, etc.).
> 4. Test with sample inputs, then enable.

---

## List of Automations/Workflows

1. **Competitor\_Research\_Agent** 
2. **Google\_Calender\_Automation** 
3. **Invoices Extraction** 
4. **LinkedIn\_post\_creator** 
5. **Potential\_Clients** 
6. **Resume\_Optimizer** 
7. **Smart\_AI\_Browser** 
8. **multimodal\_ai\_automation** 
9. **nike\_agent\_Workflow** 
10. **Clinic Agent** 
11. **Postgres & Supabase setup for RAG** 

---

## 🚀 Quick Start

### Option A — n8n Cloud

1. Sign in to **n8n Cloud**.
2. Click **Workflows → Import from URL**.
3. Paste the **raw JSON** link of a workflow from this repo. (Open a file on GitHub → click **Raw** → copy the URL.)
4. After import, open **Credentials** and map required accounts.
5. Run once to verify, then **Activate** the workflow.

### Option B — Self‑hosted n8n (Docker)

```yaml
# docker-compose.yml (minimal)
version: '3.8'
services:
  n8n:
    image: docker.n8n.io/n8nio/n8n:latest
    ports:
      - '5678:5678'
    volumes:
      - ./n8n_data:/home/node/.n8n
    env_file:
      - .env
```

Then open `http://localhost:5678`, go to **Workflows → Import from File**, and upload a JSON from this repo.

### Option C — CLI import (advanced)

```bash
# Install globally
npm install -g n8n

# Import a workflow
n8n import:workflow --input "./Clinic Agent.json"
```

---

## 🔒 Security notes

* Never commit secrets. Use **n8n Credentials** or environment variables.
* Restrict Webhook URLs and use verification tokens (WhatsApp/Meta).
* Follow API rate‑limits (LinkedIn, Google, WhatsApp).
* For PII (clinic/leads), store only what you need; prefer encrypted DBs.

---

## 🤝 Contributing

PRs are welcome! Please include:

* A clean **workflow\.json** with placeholders for credentials (no secrets).
* A short **README.md** inside the workflow folder.
* An update to the **Index of Automations** list.

---

