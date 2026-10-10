# Senior / Staff / Tech Lead Backend Node.js: 2026 job market in developed countries plus remote LATAM

Research date: 2026-10-10. Main method: full job descriptions pulled through the Indeed job-search API (US, UK, IE, DE, NL, SE, CA, AU, CH), plus web searches for HN "Who is hiring", ATS boards, salary data and survey data.

Limits on method: WebFetch and direct HTTP failed for every non-search domain in this environment (DNS errors / proxy 403 for hn.algolia.com, hnhiring.com, jobs.ashbyhq.com, hiringlab.indeed.com, howdy.com, himalayas.app). So ATS/HN/salary-report items below come from search-engine summaries, not full-page reads, and are marked that way. LinkedIn, StepStone, Seek, Otta/WTTJ and Wellfound could not be read directly.

Frequency counts use a sample of **17 postings whose full job descriptions I read** (listed under Q5, items 1–17). It is a small convenience sample, not a statistical sample. Read the percentages as directional only.

---

## Q1. Which technologies appear most in real postings?

### Takeaway
In 2026 senior Node postings, **TypeScript is effectively mandatory (15/17)**. Most also ask for **containers/Kubernetes (9/17)**, **CI/CD (10/17)**, **a relational DB, usually PostgreSQL (7/17), with MongoDB close behind (5/17)**, **AWS as the default cloud (7/17)**, and **distributed systems / microservices / event-driven experience (7/17)**. Specific Node frameworks are rarely named: NestJS 1/17 (plus Solace on HN), Express 1/17, Fastify 0. gRPC appeared in 0/17 and DDD in 0/17. A second backend language is common: Python 6/17, Rust 4/17, Go 2/17.

### Cited Findings
Tally over the 17 full JDs (sources listed in Q5):
- **TypeScript** named: 15/17 (Mimica, Visionomics, Radar, n8n, FUNKE, Cpl-Dublin contract, Grainger, Wolters Kluwer, imgix, Luxury Escapes, Palmstreet, RiseRank, TV4, Hoffmann, Cpl-Dublin GCP). Not named: Propeller ("Node.js and/or Python"), eBay (Java-first).
- **Node frameworks**: NestJS only at FUNKE ("fundierte praktische Erfahrung mit Node.js, TypeScript und NestJS") — [FUNKE/Indeed](https://to.indeed.com/aavcjy642tks). Express + Prisma at RiseRank — [RiseRank/Indeed](https://to.indeed.com/aawkyvfz89n2). Solace Health's HN Oct-2026 post lists a "TypeScript with NestJS and Node, PostgreSQL, GCP" stack — [HN Who is hiring Oct 2026](https://news.ycombinator.com/item?id=49922569) (via search summary). No posting named Fastify.
- **Databases**: PostgreSQL 7/17 (Mimica, Cpl contract, imgix, Luxury Escapes, RiseRank, TV4, eBay). MongoDB 5/17 (Mimica, Radar, Cpl contract, Grainger, eBay). DynamoDB/DocumentDB 2/17 (Wolters Kluwer, TV4). OpenSearch/Elasticsearch 3/17 (WK, Luxury Escapes, TV4). SQL Server 1 (Cpl contract).
- **Redis** 3/17 (Radar, Cpl contract, RiseRank). Trigger.dev's Senior Backend Engineer (Europe) on Ashby also lists Node.js, TypeScript, Postgres, Redis — [Trigger.dev/Ashby](https://jobs.ashbyhq.com/triggerdev/6f0f1783-fb08-4ec6-97d1-3f2c26005faf) (search summary only).
- **Messaging / queues** 3/17. Grainger: Kafka plus AWS SQS/SNS/SES/Lambda, "event driven data streaming architectures" — [Grainger/Indeed](https://to.indeed.com/aatcrxqc4x9v). Luxury Escapes: AWS SQS, SNS, S3, Lambda — [Luxury Escapes/Indeed](https://to.indeed.com/aaq72xzwckvk). eBay: "Kafka, RabbitMQ, or similar" — [eBay/Indeed](https://to.indeed.com/aapktfqm9p7z).
- **Cloud**: AWS 7/17 (Radar, Grainger, WK, Luxury, RiseRank, TV4; FUNKE as alternative). GCP 4/17 (FUNKE, imgix, Cpl-GCP, WK). Azure 3/17 (Cpl contract, Hoffmann, WK). WK lists all three.
- **Docker / Kubernetes / containers** 9/17 (Mimica, Radar [EKS], FUNKE, Grainger, WK, Palmstreet, RiseRank, TV4, Hoffmann).
- **Terraform / IaC** 4/17. Radar: "Everything is deployed to AWS via Kubernetes on EKS using Terraform" — [Radar/Indeed](https://to.indeed.com/aark4mkvqz4w). Also WK, TV4, and Hoffmann ("Infrastructure as Code").
- **Serverless (Lambda)** 2/17 (Grainger, Luxury Escapes). HN Oct-2026: PAGNOS is hiring for "AWS serverless with TypeScript/Node" at €75–80k (requires German) — [HN Oct 2026](https://news.ycombinator.com/item?id=49922569) (search summary).
- **GraphQL** 4/17. Visionomics: "REST and GraphQL… GraphQL on Node.js (schema design, resolvers, federation) is a plus" — [Visionomics/Indeed](https://to.indeed.com/aaffwtrqd24s). Also Cpl contract, imgix, and eBay ("Federated GraphQL APIs is highly desirable").
- **gRPC**: 0/17.
- **Observability**: named tools in 4/17. n8n: OpenTelemetry, Prometheus, Grafana (nice-to-have) — [n8n/Indeed](https://to.indeed.com/aahdpycvbgq9). TV4: Grafana, OpenTelemetry — [TV4/Indeed](https://to.indeed.com/aafh24d4hrwm). Grainger: Datadog. WK: "observability… cost and quality telemetry" — [Wolters Kluwer/Indeed](https://to.indeed.com/aas69zbmcqf4). Generic "monitoring / instrument what you ship" appears in about 4 more.
- **Testing** explicit in 8/17. Luxury Escapes: "test-driven development". RiseRank: Jest. imgix: "Champion our testing culture" — [imgix/Indeed](https://to.indeed.com/aarp89smh62j). Also FUNKE, Cpl contract, Grainger, WK, n8n.
- **CI/CD** explicit in 10/17 (TV4 and WK name GitHub Actions).
- **Microservices / distributed systems / event-driven** 7/17. Mimica: "microservices, load balancing, caching, horizontal/vertical scaling and stateless architectures" — [Mimica/Indeed](https://to.indeed.com/aad4frqyfplc). Grainger: "leading the evolution of monoliths to microservices".
- **DDD** named in 0/17.
- **Second language**: Python 6/17, Rust 4/17 (Visionomics, Radar, WK, TV4), Go 2/17, Java/Kotlin in Grainger and eBay, PHP/Symfony at FUNKE.
- **Fullstack drift**: React/Vue/Next.js/React Native appear in 8/17 even when the title says senior backend (n8n, imgix, Luxury, RiseRank, Hoffmann, Cpl-GCP, WK, Grainger "working knowledge of front end").
- Macro context: about 48.7–49.1% of respondents in the Stack Overflow 2025 survey use Node.js. The two figures come from secondary summaries and I could not confirm them against the official page — [dev.to summary](https://dev.to/davidshq/thoughts-on-stackoverflow-2025-developer-survey-part-1-3d5o); [survey.stackoverflow.co/2025](https://survey.stackoverflow.co/2025/).

### Inferences
- Postings name a Node framework far less often than expected. Employers screen for TypeScript + Postgres/Mongo + cloud + containers + distributed systems, not for NestJS or Fastify. NestJS is the most visible framework in the Europe/HN sample.
- "Senior Backend Node" postings increasingly expect T-shaped engineers who can work in a second backend language (Python for AI work, Rust/Go for performance) and do some frontend.
- gRPC and DDD do not work as screening keywords in this sample. They may still come up in system design interviews.

### Gaps
- Could not run large-N keyword frequency counts on LinkedIn, StepStone, Seek or Otta because pages were not fetchable. The n=17 percentages are not statistically robust.
- Could not read the official Stack Overflow 2025 TypeScript usage percentage.

---

## Q2. What do Tech Lead / Staff / Principal postings add?

### Takeaway
Staff, Lead and Principal postings add **ownership of system design across teams** (design docs, design reviews, trade-offs that include **cost**), **mentoring and pairing**, a **"you build it, you run it"/on-call** mindset, **driving migrations** such as monolith to microservices, **hiring/onboarding**, and often **steering AI tooling or agentic platforms**. They typically ask for 8+ years.

### Cited Findings
- eBay Staff SWE (Amsterdam, Sep 2026): "write technical design documents, leading design reviews… evaluating trade-offs (consistency, availability, latency, cost) and driving technical alignment across teams"; 8+ yrs; mentoring — [eBay/Indeed](https://to.indeed.com/aapktfqm9p7z).
- Grainger Staff Tech Lead (US remote, Apr/Sep 2026): "Own engineering culture… Mentor developers, conduct code reviews… pair programming… Drive complex technical initiatives in partnership with Architects… leading the evolution of monoliths to microservices and shaping cross-team technical strategies"; "Maintain software in production… triage" — [Grainger/Indeed](https://to.indeed.com/aatcrxqc4x9v).
- Wolters Kluwer Principal (NL, remote US/EU, Mar 2026): "drive architecture, mentor engineers, and take ownership of larger projects"; secure SDLC, threat modeling, least privilege; "lower cost per query"; 8+ yrs; interview = 2 live coding rounds, 1 system design, 1 presentation of past work, plus a written "Statement of Exceptional Work" — [WK/Indeed](https://to.indeed.com/aas69zbmcqf4).
- Mimica Staff/Senior (UK/IE remote, Jul 2026): 8+ yrs; "Contributing to architectural decisions"; "taking operational responsibility for what you build"; "Participating in hiring and onboarding… end-to-end project management" — [Mimica/Indeed](https://to.indeed.com/aad4frqyfplc).
- Radar Senior/Staff (NYC/US remote, May 2026): "Most engineers are in the on-call rotation"; interviews are a code screen, coding round and system design round — [Radar/Indeed](https://to.indeed.com/aark4mkvqz4w).
- TV4 Sr. Engineer Systems & AI (Stockholm, Aug 2026), a staff-like cross-team role: "architecture decisions that affect several teams"; hands-on prototyping; evaluating agent-driven development for the org (translated from Swedish) — [TV4/Indeed](https://to.indeed.com/aafh24d4hrwm).
- FUNKE Senior (Berlin): "You build it, you run it… Betrieb, Monitoring und Fehlerbehebung" — [FUNKE/Indeed](https://to.indeed.com/aavcjy642tks).
- Hoffmann Group Senior (Munich): "Technologische Gesamtverantwortung für Architektur, Technologiestack und Qualitätsstandards"; steering external developers — [Hoffmann/Indeed](https://to.indeed.com/aarlqnws9lcr).
- Mentoring or coaching appears in 11/17 postings, senior titles included (Propeller: "Mentor and guide mid-level engineers" — [Propeller/Indeed](https://to.indeed.com/aagbkjpzczqc)).
- On-call / operating production is explicit in 5/17 (Radar, imgix L3 on-call, FUNKE, Mimica, Grainger).

### Inferences
- Most postings did not use the word "RFC". The equivalent artifacts named are "technical design documents" and "design reviews". Cost appears explicitly at eBay (trade-offs) and WK (cost per query, cost telemetry).
- For a portfolio, Staff-level signals would be written design docs/ADRs, a cost analysis, an observability/on-call runbook, and a migration story.

### Gaps
- No Staff posting in the sample published FinOps/cloud-cost ownership as a primary duty. "RFC" as a term was not found.

---

## Q3. How often do Node backend postings mention LLMs, agents, RAG, vector DBs and AI coding tools?

### Takeaway
AI is now common. **10/17 postings mention AI in some form**. **7/17 explicitly expect daily use of AI coding tools** (Claude Code is named in 5, Codex in 3, Copilot and Cursor in 1 each). **6/17 involve building LLM/agent features**. Only **1/17 (Wolters Kluwer) asks for RAG + vector search + LangGraph + MCP** in depth. Postings without AI mentions are mostly traditional enterprise, agency or onsite roles (Luxury Escapes, Cpl contract, Grainger, RiseRank, Palmstreet, Propeller, Cpl-GCP).

### Cited Findings
- **AI coding tools expected**:
  - Radar: "Engineers choose what AI tools they use, Claude and Codex being the most popular… actively building Claude skills… Claude and Codex also review all PRs" — [Radar/Indeed](https://to.indeed.com/aark4mkvqz4w).
  - imgix: "Use Claude Code, Codex, Gemini, or similar daily… review an AI-generated pull request… Fluent use of AI coding assistants in real production work—you can speak specifically to how you use them, where they help, and where they don't" — [imgix/Indeed](https://to.indeed.com/aarp89smh62j).
  - eBay Staff: "AI-assisted development tools (e.g., GitHub Copilot, Claude Code)… (e.g., GitHub Copilot, Cursor, Claude Code, or equivalent)" — [eBay/Indeed](https://to.indeed.com/aapktfqm9p7z).
  - TV4: "AI och utvecklarverktyg: Claude Code, OpenAI Codex och CLI/MCP-baserade verktyg"; the team is building an agentic platform; candidates should be "actively exploring agent-driven development" — [TV4/Indeed](https://to.indeed.com/aafh24d4hrwm).
  - Hoffmann: "Erfahrung im produktiven Einsatz KI-gestützter Entwicklungstools wie Claude" — [Hoffmann/Indeed](https://to.indeed.com/aarlqnws9lcr).
  - FUNKE: "Verantwortungsvoller Einsatz von AI-gestützten Entwicklungstools" — [FUNKE/Indeed](https://to.indeed.com/aavcjy642tks).
  - Visionomics: "use generative AI tools to improve engineering productivity" — [Visionomics/Indeed](https://to.indeed.com/aaffwtrqd24s).
- **LLM / agents / RAG in the product**:
  - Wolters Kluwer: "LangChain/LangGraph, MCP/A2A… Azure OpenAI, AWS Anthropic, Google Gemini… Apply current LLM patterns (RAG, retrieval, routing, tool-use, evals)… evals, canaries… cost and quality telemetry"; nice to have "vector/RAG systems; OpenSearch"; hallucination reduction — [WK/Indeed](https://to.indeed.com/aas69zbmcqf4).
  - Visionomics: "integrate advanced capabilities such as Generative AI into production services".
  - eBay: "LLM integrations… agentic workflows".
  - imgix: "Experience integrating LLM APIs (Anthropic, OpenAI, etc.)" (nice-to-have).
  - Mimica: Node APIs "to interact with the various ML components"; the product "generates the AI agents".
  - TV4: agentic platform.
  - n8n's product is "AI workflow orchestration", but the role JD focuses on enterprise IAM, observability and APIs.
- **Vector DB** named explicitly: only WK (OpenSearch / Azure AI Search, "vector/RAG systems"). None of the 17 named pgvector, Pinecone, Weaviate or Qdrant.
- **Counter-signal**: WK bans AI assistance during interviews ("use of AI-generated responses… will be grounds for disqualification") — [WK/Indeed](https://to.indeed.com/aas69zbmcqf4).
- Market-level: Indeed Hiring Lab (Jul 8, 2026) reports that 71% of the increase in software development postings May 2025→May 2026 came from senior roles, and 37% from jobs with AI in the title. One secondary summary instead frames it as "37% of new software postings mention AI in the job title", so the framing is disputed — [Indeed Hiring Lab, Jul 2026](https://hiringlab.indeed.com/2026/07/08/ai-and-job-postings-from-destruction-to-creation/) (search summary; page not fetchable). The Indeed AI tracker share across all postings peaked at 4.2% at end-2025 — [Indeed Hiring Lab Jan 2026](https://hiringlab.indeed.com/2026/01/22/january-labor-market-update-jobs-mentioning-ai-are-growing-amid-broader-hiring-weakness/) (search summary).
- Developer side: Stack Overflow 2025 found 84% using or planning to use AI tools, 51% of professional developers using them daily, and only 3% highly trusting AI output (secondary summaries) — [eng-leadership newsletter](https://newsletter.eng-leadership.com/p/the-state-of-software-development); [survey.stackoverflow.co/2025](https://survey.stackoverflow.co/2025/).

### Inferences
- The baseline expectation for a senior/staff Node engineer in 2026 is **fluent and critical use of AI coding agents**, especially Claude Code: knowing where the tools fail, reviewing AI-generated PRs, and writing skills/MCP tools. Deep RAG/vector expertise is a differentiator for AI-platform roles, not a baseline.
- MCP shows up in both product-side (WK) and tooling-side (TV4) postings. A Node MCP server project would map directly onto both.
- Interviews may still prohibit AI, so unassisted fundamentals (live coding, system design) still matter.

### Gaps
- No reliable large-N statistic exists for "% of Node backend postings mentioning LLM/RAG/vector DB". The Indeed Hiring Lab software-specific share could not be confirmed from the primary page.

---

## Q4. Salary ranges per country and for remote LATAM contractors

### Takeaway
Posted bands in this sample: **US senior $150–210k base, US staff/lead $200–300k**, **Canada senior CAD 200–250k** (a remote outlier), **Ireland senior €85–110k**, **EU remote (n8n) €73–144k**. Benchmarks give **Germany senior €88–135k** and **UK senior £90–130k**. For **remote LATAM/Brazil**, senior Node work typically lands around **US$45–78k/year** or **about US$40–80/h** (the Visionomics US-remote contract pays $50–80/h). Quality of the Brazil data is mixed.

### Cited Findings
**Posted ranges (2026 postings):**
- US: Radar Senior/Staff $200–300k + equity (NYC / US remote) — [Radar/Indeed](https://to.indeed.com/aark4mkvqz4w). imgix Senior $180–210k (US remote) — [imgix/Indeed](https://to.indeed.com/aarp89smh62j). Grainger Staff Tech Lead $124.2–207k + up to 15% bonus — [Grainger/Indeed](https://to.indeed.com/aatcrxqc4x9v). Differential Senior SWE (FinTech, Cincinnati) $108–168k — [Indeed](https://to.indeed.com/aadnm6mf664s) (listing only).
- US (HN Oct 2026, search summary): Solace Health (US remote, TS/NestJS/Postgres/GCP) senior backend $150–200k, staff $200–225k, tech lead $200–230k. Manifest senior backend (TS/Node, Go, Python, MongoDB) $150–210k + equity — [HN Who is hiring Oct 2026](https://news.ycombinator.com/item?id=49922569).
- US remote contract: Visionomics Senior Backend (Node/TS/Rust) **$50–80/h**, full-time 40h — [Visionomics/Indeed](https://to.indeed.com/aaffwtrqd24s).
- Canada: Palmstreet Senior+ Backend (Node/TS, remote Canada) **CAD 200–250k** + equity; requires Mandarin — [Palmstreet/Indeed](https://to.indeed.com/aa7nxyv488yk).
- Ireland: Cpl client Senior TS engineer (Node/Next/RN, GCP) **€85–110k** + options; EU citizenship required — [Cpl/Indeed](https://to.indeed.com/aajj7tr6pctk).
- EU remote / Germany: n8n Senior Product Engineer (TS/Node) **€72.8k–144.4k** + equity; sponsors Germany visas — [n8n/Indeed](https://to.indeed.com/aahdpycvbgq9).
- Germany: PAGNOS AWS serverless TS/Node (non-senior title) €75–80k — [HN Oct 2026](https://news.ycombinator.com/item?id=49922569) (search summary).

**Benchmarks (secondary, vendor guides; treat with caution):**
- Germany senior €95–135k base and UK senior £90–130k (Haystack 2026 guide) — [Haystack](https://haystackapp.io/salary-guide/hire-nodejs-engineers). Germany senior €88–115k gross for 5–8 yrs — [GemProgrammers](https://gemprogrammers.com/hire-nodejs-developer-germany/).
- Australia (all levels) AUD 90–130k, median AUD 115k — [Robert Half AU](https://www.roberthalf.com/au/en/job-details/nodejs-developer). Australia senior postings in the sample (Propeller, Luxury Escapes, Sydney) did not publish pay.
- Netherlands senior ~$105k and Canada senior ~$155k (2025 data, USD) — [Mobilunity](https://mobilunity.com/blog/average-node-js-developer-salary/). Another source gives NL at about $69k; the NL figures conflict.
- Switzerland: no Node-specific salary source found.

**Remote LATAM / Brazil:**
- Goldpenguin: senior Brazil remote for US companies $45–75k/yr — [Goldpenguin](https://goldpenguin.org/blog/latam-remote-developer-salaries/).
- Howdy 2026: Brazil senior **$58–78k as all-in employer cost** (includes INSS, FGTS, 13th salary). Brazil is the lowest of 7 LatAm countries at about $54k across levels — [Howdy Brazil](https://www.howdy.com/blog/brazil-software-engineer-salary-hiring-cost-benchmarks); [Howdy LatAm 2026](https://www.howdy.com/blog/latam-software-engineer-cost-benchmarks-2026).
- Arc.dev: Brazil remote devs expect an average of $63,305 in 2026 (self-reported) — [Arc.dev](https://arc.dev/salaries/software-engineers-in-brazil).
- Hourly: an older guide puts Brazil at $40–60/h, with senior LATAM at $65–100/h — via [VanHack](https://blog.vanhack.com/hire-nodejs-developer/) / search summary. Lemon.io's 2026 rate calculator gives a $24–86/h band for Node by seniority/region — [Lemon.io](https://lemon.io/rate-calculator/node-js-developers/).
- LATAM-eligible postings: G2i "Senior Node.js Engineer (LatAm)", contractor, Brazil eligible, posted Mar 2026, no pay listed — [Himalayas/G2i](https://himalayas.app/companies/g2i/jobs/senior-node-js-engineer-latam). "Remote Senior Node.js & TypeScript Engineer (Full-Stack)" tagged LATAM/Mexico, 5+ yrs, Oct 2, 2026 — [freehire](https://freehire.me/jobs/remote-senior-node-js-typescript-engineer-full-stack-lever-inc-btim7t27). Anovium Senior Node backend "remote, global" — [Lever/Anovium](https://jobs.lever.co/Anovium/c55c1aa9-2bb0-4447-bd40-cdc616adb9c2). All three come from search summaries and were not fetched.
- Mimica Staff/Senior Node is remote across UK, Americas and Europe within **UTC-6 to UTC+1**, which covers Brazil (UTC-3) — [Mimica/Indeed](https://to.indeed.com/aad4frqyfplc).

### Inferences
- A senior Brazil-based contractor via Deel/Remote at $50–80/h (about $100–165k/yr) would be at the top of the LATAM market and close to the low end of US posted bands. Typical LATAM senior offers cluster at $45–80k/yr.
- Many US-remote postings (Solace, imgix, Radar, Grainger) are restricted to US residents. LATAM candidates should target postings that say "Americas", "global", or a UTC window, or go through LATAM-focused marketplaces (G2i, Howdy, Arc, Lemon.io, VanHack, Revelo).

### Gaps
- No primary 2026 data on Deel/Remote contractor rates for Brazilian Node engineers specifically.
- No Switzerland or Nordic Node salary data. Swedish postings did not publish pay.
- levels.fyi and Glassdoor could not be fetched.

---

## Q5. Concrete example postings (2026)

### Takeaway
21 concrete postings collected. Items 1–17 had their full JDs read via the Indeed API. Items 18–23 come from search summaries of ATS/HN pages. They cover the US, Canada, UK, Ireland, Germany, the Netherlands, Sweden, Australia and LATAM-remote.

### Cited Findings
1. **Mimica — Staff/Senior Backend Engineer (Node.js)**, London/Dublin, fully remote UK/Americas/Europe UTC-6..+1, posted 2026-07-29. 8+ yrs, TypeScript, Docker/K8s, PostgreSQL/MongoDB, microservices, caching, scaling; real-time backend + APIs to ML components; mentoring, hiring; Python bonus; AI-agent product. — [Indeed](https://to.indeed.com/aad4frqyfplc)
2. **Visionomics (for an enterprise client) — Senior SWE Backend (Node.js, TS, Rust)**, US remote, contract $50–80/h, 2026-10-01. REST + GraphQL (federation plus), HTTP fundamentals, CI/CD, GenAI integration, AI tools for productivity, mentoring. — [Indeed](https://to.indeed.com/aaffwtrqd24s)
3. **Radar Labs — Senior/Staff Product Engineer, Backend**, NYC or US remote, $200–300k + equity, 2026-05-04. Node/TS API layer, Rust DB, MongoDB, Redis, S3/Athena, Airflow, AWS EKS, Terraform, on-call; Claude/Codex; Claude skills; AI PR review; 1B API calls/day. — [Indeed](https://to.indeed.com/aark4mkvqz4w)
4. **n8n — Senior Product Engineer (TS/Node.js/Vue)**, London / EU remote, €72.8–144.4k + equity, 2026-03-04. Node services, RBAC/SSO/SCIM, CI/CD, OpenTelemetry/Prometheus/Grafana (nice), instrumentation, mentoring. — [Indeed](https://to.indeed.com/aahdpycvbgq9)
5. **FUNKE Mediengruppe (erento) — Senior SWE Backend/Fullstack**, Berlin hybrid, 2026-09-29. Node, TS, **NestJS**, PHP/Symfony, GCP/AWS, Docker, CI/CD, automated tests, "you build it you run it", AI tools; German required. — [Indeed](https://to.indeed.com/aavcjy642tks)
6. **Propeller — Senior Backend Engineer**, Sydney hybrid, 2026-08-17. Node.js and/or Python; compute-heavy processing pipelines; architecture; mentoring mid-levels. — [Indeed](https://to.indeed.com/aagbkjpzczqc)
7. **Cpl (client) — Senior Backend Engineer (Node.js)**, North Dublin hybrid, contract, 2026-10-02. 5+ yrs, Node JS/TS, REST/GraphQL, microservices, SQL Server/Postgres/MongoDB, Redis, Azure, CI/CD, Jira/Azure DevOps. — [Indeed](https://to.indeed.com/aac8zg2sd426)
8. **Grainger — Staff Tech Lead (Full Stack)**, US remote, $124.2–207k + 15%, 2026-04-17. AWS SES/SQS/SNS/Lambda, Kafka, MongoDB, Kotlin/Java, TS, K8s, Datadog; monolith→microservices; Node BFF preferred; mentoring. — [Indeed](https://to.indeed.com/aatcrxqc4x9v)
9. **Wolters Kluwer — Principal Full Stack Engineer, AI Platform & Agents**, NL (remote US/EU), 2026-03-04. TS, Node, React, Python, LangChain/LangGraph, MCP/A2A, Rust; AWS/Azure/GCP; Docker, Terraform, GitHub Actions; DynamoDB, DocumentDB, OpenSearch; RAG, evals, cost per query. — [Indeed](https://to.indeed.com/aas69zbmcqf4)
10. **imgix — Senior Software Engineer (Full Stack)**, SF / US remote, $180–210k, 2026-08-24. Python backend (Node devs welcome), Next.js, Postgres, REST/GraphQL, GCP; Claude Code/Codex daily; L3 on-call; LLM APIs nice. — [Indeed](https://to.indeed.com/aarp89smh62j)
11. **Luxury Escapes — Senior Software Engineer**, Sydney onsite, 2026-09-21. Node/TS, React, PostgreSQL, AWS SQS/SNS/S3/Lambda, REST, Elasticsearch/OpenSearch, TDD, CI/CD, microservices, mentoring. — [Indeed](https://to.indeed.com/aaq72xzwckvk)
12. **Palmstreet — Senior+ Backend Software Engineer**, Canada remote, CAD 200–250k + equity, 2026-03-03. Node/TS, scale, K8s, payments; architectural lead; Mandarin required. — [Indeed](https://to.indeed.com/aa7nxyv488yk)
13. **RiseRank — Senior Fullstack Developer (Backend focus)**, Stockholm, 2026-10-09. Node, TS, PostgreSQL, React, Express, Prisma, Redis, REST, AWS, Docker, Jest; 5+ yrs; architecture. — [Indeed](https://to.indeed.com/aawkyvfz89n2)
14. **TV4 — Sr. Engineer Systems & AI (Core)**, Stockholm office-first, 2026-08-26. Go/Rust/Node/TS, AWS, K8s, Terraform, GitHub Actions, Postgres, DynamoDB, OpenSearch, Grafana, OpenTelemetry; Claude Code, Codex, MCP; agentic platform. — [Indeed](https://to.indeed.com/aafh24d4hrwm)
15. **Hoffmann Group — Senior Software Engineer (ToolScout)**, Munich, 2026-09-14. React/TS + Java/.NET/Node, Azure, CI/CD, IaC, containers, monitoring; Claude-type AI tools; architecture ownership; German required. — [Indeed](https://to.indeed.com/aarlqnws9lcr)
16. **eBay — Staff Software Engineer, Marketing Tech**, Amsterdam, 2026-09-09. Java/Spring primary, plus Node.js/Marko/React; Kafka/RabbitMQ; Postgres/Mongo/Cassandra; federated GraphQL; design docs; Copilot/Cursor/Claude Code; LLM/agentic features. — [Indeed](https://to.indeed.com/aapktfqm9p7z)
17. **Cpl (health-tech client) — Senior Software Engineer (React Native, Next.js, Node.js, GCP)**, Dublin hybrid, €85–110k + options, 2026-10-02. TS end to end, APIs, data models, monitoring. — [Indeed](https://to.indeed.com/aajj7tr6pctk)
18. **Solace Health — Senior Backend / Staff / Tech Lead**, US remote, $150–200k / $200–225k / $200–230k, HN 2026-10-01. TS, NestJS, Node, PostgreSQL, GCP. — [HN Oct 2026](https://news.ycombinator.com/item?id=49922569) (search summary)
19. **Manifest — Senior Backend Application Engineer**, $150–210k + equity, HN Oct 2026. TS/Node, Go, Python, MongoDB. — [HN Oct 2026](https://news.ycombinator.com/item?id=49922569) (search summary)
20. **Trigger.dev — Senior Backend Engineer (Europe)**, Ashby. Node.js, TS, Postgres, Redis. — [Ashby](https://jobs.ashbyhq.com/triggerdev/6f0f1783-fb08-4ec6-97d1-3f2c26005faf) (search summary; date not confirmed)
21. **Makai Labs — Senior Backend Software Engineer (Node.js/TypeScript)**, remote, 7+ yrs, regulated environments (healthcare, SOC 2). — [Ashby](https://jobs.ashbyhq.com/makai-labs/badf8c3f-3118-438b-8fec-f595f3f5f552) (search summary; date not confirmed)
22. **G2i — Senior Node.js Engineer (LatAm)**, contractor, Brazil eligible, Mar 2026. — [Himalayas](https://himalayas.app/companies/g2i/jobs/senior-node-js-engineer-latam) (search summary)
23. **"Lever, Inc." — Remote Senior Node.js & TypeScript Engineer (Full-Stack)**, LATAM / Mexico, 5+ yrs, 2026-10-02. — [freehire](https://freehire.me/jobs/remote-senior-node-js-typescript-engineer-full-stack-lever-inc-btim7t27) (aggregator; original not verified)

Also seen (listings only, JD not read): Fanvue Senior Product Engineer (London, Feb 2026), Zalando Senior Fullstack Engineer (Dublin, Sep 2026), Domain Group / CoStar / Abby Health Senior SWE (Sydney, 2026), Avanade AI Full Stack Developer (Toronto, Mar 2026), GitLab Senior Fullstack (TS) AI Engineering (Greenhouse; remote in Canada, Ireland, Netherlands, UK, US; not LATAM) — [GitLab/Greenhouse](https://job-boards.greenhouse.io/gitlab/jobs/8452278002).

### Inferences
- For a Brazil-based candidate, postings that are realistically open are Mimica (UTC-6..+1), Visionomics-type US contracts (eligibility unconfirmed), G2i/LATAM marketplaces and "global remote" roles like Anovium. Most EU/AU postings require local residency, EU citizenship, or German/Swedish language skills (FUNKE, Hoffmann, Cpl-GCP, Luxury Escapes onsite).

### Gaps
- No Swiss Node-backend posting found. Indeed CH returned only frontend/Web3 roles.
- Indeed BR returned 0 results for international-USD Node roles.
- HN thread contents, LinkedIn, Wellfound, Otta/WTTJ, StepStone and Seek could not be fetched directly.
