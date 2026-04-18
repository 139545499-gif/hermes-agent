# OpenClaw → Hermes 迁移计划

## 目标
- 安装 Hermes Agent（Nous Research 出品）
- 双跑验证（与现有 OpenClaw 并存）
- 保留所有数据和 Token
- 确认无误后完全替换

## 当前环境
- macOS 12.7.6 (Intel x86_64)
- Homebrew 5.1.6 ✅
- Node.js v22.14.0 ✅
- Python 3.14.4 ✅
- sudo 需要密码（手动步骤需用户执行）

## 安装步骤

### 1. 安装 Hermes（一键脚本）
```bash
curl -fsSL https://raw.githubusercontent.com/NousResearch/hermes-agent/main/scripts/install.sh | bash
```

### 2. 迁移配置
- 飞书 Bot: cli_a96a631086f99ccb
- 微信接入: wechat-access
- 模型: qclaw/modelroute
- 自定义技能目录: 3 个路径

### 3. 双跑验证
- 保持现有 OpenClaw 运行
- 启动 Hermes 并配置相同渠道
- 测试消息收发

### 4. 数据迁移
- 会话历史
- 记忆文件 (MEMORY.md)
- 自定义技能

## 关键差异
| 特性 | OpenClaw | Hermes |
|------|----------|--------|
| 配置格式 | openclaw.json | hermes.yaml |
| Gateway 端口 | 28789 | 默认 8080 |
| 技能系统 | AgentSkills | 兼容 agentskills.io |
| 记忆系统 | LCM | 内置学习闭环 |
| 自我改进 | 可选 skill | 内置 |

## 下一步
执行一键安装脚本
