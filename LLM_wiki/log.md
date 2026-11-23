# 知識庫操作日誌 (Operation Log)

本檔案為追加式日誌（Append-only），按時間倒序或順序記錄對知識庫發起的每次操作（Ingest, Query, Lint）。

---

## [2026-11-23] init | 知識庫架構初始化
- **操作類型**: 系統初始化
- **建立核心文件**:
  - `AGENTS.md`：定義 AI Agent 學術架構知識庫之憲法與自動編譯規範
  - `index.md`：建立目錄骨架
  - `log.md`：建立日誌追蹤
- **說明**: 知識庫準備就緒，後續將 PDF 論文放置於 `raw/` 目錄即可觸發自動編譯與網狀鏈接更新。


## [2026-11-23] ingest | AI Agents vs. Agentic AI: A Conceptual taxonomy, applications and challenges
- **檔案**: `raw/1-s2.0-S1566253525006712-main.pdf`
- **建立來源頁**: [[2026 - Sapkota et al - AI Agents vs Agentic AI]]
- **更新/新建概念與架構頁面**:
  - [[Taxonomy of Intelligent Agents]] (新建：定義四大智慧範式與選型權衡)
  - [[Agent Memory Systems]] (新建：梳理 Working, Episodic, Semantic, Vector 記憶架構)
  - [[Agent Planning & Reasoning]] (新建：剖析 CoT, ReAct, ToT 與因果模擬規劃)
  - [[Tool Augmentation & Function Calling]] (新建：梳理工具調用閉環、API 路由與安全防護)
  - [[Multi-Agent Orchestration]] (新建：梳理集中式、去中心化與 Google A2A 編排協議)
  - [[Challenges and Failure Modes of Agentic Systems]] (新建：橫向綜述因果缺失、誤差級聯與突現不穩定性)
- **更新目錄**: [[index]]
- **核心理論收穫**: 本文作為知識庫的奠基綜述，形式化區分了「AI Agents (單體工具增強)」與「Agentic AI (分散式多體生態)」的能力界限，並為全庫的記憶、規劃、編排與失效模式奠定了統一的概念座標系。


## [2026-11-23] batch-ingest | 自動批量編譯 4 篇關鍵學術論文
- **檔案清單**:
  - `raw/2025.emnlp-main.1318.pdf`
  - `raw/2404.11584v1.pdf`
  - `raw/2407.01502v1.pdf`
  - `raw/2408.07199v1.pdf`
- **新建來源頁**:
  - [[2025 - Kang et al - Memory OS of AI Agent]] (EMNLP 2025: MemoryOS 階層分頁記憶作業系統)
  - [[2024 - Masterman et al - Landscape of Emerging AI Agent Architectures]] (IBM/Microsoft: 單體與多體拓撲、領導力效能實證)
  - [[2024 - Kapoor et al - AI Agents That Matter]] (Princeton: 成本受控評測、Pareto 前沿、破除 System 2 盲信)
  - [[2024 - Putta et al - Agent Q]] (MultiOn/Stanford: MCTS 樹搜尋 + 過程自省 + Trajectory-DPO 自主演化網頁代理)
- **新建架構與評測專頁**:
  - [[MemoryOS]] (新建架構頁：作業系統級分段分頁與熱度置換演算法)
  - [[Single vs Multi-Agent Patterns]] (新建架構頁：垂直層級 vs 水平對等拓撲、領導者影響與防閒聊機制)
  - [[Agent Q]] (新建架構頁：推論期算力擴展、POMDP 網頁狀態壓縮與離線偏好強化學習)
  - [[Cost-Controlled Agent Benchmarking]] (新建評測頁：Pareto 前沿、4 級泛化保留集規範與作弊捷徑防範)
  - [[LoCoMo]] (新建評測頁：300 輪、9K Tokens 超長週期對話記憶基準)
- **回填與深度更新頁面**:
  - [[Agent Memory Systems]] (更新：整合 MemoryOS 3 層架構、熱度淘汰公式、90 維畫像及主流架構評測對比)
  - [[Agent Planning & Reasoning]] (更新：整合 MCTS 樹搜尋、推論期算力擴展、AutoGPT+P 符號規劃，以及普林斯頓對 System 2 增益來源的反思)
  - [[Multi-Agent Orchestration]] (更新：補充垂直領導力 10% 提速實證、MetaGPT 結構化工件、DyLAN 與 AgentVerse 生命週期)
  - [[Challenges and Failure Modes of Agentic Systems]] (更新：擴展諂媚盲從、基準作弊捷徑、可重現性危機與真實環境線上探索風險)
- **更新目錄導航**: [[index]]
- **核心理論收穫**: 本次批量編譯實現了知識庫的網狀化躍遷。不僅在**記憶維度**引入了 OS 級的分段分頁實作（MemoryOS），在**規劃維度**確立了 MCTS 推論期搜尋與離線強化學習路徑（Agent Q），更在**評測與方法論維度**導入了批判性的成本控制思維（Kapoor et al.），使知識庫具備嚴謹的帕雷托架構選型視角。


## [2026-11-23] presentation | 產出 Agent Planning & Reasoning 教學型 HTML 簡報
- **產出檔案**: `presentations/agent_planning_and_reasoning.html`
- **主題**: 針對初學者的 Agent 規劃與推理架構全景解析（10 頁沉浸式互動 Slide Deck）
- **核心教學內容**:
  1. Chatbot vs. Agent 的本質差異（被動文字接龍 vs 目標導向行動）
  2. CoT（自言自語）到 ReAct（思考-行動-觀察閉環）的躍遷
  3. Reflexion（語言自省與情節記憶修復）
  4. MCTS 樹搜尋與推論期算力擴展（Agent Q 在 OpenTable 達 95.4% 的突破）
  5. AutoGPT+P 神經-符號混合規劃（結合 PDDL 確保物理約束）
  6. 普林斯頓《AI Agents That Matter》成本受控評測（Warming $2.45 vs LATS $134.50）
  7. 終極因果缺失（Causal Deficit）與分佈外漂移
  8. 建構 Agent Planning 的四大黃金法則
- **關聯回填**: 更新 [[wiki/concepts/Agent Planning & Reasoning]] 與 [[index]]


## [2026-11-23] presentation | 產出學術圖譜版 HTML 簡報 (Graph Edition)
- **產出檔案**: `presentations/agent_planning_and_reasoning_graph_edition.html`
- **設計調整**:
  1. 刪除所有通俗口語比喻，全面採用學術嚴謹術語與認知機制表述。
  2. 每頁正中央皆內嵌高解析度 SVG 向量關係圖（演進路徑圖、閉環控制圖、誤差級聯圖、ReAct三角循環、Reflexion雙層自省、MCTS樹分叉回溯、神經符號管道、Pareto前沿座標圖、因果DAG對照圖）。
  3. 每頁底部皆附有小字正式學術論文出處（包含 Sapkota 2026, Yao 2023, Shinn 2023, Putta 2024, Kapoor 2024 等）。
  4. 保留原 `agent_planning_and_reasoning.html` 檔案供使用者對照比較。
- **更新索引**: [[index]]
