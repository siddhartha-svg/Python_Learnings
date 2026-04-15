# 🤖 AI in IT — Complete Reference Chart

> A comprehensive guide to AI tools & categories for IT professionals.  
> Each section includes: **What it is | Tools | Who uses it | How to use**

---

## 📌 Table of Contents

- [1. AI Coding Assistants](#1-ai-coding-assistants)
- [2. AI for DevOps & Infrastructure](#2-ai-for-devops--infrastructure)
- [3. AI for Cloud & AWS/Azure/GCP](#3-ai-for-cloud--awsazuregcp)
- [4. AI for Cybersecurity](#4-ai-for-cybersecurity)
- [5. AI for IT Operations (AIOps)](#5-ai-for-it-operations-aiops)
- [6. AI for Testing & QA](#6-ai-for-testing--qa)
- [7. AI for Data & Analytics](#7-ai-for-data--analytics)
- [8. AI for Networking](#8-ai-for-networking)
- [9. AI Chatbots & Virtual Assistants](#9-ai-chatbots--virtual-assistants)
- [10. AI for Documentation & Knowledge](#10-ai-for-documentation--knowledge)
- [11. AI Platforms & Frameworks](#11-ai-platforms--frameworks)
- [12. Generative AI (GenAI)](#12-generative-ai-genai)

---

## 1. AI Coding Assistants

> Helps developers write, review, debug, and optimize code faster.

| Sub-Category | Tool | Where to Use | Who Can Use |
|---|---|---|---|
| Code Generation | GitHub Copilot | VS Code, JetBrains, Neovim | Developers, DevOps |
| Code Generation | Amazon CodeWhisperer | VS Code, AWS Cloud9 | Developers, Cloud Engineers |
| Code Generation | Tabnine | VS Code, IntelliJ, Vim | Developers |
| Code Review | CodeRabbit | GitHub, GitLab PRs | Developers, Tech Leads |
| Code Review | SonarQube AI | CI/CD Pipelines | DevOps, QA Engineers |
| Bug Fix & Debug | Cursor AI | VS Code-based IDE | Developers |
| Bug Fix & Debug | Codeium | Browser, VS Code | Developers |
| Code Explanation | ChatGPT / GPT-4 | Web, API | All IT roles |
| Code Explanation | Claude (Anthropic) | Web, API, VS Code | All IT roles |
| Code Search | Sourcegraph Cody | VS Code, Browser | Developers, Architects |

**▶ How to Start:**
```
GitHub Copilot  → Install VS Code extension → Sign in with GitHub
Amazon CodeWhisperer → Install AWS Toolkit → Free tier available
ChatGPT         → chat.openai.com → Paste code → Ask questions
```

---

## 2. AI for DevOps & Infrastructure

> Automates pipelines, IaC generation, incident response, and config management.

| Sub-Category | Tool | Where to Use | Who Can Use |
|---|---|---|---|
| CI/CD Automation | GitHub Actions AI | GitHub Workflows | DevOps Engineers |
| CI/CD Automation | GitLab Duo | GitLab Pipelines | DevOps Engineers |
| IaC Generation | HashiCorp AI (Terraform) | Terraform Cloud | Cloud/DevOps Engineers |
| IaC Generation | Pulumi AI | CLI, VS Code | Cloud Engineers |
| IaC Generation | AWS CloudFormation + Bedrock | AWS Console, CLI | Cloud Engineers |
| Incident Management | PagerDuty AI | Web Dashboard, Slack | SRE, Ops Teams |
| Incident Management | Opsgenie AI | Web, Mobile | SRE, DevOps |
| Log Analysis | Elastic AI (ELK) | Kibana Dashboard | SRE, DevOps |
| Log Analysis | Splunk AI (ITSI) | Splunk Dashboard | SRE, Ops Teams |
| Automated Remediation | Shoreline.io | CLI, Web | SRE Engineers |
| Container Ops | K8sGPT | kubectl CLI | Kubernetes/DevOps |
| Container Ops | Komodor | Web Dashboard | DevOps, SRE |

**▶ How to Start:**
```
K8sGPT          → brew install k8sgpt → k8sgpt analyze
Pulumi AI       → pulumi.com/ai → Describe infra in plain English
PagerDuty AI    → Enable AIOps addon in PagerDuty settings
```

---

## 3. AI for Cloud (AWS / Azure / GCP)

> AI-native services embedded in cloud platforms for automation and intelligence.

| Sub-Category | Tool | Platform | Who Can Use |
|---|---|---|---|
| AI Assistant | Amazon Q | AWS Console, CLI, IDE | Cloud Engineers, Developers |
| AI Assistant | Azure Copilot | Azure Portal | Cloud Engineers |
| AI Assistant | Gemini for Google Cloud | GCP Console | Cloud Engineers |
| ML Platform | Amazon SageMaker | AWS Console, SDK | Data Scientists, ML Engineers |
| ML Platform | Azure Machine Learning | Azure Portal, SDK | Data Scientists |
| ML Platform | Google Vertex AI | GCP Console, SDK | Data Scientists |
| AI Services | AWS Bedrock | AWS Console, API | Developers, Architects |
| AI Services | Azure OpenAI Service | Azure Portal, API | Developers |
| AI Services | Google AI Studio | Web, API | Developers |
| Cost Optimization | AWS Cost Explorer AI | AWS Console | FinOps, Cloud Engineers |
| Security AI | AWS GuardDuty | AWS Console | Security Engineers |
| Security AI | Azure Defender AI | Azure Security Center | Security Engineers |

**▶ How to Start:**
```
Amazon Q        → aws.amazon.com/q → Enable in AWS Console
Azure Copilot   → Azure Portal → Enable Preview feature
AWS Bedrock     → AWS Console → Bedrock → Select foundation model
```

---

## 4. AI for Cybersecurity

> Detects threats, automates response, and identifies vulnerabilities.

| Sub-Category | Tool | Where to Use | Who Can Use |
|---|---|---|---|
| Threat Detection | Darktrace | Network, Cloud, Email | Security Engineers, SOC |
| Threat Detection | CrowdStrike Falcon AI | Endpoint, Cloud | Security Engineers |
| SIEM + AI | Microsoft Sentinel AI | Azure Portal | SOC, Security Analysts |
| SIEM + AI | IBM QRadar AI | On-prem, Cloud | SOC Analysts |
| Vulnerability Scan | Tenable.io AI | Web Dashboard | Security Engineers |
| Vulnerability Scan | Snyk AI | VS Code, CI/CD, GitHub | Developers, DevSecOps |
| Penetration Testing | Pentera | Web Dashboard | Pen Testers |
| Code Security | GitHub Advanced Security | GitHub PRs | Developers, DevSecOps |
| Code Security | Checkmarx AI | CI/CD, IDE | DevSecOps Engineers |
| Phishing Detection | Proofpoint AI | Email Gateway | Security, IT Admins |
| Zero Trust | Zscaler AI | Network Layer | Network, Security Admins |

**▶ How to Start:**
```
Snyk            → snyk.io → Connect GitHub repo → Free plan available
GitHub Adv Sec  → GitHub Settings → Security → Enable code scanning
Microsoft Sentinel → Azure Portal → Sentinel → Enable AI insights
```

---

## 5. AI for IT Operations (AIOps)

> Reduces noise, predicts failures, and automates IT incident resolution.

| Sub-Category | Tool | Where to Use | Who Can Use |
|---|---|---|---|
| Event Correlation | Moogsoft | ITSM Dashboard | SRE, Ops Teams |
| Event Correlation | BigPanda | Web Dashboard | SRE, NOC Teams |
| Predictive Analytics | Dynatrace Davis AI | Web Dashboard, API | SRE, DevOps |
| Predictive Analytics | New Relic AI | Web Dashboard | SRE, DevOps |
| Performance Monitor | Datadog AI | Web Dashboard, CLI | SRE, DevOps |
| ITSM Automation | ServiceNow AI (Now Assist) | ITSM Portal | IT Support, ITSM Teams |
| Root Cause Analysis | Instana AI | Web Dashboard | SRE, DevOps |
| Capacity Planning | IBM Turbonomic | Web Dashboard | Cloud, Ops Teams |
| Alert Noise Reduction | PagerDuty AIOps | Web, Slack | SRE, DevOps |

**▶ How to Start:**
```
Datadog AI      → datadoghq.com → Enable Watchdog AI feature
Dynatrace       → dynatrace.com → Davis AI is built-in, no setup needed
ServiceNow      → Enable Now Assist in ServiceNow instance settings
```

---

## 6. AI for Testing & QA

> Generates test cases, detects bugs, and automates regression testing.

| Sub-Category | Tool | Where to Use | Who Can Use |
|---|---|---|---|
| Test Generation | Testim AI | Web, CI/CD | QA Engineers |
| Test Generation | Mabl | Web, CI/CD | QA Engineers |
| Test Generation | Applitools | Web, Mobile, CI/CD | QA, Developers |
| Unit Test Gen | CodiumAI (Qodo) | VS Code, JetBrains | Developers, QA |
| Unit Test Gen | Diffblue Cover | IntelliJ, CI/CD | Java Developers |
| API Testing | Postman AI | Desktop, Web | Developers, QA |
| API Testing | Katalon AI | Desktop, CI/CD | QA Engineers |
| Performance Testing | k6 AI | CLI, CI/CD | DevOps, Performance QA |
| Visual Testing | Percy (BrowserStack AI) | CI/CD, GitHub | QA, Frontend Devs |
| Bug Detection | Sentry AI | Web Dashboard | Developers, SRE |

**▶ How to Start:**
```
CodiumAI/Qodo   → VS Code Extension → qodo.ai → Auto-generates unit tests
Postman AI      → postman.com → Use Postbot for test generation
Sentry AI       → sentry.io → Connect project → Enable AI summaries
```

---

## 7. AI for Data & Analytics

> Powers data pipelines, BI dashboards, and predictive analytics in IT.

| Sub-Category | Tool | Where to Use | Who Can Use |
|---|---|---|---|
| Data Analytics | Tableau AI (Einstein) | Web Dashboard | Data Analysts, Business |
| Data Analytics | Power BI Copilot | Power BI Desktop, Web | Data Analysts, Business |
| Data Querying | ThoughtSpot | Web Dashboard | Data Analysts |
| Data Querying | Databricks Assistant | Databricks Workspace | Data Engineers |
| Data Pipeline | dbt AI | CLI, Web | Data Engineers |
| Data Pipeline | Fivetran AI | Web Dashboard | Data Engineers |
| Data Quality | Monte Carlo | Web Dashboard | Data Engineers |
| SQL Generation | Text-to-SQL (ChatGPT) | Web, API | All IT roles |
| SQL Generation | AI2SQL | Web | Developers, Analysts |

**▶ How to Start:**
```
Power BI Copilot    → Power BI Service → Enable Copilot in Settings
Databricks Asst     → Databricks workspace → Click AI Assistant icon
ChatGPT SQL         → chat.openai.com → "Write SQL query for [describe]"
```

---

## 8. AI for Networking

> Optimizes network performance, detects anomalies, and automates configuration.

| Sub-Category | Tool | Where to Use | Who Can Use |
|---|---|---|---|
| Network Analytics | Cisco ThousandEyes AI | Web Dashboard | Network Engineers |
| Network Analytics | Juniper Mist AI | Web Dashboard | Network Engineers |
| Traffic Analysis | Darktrace Network AI | Network Layer | Security, Network Admins |
| Anomaly Detection | Arista CloudVision | Web Dashboard | Network Engineers |
| SD-WAN AI | VMware SASE AI | Web Dashboard | Network Engineers |
| SD-WAN AI | Palo Alto Prisma AI | Web Dashboard | Network, Security Admins |
| Network Automation | NetBrain AI | Web Dashboard | Network Engineers |
| Config Management | BackBox AI | Web Dashboard | Network Engineers |

**▶ How to Start:**
```
Cisco ThousandEyes  → thousandeyes.com → Free trial → Connect agents
Juniper Mist AI     → mist.com → Built-in AI → No extra setup needed
```

---

## 9. AI Chatbots & Virtual Assistants

> Handles IT support, FAQ automation, and ticket deflection.

| Sub-Category | Tool | Where to Use | Who Can Use |
|---|---|---|---|
| IT Help Desk Bot | ServiceNow Virtual Agent | ITSM Portal, Slack | IT Support, End Users |
| IT Help Desk Bot | Freshservice AI (Freddy) | Freshservice Portal | IT Support |
| Enterprise Chat | Microsoft Copilot 365 | Teams, Outlook, Word | All IT roles |
| Enterprise Chat | Google Gemini Workspace | Gmail, Docs, Meet | All IT roles |
| Custom Bots | ChatGPT API | Web, App, Slack | Developers, IT Teams |
| Custom Bots | Claude API (Anthropic) | Web, App, Slack | Developers |
| Custom Bots | Azure Bot Service | Azure Portal | Developers |
| Slack AI | Slack AI | Slack | All IT roles |
| Jira AI | Atlassian Intelligence | Jira, Confluence | Developers, Project Mgrs |

**▶ How to Start:**
```
Microsoft Copilot   → Microsoft 365 Admin Center → Enable Copilot
Slack AI            → Slack Admin → Enable Slack AI (paid plan)
ChatGPT API         → platform.openai.com → Get API key → Integrate
```

---

## 10. AI for Documentation & Knowledge

> Auto-generates docs, runbooks, release notes, and knowledge articles.

| Sub-Category | Tool | Where to Use | Who Can Use |
|---|---|---|---|
| Doc Generation | Notion AI | Notion Workspace | All IT roles |
| Doc Generation | Confluence AI | Confluence Pages | All IT roles |
| Runbook Gen | GitHub Copilot Chat | VS Code, GitHub | DevOps, SRE |
| API Docs | Swagger AI / Mintlify | VS Code, Web | Developers |
| README Gen | readme.so + AI | Web | Developers |
| Meeting Notes | Otter.ai | Web, Mobile, Zoom | All IT roles |
| Meeting Notes | Fireflies.ai | Web, Zoom, Teams | All IT roles |
| Diagram Gen | Eraser AI | Web | Architects, DevOps |
| Diagram Gen | Mermaid + ChatGPT | VS Code, GitHub | Developers, Architects |

**▶ How to Start:**
```
Notion AI       → notion.so → Spacebar in any page → Ask AI
Confluence AI   → Atlassian Admin → Enable Atlassian Intelligence
Otter.ai        → otter.ai → Connect Zoom/Teams → Auto-transcribes
```

---

## 11. AI Platforms & Frameworks

> For teams building, training, and deploying AI/ML models in IT products.

| Sub-Category | Tool | Where to Use | Who Can Use |
|---|---|---|---|
| ML Framework | TensorFlow | Python, Cloud | ML Engineers |
| ML Framework | PyTorch | Python, Cloud | ML Engineers, Researchers |
| AutoML | Google AutoML | GCP Console | Data Scientists |
| AutoML | H2O.ai | Python, Web | Data Scientists |
| LLM Orchestration | LangChain | Python, API | AI Developers |
| LLM Orchestration | LlamaIndex | Python, API | AI Developers |
| Model Serving | Hugging Face | Web, API, Python | AI/ML Engineers |
| Model Serving | Ollama | Local CLI | Developers |
| Vector DB | Pinecone | API, Cloud | AI Developers |
| Vector DB | Weaviate | API, Docker | AI Developers |
| Experiment Tracking | MLflow | Python, CI/CD | ML Engineers |
| Experiment Tracking | Weights & Biases | Web, Python | ML Engineers |

**▶ How to Start:**
```
Hugging Face    → huggingface.co → Browse models → pip install transformers
Ollama          → ollama.com → brew install ollama → ollama run llama3
LangChain       → pip install langchain → Build AI app in Python
```

---

## 12. Generative AI (GenAI)

> Creates content, code, images, and automates workflows using LLMs.

| Sub-Category | Tool | Where to Use | Who Can Use |
|---|---|---|---|
| Text / Chat | ChatGPT (OpenAI) | Web, API, Mobile | All IT roles |
| Text / Chat | Claude (Anthropic) | Web, API | All IT roles |
| Text / Chat | Google Gemini | Web, API, Workspace | All IT roles |
| Text / Chat | Meta Llama 3 | Local, Cloud, API | Developers, AI Engineers |
| Image Gen | DALL-E 3 | ChatGPT, API | Developers, IT Marketing |
| Image Gen | Midjourney | Discord, Web | IT Designers |
| Code Gen | GitHub Copilot | VS Code, IDE | Developers |
| Code Gen | Replit AI | Replit IDE | Developers |
| Voice AI | ElevenLabs | Web, API | IT Product Teams |
| Workflow AI | n8n AI | Self-hosted, Cloud | DevOps, Automation |
| Workflow AI | Zapier AI | Web | All IT roles |
| Local LLM | Ollama | Local CLI | Developers, Privacy-focused |
| Local LLM | LM Studio | Desktop App | Developers |

**▶ How to Start:**
```
ChatGPT         → chat.openai.com → Free tier available
Claude          → claude.ai → Free tier available
Local LLM       → ollama.com → ollama run mistral (runs 100% offline)
n8n AI          → n8n.io → Self-host or cloud → Drag-drop AI workflows
```

---

## 🔑 Quick Access by IT Role

| IT Role | Recommended AI Tools |
|---|---|
| **Developer** | GitHub Copilot, ChatGPT, Cursor, CodiumAI, Snyk |
| **DevOps / SRE** | K8sGPT, Datadog AI, PagerDuty AI, Dynatrace, Shoreline |
| **Cloud Engineer** | Amazon Q, Azure Copilot, Pulumi AI, Terraform AI |
| **Security Engineer** | CrowdStrike, Snyk, Darktrace, Microsoft Sentinel |
| **Data Engineer** | Databricks AI, dbt, Power BI Copilot, Monte Carlo |
| **QA / Tester** | CodiumAI, Testim, Mabl, Postman AI, Sentry |
| **Network Engineer** | Cisco ThousandEyes, Juniper Mist AI, NetBrain |
| **IT Support** | ServiceNow AI, Freshservice Freddy, MS Copilot |
| **Architect** | Eraser AI, Mermaid+ChatGPT, Sourcegraph Cody |
| **ML / AI Engineer** | Hugging Face, LangChain, MLflow, PyTorch, Ollama |

---

## 🆓 Free to Start (No Credit Card)

| Tool | Free Tier |
|---|---|
| ChatGPT | Free (GPT-3.5 / limited GPT-4o) |
| Claude | Free tier on claude.ai |
| GitHub Copilot | Free for students & open source |
| Amazon Q | Free individual plan |
| Snyk | Free for open source |
| Hugging Face | Free model hosting |
| Ollama | 100% free, runs locally |
| Postman AI | Free tier |
| Notion AI | Free trial |
| K8sGPT | Open source, free |

---

*Last Updated: April 2026 | Maintained for IT Professionals*
