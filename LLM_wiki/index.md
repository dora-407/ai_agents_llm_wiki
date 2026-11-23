# AI Agents 學術知識庫目錄 (Wiki Index)

> 最後更新時間：2026-11-23  
> 本檔案由 LLM Agent 自動維護，每次攝取（Ingest）新論文或建立新架構概念時同步更新。

---

## 導覽結構

```
[[index]] 全庫索引
├── [[wiki/concepts/|核心認知概念 (Concepts)]]
├── [[wiki/architectures/|典型架構模式 (Architectures)]]
├── [[wiki/evaluations/|評測基準與方法論 (Evaluations)]]
├── [[wiki/synthesis/|專題綜述與橫向比較 (Synthesis)]]
└── [[wiki/sources/|原始文獻解讀 (Sources)]]
```

---

## 1. 核心認知概念 (Concepts)

* [[Taxonomy of Intelligent Agents]] — 智慧代理分類學：界定 Generative AI、AI Agents、Agentic AI 與 Generative Agents 的四大認知範式階層與選型邊界。(2026-11-23)
* [[Agent Memory Systems]] — 代理記憶系統架構：深入工作記憶、情節記憶、語義記憶、分段分頁中期記憶（MemoryOS）與向量共享記憶的分層運作。(2026-11-23)
* [[Agent Planning & Reasoning]] — 代理規劃與推理機制：從線性 CoT、閉環 ReAct、樹狀搜尋（LATS/Agent Q MCTS）到符號混合規劃（AutoGPT+P）與 Pareto 成本反思。(2026-11-23)
* [[Tool Augmentation & Function Calling]] — 工具增強與函式調用：LLM 從被動文字預測走向主動操縱環境與 API 的中介執行閉環與安全防護。(2026-11-23)

---

## 2. 典型架構模式 (Architectures)

* [[Multi-Agent Orchestration]] — 多智能體編排架構：集中式 Meta-Agent 編排、去中心化協同、Google A2A 協議、SOP 與角色約束（Role-bound）機制。(2026-11-23)
* [[Single vs Multi-Agent Patterns]] — 單體與多代理架構模式：垂直層級（領導者提速 10%）與水平對等拓撲對比，破解群聊客套與諂媚效應。(2026-11-23)
* [[MemoryOS]] — 智慧代理記憶作業系統：北京郵電與騰訊提出之 OS 級 3 層階層式記憶（STM/MTM/LPM）、主題分段分頁與熱度置換算法。(2026-11-23)
* [[Agent Q]] — 自主演化網頁代理架構：MultiOn 與史丹佛提出之推論期 MCTS 樹搜尋 + AI 過程自省 + 離線 Trajectory-DPO 強化學習。(2026-11-23)

---

## 3. 評測基準與方法論 (Evaluations)

* [[Cost-Controlled Agent Benchmarking]] — 成本受控之代理評測方法論：普林斯頓團隊揭露無成本對照的虛假 SOTA，提出 Pareto 前沿與 4 級泛化保留集規範。(2026-11-23)
* [[LoCoMo]] — 長週期對話記憶評測基準：ACL 2024 提出之 300 輪、9K Tokens 超長跨期對話記憶基準測試。(2026-11-23)

---

## 4. 專題綜述與橫向比較 (Synthesis)

* [[Challenges and Failure Modes of Agentic Systems]] — 智慧代理系統之失效模式與挑戰綜述：橫向剖析因果缺失、多體誤差級聯、群聊諂媚、評測作弊與成本失控四大系統級危機。(2026-11-23)
* [Agent Planning & Reasoning 學術圖譜版簡報 (Graph Edition HTML)](file:///c:/Users/User/OneDrive/文件/LLM_wiki/presentations/agent_planning_and_reasoning_graph_edition.html) — 10 頁學術嚴謹型 Graph 向量圖解簡報，含精確架構拓撲、向量示意圖與論文小字引註。(2026-11-23)
* [Agent Planning & Reasoning 基礎教學簡報 (Original HTML)](file:///c:/Users/User/OneDrive/文件/LLM_wiki/presentations/agent_planning_and_reasoning.html) — 初學者友好版互動簡報。(2026-11-23)

---

## 5. 原始文獻解讀 (Sources)

* [[2026 - Sapkota et al - AI Agents vs Agentic AI]] — *Information Fusion* 奠基綜述：全面解構 AI Agents 與 Agentic AI 之架構演進、10 大挑戰與 10 大解方。(2026-11-23)
* [[2025 - Kang et al - Memory OS of AI Agent]] — *EMNLP 2025*：提出 MemoryOS，以 OS 分段分頁與熱度置換攻克長週期對話記憶與 90 維個人化。(2026-11-23)
* [[2024 - Masterman et al - Landscape of Emerging AI Agent Architectures]] — *IBM/Microsoft Survey*：單體與多體拓撲（垂直 vs 水平）、領導力實證與 AgentVerse/MetaGPT 梳理。(2024-04-17)
* [[2024 - Kapoor et al - AI Agents That Matter]] — *Princeton University*：重磅批判評測虛火，提出成本受控、Pareto 前沿與基準保留集。(2024-07-02)
* [[2024 - Putta et al - Agent Q]] — *MultiOn & Stanford*：結合導引式 MCTS 樹搜尋、過程批判與 Trajectory-DPO，攻克長程網頁預訂與責任分配難題。(2024-08-13)
