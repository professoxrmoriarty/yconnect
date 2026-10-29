Here is the English translation of the `README.md` file you provided:

# Y CONNECT



The native desktop client for [YAKCOOL](https://yakcool.com/): view balances and consumption, manage API Keys, recharge accounts, configure models for local AI programming tools, and launch independent sessions.

## Download



| Platform | Requirements | Installation Package |
| --- | --- | --- |
| macOS | macOS 14+, Apple Silicon / Intel | [Universal DMG](https://www.google.com/search?q=https://aliyun-oss.yaklang.com/yconnect/0.5.4/YConnect-0.5.4-darwin-universal.dmg) |
| Windows | Windows 10/11 x64, .NET Framework 4.8 | [Installer](https://www.google.com/search?q=https://aliyun-oss.yaklang.com/yconnect/0.5.4/YConnect-0.5.4-windows-x64-setup.exe) · [Portable ZIP](https://www.google.com/search?q=https://aliyun-oss.yaklang.com/yconnect/0.5.4/YConnect-0.5.4-windows-x64.zip) |

[GitHub Releases / Release Notes](https://github.com/yaklang/yconnect/releases) · [Latest Version](https://aliyun-oss.yaklang.com/yconnect/version.txt) · [SHA-256 Checksum](https://aliyun-oss.yaklang.com/yconnect/0.5.4/SHA256SUMS.txt)

Officially released macOS applications are signed with a Developer ID and notarized by Apple, and Windows programs and installers are Authenticode signed. For macOS, drag the application into Applications; for Windows, run the installer or extract the portable package. Windows QR code login requires the system WebView2.

## Main Features



* **Account and Key**: Log in to your YAKCOOL account by scanning the WeChat QR code, view balances, consumption, manage Keys, and recharge via QR code; you can also just connect an API Key.


* **Desktop Quick View**: Menu bar / system tray, edge-snapping widgets, light and dark modes.


* **Client Configuration**: Select a Key and compatible models, apply configurations with one click, retain backups, and support restoration.


* **Independent Launch**: Select a working directory and launch the Agent in the terminal; session configurations are saved independently.


* **Connection Diagnostics**: Check the availability of services, Keys, and models; real model invocations and capability tests require confirmation before execution and may incur fees.



Supports OpenCode, Pi, Claude Code, Claude Desktop, Codex, Grok Build, OpenClaw, and Hermes. Independent terminal launch is only applicable to CLI clients; OpenClaw requires a separate gateway to be prepared first. Gemini CLI temporarily requires an additional protocol bridge.

## Data and Credentials



macOS uses Keychain, and Windows uses DPAPI to protect sessions. Downstream clients read Keys through private files or helpers. Configurations are automatically backed up before modification; development mode uses an independent data and client configuration directory.

## Development



macOS uses Swift / AppKit / SwiftUI, and packaging requires Xcode Command Line Tools and ImageMagick:

```sh
swift test --package-path darwin
./script/package-macos.sh --dev

```

Windows uses C# / WPF, and requires the .NET SDK and Inno Setup (when generating the installer):

```powershell
./windows/build.ps1 -Test -Package -Installer

```

[Development and Adaptation Reference](https://www.google.com/search?q=docs/DEVELOPMENT.md) · [Windows Instructions](https://www.google.com/search?q=windows/README.md) · [Versioning, Signing, and Releasing](https://www.google.com/search?q=docs/RELEASING.md) · [Client Updates](https://www.google.com/search?q=docs/UPDATES.md)
