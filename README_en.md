[简体中文](README.md) | English

# ProcessKeepAlive (进程保活)

An LSPosed / Xposed-based Android background keep-alive module. It hooks into `system_server` to stop selected apps from being killed by the Low Memory Killer (LMK) or "Force stop".

> ⚠️ For personal devices and your own apps only. Keep-alive keeps apps occupying memory and battery — do not use it to track or monitor others' devices.

## Screenshots

| Home | Apps | Settings |
| --- | --- | --- |
| ![Home](home.jpg) | ![Apps](app.jpg) | ![Settings](settings.jpg) |

## Features

- Blocks "Force stop" / background kills and lowers OOM adj (only down, never up — foreground apps are never hurt)
- Aggressive mode, persistent experiment, and boot auto-start (each toggleable)
- Pick targets in the app; changes save instantly and hot-refresh in ~30s without rebooting

## Scope

- **System framework (android)**: required — all hooks are injected into `system_server`
- This module (io.github.guys222.processkeepalive): optional, only for the home screen's live activation-status indicator (keeping it off does not affect keep-alive)

## Usage

1. Rooted with Magisk + LSPosed (Zygisk) installed
2. LSPosed Manager → Modules → enable "进程保活"
3. Tick the "System framework (android)" scope
4. Open the app and tick the apps you want to keep alive

## Download

The APK is hosted on the [Guys222/ProcessKeepAlive Releases](https://github.com/Guys222/ProcessKeepAlive/releases) page. You can also search "进程保活" in the LSPosed Manager module repository.

Source: https://github.com/Guys222/ProcessKeepAlive

## Donation

If this module helped you, feel free to buy the author a coffee ☕

![WeChat QR](wechat.jpg)
