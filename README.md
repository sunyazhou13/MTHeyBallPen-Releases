# 台球划线工具 · 构建产物

[MTHeyBallPen](https://github.com/sunyazhou13/MTHeyBallPen-Releases/releases) 的官方分发仓库 —— 只放构建产物（`.dmg`）与 Release Note，源码仓库暂未公开。

台球赛事解说用的 macOS 全局屏幕画笔：透明画布直接盖在直播画面上，画线、圈重点、标球路、标母球击点，画笔一关鼠标立刻穿透到底下的窗口。

从 v1.1.0 起还带一块 **iPad 手写板**：iPad 当无线画板，用 Apple Pencil 在上面写，笔迹直接出现在 Mac 的直播窗口上。两端**共用一个绘制栈**（每笔带时间戳、按时间排序），谁先画最后都一致；iPad 断线也能画，重连自动合并。

## 下载

前往 [Releases](https://github.com/sunyazhou13/MTHeyBallPen-Releases/releases/latest) 取最新版：

| 版本 | 安装包 | 说明 |
|:---|:---|:---|
| **v1.1.0** | `MTHeyBallPen-1.1.0.dmg` | 新增 iPad 手写板（两端共用一个绘制栈、离线可用）、编号 1~1000 两种方式；macOS 15.0+ / iPadOS 18+，Universal 2，约 7.1 MB |
| v1.0.0 | `MTHeyBallPen-1.0.0.dmg` | 首个公开构建，11 种工具 + 母球击点浮窗 + 会话预设 + 截图录屏；macOS 15.0+，Universal 2，约 5.4 MB |

## 安装提醒

安装包是 **ad-hoc 签名、未做 Apple 公证**，首次打开会被 Gatekeeper 拦一下：

- 在「系统设置 → 隐私与安全性」点「仍要打开」，或者
- 跑一句 `xattr -cr /Applications/MTHeyBallPen.app`

首次启动还需要授予三项权限：**辅助功能**（全局热键）、**屏幕录制**（截图 / 录屏）、**输入监控**（键盘事件）。

用 iPad 手写板还需要允许**本地网络**权限（Mac 与 iPad 在同一个 Wi‑Fi 下，局域网直连，不经过任何服务器）。

数据只写在本机 `~/Library/Application Support/MTHeyBallPen/`，无账号、无联网、无遥测。
