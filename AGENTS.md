# AGENTS.md — 给 AI Agent 的工作指引

本文件面向自动化 AI Agent。人类读者请看 [README.md](README.md)。

## 这个仓库是什么

`research-quality-gate` 是一个 **Agent Skill 发布包**，核心资产是 `SKILL.md`（PDCA 框架 + 6 格证据卡 + 5 维 LLM-as-Judge + 多 Agent 协作规范）与 `calibration-log.md`（校准记录）。把本目录放入 Agent 技能目录，即可对调研报告 / 情报产物做质量门禁。

## 可用的工作命令

```bash
cat SKILL.md                # 门禁主文件
cat calibration-log.md      # 校准记录
```

前置依赖：无运行时依赖（纯方法论 / 模板型技能）。

## 约定（Do）

- 修改 `SKILL.md` 时保持 YAML frontmatter 字段兼容（`name` / `version` / `license` / `author` 等）。
- 做任何质量评分前，先按 §二·补 锁定范围边界；范围外未做项不计为短板。
- 引用国际标准 / 文献时注明版本号（如 ISO 9001:2015 §0.3.2），并先联网查证。
- 5 维评分独立打分，不聚合为单一分；跨 judge κ<0.4 触发复评。

## 禁止（Don't）

- 不要改动 `LICENSE.md` 的版权主体（© 2026 注册老炮@MedXpert），也不要改 `SKILL.md` 的 `author` 字段。
- 不要声称「ISO 20252:2019 要求 PDCA」（正文未出现该词，属表述越界）。
- 不要在仓库内提交任何密钥、令牌或真实未脱敏调研数据。
- 不要把本门禁输出表述为法律 / 合规意见。

## 边界

本技能专注**研究产物质量门禁与多 Agent 协作规范**；不覆盖调研报告本身的撰写、不覆盖红队工具链实现。
