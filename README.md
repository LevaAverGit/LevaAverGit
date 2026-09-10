# Lev Averyanov

**LLM security & detection engineering.** I build measurement-first labs that
quantify where large language models help — and where they break — in security:
prompt injection, RAG knowledge-base poisoning, data-leak prevention, and
LLM-vs-rules threat detection. Every lab ships honest metrics (including negative
results), reproduces offline, and maps to **OWASP LLM Top-10** and **MITRE ATT&CK**.

## Focus — LLM × security

| Project | What it measures | Key stack | Tests |
|---|---|---|---:|
| [llm-prompt-injection-lab](https://github.com/LevaAverGit/llm-prompt-injection-lab) | Prompt-injection resilience: an `attacker → app → judge` harness scoring an **attack-class × defense breach-rate matrix** (OWASP LLM01) | **LangGraph**, LLM-as-judge, Pydantic | 65 |
| [llm-rag-poisoning-lab](https://github.com/LevaAverGit/llm-rag-poisoning-lab) | Indirect prompt injection via **RAG knowledge-base poisoning**: poisoning-class × defense breach matrix | **LlamaIndex**, **HF** embeddings + injection classifier, Ollama | 133 |
| [llm-log-anomaly-detection](https://github.com/LevaAverGit/llm-log-anomaly-detection) | Rule-based (Sigma) vs LLM incident detection, with **prompt-version and multi-model (gemma3 / Qwen / DeepSeek; GigaChat-ready) F1 comparison** | **LangChain**, scikit-learn, MITRE ATT&CK | 36 |
| [llm-data-leak-guard](https://github.com/LevaAverGit/llm-data-leak-guard) | **DLP for LLMs**: detects and redacts PII/secrets from a prompt before the model sees it (152-FZ / GDPR) | FastAPI, Presidio, regex + entropy | 80 |
| [multi-tenant-rls-isolation-lab](https://github.com/LevaAverGit/multi-tenant-rls-isolation-lab) | Tenant isolation enforced **in the database** (FORCE RLS) so a forgotten `WHERE` still can't leak across tenants | PostgreSQL RLS, psycopg | 12 |

Each repo opens with a results table or a worked example, a `make run` that
reproduces the numbers offline, and a "what I learned" that keeps the negative
results in.

## Stack

**LLM** — LangChain · LangGraph · LlamaIndex · Hugging Face Transformers · Ollama · Pydantic · prompt engineering · LLM-as-judge · OWASP LLM Top-10
**Security** — prompt injection · RAG security · DLP · Sigma detection · MITRE ATT&CK · PostgreSQL RLS · 152-FZ / GDPR
**Engineering** — Python · FastAPI · scikit-learn · pytest · Docker · REST · Git · Linux

## More security labs

IAM on Keycloak (OAuth2 / OIDC / SAML / MFA / WebAuthn) · AppSec (OWASP Top-10 vulnerable/fixed pairs, SAST/DAST) · SIEM-style detection · config hardening · 152-FZ personal-data scanner — see [all repositories »](https://github.com/LevaAverGit?tab=repositories).

## Open to

**Prompt Engineer (LLM security) · LLM / AI security · detection engineering.** Moscow / remote.

## Contact

levaaverianov@gmail.com
