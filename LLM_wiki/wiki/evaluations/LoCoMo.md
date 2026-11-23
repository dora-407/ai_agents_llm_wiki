---
title: "LoCoMo Benchmark (長週期對話記憶評測基準)"
type: evaluation
tags:
  - ai-agents
  - memory
  - benchmarks
  - evaluation
created_at: 2026-11-23
updated_at: 2026-11-23
sources:
  - "[[2025 - Kang et al - Memory OS of AI Agent]]"
---

# LoCoMo Benchmark (長週期對話記憶評測基準)

**LoCoMo (Evaluating Very Long-Term Conversational Memory of LLM Agents)** 是專為評測大型語言模型智慧代理在**超長週期、多輪交互中的長效記憶能力**所設計的學術基準測試（Maharana et al., ACL 2024；在 [[2025 - Kang et al - Memory OS of AI Agent]] 中作為核心評測基準）。

---

## 1. 基準特性與數據規格

* **對話長度**：平均每段對話高達 **300 輪（Turns）**，上下文規模約 **9,000 Tokens**。
* **評測目標**：測試代理在面臨巨大時間跨度與頻繁主題切換時，能否精準提取歷史事實、維持使用者個人偏好（Persona Consistency），並抵抗上下文衰減。

---

## 2. 四大問題分類 (Problem Taxonomy)

LoCoMo 將評測問題劃分為四個核心維度，全面檢驗記憶的不同面向：

1. **Single-hop (單跳檢索)**：
   * 考察代理能否從數百輪對話前直接檢索出單一明確事實（如使用者在第一天提到的寵物名稱）。
2. **Multi-hop (多跳關聯推理)**：
   * 需要代理整合跨越多個不同會話（Sessions）的多項事實才能推導出答案。
3. **Temporal Reasoning (時間推理)**：
   * 考察代理對事件先後順序、時間間隔與時態演進的理解能力（如「使用者是在去公園之前還是之後開始健身的？」）。
   * *注：MemoryOS 在此類別取得超過 118% 的 F1 突破性提升。*
4. **Open-domain (開放領域綜合)**：
   * 結合外部常識與歷史對話背景的綜合問答。

---

## 3. 評測指標與主流架構表現

* **評測指標**：標準 F1 分數與 BLEU-1。
* **主流記憶架構對比 (基底模型: GPT-4o-mini)**：

| 記憶機制 / 架構 | Single-hop F1 | Multi-hop F1 | Temporal F1 | Open-Domain F1 | 平均排名 |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **MemoryBank** | 5.00 | 9.68 | 5.56 | 6.61 | 5.0 |
| **TiM (Think-in-Memory)** | 16.25 | 18.43 | 8.35 | 23.74 | 3.8 |
| **MemGPT** | 26.65 | 25.52 | 9.15 | 41.04 | 2.2 |
| **A-Mem (Agentic Memory)** | 27.02 | **45.85** | 12.14 | 44.65 | 2.0 |
| **[[MemoryOS]]** | **35.27** | 41.15 | **20.02** | **48.62** | **1.0 (最優)** |

---
## 引用來源
* [[2025 - Kang et al - Memory OS of AI Agent]]
* [[MemoryOS]]
* [[Agent Memory Systems]]
