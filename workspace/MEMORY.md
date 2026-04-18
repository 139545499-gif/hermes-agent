# MEMORY.md - 虾虾的长期记忆 🦐

## 关于大哥
- **姓名：** 陈洪祥
- **称呼：** 大哥
- **时区：** Asia/Shanghai (GMT+8)
- **设备：** MacBook Air (Darwin 21.6.0, x64)，性能有限，避免重任务

## 系统配置（Hermes Agent - 2026-04-18 迁移完成）
- **Hermes Agent v0.10.0**（从 OpenClaw/QClaw 迁移）
- **安装路径：** ~/.hermes/hermes-agent
- **虚拟环境：** ~/.hermes/hermes-agent/venv (Python 3.11.15 via uv)
- **模型路由：** QClaw Gateway (http://127.0.0.1:19000/proxy/llm)，模型名 modelroute
- **飞书 Bot：** cli_a96a631086f99ccb，Bot名=涔虾，WebSocket 模式 ✅
- **飞书群：** 虾家军团队群，chat_id=`oc_dba6ed42187b10b03252d6a5d2741f48`
- **微信：** 待配置（Hermes 用 iLink Bot API，需重新扫码，与 OpenClaw wechat-access 协议不同）
- **QClaw 保留运行中：** 双跑验证阶段，确认 Hermes 稳定后完全迁移
- **OpenClaw 数据已迁移：** 9个会话/913条消息、记忆文件、QMemory、auto-memory

## OKX 网格机器人
- **版本：** v3.1，由 systemd 管理在远程服务器（SSH: tencent）
- **策略：** ETH 现货网格，间距 ~24.2U，每档 0.001 ETH
- **价格区间：** 2347-2493（截至 2026-04-18）
- **账户：** 总资产 29.84 USDT，收益率 +49.22%，ETH 0.0002
- **SSH 别名：** tencent (43.128.57.189, root, 密钥 ~/Downloads/xiaxiazhuanyong.pem)
- **面板：** http://43.128.57.189:2658 (admin/8782242chx)
- 飞书机器人正常运行（WebSocket 模式），缺少 im:chat 和 im:chat:create 权限，无法创建群/拉人，需用户手动操作

## 已安装技能
- 内置 47 个 + 用户 5 个（atomgit-mcp, auto-memory, claw-code, persona-switch, screenshot）
- 待探索：github-skill, notion, session-logs, mcporter

## 经验教训
1. **看 gateway 日志要看对的进程** — 之前看了旧的 launchd gateway 日志，误判飞书未启动
2. **残留 gateway 进程要及时清理** — PID 486 运行超7小时仍残留
3. **MacBook Air 内存有限** — 两个 gateway 进程合计 380MB，需注意资源占用

## 待办
- [ ] OKX 机器人网格区间与挂单价格有偏差，建议大哥检查是否需要重置
- [ ] 评估是否启用 github-skill / notion / session-logs
- [ ] 7个 agent 的名字和分工（大哥自己配置）
- [ ] 抖音短视频变现 & 闲鱼方向研究

## 密钥

## 经验与决策

- OKX 网格机器人 bug：create_grid() 函数曾无条件调用 cancel_all()，已修复为仅在 force=True 时调用，文件为 bot_v32_fixed.py
- webchat（OpenClaw 控制 UI）不支持文件上传，截图需通过飞书群或本地文件夹中转
