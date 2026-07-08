# About Ethan Tran

## Profile Summary

Ethan Tran is a computer science junior at California State University-Sacramento, focused on full-stack engineering, backend systems, AI engineering, and distributed systems.

His work emphasizes production readiness, clean architecture, evaluation, observability, accuracy, practical deployment, and systems that solve concrete user or developer problems.

## Technical Skills

### Programming Languages

Ethan works with:

- Python
- Rust
- C++
- C
- CUDA
- SQL
- Go
- Java
- TypeScript
- JavaScript
- HTML/CSS

Python is Ethan's primary language for full-stack and AI-integrated applications, but Ethan's favorite language to develop in is Rust. He also uses C++, C, and CUDA for performance-sensitive systems, numerical workloads, and parallelized computation.

### Full-Stack Development

Ethan has experience building full-stack services with:

- FastAPI
- Flask
- Quart
- REST APIs
- React.js
- Next.js
- Node.js
- Pydantic models
- Authentication and account linking
- OAuth-based authentication
- Role-based access control
- Full-text search and autocomplete
- Discord-integrated community utilities
- Dockerized services
- Environment-based configuration
- Cloud deployment workflows

He prefers backend designs that separate routing, service logic, data models, and external dependencies.

### AI Engineering

Ethan has experience with:

- Retrieval-Augmented Generation
- Dense vector search
- Sparse keyword search
- Hybrid retrieval
- Reciprocal Rank Fusion
- Cross-encoder reranking
- Chunking strategy evaluation
- Prompt design
- Citation-grounded answer generation
- LLM-based evaluation
- LLM-judged retrieval evaluation
- OCR-based document processing
- Document intelligence pipelines
- Data extraction and classification
- HuggingFace models
- LangChain
- LlamaIndex
- Mistral LLM
- PyTorch
- Pandas
- Scikit-learn
- AI-assisted chatbots

He is especially interested in RAG systems that can produce answers with verifiable source citations and can be evaluated through measurable retrieval quality, faithfulness, and citation accuracy.

### Backend, Data, and Distributed Systems

Ethan has experience with:

- Scalable backend systems
- Distributed systems fundamentals
- Parallelizable architecture
- Multi-instance service design
- API gateway architecture
- Rate limiting algorithms
- Token bucket rate limiting
- Sliding-window rate limiting
- Fixed-window rate limiting
- Authenticated identity forwarding
- API key handling and request sanitization
- Prometheus metrics
- Latency histograms
- In-flight request tracking
- Multi-threaded data pipelines
- ETL workflows
- Ingestion pipeline prioritization
- Connection pooling
- Query optimization
- Low-latency API design
- Deterministic simulation systems
- Rollback networking
- iOS and Android API integration

He is interested in backend systems where correctness, latency, scalability, security, observability, and maintainability all matter.

### Cloud and Deployment

Ethan has worked with:

- Docker
- Docker Compose
- Kubernetes
- Amazon Web Services
- Google Cloud
- Cloud-hosted APIs
- Environment variables and secrets
- Managed vector databases
- API gateways
- Rate limiters
- Nginx
- Redis
- Apache

He is interested in deploying AI systems and backend platforms as reliable web services rather than only local prototypes.

### Databases and Storage

Ethan has worked with:

- Postgres
- MySQL
- SQL Server
- Redis
- Qdrant
- Dense vector indexes
- Full-text search indexes
- SQL query optimization
- Connection pooling

### Developer Tools, Libraries, and Collaboration

Ethan has worked with:

- Git
- Jira
- jMeter
- Perforce
- CSV-based tooling
- Performance testing
- Configuration pipelines
- JDBC
- jQuery
- Bootstrap
- Tailwind
- Plotly

## Projects

## GitHub Documentation RAG Pipeline

### Project Summary

The GitHub Documentation RAG Pipeline is a Retrieval-Augmented Generation system that ingests public GitHub repository documentation, indexes it with dense and sparse retrieval, and answers documentation-based questions with grounded in-text citations.

The system is designed for technical documentation, where exact terms like function names, configuration keys, file paths, CLI commands, and error messages are important. It uses Qdrant, LangChain, HuggingFace, PyTorch, FastAPI, Docker, and AWS.

### Problem It Solves

Many documentation search systems rely only on semantic similarity. This can miss exact technical terms.

This project combines configurable chunking, weighted Reciprocal Rank Fusion dense/sparse search, cross-encoder reranking, and LLM-judged evaluation so the system can answer both conceptual questions and exact identifier-based questions. On a 50-question evaluation suite, the pipeline achieved over 92% faithfulness and 99% citation accuracy.

The FastAPI service is containerized with Docker and environment-based configuration for reproducible local and cloud deployment. Ethan also integrated the AI pipeline into his portfolio website as an interactive GitHub project documentation agent.

## Nvidia CUDA GPU-Accelerated Postflop Poker Solver

### Project Summary

The Nvidia CUDA GPU-Accelerated Postflop Poker Solver is a No-Limit Hold'em postflop solver built in C++, CUDA, and FLTK. It uses Counterfactual Regret Minimization across configurable game trees to compute and inspect poker strategies.

The system supports both CPU and GPU CFR execution, with flattened device-side game data and CUDA kernels for performance-oriented solving.

### Problem It Solves

Postflop poker solving is computationally expensive because it requires evaluating large game trees, legal hand-pair combinations, strategy tensors, regret tensors, and best-response behavior.

This project focuses on making solver computation faster, more memory-efficient, and more inspectable. Ethan optimized solver memory architecture by cutting memory usage by 60% through batched hand-pair evaluation, enabled near-linear vertical scaling for CFR iterations, and reduced computation time by up to 27% on entry-level consumer GPUs.

The project also includes an FLTK user interface for range input, board selection, solve configuration, and combo-level strategy visualization.

## Discord Community Utilities + Permissions Manager

### Project Summary

The Discord Community Utilities + Permissions Manager is a full-stack web platform built with Python, JavaScript, Postgres, SQL, Quart, Docker, and Google Cloud. It provides Discord-verified community utilities, progression tracking, permission management, and backend services for community engagement.

The platform was deployed to support more than 100 servers.

### Problem It Solves

Large online communities need reliable utilities for account verification, leaderboard tracking, permissions, and responsive data-backed workflows.

This project solves those problems with a scalable ingestion pipeline that prioritizes important accounts and maintains leaderboard freshness across millions of players. Ethan reduced backend response time by 21% through connection pooling to support hundreds of concurrent database calls, and he integrated role-based access control so communities can create and manage permissions linked to progression tracking.

## Distributed API Gateway + Rate Limiter

### Project Summary

The Distributed API Gateway + Rate Limiter is a configurable production API gateway built with Go, Nginx, Redis, Docker, and AWS. It enforces per-plan rate limits across multiple service instances and forwards authenticated identity metadata upstream while stripping raw API keys from requests.

### Problem It Solves

Production APIs need rate limiting that remains correct under burst traffic and multi-instance deployment. Naive local rate limiters can be bypassed when traffic is balanced across multiple service replicas.

This project addresses that problem by implementing and benchmarking token bucket, sliding-window, and fixed-window algorithms under simulated burst load. The system reduced the limit-bypass rate to zero across multi-instance deployment and exposes Prometheus metrics for request counts, rate-limit rejections, latency histograms, and in-flight requests.

## Physics-Based Multiplayer Mobile Game

### Project Summary

The Physics-Based Multiplayer Mobile Game is a cross-platform multiplayer game system built around a deterministic Rust physics engine, SQL-backed services, mobile API integration, and OAuth-based authentication.

The engine uses fixed-step floating-point integration so simulations can remain reproducible across mobile clients and backend services.

### Problem It Solves

Real-time multiplayer games must stay responsive even when players are on unstable networks. Small simulation differences between clients can create desynchronization, unfair gameplay, and inconsistent player experiences.

This project addresses those problems with deterministic simulation, rollback networking for synchronization, a reusable physics library, and CSV-based ETL tooling for live configuration updates.

## What is Ethan focused on right now?

Ethan is focused on completing his Bachelor of Science in Computer Science at CSUS while pursuing internship opportunities in backend engineering, full-stack engineering, AI engineering, and infrastructure-oriented software roles.

He is currently building depth in production RAG systems, document intelligence, distributed backend infrastructure, API gateway design, rate limiting, cloud deployment, observability, and GPU-accelerated systems.

What kind of engineering work does Ethan enjoy?

Ethan enjoys engineering work that turns specific real-world problems into reliable software systems. He is especially interested in backend platforms, full-stack products, AI-assisted tools, retrieval systems, data pipelines, performance-sensitive systems, and developer-facing infrastructure.

What are Ethan's strongest technical areas?

Ethan's strongest technical areas are backend systems, full-stack application development, AI and retrieval systems, database-backed platforms, distributed infrastructure, and performance-oriented systems programming.

What technical areas is Ethan focused on right now?

Ethan is currently focused on deepening his experience in distributed systems, scalable backend architecture, cloud-native deployment, Kubernetes, database optimization, vector search, RAG evaluation, OCR-backed document intelligence, API gateways, Redis-backed rate limiting, observability with Prometheus-style metrics, GPU acceleration, and low-latency systems.

What kind of role is Ethan looking for?

Ethan is looking for full-stack engineer, backend engineer, AI engineer, infrastructure engineer, and software engineering internship roles involving backend systems, production web services, RAG systems, document intelligence, cloud deployment, distributed systems, databases, observability, and performance engineering.

## Contact

Ethan can be reached through:

GitHub: https://github.com/quwin
LinkedIn: https://linkedin.com/in/kien-ethan-tran
Portfolio: https://quwin.dev
Email: ethantran@quwin.dev
