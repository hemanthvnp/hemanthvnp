<div align="center">

# Hemanth Vasudev N P

**Software Engineer in the making** · M.Sc. (Integrated) Software Systems, PSG College of Technology
Backend, algorithms, and the messy bits in between.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/hemanthvnp/)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/hemanthvnp)
[![Email](https://img.shields.io/badge/Email-D14836?style=flat-square&logo=gmail&logoColor=white)](mailto:hemantth06@outlook.com)
![Profile views](https://komarev.com/ghpvc/?username=hemanthvnp&label=Profile%20views&color=0e75b6&style=flat-square)

</div>

---

### Hi, I'm Hemanth.

I'm pursuing my M.Sc. (Integrated) in Software Systems at PSG College of Technology. Most of what I build leans toward the backend — APIs, systems, and algorithms. I care about why a design decision was made, not just that it works.

I'm actively looking for **SDE internships** where I can work on real systems alongside engineers who care about how things are built.

**What I work with:**
- **Languages:** Python, Java, C++
- **Frameworks:** FastAPI, Flask, Express.js, React.js
- **Databases:** MySQL, PostgreSQL, MongoDB, Redis
- **Tools:** Docker, Git, GitHub Actions, Postman

**What I'm spending time on right now:**
- Sharpening DSA fundamentals in C++
- Reading about system design — concurrency, caching, and how real services are structured
- Building projects end-to-end so I learn the unglamorous parts (deployment, error handling, fault tolerance) too

---

### Projects

**[Throttlr](https://github.com/hemanthvnp/Throttlr) — High-Performance API Gateway**
A C++20 API gateway on Linux handling security (TLS, JWT), traffic control (rate limiting), and automatic failover between backend servers, built around an epoll event loop and worker thread pool. Two problems I found interesting to solve: distributed rate-limit races (fixed with an atomic Redis Lua script instead of naive GET→SET) and circuit breaker state transitions on the hot path (wait-free via `compare_exchange_strong`, no mutex). Live config reload via SIGHUP updates rate limits and routing rules with zero dropped connections. Benchmarked at 28,548 req/s, P50 of 647µs, P99 of 2.82ms across 857K requests with zero failures.
*Stack: C++20, Linux, Redis, epoll*

**[CineScope](https://github.com/hemanthvnp/CineScope) — Film Discovery & Recommendation Platform**
My piece of a 3-person project: the ML service, hybrid recommender, and an API aggregation layer that routes frontend requests across 3 microservices with automatic fallback if one goes down. The recommender is a TF-IDF + TruncatedSVD hybrid with a 4-tier fallback strategy based on how much signal the user has given, plus LiteLLM-powered natural-language search for free-text queries. Deployed as 5 separate services (React, Node.js, Python), with 71 tests gating every deploy via GitHub Actions before it ships to Render.
*Stack: Python, FastAPI, scikit-learn, asyncio, MongoDB, Docker, GitHub Actions*

**[MargaMetis](https://github.com/hemanthvnp/MargaMetis) — Intelligent Route Optimizer**
Graph engine over a real Chennai OSM graph (22K nodes, 55K edges). Implemented Dijkstra, A*, Bidirectional A*, and Yen's K-Shortest Path from scratch — optimized Yen's to run in under 1s instead of 169s, and Bidirectional A* explored 12.9× fewer nodes than Dijkstra at 6ms vs 60ms. One shared cost-function system powers all four routing algorithms across 5 routing modes, plus a provider-agnostic LLM layer (via LiteLLM) for natural-language querying. A scoring system rates each route on speed, safety, scenery, comfort, fuel use, and toll cost. Redis caching cut repeat-query latency from 3,500ms to 16ms.
*Stack: Python, Flask, React, PostgreSQL, Redis, Docker*

> 📌 The repos pinned below are the ones I'd point you to first.

---

### Tech Stack

<table>
<tr>
<td><b>Languages</b></td>
<td>
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/Java-007396?style=flat-square&logo=openjdk&logoColor=white" />
  <img src="https://img.shields.io/badge/C++-00599C?style=flat-square&logo=c%2B%2B&logoColor=white" />
</td>
</tr>
<tr>
<td><b>Frameworks</b></td>
<td>
  <img src="https://img.shields.io/badge/Flask-000000?style=flat-square&logo=flask&logoColor=white" />
  <img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white" />
  <img src="https://img.shields.io/badge/Express.js-000000?style=flat-square&logo=express&logoColor=white" />
  <img src="https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black" />
</td>
</tr>
<tr>
<td><b>Databases</b></td>
<td>
  <img src="https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white" />
  <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white" />
  <img src="https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white" />
  <img src="https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white" />
</td>
</tr>
<tr>
<td><b>DevOps & Tools</b></td>
<td>
  <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white" />
  <img src="https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white" />
  <img src="https://img.shields.io/badge/GitHub%20Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white" />
  <img src="https://img.shields.io/badge/Postman-FF6C37?style=flat-square&logo=postman&logoColor=white" />
</td>
</tr>
</table>

---

### Beyond Code

When I'm away from a terminal, I'm usually behind a camera. Photography is my way of slowing down — composition, light, the small details most people walk past. Different kind of problem-solving than code, but it scratches the same itch.

I'm also part of the **Analyst team at FinVerse**, PSG Tech's finance club, where I get to look at markets and businesses through a more analytical lens. It's been a useful counterweight to the purely engineering side of my degree. On top of that, I'm Deputy Coordinator of the **CSA Tech Team** at the Computational Sciences Association.

---

### Get in touch

If you're hiring for **SDE internships** — backend, systems, anything where I'd get to write meaningful code — I'd love to talk.

- 📧 [hemantth06@outlook.com](mailto:hemantth06@outlook.com)
- 📱 +91 82482 72473
- 💼 [LinkedIn](https://www.linkedin.com/in/hemanthvnp/)

Always happy to talk backend architecture, weird algorithm problems, or photography.
