# xnn-learning-path

面向计算机科学与 AI 学习者的中文学习地图。它不试图列出所有资源，而是把高质量的**官方文档、大学课程和实践项目**按知识依赖组织起来：先建立基础，再选择方向，最后用项目和性能优化检验学习成果。

> 链接优先指向一手来源；课程开课信息、作业权限和版本以资源页面为准。欢迎提交失效链接与更好的学习路径。

## 如何使用

1. 先阅读「基础与数学」和一门主力语言；不要同时开始所有板块。
2. 每个阶段都完成一个可运行、可复现的项目，并记录问题与复盘。
3. 需要转向 AI、数据库、系统或算子开发时，再进入相应的专项路径。
4. 课程资料用于建立体系，官方文档用于解决工程细节；两者结合效果最好。

## 学习地图

| 模块 | 解决的问题 | 建议前置 |
| --- | --- | --- |
| [基础与数学](#1-基础与数学) | 算法、离散数学、概率、线性代数 | 高中数学与任意一门编程语言 |
| [编程语言](#2-编程语言) | 用合适的语言表达与实现想法 | 基础与数学 |
| [系统、硬件与网络](#3-系统硬件与网络) | 程序怎样在机器和网络上高效运行 | C/C++、数据结构 |
| [数据与 SQL](#4-数据与-sql) | 数据建模、查询、事务与分析 | 一门语言、基础集合论 |
| [软件工程与云原生](#5-软件工程与云原生) | 可维护、可测试、可部署的软件 | Git、主力语言 |
| [AI 与智能体](#6-ai-机器学习大模型与智能体) | 从机器学习到 LLM 应用与 Agent | 概率、线代、Python |
| [GPU、NPU 与算子开发](#7-gpunpu-并行计算与算子开发) | 从并行模型到高性能自定义算子 | C/C++、体系结构、深度学习 |

---

## 1. 基础与数学

### 数学工具箱

- [线性代数（MIT 18.06）](https://ocw.mit.edu/courses/18-06-linear-algebra-spring-2010/)：向量、矩阵、特征值和 SVD；是机器学习与图形学的共同语言。
- [概率与统计（Harvard Stat 110）](https://projects.iq.harvard.edu/stat110/home)：概率建模、条件概率、随机变量与推断。
- [离散数学与证明（MIT 6.042J）](https://ocw.mit.edu/courses/6-042j-mathematics-for-computer-science-spring-2015/)：集合、图、组合、递归与证明。
- [凸优化（Stanford EE364A）](https://web.stanford.edu/class/ee364a/)：理解损失函数、约束和优化器的理论基础。

### 计算机科学核心

- 数据结构与算法：数组、链表、栈/队列、树、图、哈希、排序、动态规划、贪心、并查集。
- [Algorithms, 4th Edition](https://algs4.cs.princeton.edu/home/)：以实现和实验理解算法。
- [MIT 6.006](https://ocw.mit.edu/courses/6-006-introduction-to-algorithms-fall-2011/)：算法设计与复杂度分析。
- [CS50](https://cs50.harvard.edu/x/)：适合作为计算机科学的项目式入门。
- 理论计算机：自动机、可计算性、复杂度（P/NP）可在掌握算法后学习。

**阶段项目**：实现一个命令行算法可视化器，比较不同输入规模下的时间/空间复杂度。

## 2. 编程语言

先选一门主力语言深入学习；其他语言以“能读、能写小项目”为目标。建议优先级：Python + C/C++，随后按方向补充。

| 语言 | 适合方向 | 首选资料 |
| --- | --- | --- |
| Python | AI、数据、自动化、后端 | [Python 官方教程](https://docs.python.org/3/tutorial/) · [NumPy](https://numpy.org/learn/) |
| C | 操作系统、嵌入式、理解内存 | [C Reference](https://en.cppreference.com/w/c) · [CS50 C](https://cs50.harvard.edu/x/) |
| C++ | 性能工程、系统、CUDA | [cppreference](https://en.cppreference.com/w/) · [C++ Core Guidelines](https://isocpp.github.io/CppCoreGuidelines/CppCoreGuidelines) |
| Java | 企业后端、JVM、Android 基础 | [dev.java Learn](https://dev.java/learn/) |
| JavaScript | Web 前端/全栈、工具链 | [MDN JavaScript Guide](https://developer.mozilla.org/docs/Web/JavaScript/Guide) |
| TypeScript | 大型前端/Node.js 工程 | [TypeScript Handbook](https://www.typescriptlang.org/docs/handbook/intro.html) |
| Rust | 系统编程、安全与并发 | [The Rust Programming Language](https://doc.rust-lang.org/book/) |
| Go | 云原生、网络服务、工具 | [A Tour of Go](https://go.dev/tour/) · [Effective Go](https://go.dev/doc/effective_go) |
| R | 统计分析、科研可视化 | [R for Data Science](https://r4ds.hadley.nz/) |

### 通用能力清单

- Git：分支、rebase、冲突解决、PR 评审；从 [Pro Git](https://git-scm.com/book/zh/v2) 开始。
- 调试与测试：断点、日志、单元测试、属性测试、性能基准。
- 工程规范：格式化、lint、依赖管理、API 设计、错误处理、代码评审。
- 并发：线程/协程、锁、原子操作、消息队列和竞态条件。

**阶段项目**：用主力语言实现一个带测试、CI 和基准测试的小型 REST 服务或 CLI 工具。

## 3. 系统、硬件与网络

### 操作系统与体系结构

- [OSTEP](https://pages.cs.wisc.edu/~remzi/OSTEP/)：进程、线程、虚拟内存、文件系统与并发。
- [CS:APP](https://csapp.cs.cmu.edu/)：程序性能、链接、异常控制流、缓存与网络。
- [MIT 6.S081 / xv6](https://pdos.csail.mit.edu/6.S081/)：通过实现操作系统理解内核。
- [Berkeley CS61C](https://cs61c.org/)：指令集、流水线、内存层次和并行。
- [Computer Architecture: A Quantitative Approach](https://www.elsevier.com/books/computer-architecture/hennessy/978-0-12-811905-1)：性能建模与现代处理器架构。

### 网络与分布式系统

- [Computer Networking: A Top-Down Approach](https://gaia.cs.umass.edu/kurose_ross/)：TCP/IP、HTTP、DNS、拥塞控制。
- [Beej's Guide to Network Programming](https://beej.us/guide/bgnet/)：Socket 编程实践。
- [MIT 6.5840](https://pdos.csail.mit.edu/6.824/)：复制、Raft、一致性与容错。
- [Designing Data-Intensive Applications](https://dataintensive.net/)：日志、流处理、复制与数据系统设计。

**阶段项目**：实现简易 Shell、线程池、KV 存储或基于 Socket 的聊天室；使用 profiler 找出并解释一个性能瓶颈。

## 4. 数据与 SQL

### SQL 与关系数据库

- [SQLBolt](https://sqlbolt.com/)：交互式 SQL 入门。
- [PostgreSQL Tutorial](https://www.postgresql.org/docs/current/tutorial.html)：以 PostgreSQL 学习标准 SQL 和数据库实践。
- [CMU 15-445/645](https://15445.courses.cs.cmu.edu/)：查询执行、索引、并发控制和恢复。
- [Use The Index, Luke](https://use-the-index-luke.com/)：索引与查询优化。

### 推荐学习顺序

1. SELECT、JOIN、GROUP BY、子查询、窗口函数与 CTE。
2. 关系模型、范式、DDL/DML、约束和迁移。
3. 索引、EXPLAIN、事务隔离级别、锁与 MVCC。
4. OLTP/OLAP、数据仓库、ETL/ELT、批处理与流处理。
5. 需要时学习 Redis、Elasticsearch、ClickHouse、Spark 等专用系统，并先理解它们与关系数据库的边界。

**阶段项目**：为一个业务场景设计 schema，导入模拟数据，写出关键报表 SQL，并用 EXPLAIN 优化慢查询。

## 5. 软件工程与云原生

- 架构与设计：模块边界、领域建模、接口契约、可观测性、限流与降级。
- 测试与交付：单元/集成/E2E 测试、CI/CD、版本管理、灰度发布、回滚。
- 容器与编排：[Docker Get Started](https://docs.docker.com/get-started/) · [Kubernetes Basics](https://kubernetes.io/docs/tutorials/kubernetes-basics/)。
- 可观测性：[OpenTelemetry](https://opentelemetry.io/docs/)；掌握 logs、metrics、traces 三件套。
- 安全：认证与授权、密钥管理、依赖漏洞、OWASP Top 10、最小权限。

**阶段项目**：把一个服务容器化，加入健康检查、结构化日志、指标和 CI；部署到本地 Kubernetes 或云端沙箱。

## 6. AI、机器学习、大模型与智能体

### 机器学习与深度学习

- [Stanford CS229](https://cs229.stanford.edu/)：监督/无监督学习、学习理论与强化学习入门。
- [Dive into Deep Learning](https://d2l.ai/)：边写代码边掌握深度学习。
- [Stanford CS231n](https://cs231n.stanford.edu/)：CNN、视觉与反向传播。
- [Stanford CS224N](https://web.stanford.edu/class/cs224n/)：词向量、Transformer、NLP 与 LLM 基础。
- [Stanford CS234](https://web.stanford.edu/class/cs234/)：强化学习。
- [PyTorch Tutorials](https://docs.pytorch.org/tutorials/)：训练循环、分布式训练与工程实践。

### 大模型与应用

- [Stanford CS324](https://stanford-cs324.github.io/winter2022/)：语言模型全生命周期与社会影响。
- [Full Stack Deep Learning](https://fullstackdeeplearning.com/)：从模型原型到生产系统。
- [Hugging Face Course](https://huggingface.co/learn/nlp-course/chapter1/1)：Transformers、数据集与推理工具。
- 建议掌握：tokenization、注意力机制、预训练/微调、LoRA、RAG、评测、推理成本、幻觉与安全。

### Agent（智能体）

- [Model Context Protocol](https://modelcontextprotocol.io/)：学习模型如何安全地连接工具与数据源。
- [LangGraph 学习中心](https://langchain-ai.github.io/langgraph/)：状态、工作流、多步骤执行与持久化。
- [Anthropic: Building effective agents](https://www.anthropic.com/engineering/building-effective-agents)：从工作流到自主 Agent 的工程取舍。
- 学习重点：工具调用、结构化输出、上下文管理、记忆、规划、检索、可观测性、人工介入和权限边界。
- 先实现确定性 workflow，再在必要处增加模型决策；为每个工具调用设计权限、超时、重试和审计日志。

**阶段项目**：实现一个有评测集的 RAG 或 Agent 应用。它至少应包含检索/工具调用、失败回退、日志追踪和成本/质量评估。

## 7. GPU、NPU、并行计算与算子开发

这一板块是“硬件架构 × 并行程序设计 × 深度学习框架”的交叉点。推荐先理解线程、缓存、矩阵乘法和性能分析，再写自定义算子。

### CUDA / NVIDIA GPU

1. [CUDA 平台与学习资源](https://developer.nvidia.com/cuda)：理解 GPU 编程环境、工具链和加速库。
2. [CUDA C++ Programming Guide](https://docs.nvidia.com/cuda/cuda-c-programming-guide/)：线程层级、内存模型、执行模型与同步。
3. [CUDA C++ Best Practices Guide](https://docs.nvidia.com/cuda/cuda-c-best-practices-guide/)：合并访存、占用率、流水线和性能验证。
4. [CUDA Samples](https://developer.nvidia.com/cuda-code-samples)：从 matrix multiply、reduction、scan 等案例练习。
5. [Nsight Systems](https://developer.nvidia.com/nsight-systems) 与 [Nsight Compute](https://developer.nvidia.com/nsight-compute)：用数据而不是直觉做性能优化。
6. 进阶：[CUTLASS](https://github.com/NVIDIA/cutlass) · [Triton](https://triton-lang.org/main/index.html)；学习 tile、warp/CTA 划分与 fused kernel。

### 华为昇腾 / CANN / Ascend C

1. [CANN Learning Hub：Ascend C 算子开发](https://gitcode.com/cann/cann-learning-hub/tree/master/tutorials/ascendc_operator_development)：从样例与目录结构入门。
2. [昇腾社区 CANN 文档](https://www.hiascend.com/document)：根据当前 CANN 版本选择安装、算子开发与性能调优文档。
3. 重点掌握：AI Core 执行模型、Global/Local/UB 等存储层级、数据搬运、Vector/Cube 计算、流水和同步、tiling、host/kernel 分工、算子注册与测试。
4. 使用 profile 工具定位数据搬运、访存和计算瓶颈；每次优化都保留 baseline、输入规模和测量方法。

### 算子开发通用路线

1. **正确性**：先写 CPU/reference 实现，覆盖随机、边界和异常输入。
2. **并行分解**：明确 batch、tile、线程块/核的映射，避免重复工作。
3. **内存访问**：连续访问、对齐、重用、减少全局内存往返。
4. **融合与流水**：减少 launch 与中间张量；在寄存器/共享内存/UB 中保持数据局部性。
5. **性能验证**：固定硬件、版本、形状、精度和预热策略；同时报告吞吐、时延与正确性误差。

**阶段项目**：从 vector add、reduction、softmax、layer norm、GEMM 开始，逐步实现并优化一个 PyTorch CUDA 扩展或 Ascend C 自定义算子；每一步附 benchmark 表。

## 8. Stanford CS 课程导航

[Stanford CS Catalog](https://explorecourses.stanford.edu/search?q=CS&view=catalog&page=0&academicYear=&filter-term-Autumn=on&filter-term-Winter=on&filter-term-Spring=on&filter-term-Summer=on&collapse=&filter-catalognumber-CS=on&filter-departmentcode-CS=on&filter-coursestatus-Active=on) 是课程编号、学期与先修要求的权威入口。可按以下路径选课：

| 目标 | 推荐课程序列 |
| --- | --- |
| 编程与算法 | CS106A → CS106B → CS161 |
| 系统 | CS107 → CS110 → CS140 / CS144 |
| 数据与软件 | CS109 → 数据库、分布式系统、软件工程相关课程 |
| 机器学习 | CS229 → CS231N / CS224N → CS234 / CS324 |
| AI 基础 | CS221 → CS229 → 选择视觉、NLP、RL 或系统方向 |
| 计算机体系结构 | CS107 → CS61C 类似课程基础 → 体系结构、并行系统与编译器课程 |

课程每学期会调整；应以 catalog 和课程主页的最新 syllabus 为准，不应只依赖旧讲义或二手整理。

## 9. 推荐的四条主线

### A. AI 应用 / Agent

Python → 数据结构与概率 → CS229 / D2L → PyTorch → Transformer 与 RAG → Agent workflow → 评测、可观测性、部署。

### B. 高性能 AI / 算子

C++ → CS:APP / 体系结构 → CUDA 基础 → profiler → GEMM/attention/normalization → CUTLASS/Triton 或 Ascend C → 框架集成与基准测试。

### C. 后端与数据

Python/Java/Go → 网络与 Linux → SQL/PostgreSQL → 缓存与消息队列 → 分布式系统 → Docker/Kubernetes → 可观测性与安全。

### D. 系统与底层

C → 数据结构与算法 → OS/网络/体系结构 → xv6/Socket/并发项目 → 编译器、存储、数据库或嵌入式专项。

## 贡献指南

欢迎用 Issue 或 PR 补充资源。请尽量遵循：

- 按知识主题归类，而不是只按机构或平台堆链接。
- 优先官方文档、开源课程主页、原始论文/代码库；标注语言和适合阶段。
- 每个新增资源说明“学什么、前置知识、为什么值得学”。
- 避免收录盗版、失效、强制登录且无公开价值的材料。
- 链接失效、课程版本变化或内容重复时，请直接提出修正。

---

持续学习的关键不是收藏更多链接，而是形成“概念 → 实现 → 测量 → 复盘”的闭环。

## 10. 中文视频补充（B站）

B站适合用中文讲解快速建立直觉、跟着实操环境和复盘难点；**知识定义、API 版本、作业与许可证仍以本 README 中的官方课程/文档为准**。下列主题检索页比单个搬运视频更抗下架，也方便按最新、时长和字幕筛选；优先选择原作者、机构号或明确标注来源的视频。

| 板块 | B站入口 | 使用建议 |
| --- | --- | --- |
| 数学、数据结构与算法 | [线性代数/概率/算法](https://search.bilibili.com/all?keyword=%E7%BA%BF%E6%80%A7%E4%BB%A3%E6%95%B0%20%E6%A6%82%E7%8E%87%E8%AE%BA%20%E6%95%B0%E6%8D%AE%E7%BB%93%E6%9E%84%20%E7%AE%97%E6%B3%95) | 用视频建立直觉，再做题和实现。 |
| Python、C/C++ | [Python](https://search.bilibili.com/all?keyword=Python%20%E7%BC%96%E7%A8%8B%20%E6%95%99%E7%A8%8B) · [C/C++](https://search.bilibili.com/all?keyword=C%2B%2B%20%E7%BC%96%E7%A8%8B%20%E6%95%99%E7%A8%8B) | 重点跟做调试、内存和工程练习。 |
| Java、JS/TS、Rust、Go、R | [Java](https://search.bilibili.com/all?keyword=Java%20%E7%BC%96%E7%A8%8B%20%E6%95%99%E7%A8%8B) · [JS/TS](https://search.bilibili.com/all?keyword=JavaScript%20TypeScript%20%E6%95%99%E7%A8%8B) · [Rust/Go/R](https://search.bilibili.com/all?keyword=Rust%20Go%20R%20%E7%BC%96%E7%A8%8B%20%E6%95%99%E7%A8%8B) | 版本差异较大时，回查各语言官方文档。 |
| 操作系统、体系结构、网络 | [操作系统/计算机网络](https://search.bilibili.com/all?keyword=%E6%93%8D%E4%BD%9C%E7%B3%BB%E7%BB%9F%20%E8%AE%A1%E7%AE%97%E6%9C%BA%E7%BD%91%E7%BB%9C%20%E8%AF%BE%E7%A8%8B) · [MIT 6.S081 中文字幕](https://www.bilibili.com/video/BV14h4oeAEvu/) | 视频配合 xv6 实验；不要只看不做 lab。 |
| SQL 与数据库 | [SQL/数据库](https://search.bilibili.com/all?keyword=SQL%20PostgreSQL%20%E6%95%B0%E6%8D%AE%E5%BA%93%20%E6%95%99%E7%A8%8B) | 用本地 PostgreSQL 跟写每一条查询。 |
| 工程化与云原生 | [Git/Docker/Kubernetes](https://search.bilibili.com/all?keyword=Git%20Docker%20Kubernetes%20%E6%95%99%E7%A8%8B) | 只把视频当环境搭建入口，实践中必须写 CI 和部署清单。 |
| 机器学习与深度学习 | [机器学习/深度学习](https://search.bilibili.com/all?keyword=%E6%9C%BA%E5%99%A8%E5%AD%A6%E4%B9%A0%20%E6%B7%B1%E5%BA%A6%E5%AD%A6%E4%B9%A0%20%E8%AF%BE%E7%A8%8B) · [CS229](https://search.bilibili.com/all?keyword=CS229%20%E6%9C%BA%E5%99%A8%E5%AD%A6%E4%B9%A0) | 对照公式、作业和代码；避免仅凭视频结论。 |
| LLM、RAG 与 Agent | [大模型/Agent](https://search.bilibili.com/all?keyword=LLM%20RAG%20AI%20Agent%20%E6%99%BA%E8%83%BD%E4%BD%93%20%E5%BC%80%E5%8F%91) | 关注工具调用、评测和权限控制，避免只做演示型 Demo。 |
| CUDA / GPU 算子 | [NVIDIA CUDA C++ 课程](https://www.bilibili.com/video/BV1QvSKB4EMr/) · [CUDA 编程检索](https://search.bilibili.com/all?keyword=CUDA%20C%2B%2B%20GPU%20%E7%BC%96%E7%A8%8B) | 公开视频与 NVIDIA 官方文档、samples 和 profiler 配套使用。 |
| CANN / Ascend C 算子 | [Ascend C 入门训练营](https://www.bilibili.com/video/BV1sa4y1X74n/) · [CANN/Ascend C 检索](https://search.bilibili.com/all?keyword=CANN%20Ascend%20C%20%E7%AE%97%E5%AD%90%E5%BC%80%E5%8F%91) | 按本机 CANN 版本对照官方文档和 Learning Hub。 |
| Stanford CS 课程 | [Stanford CS 课程检索](https://search.bilibili.com/all?keyword=Stanford%20CS106A%20CS229%20CS231N%20%E8%AF%BE%E7%A8%8B) | 核对学期和讲次，优先回到 Stanford 课程主页下载作业说明。 |

> B站视频可能是个人原创、课程复述或经过授权/未经授权的搬运；请尊重版权，并以来源明确的公开视频为优先选择。
