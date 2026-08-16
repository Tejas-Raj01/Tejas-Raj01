<!-- Header Section -->
<h1 align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=28&duration=3000&pause=1000&color=F72585&center=true&vCenter=true&width=850&height=50&lines=Hi%2C+I'm+Tejas+Raj+%F0%9F%91%8B;AI+%26+Systems+Engineer;Upstream+Open+Source+Contributor;Distributed+Systems+%26+LLM+Inference" alt="Typing SVG" />
</h1>

<p align="center">
  <i>Focusing on Generative AI, Agent Infrastructure, LLM Inference Engines, and Distributed Storage Systems.</i>
</p>

<p align="center">
  <a href="https://linkedin.com/in/tejas-raj-09aa4a236/">
    <img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" />
  </a>
  <a href="https://github.com/Tejas-Raj01">
    <img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub" />
  </a>
  <a href="mailto:rajtejas.xyz@gmail.com">
    <img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" />
  </a>
  <a href="https://www.codechef.com/users/tejas_2341">
    <img src="https://img.shields.io/badge/CodeChef-4%E2%98%85_1804-5B4638?style=for-the-badge&logo=codechef&logoColor=white" alt="CodeChef" />
  </a>
</p>

---

<!-- About Me Section -->
### 👨‍💻 About Me

I'm an **AI & Systems Engineer** who loves working inside complex infrastructure, solving deep engineering problems, and contributing improvements upstream. My technical work spans machine learning frameworks (**PyTorch**), high-throughput LLM inference engines (**vLLM**), financial AI workflow engines (**DealLens**), distributed P2P storage engines (**Tejas-DB**), and Linux ecosystem packaging toolchains (**Canonical Snapcraft & Craft Parts**).

- 🎓 **Education:** B.Tech in Computer Science & Engineering @ **NIT Durgapur** ('27)
- 🧠 **Primary Focus:** Generative AI, LLM Inference Optimization, Agent Runtimes, and Distributed Storage
- 🛠 **Open Source:** Active upstream contributor to **vLLM**, **PyTorch**, **Canonical (Snapcraft & Craft Parts)**, **CP Editor**, and **Automattic Jetpack** (9 Merged PRs)
- 🏆 **Competitive Programming:** 4★ on CodeChef (Max Rating: **1804**)

---

<!-- Major Open Source Contributions Section -->
### 🚀 Major Upstream Open Source Contributions

#### ⚡ [vLLM Project](https://github.com/vllm-project/vllm) — *High-Throughput LLM Inference & Serving Engine*
> **Merged PR [#49206](https://github.com/vllm-project/vllm/pull/49206): Fix request index preemption misalignment in `SchedulingPolicy.PRIORITY`**
- **Problem:** Under heavy KV cache memory pressure, request preemption in `SchedulingPolicy.PRIORITY` resulted in index misalignment within waiting request queues, causing lower-priority or preempted requests to be silently skipped during re-scheduling.
- **Solution:** Re-engineered preemption queue index offset calculations in `vllm/core/policy.py`, preserving strict priority queue ordering during KV cache page eviction and re-insertion.
- **Tech Stack:** `Python`, `PyTorch`, `LLM Inference`, `KV Cache Eviction`

#### 🔬 [PyTorch Core Framework](https://github.com/pytorch/pytorch) — *Core Machine Learning & Compiler Infrastructure*
> **Merged PR [#189142](https://github.com/pytorch/pytorch/pull/189142): Fix `return_annotation` schema for tuple-returning operators in PyTorch FX**
- **Problem:** Incorrect schema typing for tuple-returning operators in PyTorch FX graph tracer caused static type checkers and downstream graph transformations to crash.
- **Solution:** Corrected FX operator schema definitions to accurately return tuple type annotations across symbolic graph execution paths.
- **Tech Stack:** `Python`, `FX Graph Tracer`, `Compiler Schemas`

> **Merged PR [#190191](https://github.com/pytorch/pytorch/pull/190191): Fix floating-point division-by-zero crash in `sparse_compressed_to_dense`**
- **Problem:** Executing conversions on malformed BSR compressed sparse tensors triggered hard C++ floating-point division-by-zero runtime segmentation faults.
- **Solution:** Added strict boundary validation and non-zero checks in underlying C++ sparse tensor conversion kernels.
- **Tech Stack:** `C++`, `Sparse Tensors`, `Error Handling`

#### 🐧 Canonical Packaging Toolchains — *Linux Package Infrastructure*
> **[Craft Parts](https://github.com/canonical/craft-parts) — Merged PR [#1628](https://github.com/canonical/craft-parts/pull/1628): Prevent file deletion during self-linking in `link_or_copy`**
- **Problem:** In `link_or_copy`, when source and destination paths resolved to the same physical file (e.g., via staged symlinks), catching `EEXIST` and unlinking the destination accidentally unlinked and permanently deleted the source file itself (Fixes `canonical/snapcraft#6168`).
- **Solution:** Implemented a physical file comparison check (`os.path.samefile`) in `craft_parts/utils/file_utils.py` to safely return early without deleting the target asset.
- **Tech Stack:** `Python`, `Linux File Systems`, `Symlinks`, `Packaging Subsystems`

> **[Snapcraft](https://github.com/canonical/snapcraft) — Merged PR [#6272](https://github.com/canonical/snapcraft/pull/6272) & PR [#6269](https://github.com/canonical/snapcraft/pull/6269)**
- **Solution:** Resolved hardcoded linter fallbacks across package build pipelines via dynamic `build_base` resolution, and contributed manual connection documentation for the `personal-files` security interface.
- **Tech Stack:** `Python`, `Snapcraft CLI`, `Security Interfaces`

#### 🛠️ [CP Editor](https://github.com/cpeditor/cpeditor) — *Desktop Developer Environment for Competitive Programming*
> **Merged PR [#1501](https://github.com/cpeditor/cpeditor/pull/1501), PR [#1499](https://github.com/cpeditor/cpeditor/pull/1499), & PR [#1498](https://github.com/cpeditor/cpeditor/pull/1498)**
- **LLM Localization Pipeline (PR #1501):** Translated 3,600+ UI strings using an automated LLM translation pipeline and fixed duplicate search indexing in global search panels.
- **Dynamic Font Scaling & Tab Controls (PR #1499, #1498):** Added Ctrl+Scroll font scaling toggle and implemented Qt mouse event filters for middle-click tab closure.
- **Tech Stack:** `C++17`, `Qt Framework`, `LLM Pipeline`, `GUI Architecture`

#### 📦 [Automattic Jetpack](https://github.com/Automattic/jetpack) — *Open Source Platform Infrastructure (9 Merged PRs)*
- Contributed **9 merged PRs** fixing Gutenberg block editor state transformation crashes (PR [#50035](https://github.com/Automattic/jetpack/pull/50035), PR [#50025](https://github.com/Automattic/jetpack/pull/50025)), resolving OpenAPI parser failures via polymorphic `oneOf` schemas (PR [#50030](https://github.com/Automattic/jetpack/pull/50030)), and refactoring string store IDs to type-safe store objects in React hooks (PR [#49810](https://github.com/Automattic/jetpack/pull/49810)).

---

<!-- Highlighted Systems & AI Projects -->
### 🏗️ Highlighted Systems & AI Engineering Projects

```
+-----------------------------------------------------------------------------------------------+
|  Tejas-DB (Distributed Key-Value Database in C++17)                                           |
|  - Consistent Hashing | Gossip Protocol | Tunable Quorum (N, W, R) | WAL Engine                 |
|  - Benchmark: 33,685 req/s throughput | ~2.97 ms avg latency | 100 concurrent threads          |
+-----------------------------------------------------------------------------------------------+
|  DealLens (AI Investment Due-Diligence & RAG Workflow Engine)                                 |
|  - Deterministic 7-step DAG State Machine | PostgreSQL 16 + pgvector Hybrid Search (RRF)      |
|  - Page-aware 1-indexed PDF chunking | Custom CitationVerifier Guardrail                       |
+-----------------------------------------------------------------------------------------------+
|  NexusMatch / AI Job Platform (AI Career Intelligence)                                        |
|  - Decoupled FastAPI/Laravel Backend | scikit-learn TF-IDF & Cosine Similarity Matching        |
|  - Real-time job discovery via async Celery workers + Redis | Groq / LangChain Active Fallback|
+-----------------------------------------------------------------------------------------------+
```

#### 🌐 1. [Distributed Key-Value Database (Tejas-DB)](https://github.com/Tejas-Raj01/distributed-system)
*Decentralized P2P Storage Engine built in C++17*
- **Architecture:** Engineered a decentralized peer-to-peer key-value storage system utilizing **Consistent Hashing** for dynamic data partitioning and a **Gossip Protocol** for autonomous cluster node discovery and failure detection.
- **Concurrency & Reliability:** Implemented a concurrent engine using `std::shared_mutex`, customizable **Quorum Consensus (N, W, R)** for tunable consistency, and a **Write-Ahead Log (WAL)** engine for instant crash recovery.
- **Performance Benchmarks:** Achieved **33,685 req/sec throughput** at **~2.97 ms average latency** under 100 concurrent thread workloads. Includes dynamic Vercel Native Edge Proxy rewrites for active backend tunnels.

#### 📈 2. [DealLens](https://github.com/Tejas-Raj01/DealLens)
*AI Investment Due-Diligence & Financial RAG Engine*
- **Workflow State Machine:** Designed an asynchronous DAG workflow engine (Validation → Entity Extraction → Performance Analysis → Risk Analysis → Evidence Retrieval → Claim Verification → Report Generation) replacing non-deterministic agent loops.
- **Hybrid RAG & Provenance:** Built a PostgreSQL 16 + pgvector hybrid search engine combining dense Cosine Distance embeddings and sparse `tsvector` keyword search via **Reciprocal Rank Fusion (RRF)**. Integrated a custom `CitationVerifier` guardrail to enforce strict source provenance and prevent hallucinations in corporate document analysis.

#### 💼 3. [NexusMatch / AI Job Platform](https://github.com/Tejas-Raj01/NexusMatch)
*AI Career Intelligence & Resume Matching Platform*
- **Semantic Matching Engine:** Built a high-performance career intelligence platform featuring an optimized TF-IDF and Cosine Similarity engine that evaluates resume compatibility in milliseconds.
- **Asynchronous Scalability:** Utilized Celery and Redis for asynchronous background tasks, paired with active model fallback loops via LangChain and the Groq API.

---

<!-- Tech Stack Section -->
### 🛠 Tech Stack

<p align="center">
  <a href="https://skillicons.dev">
    <img src="https://skillicons.dev/icons?i=cpp,c,python,js,ts,qt,fastapi,react,postgres,docker,git,linux,bash,aws&theme=dark" alt="Tejas Raj Tech Stack" />
  </a>
</p>

| Category | Technologies & Tools |
| :--- | :--- |
| **Languages** | C++, C, Python, TypeScript, JavaScript, SQL, Bash |
| **AI Infrastructure & Frameworks** | PyTorch, vLLM, LangChain, Groq API, scikit-learn, pgvector |
| **Systems & Backend** | Distributed Systems (Gossip Protocol, Consistent Hashing), FastAPI, Laravel, Node.js, Qt Framework, Redis, Celery |
| **Databases & DevOps** | PostgreSQL, AWS S3, MinIO, Docker, Git, Linux, Vercel Edge Proxy |

---

<!-- GitHub Stats Section -->
### 📊 GitHub Activity

<p align="center">
  <img src="https://github-readme-stats-sigma-five.vercel.app/api?username=Tejas-Raj01&show_icons=true&theme=radical&hide_border=true&include_all_commits=true&count_private=true&v=1" width="48%" />
  <img src="https://github-readme-stats-sigma-five.vercel.app/api/top-langs/?username=Tejas-Raj01&layout=compact&theme=radical&hide_border=true&v=1" width="48%" />
</p>

<p align="center">
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=Tejas-Raj01&theme=radical&hide_border=true" width="97%" />
</p>

---

<!-- Footer -->
<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=1&height=120&section=footer"/>
</p>
