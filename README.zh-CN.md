<p align="center">
  <a href="README.md">한국어</a> · <a href="README.en.md">English</a> · <b>简体中文</b> · <a href="README.ja.md">日本語</a> · <a href="README.fr.md">Français</a>
</p>

<p align="center">
  <img src="docs/icon.png" width="128" alt="Audio Mixer">
</p>

<h1 align="center">Audio Mixer</h1>

<p align="center">
  macOS 菜单栏音频混音器 · 应用独立音量 · 均衡器 · AutoEQ<br>
  <a href="https://github.com/jayusop/Audio-Mixer/releases/latest"><b>⬇ 下载最新版</b></a> ·
  <a href="https://jayusop.github.io/Audio-Mixer/?lang=zh">官网</a>
</p>

<p align="center">
  <img alt="macOS 14.2+" src="https://img.shields.io/badge/macOS-14.2%2B-8f7dff">
  <img alt="Apple Silicon / Intel" src="https://img.shields.io/badge/Apple%20Silicon%20%2F%20Intel-supported-ff6fb6">
  <img alt="Release" src="https://img.shields.io/github/v/release/jayusop/Audio-Mixer?color=5fe1f2">
</p>

---

一款常驻菜单栏的 macOS 应用，提供**应用独立音量**、**输入/输出设备音量**、**图形/参数均衡器**以及 **AutoEQ 耳机校正配置**。无需安装虚拟音频驱动。

> 系统要求：macOS 14.2 或更高版本（Apple 芯片 / Intel）<br>
> 🌐 应用语言跟随 macOS 系统语言（英语、韩语、中文、日语），其他语言将显示为英语。

## 安装

1. 从 [Releases](https://github.com/jayusop/Audio-Mixer/releases/latest) 下载 `AudioMixer.zip` 并解压，将 `AudioMixer.app` 移到**应用程序**文件夹。
2. 首次打开时，macOS 会提示无法验证开发者（这是未经 Apple 公证的个人发布应用）。点击**完成**，然后在**系统设置 › 隐私与安全性**下方点击**仍要打开**。也可以在终端中运行：
   ```bash
   xattr -dr com.apple.quarantine /Applications/AudioMixer.app
   ```
3. 菜单栏会出现推子图标。首次处理音频时会请求**“系统录音”**权限 → **允许**。（如果错过了，可在 系统设置 › 隐私与安全性 › 录屏与系统录音 中打开。）

> 如果更新后再次请求权限，请在权限列表中删除旧的 Audio Mixer 条目后重新允许。

## 功能

| 类别 | 功能 |
|---|---|
| 混音器 | 选择输出/输入设备，硬件音量与静音；对没有硬件音量的设备（如 HDMI）使用软件音量 |
| 应用独立音量 | 自动识别正在播放的应用，0–100%（可选 200%），静音，电平表，记住每个应用的设置，排除处理 |
| 均衡器 | 10 段图形 EQ（±12 dB），最多 32 个参数滤波器（PK/LSC/HSC/LP/HP/NO），频响曲线，拖动编辑 |
| AutoEQ | 在线搜索并应用 AutoEQ 数据库（约 8,800 款耳机），导入/导出 ParametricEQ.txt |
| 预设 | 17 种内置预设 + 用户预设（保存/覆盖/删除），**按输出设备自动切换预设** |
| 音质保护 | 自动前级（按最大提升量衰减）、峰值限幅器、硬削波保护、左右声道平衡 |
| 其他 | 登录时启动、处理总开关、韩语 · 英语 · 中文 · 日语界面 |

## 放心使用

- **绝不录音**：音频仅被实时处理，不会被保存或发送到任何地方。
- **退出后声音不受影响**：Audio Mixer 退出（即使是意外退出）时，所有应用的声音会立即恢复原样。
- **自动恢复**：切换输出设备或睡眠/唤醒后会自动重新连接。
- **互不干扰**：直接输出到其他音频设备的应用（例如使用音频接口的 DAW）不会受到影响。

## 说明 / 限制

- 如果拒绝权限，应用独立音量和 EQ 将不可用（声音仍正常播放），只能控制设备音量。
- 应用刚开始播放时，可能会有极短时间听到未经处理的声音。

## 致谢与联系

- EQ 配置数据: [AutoEq](https://github.com/jaakkopasanen/AutoEq) (jaakkopasanen)
- 问题反馈: [Issues](https://github.com/jayusop/Audio-Mixer/issues) · 邮箱 jayusop@gmail.com
