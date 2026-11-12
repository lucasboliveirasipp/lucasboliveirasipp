# Lucas Oliveira

AI Engineer. I build generative AI systems that read documents, reason over them and return answers people can audit: RAG, multi-agent workflows, document AI and the APIs that put them in production.

At a large Brazilian insurer I designed and built more than 20 generative AI agents and 5 backend services used by legal, underwriting, claims, compliance and customer-service teams. The work covers the full path: prototype in Streamlit, structured outputs with Pydantic, evaluation and tests, then a production API behind the company's AI gateway with authentication, observability and LGPD-safe logging.

**Stack:** Python · LangGraph / LangChain · Azure OpenAI (GPT-4o, GPT-4.1) · Azure AI Search (hybrid and vector RAG) · Azure Document Intelligence (OCR) · FastAPI · Pydantic · Streamlit · pytest · MongoDB / Cosmos DB · PyMuPDF, pdfplumber, python-docx, openpyxl, ReportLab · Docker

## Featured projects

| Project | What it is | Status |
|---|---|---|
| [Document Verification API](https://github.com/lucasboliveirasipp/document-verification-api-case-study) | Checks registration-change requests against their supporting documents (IDs, proof of address, bank letters, photos) and returns a structured legal opinion plus a PDF report. OCR for scans and phone photos, 449 automated tests | Validated with real document batches |
| [AML Dossier Agent](https://github.com/lucasboliveirasipp/aml-dossier-agent-case-study) | Four-step LangGraph pipeline that turns up to 8 PDFs (registry, sanctions, mainframe screenshots) into an anti-money-laundering dossier for underwriters, separating credit risk from real AML signals | In use by underwriting analysts |
| [Contract Comparison](https://github.com/lucasboliveirasipp/contract-comparison-case-study) | Compares a supplier's draft with the company's standard clauses and tracks changes between contract versions, with human review and Word export. Prototype in Streamlit, then a FastAPI backend with 91 tests | Backend phases 1–3 delivered |
| [Document Curation API](https://github.com/lucasboliveirasipp/document-curation-api-case-study) | Scores PDF, Word, Excel and PowerPoint files against 24 quality criteria before they enter a RAG knowledge base, with token budgeting and a deterministic score. 111 tests | In production |
| [Multi-agent Travel Insurance Assistant](https://github.com/lucasboliveirasipp/travel-insurance-multiagent-rag-case-study) | Supervisor, librarian, classifier, analyst and writer agents answer partner sales teams' coverage questions from the product book, using hybrid search on Azure AI Search | Prototype |
| [Legal RAG Chatbot](https://github.com/lucasboliveirasipp/legal-rag-chatbot-case-study) | Corrective RAG over regulations and legal documents: intent routing, query rewriting, document grading and answers with source citations | Prototype, moving to the AI platform |

The code for these systems belongs to my employer, so each link opens a case study: the problem, the architecture, the decisions and their trade-offs. Names and data in the case studies are fictional.

**Also built:** claims pre-analysis (death certificates, heirs' declarations, ID and payroll checks), raffle audit for capitalization bonds, ombudsman ticket triage, health-network provider search with geolocation, OKR coaching assistant, NPS verbatim classification, IT contract clause extraction, regulatory Q&A over SUSEP and CNSP rules, board-report generation, and an Azure AI Search indexing CLI.

**In progress:** Ops Copilot, an open-source agent service that answers operations questions (shifts, SLAs, KPIs) by calling deterministic tools, with evaluations and synthetic data.

## How I work

I start from the business rule and the output format, then work backwards to the prompt. Anything that must be exact (scores, totals, risk rules, document types) is computed in code and validated with Pydantic, not left to the model. Every external call is mocked in tests, logs are sanitized for personal data, and I keep costs predictable with batching, parallelism limits and size caps. I use AI coding agents to move faster on what I have already designed, and I own the architecture and what goes to production.

## Contact

[LinkedIn](https://www.linkedin.com/in/lucasbassodeoliveira/)
