<div align="center">

# Hemanth Vasudev N P

**Backend Engineer** · M.Sc. (Integrated) Software Systems, PSG College of Technology

APIs, distributed systems, and algorithms.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/hemanthvnp/)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/hemanthvnp)
[![Email](https://img.shields.io/badge/Email-D14836?style=flat-square&logo=gmail&logoColor=white)](mailto:hemanth.vasudev.official@gmail.com)

</div>

---

## About

Integrated M.Sc. Software Systems student at PSG College of Technology (2024 to 2029), focused on backend engineering: APIs, systems design, and algorithms. I care about why a design decision was made, not only that it works.

I am seeking **SDE roles** where I can work on production systems alongside engineers who care about how software is built.

**Current focus**
- Data structures and algorithms in C++
- System design: concurrency, caching, and service architecture
- End-to-end projects, including deployment, security, and fault tolerance

---

## Experience

**Backend Engineering Intern, EWhizard** · Mar 2026 – Aug 2026

- Consolidated 4 transaction-parsing services into a single APScheduler-based worker, cutting the deployed stack from 9 to 5 containers (44% fewer).
- Remediated a cross-user data-isolation vulnerability in an LLM-generated SQL query pipeline across 2 production endpoints.
- Developed a frontend MCP server with 6 tools for Figma-to-code conversion: design retrieval, token sync, and component generation.

---

## Featured Projects

### [ArthaDhruva](https://github.com/hemanthvnp/ArthaDhruva) — Multi-Tenant Credit Risk Platform

Credit risk platform for mortgage lenders that scores loan default risk and projects portfolio losses.

- **Tenant isolation:** enforced with PostgreSQL Row Level Security; 150 tests passing.
- **Reproducible Monte Carlo:** each scenario is seeded independently, so parallel simulations give identical results on any thread count. Tail losses are traced to loans by replaying seeds instead of storing scenarios.
- **Network hardening:** Docker network split into public and private tiers, with only Caddy (automatic TLS) exposed and databases on an internal network. SSRF is blocked on tenant webhooks, along with container access to the cloud metadata endpoint.

`Spring Boot` `PostgreSQL` `Docker` `Caddy`

### [Throttlr](https://github.com/hemanthvnp/Throttlr) — High-Performance API Gateway

C++20 API gateway for Linux handling security (TLS, JWT), traffic control (rate limiting), and automatic failover between backends. Built on an epoll event loop with a worker thread pool.

- **Distributed rate limiting:** an atomic Redis Lua script replaces a racy GET→SET.
- **Circuit breaker:** wait-free state transitions on the hot path via `compare_exchange_strong`, with no mutex.
- **Live reload:** rate limits and routing rules update on SIGHUP with no restart or dropped connections.
- **Performance:** 28,548 req/s, P50 647 µs, P99 2.82 ms across 857K requests, zero failures.

`C++20` `Linux` `Redis` `epoll`

### [CineScope](https://github.com/hemanthvnp/CineScope) — Film Discovery & Recommendation Platform

- **LLM search:** Groq via LiteLLM plans parallel TMDB and ML calls and enforces extracted filters on results.
- **Resilience:** circuit breakers, two-tier caching, and LLM-failure fallbacks cut repeat searches from about 2 s to under 5 ms.
- **Delivery:** 5 containerized microservices deployed to Render through GitHub Actions, with every release gated on 83 tests.
- **My scope (3-person team):** ML service, hybrid TF-IDF + TruncatedSVD recommender, and the API aggregation layer.

`Python` `FastAPI` `scikit-learn` `asyncio` `MongoDB` `Docker` `GitHub Actions`

### [MargaMetis](https://github.com/hemanthvnp/MargaMetis) — Intelligent Route Optimizer

Routing engine over a real Chennai OpenStreetMap graph (22K nodes, 55K edges).

- **Algorithms:** Dijkstra, A*, Bidirectional A*, and Yen's K-Shortest Paths, implemented from scratch.
- **Optimization:** Yen's cut from 169 s to under 1 s; Bidirectional A* explores 12.9× fewer nodes than Dijkstra.
- **Caching:** Redis reduced repeat-query latency from 3,500 ms to 16 ms.

`Python` `Flask` `React` `PostgreSQL` `Redis` `Docker`

---

## Technical Skills

| Category | Technologies |
|---|---|
| **Languages** | Python, Java, C++, SQL, JavaScript |
| **Frameworks** | Spring Boot, FastAPI, Flask, Node.js, Express.js, React.js |
| **Databases** | MySQL, PostgreSQL, MongoDB, Redis |
| **DevOps & Tools** | Docker, Git, GitHub Actions, CI/CD, Postman |

---

## Education

- **M.Sc. (Integrated) Software Systems**, PSG College of Technology, Coimbatore · 2024 – 2029 · CGPA 8.43/10

---

## Leadership & Activities

- **Deputy Coordinator, CSA Tech Team**, Computational Sciences Association, PSG Tech
- **Member, FinVerse**, PSG Tech's finance club
- **Photography**, personal interest

---

## Contact

- Email: [hemanth.vasudev.official@gmail.com](mailto:hemanth.vasudev.official@gmail.com)
- LinkedIn: [linkedin.com/in/hemanthvnp](https://www.linkedin.com/in/hemanthvnp/)
