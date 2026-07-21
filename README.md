<p align="center">
  <img src="https://grasses.brainbeats.pro/assets/grasses-icon.png" width="96" height="96" alt="Grasses icon">
</p>

<h1 align="center">Grasses</h1>

<p align="center"><strong>Stay where you are. Understand English.</strong></p>

<p align="center">
  <a href="README.zh-CN.md">简体中文</a>
  ·
  <a href="https://grasses.brainbeats.pro">Website</a>
  ·
  <a href="https://github.com/Brain-Beats/grasses-release/releases">Download</a>
  ·
  <a href="https://grasses.brainbeats.pro/privacy.html?lang=en">Privacy</a>
</p>

Grasses is a native macOS menu bar companion for reading English. Select text, read from the clipboard, or capture text from an image, then get the analysis beside the content you are already reading.

This public repository is the official distribution channel for Grasses. It will host release packages and release notes. A Sparkle update feed will also be published here after automatic updates are integrated into the app. The application source code is maintained separately.

![Grasses word analysis result](assets/grasses-result-light-en.png)

## Download

Published builds are available from [GitHub Releases](https://github.com/Brain-Beats/grasses-release/releases). If no release is listed yet, the first public build has not been published.

1. Open the latest available release and download `Grasses.dmg`.
2. Open the disk image and drag Grasses into Applications.
3. Launch Grasses. It stays in the menu bar instead of opening a permanent main window.
4. Choose an AI Provider, enter your own API key, and test the connection.

Before publication, release packages are built as Universal binaries for Apple silicon and Intel Macs, signed with a Developer ID certificate, and notarized by Apple.

## Read Without Leaving Your Place

Grasses keeps the reading workflow close to the text instead of sending you through another browser tab or application.

| Input | Default shortcut | What it does |
| --- | --- | --- |
| Selected text | `Option + G` | Reads the text selected in another app, then restores the previous clipboard contents. |
| Clipboard | `Option + Shift + G` | Analyzes text or an image you copied explicitly. |
| Screen region | `Option + Control + G` | Captures a region, recognizes its text locally, and presents clickable text blocks. |

Shortcuts can be customized in Settings. On macOS 15 or later, newly recorded shortcuts that use Option must also include Command or Control; the existing defaults remain available.

## Results Adapt to the Text

- **Words and short phrases:** lemma, IPA, common forms, parts of speech, definitions, examples, and on-device system pronunciation.
- **Sentences:** translation and grammar analysis run in parallel, with configurable colors for subjects, predicates, objects, complements, modifiers, and other roles.
- **Paragraphs:** a complete translation first, followed by on-demand analysis of individual sentences with results reused during the current session.
- **Images:** Vision OCR runs on the Mac, preserves recognized line positions and reading order, and lets you select a specific text block for analysis.

## AI Providers

Grasses connects directly from your Mac to the service you configure. Built-in defaults are available for:

- SiliconFlow
- DeepSeek
- Zhipu
- Kimi
- Mimo
- Qwen

You provide the API key and choose the model. Credentials are stored in macOS Keychain, and providers with fixed model support reject unsupported model names instead of silently changing them.

## Permissions

Grasses asks for a system permission only when you use the related workflow:

- **Accessibility:** required for Read Selection. After you trigger the command, Grasses simulates Copy, reads the selected text, and restores the previous clipboard contents.
- **Screen Recording:** required for Read Image. It is used only for the screen region you select; Grasses does not continuously record or scan the screen in the background.
- **Clipboard reading:** requires no additional system permission and only runs after your command.

You can revoke either system permission in System Settings at any time. Other workflows remain available.

## Privacy

- Grasses has no account system and operates no relay server for reading content.
- Screenshots and clipboard images stay on your Mac and are used only for local Vision OCR.
- Only the text you choose to analyze is sent directly to your configured AI service.
- API keys stay in macOS Keychain.
- Grasses creates no reading or image history.
- Diagnostic logs exclude API keys, screenshots, full selected or OCR text, and full AI responses.

Before sending sensitive text, review the privacy terms and account settings of the AI Provider you selected. See the complete [Privacy Policy](https://grasses.brainbeats.pro/privacy.html?lang=en) for data handling, retention, and deletion details.

## System Requirements

- macOS 13 or later
- Apple silicon or Intel Mac
- An API key for a supported AI service to use analysis features

## Support

- Email: [support@grasses.brainbeats.pro](mailto:support@grasses.brainbeats.pro)
- Issues: [GitHub Issues](https://github.com/Brain-Beats/grasses-release/issues)
- Website: [grasses.brainbeats.pro](https://grasses.brainbeats.pro)

When reporting a problem, do not include API keys, private reading content, screenshots containing sensitive information, or full AI responses.
