# DeepSeek Harness Desktop - TUP

**DeepSeek Harness 便携式 Electron 桌面客户端** · Portable Electron desktop client for DeepSeek Harness

脱离浏览器，以独立软件窗口运行 DeepSeek Harness，开箱即用、免安装 Node.js、内置 11 个精选插件。
Runs DeepSeek Harness in a standalone desktop window — no browser, no Node.js installation, 11 curated plugins built in.

> 最新版本 **v1.2.0** · 下载见 [Releases](https://github.com/sHartet/DSH-Desktop/releases)

---

## ✨ Features / 特性

- 🪟 **独立软件窗口** — Electron 桌面外壳，不调用浏览器；关闭窗口即停止服务
- 🚫 **免安装运行环境** — 内置 Node.js 运行时（`node-runtime/`），无需在系统安装 Node/npm
- 📦 **便携目录** — 整个应用就是一个文件夹，拷走即用，不写注册表、不动系统环境
- 🔌 **内置 11 个插件** — 插件市场 / 视觉路由 / 技能管理 / 附件 / Markdown 预览等，开箱即用
- 🔒 **纯净无隐私** — 包内不含任何个人数据（API Key、会话、附件、设置），首次启动自动生成
- 🌐 **端口自动选择** — 自动挑选空闲端口，多开或端口冲突不再报错；可用 `--port` 手动指定

## 📦 Included Plugins / 内置插件（11 个）

| 插件 | 说明 |
| --- | --- |
| **Aqua 透明 UI** (`dsh-client-ui-aqua`) | 毛玻璃 / 粒子鲸鱼透明主题 |
| **dshmarket** | 插件市场：应用内在线浏览、安装新插件 |
| **dsh-vision-router** | 视觉能力路由（看图、OCR、图像处理） |
| **dsh-skill-manager-ytxue** | 技能管理器：一键安装 / 管理技能 |
| **dsh-client-auto-continue** | 长任务自动继续 |
| **dsh-plugin-wallpaper-engine** | 动态壁纸引擎 |
| **dsh-usage-chart** | Token 用量统计图表 |
| **dsh-ds-attach** | chat.deepseek.com 同款附件：上传、文件卡片、拖拽，PDF/DOCX/XLSX/TXT 自动提取文本 |
| **dsh-markdown-preview** | 会话内 Markdown / 图片 / 文本文件预览 |
| **dsh-whale-musume** | 鲸鱼娘看板娘吉祥物 |
| **dsh-message-outline** | 消息大纲侧边栏：hover 展开大纲，点击定位消息 |

## ⬇️ Download & Install / 下载与安装

1. 从 [Releases](https://github.com/sHartet/DSH-Desktop/releases) 下载 `DSHarness-Desktop-TUP.zip`
2. **完全解压**到本地文件夹（例如 `D:\DSHarness`）——**不要直接在压缩包内运行 exe**
3. 双击 `DeepSeekHarness.exe` 启动
4. 进入「设置」填写你自己的 **API Key**，开始使用

> 仅支持 **Windows** 系统（x64）。

## 🗂️ Directory Structure / 目录结构

```
DSH-Desktop/
├── DeepSeekHarness.exe          # 桌面外壳（Electron）
├── resources/app/               # 外壳主进程代码（main.js）
├── node-runtime/                # 内置 Node.js 运行时
├── app/
│   ├── dsh/                     # dsh CLI（配置与命令入口）
│   └── node_modules/            # 全部依赖（含预编译原生模块）
└── dsh-home/                    # 用户数据（首次启动自动初始化）
    ├── plugins/                 # 插件
    ├── profiles/web/            # web profile（已挂载全部插件）
    ├── sessions/                # 历史会话
    └── logs/                    # 运行日志（server.log）
```

## ❓ FAQ / 常见问题

**Q: 杀毒软件 / SmartScreen 提示未知发布者？**
A: Electron 打包程序未签名，选择「仍要运行」或在杀软中添加信任即可。

**Q: 启动后没有窗口？**
A: 查看同目录 `logs\server.log` 定位原因；或命令行运行 `DeepSeekHarness.exe --port 8080` 手动指定端口。

**Q: 技能（skills）在哪里？**
A: 包内未内置技能，打开「插件」→「技能管理器」自行安装。

**Q: 想把 API Key 迁移到别的电脑？**
A: 拷贝 `dsh-home\.credentials.yaml` 到新机器的 `dsh-home\` 下即可。

## ⚠️ Disclaimer / 声明

- 本项目是基于 [DeepSeek Harness](https://github.com/deepseek-ai/deepseek-harness) 的桌面封装（MIT License），仅供学习交流
- 请自行申请并妥善保管 API Key；本项目不收集、不存储任何账号信息
- 使用过程中产生的 API 费用由使用者自行承担
