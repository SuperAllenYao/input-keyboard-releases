# IKB 输入法

为 macOS 量身设计的中英双语输入法。中英自由切换、键入流畅，自带拼音学习与英文释义。

## ✨ 主要特性

- **小鹤双拼 / 全拼**双方案可选，菜单栏一键切换
- **南方 / 北方模糊音预设**：覆盖 zh/z、ch/c、sh/s、l/n、f/h、in/ing、en/eng、an/ang 常见混淆
- **左 Shift 短按切换中英文**：模式切换时浮层即时反馈
- **英文释义 + 上下文联想**：候选词附带音标与释义；commit 后基于 ngram 的下一词联想
- **自动成对符号**：输入 `"`、`'`、`{`、`[`、`(`、`` ` ``、`<` 自动成对，光标停中间；中文标点风格下映射 `「」` / `《》` / `｛｝` / `（）` 等中文标点
- **本地学习**：选词频率本机记录，越用越准（数据不上传任何服务器）
- **Liquid Glass 视觉**：候选面板与模式切换浮层适配 macOS 最新视觉风格

## 📦 安装

1. 到 [Releases](../../releases/latest) 下载最新 `IKB-x.y.z.pkg`
2. 双击 `.pkg` 按提示安装（已 Apple Developer ID 签名 + Notarized + Stapled，不会触发 Gatekeeper 警告）
3. **注销重登 macOS**——否则系统找不到刚装的输入法（Apple 官方约束，所有第三方 IM 通用）
4. 系统设置 → 键盘 → 输入法 → 「+」→ 中文（简体）→ 选 `IKB` → 添加
5. 首次切到 IKB 时按提示授权辅助功能（用于接收左 Shift 切换事件）

## 💻 系统要求

- macOS 14 (Sonoma) 或更高
- Apple Silicon Mac（M 系列芯片）

## 🔄 升级

下载新版 `.pkg` 双击安装即可，已有数据自动保留。`.app` 包与用户数据物理分离，升级不会清除：
- 设置：`~/Library/Preferences/com.inputkeyboard.inputmethod.ikb.plist`
- 拼音词库：`~/Library/Application Support/IKB/Rime/`
- 英文学习数据：`~/Library/Application Support/IKB/`
- 诊断日志：`~/Library/Logs/IKB/`

## 🗑️ 卸载

菜单栏 IKB 图标 → 「卸载 IKB 输入法…」→ 输入管理员密码。卸载会清除应用、词典与所有缓存。

## 🐞 反馈

发现问题、有改进建议或想请求新功能？欢迎在 [Issues](../../issues) 提交，附上 macOS 版本与复现步骤；如有诊断日志（菜单栏「导出诊断日志到桌面」），一并附上更佳。

## ⚖️ 许可与致谢

IKB 站在以下开源项目肩上：

- [Rime / librime](https://rime.im/) — 输入法引擎，GPL-3.0
- [Rime Ice](https://github.com/iDvel/rime-ice) — 全拼词库，GPL-3.0
- [雾凇模型](https://github.com/lotem/rime-octagram-data) — 上下文语言模型
- [ECDICT](https://github.com/skywind3000/ECDICT) — 英文词典与释义，MIT
