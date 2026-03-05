# openclaw-add-feishu-bot

一个 [Claude Code](https://claude.com/claude-code) Skill，用于自动化向 [openclaw](https://github.com/nicepkg/openclaw) 注册新飞书 Bot 的完整流程。

## 功能

自动完成以下操作：

1. 编辑 `openclaw.json` 配置文件，添加飞书账户（支持单账户自动迁移为多账户格式）
2. 创建新 agent 并绑定到飞书账户
3. 创建 workspace 目录
4. 重启 openclaw gateway 服务
5. 执行 pairing approve（可选）

## 安装

```bash
claude install-skill /path/to/openclaw-add-feishu-bot
```

或直接从 GitHub 安装：

```bash
claude install-skill https://github.com/Moseschan/openclaw-add-feishu-bot
```

## 使用

在 Claude Code 中直接用自然语言触发即可，例如：

- "add feishu bot"
- "新增飞书 bot"
- "接入飞书"
- "register feishu app"

Skill 会要求你提供以下信息：

| 参数 | 说明 | 示例 |
|------|------|------|
| `agentId` | Bot/Agent 的唯一标识 | `dabao` |
| `appId` | 飞书开放平台的 App ID | `cli_a923823d9aba5ced` |
| `appSecret` | 飞书开放平台的 App Secret | `m7Lx82it3aLB9esksNvXbgKnZ13YA6YZ` |
| `pairingCode` | （可选）Bot 已加入群组时的配对码 | `LNPQR9W9` |

## 前置条件

- 已安装并配置 [openclaw](https://github.com/nicepkg/openclaw)
- 已在[飞书开放平台](https://open.feishu.cn/)创建应用并获取 App ID 和 App Secret
- openclaw gateway 已通过 launchctl 管理

## License

MIT
