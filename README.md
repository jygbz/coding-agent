# Coding Agent

基于 ReAct 工具调用循环的终端编程助手，包含多模型接入、MCP 工具发现、跨会话记忆、上下文压缩、权限确认和多 Agent 协作。

## 运行

需要 Python 3.11+ 和 uv。在项目根目录运行：

```bash
uv sync
cp .coding_agent/config.yaml.example .coding_agent/config.yaml
# 按示例配置模型供应商，通过环境变量配置 API Key
uv run coding_agent
```

入口：`coding_agent/__main__.py`；主循环：`coding_agent/agent.py`；记忆：`coding_agent/memory/`；权限：`coding_agent/permissions/`；平台沙箱：`coding_agent/sandbox/`；协作：`coding_agent/teams/`。

## 验证与迭代

目录包含记忆、压缩、MCP、权限和协作测试；本次发布整理仅做静态语法与名称一致性检查。尚未找到可支持简历中 Token 减少 85%、保留率 17%→100%、持续 8 小时、弹窗 30→5、协作耗时减少 60% 的完整实测报告，未将这些数值写为已验证成果。SWE-bench-Live 结果亦待提供。

## 来源与个人贡献边界

此仓库为基于参考源码的复现整理作品。命名、公开材料整理与原参考实现的归属分别说明；个人功能改造需以实际变更记录为据。参见 `THIRD_PARTY_NOTICES.md`。

## 本地配置与数据

密钥、数据库密码和管理账号由运行者在本地配置；仓库仅保留环境变量模板。测试账号使用 example.invalid，测试路径使用 /workspace，不对应真实人员或设备。源码中的演示/测试数据不代表线上用户数据。
