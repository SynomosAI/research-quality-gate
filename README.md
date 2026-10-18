# research-quality-gate · 研究质量闸门

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE.md)
[![Agent Skill](https://img.shields.io/badge/Agent%20Skill-SKILL.md-blue.svg)](SKILL.md)
[![LLM-as-Judge](https://img.shields.io/badge/LLM-as--judge-5--dim-brightgreen.svg)](SKILL.md)
[![PDCA / ISO](https://img.shields.io/badge/PDCA-ISO%209001%20%7C%2017025-2ea44f.svg)](SKILL.md)
[![Evidence Card](https://img.shields.io/badge/evidence-6--grid-informational.svg)](SKILL.md)
[![Version](https://img.shields.io/badge/version-1.7.0-informational.svg)](SKILL.md)

SynomosAI 四支柱体系：**身份（Identity）· 溯源（Traceability）· 治理（Governance）· 共生（Symbiosis）**——当 AI 进入商业，可信是唯一的硬通货。

> 本仓库属于 [SynomosAI](https://github.com/SynomosAI) 生态技能包的一员。生态全景见 [`synomosai-skills`](https://github.com/SynomosAI/synomosai-skills)，理论站位见 [`traceability-audit`](https://github.com/SynomosAI/traceability-audit)。

**关键词 / Keywords**：研究质量门禁 · 6 格证据卡 · LLM-as-Judge 5 维评分 · 原子声明拆解 · 多 Agent 协作规范 · PDCA · 校准 · research quality gate · evidence-based · llm judge

调研 / 情报产物的**质量门禁与多 Agent 协作规范**。给调研报告做「6 格证据卡」合理性检查、5 维 LLM-as-Judge 评分（含原子声明拆解与偏见控制），并规定专家团内部协作范式。v1.3 起嵌入 PDCA 国际质量循环（Plan-Do-Check-Act），与 ISO 9001 / 14001 / 27001 / 17025 同构。

---

## ✨ 特性 / Features

- **6 格证据卡**：每条关键结论过 6 格检查（证据等级 GRADE / ICD 203 七档可能性词 / 来源摘要 SIFT / 备选假设三角验证 / 与上次判断异同 / 溯源包），缺任一格 = 不合理。
- **5 维 LLM-as-Judge**：事实准确（FActScore 式原子声明拆解）、引用精确（NLI 校验）、完整性、来源质量、工具效率；配偏见控制（维度随机化、跨模型裁判、独立打分不聚合）。
- **范围边界核对**：评估前先锁定既定范围，范围外未做不计为短板（v1.5）。
- **复现性阈值**：跨 judge Cohen's κ ≥ 0.4；κ<0.4 触发复评 / 升级人类（v1.7）。
- **R&R 实操模板**：客观 grounding 率 + N=5 复跑 + 配置变体，按 ISO 5725 做稳定性自证（v1.6）。
- **多 Agent 协作 7 规范**：先独立并行后投票、辩论只作定向干预、异构化、共享完整执行轨迹等。

---

## 🚀 快速开始 / Quick Start

> 前置：把本目录放入 Agent 技能目录；本技能为方法论 / 模板型，无可执行依赖。

```bash
# 1. 克隆本仓
git clone https://github.com/SynomosAI/research-quality-gate.git
cd research-quality-gate

# 2. 查看门禁主文件（PDCA / 6 格证据卡 / 5 维评分卡）
cat SKILL.md

# 3. 查看校准记录
cat calibration-log.md
```

拿到一份调研报告后，先按 §二·补 核对范围边界，再逐条过 6 格证据卡，最后跑 5 维 LLM-as-Judge 评分。

```text
触发词示例：
  调研质量门禁 / 报告合理性检查 / 6 格证据卡
  专家团协作规范 / 调研质量尺 / ISO 5725 稳定性 / PDCA 调研框架
```

---

## 📖 使用方式 / Usage

1. 克隆本仓库或将技能目录放入 Agent 技能目录；
2. 调研报告产出后，按 `SKILL.md` 第二节做 6 格证据卡检查；
3. 按第三节做 5 维 LLM-as-Judge 评分（先原子声明拆解）；
4. 多 Agent 调研团队按第四节协作 7 规范组织并行检索与汇总。

### 6 格证据卡示例（节选）

```text
结论：「X 市场 2026 年渗透率约 60%」
  ① 证据等级：中（单一首源 + 外推，降级理由=不精确）
  ② 可能性词：highly likely（80–95%）—— 使用 ICD 203 七档
  ③ 来源摘要：一手行业报告 + 二手新闻；强弱已标注
  ④ 备选假设：若统计口径含免费用户，实际付费渗透可能仅 35%
  ⑤ 与上次判断：上季度为 52%，环比 +8pct
  ⑥ 溯源包：URL + 抓取时间 + 快照路径（已归档）
→ 6 格齐全，通过；否则退回补证。
```

---

## 🧩 仓库结构 / Repository layout

```text
research-quality-gate/
├── README.md                # 本文件
├── README.en.md             # 英文版说明
├── SKILL.md                 # 技能主文件（v1.7.0，PDCA/6格/5维/协作规范）
├── calibration-log.md        # 门禁自评偏差校准记录
├── LICENSE.md                # MIT License
├── llms.txt / llms-full.txt  # 给 AI 的索引与完整文本
├── AGENTS.md                 # 给 AI Agent 的工作指引
├── SECURITY.md               # 安全策略
└── CODEOWNERS                # 代码所有者
```

---

## 🔎 方法学背书 / Methodology

PDCA 显式载入 ISO 9001:2015 §0.3.2、14001:2015 §0.4、27001:2022、17025:2017（Annex SL 高阶架构）；证据卡借鉴 GRADE（WHO/Cochrane）、SIFT（Caulfield 2019）、三角验证（Denzin 1978）、Self-RAG（arXiv:2310.11511）；评分借鉴 FActScore（EMNLP 2023）、G-Eval（EMNLP 2023）、Prometheus（ICLR 2024）。诚实边界：ISO 20252:2019 正文未出现「PDCA」一词，对标表述为「对齐其规划-交付-评审-改进」。

---

## ❓ 常见问题 / FAQ

- **评分是绝对标准吗？** 5 维 0–1 分需人类校准相关性 ≥0.7 才可信；跨 judge κ<0.4 触发复评。
- **范围外没做的项算短板吗？** 不算。Check 第 0 步先锁范围，范围外不评。
- **能直接用于商业报告吗？** 本技能为方法论框架；正式报告的法律 / 合规结论请独立核实。

---

## License / 许可

本项目以 **MIT** 许可发布，详见仓库根目录 [LICENSE.md](LICENSE.md)。版权：© 2026 注册老炮@MedXpert。

---

## 🔒 安全 / Security

如发现安全问题，请按 [`SECURITY.md`](SECURITY.md) 的方式私下报告，不要在公开 issue 中披露。

## 🤝 贡献 / Contributing

欢迎补充证据卡规则、评分锚点与校准记录；修改 `SKILL.md` 时保持 YAML frontmatter 字段兼容。代码所有者见 [CODEOWNERS](CODEOWNERS)。

---

## 免责声明

本仓库内容为 SynomosAI 的**理论站位与工具化探索**，不代表任何已获认证、已商业化交付或已服务特定客户的声明；文中涉及的 ISO 9001 / 14001 / 27001 / 17025 / 20252、GRADE、FActScore 等外部标准与文献信息为公开资料转述，正式引用前请**独立核实**。API、授权码与形象大使等为路线图（roadmap）事项，尚未上线。
