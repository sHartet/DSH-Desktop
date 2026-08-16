# DeepSeek‑Harness Desktop

💻 **DeepSeek‑Harness 本地桌面客户端**

基于 Electron 封装，将 DeepSeek‑Harness 打包为独立 Windows 桌面程序。
无需浏览器，直接以原生软件窗口运行，**内置开源插件 DSH‑Transparent‑UI‑Plugin**，开箱即可使用透明UI效果。

## ✨ 主要特性
- 🖥️ 独立桌面窗口，脱离浏览器环境，普通软件式启动
- 🧩 内置开源插件 **DSH‑Transparent‑UI‑Plugin**，支持透明界面、无边框效果
- 🚫 无需另外安装node.js
- ⚙️ 保留原版全部能力：对话、api管理、插件系统、参数配置
- 📺 窗口支持缩放、最小化，适配透明UI渲染

## 📦 下载发行版
前往 [Releases](https://github.com/sHartet/DSH‑Desktop/releases) 下载：
`DSHarness‑Desktop‑TUP.zip`

> ⚠️ GitHub仓库仅保存源代码，**不包含 exe、dll、运行时与模型文件**。
> 可直接下载 Releases 内的 `DSHarness‑Desktop‑TUP.zip`，解压即可使用。

### 使用步骤（预打包版本）
1. 下载 `DSHarness‑Desktop‑TUP.zip`，完整解压到本地文件夹
2. 运行 `DeepSeekHarness.exe` 启动客户端
3. 在插件面板启用 `DSH‑Transparent‑UI‑Plugin`，开启透明UI主题
4. 配置本地模型路径，加载模型后即可对话

> 模型权重需要自行下载准备，本程序不附带AI模型文件。

## 🚀 源码编译（自行构建）
环境依赖：`Node.js 18+`

```bash
git clone https://github.com/sHartet/DSH‑Desktop.git
cd DSH‑Desktop

npm install
npm run dev     # 开发模式运行
npm run build   # 打包生成 Windows 程序
