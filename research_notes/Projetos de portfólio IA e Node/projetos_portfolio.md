# Portfolio projects that show senior Node.js backend and AI engineering skills (2025-2026)

> Method note: research ran on 2026-10-10. Most direct page fetches failed with DNS errors in this environment, and GitHub API access was blocked. Most findings below therefore come from search-result excerpts, not from full-page reads. Many sources are vendor or career blogs. Their quality is flagged inline. I did not verify any primary hiring-manager survey on portfolio projects.

## 1. What makes a portfolio project credible for senior roles?

### Takeaway
At senior and tech-lead level, side projects count for much less than proven business impact. They help only when they show something your work history does not already show, and only if you can discuss them in depth. For AI roles, the clearest credibility signals are end-to-end ownership (API, deployment, observability), measurable results, and above all a real evaluation layer.

### Cited Findings
- A techinterview.org guide says a side project earns a place on a senior résumé only if it shows something the work-history bullets don't. Its test is whether a hiring manager would learn anything new from it. It also says most senior engineers shouldn't have a projects section at all. — [techinterview.org](https://www.techinterview.org/post/3233474610/side-projects-open-source-engineering-resume/)
- An r/ExperiencedDevs thread asked whether seniors should build side projects to show complexity. A recap summarised the answer as "kinda sorta." — [Dev Leader weekly recap, 2025-08-08](https://devleader.substack.com/p/weekly-recap-2025-08-08)
- A recruiter on a Taro thread said a side-projects section on a senior résumé would seem odd to them, because they look mainly for business impact. — [Jointaro](https://jointaro.com/question/SzhkjSOV9o1KNLAnQzPp/do-personal-projects-matter-or-help)
- A 2026 essay argues that at senior level, professional impact (systems improved, costs cut) matters more than a GitHub profile. — [digitalbiztalk](https://digitalbiztalk.com/article/why-senior-devs-don-t-need-github-side-projects-in-2026)
- A co-founder who has reviewed hundreds of résumés says interviews often expose shallow knowledge behind long project lists. — [HackerNoon](https://sia.hackernoon.com/do-hiring-managers-value-side-projects-fi103wrs)
- Many portfolios lack end-to-end ownership: API, UI, deployment and observability. One guide recommends 3–5 polished projects that cover the lifecycle, including deployment and monitoring. — [DataExpert.io guide, Mar 2026](https://www.dataexpert.io/blog/ultimate-guide-ai-engineering-portfolios) (vendor/bootcamp source)
- One vendor blog claims recruiters engage 80% more with GitHub projects that have runnable code or live demos, and that recruiters scan a portfolio for 6–10 seconds. These figures are unverified and single-sourced. — [DataExpert.io](https://www.dataexpert.io/blog/ultimate-guide-ai-engineering-portfolios); [Upskillist](https://www.upskillist.com/blog/10-ai-portfolio-examples-impress-recruiters/)
- Evals are the "section almost no candidate has" and "the single highest-leverage thing you can add." An eval here means test inputs, the property each output should have, and a script that scores the pass rate. — [ai-tldr.dev](https://ai-tldr.dev/learn/building-ai-apps/ai-career-path/build-ai-portfolio/) (search excerpt)
- Hamel Husain's thesis: unsuccessful AI products almost always share one root cause, which is failing to build robust evaluation systems. On past projects, 60–80% of development time went to error analysis and evaluation. He describes three eval levels: code assertions and unit tests, human or LLM-judge evaluation, and A/B tests against user outcomes. — [Antoine Buteau summary](https://www.antoinebuteau.com/lessons-from-hamel-husain.md); [HeroHunt 2026 guide](https://www.herohunt.ai/blog/how-to-recruit-ai-evals-engineers-2026/)
- A 2026 roadmap says job posts began listing evals experience explicitly, and that cost optimisation and observability rose to core-skill status. This is narrative, not a counted dataset. — [youngju.dev, Jul 2026](https://www.youngju.dev/blog/culture/2026-07-02-how-to-become-ai-engineer-2026-llm-rag-agents-evals-career-roadmap-deep-dive.en)
- Résumés are increasingly AI-generated, so hiring has shifted toward referrals, personal projects, live assessments and in-person interviews. — [Gauntlet AI](https://gauntletai.com/night-school/what-hiring-managers-actually-look-for-in-ai-engineers) (search excerpt)
- Senior observability job postings stress production debugging, SLOs and alerting, telemetry pipelines and "dashboards as code." This shows what employers value, not how they judge portfolios. — [Honeycomb posting](https://job-boards.greenhouse.io/honeycomb/jobs/5132852008); [builtin](https://builtin.com/job/senior-full-stack-engineer/3859118)

### Inferences
- For a Brazilian senior engineer applying abroad, a portfolio does a different job than for a junior. It cuts the "unknown candidate" risk for overseas employers and gives interviewers concrete material for deep design discussion. Depth beats breadth: 1–3 flagship projects are better than 10 demos.
- The credibility bundle a senior project should carry, combining the sources above:
  - a live deployment
  - a README that opens with the problem, the architecture diagram and the numbers
  - ADRs, which turn trade-off discussion into an artifact for tech-lead roles
  - tests in CI
  - OpenTelemetry traces and dashboards
  - load-test results (k6) with p95/p99 latency and cost per request or task
  - for AI projects, an eval suite with tracked pass rates and an error-analysis write-up
  - a blog post explaining the design decisions
- Framing tip: present each project as "problem → constraints → decisions → measured result," the same shape as impact bullets on a senior résumé.

### Gaps
- I found no rigorous survey or primary hiring-manager dataset on how much portfolios weigh in senior US/EU hiring. Evidence is mostly anecdotal or from vendors.
- I could not fetch the full r/ExperiencedDevs or HN threads. Only recaps or excerpts were available.
- I found no source that specifically names ADRs or load tests as hiring-manager signals. These are inferred from senior job requirements.

## 2. Which AI project types stand out, and which are saturated?

### Takeaway
A plain "chat with your docs" RAG bot is the "hello world" of GenAI and does not differentiate a candidate. Sources consistently point to these as differentiators:
- evaluation and error analysis
- agents built from simple, composable patterns with tools
- MCP servers and integrations
- durable or long-running agent workflows
- observability and cost control
- production concerns such as multi-tenancy and security

### Cited Findings
- A document RAG chatbot is called "the 'hello world' of GenAI engineering." — [Careery 2026](https://careery.pro/blog/ai-careers/ai-engineer-project-ideas)
- A niche corpus you know well beats a generic PDF, because you'll notice when answers are subtly wrong, "and noticing is the skill." — [ai-tldr.dev](https://ai-tldr.dev/learn/building-ai-apps/ai-career-path/build-ai-portfolio/) (search excerpt)
- Strong projects "go beyond generic chatbot demos." They show a user problem, application code, data or document context, and evaluation. Source citation (page and paragraph) is suggested as an upgrade for document chat. — [DataTalks.Club podwiki](https://datatalks.club/podwiki/wiki/ai-engineering-portfolio-projects/); [Scaler 2026](https://www.scaler.com/blog/10-ai-portfolio-projects-to-land-your-dream-job-2026/)
- Anthropic reports that across dozens of teams, the most successful agent builds used "simple, composable patterns," not complex frameworks. It distinguishes workflows (predefined code paths) from agents (the LLM directs its own process). The named patterns are prompt chaining, routing, parallelization, orchestrator-workers and evaluator-optimizer. — [Anthropic, Building effective agents](https://www.anthropic.com/research/building-effective-agents)
- MCP adoption:
  - About 97M monthly SDK downloads across Python and TypeScript, from Anthropic's December 2025 ecosystem update, up from about 2M at launch in November 2024.
  - More than 10,000 active public servers.
  - A May 2026 snapshot counted 9,652 latest records in the official registry.
  - 41% of surveyed software organisations ran MCP servers in limited or broad production (Stacklok 2026).
  - Reports say MCP was donated to the Linux Foundation in December 2025, but that claim is single-sourced.
  - Reports also say a large share of public servers had exploitable flaws, which makes security a gap a project can fill (single-sourced).
  — [digitalapplied MCP stats 2026](https://digitalapplied.com/blog/mcp-adoption-statistics-2026); [dev.to](https://dev.to/akaranjkar08/mcp-hit-97m-downloads-what-developers-need-to-know-in-2026-1552); [algeriatech.news](https://algeriatech.news/mcp-97-million-installs-2026/)
- One course page claims 1,000+ job postings mentioned MCP in February 2026, with TypeScript or Python in 95% of them. The method is unverified. — [mejba.me](https://www.mejba.me/ai-school/master-mcp-servers-build-ai-powered-tools-integrations/lessons/mcp-career-mastery/mcp-job-market-2026)
- Durable execution for agents:
  - Long agent runs fail partway through. Durable platforms persist each step and retry only the failed part.
  - The shared rules: LLM outputs are recorded once and replayed (never re-called) on recovery, workflow code must be deterministic, and side-effecting tool calls must be idempotent.
  - Temporal: the TypeScript SDK has determinism constraints, and large LLM payloads can saturate workflow history, which calls for payload codecs.
  - Inngest: the fastest path from TypeScript app code via `step.run()`, though billed steps grow with retries.
  - Alternatives: Trigger.dev, Restate and Vercel Workflow.
  — [noqta.tn 2026](https://www.noqta.tn/blog/durable-execution-ai-agents-inngest-trigger-temporal-2026); [ZenML](https://www.zenml.io/blog/inngest-vs-temporal); [alexcloudstar 2026](https://alexcloudstar.com/blog/temporal-vs-inngest-vs-vercel-workflow-2026/)
- Python is the default AI-engineering language and TypeScript the second working language. Model, data and eval ecosystems live mainly in Python. — [youngju.dev 2026](https://www.youngju.dev/blog/culture/2026-07-02-how-to-become-ai-engineer-2026-llm-rag-agents-evals-career-roadmap-deep-dive.en)
- Market signals:
  - A 365 Data Science study of 903 US Glassdoor AI-engineer postings found only 2.5% target juniors (0–2 years).
  - CompTIA (reported secondhand) says dedicated AI roles grew 81% year over year.
  — [365 Data Science](https://365datascience.com/career-advice/career-guides/ai-engineer-job-outlook-2025/)
- Eval-focused open-source companies are hiring remote AI engineers. Arize posted an "Open Source AI Engineer – Evals" role at $185k–200k, and Confident AI (DeepEval) a founding OSS role with a paid work trial. — [builtin/Arize](https://builtin.com/job/open-source-ai-engineer-evals/4217931); [YC/Confident AI](https://www.ycombinator.com/companies/confident-ai/jobs/4OrG8Sb-founding-open-source-growth-engineer)

### Inferences: saturated vs. differentiating
- **Saturated:** generic PDF or website chatbots, ChatGPT wrappers, "AI SaaS" clones, notebooks on Kaggle or Titanic datasets, and LangChain tutorial agents with no evals.
- **Differentiating, in rough order of senior signal:**
  1. eval harnesses with error analysis
  2. multi-tenant RAG with access control and citations
  3. AI gateways with routing, caching, budgets and fallbacks
  4. production-grade MCP servers with auth, permissions, audit and tests
  5. durable agent workflows with human-in-the-loop
  6. LLM observability and cost dashboards
  7. voice or realtime agents (latency engineering)
  8. coding or ops agents working on real systems
- Node.js angle: TypeScript is the "second language" of AI engineering. A Node specialist stands out by owning the production layer around models: gateways, workflows, multi-tenancy, observability, MCP servers and streaming APIs. Pairing this with a small Python eval or notebook component shows range.

### Concrete project archetypes and suggested stacks
These are my synthesis. Each maps to a trend cited above, but no single source prescribes this list.

1. **Eval harness and CI regression gate for an LLM feature.**
   - Stack: TypeScript with promptfoo or a custom runner, Vitest, a curated golden dataset, LLM-as-judge with agreement checks against human labels, and a GitHub Actions gate that fails a PR when the pass rate drops.
   - Publish: an error-analysis write-up (Husain-style).
2. **Multi-tenant RAG with document-level access control and citations.**
   - Stack: NestJS or Fastify, Postgres + pgvector with row-level security, hybrid BM25 + vector retrieval with a reranker, per-tenant ACL filtering at query time, citations down to page and paragraph, and a retrieval eval (recall@k, faithfulness).
3. **AI gateway / LLM proxy.**
   - Stack: Fastify, Redis for semantic and exact caching, per-tenant rate limits and token budgets, provider fallback/routing (OpenAI, Anthropic, local), streaming SSE pass-through, OpenTelemetry GenAI semantic conventions, and k6 load tests with p95 overhead numbers.
   - Compare against LiteLLM and Portkey in an ADR.
4. **Production MCP server for a real domain** (an internal API, Postgres, a SaaS).
   - Stack: `@modelcontextprotocol/sdk` (TypeScript), Streamable HTTP transport, OAuth, scoped tools, audit logging, input validation with Zod, contract tests, and publication to the MCP registry.
   - Include a threat model (prompt injection, tool poisoning), given the security findings cited above.
5. **Durable agent workflow with human-in-the-loop approval.** Example: refund or claims processing, or invoice extraction then approval then ERP posting.
   - Stack: Temporal TypeScript SDK or Inngest, idempotent tools, replay-safe LLM steps, a dashboard, and a demo of chaos testing (kill the worker mid-run).
6. **Tool-using agent built from Anthropic's composable patterns**, compared against a framework.
   - Stack: Vercel AI SDK or the plain provider SDK, then the same task in Mastra or LangGraph.js. Report cost, latency and success rate on an eval set.
7. **LLM observability / cost analytics service.**
   - Stack: OpenTelemetry collector, ClickHouse, Grafana, Node ingestion; or self-hosted Langfuse with custom dashboards. Track cost per tenant, cost per successful task and drift alerts.
8. **Realtime voice agent** (for example, scheduling or customer support in PT/EN).
   - Stack: LiveKit Agents JS or the OpenAI Realtime API over WebRTC/WebSockets, Node backend, tool calls into a booking system. Measure turn-taking latency budgets and barge-in handling.
9. **Event-driven backend at scale with an AI enrichment step.** This is the core senior Node signal.
   - Stack: NestJS microservices, Kafka or NATS, an outbox pattern, idempotent consumers, a dead-letter queue, an LLM classification/enrichment stage with batching and cost caps, Kubernetes/Helm or Fly.io, and k6 load tests with documented throughput.
10. **Structured data extraction pipeline with validation.** Example: invoices, contracts, or Brazilian documents such as NF-e and boletos, which make good niche corpora.
    - Stack: AI SDK `generateObject` with Zod schemas, a retry/repair loop, and field-level accuracy evals against a labelled set.
11. **Coding or ops agent for a real workflow.** Examples: a PR-review bot, an incident-triage agent reading logs and metrics through MCP.
    - Stack: GitHub App with Probot or Octokit, sandboxed execution, and evals on historical PRs or incidents.
12. **Agentic workflow engine with guardrails.**
    - Stack: policy layer for PII redaction, output validation, injection detection, rate and budget limits. Package it as an npm library with docs and semver releases. The library-maintainer signal matters here.
13. **Multi-tenant SaaS starter for AI features**, as an open-source template.
    - Stack: auth, billing/usage metering per token, tenant isolation, feature flags, OpenTelemetry, and IaC (Terraform). This is valuable for showing tech-lead "platform" thinking.
14. **Benchmark or reproducible study write-up.** Examples: "pgvector vs. dedicated vector DB at 10M vectors," or "streaming latency across providers from São Paulo vs. us-east."
    - Stack: a public repo with scripts and a blog post. It works as a standalone credibility piece for writing and measurement.
15. **Local-first / on-prem LLM service.**
    - Stack: Ollama or vLLM behind a Node gateway, quantised models, a cost comparison against API models, and a privacy/compliance (LGPD/GDPR) ADR. This is relevant to EU employers.

### Gaps
- I found no hiring-manager quote that explicitly ranks these archetypes against each other. The ranking above is inference.
- MCP job-posting numbers come from a course page and are unverified. MCP adoption numbers rely on secondary blogs citing Anthropic's December 2025 update.
- I found no data on voice-agent demand specifically.

## 3. Which open-source ecosystems are good for contributions?

### Takeaway
TypeScript AI tooling is large and actively growing, which makes it a good target for meaningful, discussable contributions. The candidates are the MCP TypeScript SDK, the Vercel AI SDK, Mastra, LangChain.js / LangGraph.js, and eval/observability tools (promptfoo, Langfuse). Classic backend projects (NestJS, Fastify, Node core) carry senior-backend signal. Contributions must be substantive and well understood: not typos or dependency bumps.

### Cited Findings
- MCP SDKs: about 97M monthly downloads across Python and TypeScript (December 2025). A TypeScript SDK is official. — [digitalapplied](https://digitalapplied.com/blog/mcp-adoption-statistics-2026)
- The Vercel AI SDK (`ai` on npm) gets roughly 11–21M weekly downloads, depending on the snapshot. Stork.ai cites 15.1M weekly as of June 2026. Sources conflict, and the PkgPulse figure of about 1.5M looks like an outlier. — [Stork.ai](https://www.stork.ai/en/ai-sdk-vercel); [Snyk](https://security.snyk.io/package/npm/ai); [Socket](https://socket.dev/npm/package/ai/overview/5.0.270)
- Mastra:
  - Open-source TypeScript agent framework from the Gatsby team, Apache-2.0 core.
  - v1.0 shipped in January 2026.
  - Reported star counts range from about 19k (at v1.0) to about 26–28k (mid/late 2026), with 300k+ weekly npm downloads.
  - 300+ contributors as of the October 2025 seed round.
  — [AI Agent Index](https://theaiagentindex.com/agents/mastra); [OSS Insight](https://ossinsight.io/analyze/mastra-ai/mastra); [agenticwire](https://www.agenticwire.news/article/mastra-framework-open-source-ai-tooling-heats-up)
- A CTO (Arjé Cahn, Hippo) says open source lets you "see the quality of code the developers are writing without having them even walk into the office," and that some of their best hires came this way. — [Terminal.io](https://www.terminal.io/blog/five-ways-open-source-can-boost-your-skills-and-portfolio)
- Merged PRs make international applicants look less like a "risky unknown" (vendor opinion). — [F1Jobs 2026](https://www.f1jobs.io/resources/blog/open-source-contributions-international-job-seekers)
- Quality bar: one hiring posting explicitly excludes documentation updates, dependency bumps, formatting and typo fixes, and expects candidates to discuss their PRs in detail. — [RemoteJobs.org / micro1](https://remotejobs.org/remote-jobs/open-source-contributor-github-micro1)
- Eval OSS companies (Arize Phoenix, Confident AI's DeepEval) hire open-source engineers directly. Contributing to them is a direct hiring path. — [builtin/Arize](https://builtin.com/job/open-source-ai-engineer-evals/4217931); [YC/Confident AI](https://www.ycombinator.com/companies/confident-ai/jobs/4OrG8Sb-founding-open-source-growth-engineer)

### Inferences
- Best ROI for a Node + AI profile:
  - (a) MCP TypeScript SDK: transports, auth and examples. The spec is evolving, so new features need implementations.
  - (b) Vercel AI SDK: provider adapters, bugs in streaming and tool calling.
  - (c) Mastra: young and fast-moving, so maintainers are reachable and issues are plentiful.
  - (d) promptfoo / Langfuse JS SDK: eval and observability integrations.
  - (e) NestJS or Fastify plugins (for example, an OpenTelemetry or LLM plugin), which keep backend credibility.
- Node core is the highest prestige but slowest path. It suits someone aiming for runtime or performance roles.
- Writing and maintaining a small, focused npm package that others actually depend on (an MCP server, a provider adapter, a NestJS module) can be stronger than scattered PRs. Download counts are a citable metric.

### Gaps
- GitHub API access was blocked, so I could not verify current star counts or good-first-issue counts for the MCP SDK, AI SDK, LangChain.js, NestJS, Fastify or Node.
- I found no data quantifying how much open-source contributions affect senior or international hiring outcomes.

## 4. Examples of strong portfolios or projects from engineers who got hired

### Takeaway
I found no verifiable, well-documented 2025-2026 case of a "project X led to a senior offer" for Node/AI roles. The best evidence is indirect: companies hiring through OSS contribution or paid trials, and portfolio guides describing production-grade RAG portfolios.

### Cited Findings
- One example is a production-grade AI portfolio with "agentic RAG" (the santifer CV project), described as a showcase of deployment and architecture. It is a blog write-up, not hiring evidence. — [brightcoding](https://prompts.brightcoding.dev/blog/santifercv-santiago-production-grade-ai-portfolio-with-agentic-rag)
- An Educative piece is titled "the AI project that got me hired as an ML engineer." The content was not retrieved and is likely promotional. — [Educative](https://learn.educative.io/the-ai-project-that-got-me-hired-as-an-ml-engineer)
- Confident AI's hiring process goes screen, technical interview, paid work trial, then offer. This shows OSS-adjacent practical evaluation. — [YC](https://www.ycombinator.com/companies/confident-ai/jobs/4OrG8Sb-founding-open-source-growth-engineer)
- Chip Huyen (via Pragmatic Engineer) frames AI engineers as often regular software engineers who have mastered LLM basics. This supports the idea that backend seniors can pivot by showing production LLM work. — [Pragmatic Engineer: The AI Engineering Stack](https://newsletter.pragmaticengineer.com/p/the-ai-engineering-stack)
- The Latent Space "Rise of the AI Engineer" essay (2023) defines the role as applying foundation models through APIs and open-source tools, including product-specific data and evals. — [Latent Space about](https://www.latent.space/about)

### Inferences
- The recurring pattern in credible public examples is that the engineer published writing about measured results (benchmarks, evals, post-mortems) alongside code. Simon Willison's and Hamel Husain's public work are the reference models for "learning in public," but I have no source tying them to hiring outcomes.

### Gaps
- I found no first-person, verifiable 2025-2026 accounts of senior Node.js or AI engineers hired through a specific portfolio project. Reddit and HN threads could not be fetched. This is a significant gap. The report should not claim specific success stories.
