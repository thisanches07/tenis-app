# Perfil de Thiago Sanches: skills, stack, experiência, projetos e lacunas

> Nota de método (2026-10-10): **thiagosanches.com não pôde ser acessado** desta sessão. WebFetch retornou `getaddrinfo ENOTFOUND` e o curl via proxy retornou `CONNECT tunnel failed, 403`, inclusive para `www.`. A busca web por "thiagosanches.com" não encontrou páginas indexadas, e web.archive.org está bloqueado para o fetcher. O LinkedIn (linkedin.com/in/thiago-sanches-profile) e o portfólio antigo thisanches07.github.io também deram ENOTFOUND. **Tudo abaixo vem do GitHub** (perfil, lista de repositórios, READMEs e package.json via github.com/raw.githubusercontent.com) e do clone local. Cargos, empresas, anos de experiência e certificações listados no site **não foram verificados** e precisam ser confirmados pelo próprio Thiago ou colando o conteúdo do site.

## 1. O que o portfólio/perfil público lista: cargos, empresas, anos, stack, certificações, idiomas

### Takeaway
O perfil observável é de um desenvolvedor backend Node.js/TypeScript baseado em Sorocaba-SP, formado (ou formando) em Engenharia de Computação, com foco em NestJS + PostgreSQL. Nenhum empregador, nº de anos de experiência ou certificação aparece nas fontes que consegui acessar.

### Cited Findings
- Nome "Thiago Sanches", usuário `thisanches07`, localização Sorocaba, São Paulo, Brasil (UTC-03:00); bio "Computer Engineering Student"; 6 seguidores / 3 seguindo; conquistas Pair Extraordinaire x3, Pull Shark x3, Quickdraw; empresa não informada — [GitHub profile](https://github.com/thisanches07)
- Link para o LinkedIn `linkedin.com/in/thiago-sanches-profile` e badge de contato do Gmail no README — [GitHub profile](https://github.com/thisanches07)
- O README do perfil o descreve como "Computer Engineer" e "Software Developer working with NodeJS". Tecnologias: Node.js, Java, Python, HTML, CSS, Git. Ferramentas: VS Code, Postman. "Currently studying": NestJS e Node.js. Nenhuma empresa citada — [profile README](https://raw.githubusercontent.com/thisanches07/thisanches07/main/README.md)
- Há uma inconsistência: a bio diz "Computer Engineering **Student**" e o README diz "Computer Engineer" — [GitHub profile](https://github.com/thisanches07); [profile README](https://raw.githubusercontent.com/thisanches07/thisanches07/main/README.md)
- Os repositórios de trabalhos acadêmicos trazem o RA 190006 (por exemplo "AC2-Thiago-Sanches-RA-190006-…" e "AF-Thiago-Sanches-RA-190006-…"), com a atividade acadêmica entre dez/2020 e mai/2023 — [GitHub repositories](https://github.com/thisanches07?tab=repositories)
- Idioma: os READMEs dos projetos estão em português do Brasil (wallet-backend, Projeto-Gerenciamento-de-Produtos, wallet-frontend) — [wallet-backend](https://github.com/thisanches07/wallet-backend); [Projeto-Gerenciamento-de-Produtos](https://github.com/thisanches07/Projeto-Gerenciamento-de-Produtos)
- As buscas web por "Thiago Sanches" (Node.js; desenvolvedor Sorocaba) não acharam perfis correspondentes. Os resultados eram de outros "Thiagos" (por exemplo github.com/thiagosf), que **não devem ser confundidos** com ele — [search result example](https://www.Github.com/thiagosf)

### Inferences
- Pelo padrão RA "190006" (matrícula de 2019) e pelos repositórios acadêmicos até 2023, a graduação provavelmente começou em 2019 e terminou por volta de 2023/2024. A experiência profissional em Node.js deve ficar entre ~2 e 4 anos, o que é inferência e não está confirmado.
- Ele contribui numa organização (Smart-Health-Organization) com 221 commits e deploy em Cloud Run com ambientes dev e prod. Isso sugere trabalho em equipe real, talvez um TCC ou startup, mas o contexto não está documentado.
- Como o README ainda lista NestJS como "currently studying" enquanto os projetos de 2025 já usam NestJS 11, o README do perfil provavelmente está desatualizado.

### Gaps
- Cargos, empresas, datas, anos de experiência, certificações e idiomas declarados em thiagosanches.com/LinkedIn: **não verificados** (site e LinkedIn inacessíveis).
- Formação exata (instituição, ano de conclusão): não encontrada.

## 2. Projetos (site e GitHub) e tecnologias; o que é o tenis-app

### Takeaway
O GitHub tem 22 repositórios. Os mais relevantes e recentes formam o par "Wallet AI": um backend NestJS 11 + PostgreSQL + TypeORM + Firebase Auth + integração Pluggy, com deploy no Cloud Run, e um frontend Next.js + Tailwind + React Query na Vercel. O **tenis-app está vazio**: foi criado em 01/11/2025 com tamanho 0 e sem commits, então ainda não há stack nem funcionalidade.

### Cited Findings
**tenis-app**
- Repositório `thisanches07/tenis-app`: descrição "tenis-app", language null, size 0, criado e com último push em 2025-11-01T14:21:42Z, sem topics. A API de linguagens retorna `{}` — [GitHub API repos/thisanches07/tenis-app](https://github.com/thisanches07/tenis-app)
- O clone local (/home/user/tenis-app) não tem commits ("your current branch 'master' does not have any commits yet"). Só contém as pastas `reports/` e `research_notes/` criadas por esta pesquisa — [repo](https://github.com/thisanches07/tenis-app)

**wallet-backend (projeto principal, atualizado em dez/2025)**
- API REST de finanças pessoais (README em PT-BR) para despesas, receitas, investimentos, conexões bancárias via Pluggy e análise de portfólio. Módulos: users, expenses, incomes, pluggy, portfolio, summary, firebase. 39 commits — [wallet-backend](https://github.com/thisanches07/wallet-backend)
- Stack: NestJS 11, TypeORM 0.3 com migrations, pg, Firebase Admin (Bearer token), class-validator/class-transformer, Swagger (`/api/docs`), nestjs-pino/pino (logs), axios, exceljs; Jest + supertest (unit e e2e, coverage); ESLint 9 + Prettier; SWC; TypeScript 5.7 — [package.json](https://raw.githubusercontent.com/thisanches07/wallet-backend/main/package.json)
- Infra: Dockerfile, docker-compose, `cloud-run-config.yaml`, scripts `deploy-cloud-run.sh`/`.ps1` e `DEPLOY.md` (Google Cloud Run). O README cobre health checks e troubleshooting — [wallet-backend](https://github.com/thisanches07/wallet-backend)
- Pontos de qualidade observados: dependência auto-referente `wallet-api: file:`, `@types/exceljs` em dependencies e um arquivo duplicado "README copy.md" — [package.json](https://raw.githubusercontent.com/thisanches07/wallet-backend/main/package.json); [wallet-backend](https://github.com/thisanches07/wallet-backend)

**wallet-frontend ("Wallet AI", out/2025)**
- Dashboard "Wallet AI" para investimentos, recomendações e análise de portfólio. Stack: Next.js (pages router), TypeScript, Tailwind, React Query v5, Firebase client, Pluggy. Demo em wallet-frontend-delta.vercel.app. 45 commits. O token fica em `localStorage`. O README documenta um `TypeError` em `investments.tsx` quando o payload de `portfolioAnalysis` vem incompleto — [wallet-frontend](https://github.com/thisanches07/wallet-frontend)

**Projeto-Gerenciamento-de-Produtos (jan/2025)**
- API REST NestJS + PostgreSQL de produtos e pedidos, com controle de estoque e cálculo de total do pedido. Tem Swagger, Docker/docker-compose (app + Postgres), coleção de requisições e 32 commits. O `ormconfig.js` sugere TypeORM — [Projeto-Gerenciamento-de-Produtos](https://github.com/thisanches07/Projeto-Gerenciamento-de-Produtos)

**Smart-Health-Organization/smart-health-api (fixado no perfil)**
- Backend NestJS/TypeScript com 221 commits na branch `prod`. Usa PostgreSQL (README), Docker/docker-compose, Husky, ESLint, Prettier, diretório `.github/workflows` (CI existe, mas o conteúdo não foi visto), testes unit/e2e/cov, e deploy de prod e dev no Google Cloud Run com Swagger. O README é basicamente o starter do NestJS e não descreve o propósito do sistema nem a autoria individual — [smart-health-api](https://github.com/Smart-Health-Organization/smart-health-api)

**Outros repositórios (mais antigos, majoritariamente estudo/acadêmico)** — [GitHub repositories](https://github.com/thisanches07?tab=repositories)
- servidor-HTTP-1.1 (CSS, set/2023): o nome sugere a implementação de um servidor HTTP/1.1, o que não foi verificado.
- Algoritmo-Genetico (Jupyter, mai/2023): 1 notebook `AC2_Algoritmo_Genetico.ipynb`, 5 commits, sem README útil — [Algoritmo-Genetico](https://github.com/thisanches07/Algoritmo-Genetico)
- market-list (TS, 2023); NodeJS-RestAPI (JS, 2022); node-course (EJS, 2022); api-petshop (JS, 2021).
- NFTMarketplace (Dart/Flutter, 2022) + NFTMarketplaceApi (Java, 2022).
- projeto-vue (Vue), Letmeask (React, "Estudo React.JS Rocketseat"), Interface-Netflix (HTML), Snake-game (C#), SchoolProject/cursorestful-springboot e trabalhos AC2/AF (Java), thisanches07.github.io ("Portfólio Thiago Sanches", 2021).

### Inferences
- A trajetória vai de Java/Spring e estudos web (2020-2022) para Node/NestJS + TypeScript (2022-2025). O núcleo atual é NestJS + PostgreSQL + TypeORM + Docker + GCP Cloud Run.
- O "Wallet AI" é o projeto de portfólio mais maduro e o candidato natural a receber features reais de IA.

### Gaps
- Projetos listados em thiagosanches.com: não verificados.
- Não sei qual era a intenção do tenis-app (o nome sugere um app de tênis, o esporte, ou de calçados). O repo não tem conteúdo.
- Contribuição individual de Thiago no smart-health-api: não verificada.

## 3. Trabalho existente com IA/LLM e evidências de sistemas distribuídos, cloud, observabilidade, testes e system design

### Takeaway
Não há evidência de trabalho real com IA/LLM: "AI" aparece só no nome "Wallet AI", e o backend não tem nenhuma lib de LLM. Há evidência sólida de fundamentos (testes Jest/e2e, Docker, deploy em Cloud Run, logs estruturados com pino, migrations, Swagger), mas nada de sistemas distribuídos, filas, cache, tracing ou métricas.

### Cited Findings
- package.json do wallet-backend: **nenhuma** lib de AI/LLM (openai, anthropic, langchain etc.), **nenhuma** fila, **nenhum** cache. Observabilidade se resume a logs (nestjs-pino/pino), sem tracing nem métricas — [package.json](https://raw.githubusercontent.com/thisanches07/wallet-backend/main/package.json)
- No wallet-frontend, "AI" aparece apenas no nome do produto. A página não descreve integração com LLM, e a origem das "recomendações" não está documentada — [wallet-frontend](https://github.com/thisanches07/wallet-frontend)
- Cloud: Google Cloud Run (wallet-backend com configs e scripts de deploy; smart-health-api com ambientes prod e dev), Firebase Auth, Vercel (frontend) — [wallet-backend](https://github.com/thisanches07/wallet-backend); [smart-health-api](https://github.com/Smart-Health-Organization/smart-health-api); [wallet-frontend](https://github.com/thisanches07/wallet-frontend)
- Testes: Jest unit + e2e (supertest) + coverage no wallet-backend e no smart-health-api — [package.json](https://raw.githubusercontent.com/thisanches07/wallet-backend/main/package.json); [smart-health-api](https://github.com/Smart-Health-Organization/smart-health-api)
- CI: diretório `.github/workflows` no smart-health-api (conteúdo não visto). Não há workflows visíveis no wallet-backend nem no Projeto-Gerenciamento — [smart-health-api](https://github.com/Smart-Health-Organization/smart-health-api); [wallet-backend](https://github.com/thisanches07/wallet-backend)
- Python e ML: Python aparece no README do perfil, e há um notebook acadêmico de algoritmo genético (2023) — [profile README](https://raw.githubusercontent.com/thisanches07/thisanches07/main/README.md); [Algoritmo-Genetico](https://github.com/thisanches07/Algoritmo-Genetico)
- Integração com API financeira de terceiros (Pluggy) no backend e no frontend — [wallet-backend](https://github.com/thisanches07/wallet-backend)

### Inferences
- O nível observável é de pleno em backend Node: monólitos NestJS bem estruturados, com testes, Docker e deploy serverless em container. Faltam artefatos que sinalizem senioridade (arquitetura distribuída, ADRs, escalabilidade, resiliência).
- O código de ML se limita a trabalho acadêmico. Nada indica RAG, agentes, embeddings, avaliação de LLM ou MLOps.

### Gaps
- O conteúdo dos workflows de CI do smart-health-api e a cobertura real de testes não foram verificados.
- Não sei se existe trabalho privado ou profissional com IA, cloud ou sistemas distribuídos (por exemplo, citado no site ou no LinkedIn).

## 4. Lacunas em relação a vagas Senior/Specialist/Tech Lead Node.js backend e AI Engineer

### Takeaway
As lacunas principais são: (a) nenhuma prova pública de IA/LLM aplicada; (b) nenhum projeto com arquitetura distribuída e orientada a eventos; (c) observabilidade além de logs; (d) documentação de decisões e system design; (e) sinais de liderança e qualidade de produção (CI/CD visível, IaC, segurança). O site não pôde ser verificado, então lacunas de "experiência declarada" não foram avaliadas.

### Cited Findings (base observada)
- Sem filas, cache, tracing ou métricas, sem libs de LLM e só com logging pino no projeto principal — [package.json](https://raw.githubusercontent.com/thisanches07/wallet-backend/main/package.json)
- Sem CI visível nos projetos pessoais. Há bugs e ruídos documentados ou visíveis: o TypeError no frontend, o README duplicado e a dependência auto-referente — [wallet-frontend](https://github.com/thisanches07/wallet-frontend); [wallet-backend](https://github.com/thisanches07/wallet-backend)
- Repositórios sem descrição e topics, READMEs só em PT-BR, e README do perfil desatualizado ("studying NestJS") — [GitHub repositories](https://github.com/thisanches07?tab=repositories); [profile README](https://raw.githubusercontent.com/thisanches07/thisanches07/main/README.md)
- Baixa visibilidade pública: 6 seguidores, 0 estrelas nos projetos principais e nenhum resultado de busca para o nome — [GitHub profile](https://github.com/thisanches07); [wallet-backend](https://github.com/thisanches07/wallet-backend)

### Inferences (lacunas a cobrir com projetos; todas são inferências)
- **Backend sênior Node.js:** mensageria (Kafka/RabbitMQ/SQS/PubSub), padrões outbox/saga/idempotência, Redis (cache e rate-limit), concorrência e locks, multi-tenancy, OpenTelemetry (traces + métricas + Grafana/Prometheus), testes de carga (k6), testcontainers, IaC (Terraform), CI/CD com GitHub Actions visível, segurança (OWASP, secrets, RBAC), ADRs e diagramas C4, e conhecimento de runtime Node (event loop, streams, workers).
- **AI Engineer:** integração com LLM (Anthropic/OpenAI) com tool use e structured outputs, RAG com pgvector (encaixa no Postgres que ele já usa), pipelines de ingestão e embeddings, avaliação (evals, LLM-as-judge), guardrails, controle de custo e latência (cache, streaming), agentes e MCP, e observabilidade de LLM (Langfuse/OTel). O "Wallet AI" pode virar um assistente financeiro real (RAG sobre transações, classificação de despesas com LLM, insights de portfólio).
- **Tech Lead:** documentação em inglês, ADRs, roadmap e issues organizadas, PRs com review, e conteúdo público (posts/talks) para aumentar a visibilidade.
- Python aparece só de forma superficial. Para vagas de AI Engineer, um serviço Python (FastAPI) ao lado do Node seria um diferencial.

### Gaps
- Sem acesso ao site e ao LinkedIn, não dá para saber se essas lacunas já são cobertas por experiência profissional declarada (por exemplo, empresa com Kafka ou AWS).
