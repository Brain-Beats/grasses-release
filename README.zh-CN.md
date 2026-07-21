<p align="center">
  <img src="https://grasses.brainbeats.pro/assets/grasses-icon.png" width="96" height="96" alt="Grasses 图标">
</p>

<h1 align="center">Grasses</h1>

<p align="center"><strong>留在原处，读懂英文。</strong></p>

<p align="center">
  <a href="README.md">English</a>
  ·
  <a href="https://grasses.brainbeats.pro">官方网站</a>
  ·
  <a href="https://github.com/Brain-Beats/grasses-release/releases">下载</a>
  ·
  <a href="https://grasses.brainbeats.pro/privacy.html?lang=zh-CN">隐私政策</a>
</p>

Grasses 是一款原生 macOS 菜单栏英语阅读工具。你可以选中文字、读取剪贴板，或框选图片中的文字，然后在当前阅读内容旁边查看分析结果。

这个公开仓库是 Grasses 的官方分发渠道，将用于发布安装包和版本说明。应用完成自动更新集成后，Sparkle 更新源也会发布在这里。应用源代码在其他位置独立维护。

![Grasses 单词分析结果](https://grasses.brainbeats.pro/assets/grasses-result-light.png)

## 下载与安装

已发布的版本可从 [GitHub Releases](https://github.com/Brain-Beats/grasses-release/releases) 下载。如果页面中尚无 Release，说明首个公开版本还未发布。

1. 打开当前最新的可用 Release，下载 `Grasses.dmg`。
2. 打开磁盘映像，将 Grasses 拖入“应用程序”文件夹。
3. 启动 Grasses。它会常驻菜单栏，不会持续占用一个主窗口。
4. 选择 AI Provider，填写你自己的 API Key，并测试连接。

正式安装包会在发布前构建为同时支持 Apple 芯片和 Intel Mac 的通用版本，使用 Developer ID 证书签名，并经过 Apple 公证。

## 留在当前阅读现场

Grasses 将理解过程放在正在阅读的文字旁边，减少在浏览器标签和其他应用之间来回切换。

| 输入方式 | 默认快捷键 | 工作方式 |
| --- | --- | --- |
| 选中文字 | `Option + G` | 读取其他应用中当前选中的文字，完成后恢复原来的剪贴板内容。 |
| 剪贴板 | `Option + Shift + G` | 分析你主动复制的文字或图片。 |
| 屏幕区域 | `Option + Control + G` | 框选屏幕区域，在本机识别文字，并展示可点击的文本块。 |

所有快捷键均可在设置中修改。在 macOS 15 及以上版本中，新录制的 Option 快捷键必须同时包含 Command 或 Control；现有默认快捷键仍可使用。

## 根据文本提供不同结果

- **单词与短语：**提供词元、IPA、常见词形、词性、释义和例句，并使用 macOS 本机语音朗读。
- **句子：**并行返回翻译和语法分析，以可配置颜色标出主语、谓语、宾语、补语、修饰语等句子成分。
- **段落：**先给出完整翻译，再按需分析其中某一句，并在当前会话中复用已有结果。
- **图片：**使用本机 Vision OCR，保留文字行位置和阅读顺序，并允许选择具体文本块继续分析。

## AI 服务

Grasses 会从你的 Mac 直接连接到你配置的服务。应用内置以下 Provider 的默认配置：

- SiliconFlow
- DeepSeek
- 智谱
- Kimi
- Mimo
- 千问

API Key 由你自行提供，模型由你选择。凭据保存在 macOS 钥匙串中；对于仅支持固定模型列表的 Provider，Grasses 会明确拒绝不受支持的模型，而不是静默替换。

## 权限说明

Grasses 只会在你使用对应功能时请求系统权限：

- **辅助功能：**用于“读取选中内容”。你主动触发命令后，Grasses 会模拟复制、读取选中文字，然后恢复之前的剪贴板内容。
- **屏幕录制：**用于“阅读图片”。它只处理你手动框选的屏幕区域；Grasses 不会持续录屏，也不会在后台扫描屏幕。
- **剪贴板读取：**不需要额外系统权限，仅在你主动执行命令后运行。

你可以随时在“系统设置”中撤销权限，不使用该权限的其他工作方式仍然可用。

## 隐私

- Grasses 不要求注册账户，也不运营接收阅读内容的中转服务器。
- 截图和剪贴板图片留在 Mac 本机，仅用于 Vision OCR。
- 只有你选择分析的相关文本会直接发送到当前配置的 AI 服务。
- API Key 保存在 macOS 钥匙串中。
- Grasses 不建立阅读历史或图片历史。
- 诊断日志不包含 API Key、截图、完整选中文本、完整 OCR 文本或完整 AI 响应。

提交敏感文字前，请先确认所选 AI Provider 的隐私政策和账户设置符合你的需要。完整的数据处理、保留和删除说明请参阅[隐私政策](https://grasses.brainbeats.pro/privacy.html?lang=zh-CN)。

## 系统要求

- macOS 13 或更高版本
- Apple 芯片或 Intel Mac
- 使用分析功能需要受支持 AI 服务的 API Key

## 支持

- 邮箱：[support@grasses.brainbeats.pro](mailto:support@grasses.brainbeats.pro)
- 问题反馈：[GitHub Issues](https://github.com/Brain-Beats/grasses-release/issues)
- 官网：[grasses.brainbeats.pro](https://grasses.brainbeats.pro)

反馈问题时，请勿提交 API Key、私人阅读内容、包含敏感信息的截图或完整 AI 响应。
