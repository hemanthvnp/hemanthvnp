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
- **Languages:** Python, C++, C, JavaScript
- **Frameworks:** FastAPI, Flask, Node.js, React.js
- **Libraries:** scikit-learn, NumPy, SciPy, sentence-transformers, asyncio
- **Databases:** PostgreSQL, MongoDB, MySQL, Redis
- **DevOps:** Docker, Linux, Git, Postman

**What I'm spending time on right now:**
- Sharpening DSA fundamentals in C++
- Reading about system design — concurrency, caching, and how real services are structured
- Building projects end-to-end so I learn the unglamorous parts (deployment, error handling, fault tolerance) too

---

### Projects

**[CineScope](https://github.com/hemanthvnp/CineScope) — Film Discovery & Recommendation Platform**
My piece of a 3-person project: the ML service, hybrid recommender, and the AI orchestration layer. The interesting part was the query pipeline — Groq LLaMA 3.1 with function calling classifies free-text queries into 8 intent types and 10 entity fields, replacing the keyword-matching approach. On the ML side, a TF-IDF + TruncatedSVD hybrid recommender with a tiered fallback strategy (hybrid → content-only → genre → trending) based on how much signal the user has given. Service calls fan out in parallel via asyncio with per-service circuit breakers.
*Stack: Python, FastAPI, scikit-learn, asyncio, MongoDB, Docker, GitHub Actions*

**[Throttlr](https://github.com/hemanthvnp/Throttlr) — High-Performance API Gateway**
A C++20 API gateway on Linux built around an epoll event loop and worker thread pool. Two problems I found interesting to solve: distributed rate-limit races (fixed with an atomic Redis Lua script instead of naive GET→SET) and circuit breaker state transitions on the hot path (wait-free via `compare_exchange_strong`, no mutex). Also has SIGHUP config reload with zero dropped connections and four load balancing strategies including consistent hashing.
*Stack: C++20, Linux, Redis, epoll*

**[MargaMetis](https://github.com/hemanthvnp/MargaMetis) — Intelligent Route Optimizer**
Graph engine over a real Chennai OSM graph (22K nodes, 55K edges). Implemented Dijkstra, A*, Bidirectional A*, and Yen's K-Shortest from scratch — Bidirectional A* explored 12.9× fewer nodes than Dijkstra at 6ms vs 60ms. The design I'm most proud of: a cost-function injection architecture where each routing mode supplies a `(u, v, data) → float` callable at traversal time, decoupling routing logic from cost policy entirely. Groq LLaMA 3.1 with few-shot prompting parses natural-language constraints into structured JSON cost weights. Redis caching cut repeat-query latency from 3,500ms to 16ms.
*Stack: Python, Flask, React, PostgreSQL, Redis, Docker*

**[VEDA](https://github.com/hemanthvnp/VEDA) — Multi-Source Signal Fusion**
Generalized eigenproblem solver (S_b W = λ S_w W) with three variants — classical ratio trace, Exponential DA (robust to small-sample singularity when d ≈ n), and Harmonic-mean LDA — implemented from scratch in NumPy/SciPy, no ML framework. Applied to Nifty 50 sector classification from price/volume signals: 48% accuracy vs 14.3% random baseline (3.4×). The gap between linear fusion (31%) and Random Forest (48%) is what's interesting — it quantifies how much nonlinear regime-switching is in the data. Validated the same solver on digit classification (98.7%, 6-view) and face recognition (95% rank-1, 200 subjects).
*Stack: NumPy, SciPy*

> 📌 The repos pinned below are the ones I'd point you to first.

---

### Tech Stack

<table>
<tr>
<td><b>Languages</b></td>
<td>
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/C++-00599C?style=flat-square&logo=c%2B%2B&logoColor=white" />
  <img src="https://img.shields.io/badge/C-A8B9CC?style=flat-square&logo=c&logoColor=black" />
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black" />
</td>
</tr>
<tr>
<td><b>Frameworks</b></td>
<td>
  <img src="https://img.shields.io/badge/Flask-000000?style=flat-square&logo=flask&logoColor=white" />
  <img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white" />
  <img src="https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=node.js&logoColor=white" />
  <img src="https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black" />
</td>
</tr>
<tr>
<td><b>Databases</b></td>
<td>
  <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white" />
  <img src="https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white" />
  <img src="https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white" />
  <img src="https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white" />
</td>
</tr>
<tr>
<td><b>DevOps & Tools</b></td>
<td>
  <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white" />
  <img src="https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white" />
  <img src="https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black" />
  <img src="https://img.shields.io/badge/Postman-FF6C37?style=flat-square&logo=postman&logoColor=white" />
</td>
</tr>
</table>

---

### Beyond Code

When I'm away from a terminal, I'm usually behind a camera. Photography is my way of slowing down — composition, light, the small details most people walk past. Different kind of problem-solving than code, but it scratches the same itch.

I'm also part of the **Analyst team at FinVerse**, PSG Tech's finance club, where I get to look at markets and businesses through a more analytical lens. It's been a useful counterweight to the purely engineering side of my degree.

---

### Get in touch

If you're hiring for **SDE internships** — backend, systems, anything where I'd get to write meaningful code — I'd love to talk.

- 📧 [hemantth06@outlook.com](mailto:hemantth06@outlook.com)
- 📱 +91 82482 72473
- 💼 [LinkedIn](https://www.linkedin.com/in/hemanthvnp/)

Always happy to talk backend architecture, weird algorithm problems, or photography.
