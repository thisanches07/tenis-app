# 2026 Job Market for AI Engineer / LLM / Applied AI / AI Platform / Full-stack AI Engineer roles (developed countries + LATAM-remote)

Research date: 2026-10-10. Method: Indeed job API (mcp__Indeed__search_jobs / get_job_details) in US, UK, DE, NL, CA, AU, IE, plus web search. 14 postings were read in full (job descriptions retrieved); ~7 more are known only from search snippets/aggregators. Many direct fetches (Lever, Remotive, itjobswatch, agentic-engineering-jobs.com) failed with DNS errors from the sandbox, so some figures are from search-result snippets only (flagged).

Indeed short links (to.indeed.com) are the URLs returned by the Indeed API; they may expire.

## Q1. Which stacks/tools are most requested?

### Takeaway
Across 14 fully read 2026 postings, the near-universal core is Python (13/14) and agents with tool calling/integration (11/14). Next come observability (8/14) and RAG, evals and security/guardrails (7/14 each). LangChain/LangGraph is the most-named framework, but only 5/14 name it, and many postings say they are framework-agnostic. MCP, the Vercel AI SDK, FastAPI and specific eval tools (LangSmith/Braintrust) show up in a minority of postings but cluster in product companies and senior roles.

### Cited Findings
**Own tally from 14 full postings (small sample; counts = postings mentioning the item as required or nice-to-have):**
- Python explicitly required/primary or listed: 13/14. The only exception is Supermetrics, which names no language. Sources: the postings in the Q5 table.
- Agents / tool calling / integrating LLMs with external APIs: 11/14 (EZContacts, Re:Build, Luxoft, Reply, Toronto agentic role, Eraneos, Delivery Centric, Anthropic, Keeper, First American/FCT, Supermetrics).
- Observability/monitoring/tracing of AI services: 8/14 (Re:Build, Hostaway, Keeper, FCT, Supermetrics, Luxoft, Delivery Centric, Valence).
- RAG / retrieval: 7/14 (EZContacts, Re:Build, Luxoft, Reply, Toronto agentic, Eraneos, Anthropic).
- Evals / evaluation frameworks / regression testing of prompts: 7/14 (Re:Build, Toronto agentic, Anthropic, FCT, Supermetrics, Valence, Luxoft nice-to-have).
- Security / guardrails / governance / auth in LLM context: 7/14 (Luxoft "safety/guardrails", Delivery Centric "OAuth and RBAC… security guardrails", Keeper, FCT "governance, and safety", Supermetrics "guardrails", Reply "AI Governance, Security, Authentifizierung", Re:Build "OIDC, JWT… secure handling of user data in LLM contexts").
- Fine-tuning: 6/14, mostly nice-to-have or at consultancies/ML-heavy roles (Bluefish, Eraneos, Delivery Centric, Luxoft "fine tuning/LoRA" nice, Re:Build nice, Reply).
- LangChain/LangGraph named: 5/14 (Re:Build "LangChain DeepAgent… LangGraph", Toronto agentic, Eraneos, Delivery Centric, Hostaway). LlamaIndex 2/14; CrewAI/AutoGen 2/14; Semantic Kernel 1/14; Vercel AI SDK 1/14 (Hostaway).
- Cost and latency management / token economics: 5/14 (Luxoft, Re:Build, Keeper, FCT, Supermetrics).
- Vector DBs named: 4/14. Pinecone (Re:Build, Toronto), Weaviate (Re:Build, Toronto), pgvector (Re:Build), Milvus (Toronto); "vector databases" generic (Luxoft, Eraneos).
- Docker/Kubernetes: 4/14 (Reply, Valence, Delivery Centric, FCT).
- TypeScript/JS: 6/14, required in only 2 (Keeper requires JS/TS+React; EZContacts "Python or TypeScript"). It is nice-to-have at Re:Build ("TypeScript / React… streaming agent UIs") and Luxoft ("React (TypeScript preferred)"), listed at FCT, and implied at Hostaway via the Vercel AI SDK.
- MCP: 2/14 (Keeper "Model Context Protocol (MCP)" preferred; Hostaway "MCP servers").
- FastAPI: 2/14 (Luxoft "FastAPI preferred", Delivery Centric "Python (primary) with FastAPI").
- Async/background job pipelines for long-running agents: 2/14 (Re:Build "Celery, RQ, Temporal"; EZContacts "job queues, retries and monitoring").
- Use of AI coding tools as a requirement: 3/14 (Re:Build "Cursor, Copilot, Claude", Keeper "Claude, ChatGPT, GitHub Copilot", FCT "Cursor, Claude Code, GitHub Copilot").
- LLM providers named: OpenAI 4, Anthropic 4, Azure OpenAI 2, Gemini 2, AWS Bedrock 1 (Luxoft, Toronto agentic, FCT, Eraneos, Supermetrics "Vertex AI, Agent Builder, Gemini API", Delivery Centric "Bedrock").
- Clouds: AWS most common (Luxoft, Delivery Centric, Reply, Valence, Keeper). GCP appears at Supermetrics (Cloud Run, Pub/Sub, BigQuery), and Azure at Reply and FCT.

**External aggregate claims (lower confidence):**
- One job board's analysis says LangChain appears in 34.3% of 534 agentic AI job listings, 1.5x the next framework, but the same site elsewhere reports 39.9%. It is a vendor with a stake in the answer — [agentic-engineering-jobs.com, LangChain market 2026](https://agentic-engineering-jobs.com/langchain-job-market-2026) (via search snippet; fetch failed).
- Aggregator snapshot: 42 remote-US LangGraph jobs; postings combining LangGraph + MCP include Sonatype Staff (remote, 2026-05-06), Luxury Presence Applied AI ($200K–$270K) and Flex Staff Platform ($200K–$250K) — [agentic-engineering-jobs.com LangGraph remote US](https://agentic-engineering-jobs.com/jobs/langgraph/remote/us) (search snippet only).
- One posting cited in search results asks for eval/observability platforms "such as Braintrust, LangSmith, Arize, or Weights & Biases" and "LLM-as-judge scoring pipelines" — [jobright.ai listing](https://jobright.ai/jobs/info/689f9747b3e889632cf08df3) (search snippet).
- Resume-keyword claim: PyTorch in ~38% of postings; methodology not described — [levstack.io](https://levstack.io/en/blog/ai-engineer-resume-2026/) (search snippet).
- Vercel AI SDK 6 adds an Agent abstraction, stable MCP support, human-in-the-loop tool approval and structured outputs. This is the TS ecosystem's MCP path — [noqta.tn guide](https://noqta.tn/en/blog/vercel-ai-sdk-6-typescript-ai-agents-guide-2026).

### Inferences
- The tool most worth showing in a portfolio is not a specific framework but the cross-cutting pattern: agent + tool calling + RAG + evals + observability + guardrails + cost/latency tracking. Re:Build states it outright: "understands how agent systems work under the hood, not just one framework's abstractions."
- Specific eval/observability tools (LangSmith, Langfuse, Braintrust, promptfoo) are rarely named in mainstream postings. "Evaluation frameworks" and "tracing" are asked for generically, so any credible tool works if the eval discipline is visible.
- MCP is an emerging differentiator (2/14 in mainstream postings, more common at AI-native startups per aggregator snippets). It is cheap to add to a portfolio and signals currency.
- I found no 2026 mainstream posting naming Mastra, Pydantic AI, the OpenAI Agents SDK or the Claude Agent SDK. They are probably too new or niche to be listed as requirements, though they show framework fluency.

### Gaps
- No rigorous, methodology-backed 2026 skill-frequency dataset (Lightcast/LinkedIn/Indeed Hiring Lab) was found. The percentages above come from a small hand-tallied sample plus vendor claims.
- Frequency of AI gateways (LiteLLM, Portkey, Cloudflare AI Gateway) and of named guardrail tools (NeMo Guardrails, Guardrails AI): none of the 14 postings named them, and I found no data.
- Pinecone vs pgvector vs Qdrant relative demand is not quantified.

## Q2. AI Engineer vs ML Engineer; Python vs TypeScript

### Takeaway
"AI Engineer" postings describe building products on top of foundation-model APIs: agents, RAG, integrations, evals, production ops. "ML Engineer" or ML-flavored postings ask for model training, PyTorch/TensorFlow, MLOps and data science tooling. Python is the default language. TypeScript appears mainly in full-stack/product roles, usually as a second language for streaming UIs or for the Vercel AI SDK, not as the sole language.

### Cited Findings
- Framing: "ML engineers build systems that make predictions at scale. AI engineers ship products powered by large language models"; "read the verbs in the job description, not just the noun in the title" — [letsdatascience.com](https://letsdatascience.com/blog/data-scientist-vs-ml-engineer-vs-ai-engineer-in-2026); [refontelearning](https://www.refontelearning.com/blog/ai-engineer-vs-machine-learning-engineer).
- Product-style AI Engineer example: Keeper says "This is a hands-on full-stack engineering role, not a research or model-training position" — [Keeper Security, Indeed](https://to.indeed.com/aal24xf6wgwl).
- Supermetrics: "This is a software engineering role, not a workflow-automation role" — [Supermetrics, Indeed](https://to.indeed.com/aa69mdr4ty7y).
- ML-flavored "AI Engineer" titles still exist. Bluefish's Senior AI Engineer leads "development, training, and fine-tuning of large language models", and Reply (DE) wants TensorFlow/PyTorch/Keras plus MLflow/Kubeflow/Seldon — [Bluefish, Indeed](https://to.indeed.com/aar7vh7bpylv); [Reply, Indeed](https://to.indeed.com/aawd6jj6k9w2).
- Valence's "Applied AI" Staff role asks for NumPy, scikit-learn, Pandas and PySpark, which signals a data science blend — [Valence, Indeed](https://to.indeed.com/aamnn4pctjsj).
- Python-only examples: Re:Build ("Proficiency with Python in production"; TypeScript/React only "Highly Valuable"), Toronto agentic role, Anthropic Applied AI, Delivery Centric, Eraneos — URLs in the Q5 table.
- Both languages: EZContacts ("Strong Python or TypeScript"); Hostaway (Python plus "LangChain, Vercel AI SDK, MCP servers… bridging stacks"); Keeper (TS/React required, Python AI services preferred); Allied Technology Services LATAM (TypeScript, NestJS/Next.js, AI assistants and agentic workflows); Coderio LATAM ("Senior AI Engineer - Python/Typescript") — [Allied via Remotive](https://remotive.com/remote/jobs/artificial-intelligence/senior-ai-engineer-6118790) and [Coderio, Lever](https://jobs.lever.co/coderio/4ac1fb01-ef01-47c8-a05c-e5c4bf35db95) (both from search snippets; fetch failed).
- TS-centric example: Vercel "Software Engineer, AI SDK" asks for 5+ years of JavaScript/TypeScript and open source contributions, at USD 192k–288k + equity (another listing says $196K–$294K; posted Mar 2026, reposted Jul 2026) — [Vercel careers](https://vercel.com/careers/software-engineer-ai-sdk-5474915004).
- Packt-cited emerging title counts: Forward Deployed Engineer (229), GenAI Engineer (215), Agentic AI Engineer (125). Unclear basis — [Packt author posts](https://www.packtpub.com/en-CY/learning/author-posts) (search snippet).
- Unverified claim that AI Engineer listings outnumber ML Engineer listings about 5:1 on LinkedIn (single blog, no source) — [aiagentrank.io](https://aiagentrank.io/blog/how-to-become-ai-engineer-2026).

### Inferences
- For a Python + TypeScript/Node candidate, the strongest positioning is "Python backend for LLM services (FastAPI) + TypeScript for streaming agent UIs and Vercel AI SDK/MCP." That matches the "highly valuable" lines in Re:Build, Luxoft and Hostaway.
- TypeScript-only AI roles exist (Vercel, LATAM agency roles with NestJS/Next.js), but they are a minority. Lacking Python would close most doors in DE/NL/UK enterprise and consultancy postings.
- New title variants such as "Agentic AI Engineer", "AI Platform Integration", "Forward Deployed / Applied AI" all map to the same skill core.

### Gaps
- No quantitative Python vs TypeScript share in 2026 AI postings was found.

## Q3. What do senior/staff/lead postings expect?

### Takeaway
Senior and staff postings expect 5–8+ years of software engineering, with 2+ years shipping LLM/agent systems to production. They also expect ownership of eval and observability infrastructure, explicit treatment of cost, latency, governance and safety, async/long-running agent reliability, multi-agent orchestration, and cross-team technical leadership. Build-vs-adopt judgment on fast-changing frameworks is called out explicitly.

### Cited Findings
- Re:Build Senior AI Engineer: "5+ years… 2+ years focused on bringing LLM-based applications or agent systems to market"; "Building evaluation and observability infrastructure… tracing, cost tracking, latency monitoring, and automated quality benchmarks"; "streaming agent interfaces"; "background job / async task pipelines (Celery, RQ, Temporal)… reliable retries"; "multi-agent systems with planning, delegation"; "regression testing for prompts"; "model selection/routing strategies" — [Indeed](https://to.indeed.com/aapfd2rkrvdg).
- First American/FCT Staff (AI-Native Platform): "Deep understanding of AI operational concerns including evaluation strategies, model selection, latency optimization, cost management, observability, governance, and safety"; "reusable engineering platforms"; OpenTelemetry/Datadog; Terraform/CDK — [Indeed](https://to.indeed.com/aaygq9fft2x7).
- Luxoft Senior (London): "8+ years"; FastAPI with OpenAPI, versioning and observability; AWS eventing/queues/serverless; "prompt design, safety/guardrails, and cost/perf tuning"; AgentCore nice-to-have — [Indeed](https://to.indeed.com/aa2ykftdnss9).
- Supermetrics: "owned the pager"; "agents or LLM-backed services you shipped and operated, including evaluation, guardrails, cost, and latency management"; an agent registry — [Indeed](https://to.indeed.com/aa69mdr4ty7y).
- Keeper Senior: "execution safety, reliability, observability and predictable system behavior"; zero-knowledge security constraints — [Indeed](https://to.indeed.com/aal24xf6wgwl).
- Toronto agentic role: "evaluation frameworks to monitor agent performance, reduce hallucinations, and ensure safe and predictable behavior"; "context engineering" — [Indeed](https://to.indeed.com/aalr4jsjnx7q).
- Anthropic Applied AI (Sydney): 8+ years; "advanced prompt engineering, agent development, evaluation frameworks, and deployment at scale"; build "evaluation suites" for customers — [Indeed](https://to.indeed.com/aar24xjs64jk).
- Fieldguide "AI Engineer, Quality (Evals)" is a dedicated evals role (remote US, $170K–$220K, LangGraph/LangSmith, listed 2026-04-19) — [agentic-engineering-jobs.com LangSmith](https://agentic-engineering-jobs.com/jobs/langsmith) (snippet); [Fieldguide AI Engineer on 8vc board](https://jobs.8vc.com/companies/fieldguide/jobs/58380612-ai-engineer).

### Inferences
- Prompt injection is rarely named explicitly. Security shows up as "guardrails", "execution safety", "auth (OAuth/RBAC/OIDC/JWT)" and "secure handling of user data in LLM contexts". A portfolio showing prompt-injection defenses plus tool-permission scoping would map onto these lines.
- "Eval-driven development" is the clearest seniority signal: eval suites, regression tests for prompts, and LLM-as-judge.

### Gaps
- No staff posting in the sample explicitly mentioned "prompt injection" by name.

## Q4. Salary ranges per country

### Takeaway
The US pays by far the most: about $110K–$140K for small-company mid-level roles, $145K–$220K for senior, and $190K–$290K+ at AI-native companies. Canada top roles reach C$185K–225K. UK medians sit around £70K–85K (London higher). Germany is about €65K–115K (senior €115K–150K+ in Munich/Berlin), and the Netherlands consultancy scale is about €46K–87K. LATAM contractor roles cluster around US$4K/month to US$57K–78K/year.

### Cited Findings
- US: EZContacts AI Engineer (NY, remote) $110K–$140K, posted 2026-10-07 — [Indeed](https://to.indeed.com/aa8pk7gp99zm). Re:Build Senior AI Engineer $143.7K–$215.5K, posted 2026-04-28 — [Indeed](https://to.indeed.com/aapfd2rkrvdg). First American Staff $148.6K–$198.2K, posted 2026-09-23 — [Indeed](https://to.indeed.com/aaygq9fft2x7). Cookunity "AI Native Engineer" $130K–$140K, posted 2026-04-28 — [Indeed](https://to.indeed.com/aadq846cxrbb). Vercel AI SDK $192K–$288K — [Vercel](https://vercel.com/careers/software-engineer-ai-sdk-5474915004). Aggregator medians: mid-level US LangGraph roles about $150K–$205K; remote LangGraph average $165.7K–$236.5K — [agentic-engineering-jobs.com](https://agentic-engineering-jobs.com/jobs/mid/langgraph/us) (snippet). Recruiter claim: LLM engineer mid $145K–$200K, senior $200K–$320K — [KORE1](https://www.kore1.com/hire-llm-engineers-2026/).
- Canada: Toronto "Software Engineer - Agentic AI" $185,000–$225,000 (currency presumably CAD; posting says "RRSP match"), posted 2026-10-07 — [Indeed](https://to.indeed.com/aalr4jsjnx7q). Secondary sources conflict: averages of C$85K+, ~$110K and $129,850 — [pwskills](https://pwskills.com/blog/ai-engineers-salary-2026/); [qubit-labs](https://qubit-labs.com/ai-engineer-salary-guide/).
- UK: itjobswatch AI Engineer median £85,000 (UK, 6 months to May 2025, only 33 salaries) and £52,000 outside London. The broader "AI" category median was £71,000 for the 6 months to 18 Jan 2026, down 7.79% YoY — [itjobswatch AI Engineer](https://www.itjobswatch.co.uk/jobs/uk/artificial%20intelligence%20engineer.do); [itjobswatch AI](https://www.itjobswatch.co.uk/jobs/uk/artificial%20intelligence.do) (search snippets). Another job-ads median: £77,500 (P25–P75 £62.5K–£100K, 6 months to Nov 2025) — [digitaldefynd](https://digitaldefynd.com/IQ/ai-salaries-in-europe/) (snippet).
- Germany: SalaryExpert average €92,232 (entry about €64.6K, senior about €114.6K); senior ML in Munich/Berlin €115K–150K+ — [digitaldefynd](https://digitaldefynd.com/IQ/ai-salaries-in-europe/); [qubit-labs](https://qubit-labs.com/ai-engineer-salary-guide/) (snippets).
- Netherlands: Eraneos (Senior) AI Engineer gross monthly salary €3,551–€5,086 (engineer) and €4,799–€6,719 (senior), excluding 8% holiday pay, on a 40h week. That is about €46K–66K for engineer and €62K–87K for senior per year including holiday pay (my calculation) — [Indeed](https://to.indeed.com/aa9mxtvxzgqk).
- LATAM remote: Allied Technology Services Senior AI Engineer US$4,000/month contractor, EST hours — [Remotive](https://remotive.com/remote/jobs/artificial-intelligence/senior-ai-engineer-6118790) (snippet). Space Inch AI Engineer LATAM USD 57,000–78,000 (posted Dec 2025) — [Workable](https://apply.workable.com/spaceinch/jobs/view/3B9B02C969.md) (snippet).

### Inferences
- European postings (UK/DE/NL/IE/AU) in the Indeed sample mostly omit salary. US/Canada postings disclose ranges due to pay-transparency laws.

### Gaps
- No reliable 2026 figures were found for Switzerland, the Nordics, Ireland or Australia AI Engineer salaries. Postings found there (Supermetrics Helsinki/Dublin, Mistral/Anthropic Sydney, Mastercard Dublin) did not list pay.
- The UK itjobswatch AI Engineer-specific figure is from 2025; a 2026 equivalent could not be fetched.

## Q5. Concrete example postings (2026)

### Takeaway
Twenty postings from 2026 (dates in the table) span US, UK, DE, NL, CA, AU, IE/FI and LATAM. The 14 marked "full" were read in full via the Indeed API; the rest are from search snippets.

### Cited Findings
| # | Company | Country / mode | Title | Posted | Key requirements | URL |
|---|---|---|---|---|---|---|
| 1 | EZContacts | US (NY), remote | AI Engineer | 2026-10-07 | 2+ yrs shipping LLM products (agents, RAG, voice/chat bots); Python **or** TypeScript; GitHub/portfolio required; long-running agents with memory, queues, retries; $110–140K (full) | [link](https://to.indeed.com/aa8pk7gp99zm) |
| 2 | Re:Build Manufacturing (Reflow) | US, remote-first | Senior AI Engineer | 2026-04-28 | LangChain DeepAgent/LangGraph, CrewAI/AutoGen; RAG, tool calling, token economics; eval + tracing + cost/latency; Celery/Temporal; multi-agent; Pinecone/Weaviate/pgvector; TS/React for streaming UIs; $143.7–215.5K (full) | [link](https://to.indeed.com/aapfd2rkrvdg) |
| 3 | Keeper Security | US, 100% remote | Senior Software Engineer, AI Platform Integration | 2026-10-08 | Full-stack; JS/TS + React; Rust/Python/Go etc.; LLM tool-calling integration; **MCP** preferred; latency/cost/observability; AI coding tools (full) | [link](https://to.indeed.com/aal24xf6wgwl) |
| 4 | First American (FCT) | US, remote | Staff Software Engineer (AI-Native Platform) | 2026-09-23 | Production LLM/agentic systems; evals, model selection, latency, cost, governance, safety; OpenAI/Azure OpenAI/Anthropic; Python/TS/C#; K8s, Terraform, OpenTelemetry; $148.6–198.2K (full) | [link](https://to.indeed.com/aaygq9fft2x7) |
| 5 | Luxoft | UK (London) | AI engineer with Agentic experience (Senior) | 2026-10-09 | 8+ yrs Python; FastAPI; AWS (queues, serverless); agents; vector DB/RAG; OpenAI/Azure/Anthropic; guardrails; cost/perf; AgentCore; React+TS nice (full) | [link](https://to.indeed.com/aa2ykftdnss9) |
| 6 | Bluefish AI | UK (London), hybrid/remote UK | Senior AI Engineer | 2026-05-06 | ML/NLP-heavy: training and fine-tuning LLMs, Python, model evaluation (full) | [link](https://to.indeed.com/aar7vh7bpylv) |
| 7 | Reply | Germany (Berlin/Munich/Hamburg), hybrid | (Senior) Agentic AI Engineer | 2026-08-26 | RAG, LLM orchestration, multi-agent; Python; PyTorch/TF; AWS/Azure; Docker/K8s; MLOps/LLMOps (MLflow, Kubeflow); knowledge graphs/Neo4j; German + English (full) | [link](https://to.indeed.com/aawd6jj6k9w2) |
| 8 | Eraneos | Netherlands (Amsterdam) | (Senior) AI Engineer | 2026-03-25 | Fine-tuning, advanced RAG, agentic workflows, "harnesses"; Python; LangChain/LlamaIndex, HF, MLflow, vector DBs; presales/demos; Dutch + English; €3.5–6.7K/month (full) | [link](https://to.indeed.com/aa9mxtvxzgqk) |
| 9 | Hyrr AI (per search listing) | Canada (Toronto), hybrid | Software Engineer - Agentic AI | 2026-10-07 | Python; LangChain/LlamaIndex/AutoGen; context engineering; Gemini/OpenAI/Anthropic; RAG with Pinecone/Weaviate/Milvus; eval frameworks; $185–225K (full) | [link](https://to.indeed.com/aalr4jsjnx7q) |
| 10 | Valence | Canada (Toronto)/NYC hybrid or remote | Staff Software Engineer, Applied AI | 2026-08-09 | 8+ yrs; LLM components + evaluation; NumPy/Pandas/PySpark; AWS/GCP/Azure; Docker/K8s; MLflow/W&B nice (full) | [link](https://to.indeed.com/aamnn4pctjsj) |
| 11 | Delivery Centric | Australia (Sydney), on-site | Agentic AI Engineer | 2026-10-08 | Python + FastAPI; Docker/K8s; OAuth/RBAC; LangChain/LangGraph, Semantic Kernel; AWS Bedrock/SageMaker/EKS; Postgres/Snowflake; guardrails; banking (full) | [link](https://to.indeed.com/aay6xwpt9dsj) |
| 12 | Anthropic | Australia (Sydney), hybrid | Applied AI Engineer | 2026-06-05 | 8+ yrs; Python; prompt engineering, agents, evaluation frameworks, retrieval; customer-facing; builds eval suites (full) | [link](https://to.indeed.com/aar24xjs64jk) |
| 13 | Supermetrics | Ireland (Dublin) / Finland (Helsinki), hybrid | Agentic AI Engineer | 2026-08-26 | Production LLM agents incl. evaluation, guardrails, cost, latency; GCP Cloud Run/Pub/Sub; BigQuery/SQL; REST/webhooks; Gemini/Vertex nice (full) | [link](https://to.indeed.com/aa69mdr4ty7y) |
| 14 | Hostaway | Remote EMEA (listed Dublin) | Senior Backend Engineer, AI Platform | 2026-09-03 | Python; REST; **LangChain, Vercel AI SDK, MCP servers**; observability for AI services (full) | [link](https://to.indeed.com/aawq7bgs4ls6) |
| 15 | Vercel | US / remote | Software Engineer, AI SDK | Mar & Jul 2026 | 5+ yrs TypeScript; OSS; AI SDK (agents, MCP); $192–288K (snippet) | [link](https://vercel.com/careers/software-engineer-ai-sdk-5474915004) |
| 16 | Fieldguide | US, remote | AI Engineer, Quality (Evals) | 2026-04-19 | LangGraph, LangSmith; evals focus; $170–220K (snippet) | [link](https://agentic-engineering-jobs.com/jobs/langsmith) |
| 17 | Mistral AI | UK (London) | Applied AI, Forward Deployed ML Engineer | 2026-10-09 | (details not retrieved) | [link](https://to.indeed.com/aavtpd7j28nf) |
| 18 | Mistral AI | Australia (Sydney) | Applied AI Engineer, Australia | 2026-09-16 | (details not retrieved) | [link](https://to.indeed.com/aa68vh8hdc7s) |
| 19 | Allied Technology Services | LATAM remote (EST) | Senior AI Engineer | 2026 (date not confirmed) | TypeScript, NestJS/Next.js, AI assistants, agentic workflows; US$4K/month contractor (snippet) | [link](https://remotive.com/remote/jobs/artificial-intelligence/senior-ai-engineer-6118790) |
| 20 | Coderio | LATAM remote (AR, MX, PE, CL, BR) | Senior AI Engineer - Python/Typescript | 2026 (date not confirmed) | LLM integration into production, agentic workflows (snippet) | [link](https://jobs.lever.co/coderio/4ac1fb01-ef01-47c8-a05c-e5c4bf35db95) |

Other 2026 titles seen in Indeed listings only (not read): Mastercard "Agentic AI - Senior Software Engineer" (Dublin, 2026-07-23); ServiceNow "Forward Deployed Solution Engineer – Applied AI FDE" (Dublin, 2026-09-25); Google "Staff Forward Deployed Engineer, Developer AI" (Sydney, 2026-09-07); Okta "Staff Backend Software Engineer, SecureAI" (Toronto, 2026-10-08); ITQ "AI Platform Engineer" (NL, 2026-04-28); Feathery "Senior Software Engineer - Applied AI" (Toronto, 2026-04-09); LangChain "Senior Technical Support Engineer" (NY, $130–195K, 2026-05-06).

### Inferences
- Several postings demand demonstrable production work. EZContacts requires "Real projects running in production that you can show us; a GitHub or portfolio is required," which shows the value of a deployed, documented portfolio project with evals and observability.
- Hiring is spread across EMEA-remote (Hostaway) and LATAM-remote contractor channels, but most developed-country roles in the sample are hybrid or on-site and some require work authorization. Re:Build is US citizens/permanent residents only; Valence requires US work documents without restrictions.

### Gaps
- No Switzerland or Nordics-only postings were read in full. Supermetrics (Helsinki/Dublin) is the only Nordic example.
- The HN "Who is hiring" October 2026 thread could not be located through search.
- Rows 17–20 lack verified full descriptions because sandbox fetches to Lever/Remotive failed.
