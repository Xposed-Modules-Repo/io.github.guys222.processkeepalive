简体中文 | [English](README_en.md)

# 进程保活（ProcessKeepAlive）

基于 **LSPosed / Xposed** 的 Android 后台保活模块。在 `system_server` 进程内部拦截杀进程行为，让选定的应用不被低内存杀手（LMK）或「强行停止」杀掉。

> ⚠️ 仅限个人设备、自己安装的应用使用。保活会让应用持续占用内存与电量，请勿用于追踪、监控他人设备。

## 截图

| 主页 | 应用 | 设置 |
| --- | --- | --- |
| ![主页](home.jpg) | ![应用](app.jpg) | ![设置](settings.jpg) |

## 功能

- 阻止「强行停止」/ 后台杀死，压低 OOM adj（仅下调、不上调，不误伤前台）
- 强力模式、常驻实验、开机自启动（可单独开关）
- 应用内勾选保活目标，即时保存、约 30 秒热刷新，无需反复重启

## 作用域

- **系统框架 (android)**：必需，钩子全部注入 `system_server`
- 本模块（io.github.guys222.processkeepalive）：可选，仅用于主页「模块激活状态」实时检测（不勾不影响保活）

## 使用

1. 已刷 Magisk + LSPosed（Zygisk 版）
2. LSPosed Manager → 模块 → 启用「进程保活」
3. 作用域勾选「系统框架（android）」
4. 打开 App 勾选要保活的应用

## 下载

APK 托管在 [Guys222/ProcessKeepAlive 的 Releases](https://github.com/Guys222/ProcessKeepAlive/releases)，也可直接在 LSPosed Manager 的模块仓库搜索「进程保活」安装。

源码：https://github.com/Guys222/ProcessKeepAlive

## 打赏

如果这个模块帮到了你，欢迎请作者喝杯奶茶 ☕

![微信收款码](wechat.jpg)
