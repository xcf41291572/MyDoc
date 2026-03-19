# Claude Code

## 安装

[安装方法参考](https://www.runoob.com/claude-code/claude-code-install.html)

## 绕过VSCode登录页面

通过修改配置文件和设置环境变量，可以在 VSCode 中绕过 Claude Code 插件的强制登录验证，并接入自定义大模型服务。

- 找到配置文件路径（Linux/macOS: `~/.claude/config.json`，Windows: `%USERPROFILE%\.claude\config.json`）

- 编辑 config.json，添加任意字符串作为 `primaryApiKey`，例如 "primaryApiKey": "any-string-is-ok-here"。该字段仅用于本地状态校验，完成后重启 VSCode 即可绕过登录验证。

## 配置模型API

在（Linux/macOS: `~/.claude/settings.json`，Windows: `%USERPROFILE%\.claude\settings.json`）中配置。

配置参考(使用Deepseek模型)：

```json
"env": {
    "ANTHROPIC_AUTH_TOKEN": "YOUR API KEY",
    "ANTHROPIC_BASE_URL": "https://api.deepseek.com/anthropic",
    "ANTHROPIC_DEFAULT_HAIKU_MODEL": "deepseek-reasoner",
    "ANTHROPIC_DEFAULT_SONNET_MODEL": "deepseek-reasoner",
    "ANTHROPIC_DEFAULT_OPUS_MODEL": "deepseek-reasoner"
  },
```

