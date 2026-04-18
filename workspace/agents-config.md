# 飞书多 Agent 配置

> 最后更新：2026-04-17

## 当前 OpenClaw Agent 状态

| # | Agent ID | 用途 | 状态 |
|---|----------|------|------|
| 1 | main (defaults) | 主助手，日常对话 | ✅ 运行中 |
| 2–8 | _(待配置)_ | 专项agent | ❌ 未创建 |

---

## 规划：7个专项 Agent（待大哥确认）

| # | 名字 | 职能 | 模型 | 触发词 |
|---|------|------|------|--------|
| 1 | **虾虾** | 主助手，日常对话、记忆、提醒 | qclaw/modelroute | 默认 |
| 2 | **虾盯盘** | 盯OKX网格机器人、报告状态 | qclaw/modelroute | @盯盘 |
| 3 | **虾百科** | 搜索、查询、知识问答 | qclaw/modelroute | @百科 |
| 4 | **虾写手** | 内容创作、文案、报告 | qclaw/modelroute | @写手 |
| 5 | **虾秘书** | 飞书文档、表格、会议管理 | qclaw/modelroute | @秘书 |
| 6 | **虾猎手** | 浏览器自动化、信息抓取 | qclaw/modelroute | @猎手 |
| 7 | **虾技师** | 代码、技术问题、脚本编写 | qclaw/modelroute | @技师 |
| 8 | **虾监控** | 后台巡检、定时汇报、异常告警 | qclaw/modelroute | @监控 |

---

## 配置方式

通过 OpenClaw 配置 `agents` 字段，每个 agent 有：
- `id`：唯一标识
- `name`：显示名字
- `description`：职能描述
- `systemPrompt`：人格设定
- `model`：使用模型
- `triggerKeywords`：触发关键词（飞书里@时用）

---

## 飞书机器人信息

| 项目 | 值 |
|------|-----|
| App ID | cli_a96a631086f99ccb |
| Bot 名 | 涔虾 / 虾虾 |
| open_id | ou_bee737b19a5d6687c97453c3f6cff16c |
| 所在群 | 虾家军团协作群 |
| 权限数 | 103个 |

---

## 待大哥确认

1. 这8个名字和分工合适吗？要不要调整？
2. 每个agent的性格设定要什么样？（严肃型/轻松型/专业型？）
3. 要不要给每个agent配上不同的头像/emoji？
