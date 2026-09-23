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
| [llm-log-anomaly-detection](https://github.com/LevaAverGit/llm-log-anomaly-detection) | Rule-based (Sigma) vs LLM incident detection, with **prompt-version and multi-model (gemma3 / Qwen / DeepSeek / GigaChat-2) F1 comparison** | **LangChain**, scikit-learn, MITRE ATT&CK | 52 |
| [llm-data-leak-guard](https://github.com/LevaAverGit/llm-data-leak-guard) | **DLP for LLMs**: detects and redacts PII/secrets from a prompt before the model sees it (152-FZ / GDPR) | FastAPI, Presidio, regex + entropy | 80 |
| [multi-tenant-rls-isolation-lab](https://github.com/LevaAverGit/multi-tenant-rls-isolation-lab) | Tenant isolation enforced **in the database** (FORCE RLS) so a forgotten `WHERE` still can't leak across tenants | PostgreSQL RLS, psycopg | 13 |

Each repo opens with a results table or a worked example, a `make run` that
reproduces the numbers offline, and a "what I learned" that keeps the negative
results in.

## Stack

**LLM** — LangChain · LangGraph · LlamaIndex · Hugging Face Transformers · Ollama · Pydantic · prompt engineering · LLM-as-judge · OWASP LLM Top-10
**Security** — prompt injection · RAG security · DLP · Sigma detection · MITRE ATT&CK · PostgreSQL RLS · 152-FZ / GDPR
**Engineering** — Python · FastAPI · scikit-learn · pytest · Docker · REST · Git · Linux

## More security labs

IAM on Keycloak (OAuth2 / OIDC / SAML / MFA / WebAuthn) · AppSec (OWASP Top-10 vulnerable/fixed pairs, SAST/DAST) · SIEM-style detection · config hardening · 152-FZ personal-data scanner — see [all repositories »](https://github.com/LevaAverGit?tab=repositories).

## Backend & data — skill → proof

Enterprise-Python skills, each one click from the file that uses it:

| Skill | Repo | What / where |
|---|---|---|
| **Django** | [soc-triage-console](https://github.com/LevaAverGit/soc-triage-console) | SOC incident-triage console: models, CBV + FBV, L1/L2 role transitions enforced **server-side** ([transitions.py](https://github.com/LevaAverGit/soc-triage-console/blob/main/triage/transitions.py)), append-only audit trail, admin, management commands · 42 tests, green CI |
| **SQLAlchemy** | [multi-tenant-rls-isolation-lab](https://github.com/LevaAverGit/multi-tenant-rls-isolation-lab) | ORM + Core, engine/pool, sessions, per-transaction tenant context via `set_config` for RLS ([app/orm.py](https://github.com/LevaAverGit/multi-tenant-rls-isolation-lab/blob/main/app/orm.py)) |
| **OpenPyXL** | [mini-siem-detection-lab-v2](https://github.com/LevaAverGit/mini-siem-detection-lab-v2) | Per-incident Excel report: 3 sheets, header styles, freeze panes, severity fills ([report_service.py](https://github.com/LevaAverGit/mini-siem-detection-lab-v2/blob/main/app/services/report_service.py)) |
| **Grafana** | [mini-siem-detection-lab-v2](https://github.com/LevaAverGit/mini-siem-detection-lab-v2) | Provisioned-as-code SOC dashboard: 11 SQL panels, read-only DB mount ([grafana/](https://github.com/LevaAverGit/mini-siem-detection-lab-v2/tree/main/grafana)) |
| **Flask** | [security-config-audit-lab-v2](https://github.com/LevaAverGit/security-config-audit-lab-v2) | Hardened vs vulnerable web apps compared by a config scanner ([hardened app](https://github.com/LevaAverGit/security-config-audit-lab-v2/blob/main/hardened/app/app.py)) |

## Open to

**Prompt Engineer (LLM security) · LLM / AI security · detection engineering.** Moscow / remote.

## Contact

levaaverianov@gmail.com
