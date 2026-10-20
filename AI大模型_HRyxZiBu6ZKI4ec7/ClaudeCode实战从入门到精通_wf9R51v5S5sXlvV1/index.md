# Claude Code 实战从入门到精通

# Claude Code 核心能力揭秘与环境快速搭建

## <font style="color:rgb(51, 51, 51);">Claude Code 简介</font>

<font style="color:rgb(51, 51, 51);">Claude Code 是 Anthropic 推出的面向开发者的 AI 编程协作工具，与在聊天窗口里写几段代码不同，Claude Code 的核心目标是理解你的整个项目，并参与到真实的编码、修改和重构过程中。</font>

<font style="color:rgb(51, 51, 51);">Claude Code 不是一个代码生成器，而是一个能读项目、懂上下文、遵守约束的 AI 编程搭档。</font>

<font style="color:rgb(51, 51, 51);">简单说:</font>**<font style="color:rgb(51, 51, 51);">Claude Code 是 Claude 的命令行版本,专门为编程场景设计</font>**<font style="color:rgb(51, 51, 51);">。</font>

<font style="color:rgb(51, 51, 51);">它不是网页里的聊天框，而是直接在你的终端(Terminal)里运行,可以:</font>

* **<font style="color:rgb(51, 51, 51);">读取你整个项目的代码</font>**
* **<font style="color:rgb(51, 51, 51);">理解文件之间的关系</font>**
* **<font style="color:rgb(51, 51, 51);">直接修改代码文件</font>**
* **<font style="color:rgb(51, 51, 51);">执行你的指令并给出建议</font>**

![1783580038639-aae4a567-9ff7-42a1-a892-4d17179da8f1.png](./img/wf9R51v5S5sXlvV1/1783580038639-aae4a567-9ff7-42a1-a892-4d17179da8f1-096710.png)

<font style="color:rgb(51, 51, 51);">从能力角度看，Claude Code 主要具备三点特征：</font>

* **<font style="color:rgb(51, 51, 51);">上下文感知</font>**<font style="color:rgb(51, 51, 51);">：不仅理解单个文件，而是理解整个项目结构</font>
* **<font style="color:rgb(51, 51, 51);">工程化导向</font>**<font style="color:rgb(51, 51, 51);">：关注可维护性、规范、测试，而不是一次性代码</font>
* **<font style="color:rgb(51, 51, 51);">可定制行为</font>**<font style="color:rgb(51, 51, 51);">：通过 Skills（技能包）让 AI 遵守你的规则</font>

<font style="color:rgb(51, 51, 51);">打个比方:</font>

* **<font style="color:rgb(51, 51, 51);">Claude(网页版)</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">就像一个顾问，你把代码截图或复制给他，他给你建议，但你得自己动手改。</font>
* **<font style="color:rgb(51, 51, 51);">Claude Code</font>**<font style="color:rgb(51, 51, 51);"> 就像一个坐在你旁边的搭档，他能看到你的整个项目，帮你改代码，甚至帮你写测试、重构函数。</font>

## <font style="color:rgb(51, 51, 51);">Claude Code 的核心能力</font>

### <font style="color:rgb(51, 51, 51);">Claude Code 的核心理念：协作，而不是替代</font>

<font style="color:rgb(51, 51, 51);">Claude Code 并不是在追求把开发者踢出局，它的设计理念非常明确：</font>

* **<font style="color:rgb(51, 51, 51);">人负责：</font>**<font style="color:rgb(51, 51, 51);">目标、约束、判断、审美</font>
* **<font style="color:rgb(51, 51, 51);">AI 负责：</font>**<font style="color:rgb(51, 51, 51);">执行、分析、对比、重复劳动</font>

### <font style="color:rgb(51, 51, 51);">对编程新手: 降低学习门槛</font>

<font style="color:rgb(51, 51, 51);">如果你是新手，最痛苦的可能是:</font>

* <font style="color:rgb(51, 51, 51);">看不懂别人的代码</font>
* <font style="color:rgb(51, 51, 51);">不知道为什么报错</font>
* <font style="color:rgb(51, 51, 51);">不知道好代码长什么样</font>

<font style="color:rgb(51, 51, 51);">Claude Code 可以:</font>

* **<font style="color:rgb(51, 51, 51);">用人话解释代码</font>**<font style="color:rgb(51, 51, 51);">:这段代码的意思是先检查用户是否登录，如果没登录就跳转到登录页</font>
* **<font style="color:rgb(51, 51, 51);">帮你 Debug</font>**<font style="color:rgb(51, 51, 51);">: 这里报错是因为变量名拼错了，应该是</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">username</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">不是</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">usrname</font></code>
* **<font style="color:rgb(51, 51, 51);">教你写更好的代码</font>**<font style="color:rgb(51, 51, 51);">: 这个函数太长了，可以拆成三个小函数，分别负责验证、处理、返回</font>

***

## <font style="color:rgb(51, 51, 51);">对独立开发者: 提升开发效率</font>

<font style="color:rgb(51, 51, 51);">如果你是独立开发者，你可能:</font>

* <font style="color:rgb(51, 51, 51);">一个人负责前后端</font>
* <font style="color:rgb(51, 51, 51);">没人帮你 Code Review</font>
* <font style="color:rgb(51, 51, 51);">需要快速试错和迭代</font>

<font style="color:rgb(51, 51, 51);">Claude Code 可以:</font>

* **<font style="color:rgb(51, 51, 51);">帮你快速理解第三方库的用法</font>**
* **<font style="color:rgb(51, 51, 51);">自动生成测试用例</font>**
* **<font style="color:rgb(51, 51, 51);">帮你重构混乱的代码</font>**

***

## <font style="color:rgb(51, 51, 51);">对团队: 统一规范,降低协作成本</font>

<font style="color:rgb(51, 51, 51);">如果你在团队工作，你可能遇到:</font>

* <font style="color:rgb(51, 51, 51);">每个人代码风格不一样</font>
* <font style="color:rgb(51, 51, 51);">新人上手慢,老是问重复问题</font>
* <font style="color:rgb(51, 51, 51);">Code Review 花时间</font>

<font style="color:rgb(51, 51, 51);">Claude Code 可以:</font>

* **<font style="color:rgb(51, 51, 51);">通过 Skills 统一团队规范</font>**<font style="color:rgb(51, 51, 51);">(所有人用同一套规则)</font>
* **<font style="color:rgb(51, 51, 51);">帮新人快速理解项目</font>**
* **<font style="color:rgb(51, 51, 51);">在提交前自动检查代码质量</font>**

## <font style="color:rgb(51, 51, 51);">Claude Code 安装与使用</font>

<font style="color:rgb(51, 51, 51);">在正式安装之前，先了解一下 Claude Code 有哪几种使用方式，选择最适合自己的方式入手。</font>

| <font style="color:rgb(255, 255, 255);">方式</font> | <font style="color:rgb(255, 255, 255);">适合人群</font> | <font style="color:rgb(255, 255, 255);">优点</font> | <font style="color:rgb(255, 255, 255);">缺点</font> |
| --- | --- | --- | --- |
| **<font style="color:rgb(51, 51, 51);">Web 端</font>** | <font style="color:rgb(51, 51, 51);">完全新手</font> | <font style="color:rgb(51, 51, 51);">无需安装，打开浏览器即可使用</font> | <font style="color:rgb(51, 51, 51);">功能相对有限，无法深度集成本地代码</font> |
| **<font style="color:rgb(51, 51, 51);">CLI（命令行）</font>** | <font style="color:rgb(51, 51, 51);">有一定基础的开发者</font> | <font style="color:rgb(51, 51, 51);">功能完整，集成度高，最接近设计初衷</font> | <font style="color:rgb(51, 51, 51);">需要熟悉命令行操作</font> |
| **<font style="color:rgb(51, 51, 51);">编辑器集成（VS Code / Cursor 等）</font>** | <font style="color:rgb(51, 51, 51);">日常开发者</font> | <font style="color:rgb(51, 51, 51);">无缝融入已有工作流，不需要切换窗口</font> | <font style="color:rgb(51, 51, 51);">依赖插件和环境配置</font> |

**<font style="color:rgb(51, 51, 51);">选择建议：</font>**

* <font style="color:rgb(51, 51, 51);">如果你是</font>**<font style="color:rgb(51, 51, 51);">完全新手</font>**<font style="color:rgb(51, 51, 51);">，先访问</font><font style="color:rgb(51, 51, 51);"> </font>[<font style="color:rgb(0, 102, 0);">https://claude.ai/</font>](https://claude.ai/)<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">用 Web 端试试手感，熟悉 Claude 的对话方式</font>
* <font style="color:rgb(51, 51, 51);">如果你想</font>**<font style="color:rgb(51, 51, 51);">真正用于开发</font>**<font style="color:rgb(51, 51, 51);">，直接学习</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:rgb(51, 51, 51);">CLI（命令行）</font>**<font style="color:rgb(51, 51, 51);">，功能最完整</font>
* <font style="color:rgb(51, 51, 51);">等 CLI 用熟之后，再根据需要考虑</font>**<font style="color:rgb(51, 51, 51);">编辑器集成</font>**

<font style="color:rgb(51, 51, 51);">目前 Claude Code 也提供了桌面版，可在以下地址下载：</font>[<font style="color:rgb(0, 102, 0);">https://claude.com/download</font>](https://claude.com/download)

## <font style="color:rgb(51, 51, 51);">安装 Claude Code CLI</font>

### <font style="color:rgb(51, 51, 51);">1、前置准备</font>

<font style="color:rgb(51, 51, 51);">在安装之前，你需要准备好以下两项：</font>

**<font style="color:rgb(51, 51, 51);">① Claude 账号</font>**

* <font style="color:rgb(51, 51, 51);">访问</font><font style="color:rgb(51, 51, 51);"> </font>[<font style="color:rgb(0, 102, 0);">claude.ai</font>](https://claude.ai/)<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">注册一个账号</font>
* <font style="color:rgb(51, 51, 51);">如果你已经在使用 Claude 网页版聊天，说明账号已经有了，可以跳过这步</font>
* <font style="color:rgb(51, 51, 51);">如果你打算使用国内大模型（如 DeepSeek、Minimax、GLM 等），可以暂时跳过账号注册，后文会介绍如何切换</font>

**<font style="color:rgb(51, 51, 51);">② 命令行工具</font>**

* **<font style="color:rgb(51, 51, 51);">Mac / Linux：</font>**<font style="color:rgb(51, 51, 51);">打开系统自带的 Terminal（终端）即可</font>
* **<font style="color:rgb(51, 51, 51);">Windows：</font>**<font style="color:rgb(51, 51, 51);">打开 PowerShell，或者安装并使用 WSL（Windows Subsystem for Linux）</font>

### <font style="color:rgb(51, 51, 51);">2、使用官方脚本安装（推荐）</font>

<font style="color:rgb(51, 51, 51);">官方提供了一键安装脚本，根据你的系统选择对应的命令执行：</font>

**<font style="color:rgb(51, 51, 51);">macOS、Linux、WSL：</font>**

curl -fsSL https://claude.ai/install.sh | bash

**<font style="color:rgb(51, 51, 51);">Windows PowerShell：</font>**

irm https://claude.ai/install.ps1 | iex

**<font style="color:rgb(51, 51, 51);">Windows CMD：</font>**

curl -fsSL https://claude.ai/install.cmd -o install.cmd && install.cmd && del install.cmd

**<font style="color:rgb(51, 51, 51);">Homebrew:</font>**

brew install --cask claude-code

**<font style="color:rgb(51, 51, 51);">WinGet:</font>**

winget install Anthropic.ClaudeCode

**<font style="color:rgb(51, 51, 51);">安装完成后，验证是否安装成功：</font>**

claude --version

<font style="color:rgb(51, 51, 51);">如果终端输出了版本号（如</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">1.x.x</font></code><font style="color:rgb(51, 51, 51);">），说明安装成功:</font>

2.1.81 (Claude Code)

### <font style="color:rgb(51, 51, 51);">3、使用 npm 安装（不推荐）</font>

<font style="color:rgb(51, 51, 51);">官方目前已不再推荐使用 npm 安装方式，建议优先使用上方的官方脚本。如果确实需要通过 npm 安装，请先确认已安装 Node.js：</font>

node --version

<font style="color:rgb(51, 51, 51);">如果输出了版本号（如</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">v18.17.0</font></code><font style="color:rgb(51, 51, 51);">），说明已安装。如果提示命令不存在，请前往</font><font style="color:rgb(51, 51, 51);"> </font>[<font style="color:rgb(0, 102, 0);">nodejs.org</font>](https://nodejs.org/)<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">下载并安装。</font>

<font style="color:rgb(51, 51, 51);">确认 Node.js 可用后，执行以下命令安装 Claude Code：</font>

npm install -g @anthropic-ai/claude-code

<font style="color:rgb(51, 51, 51);">等待安装完成（可能需要几分钟），然后验证：</font>

claude --version

### <font style="color:rgb(51, 51, 51);">4、更新 Claude Code</font>

<font style="color:rgb(51, 51, 51);">可以直接用以下命令更新：</font>

claude install

<font style="color:rgb(51, 51, 51);">或者：</font>

claude update

<font style="color:rgb(51, 51, 51);">Claude Code 在启动和运行时会</font>**<font style="color:rgb(51, 51, 51);">自动检查更新</font>**<font style="color:rgb(51, 51, 51);">，后台下载完成后，下次启动即生效。自动更新相关配置写在 </font><code><font style="color:rgb(51, 51, 51);">settings.json</font></code><font style="color:rgb(51, 51, 51);"> 中：</font>

### <font style="color:rgb(51, 51, 51);">5、常见安装问题排查</font>

**<font style="color:rgb(51, 51, 51);">问题一：提示</font>\*\*\*\*<font style="color:rgb(51, 51, 51);"> </font>**<code>**<font style="color:rgb(51, 51, 51);">npm command not found</font>**</code>

* **<font style="color:rgb(51, 51, 51);">原因：</font>**<font style="color:rgb(51, 51, 51);">电脑上没有安装 Node.js</font>
* **<font style="color:rgb(51, 51, 51);">解决：</font>**<font style="color:rgb(51, 51, 51);">前往</font><font style="color:rgb(51, 51, 51);"> </font>[<font style="color:rgb(0, 102, 0);">nodejs.org</font>](https://nodejs.org/)<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">下载安装 Node.js，安装完成后重新执行安装命令</font>

**<font style="color:rgb(51, 51, 51);">问题二：提示</font>\*\*\*\*<font style="color:rgb(51, 51, 51);"> </font>**<code>**<font style="color:rgb(51, 51, 51);">permission denied</font>**</code>

* **<font style="color:rgb(51, 51, 51);">原因：</font>**<font style="color:rgb(51, 51, 51);">当前用户没有全局安装权限</font>
* **<font style="color:rgb(51, 51, 51);">解决（Mac / Linux）：</font>**<font style="color:rgb(51, 51, 51);">在命令前加</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">sudo</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">提升权限：</font><font style="color:rgb(51, 51, 51);">sudo npm install -g @anthropic-ai/claude-code</font>
* **<font style="color:rgb(51, 51, 51);">解决（Windows）：</font>**<font style="color:rgb(51, 51, 51);">右键 PowerShell，选择"以管理员身份运行"，然后重新执行安装命令</font>

**<font style="color:rgb(51, 51, 51);">问题三：安装速度很慢或卡住</font>**

* **<font style="color:rgb(51, 51, 51);">原因：</font>**<font style="color:rgb(51, 51, 51);">网络访问境外源速度慢</font>
* **<font style="color:rgb(51, 51, 51);">解决：</font>**<font style="color:rgb(51, 51, 51);">添加</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">--registry</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">参数切换到国内镜像源：</font><font style="color:rgb(51, 51, 51);">npm install -g @anthropic-ai/claude-code --registry=https://registry.npmmirror.com</font>

**<font style="color:rgb(51, 51, 51);">终端推荐：</font>**<font style="color:rgb(51, 51, 51);">如果你觉得系统默认终端体验一般，以下这些终端在使用 Claude Code 时体验更佳：</font>

* <font style="color:rgb(51, 51, 51);">WezTerm（跨平台）：</font>[<font style="color:rgb(0, 102, 0);">https://wezterm.org/</font>](https://wezterm.org/)
* <font style="color:rgb(51, 51, 51);">Alacritty（跨平台）：</font>[<font style="color:rgb(0, 102, 0);">https://alacritty.org/</font>](https://alacritty.org/)
* <font style="color:rgb(51, 51, 51);">Ghostty（Linux / macOS）：</font>[<font style="color:rgb(0, 102, 0);">https://ghostty.org/</font>](https://ghostty.org/)
* <font style="color:rgb(51, 51, 51);">Kitty（Linux / macOS）：</font>[<font style="color:rgb(0, 102, 0);">https://github.com/kovidgoyal/kitty</font>](https://github.com/kovidgoyal/kitty)

***

## <font style="color:rgb(51, 51, 51);">Claude Code 切换国产大模型</font>

通过开源工具 cc-switch 切换国产大模型，可以让原本仅支持 <font style="color:rgb(51, 51, 51);">Claude Code</font> 的 IDE 插件、Claude Cli、Claude App直接调用国内大模型（如 DeepSeek、Kimi、通义千问、智谱 AI 等）。

cc-switch 的核心原理是在本地建立代理服务器，拦截发往官方的请求，并自动将 Codex 协议转换为国内大模型通用的 **Chat Completions 协议**，同时保留流式输出（SSE）和思考过程（Reasoning）。

![1781325452683-5e45c6cd-a7c0-422d-880c-1f01b009ebf4.webp](./img/wf9R51v5S5sXlvV1/1781325452683-5e45c6cd-a7c0-422d-880c-1f01b009ebf4-737976.webp)

### <font style="color:rgb(51, 51, 51);">第一步：下载与安装工具</font>

1. 访问 cc-switch 的官方开源仓库：[GitHub - farion1231/cc-switch](https://github.com/farion1231/cc-switch)。
2. 在 **Releases** 页面下载适合你操作系统的安装包（Windows 下载 `.exe`，Mac 下载 `.dmg`）。

下载地址：<https://github.com/farion1231/cc-switch/releases/tag/v3.16.2>

3. 安装并打开软件，确保软件处于运行状态。

![1781325516367-1f4e6148-6c9a-4c65-887c-4059cfd1d387.png](./img/wf9R51v5S5sXlvV1/1781325516367-1f4e6148-6c9a-4c65-887c-4059cfd1d387-343315.png)

### <font style="color:rgb(51, 51, 51);">第二步：获取国产大模型 API 凭证</font>

你需要准备好国产大模型的 API Key。以下为常用厂商的开放平台：

* **DeepSeek**：登录 DeepSeek 开放平台申请 Key，地址：<https://platform.deepseek.com/api_keys>
* **Kimi**：登录 Kimi 开放平台申请Key ，地址：<https://platform.kimi.com/console/api-keys>
* **通义千问**：登录 阿里云百炼平台 获取 Key（标准地址：`https://aliyuncs.com`）。
* **智谱清言**：登录 智谱大模型开放平台 获取 Key。

*注意：请确保大模型账户内有余额，否则在后续调用中会触发 *<code>_402_</code>* 欠费错误。*

***

### <font style="color:rgb(51, 51, 51);">第三步：在 cc-switch 中配置供应商</font>

1. 打开 cc-switch 客户端，在顶部导航栏中**点击切换到带有 Claude Code 图标的模块页面**。

![1783817604163-b8293a87-02d9-4134-971a-183993db76d3.png](./img/wf9R51v5S5sXlvV1/1783817604163-b8293a87-02d9-4134-971a-183993db76d3-069432.png)

2. 点击界面右上角的 **「+」号（添加供应商 / Add Provider）**。

![1783817629247-25a21b2e-30e1-4b6e-b2fd-4b61bc201193.png](./img/wf9R51v5S5sXlvV1/1783817629247-25a21b2e-30e1-4b6e-b2fd-4b61bc201193-081183.png)

3. **选择并填写参数**：
   * **使用内置预设**：在列表中直接选择 `DeepSeek`、`Qwen (阿里云)` 等。此时软件会自动填入标准的 **Base URL**，你只需在 `API Key` 框中**粘贴你刚才复制的密钥**。
   * **使用自定义/第三方中转**：如果列表里没有你要的模型，或者你使用的是第三方中转 API，请选择 <code>**Custom**</code>\*\* (自定义 OpenAI 兼容)\*\*。手动填入中转商提供的 `Base URL`、`API Key` 以及特定的 `Model Name`（模型名称）。

![1781428845156-a7a37d0f-3386-4e46-8ab9-f83349607f55.png](./img/wf9R51v5S5sXlvV1/1781428845156-a7a37d0f-3386-4e46-8ab9-f83349607f55-848308.png)

4. 点击右下角的 **「添加」** 按钮保存。

![1781542394363-5286c72b-fcb8-484d-b549-1999f2f478e7.png](./img/wf9R51v5S5sXlvV1/1781542394363-5286c72b-fcb8-484d-b549-1999f2f478e7-189996.png)

### <font style="color:rgb(51, 51, 51);">第四步：开启路由</font>

切换到 DeepSeek，系统会提示我们开启路由，我们可以点击左上角的设置按钮进入设置页面开启：

![1783817575080-37b384f7-b2a1-41fa-abe2-6b83b1366b2b.png](./img/wf9R51v5S5sXlvV1/1783817575080-37b384f7-b2a1-41fa-abe2-6b83b1366b2b-756467.png)

<font style="color:rgb(51, 51, 51);">点击击路由设置菜单，开启路由：</font>

![1781428969016-5ab0816e-307a-41ba-b9e7-386d94db5e6e.png](./img/wf9R51v5S5sXlvV1/1781428969016-5ab0816e-307a-41ba-b9e7-386d94db5e6e-407275.png)

<font style="color:rgb(51, 51, 51);">然后选择 Claude：</font>

![1781542473410-dd341765-f8a8-4150-b963-0512ce5fc96e.png](./img/wf9R51v5S5sXlvV1/1781542473410-dd341765-f8a8-4150-b963-0512ce5fc96e-983146.png)

<font style="color:rgb(51, 51, 51);">接下来你重新打开 Claude CLI，就可以看到 DeepSeek 的模型标志了：</font>

![1783817685675-161b96bb-7b71-4815-9719-578e0c68a432.png](./img/wf9R51v5S5sXlvV1/1783817685675-161b96bb-7b71-4815-9719-578e0c68a432-334664.png)

***

###

## <font style="color:rgb(51, 51, 51);">卸载 Claude Code</font>

<font style="color:rgb(51, 51, 51);">根据你当初的安装方式选择对应的卸载命令。</font>

### <font style="color:rgb(51, 51, 51);">1、官方脚本安装（原生安装）</font>

<font style="color:rgb(51, 51, 51);">删除 Claude Code 的可执行文件和版本文件：</font>

**<font style="color:rgb(51, 51, 51);">macOS、Linux、WSL：</font>**

```plain
rm -f ~/.local/bin/claude
rm -rf ~/.local/share/claude
```

**<font style="color:rgb(51, 51, 51);">Windows PowerShell：</font>**

```plain
Remove-Item -Path "$env:USERPROFILE\.local\bin\claude.exe" -Force
Remove-Item -Path "$env:USERPROFILE\.local\share\claude" -Recurse -Force
```

### <font style="color:rgb(51, 51, 51);">2、Homebrew 安装</font>

brew uninstall --cask claude-code

### <font style="color:rgb(51, 51, 51);">3、WinGet 安装</font>

winget uninstall Anthropic.ClaudeCode

### <font style="color:rgb(51, 51, 51);">4、npm 安装</font>

npm uninstall -g @anthropic-ai/claude-code

### <font style="color:rgb(51, 51, 51);">5、删除配置文件（可选）</font>

<font style="color:rgb(51, 51, 51);">以上命令只卸载了可执行程序，配置文件和历史记录不会自动删除。如果你希望完全清除所有数据（包括设置、授权工具、MCP 服务器配置和会话历史），需要额外执行以下命令：</font>

*<font style="color:rgb(44, 58, 94);">⚠️</font>**<font style="color:rgb(44, 58, 94);"> 删除配置文件是</font>**__<font style="color:rgb(44, 58, 94);">不可恢复</font>__\_\_<font style="color:rgb(44, 58, 94);">的操作，所有本地设置和历史记录将永久丢失，执行前请确认。</font>*

**<font style="color:rgb(51, 51, 51);">macOS、Linux、WSL：</font>**

```plain
# 删除全局用户设置和状态
rm -rf ~/.claude
rm ~/.claude.json

# 删除当前项目的本地设置（在项目目录中执行）
rm -rf .claude
rm -f .mcp.json
```

**<font style="color:rgb(51, 51, 51);">Windows PowerShell：</font>**

```plain
# 删除全局用户设置和状态
Remove-Item -Path "$env:USERPROFILE\.claude" -Recurse -Force
Remove-Item -Path "$env:USERPROFILE\.claude.json" -Force

# 删除当前项目的本地设置（在项目目录中执行）
Remove-Item -Path ".claude" -Recurse -Force
Remove-Item -Path ".mcp.json" -Force
```

***

## <font style="color:rgb(51, 51, 51);">登录 Claude Code</font>

### <font style="color:rgb(51, 51, 51);">1、首次登录流程</font>

<font style="color:rgb(51, 51, 51);">在项目目录中启动 Claude Code：</font>

claude

<font style="color:rgb(51, 51, 51);">首次启动时，Claude Code 会引导你完成登录。你也可以在进入界面后手动输入登录命令：</font>

/login

<font style="color:rgb(51, 51, 51);">按照终端中的提示完成登录授权即可。登录后，凭据会保存在本地，</font>**<font style="color:rgb(51, 51, 51);">下次启动无需重复登录</font>**<font style="color:rgb(51, 51, 51);">。如果需要切换账号，重新执行</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">/login</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">即可。</font>

### <font style="color:rgb(51, 51, 51);">2、支持的账号类型</font>

<font style="color:rgb(51, 51, 51);">你可以使用以下任意一种账号类型登录：</font>

#### <font style="color:rgb(51, 51, 51);">① Claude 订阅账号（推荐）</font>

* **<font style="color:rgb(51, 51, 51);">Claude Pro</font>**<font style="color:rgb(51, 51, 51);">：个人专业版</font>
* **<font style="color:rgb(51, 51, 51);">Claude Max</font>**<font style="color:rgb(51, 51, 51);">：最高级别订阅</font>
* **<font style="color:rgb(51, 51, 51);">Claude Teams</font>**<font style="color:rgb(51, 51, 51);">：团队版</font>
* **<font style="color:rgb(51, 51, 51);">Claude Enterprise</font>**<font style="color:rgb(51, 51, 51);">：企业版</font>

#### <font style="color:rgb(51, 51, 51);">② Claude Console 账号（API 访问）</font>

* <font style="color:rgb(51, 51, 51);">通过 API 访问，使用预付费积分计费</font>
* <font style="color:rgb(51, 51, 51);">适合开发者和需要程序化访问的场景</font>
* <font style="color:rgb(51, 51, 51);">同一个邮箱可以同时拥有订阅账号和 Console 账号两种类型</font>

### <font style="color:rgb(51, 51, 51);">3、自动创建工作区（Console 账号）</font>

<font style="color:rgb(51, 51, 51);">首次使用 Claude Console 账号认证 Claude Code 时，系统会自动在你的 Console 中创建一个名为</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:rgb(51, 51, 51);">"Claude Code"</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">的工作区，用于：</font>

* <font style="color:rgb(51, 51, 51);">集中跟踪所有 Claude Code 的 API 使用成本</font>
* <font style="color:rgb(51, 51, 51);">便于管理组织内多人的 Claude Code 使用情况</font>

***

## <font style="color:rgb(51, 51, 51);">启动第一次会话</font>

### <font style="color:rgb(51, 51, 51);">1、在项目目录中启动</font>

<font style="color:rgb(51, 51, 51);">打开终端，先切换到你的项目目录，再启动 Claude Code。这样 Claude 才能读取你的项目文件，提供针对性的帮助：</font>

```plain
cd /path/to/your/project
claude
```

### <font style="color:rgb(51, 51, 51);">2、欢迎界面</font>

<font style="color:rgb(51, 51, 51);">启动后，你会看到 Claude Code 的欢迎界面，包括当前会话信息、最近的对话记录和最新更新说明：</font>

![1783580273398-c6d7563c-b360-4ccd-997a-2a64f576de0b.png](./img/wf9R51v5S5sXlvV1/1783580273398-c6d7563c-b360-4ccd-997a-2a64f576de0b-859096.png)

### <font style="color:rgb(51, 51, 51);">3、查看可用命令</font>

<font style="color:rgb(51, 51, 51);">在输入框中输入</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">/help</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">可以查看所有可用功能：</font>

/help

<font style="color:rgb(51, 51, 51);">输入</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">/resume</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">可以恢复之前中断的对话：</font>

/resume

<font style="color:rgb(51, 51, 51);">在输入框中直接输入</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">/</font></code><font style="color:rgb(51, 51, 51);">，会弹出所有可用命令的补全列表：</font>

![1783580273293-532521ec-9359-4fff-9128-6d3b5160d812.png](./img/wf9R51v5S5sXlvV1/1783580273293-532521ec-9359-4fff-9128-6d3b5160d812-284047.png)

<font style="color:rgb(51, 51, 51);">详细的凭据管理信息可参考官方文档的</font><font style="color:rgb(51, 51, 51);"> </font>[<font style="color:rgb(0, 102, 0);">Credential Management</font>](https://code.claude.com/docs/en/iam#credential-management)<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">部分。</font>

***

## <font style="color:rgb(51, 51, 51);">提出第一个问题</font>

### <font style="color:rgb(51, 51, 51);">1、理解项目</font>

<font style="color:rgb(51, 51, 51);">进入项目目录启动 Claude Code 后，可以先让它分析你的代码库：</font>

what does this project do?

<font style="color:rgb(51, 51, 51);">Claude 会自动读取项目文件，并给出项目概要。</font>

***<font style="color:rgb(44, 58, 94);">Claude Code 会根据需要自动读取文件</font>**\_\_<font style="color:rgb(44, 58, 94);">——你不需要手动把文件内容复制粘贴到对话中，它会自己找到需要的上下文。</font>*

### <font style="color:rgb(51, 51, 51);">2、更多项目相关问题</font>

<font style="color:rgb(51, 51, 51);">你还可以询问更具体的信息：</font>

what technologies does this project use?where is the main entry point?explain the folder structure

### <font style="color:rgb(51, 51, 51);">3、询问 Claude Code 的能力</font>

<font style="color:rgb(51, 51, 51);">也可以直接问 Claude 关于它自己能做什么：</font>

what can Claude Code do?how do I use slash commands in Claude Code?can Claude Code work with Docker?

<font style="color:rgb(51, 51, 51);">Claude 可以访问自己的文档，能够准确回答关于自身功能和特性的问题。</font>

***

## <font style="color:rgb(51, 51, 51);">进行第一次代码修改</font>

### <font style="color:rgb(51, 51, 51);">1、动手试一个简单任务</font>

<font style="color:rgb(51, 51, 51);">下面让 Claude Code 实际编写代码。我们创建一个测试目录，让它在</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">test.py</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">文件中添加一个 Hello World 函数：</font>

```plain
cd runoob-test    # 进入测试目录（没有则新建一个）
claude            # 启动 Claude Code
```

<font style="color:rgb(51, 51, 51);">进入界面后，输入：</font>

在 test.py 文件中添加 hello world 函数

<font style="color:rgb(51, 51, 51);">Claude Code 会展示建议的代码修改，并在执行前请求你的确认，选择</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:rgb(51, 51, 51);">yes</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">后按回车即可应用：</font>

![1783580273576-12cdc861-7234-4d53-b55f-e59862c845f2.png](./img/wf9R51v5S5sXlvV1/1783580273576-12cdc861-7234-4d53-b55f-e59862c845f2-394338.png)

### <font style="color:rgb(51, 51, 51);">2、Claude Code 的修改工作流</font>

<font style="color:rgb(51, 51, 51);">每次代码修改，Claude Code 都会按以下流程执行：</font>

1. **<font style="color:rgb(51, 51, 51);">找到相关文件</font>**<font style="color:rgb(51, 51, 51);">：自动在项目中定位需要修改的文件</font>
2. **<font style="color:rgb(51, 51, 51);">展示建议的修改</font>**<font style="color:rgb(51, 51, 51);">：以差异对比的形式展示将要做的改动</font>
3. **<font style="color:rgb(51, 51, 51);">请求你的批准</font>**<font style="color:rgb(51, 51, 51);">：执行前必须经过你的确认</font>
4. **<font style="color:rgb(51, 51, 51);">执行编辑</font>**<font style="color:rgb(51, 51, 51);">：确认后写入文件</font>

<font style="color:rgb(51, 51, 51);">你可以逐个审批每处修改，也可以在当前会话中开启"全部接受"模式批量确认。</font>

***

## <font style="color:rgb(51, 51, 51);">使用 Git 功能</font>

<font style="color:rgb(51, 51, 51);">Claude Code 让 Git 操作变得像日常对话一样简单，直接用自然语言描述你想做的事即可。</font>

### <font style="color:rgb(51, 51, 51);">1、基础 Git 操作</font>

**<font style="color:rgb(51, 51, 51);">查看已修改的文件：</font>**

what files have I changed?

**<font style="color:rgb(51, 51, 51);">提交更改（Claude 会自动生成提交信息）：</font>**

commit my changes with a descriptive message

### <font style="color:rgb(51, 51, 51);">2、更复杂的 Git 操作</font>

**<font style="color:rgb(51, 51, 51);">创建新分支：</font>**

create a new branch called feature/quickstart

**<font style="color:rgb(51, 51, 51);">查看最近的提交历史：</font>**

show me the last 5 commits

**<font style="color:rgb(51, 51, 51);">协助解决合并冲突：</font>**

help me resolve merge conflicts

***

## <font style="color:rgb(51, 51, 51);">修复 Bug 或添加功能</font>

### <font style="color:rgb(51, 51, 51);">1、添加新功能</font>

<font style="color:rgb(51, 51, 51);">用自然语言描述你想要添加的功能，Claude Code 会找到合适的位置并实现它：</font>

add input validation to the user registration form

### <font style="color:rgb(51, 51, 51);">2、修复现有问题</font>

<font style="color:rgb(51, 51, 51);">描述 Bug 现象，让 Claude 定位并修复：</font>

there's a bug where users can submit empty forms - fix it

### <font style="color:rgb(51, 51, 51);">3、Claude Code 的问题处理流程</font>

1. **<font style="color:rgb(51, 51, 51);">定位相关代码</font>**<font style="color:rgb(51, 51, 51);">：在代码库中找到与问题相关的文件和函数</font>
2. **<font style="color:rgb(51, 51, 51);">理解上下文</font>**<font style="color:rgb(51, 51, 51);">：分析代码逻辑，理解问题的根本原因</font>
3. **<font style="color:rgb(51, 51, 51);">实现解决方案</font>**<font style="color:rgb(51, 51, 51);">：给出修改建议并展示 diff</font>
4. **<font style="color:rgb(51, 51, 51);">运行测试</font>**<font style="color:rgb(51, 51, 51);">：如果项目中存在测试，Claude 会尝试运行以验证修复效果</font>

***

## <font style="color:rgb(51, 51, 51);">其他常见工作流</font>

### <font style="color:rgb(51, 51, 51);">代码重构</font>

refactor the authentication module to use async/await instead of callbacks

### <font style="color:rgb(51, 51, 51);">编写测试</font>

write unit tests for the calculator functions

### <font style="color:rgb(51, 51, 51);">更新文档</font>

update the README with installation instructions

### <font style="color:rgb(51, 51, 51);">代码审查</font>

review my changes and suggest improvements

***<font style="color:rgb(44, 58, 94);">Claude Code 是你的 AI 结对编程伙伴。</font>**\_\_<font style="color:rgb(44, 58, 94);">像跟一个有经验的同事交流一样跟它对话——描述你想实现什么，不用拘泥于特定命令格式，用自然语言表达即可，它会帮你找到最佳实现方式。</font>*

***

## <font style="color:rgb(51, 51, 51);">常用命令速查表</font>

### <font style="color:rgb(51, 51, 51);">命令行命令（在终端中使用）</font>

| <font style="color:rgb(255, 255, 255);">命令</font> | <font style="color:rgb(255, 255, 255);">功能</font> | <font style="color:rgb(255, 255, 255);">示例</font> |
| --- | --- | --- |
| <code><font style="color:rgb(51, 51, 51);">claude</font></code> | <font style="color:rgb(51, 51, 51);">启动交互模式（最常用）</font> | <code><font style="color:rgb(51, 51, 51);">claude</font></code> |
| <code><font style="color:rgb(51, 51, 51);">claude "任务描述"</font></code> | <font style="color:rgb(51, 51, 51);">执行一次性任务后退出交互模式</font> | <code><font style="color:rgb(51, 51, 51);">claude "fix the build error"</font></code> |
| <code><font style="color:rgb(51, 51, 51);">claude -p "查询内容"</font></code> | <font style="color:rgb(51, 51, 51);">执行单次查询后立即退出（适合脚本集成）</font> | <code><font style="color:rgb(51, 51, 51);">claude -p "explain this function"</font></code> |
| <code><font style="color:rgb(51, 51, 51);">claude -c</font></code> | <font style="color:rgb(51, 51, 51);">继续当前目录的最近一次对话</font> | <code><font style="color:rgb(51, 51, 51);">claude -c</font></code> |
| <code><font style="color:rgb(51, 51, 51);">claude -r</font></code> | <font style="color:rgb(51, 51, 51);">从历史中选择并恢复一次对话</font> | <code><font style="color:rgb(51, 51, 51);">claude -r</font></code> |
| <code><font style="color:rgb(51, 51, 51);">claude commit</font></code> | <font style="color:rgb(51, 51, 51);">让 Claude 自动生成 Git 提交信息并提交</font> | <code><font style="color:rgb(51, 51, 51);">claude commit</font></code> |
| <code><font style="color:rgb(51, 51, 51);">claude update</font></code> | <font style="color:rgb(51, 51, 51);">手动更新 Claude Code 到最新版本</font> | <code><font style="color:rgb(51, 51, 51);">claude update</font></code> |
| <code><font style="color:rgb(51, 51, 51);">claude --version</font></code> | <font style="color:rgb(51, 51, 51);">查看当前安装的版本号</font> | <code><font style="color:rgb(51, 51, 51);">claude --version</font></code> |

### <font style="color:rgb(51, 51, 51);">交互模式内命令（在 Claude Code 界面中使用）</font>

| <font style="color:rgb(255, 255, 255);">命令</font> | <font style="color:rgb(255, 255, 255);">功能</font> | <font style="color:rgb(255, 255, 255);">示例</font> |
| --- | --- | --- |
| <code><font style="color:rgb(51, 51, 51);">/help</font></code> | <font style="color:rgb(51, 51, 51);">显示所有可用命令和功能说明</font> | <code><font style="color:rgb(51, 51, 51);">/help</font></code> |
| <code><font style="color:rgb(51, 51, 51);">/login</font></code> | <font style="color:rgb(51, 51, 51);">登录账号或切换到其他账号</font> | <code><font style="color:rgb(51, 51, 51);">/login</font></code> |
| <code><font style="color:rgb(51, 51, 51);">/resume</font></code> | <font style="color:rgb(51, 51, 51);">从历史中恢复之前中断的对话</font> | <code><font style="color:rgb(51, 51, 51);">/resume</font></code> |
| <code><font style="color:rgb(51, 51, 51);">/clear</font></code> | <font style="color:rgb(51, 51, 51);">清除当前对话历史，开始全新会话</font> | <code><font style="color:rgb(51, 51, 51);">/clear</font></code> |
| <code><font style="color:rgb(51, 51, 51);">/config</font></code> | <font style="color:rgb(51, 51, 51);">查看和修改 Claude Code 配置</font> | <code><font style="color:rgb(51, 51, 51);">/config</font></code> |
| <code><font style="color:rgb(51, 51, 51);">exit</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">或</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">Ctrl+C</font></code> | <font style="color:rgb(51, 51, 51);">退出 Claude Code，返回终端</font> | <code><font style="color:rgb(51, 51, 51);">exit</font></code> |

##

# Claude Code IDE 深度集成：VS Code 与 JetBrains 双端实战

## <font style="color:rgb(51, 51, 51);">VS Code 安装 Claude Code</font>

<font style="color:rgb(51, 51, 51);">如果不喜欢使用 Claude Code 的命令行模型，我们可以在 VS Code 编辑器中安装 Claude Code。</font>

<font style="color:rgb(51, 51, 51);">打开 VS Code，进入扩展市场，搜索</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:rgb(51, 51, 51);">Claude Code</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">安装：</font>

![1783580729129-852752e4-6653-4e37-a858-7b823c25add4.png](./img/wf9R51v5S5sXlvV1/1783580729129-852752e4-6653-4e37-a858-7b823c25add4-170847.png)

<font style="color:rgb(51, 51, 51);">安装完成后，点击右上角 Claude Code 图标，即可进入 Claude Code 页面：</font>

![1783580729307-50884291-6ae1-4e38-ba4f-bc056bec3e7a.png](./img/wf9R51v5S5sXlvV1/1783580729307-50884291-6ae1-4e38-ba4f-bc056bec3e7a-201559.png)

<font style="color:rgb(51, 51, 51);">这样有账号的可以使用 /login 登录：</font>

![1783580729444-8e03ed1c-1ca6-4d45-9f50-e7f6b91d5e77.png](./img/wf9R51v5S5sXlvV1/1783580729444-8e03ed1c-1ca6-4d45-9f50-e7f6b91d5e77-183715.png)

<font style="color:rgb(51, 51, 51);">也可以在对话框输入 /config 进入设置，勾选 Disable Login Prompt 配置来关闭登录页面:</font>

![1783580729303-db0dd577-c65f-4989-9e04-1aa376750ad9.png](./img/wf9R51v5S5sXlvV1/1783580729303-db0dd577-c65f-4989-9e04-1aa376750ad9-299977.png)

<font style="color:rgb(51, 51, 51);">我们可以选中文件中的代码，让 Claude Code 帮我们解析说明或修改，选中后，会提示已经选中的代码行数：</font>

![1783580729416-2228c456-14ff-4f11-8c68-85ef42c41deb.png](./img/wf9R51v5S5sXlvV1/1783580729416-2228c456-14ff-4f11-8c68-85ef42c41deb-927730.png)

<font style="color:rgb(51, 51, 51);">当 Claude 需要修改文件时，它会自动打开并排对比视图，左边显示文件原始内容，右边显示建议修改后的内容，然后询问您是否同意修改。</font>

![1783580729885-a4ddb4c1-4190-4e56-9da5-02f0cf5fd0e6.png](./img/wf9R51v5S5sXlvV1/1783580729885-a4ddb4c1-4190-4e56-9da5-02f0cf5fd0e6-966922.png)

### <font style="color:rgb(51, 51, 51);">使用提示框（聊天输入框）</font>

<font style="color:rgb(51, 51, 51);">提示框就是你和 Claude 聊天的地方，它功能很强大，以下是常用功能，一看就会用：</font>

**<font style="color:rgb(51, 51, 51);">1、权限模式</font>**<font style="color:rgb(51, 51, 51);">：\
</font><font style="color:rgb(51, 51, 51);">点击提示框</font>**<font style="color:rgb(51, 51, 51);">底部</font>**<font style="color:rgb(51, 51, 51);">的模式指示器，就可以切换权限模式。</font>

* **<font style="color:rgb(51, 51, 51);">正常模式</font>**<font style="color:rgb(51, 51, 51);">（默认）：Claude 每次要操作前都会先问你同不同意。</font>
* **<font style="color:rgb(51, 51, 51);">Plan Mode（计划模式）</font>**<font style="color:rgb(51, 51, 51);">：Claude 先告诉你它打算怎么做，得到你批准后才动手修改。</font>
* **<font style="color:rgb(51, 51, 51);">自动接受模式</font>**<font style="color:rgb(51, 51, 51);">：Claude 直接编辑，不再每次询问。\
  </font><font style="color:rgb(51, 51, 51);">你也可以在 VS Code 设置里搜索</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">claudeCode.initialPermissionMode</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">来设置默认模式。</font>

![1783580729875-2f6baccd-a926-42b8-bf2f-00df8bd062e2.png](./img/wf9R51v5S5sXlvV1/1783580729875-2f6baccd-a926-42b8-bf2f-00df8bd062e2-731823.png)

**<font style="color:rgb(51, 51, 51);">2、命令菜单</font>**<font style="color:rgb(51, 51, 51);">：\
</font><font style="color:rgb(51, 51, 51);">在提示框里输入</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">/</font></code><font style="color:rgb(51, 51, 51);">（或点击输入框）就能打开命令菜单。</font>

<font style="color:rgb(51, 51, 51);">常用选项包括：附加文件、切换模型、开启扩展思考、查看使用量（输入</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">/usage</font></code><font style="color:rgb(51, 51, 51);">）。</font>

<font style="color:rgb(51, 51, 51);">下方的"自定义"部分还能管理 MCP servers、hooks、记忆、权限和插件。</font>

<font style="color:rgb(51, 51, 51);">带有</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:rgb(51, 51, 51);">终端图标</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">的命令，会在 VS Code 的集成终端里直接打开。</font>

![1783580729975-bd7d9c21-ca4b-49c2-954c-38bad8d3a12a.png](./img/wf9R51v5S5sXlvV1/1783580729975-bd7d9c21-ca4b-49c2-954c-38bad8d3a12a-150145.png)

**<font style="color:rgb(51, 51, 51);">3、上下文用量指示器</font>**<font style="color:rgb(51, 51, 51);">：提示框下方会实时显示你已经用了多少 Claude 的上下文窗口（context）。</font>

<font style="color:rgb(51, 51, 51);">Claude 会自动帮你压缩内容；如果你想手动压缩，输入</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">/compact</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">即可。</font>

**<font style="color:rgb(51, 51, 51);">4、扩展思考（Extended Thinking）</font>**<font style="color:rgb(51, 51, 51);">：遇到复杂问题时，可以让 Claude 多花点时间深度思考。</font>

<font style="color:rgb(51, 51, 51);">通过命令菜单（输入</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">/</font></code><font style="color:rgb(51, 51, 51);">）切换开启/关闭。</font>

**<font style="color:rgb(51, 51, 51);">5、多行输入</font>**<font style="color:rgb(51, 51, 51);">：\
</font><font style="color:rgb(51, 51, 51);">按</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:rgb(51, 51, 51);">Shift + Enter</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">可以换行，不用立刻发送消息。</font>

<font style="color:rgb(51, 51, 51);">在弹出的"其他"自由文本框里也同样适用。</font>

### <font style="color:rgb(51, 51, 51);">引用文件和文件夹（@ 提及功能）</font>

<font style="color:rgb(51, 51, 51);">想让 Claude 看懂你的代码？直接用</font><font style="color:rgb(51, 51, 51);"> </font><code>**<font style="color:rgb(51, 51, 51);">@</font>**</code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">提到文件或文件夹就行！</font>

<font style="color:rgb(51, 51, 51);">输入</font><font style="color:rgb(51, 51, 51);"> </font><code>**<font style="color:rgb(51, 51, 51);">@</font>**</code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">后面跟文件名或文件夹名，Claude 就会自动读取内容，可以回答问题或直接修改。</font>

![1783580730040-f13c7ea0-4ddd-4bed-8937-1415126b1fef.png](./img/wf9R51v5S5sXlvV1/1783580730040-f13c7ea0-4ddd-4bed-8937-1415126b1fef-290926.png)

<font style="color:rgb(51, 51, 51);">支持</font>**<font style="color:rgb(51, 51, 51);">模糊匹配</font>**<font style="color:rgb(51, 51, 51);">，不用打全名：</font>

```plain
解释一下 @auth 的逻辑（会自动匹配 auth.js、AuthService.ts 等）
@src/components/ 里有什么？（文件夹要加斜杠 / ）
```

**<font style="color:rgb(51, 51, 51);">超实用小技巧</font>**<font style="color:rgb(51, 51, 51);">：</font>

* **<font style="color:rgb(51, 51, 51);">选中代码时</font>**<font style="color:rgb(51, 51, 51);">：直接在编辑器里选中一段代码，Claude 会自动看到你选中的部分。提示框下方会显示"已选中 XX 行"。</font>
* **<font style="color:rgb(51, 51, 51);">快速插入</font>**<font style="color:rgb(51, 51, 51);">：按</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:rgb(51, 51, 51);">Option + K</font>**<font style="color:rgb(51, 51, 51);">（Mac）或</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:rgb(51, 51, 51);">Alt + K</font>**<font style="color:rgb(51, 51, 51);">（Windows/Linux），就能插入带文件路径和行号的 @ 提及，例如</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">@app.ts#5-10</font></code><font style="color:rgb(51, 51, 51);">。</font>
* **<font style="color:rgb(51, 51, 51);">隐藏选中内容</font>**<font style="color:rgb(51, 51, 51);">：点击提示框底部的"选择指示器"（眼睛图标），斜杠眼睛表示 Claude 看不到你选中的文本。</font>
* **<font style="color:rgb(51, 51, 51);">拖拽附件</font>**<font style="color:rgb(51, 51, 51);">：把文件拖到提示框时按住</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:rgb(51, 51, 51);">Shift</font>**<font style="color:rgb(51, 51, 51);">，可以作为附件添加。\
  </font><font style="color:rgb(51, 51, 51);">想删除附件？点击附件右上角的 × 即可。</font>

**<font style="color:rgb(51, 51, 51);">PDF 大文件专属</font>**<font style="color:rgb(51, 51, 51);">：你可以指定让 Claude 只读某几页，例如"第 1-10 页"或"从第 3 页开始"。</font>

### <font style="color:rgb(51, 51, 51);">恢复过去的对话</font>

<font style="color:rgb(51, 51, 51);">点击 Claude Code 面板</font>**<font style="color:rgb(51, 51, 51);">顶部</font>**<font style="color:rgb(51, 51, 51);">的下拉菜单，就能看到你的所有聊天历史记录。</font>

<font style="color:rgb(51, 51, 51);">支持</font>**<font style="color:rgb(51, 51, 51);">关键字搜索</font>**<font style="color:rgb(51, 51, 51);">，也能按时间筛选（今天、昨天、过去 7 天等）。</font>

<font style="color:rgb(51, 51, 51);">点击任意一条记录，就能完整恢复之前的对话内容。</font>

<font style="color:rgb(51, 51, 51);">鼠标悬停在某条记录上，会出现</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:rgb(51, 51, 51);">重命名</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">和</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:rgb(51, 51, 51);">删除</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">按钮：</font>

* <font style="color:rgb(51, 51, 51);">重命名：给对话起个好记的标题</font>
* <font style="color:rgb(51, 51, 51);">删除：把这条记录从列表里移除</font>

![1783580730162-5c8b25d0-4219-4fd4-9071-c75b75e156d9.png](./img/wf9R51v5S5sXlvV1/1783580730162-5c8b25d0-4219-4fd4-9071-c75b75e156d9-993374.png)

## <font style="color:rgb(51, 51, 51);">JetBrains IDEs 中使用 Claude Code</font>

<font style="color:rgb(51, 51, 51);">Claude Code 通过专用插件与 JetBrains IDEs 深度集成，提供交互式差异查看、代码选区上下文共享等强大功能，让 AI 辅助编程无缝融入你的开发工作流。</font>

### <font style="color:rgb(51, 51, 51);">支持的 IDE</font>

<font style="color:rgb(51, 51, 51);">Claude Code 插件支持绝大多数 JetBrains IDE，包括：</font>

* <font style="color:rgb(51, 51, 51);">IntelliJ IDEA</font>
* <font style="color:rgb(51, 51, 51);">PyCharm</font>
* <font style="color:rgb(51, 51, 51);">Android Studio</font>
* <font style="color:rgb(51, 51, 51);">WebStorm</font>
* <font style="color:rgb(51, 51, 51);">PhpStorm</font>
* <font style="color:rgb(51, 51, 51);">GoLand</font>

### <font style="color:rgb(51, 51, 51);">核心功能</font>

| <font style="color:rgb(255, 255, 255);">功能</font> | <font style="color:rgb(255, 255, 255);">说明</font> |
| --- | --- |
| **<font style="color:rgb(51, 51, 51);">快速启动</font>** | <font style="color:rgb(51, 51, 51);">Mac 使用</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">Cmd+Esc</font></code><br/><font style="color:rgb(51, 51, 51);">，Windows/Linux 使用</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">Ctrl+Esc</font></code><br/><font style="color:rgb(51, 51, 51);">，直接从编辑器打开 Claude Code</font> |
| **<font style="color:rgb(51, 51, 51);">Diff 查看</font>** | <font style="color:rgb(51, 51, 51);">代码变更直接在 IDE 的 Diff 查看器中展示，而非在终端中</font> |
| **<font style="color:rgb(51, 51, 51);">选区上下文共享</font>** | <font style="color:rgb(51, 51, 51);">IDE 中当前选中的代码或标签页内容会自动共享给 Claude Code</font> |
| **<font style="color:rgb(51, 51, 51);">文件引用快捷键</font>** | <font style="color:rgb(51, 51, 51);">Mac 使用</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">Cmd+Option+K</font></code><br/><font style="color:rgb(51, 51, 51);">，Linux/Windows 使用</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">Alt+Ctrl+K</font></code><br/><font style="color:rgb(51, 51, 51);">，快速插入如</font><font style="color:rgb(51, 51, 51);"> </font><code>[<font style="color:rgb(0, 102, 0);">@src</font>](https://github.com/src)<font style="color:rgb(51, 51, 51);">/auth.ts#L1-99</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">形式的文件引用</font> |
| **<font style="color:rgb(51, 51, 51);">诊断信息共享</font>** | <font style="color:rgb(51, 51, 51);">IDE 中的 lint 错误、语法错误等诊断信息会在你工作时自动共享给 Claude</font> |

***

### <font style="color:rgb(51, 51, 51);">安装配置</font>

### <font style="color:rgb(51, 51, 51);">第一步：安装前提条件</font>

<font style="color:rgb(51, 51, 51);">在安装 JetBrains 插件之前，需要先安装 Claude Code CLI。</font>

```plain
# macOS、Linux、WSL 安装
curl -fsSL https://claude.ai/install.sh | bash
# Windows PowerShell 安装
irm https://claude.ai/install.ps1 | iex

# 验证安装
claude --version
```

*<font style="color:rgb(44, 58, 94);">如需详细安装步骤，请参考</font>\_\_<font style="color:rgb(44, 58, 94);"> </font>*[*<font style="color:rgb(0, 102, 0);">Claude Code 安装指南</font>*](https://www.runoob.com/claude-code/claude-code-install.html)*<font style="color:rgb(44, 58, 94);">。</font>*

#### <font style="color:rgb(51, 51, 51);">第二步：安装 JetBrains 插件</font>

1. <font style="color:rgb(51, 51, 51);">打开你的 JetBrains IDE</font>
2. <font style="color:rgb(51, 51, 51);">进入</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:rgb(51, 51, 51);">Settings（设置）→ Plugins（插件）</font>**
3. <font style="color:rgb(51, 51, 51);">切换到</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:rgb(51, 51, 51);">Marketplace（市场）</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">标签</font>
4. <font style="color:rgb(51, 51, 51);">搜索</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:rgb(51, 51, 51);">Claude Code</font>**
5. <font style="color:rgb(51, 51, 51);">点击</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:rgb(51, 51, 51);">Install（安装）</font>**
6. <font style="color:rgb(51, 51, 51);">安装完成后</font>**<font style="color:rgb(51, 51, 51);">重启 IDE</font>**

![1783580755298-21c95458-ad9a-44eb-b792-886caec462a5.png](./img/wf9R51v5S5sXlvV1/1783580755298-21c95458-ad9a-44eb-b792-886caec462a5-566718.png)

#### <font style="color:rgb(51, 51, 51);">第三步：启动并连接 Claude Code</font>

#### <font style="color:rgb(51, 51, 51);">从 IDE 集成终端启动（推荐）</font>

<font style="color:rgb(51, 51, 51);">在 IDE 内置终端中运行以下命令，所有集成功能将自动激活：</font>

claude

![1783580755232-db68062a-e031-4579-a235-e73dc008b7b7.png](./img/wf9R51v5S5sXlvV1/1783580755232-db68062a-e031-4579-a235-e73dc008b7b7-711158.png)

<font style="color:rgb(51, 51, 51);">这是一个欢迎界面，按下 Enter 后，就可以开始干活了：</font>

![1783580755186-3a4008a7-a6d4-4973-84be-4b7f653a0159.png](./img/wf9R51v5S5sXlvV1/1783580755186-3a4008a7-a6d4-4973-84be-4b7f653a0159-476841.png)

#### <font style="color:rgb(51, 51, 51);">从外部终端连接</font>

<font style="color:rgb(51, 51, 51);">如果你使用的是外部终端，可以通过</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">/ide</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">命令将 Claude Code 连接到你的 JetBrains IDE：</font>

```plain
# 先启动 Claude Code
claude

# 然后执行 /ide 命令连接 IDE
/ide
```

![1783580755252-3b885576-f71f-45ad-a0bd-900ec61ce511.png](./img/wf9R51v5S5sXlvV1/1783580755252-3b885576-f71f-45ad-a0bd-900ec61ce511-199125.png)

*<font style="color:rgb(44, 58, 94);">💡</font>**<font style="color:rgb(44, 58, 94);"> </font>**__<font style="color:rgb(44, 58, 94);">提示</font>__\_\_<font style="color:rgb(44, 58, 94);">：为确保 Claude 能访问与 IDE 相同的文件，请从 IDE 项目根目录启动 Claude Code。</font>*

#### <font style="color:rgb(51, 51, 51);">第四步：配置 Claude Code</font>

#### <font style="color:rgb(51, 51, 51);">配置 Diff 工具</font>

<font style="color:rgb(51, 51, 51);">运行 Claude Code 后，通过以下步骤设置 Diff 显示方式：</font>

```plain
# 启动 Claude Code
claude

# 进入配置
/config
```

<font style="color:rgb(51, 51, 51);">将 diff 工具设置为</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">auto</font></code><font style="color:rgb(51, 51, 51);">，代码变更将直接在 IDE Diff 查看器中显示；设置为</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">terminal</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">则保留在终端中展示。</font>

![1783580755304-43dec574-913a-42e1-8969-09333c9286fe.png](./img/wf9R51v5S5sXlvV1/1783580755304-43dec574-913a-42e1-8969-09333c9286fe-167446.png)

#### <font style="color:rgb(51, 51, 51);">配置插件设置</font>

<font style="color:rgb(51, 51, 51);">进入</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:rgb(51, 51, 51);">Settings → Tools → Claude Code \[Beta]</font>**<font style="color:rgb(51, 51, 51);">，可以配置以下选项：</font>

* **<font style="color:rgb(51, 51, 51);">Claude command（Claude 命令路径）</font>**<font style="color:rgb(51, 51, 51);">：自定义运行 Claude 的命令，例如</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">claude</font></code><font style="color:rgb(51, 51, 51);">、</font><code><font style="color:rgb(51, 51, 51);">/usr/local/bin/claude</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">或</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">npx @anthropic-ai/claude-code</font></code>
* **<font style="color:rgb(51, 51, 51);">Suppress notification for Claude command not found</font>**<font style="color:rgb(51, 51, 51);">：关闭找不到 Claude 命令时的通知提示</font>
* **<font style="color:rgb(51, 51, 51);">Enable using Option+Enter for multi-line prompts</font>**<font style="color:rgb(51, 51, 51);">（仅 macOS）：启用后，</font><code><font style="color:rgb(51, 51, 51);">Option+Enter</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">可在提示框中插入换行</font>
* **<font style="color:rgb(51, 51, 51);">Enable automatic updates</font>**<font style="color:rgb(51, 51, 51);">：自动检查并安装插件更新，重启后生效</font>

![1783580755656-c4967a4f-91ea-455e-b4af-5368dba8b32e.png](./img/wf9R51v5S5sXlvV1/1783580755656-c4967a4f-91ea-455e-b4af-5368dba8b32e-128575.png)

*<font style="color:rgb(44, 58, 94);">💡</font>**<font style="color:rgb(44, 58, 94);"> </font>**__<font style="color:rgb(44, 58, 94);">WSL 用户</font>__**<font style="color:rgb(44, 58, 94);">：将 Claude 命令设置为</font>**<font style="color:rgb(44, 58, 94);"> </font>*<code>_<font style="color:rgb(44, 58, 94);">wsl -d Ubuntu -- bash -lic "claude"</font>_</code>*<font style="color:rgb(44, 58, 94);">（将</font>\_\_<font style="color:rgb(44, 58, 94);"> </font>*<code>_<font style="color:rgb(44, 58, 94);">Ubuntu</font>_</code>*<font style="color:rgb(44, 58, 94);"> </font>\_\_<font style="color:rgb(44, 58, 94);">替换为你的 WSL 发行版名称）。</font>*

##### <font style="color:rgb(51, 51, 51);">配置 ESC 键（可选）</font>

<font style="color:rgb(51, 51, 51);">如果</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">ESC</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">键无法中断 Claude Code 操作，按以下步骤修复：</font>

1. <font style="color:rgb(51, 51, 51);">进入</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:rgb(51, 51, 51);">Settings → Tools → Terminal</font>**
2. <font style="color:rgb(51, 51, 51);">取消勾选</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:rgb(51, 51, 51);">"Move focus to the editor with Escape"</font>**<font style="color:rgb(51, 51, 51);">，或点击</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:rgb(51, 51, 51);">"Configure terminal keybindings"</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">并删除</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:rgb(51, 51, 51);">"Switch focus to Editor"</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">快捷键</font>
3. <font style="color:rgb(51, 51, 51);">应用更改</font>

![1783580755641-5fd6c22d-dcfb-4121-92ab-8ea4a1dd070e.png](./img/wf9R51v5S5sXlvV1/1783580755641-5fd6c22d-dcfb-4121-92ab-8ea4a1dd070e-000043.png)

***

### <font style="color:rgb(51, 51, 51);">特殊场景配置</font>

### <font style="color:rgb(51, 51, 51);">远程开发（Remote Development）</font>

<font style="color:rgb(51, 51, 51);">使用 JetBrains Remote Development 时，必须将插件安装在</font>**<font style="color:rgb(51, 51, 51);">远程主机</font>**<font style="color:rgb(51, 51, 51);">上，而非本地客户端机器。</font>

<font style="color:rgb(51, 51, 51);">操作路径：</font>**<font style="color:rgb(51, 51, 51);">Settings → Plugin (Host)</font>**

#### <font style="color:rgb(51, 51, 51);">WSL2 配置</font>

<font style="color:rgb(51, 51, 51);">如果在 WSL2 环境下使用 Claude Code，且出现</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:rgb(51, 51, 51);">"No available IDEs detected"</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">错误，通常是 WSL2 的 NAT 网络或 Windows 防火墙阻断了连接。</font>

**<font style="color:rgb(51, 51, 51);">方案一：添加 Windows 防火墙规则（推荐）</font>**

```plain
# 第一步：在 WSL 中查看 IP 地址
hostname -I
# 例如输出 172.21.123.45，子网为 172.21.0.0/16
```

```plain
# 第二步：以管理员身份打开 PowerShell，创建防火墙规则（根据你的子网调整 IP 范围）
New-NetFirewallRule -DisplayName "Allow WSL2 Internal Traffic" -Direction Inbound -Protocol TCP -Action Allow -RemoteAddress 172.21.0.0/16 -LocalAddress 172.21.0.0/16
```

<font style="color:rgb(51, 51, 51);">然后重启 IDE 和 Claude Code 即可生效。</font>

**<font style="color:rgb(51, 51, 51);">方案二：切换 WSL2 为镜像网络模式</font>**<font style="color:rgb(51, 51, 51);">（需要 Windows 11 22H2 或更高版本）</font>

<font style="color:rgb(51, 51, 51);">在 Windows 用户目录下的</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">.wslconfig</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">文件中添加：</font>

```plain
[wsl2]
networkingMode=mirrored
```

<font style="color:rgb(51, 51, 51);">然后在 PowerShell 中执行</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">wsl --shutdown</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">重启 WSL。</font>

***

### <font style="color:rgb(51, 51, 51);">常见问题排查</font>

#### <font style="color:rgb(51, 51, 51);">插件安装后功能未出现</font>

* <font style="color:rgb(51, 51, 51);">确认 Claude Code 是从</font>**<font style="color:rgb(51, 51, 51);">项目根目录</font>**<font style="color:rgb(51, 51, 51);">启动的</font>
* <font style="color:rgb(51, 51, 51);">检查 JetBrains 插件是否已在 IDE 设置中启用</font>
* <font style="color:rgb(51, 51, 51);">尝试</font>**<font style="color:rgb(51, 51, 51);">完全重启 IDE</font>**<font style="color:rgb(51, 51, 51);">（可能需要多次重启）</font>
* <font style="color:rgb(51, 51, 51);">远程开发场景下，确认插件已安装在远程主机上</font>

#### <font style="color:rgb(51, 51, 51);">提示 "No available IDEs detected"</font>

* <font style="color:rgb(51, 51, 51);">确认插件已安装并启用</font>
* <font style="color:rgb(51, 51, 51);">完全重启 IDE</font>
* <font style="color:rgb(51, 51, 51);">确保 Claude Code 是从 IDE 集成终端中运行的</font>
* <font style="color:rgb(51, 51, 51);">WSL 用户请参考上方</font><font style="color:rgb(51, 51, 51);"> </font>[<font style="color:rgb(0, 102, 0);">WSL2 配置</font>](https://www.runoob.com/claude-code/claude-code-jetbrains.html#wsl2-%E9%85%8D%E7%BD%AE)<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">章节</font>

#### <font style="color:rgb(51, 51, 51);">点击 Claude 图标提示 "command not found"</font>

1. <font style="color:rgb(51, 51, 51);">在终端运行</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">claude --version</font></code><font style="color:rgb(51, 51, 51);">，验证 Claude Code 已正确安装</font>
2. <font style="color:rgb(51, 51, 51);">在插件设置中手动配置 Claude 命令路径</font>
3. <font style="color:rgb(51, 51, 51);">WSL 用户请使用前述 WSL 命令格式</font>

# Claude Code 项目初始化与 CLI 高效交互指南

## <font style="color:rgb(51, 51, 51);">Claude Code 项目初始化</font>

<font style="color:rgb(51, 51, 51);">Claude Code 项目初始化可以在 Claude Code 的交互界面中输入：</font>

/init

<font style="color:rgb(51, 51, 51);">我们可以在一个已有的项目目录初始化，也可以新建一个。</font>

<font style="color:rgb(51, 51, 51);">我们可以先创建一个目录：</font>

mkdir claude-runoob-test

<font style="color:rgb(51, 51, 51);">进入该目录：</font>

cd claude-runoob-test

<font style="color:rgb(51, 51, 51);">创建一个测试文件 test.py，代码如下：</font>

print("Hello, Runoob!")

<font style="color:rgb(51, 51, 51);">进入 Claude Code 的交互界面：</font>

claude

<font style="color:rgb(51, 51, 51);">使用</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:rgb(51, 51, 51);">/init</font>\*\*\*\*<font style="color:rgb(51, 51, 51);"> </font>**<font style="color:rgb(51, 51, 51);">命令来初始化项目：</font>

/init

![1783581011230-b62a4ce4-8344-4df9-9c82-071048bb3b83.png](./img/wf9R51v5S5sXlvV1/1783581011230-b62a4ce4-8344-4df9-9c82-071048bb3b83-417073.png)

<font style="color:rgb(51, 51, 51);">如果使用 VS Code，也可以在 VS Code 的 Claude Code 界面输入</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:rgb(51, 51, 51);">/init</font>**<font style="color:rgb(51, 51, 51);">:</font>

![1783581011189-9abfae1e-bc8d-44f7-9272-10f6ff5aa72e.png](./img/wf9R51v5S5sXlvV1/1783581011189-9abfae1e-bc8d-44f7-9272-10f6ff5aa72e-179919.png)

<font style="color:rgb(51, 51, 51);">Claude 会自动扫描你的代码库——读取 package.json、现有文档、配置文件以及代码结构，然后生成一份专属于你项目的 CLAUDE.md 文件。</font>

<font style="color:rgb(51, 51, 51);">Claude 整个过程无需手动操作，Claude 会自行分析并输出初始配置。</font>

![1783581011257-f4bbb4c0-4ca3-476d-aec2-479a008d1d4a.png](./img/wf9R51v5S5sXlvV1/1783581011257-f4bbb4c0-4ca3-476d-aec2-479a008d1d4a-495321.png)

### <font style="color:rgb(51, 51, 51);">CLAUDE.md 文件</font>

<font style="color:rgb(51, 51, 51);">CLAUDE.md 是一个放在项目根目录的 Markdown 文件，Claude Code 在每次会话开始时都会自动读取。</font>

<font style="color:rgb(51, 51, 51);">CLAUDE.md 会成为 Claude 系统提示的一部分，使每次对话都能预先加载项目上下文，不再需要重复解释基本信息。</font>

<font style="color:rgb(51, 51, 51);">一份好的 CLAUDE.md 应该覆盖三个维度：</font>

* <font style="color:rgb(51, 51, 51);">WHAT（是什么）：技术栈、项目结构，为 Claude 提供代码库的全局地图</font>
* <font style="color:rgb(51, 51, 51);">WHY（为什么）：项目的目的，各模块的功能与定位</font>
* <font style="color:rgb(51, 51, 51);">HOW（怎么做）：开发方式，例如使用 bun 而非 node，以及 Claude 如何验证改动是否正确 Humanlayer</font>

<font style="color:rgb(51, 51, 51);">以下是一份典型的 CLAUDE.md 结构示例：</font>

```plain
# 项目名称

## 项目概述
简述这个项目的目的和功能。

## 技术栈
- Frontend: React + TypeScript
- Backend: Node.js + Express
- Database: PostgreSQL

## 目录结构
- `src/components/` - React 组件
- `src/api/`        - API 层
- `tests/`          - 测试文件

## 常用命令
- 启动开发服务器：`pnpm dev`
- 运行测试：`pnpm test`
- 代码检查：`pnpm lint`

## 开发规范
- 使用 TypeScript strict 模式
- 优先使用 interface 而非 type
- 禁止使用 any，使用 unknown 替代
```

### 文件位置与层级

项目的核心文件结构如下：

```
your-project/
├── CLAUDE.md                  # 项目主记忆文件（团队共享）
├── .claude/
│   ├── settings.json          # Hooks、权限、环境配置
│   ├── settings.local.json    # 个人配置（建议加入 .gitignore）
│   └── commands/              # 自定义斜杠命令
│       └── my-command.md
└── .mcp.json                  # MCP 服务配置
```

````

---

## <font style="color:rgb(51, 51, 51);">初始化后的最佳实践</font>
_**<font style="color:rgb(44, 58, 94);">迭代优化，而非一次写死。</font>**_

`**<font style="color:rgb(51, 51, 51);">/init</font>**`<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">命令适合快速入门，但真正的价值来自于随时间不断迭代，可以补充 Claude 无法自动推断的内容，例如分支命名规范、部署流程、Code Review 要求；同时删去不适用的通用建议。</font>

+ **<font style="color:rgb(51, 51, 51);">提交到版本控制</font>**<font style="color:rgb(51, 51, 51);">：将</font><font style="color:rgb(51, 51, 51);"> </font>`<font style="color:rgb(51, 51, 51);">CLAUDE.md</font>`<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">提交到 Git，这样整个团队都能从中受益，新成员可以通过让 Claude 解释代码库来快速上手。</font>
+ **<font style="color:rgb(51, 51, 51);">保持精简</font>**<font style="color:rgb(51, 51, 51);">：内容要简洁且普遍适用。采用"渐进式披露"原则——不要把所有你想让 Claude 知道的内容都塞进去，而是告诉它</font>**<font style="color:rgb(51, 51, 51);">如何查找重要信息</font>**<font style="color:rgb(51, 51, 51);">，让它按需获取，避免撑爆上下文窗口。</font>
+ **<font style="color:rgb(51, 51, 51);">不要让 CLAUDE.md 替代 linter</font>**<font style="color:rgb(51, 51, 51);">：在文件中写代码风格规范是最常见的误区之一。永远不要用 LLM 来做 linter 的工作——linter 更快、更便宜，而且是确定性的。代码风格约束只会让上下文窗口膨胀，降低 Claude 的指令遵从质量。</font>

---

## <font style="color:rgb(51, 51, 51);">使用</font><font style="color:rgb(51, 51, 51);"> </font>`<font style="color:rgb(51, 51, 51);">#</font>`<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">快捷键持续更新</font>
<font style="color:rgb(51, 51, 51);">在对话中，随时用</font><font style="color:rgb(51, 51, 51);"> </font>`<font style="color:rgb(51, 51, 51);">#</font>`<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">前缀给 Claude 发送记忆指令：</font>

```plain
# 我们始终使用 pnpm，不用 npm
# 所有组件必须包含单元测试
````

<font style="color:rgb(51, 51, 51);">这些补充会逐渐积累，形成一份真正反映团队实际工作方式的</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">CLAUDE.md</font></code><font style="color:rgb(51, 51, 51);">。</font>

***

## <font style="color:rgb(51, 51, 51);">验证初始化效果</font>

<font style="color:rgb(51, 51, 51);">初始化完成后，可以通过以下对话确认 Claude 是否正确理解了项目：</font>

* <font style="color:rgb(51, 51, 51);">这个项目是做什么的？</font>
* <font style="color:rgb(51, 51, 51);">解释一下目录结构。</font>
* <font style="color:rgb(51, 51, 51);">项目用了哪些技术？</font>
* <font style="color:rgb(51, 51, 51);">运行测试的命令是什么？</font>

<font style="color:rgb(51, 51, 51);"></font>

## <font style="color:rgb(51, 51, 51);">Claude Code CLI 高效交互指南</font>

***

## <font style="color:rgb(51, 51, 51);">一、CLI 命令</font>

| <font style="color:rgb(255, 255, 255);">命令</font> | <font style="color:rgb(255, 255, 255);">描述</font> | <font style="color:rgb(255, 255, 255);">示例</font> |
| --- | --- | --- |
| <code><font style="color:rgb(51, 51, 51);">claude</font></code> | <font style="color:rgb(51, 51, 51);">启动交互式 REPL</font> | <code><font style="color:rgb(51, 51, 51);">claude</font></code> |
| <code><font style="color:rgb(51, 51, 51);">claude "query"</font></code> | <font style="color:rgb(51, 51, 51);">带初始提示启动 REPL</font> | <code><font style="color:rgb(51, 51, 51);">claude "explain this project"</font></code> |
| <code><font style="color:rgb(51, 51, 51);">claude -p "query"</font></code> | <font style="color:rgb(51, 51, 51);">SDK 查询后退出</font> | <code><font style="color:rgb(51, 51, 51);">claude -p "explain this function"</font></code> |
| <font style="color:rgb(51, 51, 51);">cat file | claude -p "query"</font> | <font style="color:rgb(51, 51, 51);">处理管道输入内容</font> | <font style="color:rgb(51, 51, 51);">cat logs.txt | claude -p "explain"</font> |
| <code><font style="color:rgb(51, 51, 51);">claude -c</font></code> | <font style="color:rgb(51, 51, 51);">继续当前目录最近对话</font> | <code><font style="color:rgb(51, 51, 51);">claude -c</font></code> |
| <code><font style="color:rgb(51, 51, 51);">claude -c -p "query"</font></code> | <font style="color:rgb(51, 51, 51);">通过 SDK 继续对话</font> | <code><font style="color:rgb(51, 51, 51);">claude -c -p "Check for type errors"</font></code> |
| <code><font style="color:rgb(51, 51, 51);">claude -r "<session>" "query"</font></code> | <font style="color:rgb(51, 51, 51);">按 ID/名称恢复会话</font> | <code><font style="color:rgb(51, 51, 51);">claude -r "auth-refactor" "Finish this PR"</font></code> |
| <code><font style="color:rgb(51, 51, 51);">claude update</font></code> | <font style="color:rgb(51, 51, 51);">更新至最新版本</font> | <code><font style="color:rgb(51, 51, 51);">claude update</font></code> |
| <code><font style="color:rgb(51, 51, 51);">claude mcp</font></code> | <font style="color:rgb(51, 51, 51);">配置 MCP 服务器</font> | <font style="color:rgb(51, 51, 51);">详见</font><font style="color:rgb(51, 51, 51);"> </font>[<font style="color:rgb(0, 102, 0);">Claude Code MCP 文档</font>](https://www.runoob.com/claude-code/claude-code-mcp.html) |

***

## <font style="color:rgb(51, 51, 51);">二、CLI 标志</font>

<font style="color:rgb(51, 51, 51);">通过以下标志可自定义 Claude Code 运行行为：</font>

| <font style="color:rgb(255, 255, 255);">标志</font> | <font style="color:rgb(255, 255, 255);">描述</font> | <font style="color:rgb(255, 255, 255);">示例</font> |
| --- | --- | --- |
| <code><font style="color:rgb(51, 51, 51);">--add-dir</font></code> | <font style="color:rgb(51, 51, 51);">添加工作目录（自动验证路径有效性）</font> | <code><font style="color:rgb(51, 51, 51);">claude --add-dir ../apps ../lib</font></code> |
| <code><font style="color:rgb(51, 51, 51);">--agent</font></code> | <font style="color:rgb(51, 51, 51);">指定会话代理（覆盖默认</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">agent</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">设置）</font> | <code><font style="color:rgb(51, 51, 51);">claude --agent my-custom-agent</font></code> |
| <code><font style="color:rgb(51, 51, 51);">--agents</font></code> | <font style="color:rgb(51, 51, 51);">以 JSON 定义自定义子代理</font> | <code><font style="color:rgb(51, 51, 51);">claude --agents '{"reviewer":{"description":"Reviews code","prompt":"You are a code reviewer"}}'</font></code> |
| <code><font style="color:rgb(51, 51, 51);">--allowedTools</font></code> | <font style="color:rgb(51, 51, 51);">免权限提示的可用工具（限制工具用</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">--tools</font></code><br/><font style="color:rgb(51, 51, 51);">）</font> | <code><font style="color:rgb(51, 51, 51);">"Bash(git log:*)" "Bash(git diff:*)" "Read"</font></code> |
| <code><font style="color:rgb(51, 51, 51);">--append-system-prompt</font></code> | <font style="color:rgb(51, 51, 51);">追加内容到默认系统提示（交互/打印模式均生效）</font> | <code><font style="color:rgb(51, 51, 51);">claude --append-system-prompt "Always use TypeScript"</font></code> |
| <code><font style="color:rgb(51, 51, 51);">--betas</font></code> | <font style="color:rgb(51, 51, 51);">API 请求附加 Beta 标头（仅限 API 密钥用户）</font> | <code><font style="color:rgb(51, 51, 51);">claude --betas interleaved-thinking</font></code> |
| <code><font style="color:rgb(51, 51, 51);">--chrome</font></code> | <font style="color:rgb(51, 51, 51);">启用 Chrome 浏览器集成（网络自动化/测试）</font> | <code><font style="color:rgb(51, 51, 51);">claude --chrome</font></code> |
| <code><font style="color:rgb(51, 51, 51);">--continue</font></code><br/><font style="color:rgb(51, 51, 51);">,</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">-c</font></code> | <font style="color:rgb(51, 51, 51);">加载当前目录最近对话</font> | <code><font style="color:rgb(51, 51, 51);">claude --continue</font></code> |
| <code><font style="color:rgb(51, 51, 51);">--dangerously-skip-permissions</font></code> | <font style="color:rgb(51, 51, 51);">跳过权限提示（谨慎操作）</font> | <code><font style="color:rgb(51, 51, 51);">claude --dangerously-skip-permissions</font></code> |
| <code><font style="color:rgb(51, 51, 51);">--debug</font></code> | <font style="color:rgb(51, 51, 51);">启用调试模式，支持类别过滤（如</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">"api,hooks"</font></code><br/><font style="color:rgb(51, 51, 51);">）</font> | <code><font style="color:rgb(51, 51, 51);">claude --debug "api,mcp"</font></code> |
| <code><font style="color:rgb(51, 51, 51);">--disallowedTools</font></code> | <font style="color:rgb(51, 51, 51);">禁用指定工具（从上下文移除）</font> | <code><font style="color:rgb(51, 51, 51);">"Bash(git log:*)" "Bash(git diff:*)" "Edit"</font></code> |
| <code><font style="color:rgb(51, 51, 51);">--fallback-model</font></code> | <font style="color:rgb(51, 51, 51);">默认模型过载时自动切换（仅打印模式）</font> | <code><font style="color:rgb(51, 51, 51);">claude -p --fallback-model sonnet "query"</font></code> |
| <code><font style="color:rgb(51, 51, 51);">--fork-session</font></code> | <font style="color:rgb(51, 51, 51);">恢复会话时生成新 ID（搭配</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">--resume</font></code><br/><font style="color:rgb(51, 51, 51);">/</font><code><font style="color:rgb(51, 51, 51);">--continue</font></code><br/><font style="color:rgb(51, 51, 51);">）</font> | <code><font style="color:rgb(51, 51, 51);">claude --resume abc123 --fork-session</font></code> |
| <code><font style="color:rgb(51, 51, 51);">--ide</font></code> | <font style="color:rgb(51, 51, 51);">自动连接可用 IDE</font> | <code><font style="color:rgb(51, 51, 51);">claude --ide</font></code> |
| <code><font style="color:rgb(51, 51, 51);">--include-partial-messages</font></code> | <font style="color:rgb(51, 51, 51);">输出包含部分流事件（需搭配</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">--print</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">和</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">--output-format=stream-json</font></code><br/><font style="color:rgb(51, 51, 51);">）</font> | <code><font style="color:rgb(51, 51, 51);">claude -p --output-format stream-json --include-partial-messages "query"</font></code> |
| <code><font style="color:rgb(51, 51, 51);">--input-format</font></code> | <font style="color:rgb(51, 51, 51);">打印模式输入格式（可选</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">text</font></code><br/><font style="color:rgb(51, 51, 51);">/</font><code><font style="color:rgb(51, 51, 51);">stream-json</font></code><br/><font style="color:rgb(51, 51, 51);">）</font> | <code><font style="color:rgb(51, 51, 51);">claude -p --output-format json --input-format stream-json</font></code> |
| <code><font style="color:rgb(51, 51, 51);">--json-schema</font></code> | <font style="color:rgb(51, 51, 51);">输出符合 JSON Schema 的验证结果（仅打印模式）</font> | <code><font style="color:rgb(51, 51, 51);">claude -p --json-schema '{"type":"object","properties":{...}}' "query"</font></code> |
| <code><font style="color:rgb(51, 51, 51);">--max-turns</font></code> | <font style="color:rgb(51, 51, 51);">限制代理轮次（仅打印模式，超限报错退出）</font> | <code><font style="color:rgb(51, 51, 51);">claude -p --max-turns 3 "query"</font></code> |
| <code><font style="color:rgb(51, 51, 51);">--mcp-config</font></code> | <font style="color:rgb(51, 51, 51);">从 JSON 文件/字符串加载 MCP 配置</font> | <code><font style="color:rgb(51, 51, 51);">claude --mcp-config ./mcp.json</font></code> |
| <code><font style="color:rgb(51, 51, 51);">--model</font></code> | <font style="color:rgb(51, 51, 51);">指定会话模型（支持别名</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">sonnet</font></code><br/><font style="color:rgb(51, 51, 51);">/</font><code><font style="color:rgb(51, 51, 51);">opus</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">或完整名称）</font> | <code><font style="color:rgb(51, 51, 51);">claude --model claude-sonnet-4-5-20250929</font></code> |
| <code><font style="color:rgb(51, 51, 51);">--no-chrome</font></code> | <font style="color:rgb(51, 51, 51);">禁用 Chrome 集成</font> | <code><font style="color:rgb(51, 51, 51);">claude --no-chrome</font></code> |
| <code><font style="color:rgb(51, 51, 51);">--output-format</font></code> | <font style="color:rgb(51, 51, 51);">打印模式输出格式（可选</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">text</font></code><br/><font style="color:rgb(51, 51, 51);">/</font><code><font style="color:rgb(51, 51, 51);">json</font></code><br/><font style="color:rgb(51, 51, 51);">/</font><code><font style="color:rgb(51, 51, 51);">stream-json</font></code><br/><font style="color:rgb(51, 51, 51);">）</font> | <code><font style="color:rgb(51, 51, 51);">claude -p "query" --output-format json</font></code> |
| <code><font style="color:rgb(51, 51, 51);">--permission-mode</font></code> | <font style="color:rgb(51, 51, 51);">按指定权限模式启动</font> | <code><font style="color:rgb(51, 51, 51);">claude --permission-mode plan</font></code> |
| <code><font style="color:rgb(51, 51, 51);">--permission-prompt-tool</font></code> | <font style="color:rgb(51, 51, 51);">非交互模式指定权限提示处理工具</font> | <code><font style="color:rgb(51, 51, 51);">claude -p --permission-prompt-tool mcp_auth_tool "query"</font></code> |
| <code><font style="color:rgb(51, 51, 51);">--plugin-dir</font></code> | <font style="color:rgb(51, 51, 51);">加载指定目录插件（可重复使用）</font> | <code><font style="color:rgb(51, 51, 51);">claude --plugin-dir ./my-plugins</font></code> |
| <code><font style="color:rgb(51, 51, 51);">--print</font></code><br/><font style="color:rgb(51, 51, 51);">,</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">-p</font></code> | <font style="color:rgb(51, 51, 51);">打印响应后退出（非交互模式）</font> | <code><font style="color:rgb(51, 51, 51);">claude -p "query"</font></code> |
| <code><font style="color:rgb(51, 51, 51);">--resume</font></code><br/><font style="color:rgb(51, 51, 51);">,</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">-r</font></code> | <font style="color:rgb(51, 51, 51);">按 ID/名称恢复会话，或唤起交互式选择器</font> | <code><font style="color:rgb(51, 51, 51);">claude --resume auth-refactor</font></code> |
| <code><font style="color:rgb(51, 51, 51);">--session-id</font></code> | <font style="color:rgb(51, 51, 51);">指定会话 ID（需为有效 UUID）</font> | <code><font style="color:rgb(51, 51, 51);">claude --session-id "550e8400-e29b-41d4-a716-446655440000"</font></code> |
| <code><font style="color:rgb(51, 51, 51);">--setting-sources</font></code> | <font style="color:rgb(51, 51, 51);">指定加载的设置源（逗号分隔</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">user</font></code><br/><font style="color:rgb(51, 51, 51);">/</font><code><font style="color:rgb(51, 51, 51);">project</font></code><br/><font style="color:rgb(51, 51, 51);">/</font><code><font style="color:rgb(51, 51, 51);">local</font></code><br/><font style="color:rgb(51, 51, 51);">）</font> | <code><font style="color:rgb(51, 51, 51);">claude --setting-sources user,project</font></code> |
| <code><font style="color:rgb(51, 51, 51);">--settings</font></code> | <font style="color:rgb(51, 51, 51);">加载自定义 JSON 配置文件/字符串</font> | <code><font style="color:rgb(51, 51, 51);">claude --settings ./settings.json</font></code> |
| <code><font style="color:rgb(51, 51, 51);">--strict-mcp-config</font></code> | <font style="color:rgb(51, 51, 51);">仅使用</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">--mcp-config</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">配置，忽略其他 MCP 设置</font> | <code><font style="color:rgb(51, 51, 51);">claude --strict-mcp-config --mcp-config ./mcp.json</font></code> |
| <code><font style="color:rgb(51, 51, 51);">--system-prompt</font></code> | <font style="color:rgb(51, 51, 51);">替换默认系统提示（交互/打印模式均生效）</font> | <code><font style="color:rgb(51, 51, 51);">claude --system-prompt "You are a Python expert"</font></code> |
| <code><font style="color:rgb(51, 51, 51);">--system-prompt-file</font></code> | <font style="color:rgb(51, 51, 51);">从文件加载系统提示（替换默认，仅打印模式）</font> | <code><font style="color:rgb(51, 51, 51);">claude -p --system-prompt-file ./custom-prompt.txt "query"</font></code> |
| <code><font style="color:rgb(51, 51, 51);">--tools</font></code> | <font style="color:rgb(51, 51, 51);">限制可用内置工具（</font><code><font style="color:rgb(51, 51, 51);">""</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">禁用全部，</font><code><font style="color:rgb(51, 51, 51);">"default"</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">启用全部）</font> | <code><font style="color:rgb(51, 51, 51);">claude --tools "Bash,Edit,Read"</font></code> |
| <code><font style="color:rgb(51, 51, 51);">--verbose</font></code> | <font style="color:rgb(51, 51, 51);">启用详细日志，展示完整逐轮输出</font> | <code><font style="color:rgb(51, 51, 51);">claude --verbose</font></code> |
| <code><font style="color:rgb(51, 51, 51);">--version</font></code><br/><font style="color:rgb(51, 51, 51);">,</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">-v</font></code> | <font style="color:rgb(51, 51, 51);">输出版本号</font> | <code><font style="color:rgb(51, 51, 51);">claude -v</font></code> |

***<font style="color:rgb(44, 58, 94);">提示</font>**\_\_<font style="color:rgb(44, 58, 94);">：</font>*<code>_<font style="color:rgb(44, 58, 94);">--output-format json</font>_</code>*<font style="color:rgb(44, 58, 94);"> </font>\_\_<font style="color:rgb(44, 58, 94);">标志非常适合脚本和自动化场景，可直接编程解析 Claude 响应结果。</font>*

***

## <font style="color:rgb(51, 51, 51);">三、扩展说明</font>

### <font style="color:rgb(51, 51, 51);">3.1 代理标志格式</font>

<code><font style="color:rgb(51, 51, 51);">--agents</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">标志接收 JSON 对象，用于定义一个或多个自定义子代理。每个子代理需配置唯一名称作为键，值为包含以下字段的对象：</font>

| <font style="color:rgb(255, 255, 255);">字段</font> | <font style="color:rgb(255, 255, 255);">必填</font> | <font style="color:rgb(255, 255, 255);">描述</font> |
| --- | --- | --- |
| <code><font style="color:rgb(51, 51, 51);">description</font></code> | <font style="color:rgb(51, 51, 51);">是</font> | <font style="color:rgb(51, 51, 51);">描述子代理的适用场景</font> |
| <code><font style="color:rgb(51, 51, 51);">prompt</font></code> | <font style="color:rgb(51, 51, 51);">是</font> | <font style="color:rgb(51, 51, 51);">定义子代理行为的系统提示</font> |
| <code><font style="color:rgb(51, 51, 51);">tools</font></code> | <font style="color:rgb(51, 51, 51);">否</font> | <font style="color:rgb(51, 51, 51);">子代理专属工具列表（如</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">["Read", "Edit"]</font></code><br/><font style="color:rgb(51, 51, 51);">，省略则继承全部工具）</font> |
| <code><font style="color:rgb(51, 51, 51);">model</font></code> | <font style="color:rgb(51, 51, 51);">否</font> | <font style="color:rgb(51, 51, 51);">子代理使用模型（支持</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">sonnet</font></code><br/><font style="color:rgb(51, 51, 51);">/</font><code><font style="color:rgb(51, 51, 51);">opus</font></code><br/><font style="color:rgb(51, 51, 51);">/</font><code><font style="color:rgb(51, 51, 51);">haiku</font></code><br/><font style="color:rgb(51, 51, 51);">，省略则用默认模型）</font> |

**<font style="color:rgb(51, 51, 51);">示例</font>**

```plain
claude --agents '{
  "code-reviewer": {
    "description": "Expert code reviewer. Use proactively after code changes.",
    "prompt": "You are a senior code reviewer. Focus on code quality, security, and best practices.",
    "tools": ["Read", "Grep", "Glob", "Bash"],
    "model": "sonnet"
  },
  "debugger": {
    "description": "Debugging specialist for errors and test failures.",
    "prompt": "You are an expert debugger. Analyze errors, identify root causes, and provide fixes."
  }
}'
```

### <font style="color:rgb(51, 51, 51);">系统提示标志</font>

<font style="color:rgb(51, 51, 51);">Claude Code 提供 3 种系统提示自定义方式，满足不同使用需求：</font>

| <font style="color:rgb(255, 255, 255);">标志</font> | <font style="color:rgb(255, 255, 255);">行为</font> | <font style="color:rgb(255, 255, 255);">适用模式</font> | <font style="color:rgb(255, 255, 255);">典型用例</font> |
| --- | --- | --- | --- |
| <code><font style="color:rgb(51, 51, 51);">--system-prompt</font></code> | <font style="color:rgb(51, 51, 51);">替换默认系统提示</font> | <font style="color:rgb(51, 51, 51);">交互+打印</font> | <font style="color:rgb(51, 51, 51);">完全自定义 Claude 行为指令</font> |
| <code><font style="color:rgb(51, 51, 51);">--system-prompt-file</font></code> | <font style="color:rgb(51, 51, 51);">从文件加载提示并替换</font> | <font style="color:rgb(51, 51, 51);">仅打印</font> | <font style="color:rgb(51, 51, 51);">团队共享提示模板、版本控制</font> |
| <code><font style="color:rgb(51, 51, 51);">--append-system-prompt</font></code> | <font style="color:rgb(51, 51, 51);">追加内容到默认提示</font> | <font style="color:rgb(51, 51, 51);">交互+打印</font> | <font style="color:rgb(51, 51, 51);">保留默认功能，添加个性化指令</font> |

#### <font style="color:rgb(51, 51, 51);">使用场景与示例</font>

1. <code>**<font style="color:rgb(51, 51, 51);">--system-prompt</font>**</code><font style="color:rgb(51, 51, 51);">：完全接管系统提示，清空默认指令</font><font style="color:rgb(51, 51, 51);">claude --system-prompt "You are a Python expert who only writes type-annotated code"</font>
2. <code>**<font style="color:rgb(51, 51, 51);">--system-prompt-file</font>**</code><font style="color:rgb(51, 51, 51);">：从文件读取提示，适合标准化场景</font><font style="color:rgb(51, 51, 51);">claude -p --system-prompt-file ./prompts/code-review.txt "Review this PR"</font>
3. <code>**<font style="color:rgb(51, 51, 51);">--append-system-prompt</font>**</code><font style="color:rgb(51, 51, 51);">：保留默认功能，追加定制要求（推荐大多数场景使用）</font><font style="color:rgb(51, 51, 51);">claude --append-system-prompt "Always use TypeScript and include JSDoc comments"</font>

***<font style="color:rgb(44, 58, 94);">注意</font>**\_\_<font style="color:rgb(44, 58, 94);">：</font>*<code>_<font style="color:rgb(44, 58, 94);">--system-prompt</font>_</code>*<font style="color:rgb(44, 58, 94);"> </font>**<font style="color:rgb(44, 58, 94);">和</font>**<font style="color:rgb(44, 58, 94);"> </font>*<code>_<font style="color:rgb(44, 58, 94);">--system-prompt-file</font>_</code>*<font style="color:rgb(44, 58, 94);"> </font>**<font style="color:rgb(44, 58, 94);">互斥，不可同时使用。\
</font>**__<font style="color:rgb(44, 58, 94);">提示</font>__**<font style="color:rgb(44, 58, 94);">：优先使用</font>**<font style="color:rgb(44, 58, 94);"> </font>*<code>_<font style="color:rgb(44, 58, 94);">--append-system-prompt</font>_</code>*<font style="color:rgb(44, 58, 94);">，既能保留 Claude Code 内置能力，又能满足定制需求；仅需完全自定义时，再使用另外两个标志。</font>*

<font style="color:rgb(51, 51, 51);">打印模式（</font><code><font style="color:rgb(51, 51, 51);">-p</font></code><font style="color:rgb(51, 51, 51);">）的详细用法（输出格式、流式传输、程序化集成等），参考 </font>[<font style="color:rgb(0, 102, 0);">SDK 文档</font>](https://docs.claude.com/en/docs/agent-sdk)<font style="color:rgb(51, 51, 51);">。</font>

# CLAUDE.md 配置体系与项目架构设计

## <font style="color:rgb(51, 51, 51);">Claude Code 项目初始化</font>

<font style="color:rgb(51, 51, 51);">Claude Code 项目初始化可以在 Claude Code 的交互界面中输入：</font>

/init

<font style="color:rgb(51, 51, 51);">我们可以在一个已有的项目目录初始化，也可以新建一个。</font>

<font style="color:rgb(51, 51, 51);">我们可以先创建一个目录：</font>

mkdir claude-runoob-test

<font style="color:rgb(51, 51, 51);">进入该目录：</font>

cd claude-runoob-test

<font style="color:rgb(51, 51, 51);">创建一个测试文件 test.py，代码如下：</font>

print("Hello, Runoob!")

<font style="color:rgb(51, 51, 51);">进入 Claude Code 的交互界面：</font>

claude

<font style="color:rgb(51, 51, 51);">使用</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:rgb(51, 51, 51);">/init</font>\*\*\*\*<font style="color:rgb(51, 51, 51);"> </font>**<font style="color:rgb(51, 51, 51);">命令来初始化项目：</font>

/init

![1783648913077-6ffcfd0a-2af7-4742-823b-1d8a678a88bb.png](./img/wf9R51v5S5sXlvV1/1783648913077-6ffcfd0a-2af7-4742-823b-1d8a678a88bb-300427.png)

<font style="color:rgb(51, 51, 51);">如果使用 VS Code，也可以在 VS Code 的 Claude Code 界面输入</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:rgb(51, 51, 51);">/init</font>**<font style="color:rgb(51, 51, 51);">:</font>

![1783648913896-943027c5-eb8b-40f9-ab79-e60e1e61c0b4.png](./img/wf9R51v5S5sXlvV1/1783648913896-943027c5-eb8b-40f9-ab79-e60e1e61c0b4-359664.png)

<font style="color:rgb(51, 51, 51);">Claude 会自动扫描你的代码库——读取 package.json、现有文档、配置文件以及代码结构，然后生成一份专属于你项目的 CLAUDE.md 文件。</font>

<font style="color:rgb(51, 51, 51);">Claude 整个过程无需手动操作，Claude 会自行分析并输出初始配置。</font>

![1783648912239-aa8716dc-20c9-4e4e-b7a7-d709e03e59a7.png](./img/wf9R51v5S5sXlvV1/1783648912239-aa8716dc-20c9-4e4e-b7a7-d709e03e59a7-718632.png)

### <font style="color:rgb(51, 51, 51);">CLAUDE.md 文件</font>

<font style="color:rgb(51, 51, 51);">CLAUDE.md 是一个放在项目根目录的 Markdown 文件，Claude Code 在每次会话开始时都会自动读取。</font>

<font style="color:rgb(51, 51, 51);">CLAUDE.md 会成为 Claude 系统提示的一部分，使每次对话都能预先加载项目上下文，不再需要重复解释基本信息。</font>

<font style="color:rgb(51, 51, 51);">一份好的 CLAUDE.md 应该覆盖三个维度：</font>

* <font style="color:rgb(51, 51, 51);">WHAT（是什么）：技术栈、项目结构，为 Claude 提供代码库的全局地图</font>
* <font style="color:rgb(51, 51, 51);">WHY（为什么）：项目的目的，各模块的功能与定位</font>
* <font style="color:rgb(51, 51, 51);">HOW（怎么做）：开发方式，例如使用 bun 而非 node，以及 Claude 如何验证改动是否正确 Humanlayer</font>

<font style="color:rgb(51, 51, 51);">以下是一份典型的 CLAUDE.md 结构示例：</font>

```plain
# 项目名称

## 项目概述
简述这个项目的目的和功能。

## 技术栈
- Frontend: React + TypeScript
- Backend: Node.js + Express
- Database: PostgreSQL

## 目录结构
- `src/components/` - React 组件
- `src/api/`        - API 层
- `tests/`          - 测试文件

## 常用命令
- 启动开发服务器：`pnpm dev`
- 运行测试：`pnpm test`
- 代码检查：`pnpm lint`

## 开发规范
- 使用 TypeScript strict 模式
- 优先使用 interface 而非 type
- 禁止使用 any，使用 unknown 替代
```

### 文件位置与层级

项目的核心文件结构如下：

```
your-project/
├── CLAUDE.md                  # 项目主记忆文件（团队共享）
├── .claude/
│   ├── settings.json          # Hooks、权限、环境配置
│   ├── settings.local.json    # 个人配置（建议加入 .gitignore）
│   └── commands/              # 自定义斜杠命令
│       └── my-command.md
└── .mcp.json                  # MCP 服务配置
```

````

---

## <font style="color:rgb(51, 51, 51);">初始化后的最佳实践</font>
_**<font style="color:rgb(44, 58, 94);">迭代优化，而非一次写死。</font>**_

`**<font style="color:rgb(51, 51, 51);">/init</font>**`<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">命令适合快速入门，但真正的价值来自于随时间不断迭代，可以补充 Claude 无法自动推断的内容，例如分支命名规范、部署流程、Code Review 要求；同时删去不适用的通用建议。</font>

+ **<font style="color:rgb(51, 51, 51);">提交到版本控制</font>**<font style="color:rgb(51, 51, 51);">：将</font><font style="color:rgb(51, 51, 51);"> </font>`<font style="color:rgb(51, 51, 51);">CLAUDE.md</font>`<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">提交到 Git，这样整个团队都能从中受益，新成员可以通过让 Claude 解释代码库来快速上手。</font>
+ **<font style="color:rgb(51, 51, 51);">保持精简</font>**<font style="color:rgb(51, 51, 51);">：内容要简洁且普遍适用。采用"渐进式披露"原则——不要把所有你想让 Claude 知道的内容都塞进去，而是告诉它</font>**<font style="color:rgb(51, 51, 51);">如何查找重要信息</font>**<font style="color:rgb(51, 51, 51);">，让它按需获取，避免撑爆上下文窗口。</font>
+ **<font style="color:rgb(51, 51, 51);">不要让 CLAUDE.md 替代 linter</font>**<font style="color:rgb(51, 51, 51);">：在文件中写代码风格规范是最常见的误区之一。永远不要用 LLM 来做 linter 的工作——linter 更快、更便宜，而且是确定性的。代码风格约束只会让上下文窗口膨胀，降低 Claude 的指令遵从质量。</font>

---

## <font style="color:rgb(51, 51, 51);">使用</font><font style="color:rgb(51, 51, 51);"> </font>`<font style="color:rgb(51, 51, 51);">#</font>`<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">快捷键持续更新</font>
<font style="color:rgb(51, 51, 51);">在对话中，随时用</font><font style="color:rgb(51, 51, 51);"> </font>`<font style="color:rgb(51, 51, 51);">#</font>`<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">前缀给 Claude 发送记忆指令：</font>

```plain
# 我们始终使用 pnpm，不用 npm
# 所有组件必须包含单元测试
````

<font style="color:rgb(51, 51, 51);">这些补充会逐渐积累，形成一份真正反映团队实际工作方式的</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">CLAUDE.md</font></code><font style="color:rgb(51, 51, 51);">。</font>

***

## <font style="color:rgb(51, 51, 51);">验证初始化效果</font>

<font style="color:rgb(51, 51, 51);">初始化完成后，可以通过以下对话确认 Claude 是否正确理解了项目：</font>

* <font style="color:rgb(51, 51, 51);">这个项目是做什么的？</font>
* <font style="color:rgb(51, 51, 51);">解释一下目录结构。</font>
* <font style="color:rgb(51, 51, 51);">项目用了哪些技术？</font>
* <font style="color:rgb(51, 51, 51);">运行测试的命令是什么？</font>

<font style="color:rgb(51, 51, 51);"></font>

## <font style="color:rgb(51, 51, 51);">Claude Code 项目目录结构</font>

<font style="color:rgb(51, 51, 51);">一个典型的 Claude Code 项目目录结构如下：</font>

```plain
your-project/
├── CLAUDE.md                    ← 团队共享指令，提交到 git
├── CLAUDE.local.md              ← 个人覆盖，被 git 忽略
└── .claude/
    ├── settings.json            ← 权限 + 配置，提交到 git
    ├── settings.local.json      ← 个人权限，被 git 忽略
    ├── commands/                ← 自定义斜杠命令
    │   ├── review.md            →  /project:review
    │   ├── fix-issue.md         →  /project:fix-issue
    │   └── deploy.md            →  /project:deploy
    ├── rules/                   ← 模块化指令文件（全局生效）
    │   ├── code-style.md
    │   ├── testing.md
    │   └── api-conventions.md
    ├── skills/                  ← 自动调用的工作流
    │   ├── security-review/
    │   │   └── SKILL.md
    │   └── deploy/
    │       └── SKILL.md
    └── agents/                  ← 子代理角色定义
        ├── code-reviewer.md
        └── security-auditor.md
```

![1783648968229-de8c1a8e-fd24-4233-bbb1-35f941194f1f.png](./img/wf9R51v5S5sXlvV1/1783648968229-de8c1a8e-fd24-4233-bbb1-35f941194f1f-642771.png)

***

## <font style="color:rgb(51, 51, 51);">CLAUDE.md -- 项目核心指令</font>

### <font style="color:rgb(51, 51, 51);">CLAUDE.md </font>

<font style="color:rgb(51, 51, 51);">这是 Claude 进入项目时</font>**<font style="color:rgb(51, 51, 51);">第一个读取</font>**<font style="color:rgb(51, 51, 51);">的文件，相当于项目欢迎手册。</font>

<font style="color:rgb(51, 51, 51);">CLAUDE.md 放置在项目根目录，所有团队成员共享，它告诉 Claude：这个项目是什么、如何运行、有什么约定。</font>

**<font style="color:rgb(51, 51, 51);">典型内容：</font>**

```plain
# My Project

一句话描述项目用途。

## Tech Stack
- Backend: Python / FastAPI
- Frontend: React + TypeScript
- Database: PostgreSQL

## Common Commands
\`npm run dev\`    # 启动开发服务器
\`pytest tests/\`  # 运行测试
\`npm run build\`  # 构建生产版本

## Code Conventions
- 使用 snake_case 命名变量
- 所有 API 需要写单元测试
- PR 合并前必须通过 CI

## Architecture Overview
src/
├── api/        # FastAPI 路由层
├── services/   # 业务逻辑层
└── models/     # 数据模型层
```

***<font style="color:rgb(44, 58, 94);">💡</font>****__<font style="color:rgb(44, 58, 94);"> 提示：</font>__**<font style="color:rgb(44, 58, 94);"> </font>\_\_<font style="color:rgb(44, 58, 94);">Claude 会自动递归读取父目录中的 CLAUDE.md。在 monorepo 中，子包内可再放一个 CLAUDE.md，Claude 会将两层指令合并理解。</font>*

### <font style="color:rgb(51, 51, 51);">CLAUDE.local.md</font>

<font style="color:rgb(51, 51, 51);">个人专属的覆盖层，叠加在 CLAUDE.md 之上。</font>

<font style="color:rgb(51, 51, 51);">CLAUDE.local.md 存放只与你本人相关的偏好或临时指令，不应共享给团队。</font>

<font style="color:rgb(51, 51, 51);">典型内容：</font>

```plain
# 我的本地覆盖

本地数据库地址：localhost:5433（非默认端口）

调试时请优先输出详细日志。

## 临时规则（本次任务用）
目前专注于重构 auth/ 模块，其他模块暂时不要改动。
```

![1783648963983-0a0a5af2-c866-4d3c-9fb4-630204faf2fd.svg](./img/wf9R51v5S5sXlvV1/1783648963983-0a0a5af2-c866-4d3c-9fb4-630204faf2fd-539747.svg)

***

## <code><font style="color:rgb(51, 51, 51);">.claude/settings.json</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">-- 权限与配置中心</font>

### <font style="color:rgb(51, 51, 51);">settings.json</font>

<font style="color:rgb(51, 51, 51);">团队共享的配置文件，控制 Claude</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:rgb(51, 51, 51);">允许或禁止</font>**<font style="color:rgb(51, 51, 51);">执行哪些操作，作为团队安全基线。</font>

```plain
{
  "permissions": {
    "allow": [
      "Bash(npm run *)",
      "Bash(pytest:*)",
      "Bash(git diff:*)",
      "Bash(git log:*)"
    ],
    "deny": [
      "Bash(rm -rf *)",
      "Bash(curl * | bash)"
    ]
  }
}
```

### <font style="color:rgb(51, 51, 51);">settings.local.json</font>

<font style="color:rgb(51, 51, 51);">个人本地权限覆盖，临时放开或收紧某些权限，不影响团队其他成员。</font>

```plain
{
  "permissions": {
    "allow": [
      "Bash(rm ./tmp/*)"
    ]
  }
}
```

![1783648963930-e292f2fa-6ad1-4afb-858a-09ad71d8db00.svg](./img/wf9R51v5S5sXlvV1/1783648963930-e292f2fa-6ad1-4afb-858a-09ad71d8db00-684234.svg)

***

## <code><font style="color:rgb(51, 51, 51);">.claude/commands/</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">-- 自定义斜杠命令</font>

<font style="color:rgb(51, 51, 51);">目录下每个</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">.md</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">文件自动映射为一条</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">/project:文件名</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">命令。</font>

<code><font style="color:rgb(51, 51, 51);">.claude/commands/</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">是团队将重复性任务</font>**<font style="color:rgb(51, 51, 51);">标准化</font>**<font style="color:rgb(51, 51, 51);">的核心机制。</font>

| <font style="color:rgb(255, 255, 255);">文件名</font> | <font style="color:rgb(255, 255, 255);">对应命令</font> |
| --- | --- |
| <code><font style="color:rgb(51, 51, 51);">review.md</font></code> | <code><font style="color:rgb(51, 51, 51);">/project:review</font></code> |
| <code><font style="color:rgb(51, 51, 51);">fix-issue.md</font></code> | <code><font style="color:rgb(51, 51, 51);">/project:fix-issue</font></code> |
| <code><font style="color:rgb(51, 51, 51);">deploy.md</font></code> | <code><font style="color:rgb(51, 51, 51);">/project:deploy</font></code> |

### <font style="color:rgb(51, 51, 51);">示例：</font><code><font style="color:rgb(51, 51, 51);">commands/review.md</font></code>

```plain
# Code Review

请对当前修改执行完整的代码审查：

1. 检查是否有安全漏洞（SQL 注入、XSS 等）
2. 验证错误处理是否完整
3. 确认测试覆盖率是否达标
4. 检查是否符合代码风格规范
5. 评估性能影响

用中文输出结构化审查报告，按严重程度排列问题。
```

### <font style="color:rgb(51, 51, 51);">示例：</font><code><font style="color:rgb(51, 51, 51);">commands/fix-issue.md</font></code><font style="color:rgb(51, 51, 51);">（带参数）</font>

```plain
# Fix GitHub Issue

给定 Issue 编号 $ARGUMENTS，请：

1. 读取并理解 Issue 描述
2. 定位相关代码文件
3. 实现最小化修复方案
4. 编写对应的单元测试
5. 更新 CHANGELOG.md

调用方式：/project:fix-issue 123
```

***<font style="color:rgb(44, 58, 94);">💡</font>****__<font style="color:rgb(44, 58, 94);"> 参数传递：</font>__**<font style="color:rgb(44, 58, 94);"> </font>**<font style="color:rgb(44, 58, 94);">命令文件中可使用</font>**<font style="color:rgb(44, 58, 94);"> </font>*<code>_<font style="color:rgb(44, 58, 94);">$ARGUMENTS</font>_</code>*<font style="color:rgb(44, 58, 94);"> </font>\_\_<font style="color:rgb(44, 58, 94);">占位符接收调用时传入的参数。</font>*

![1783648964037-de0c00ac-dccd-43af-8cda-aa6e124fa68f.svg](./img/wf9R51v5S5sXlvV1/1783648964037-de0c00ac-dccd-43af-8cda-aa6e124fa68f-215589.svg)

***

## <code><font style="color:rgb(51, 51, 51);">.claude/rules/</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">-- 模块化行为规则</font>

<font style="color:rgb(51, 51, 51);">将 CLAUDE.md 中的规则</font>**<font style="color:rgb(51, 51, 51);">拆分模块化</font>**<font style="color:rgb(51, 51, 51);">存放，Claude 在整个会话中始终遵守。适合存放长期稳定执行的行为约定，避免 CLAUDE.md 过于臃肿。</font>

### <font style="color:rgb(51, 51, 51);">示例：</font><code><font style="color:rgb(51, 51, 51);">rules/code-style.md</font></code>

```plain
# Code Style Rules

- TypeScript 严格模式，禁用 any 类型
- 函数长度不超过 40 行，超出则拆分
- 优先使用 const，避免使用 let
- 导入顺序：标准库 → 三方包 → 本地模块
- 所有 export 的函数/类型需要 JSDoc 注释
- 禁止使用 console.log，使用项目 logger
```

### <font style="color:rgb(51, 51, 51);">示例：</font><code><font style="color:rgb(51, 51, 51);">rules/testing.md</font></code>

```plain
# Code Style Rules

- TypeScript 严格模式，禁用 any 类型
- 函数长度不超过 40 行，超出则拆分
- 优先使用 const，避免使用 let
- 导入顺序：标准库 → 三方包 → 本地模块
- 所有 export 的函数/类型需要 JSDoc 注释
- 禁止使用 console.log，使用项目 logger
```

### <font style="color:rgb(51, 51, 51);">示例：</font><code><font style="color:rgb(51, 51, 51);">rules/api-conventions.md</font></code>

```plain
# API Conventions

- RESTful 风格，资源名使用复数形式
- 统一响应格式：{ data, error, meta }
- 错误码遵循 HTTP 标准语义
- 所有接口需要在 OpenAPI 文档中声明
- 分页参数统一使用 page / page_size
```

![1783648964116-3755dcc2-4d7d-476c-872f-dcff62e5ebc6.svg](./img/wf9R51v5S5sXlvV1/1783648964116-3755dcc2-4d7d-476c-872f-dcff62e5ebc6-425183.svg)

***

## <code><font style="color:rgb(51, 51, 51);">.claude/skills/</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">-- 自动调用的工作流</font>

<font style="color:rgb(51, 51, 51);">Skills 是更高级的</font>**<font style="color:rgb(51, 51, 51);">复合工作流</font>**<font style="color:rgb(51, 51, 51);">。当 Claude 判断某个任务适合某个 skill 时，会自动读取并执行对应的 SKILL.md，</font>**<font style="color:rgb(51, 51, 51);">无需手动调用</font>**<font style="color:rgb(51, 51, 51);">。</font>

<font style="color:rgb(51, 51, 51);">每个 skill 是一个子目录，目录内包含</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">SKILL.md</font></code><font style="color:rgb(51, 51, 51);">。</font>

### <font style="color:rgb(51, 51, 51);">示例：</font><code><font style="color:rgb(51, 51, 51);">skills/security-review/SKILL.md</font></code>

```plain
# Security Review Skill

## 触发条件
当用户请求代码审查、代码涉及认证/授权/加密/用户输入处理时自动触发。

## 执行步骤
1. 扫描 SQL 注入风险（检查所有数据库查询）
2. 检查 XSS 防护（验证输出转义）
3. 审计权限边界（确认最小权限原则）
4. 检查敏感数据处理（日志、错误信息中是否泄露）
5. 输出 OWASP Top 10 对照检查表

## 输出格式
按 CVSS 评分排列，高危问题优先展示。
```

***<font style="color:rgb(44, 58, 94);">⚡</font>**\_\_**<font style="color:rgb(44, 58, 94);"> Skills vs Commands 的区别：</font>***

* **<font style="color:rgb(44, 58, 94);">Commands</font>**<font style="color:rgb(44, 58, 94);"> </font><font style="color:rgb(44, 58, 94);">需要用户主动输入斜杠命令触发，是"工具箱"</font>
* **<font style="color:rgb(44, 58, 94);">Skills</font>**<font style="color:rgb(44, 58, 94);"> </font><font style="color:rgb(44, 58, 94);">由 Claude 根据上下文自动判断是否调用，是"智能本能"</font>

![1783648964876-09b1e6c7-8e9e-437e-a6bc-59ec89181467.svg](./img/wf9R51v5S5sXlvV1/1783648964876-09b1e6c7-8e9e-437e-a6bc-59ec89181467-177725.svg)

***

## <code><font style="color:rgb(51, 51, 51);">.claude/agents/</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">-- 子代理角色</font>

<font style="color:rgb(51, 51, 51);">定义可被主 Claude 实例</font>**<font style="color:rgb(51, 51, 51);">派遣的专业子代理</font>**<font style="color:rgb(51, 51, 51);">。在复杂任务中，主代理将子任务委派给对应专家角色，实现</font>**<font style="color:rgb(51, 51, 51);">多代理协作</font>**<font style="color:rgb(51, 51, 51);">。子代理在隔离上下文中运行，拥有独立的权限范围。</font>

### <font style="color:rgb(51, 51, 51);">示例：</font><code><font style="color:rgb(51, 51, 51);">agents/code-reviewer.md</font></code>

```plain
---
name: code-reviewer
description: 资深代码审查员，专注代码质量与可维护性
---

# 代码审查员

## 角色定位
你是一名拥有 10 年经验的资深工程师，专注于代码可读性、性能优化和最佳实践。

## 审查重点
- 命名是否清晰表达意图
- 函数/类的单一职责原则
- 边界条件和错误处理
- 性能瓶颈（N+1 查询、不必要的循环等）

## 权限
只读访问，不直接修改文件。

## 输出格式
使用 Markdown 表格输出，包含：问题位置、严重程度、建议方案。
```

### <font style="color:rgb(51, 51, 51);">示例：</font><code><font style="color:rgb(51, 51, 51);">agents/security-auditor.md</font></code>

```plain
---
name: security-auditor
description: 安全审计专家，专注漏洞扫描与合规审计
---

# 安全审计员

## 角色定位
你是一名安全工程师，熟悉 OWASP、CVE 数据库和常见攻击向量。

## 审计范围
- 认证与授权逻辑
- 输入验证与输出转义
- 依赖包已知漏洞（结合 npm audit / pip audit）
- 敏感信息泄露风险

## 权限
只读访问 + 可运行安全扫描工具。

## 输出格式
按 CVSS 3.1 评分排列，包含：漏洞描述、影响范围、修复建议、参考链接。
```

![1783648964965-b7960cf3-1b45-4ffc-bc39-88e0f6cb2964.svg](./img/wf9R51v5S5sXlvV1/1783648964965-b7960cf3-1b45-4ffc-bc39-88e0f6cb2964-844589.svg)

***

## <font style="color:rgb(51, 51, 51);">速查表</font>

| <font style="color:rgb(255, 255, 255);">文件 / 目录</font> | <font style="color:rgb(255, 255, 255);">提交 Git</font> | <font style="color:rgb(255, 255, 255);">触发方式</font> | <font style="color:rgb(255, 255, 255);">核心用途</font> |
| --- | --- | --- | --- |
| <code><font style="color:rgb(51, 51, 51);">CLAUDE.md</font></code> | <font style="color:rgb(51, 51, 51);">✅</font><font style="color:rgb(51, 51, 51);"> 是</font> | <font style="color:rgb(51, 51, 51);">自动（启动时）</font> | <font style="color:rgb(51, 51, 51);">项目基础指令与约定</font> |
| <code><font style="color:rgb(51, 51, 51);">CLAUDE.local.md</font></code> | <font style="color:rgb(51, 51, 51);">❌</font><font style="color:rgb(51, 51, 51);"> 否</font> | <font style="color:rgb(51, 51, 51);">自动（启动时）</font> | <font style="color:rgb(51, 51, 51);">个人覆盖、临时指令</font> |
| <code><font style="color:rgb(51, 51, 51);">.claude/settings.json</font></code> | <font style="color:rgb(51, 51, 51);">✅</font><font style="color:rgb(51, 51, 51);"> 是</font> | <font style="color:rgb(51, 51, 51);">自动（启动时）</font> | <font style="color:rgb(51, 51, 51);">团队权限基线</font> |
| <code><font style="color:rgb(51, 51, 51);">.claude/settings.local.json</font></code> | <font style="color:rgb(51, 51, 51);">❌</font><font style="color:rgb(51, 51, 51);"> 否</font> | <font style="color:rgb(51, 51, 51);">自动（启动时）</font> | <font style="color:rgb(51, 51, 51);">个人权限覆盖</font> |
| <code><font style="color:rgb(51, 51, 51);">.claude/commands/*.md</font></code> | <font style="color:rgb(51, 51, 51);">✅</font><font style="color:rgb(51, 51, 51);"> 是</font> | <font style="color:rgb(51, 51, 51);">手动（</font><code><font style="color:rgb(51, 51, 51);">/project:xxx</font></code><br/><font style="color:rgb(51, 51, 51);">）</font> | <font style="color:rgb(51, 51, 51);">可复用的标准化流程</font> |
| <code><font style="color:rgb(51, 51, 51);">.claude/rules/*.md</font></code> | <font style="color:rgb(51, 51, 51);">✅</font><font style="color:rgb(51, 51, 51);"> 是</font> | <font style="color:rgb(51, 51, 51);">自动（全局生效）</font> | <font style="color:rgb(51, 51, 51);">模块化行为规范</font> |
| <code><font style="color:rgb(51, 51, 51);">.claude/skills/*/SKILL.md</font></code> | <font style="color:rgb(51, 51, 51);">✅</font><font style="color:rgb(51, 51, 51);"> 是</font> | <font style="color:rgb(51, 51, 51);">自动（Claude 判断）</font> | <font style="color:rgb(51, 51, 51);">智能复合工作流</font> |
| <code><font style="color:rgb(51, 51, 51);">.claude/agents/*.md</font></code> | <font style="color:rgb(51, 51, 51);">✅</font><font style="color:rgb(51, 51, 51);"> 是</font> | <font style="color:rgb(51, 51, 51);">自动（主代理派遣）</font> | <font style="color:rgb(51, 51, 51);">专业子代理角色定义</font> |

![1783648965902-c5789c48-9cd7-44ed-a63c-8ff8b8337a4d.png](./img/wf9R51v5S5sXlvV1/1783648965902-c5789c48-9cd7-44ed-a63c-8ff8b8337a4d-674116.png)

***

## <font style="color:rgb(51, 51, 51);">最佳实践建议</font>

**<font style="color:rgb(51, 51, 51);">从最小可行配置开始：</font>**

```plain
your-project/
├── CLAUDE.md        # 先从这里开始
└── .claude/
    └── settings.json    # 配置基本权限
```

<font style="color:rgb(51, 51, 51);">随着项目发展，再逐步引入：</font>

1. <code><font style="color:rgb(51, 51, 51);">commands/</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">— 当你发现自己重复输入相同的指令时</font>
2. <code><font style="color:rgb(51, 51, 51);">rules/</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">— 当 CLAUDE.md 超过 100 行时，拆分模块</font>
3. <code><font style="color:rgb(51, 51, 51);">skills/</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">— 当有复杂的多步骤工作流需要标准化时</font>
4. <code><font style="color:rgb(51, 51, 51);">agents/</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">— 当任务复杂到需要多个专业视角并行时</font>

***<font style="color:rgb(44, 58, 94);">原则：</font>**\_\_<font style="color:rgb(44, 58, 94);"> "够用"胜过"完美"。不要一开始就构建复杂的多代理系统，在真正需要时再引入。</font>*

# Claude Code 上下文管理与权限可控性治理

## <font style="color:rgb(51, 51, 51);">Claude Code 上下文管理</font>

<font style="color:rgb(51, 51, 51);">上下文管理是高效使用 Claude Code 的核心技能。</font>

<font style="color:rgb(51, 51, 51);">官方文档明确指出：</font>**<font style="color:rgb(51, 51, 51);">上下文窗口是 Claude Code 最重要的资源</font>**<font style="color:rgb(51, 51, 51);">，随着上下文填满，模型性能会逐渐下降（称为上下文衰退，context rot）——这是使用 Claude Code 时需要主动对抗的核心问题。</font>

<font style="color:rgb(51, 51, 51);">本章深入讲解如何通过 CLAUDE.md 指令文件、自动记忆系统、上下文窗口优化命令等手段，让 Claude 在长会话和跨会话中保持高效状态。</font>

***

## <font style="color:rgb(51, 51, 51);">上下文窗口基础</font>

### <font style="color:rgb(51, 51, 51);">1、上下文窗口包含什么</font>

<font style="color:rgb(51, 51, 51);">Claude Code 的上下文窗口大小为</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:rgb(51, 51, 51);">1,000,000 tokens（100 万 token）</font>**<font style="color:rgb(51, 51, 51);">。它容纳了 Claude 在当前会话中"看到"的一切内容：</font>

| <font style="color:rgb(255, 255, 255);">内容来源</font> | <font style="color:rgb(255, 255, 255);">加载时机</font> | <font style="color:rgb(255, 255, 255);">Token 占用</font> |
| --- | --- | --- |
| <font style="color:rgb(51, 51, 51);">系统提示词（Claude Code 行为规范）</font> | <font style="color:rgb(51, 51, 51);">每次会话启动</font> | <font style="color:rgb(51, 51, 51);">固定占用</font> |
| <font style="color:rgb(51, 51, 51);">CLAUDE.md 文件</font> | <font style="color:rgb(51, 51, 51);">启动时完整加载</font> | <font style="color:rgb(51, 51, 51);">取决于文件大小</font> |
| <font style="color:rgb(51, 51, 51);">自动记忆（Auto memory）</font> | <font style="color:rgb(51, 51, 51);">启动时加载（前 200 行或 25KB）</font> | <font style="color:rgb(51, 51, 51);">有上限</font> |
| <font style="color:rgb(51, 51, 51);">对话历史</font> | <font style="color:rgb(51, 51, 51);">累积增长</font> | <font style="color:rgb(51, 51, 51);">随会话持续增加</font> |
| <font style="color:rgb(51, 51, 51);">工具结果（文件读取、命令输出等）</font> | <font style="color:rgb(51, 51, 51);">每次工具调用后追加</font> | <font style="color:rgb(51, 51, 51);">日志/大文件消耗极快</font> |
| <font style="color:rgb(51, 51, 51);">MCP 工具名称、Skills 描述等</font> | <font style="color:rgb(51, 51, 51);">启动时加载</font> | <font style="color:rgb(51, 51, 51);">中等</font> |

### <font style="color:rgb(51, 51, 51);">2、上下文衰退（Context rot）</font>

<font style="color:rgb(51, 51, 51);">官方明确指出：随着上下文填满，</font>**<font style="color:rgb(51, 51, 51);">LLM 性能会下降</font>**<font style="color:rgb(51, 51, 51);">，因为注意力被分散到更多 token 上，旧的、不相关的内容开始干扰当前任务。具体症状包括：</font>

* <font style="color:rgb(51, 51, 51);">Claude 开始前后矛盾，忘记之前达成的决策</font>
* <font style="color:rgb(51, 51, 51);">响应变得模糊、笼统，细节减少</font>
* <font style="color:rgb(51, 51, 51);">对同一问题反复询问已经回答过的内容</font>
* <font style="color:rgb(51, 51, 51);">在同一个会话里对同一个问题纠正了两次以上</font>

<font style="color:rgb(51, 51, 51);">出现以上症状说明上下文已经"污染"，此时应主动使用</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">/compact</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">或</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">/clear</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">处理，而不是继续在同一会话中纠正。</font>

<font style="color:rgb(51, 51, 51);">使用</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">/context</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">命令可以随时查看当前上下文的详细用量分析：</font>

/context

<font style="color:rgb(51, 51, 51);">它会按分类（系统提示、CLAUDE.md、记忆文件、会话历史等）列出 token 占用，并给出优化建议。建议在开始重要任务前先检查一次。</font>

***

## <font style="color:rgb(51, 51, 51);">CLAUDE.md 指令文件</font>

<font style="color:rgb(51, 51, 51);">CLAUDE.md 是 Claude Code 中记录静态指令和项目规范的核心文件。每次会话启动时，Claude 会自动将其加载到上下文窗口中。</font>

### <font style="color:rgb(51, 51, 51);">1、存放位置与作用范围</font>

<font style="color:rgb(51, 51, 51);">CLAUDE.md 支持多个位置，</font>**<font style="color:rgb(51, 51, 51);">更具体的位置优先级更高</font>**<font style="color:rgb(51, 51, 51);">：</font>

| <font style="color:rgb(255, 255, 255);">范围</font> | <font style="color:rgb(255, 255, 255);">文件路径</font> | <font style="color:rgb(255, 255, 255);">适用场景</font> | <font style="color:rgb(255, 255, 255);">是否提交 git</font> |
| --- | --- | --- | --- |
| **<font style="color:rgb(51, 51, 51);">组织级</font>** | <font style="color:rgb(51, 51, 51);">macOS:</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">/Library/Application Support/ClaudeCode/CLAUDE.md</font></code><br/><font style="color:rgb(51, 51, 51);">   </font><font style="color:rgb(51, 51, 51);">Linux/WSL:</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">/etc/claude-code/CLAUDE.md</font></code> | <font style="color:rgb(51, 51, 51);">公司编码标准、合规要求</font> | <font style="color:rgb(51, 51, 51);">由 IT 统一管理</font> |
| **<font style="color:rgb(51, 51, 51);">项目级</font>** | <code><font style="color:rgb(51, 51, 51);">./CLAUDE.md</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">或</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">./.claude/CLAUDE.md</font></code> | <font style="color:rgb(51, 51, 51);">项目架构、编码规范、工作流</font> | <font style="color:rgb(51, 51, 51);">是，与团队共享</font> |
| **<font style="color:rgb(51, 51, 51);">用户级</font>** | <code><font style="color:rgb(51, 51, 51);">~/.claude/CLAUDE.md</font></code> | <font style="color:rgb(51, 51, 51);">个人编码偏好，适用所有项目</font> | <font style="color:rgb(51, 51, 51);">否，个人私有</font> |
| **<font style="color:rgb(51, 51, 51);">本地私有</font>** | <code><font style="color:rgb(51, 51, 51);">./CLAUDE.local.md</font></code><br/><font style="color:rgb(51, 51, 51);">（加入 .gitignore）</font> | <font style="color:rgb(51, 51, 51);">个人的项目特定配置，不提交 git</font> | <font style="color:rgb(51, 51, 51);">否，加入 .gitignore</font> |

<code>_<font style="color:rgb(44, 58, 94);">CLAUDE.local.md</font>_</code>*<font style="color:rgb(44, 58, 94);"> </font>**<font style="color:rgb(44, 58, 94);">是个人私有配置的官方推荐方式：沙箱 URL、本地测试账号、个人调试习惯等不应共享的内容，应放在这里而不是</font>**<font style="color:rgb(44, 58, 94);"> </font>*<code>_<font style="color:rgb(44, 58, 94);">CLAUDE.md</font>_</code>*<font style="color:rgb(44, 58, 94);"> </font>**<font style="color:rgb(44, 58, 94);">中。运行</font>**<font style="color:rgb(44, 58, 94);"> </font>*<code>_<font style="color:rgb(44, 58, 94);">/init</font>_</code>*<font style="color:rgb(44, 58, 94);"> </font>**<font style="color:rgb(44, 58, 94);">时选择"个人"选项，它会自动将该文件加入</font>**<font style="color:rgb(44, 58, 94);"> </font>*<code>_<font style="color:rgb(44, 58, 94);">.gitignore</font>_</code>*<font style="color:rgb(44, 58, 94);">。</font>*

### <font style="color:rgb(51, 51, 51);">2、创建 CLAUDE.md</font>

<font style="color:rgb(51, 51, 51);">执行以下命令，Claude 会自动分析项目并生成初始 CLAUDE.md：</font>

/init

<font style="color:rgb(51, 51, 51);">如果已有 CLAUDE.md，</font><code><font style="color:rgb(51, 51, 51);">/init</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">会建议改进而不是直接覆盖。生成后，手动补充 Claude 无法自动发现的内容（如禁止修改的文件、特殊约束等）。</font>

<font style="color:rgb(51, 51, 51);">也可以在会话中用</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">#</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">快捷键快速向 CLAUDE.md 追加一条记忆：</font>

# 所有 API 错误响应必须使用 { code, message } 格式

<font style="color:rgb(51, 51, 51);">按下</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">#</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">后输入内容回车，Claude 会将其写入对应层级的 CLAUDE.md，作为持久指令保存。</font>

### <font style="color:rgb(51, 51, 51);">3、CLAUDE.md 内容要求</font>

<font style="color:rgb(51, 51, 51);">官方要求每个 CLAUDE.md 文件</font>**<font style="color:rgb(51, 51, 51);">控制在 200 行以内</font>**<font style="color:rgb(51, 51, 51);">。文件越大，消耗的启动 token 越多，Claude 的遵守率反而越低。以下是内容建议：</font>

**<font style="color:rgb(51, 51, 51);">应该写入：</font>**

* <font style="color:rgb(51, 51, 51);">构建、测试、部署的常用命令</font>
* <font style="color:rgb(51, 51, 51);">代码规范：命名约定、缩进、禁止使用的模式</font>
* <font style="color:rgb(51, 51, 51);">关键约束："始终使用 pnpm"、"禁止修改 migrations/ 目录"</font>
* <font style="color:rgb(51, 51, 51);">项目架构说明：主要目录的用途</font>

**<font style="color:rgb(51, 51, 51);">不应该写入：</font>**

* <font style="color:rgb(51, 51, 51);">多步骤操作流程（应放到 Skills 文件中）</font>
* <font style="color:rgb(51, 51, 51);">只与代码库某一部分相关的规则（应使用</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">.claude/rules/</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">按路径限定）</font>
* <font style="color:rgb(51, 51, 51);">Claude 通过读取代码就能自己发现的信息</font>

## <font style="color:rgb(97, 127, 16);">实例</font>

<font style="color:rgb(51, 51, 51);"># CLAUDE.md 示例（精简具体，每个文件控制在 200 行以内）

</font><font style="color:rgb(51, 51, 51);">## 常用命令\
</font><font style="color:rgb(51, 51, 51);">- 包管理：始终使用 pnpm，不要使用 npm 或 yarn\
</font><font style="color:rgb(51, 51, 51);">- 运行测试：pnpm test:watch\
</font><font style="color:rgb(51, 51, 51);">- 构建：pnpm build

</font><font style="color:rgb(51, 51, 51);">## 代码规范\
</font><font style="color:rgb(51, 51, 51);">- TypeScript strict 模式，不允许 any\
</font><font style="color:rgb(51, 51, 51);">- 组件文件使用 PascalCase 命名（如 UserProfile.tsx）\
</font><font style="color:rgb(51, 51, 51);">- 数据库时间戳统一使用 UTC 格式

</font><font style="color:rgb(51, 51, 51);">## 约束事项\
</font><font style="color:rgb(51, 51, 51);">- 禁止直接修改 prisma/migrations/ 目录下的已有文件\
</font><font style="color:rgb(51, 51, 51);">- .env.local 包含真实密钥，禁止读取或输出文件内容\
</font><font style="color:rgb(51, 51, 51);">- API 接口统一在 src/api/ 目录下管理，不在其他地方直接发请求</font>

### <font style="color:rgb(51, 51, 51);">4、按路径限定规则（.claude/rules/）</font>

<font style="color:rgb(51, 51, 51);">对于较大的项目，可以用</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">.claude/rules/</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">目录将指令拆分为按文件路径生效的细粒度规则，避免所有规则都堆在根 CLAUDE.md 中消耗启动 token：</font>

```plain
.claude/
└── rules/
    ├── api.md         # 只对 src/api/**/*.ts 文件生效
    ├── frontend.md    # 只对 src/components/**/*.tsx 文件生效
    └── testing.md     # 只对 *.test.ts 文件生效
```

<font style="color:rgb(51, 51, 51);">路径限定规则只在 Claude 读取对应目录下的文件时才会加载，不在启动时全量占用上下文。</font>

***

## <font style="color:rgb(51, 51, 51);">自动记忆（Auto memory）</font>

<font style="color:rgb(51, 51, 51);">自动记忆是 Claude Code v2.1.59 及以上版本内置的跨会话记忆系统，</font>**<font style="color:rgb(51, 51, 51);">默认开启</font>**<font style="color:rgb(51, 51, 51);">，无需任何配置。它让 Claude 在工作过程中自主记录发现的构建命令、调试经验、代码风格偏好等信息。</font>

### <font style="color:rgb(51, 51, 51);">1、工作机制</font>

* <font style="color:rgb(51, 51, 51);">Claude 不会每次会话都写记忆，它会判断信息是否值得保留（在未来对话中是否有用）</font>
* <font style="color:rgb(51, 51, 51);">记忆按 git 仓库路径隔离，存储于</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">~/.claude/projects/<项目路径>/memory/</font></code>
* <font style="color:rgb(51, 51, 51);">同一仓库的所有工作树共享一份自动记忆</font>
* <font style="color:rgb(51, 51, 51);">写入记忆时，终端会显示 "Writing memory"；下次检索时显示 "Recalled memory"</font>

### <font style="color:rgb(51, 51, 51);">2、查看与编辑记忆（/memory）</font>

<font style="color:rgb(51, 51, 51);">使用</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">/memory</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">命令查看和编辑所有记忆内容，包括各级 CLAUDE.md 和自动记忆：</font>

/memory

<font style="color:rgb(51, 51, 51);">在编辑器中可以删除不准确的条目，或使用 Auto memory 开关禁用自动记忆功能。也可以通过环境变量临时禁用：</font>

CLAUDE_CODE_DISABLE_AUTO_MEMORY=1 claude

### <font style="color:rgb(51, 51, 51);">3、主动让 Claude 记住内容</font>

<font style="color:rgb(51, 51, 51);">对话中可以直接让 Claude 写入记忆：</font>

记住：我们的 API 测试需要本地运行一个 Redis 实例以后请记住：处理错误时，统一返回 { code, message } 结构

<font style="color:rgb(51, 51, 51);">如果想升级为强制规范而非只是偏好记忆，可以说："把这条规则写进 CLAUDE.md"，Claude 会将其写入对应的 CLAUDE.md 文件。</font>

***

## <font style="color:rgb(51, 51, 51);">上下文窗口优化命令</font>

### <font style="color:rgb(51, 51, 51);">1、自动压缩（Auto-compaction）</font>

<font style="color:rgb(51, 51, 51);">Claude Code 在</font>**<font style="color:rgb(51, 51, 51);">上下文接近限制时会自动触发压缩</font>**<font style="color:rgb(51, 51, 51);">（约在 75% 用量左右），将对话历史总结为摘要后继续工作。但官方建议不要等待自动压缩，应</font>**<font style="color:rgb(51, 51, 51);">主动在 60~70% 时手动触发</font>**<font style="color:rgb(51, 51, 51);">，避免在关键任务中间被打断，且主动压缩可以通过指令控制保留哪些内容。</font>

### <font style="color:rgb(51, 51, 51);">2、压缩上下文（/compact）</font>

<font style="color:rgb(51, 51, 51);">手动压缩对话历史，将长会话总结为精简摘要继续工作：</font>

/compact

<code><font style="color:rgb(51, 51, 51);">/compact</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">支持传入自定义指令，控制压缩时重点保留哪些内容：</font>

/compact Focus on the API changes/compact 保留认证流程的架构决策，丢弃调试过程中的无效尝试

*<font style="color:rgb(44, 58, 94);">压缩是有损操作。压缩时 Claude 处于上下文最满、性能最弱的状态，如果不给指令，它可能丢掉你认为重要的内容。</font>**__<font style="color:rgb(44, 58, 94);">在重大决策后立即主动压缩，并用指令说明保留重点</font>__**<font style="color:rgb(44, 58, 94);">，比等待自动压缩效果好得多。</font>*

### <font style="color:rgb(51, 51, 51);">3、清除上下文（/clear）</font>

<font style="color:rgb(51, 51, 51);">切换到全新任务时清除所有对话历史：</font>

/clear

<font style="color:rgb(51, 51, 51);">清除后 CLAUDE.md 和自动记忆不受影响，仍会在新会话中加载。官方建议：</font>**<font style="color:rgb(51, 51, 51);">如果在同一会话里对同一问题纠正了两次以上，不如直接 /clear，带着学到的约束重新开始一个更精准的提示词</font>**<font style="color:rgb(51, 51, 51);">——干净的会话加上更好的提示，几乎总是好过在污染的上下文中继续纠正。</font>

### <font style="color:rgb(51, 51, 51);">4、回退到检查点（/rewind）</font>

<font style="color:rgb(51, 51, 51);">Claude Code 在每次修改文件前会自动创建检查点。双击</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">Esc</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">或执行</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">/rewind</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">可打开回退菜单，选择要恢复的检查点：</font>

/rewind（或双击 Esc 键）

<font style="color:rgb(51, 51, 51);">在回退菜单中，你可以选择以下操作：</font>

| <font style="color:rgb(255, 255, 255);">操作</font> | <font style="color:rgb(255, 255, 255);">效果</font> | <font style="color:rgb(255, 255, 255);">适用场景</font> |
| --- | --- | --- |
| **<font style="color:rgb(51, 51, 51);">恢复对话 + 代码</font>** | <font style="color:rgb(51, 51, 51);">回退对话历史和文件改动，完全还原</font> | <font style="color:rgb(51, 51, 51);">Claude 走偏了，改动有问题，全部撤销</font> |
| **<font style="color:rgb(51, 51, 51);">仅恢复对话</font>** | <font style="color:rgb(51, 51, 51);">回退对话历史，保留文件改动</font> | <font style="color:rgb(51, 51, 51);">想重试不同思路，但代码改动可以保留</font> |
| **<font style="color:rgb(51, 51, 51);">仅恢复代码</font>** | <font style="color:rgb(51, 51, 51);">还原文件到检查点状态，保留对话</font> | <font style="color:rgb(51, 51, 51);">代码改坏了，但对话中的分析有参考价值</font> |
| **<font style="color:rgb(51, 51, 51);">从此处摘要（Summarize from here）</font>** | <font style="color:rgb(51, 51, 51);">将该检查点之后的对话压缩为摘要，保留之前的完整历史</font> | <font style="color:rgb(51, 51, 51);">只想清理后半段冗余对话，保留前期的完整上下文</font> |

*<font style="color:rgb(44, 58, 94);">检查点跨会话持久保存——关闭终端后仍然可以回退到之前的检查点。这不是 git 的替代品，但在探索性实验中比手动 git stash 更方便。</font>*

### <font style="color:rgb(51, 51, 51);">5、快速提问不污染上下文（/btw）</font>

<font style="color:rgb(51, 51, 51);">如果需要快速查询一个小细节，但不想让这次问答进入对话历史（消耗上下文），使用</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">/btw</font></code><font style="color:rgb(51, 51, 51);">：</font>

/btw 这个项目的 TypeScript 版本是多少？

<font style="color:rgb(51, 51, 51);">答案会以浮层方式展示，问题和答案都不会进入对话历史，适合查阅配置、版本号等不需要保留的一次性信息。</font>

***

## <font style="color:rgb(51, 51, 51);">会话管理命令</font>

| <font style="color:rgb(255, 255, 255);">命令</font> | <font style="color:rgb(255, 255, 255);">功能</font> | <font style="color:rgb(255, 255, 255);">使用场景</font> |
| --- | --- | --- |
| <code><font style="color:rgb(51, 51, 51);">/context</font></code> | <font style="color:rgb(51, 51, 51);">查看上下文各部分的详细 token 用量分析</font> | <font style="color:rgb(51, 51, 51);">排查哪部分消耗了过多 token</font> |
| <code><font style="color:rgb(51, 51, 51);">/compact [指令]</font></code> | <font style="color:rgb(51, 51, 51);">压缩对话历史为摘要，可指定保留重点</font> | <font style="color:rgb(51, 51, 51);">上下文 60~70% 时主动压缩</font> |
| <code><font style="color:rgb(51, 51, 51);">/clear</font></code> | <font style="color:rgb(51, 51, 51);">清除所有对话历史，保留 CLAUDE.md 和记忆</font> | <font style="color:rgb(51, 51, 51);">切换到新任务，或上下文已严重污染</font> |
| <code><font style="color:rgb(51, 51, 51);">/rewind</font></code><br/><font style="color:rgb(51, 51, 51);">（或双击 Esc）</font> | <font style="color:rgb(51, 51, 51);">打开检查点菜单，可选择恢复对话/代码/两者，或从某处摘要</font> | <font style="color:rgb(51, 51, 51);">Claude 走偏了，需要回退后重试</font> |
| <code><font style="color:rgb(51, 51, 51);">/memory</font></code> | <font style="color:rgb(51, 51, 51);">查看和编辑 CLAUDE.md 及自动记忆内容</font> | <font style="color:rgb(51, 51, 51);">检查记忆是否准确，删除过时条目</font> |
| <code><font style="color:rgb(51, 51, 51);">/btw</font></code> | <font style="color:rgb(51, 51, 51);">快速提问，答案不进入对话历史</font> | <font style="color:rgb(51, 51, 51);">查阅小细节，不想污染上下文</font> |
| <code><font style="color:rgb(51, 51, 51);">/init</font></code> | <font style="color:rgb(51, 51, 51);">分析项目并生成或改进 CLAUDE.md</font> | <font style="color:rgb(51, 51, 51);">首次在新项目使用，或项目有重大变更</font> |
| <code><font style="color:rgb(51, 51, 51);">#</font></code><br/><font style="color:rgb(51, 51, 51);">（快捷键）</font> | <font style="color:rgb(51, 51, 51);">快速向 CLAUDE.md 添加一条持久指令</font> | <font style="color:rgb(51, 51, 51);">随时记录规范或约定</font> |
| <code><font style="color:rgb(51, 51, 51);">claude --continue</font></code> | <font style="color:rgb(51, 51, 51);">继续最近一次会话</font> | <font style="color:rgb(51, 51, 51);">重新打开终端后接着工作</font> |
| <code><font style="color:rgb(51, 51, 51);">claude --resume</font></code> | <font style="color:rgb(51, 51, 51);">从历史列表中选择一次会话继续</font> | <font style="color:rgb(51, 51, 51);">恢复几天前的某个特定任务</font> |

***

## <font style="color:rgb(51, 51, 51);">常见问题与解决方案</font>

**<font style="color:rgb(51, 51, 51);">问题一：Claude 没有遵守 CLAUDE.md 中的规则</font>**

* <font style="color:rgb(51, 51, 51);">检查 CLAUDE.md 是否过大（超过 200 行时遵守率下降）</font>
* <font style="color:rgb(51, 51, 51);">将模糊表述改为具体指令：不要"写整洁的代码"，要"使用 2 个空格缩进"</font>
* <font style="color:rgb(51, 51, 51);">用</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">/memory</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">检查是否有冲突的自动记忆条目</font>
* <font style="color:rgb(51, 51, 51);">考虑用</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">.claude/rules/</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">将规则按文件路径拆分，减少每次加载量</font>

**<font style="color:rgb(51, 51, 51);">问题二：Claude 开始前后矛盾，"忘记"之前的决策</font>**

* <font style="color:rgb(51, 51, 51);">这是上下文衰退的典型症状，不要继续在同一会话纠正</font>
* <font style="color:rgb(51, 51, 51);">运行</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">/compact 保留关键决策</font></code><font style="color:rgb(51, 51, 51);">，或直接</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">/clear</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">后带着总结重新开始</font>
* <font style="color:rgb(51, 51, 51);">重要结论用</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">#</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">快捷键写入 CLAUDE.md，确保下次会话仍然有效</font>

**<font style="color:rgb(51, 51, 51);">问题三：/compact 后关键信息丢失</font>**

* <font style="color:rgb(51, 51, 51);">压缩时传入具体指令：</font><code><font style="color:rgb(51, 51, 51);">/compact 保留认证流程的架构决策和已确认的 API 格式</font></code>
* <font style="color:rgb(51, 51, 51);">在压缩前将最重要的结论写入 CLAUDE.md</font>
* <font style="color:rgb(51, 51, 51);">调试失败的尝试不值得保留，可以更激进地压缩或 /clear</font>

**<font style="color:rgb(51, 51, 51);">问题四：关闭终端后如何继续上次工作</font>**

* <font style="color:rgb(51, 51, 51);">使用</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">claude --continue</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">继续最近一次会话</font>
* <font style="color:rgb(51, 51, 51);">使用</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">claude --resume</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">从历史列表选择特定会话</font>
* <font style="color:rgb(51, 51, 51);">用</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">/rename</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">给重要会话起一个描述性名称（如 "oauth-migration"），方便以后找到</font>

**<font style="color:rgb(51, 51, 51);">问题五：某个大任务会产生大量工具输出，怎么避免上下文爆满</font>**

* <font style="color:rgb(51, 51, 51);">使用子代理（subagent）委托执行：主对话只收到摘要，中间输出留在子代理独立上下文中</font>
* <font style="color:rgb(51, 51, 51);">例如：</font><code><font style="color:rgb(51, 51, 51);">使用子代理分析所有日志文件，找出性能瓶颈，只把结论告诉我</font></code>

<font style="color:rgb(51, 51, 51);"></font>

## <font style="color:rgb(51, 51, 51);">Claude Code 权限配置</font>

<font style="color:rgb(51, 51, 51);">Claude Code 使用分层权限系统来平衡功能和安全性，支持细粒度权限规则、权限模式和沙箱策略来控制 Claude 可以访问和执行的操作。合理配置权限，既能让 AI 高效完成任务，又能防止误操作破坏代码或泄露敏感文件。</font>

*<font style="color:rgb(44, 58, 94);">从 Claude Code v1.1.1 开始，推荐使用新的权限配置方式。旧的</font>\_\_<font style="color:rgb(44, 58, 94);"> </font>*<code>_<font style="color:rgb(44, 58, 94);">tools</font>_</code>*<font style="color:rgb(44, 58, 94);"> </font>\_\_<font style="color:rgb(44, 58, 94);">布尔配置仍被支持，但建议迁移到新的权限规则语法。</font>*

***

## <font style="color:rgb(51, 51, 51);">权限系统概述</font>

<font style="color:rgb(51, 51, 51);">Claude Code 的权限系统将操作分为三类，不同类型的操作有不同的默认权限策略：</font>

| <font style="color:rgb(255, 255, 255);">工具类型</font> | <font style="color:rgb(255, 255, 255);">示例</font> | <font style="color:rgb(255, 255, 255);">是否需要批准</font> | <font style="color:rgb(255, 255, 255);">永久允许行为</font> |
| --- | --- | --- | --- |
| <font style="color:rgb(51, 51, 51);">只读操作</font> | <font style="color:rgb(51, 51, 51);">文件读取、Grep 搜索</font> | <font style="color:rgb(51, 51, 51);">否</font> | <font style="color:rgb(51, 51, 51);">不适用</font> |
| <font style="color:rgb(51, 51, 51);">Bash 命令</font> | <font style="color:rgb(51, 51, 51);">Shell 命令执行</font> | <font style="color:rgb(51, 51, 51);">是</font> | <font style="color:rgb(51, 51, 51);">每个项目目录和命令永久有效</font> |
| <font style="color:rgb(51, 51, 51);">文件修改</font> | <font style="color:rgb(51, 51, 51);">Edit/Write 文件</font> | <font style="color:rgb(51, 51, 51);">是</font> | <font style="color:rgb(51, 51, 51);">直到会话结束</font> |

***

## <font style="color:rgb(51, 51, 51);">三种权限动作</font>

<font style="color:rgb(51, 51, 51);">每条权限规则最终会解析为以下三种动作之一：</font>

| <font style="color:rgb(255, 255, 255);">动作</font> | <font style="color:rgb(255, 255, 255);">效果</font> | <font style="color:rgb(255, 255, 255);">适用场景</font> |
| --- | --- | --- |
| <code><font style="color:rgb(51, 51, 51);">"allow"</font></code> | <font style="color:rgb(51, 51, 51);">无需审批，直接自动运行</font> | <font style="color:rgb(51, 51, 51);">低风险、高频操作，如 git status、npm run build</font> |
| <code><font style="color:rgb(51, 51, 51);">"ask"</font></code> | <font style="color:rgb(51, 51, 51);">弹出审批提示，由你决定是否允许</font> | <font style="color:rgb(51, 51, 51);">有一定风险的操作，如文件写入、危险命令执行</font> |
| <code><font style="color:rgb(51, 51, 51);">"deny"</font></code> | <font style="color:rgb(51, 51, 51);">直接阻止，不会执行也不会提示</font> | <font style="color:rgb(51, 51, 51);">明确不允许的危险操作，如 git push、rm -rf</font> |

***<font style="color:rgb(44, 58, 94);">规则优先级：deny → ask → allow。</font>****<font style="color:rgb(44, 58, 94);"> </font>**<font style="color:rgb(44, 58, 94);">第一个匹配的规则获胜，因此 deny 规则始终优先于 allow 和 ask。</font>*

***

## <font style="color:rgb(51, 51, 51);">权限模式</font>

<font style="color:rgb(51, 51, 51);">权限模式控制 Claude 是否在执行操作前询问用户。不同的任务需要不同级别的自主权。</font>

### <font style="color:rgb(51, 51, 51);">1、六种可用模式</font>

| <font style="color:rgb(255, 255, 255);">模式</font> | <font style="color:rgb(255, 255, 255);">描述</font> | <font style="color:rgb(255, 255, 255);">最适用场景</font> |
| --- | --- | --- |
| <code><font style="color:rgb(51, 51, 51);">default</font></code> | <font style="color:rgb(51, 51, 51);">标准行为：首次使用每个工具时提示权限</font> | <font style="color:rgb(51, 51, 51);">入门学习、敏感工作需要完全监督</font> |
| <code><font style="color:rgb(51, 51, 51);">acceptEdits</font></code> | <font style="color:rgb(51, 51, 51);">自动接受会话的文件编辑权限，受保护目录除外</font> | <font style="color:rgb(51, 51, 51);">迭代正在审查的代码</font> |
| <code><font style="color:rgb(51, 51, 51);">plan</font></code> | <font style="color:rgb(51, 51, 51);">Plan Mode：Claude 可以分析但不能修改文件或执行命令</font> | <font style="color:rgb(51, 51, 51);">探索代码库、规划重构</font> |
| <code><font style="color:rgb(51, 51, 51);">auto</font></code> | <font style="color:rgb(51, 51, 51);">自动批准工具调用，并进行后台安全检查（研究预览）</font> | <font style="color:rgb(51, 51, 51);">长时间运行的任务、减少提示疲劳</font> |
| <code><font style="color:rgb(51, 51, 51);">dontAsk</font></code> | <font style="color:rgb(51, 51, 51);">自动拒绝工具调用，除非通过权限规则预先批准</font> | <font style="color:rgb(51, 51, 51);">锁定环境、CI 管道</font> |
| <code><font style="color:rgb(51, 51, 51);">bypassPermissions</font></code> | <font style="color:rgb(51, 51, 51);">跳过权限提示，但对受保护目录的写入仍会提示</font> | <font style="color:rgb(51, 51, 51);">仅隔离容器和 VM</font> |

***<font style="color:rgb(44, 58, 94);">受保护目录说明：</font>****<font style="color:rgb(44, 58, 94);">无论模式如何，对</font>**<font style="color:rgb(44, 58, 94);"> </font>*<code>_<font style="color:rgb(44, 58, 94);">.git</font>_</code>*<font style="color:rgb(44, 58, 94);">、</font>*<code>_<font style="color:rgb(44, 58, 94);">.vscode</font>_</code>*<font style="color:rgb(44, 58, 94);">、</font>*<code>_<font style="color:rgb(44, 58, 94);">.idea</font>_</code>*<font style="color:rgb(44, 58, 94);">、</font>*<code>_<font style="color:rgb(44, 58, 94);">.husky</font>_</code>*<font style="color:rgb(44, 58, 94);"> </font>**<font style="color:rgb(44, 58, 94);">和</font>**<font style="color:rgb(44, 58, 94);"> </font>*<code>_<font style="color:rgb(44, 58, 94);">.claude</font>_</code>*<font style="color:rgb(44, 58, 94);"> </font>**<font style="color:rgb(44, 58, 94);">的写入永远不会自动批准，除了</font>**<font style="color:rgb(44, 58, 94);"> </font>*<code>_<font style="color:rgb(44, 58, 94);">.claude/commands</font>_</code>*<font style="color:rgb(44, 58, 94);">、</font>*<code>_<font style="color:rgb(44, 58, 94);">.claude/agents</font>_</code>*<font style="color:rgb(44, 58, 94);"> </font>**<font style="color:rgb(44, 58, 94);">和</font>**<font style="color:rgb(44, 58, 94);"> </font>*<code>_<font style="color:rgb(44, 58, 94);">.claude/skills</font>_</code>*<font style="color:rgb(44, 58, 94);">。</font>*

### <font style="color:rgb(51, 51, 51);">2、切换权限模式</font>

**<font style="color:rgb(51, 51, 51);">会话期间切换：</font>**<font style="color:rgb(51, 51, 51);">按</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">Shift+Tab</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">循环切换</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">default</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">→</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">acceptEdits</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">→</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">plan</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">→</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">auto</font></code>

**<font style="color:rgb(51, 51, 51);">启动时指定模式：</font>**

```plain
claude --permission-mode plan
claude --permission-mode bypassPermissions
```

**<font style="color:rgb(51, 51, 51);">设置为默认模式（settings.json）：</font>**

**<font style="color:rgb(97, 127, 16);">实例</font>**

<font style="color:rgb(0, 153, 0);">{</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"permissions"</font><font style="color:rgb(51, 153, 51);">:</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">{</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"defaultMode"</font><font style="color:rgb(51, 153, 51);">:</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"acceptEdits"</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">}</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(0, 153, 0);">}</font>

***

## <font style="color:rgb(51, 51, 51);">权限规则语法</font>

### <font style="color:rgb(51, 51, 51);">1、基本格式</font>

<font style="color:rgb(51, 51, 51);">权限规则遵循格式</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">Tool</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">或</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">Tool(specifier)</font></code><font style="color:rgb(51, 51, 51);">：</font>

<font style="color:rgb(97, 127, 16);">实例</font>

<font style="color:rgb(0, 153, 0);">{</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"permissions"</font><font style="color:rgb(51, 153, 51);">:</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">{</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"allow"</font><font style="color:rgb(51, 153, 51);">:</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">\[</font><font style="color:rgb(51, 102, 204);">"Bash"</font><font style="color:rgb(51, 153, 51);">,</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"WebFetch"</font><font style="color:rgb(51, 153, 51);">,</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"Read"</font><font style="color:rgb(0, 153, 0);">]</font><font style="color:rgb(51, 153, 51);">,</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"deny"</font><font style="color:rgb(51, 153, 51);">:</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">\[</font><font style="color:rgb(51, 102, 204);">"Edit"</font><font style="color:rgb(0, 153, 0);">]</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">}</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(0, 153, 0);">}</font>

### <font style="color:rgb(51, 51, 51);">2、匹配所有工具使用</font>

<font style="color:rgb(51, 51, 51);">不带说明符的规则匹配该工具的所有使用：</font>

| <font style="color:rgb(255, 255, 255);">规则</font> | <font style="color:rgb(255, 255, 255);">效果</font> |
| --- | --- |
| <code><font style="color:rgb(51, 51, 51);">Bash</font></code> | <font style="color:rgb(51, 51, 51);">匹配所有 Bash 命令</font> |
| <code><font style="color:rgb(51, 51, 51);">WebFetch</font></code> | <font style="color:rgb(51, 51, 51);">匹配所有网络获取请求</font> |
| <code><font style="color:rgb(51, 51, 51);">Read</font></code> | <font style="color:rgb(51, 51, 51);">匹配所有文件读取</font> |
| <code><font style="color:rgb(51, 51, 51);">Edit</font></code> | <font style="color:rgb(51, 51, 51);">匹配所有文件编辑</font> |

<code><font style="color:rgb(51, 51, 51);">Bash(*)</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">等同于</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">Bash</font></code><font style="color:rgb(51, 51, 51);">，两者效果相同。</font>

### <font style="color:rgb(51, 51, 51);">3、使用说明符进行细粒度控制</font>

**<font style="color:rgb(97, 127, 16);">实例</font>**

<font style="color:rgb(0, 153, 0);">{</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"permissions"</font><font style="color:rgb(51, 153, 51);">:</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">{</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"allow"</font><font style="color:rgb(51, 153, 51);">:</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">\[</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"Bash(npm run build)"</font><font style="color:rgb(51, 153, 51);">,</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">   </font><font style="color:rgb(51, 51, 51);"> </font>*<font style="color:rgb(0, 102, 0);">// 匹配确切的命令</font>*<font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"Read(./.env)"</font><font style="color:rgb(51, 153, 51);">,</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">           </font><font style="color:rgb(51, 51, 51);"> </font>*<font style="color:rgb(0, 102, 0);">// 匹配读取当前目录中的 .env 文件</font>*<font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"WebFetch(domain:example.com)"</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);"> </font>*<font style="color:rgb(0, 102, 0);">// 匹配对 example.com 的获取请求</font>*<font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">]</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">}</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(0, 153, 0);">}</font>

### <font style="color:rgb(51, 51, 51);">4、通配符模式</font>

<font style="color:rgb(51, 51, 51);">Bash 规则支持带有</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">*</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">的 glob 模式，通配符可以出现在命令中的任何位置：</font>

**<font style="color:rgb(97, 127, 16);">实例</font>**

<font style="color:rgb(0, 153, 0);">{</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"permissions"</font><font style="color:rgb(51, 153, 51);">:</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">{</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"allow"</font><font style="color:rgb(51, 153, 51);">:</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">\[</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"Bash(npm run _)"</font><font style="color:rgb(51, 153, 51);">,</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">       </font><font style="color:rgb(51, 51, 51);"> </font>*<font style="color:rgb(0, 102, 0);">// 匹配 npm run build、npm run test 等</font>*<font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"Bash(git commit _)"</font><font style="color:rgb(51, 153, 51);">,</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">     </font>*<font style="color:rgb(0, 102, 0);">// 匹配 git commit -m "message" 等</font>*<font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"Bash(git \* main)"</font><font style="color:rgb(51, 153, 51);">,</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">       </font>*<font style="color:rgb(0, 102, 0);">// 匹配 git checkout main、git merge main 等</font>*<font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"Bash(_ --version)"</font><font style="color:rgb(51, 153, 51);">,</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">     </font><font style="color:rgb(51, 51, 51);"> </font>*<font style="color:rgb(0, 102, 0);">// 匹配任何带 --version 参数的命令</font>*<font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"Bash(_ --help \*)"</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">       </font><font style="color:rgb(51, 51, 51);"> </font>*<font style="color:rgb(0, 102, 0);">// 匹配任何带 --help 参数的命令</font>*<font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">]</font><font style="color:rgb(51, 153, 51);">,</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"deny"</font><font style="color:rgb(51, 153, 51);">:</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">\[</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"Bash(git push \*)"</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">       </font><font style="color:rgb(51, 51, 51);"> </font>*<font style="color:rgb(0, 102, 0);">// 阻止所有 git push 操作</font>*<font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">]</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">}</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(0, 153, 0);">}</font>

***<font style="color:rgb(44, 58, 94);">注意通配符前的空格：</font>***<code>_<font style="color:rgb(44, 58, 94);">Bash(ls *)</font>_</code>*<font style="color:rgb(44, 58, 94);"> </font>**<font style="color:rgb(44, 58, 94);">匹配</font>**<font style="color:rgb(44, 58, 94);"> </font>*<code>_<font style="color:rgb(44, 58, 94);">ls -la</font>_</code>*<font style="color:rgb(44, 58, 94);"> </font>**<font style="color:rgb(44, 58, 94);">但不匹配</font>**<font style="color:rgb(44, 58, 94);"> </font>*<code>_<font style="color:rgb(44, 58, 94);">lsof</font>_</code>*<font style="color:rgb(44, 58, 94);">；</font>*<code>_<font style="color:rgb(44, 58, 94);">Bash(ls*)</font>_</code>*<font style="color:rgb(44, 58, 94);"> </font>\_\_<font style="color:rgb(44, 58, 94);">匹配两者。</font>*

***

## <font style="color:rgb(51, 51, 51);">工具特定的权限规则</font>

### <font style="color:rgb(51, 51, 51);">1、Bash 命令</font>

| <font style="color:rgb(255, 255, 255);">规则</font> | <font style="color:rgb(255, 255, 255);">匹配示例</font> |
| --- | --- |
| <code><font style="color:rgb(51, 51, 51);">Bash(npm run build)</font></code> | <font style="color:rgb(51, 51, 51);">仅</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">npm run build</font></code> |
| <code><font style="color:rgb(51, 51, 51);">Bash(npm run test *)</font></code> | <code><font style="color:rgb(51, 51, 51);">npm run test</font></code><br/><font style="color:rgb(51, 51, 51);">、</font><code><font style="color:rgb(51, 51, 51);">npm run test --coverage</font></code> |
| <code><font style="color:rgb(51, 51, 51);">Bash(npm *)</font></code> | <font style="color:rgb(51, 51, 51);">任何以 npm 开头的命令</font> |
| <code><font style="color:rgb(51, 51, 51);">Bash(* install)</font></code> | <font style="color:rgb(51, 51, 51);">任何以 install 结尾的命令</font> |
| <code><font style="color:rgb(51, 51, 51);">Bash(git * main)</font></code> | <code><font style="color:rgb(51, 51, 51);">git checkout main</font></code><br/><font style="color:rgb(51, 51, 51);">、</font><code><font style="color:rgb(51, 51, 51);">git merge main</font></code> |

***<font style="color:rgb(44, 58, 94);">重要限制：</font>****<font style="color:rgb(44, 58, 94);">尝试约束命令参数的 Bash 权限模式可能很脆弱。URL 前的选项、不同的协议、重定向、变量、额外空格都可能导致不匹配。建议使用 WebFetch 工具配合</font>**<font style="color:rgb(44, 58, 94);"> </font>*<code>_<font style="color:rgb(44, 58, 94);">domain:</font>_</code>*<font style="color:rgb(44, 58, 94);"> </font>\_\_<font style="color:rgb(44, 58, 94);">权限进行 URL 过滤。</font>*

### <font style="color:rgb(51, 51, 51);">2、Read 和 Edit（文件操作）</font>

<font style="color:rgb(51, 51, 51);">文件路径支持多种路径前缀模式：</font>

| <font style="color:rgb(255, 255, 255);">模式前缀</font> | <font style="color:rgb(255, 255, 255);">含义</font> | <font style="color:rgb(255, 255, 255);">示例</font> |
| --- | --- | --- |
| <code><font style="color:rgb(51, 51, 51);">//path</font></code> | <font style="color:rgb(51, 51, 51);">绝对路径（从文件系统根目录）</font> | <code><font style="color:rgb(51, 51, 51);">Read(//Users/alice/secrets/**)</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">匹配</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">/Users/alice/secrets/**</font></code> |
| <code><font style="color:rgb(51, 51, 51);">~/path</font></code> | <font style="color:rgb(51, 51, 51);">主目录路径</font> | <code><font style="color:rgb(51, 51, 51);">Read(~/Documents/*.pdf)</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">匹配</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">/Users/alice/Documents/*.pdf</font></code> |
| <code><font style="color:rgb(51, 51, 51);">/path</font></code> | <font style="color:rgb(51, 51, 51);">相对于项目根目录</font> | <code><font style="color:rgb(51, 51, 51);">Edit(/src/**/*.ts)</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">匹配</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);"><project root>/src/**/*.ts</font></code> |
| <code><font style="color:rgb(51, 51, 51);">path</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">或</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">./path</font></code> | <font style="color:rgb(51, 51, 51);">相对于当前目录</font> | <code><font style="color:rgb(51, 51, 51);">Read(*.env)</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">匹配</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);"><cwd>/*.env</font></code> |

**<font style="color:rgb(97, 127, 16);">实例</font>**

<font style="color:rgb(0, 153, 0);">{</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"permissions"</font><font style="color:rgb(51, 153, 51);">:</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">{</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"allow"</font><font style="color:rgb(51, 153, 51);">:</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">\[</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"Edit(/docs/**)"</font><font style="color:rgb(51, 153, 51);">,</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">         </font>*<font style="color:rgb(0, 102, 0);">// 允许编辑项目 docs 目录下的文件</font>*<font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"Read(~/.zshrc)"</font><font style="color:rgb(51, 153, 51);">,</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">       </font><font style="color:rgb(51, 51, 51);"> </font>*<font style="color:rgb(0, 102, 0);">// 允许读取主目录的 .zshrc</font>*<font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"Edit(//tmp/scratch.txt)"</font><font style="color:rgb(51, 153, 51);">,</font><font style="color:rgb(51, 51, 51);"> </font>*<font style="color:rgb(0, 102, 0);">// 允许编辑绝对路径的临时文件</font>*<font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"Read(src/**)"</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">           </font>*<font style="color:rgb(0, 102, 0);">// 允许读取当前目录 src 子目录的文件</font>*<font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">]</font><font style="color:rgb(51, 153, 51);">,</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"deny"</font><font style="color:rgb(51, 153, 51);">:</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">\[</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"Read(\*.env)"</font><font style="color:rgb(51, 153, 51);">,</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">           </font>*<font style="color:rgb(0, 102, 0);">// 阻止读取 .env 文件（防止泄露密钥）</font>*<font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"Edit(//etc/\*\*)"</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">         </font>*<font style="color:rgb(0, 102, 0);">// 阻止编辑系统目录文件</font>*<font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">]</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">}</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(0, 153, 0);">}</font>

***<font style="color:rgb(44, 58, 94);">注意：</font>****<font style="color:rgb(44, 58, 94);">Read 和 Edit deny 规则不适用于 Bash 子进程中的</font>**<font style="color:rgb(44, 58, 94);"> </font>*<code>_<font style="color:rgb(44, 58, 94);">cat .env</font>_</code>*<font style="color:rgb(44, 58, 94);">。要获得 OS 级别强制执行，需启用沙箱。</font>*

### <font style="color:rgb(51, 51, 51);">3、WebFetch（网络请求）</font>

**<font style="color:rgb(97, 127, 16);">实例</font>**

<font style="color:rgb(0, 153, 0);">{</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"permissions"</font><font style="color:rgb(51, 153, 51);">:</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">{</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"allow"</font><font style="color:rgb(51, 153, 51);">:</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">\[</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"WebFetch(domain:github.com)"</font><font style="color:rgb(51, 153, 51);">,</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">   </font>*<font style="color:rgb(0, 102, 0);">// 允许访问 GitHub</font>*<font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"WebFetch(domain:api.example.com)"</font><font style="color:rgb(51, 51, 51);"> </font>*<font style="color:rgb(0, 102, 0);">// 允许访问内部 API</font>*<font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">]</font><font style="color:rgb(51, 153, 51);">,</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"deny"</font><font style="color:rgb(51, 153, 51);">:</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">\[</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"WebFetch(domain:untrusted.com)"</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);"> </font>*<font style="color:rgb(0, 102, 0);">// 阻止访问不可信域名</font>*<font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">]</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">}</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(0, 153, 0);">}</font>

### <font style="color:rgb(51, 51, 51);">4、MCP（模型上下文协议）</font>

**<font style="color:rgb(97, 127, 16);">实例</font>**

<font style="color:rgb(0, 153, 0);">{</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"permissions"</font><font style="color:rgb(51, 153, 51);">:</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">{</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"allow"</font><font style="color:rgb(51, 153, 51);">:</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">\[</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"mcp__puppeteer"</font><font style="color:rgb(51, 153, 51);">,</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">                     </font>*<font style="color:rgb(0, 102, 0);">// 允许 puppeteer 服务器提供的任何工具</font>*<font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"mcp__puppeteer\_\_\*"</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">                   </font>*<font style="color:rgb(0, 102, 0);">// 允许来自 puppeteer 服务器的所有工具</font>*<font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">]</font><font style="color:rgb(51, 153, 51);">,</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"deny"</font><font style="color:rgb(51, 153, 51);">:</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">\[</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"mcp__puppeteer__puppeteer_navigate"</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);"> </font>*<font style="color:rgb(0, 102, 0);">// 阻止特定工具</font>*<font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">]</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">}</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(0, 153, 0);">}</font>

### <font style="color:rgb(51, 51, 51);">5、Agent（子代理）</font>

**<font style="color:rgb(97, 127, 16);">实例</font>**

<font style="color:rgb(0, 153, 0);">{</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"permissions"</font><font style="color:rgb(51, 153, 51);">:</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">{</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"allow"</font><font style="color:rgb(51, 153, 51);">:</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">\[</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"Agent(Explore)"</font><font style="color:rgb(51, 153, 51);">,</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">         </font><font style="color:rgb(51, 51, 51);"> </font>*<font style="color:rgb(0, 102, 0);">// 允许使用 Explore 子代理</font>*<font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"Agent(Plan)"</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">             </font><font style="color:rgb(51, 51, 51);"> </font>*<font style="color:rgb(0, 102, 0);">// 允许使用 Plan 子代理</font>*<font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">]</font><font style="color:rgb(51, 153, 51);">,</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"deny"</font><font style="color:rgb(51, 153, 51);">:</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">\[</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"Agent(my-custom-agent)"</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">   </font>*<font style="color:rgb(0, 102, 0);">// 阻止自定义子代理</font>*<font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">]</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">}</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(0, 153, 0);">}</font>

***

## <font style="color:rgb(51, 51, 51);">工作目录配置</font>

<font style="color:rgb(51, 51, 51);">默认情况下，Claude Code 只允许访问启动时的工作目录及其子目录。如果需要访问项目目录之外的路径，必须显式配置。</font>

### <font style="color:rgb(51, 51, 51);">1、扩展访问方式</font>

* **<font style="color:rgb(51, 51, 51);">启动期间：</font>**<font style="color:rgb(51, 51, 51);">使用</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">--add-dir <path></font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">CLI 参数</font>
* **<font style="color:rgb(51, 51, 51);">会话期间：</font>**<font style="color:rgb(51, 51, 51);">使用</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">/add-dir</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">命令</font>
* **<font style="color:rgb(51, 51, 51);">持久配置：</font>**<font style="color:rgb(51, 51, 51);">添加到 settings.json 中的</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">additionalDirectories</font></code>

**<font style="color:rgb(97, 127, 16);">实例</font>**

<font style="color:rgb(0, 153, 0);">{</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"additionalDirectories"</font><font style="color:rgb(51, 153, 51);">:</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">\[</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"~/projects/personal/**"</font><font style="color:rgb(51, 153, 51);">,</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">   </font>*<font style="color:rgb(0, 102, 0);">// 允许访问个人项目目录</font>*<font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"~/projects/work/**"</font><font style="color:rgb(51, 153, 51);">,</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">       </font>*<font style="color:rgb(0, 102, 0);">// 允许访问工作项目目录</font>*<font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"~/dotfiles/\*\*"</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">             </font><font style="color:rgb(51, 51, 51);"> </font>*<font style="color:rgb(0, 102, 0);">// 允许访问配置文件目录</font>*<font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">]</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(0, 153, 0);">}</font>

### <font style="color:rgb(51, 51, 51);">2、例外情况</font>

<font style="color:rgb(51, 51, 51);">以下内容在设置额外目录后仍可访问，无需额外配置：</font>

* <code><font style="color:rgb(51, 51, 51);">.claude/skills/</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">中的 Skills（带有实时重新加载）</font>
* <code><font style="color:rgb(51, 51, 51);">.claude/settings.json</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">中的插件设置（仅</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">enabledPlugins</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">和</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">extraKnownMarketplaces</font></code><font style="color:rgb(51, 51, 51);">）</font>
* <font style="color:rgb(51, 51, 51);">CLAUDE.md 文件和</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">.claude/rules/</font></code><font style="color:rgb(51, 51, 51);">（仅当设置</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">CLAUDE_CODE_ADDITIONAL_DIRECTORIES_CLAUDE_MD=1</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">时）</font>

***

## <font style="color:rgb(51, 51, 51);">自动模式（Auto Mode）</font>

<font style="color:rgb(51, 51, 51);">自动模式是 Claude Code 引入的一种新机制，通过模型驱动的分类器替代人工审批，在保证效率的同时尽量控制风险。</font>

### <font style="color:rgb(51, 51, 51);">1、可用条件</font>

* <font style="color:rgb(51, 51, 51);">仅限 Team、Enterprise 和 API 计划</font>
* <font style="color:rgb(51, 51, 51);">需要 Claude Sonnet 4.6 或 Claude Opus 4.6</font>
* <font style="color:rgb(51, 51, 51);">在 Haiku、claude-3 模型或第三方提供商上不可用</font>
* <font style="color:rgb(51, 51, 51);">管理员必须在 Claude Code 管理员设置中启用</font>

### <font style="color:rgb(51, 51, 51);">2、工作原理</font>

<font style="color:rgb(51, 51, 51);">在每个操作运行前，一个单独的分类器模型审查对话并决定该操作是否与用户要求的相匹配。</font>

**<font style="color:rgb(51, 51, 51);">防御层次：</font>**

1. <font style="color:rgb(51, 51, 51);">服务器端探针扫描传入的工具结果</font>
2. <font style="color:rgb(51, 51, 51);">分类器永远不会看到工具结果，防止注入指令影响决策</font>

**<font style="color:rgb(51, 51, 51);">操作评估顺序：</font>**

1. <font style="color:rgb(51, 51, 51);">与允许或拒绝规则匹配的操作立即解决</font>
2. <font style="color:rgb(51, 51, 51);">只读操作和工作目录中的文件编辑自动批准（受保护目录除外）</font>
3. <font style="color:rgb(51, 51, 51);">其他内容发送到分类器</font>
4. <font style="color:rgb(51, 51, 51);">如果分类器阻止，Claude 收到原因并尝试替代方法</font>

### <font style="color:rgb(51, 51, 51);">3、分类器默认行为</font>

| <font style="color:rgb(255, 255, 255);">操作类型</font> | <font style="color:rgb(255, 255, 255);">行为</font> |
| --- | --- |
| **<font style="color:rgb(51, 51, 51);">默认阻止</font>** | |
| <font style="color:rgb(51, 51, 51);">下载和执行代码</font> | <code><font style="color:rgb(51, 51, 51);">curl | bash</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">等</font> |
| <font style="color:rgb(51, 51, 51);">向外部端点发送敏感数据</font> | <font style="color:rgb(51, 51, 51);">数据泄露风险</font> |
| <font style="color:rgb(51, 51, 51);">生产部署和迁移</font> | <font style="color:rgb(51, 51, 51);">生产环境修改</font> |
| <font style="color:rgb(51, 51, 51);">云存储上的大规模删除</font> | <font style="color:rgb(51, 51, 51);">数据丢失风险</font> |
| <font style="color:rgb(51, 51, 51);">授予 IAM 或仓库权限</font> | <font style="color:rgb(51, 51, 51);">权限提升风险</font> |
| <font style="color:rgb(51, 51, 51);">修改共享基础设施</font> | <font style="color:rgb(51, 51, 51);">影响其他用户</font> |
| <font style="color:rgb(51, 51, 51);">不可逆地销毁文件</font> | <font style="color:rgb(51, 51, 51);">会话开始前存在的文件</font> |
| <font style="color:rgb(51, 51, 51);">破坏性源代码控制操作</font> | <font style="color:rgb(51, 51, 51);">强制推送、直接推送到 main</font> |
| **<font style="color:rgb(51, 51, 51);">默认允许</font>** | |
| <font style="color:rgb(51, 51, 51);">工作目录中的本地文件操作</font> | <font style="color:rgb(51, 51, 51);">安全范围内</font> |
| <font style="color:rgb(51, 51, 51);">安装声明的依赖项</font> | <font style="color:rgb(51, 51, 51);">package.json 中已有的依赖</font> |
| <font style="color:rgb(51, 51, 51);">读取 .env 并发送凭证</font> | <font style="color:rgb(51, 51, 51);">向匹配的 API 发送</font> |
| <font style="color:rgb(51, 51, 51);">只读 HTTP 请求</font> | <font style="color:rgb(51, 51, 51);">GET 请求</font> |
| <font style="color:rgb(51, 51, 51);">推送到启动的分支</font> | <font style="color:rgb(51, 51, 51);">安全分支操作</font> |

### <font style="color:rgb(51, 51, 51);">4、自动模式配置</font>

**<font style="color:rgb(97, 127, 16);">实例</font>**

<font style="color:rgb(0, 153, 0);">{</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"autoMode"</font><font style="color:rgb(51, 153, 51);">:</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">{</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"environment"</font><font style="color:rgb(51, 153, 51);">:</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">\[</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"Source control: github.example.com/acme-corp and all repos under it"</font><font style="color:rgb(51, 153, 51);">,</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"Trusted cloud buckets: s3://acme-build-artifacts, gs://acme-ml-datasets"</font><font style="color:rgb(51, 153, 51);">,</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"Trusted internal domains: \*.corp.example.com, api.internal.example.com"</font><font style="color:rgb(51, 153, 51);">,</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"Key internal services: Jenkins at ci.example.com, Artifactory at artifacts.example.com"</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">]</font><font style="color:rgb(51, 153, 51);">,</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"allow"</font><font style="color:rgb(51, 153, 51);">:</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">\[</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"Deploying to the staging namespace is allowed"</font><font style="color:rgb(51, 153, 51);">,</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"Writing to s3://acme-scratch/ is allowed"</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">]</font><font style="color:rgb(51, 153, 51);">,</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"soft_deny"</font><font style="color:rgb(51, 153, 51);">:</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">\[</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"Never run database migrations outside the migrations CLI"</font><font style="color:rgb(51, 153, 51);">,</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"Never modify files under infra/terraform/prod/: production infrastructure changes go through the review workflow"</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">]</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">}</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(0, 153, 0);">}</font>

### <font style="color:rgb(51, 51, 51);">5、回退机制</font>

<font style="color:rgb(51, 51, 51);">如果分类器在一行中阻止操作 3 次，或在一个会话中总共阻止 20 次，自动模式会暂停，Claude Code 恢复为每个操作提示。</font>

<font style="color:rgb(51, 51, 51);">/permissions  # 在 "最近拒绝" 选项卡查看被拒绝的操作</font>

***

## <font style="color:rgb(51, 51, 51);">沙箱与权限的关系</font>

<font style="color:rgb(51, 51, 51);">沙箱和权限是互补的安全层，协同工作：</font>

| <font style="color:rgb(255, 255, 255);">方面</font> | <font style="color:rgb(255, 255, 255);">权限</font> | <font style="color:rgb(255, 255, 255);">沙箱</font> |
| --- | --- | --- |
| **<font style="color:rgb(51, 51, 51);">控制对象</font>** | <font style="color:rgb(51, 51, 51);">控制 Claude Code 可以使用哪些工具</font> | <font style="color:rgb(51, 51, 51);">限制 Bash 命令可访问的文件系统和网络内容</font> |
| **<font style="color:rgb(51, 51, 51);">评估时机</font>** | <font style="color:rgb(51, 51, 51);">在任何工具运行之前进行评估</font> | <font style="color:rgb(51, 51, 51);">仅适用于 Bash 命令及其子进程</font> |
| **<font style="color:rgb(51, 51, 51);">适用范围</font>** | <font style="color:rgb(51, 51, 51);">所有工具：Bash、Read、Edit、WebFetch、MCP 等</font> | <font style="color:rgb(51, 51, 51);">仅 Bash 命令</font> |

### <font style="color:rgb(51, 51, 51);">1、启用沙箱</font>

<font style="color:rgb(51, 51, 51);">/sandbox</font>

<font style="color:rgb(51, 51, 51);">运行</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">/sandbox</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">命令启用沙箱，会打开一个菜单选择沙箱模式。</font>

### <font style="color:rgb(51, 51, 51);">2、配置沙箱</font>

**<font style="color:rgb(97, 127, 16);">实例</font>**

<font style="color:rgb(0, 153, 0);">{</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"sandbox"</font><font style="color:rgb(51, 153, 51);">:</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">{</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"enabled"</font><font style="color:rgb(51, 153, 51);">:</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:rgb(0, 51, 102);">true</font>**<font style="color:rgb(51, 153, 51);">,</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"filesystem"</font><font style="color:rgb(51, 153, 51);">:</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">{</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"allowWrite"</font><font style="color:rgb(51, 153, 51);">:</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">\[</font><font style="color:rgb(51, 102, 204);">"~/.kube"</font><font style="color:rgb(51, 153, 51);">,</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"/tmp/build"</font><font style="color:rgb(0, 153, 0);">]</font><font style="color:rgb(51, 153, 51);">,</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">   </font>*<font style="color:rgb(0, 102, 0);">// 允许写入这些路径</font>*<font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"denyWrite"</font><font style="color:rgb(51, 153, 51);">:</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">\[</font><font style="color:rgb(51, 102, 204);">"~/important/\*\*"</font><font style="color:rgb(0, 153, 0);">]</font><font style="color:rgb(51, 153, 51);">,</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">           </font>*<font style="color:rgb(0, 102, 0);">// 阻止写入重要目录</font>*<font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"denyRead"</font><font style="color:rgb(51, 153, 51);">:</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">\[</font><font style="color:rgb(51, 102, 204);">"~/"</font><font style="color:rgb(0, 153, 0);">]</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">                         </font><font style="color:rgb(51, 51, 51);"> </font>*<font style="color:rgb(0, 102, 0);">// 阻止读取主目录</font>*<font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">}</font><font style="color:rgb(51, 153, 51);">,</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"network"</font><font style="color:rgb(51, 153, 51);">:</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">{</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"httpProxyPort"</font><font style="color:rgb(51, 153, 51);">:</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(204, 0, 0);">8080</font><font style="color:rgb(51, 153, 51);">,</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">                     </font><font style="color:rgb(51, 51, 51);"> </font>*<font style="color:rgb(0, 102, 0);">// HTTP 代理端口</font>*<font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"socksProxyPort"</font><font style="color:rgb(51, 153, 51);">:</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(204, 0, 0);">8081</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">                     </font><font style="color:rgb(51, 51, 51);"> </font>*<font style="color:rgb(0, 102, 0);">// SOCKS 代理端口</font>*<font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">}</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">}</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(0, 153, 0);">}</font>

***<font style="color:rgb(44, 58, 94);">深度防御：</font>**\_\_<font style="color:rgb(44, 58, 94);">权限和沙箱应同时启用。权限 deny 规则阻止 Claude 尝试访问受限资源，沙箱限制防止 Bash 命令到达定义边界之外的资源。</font>*

***

## <font style="color:rgb(51, 51, 51);">使用 Hooks 扩展权限</font>

<font style="color:rgb(51, 51, 51);">PreToolUse hooks 在权限提示之前运行，可以：</font>

* <font style="color:rgb(51, 51, 51);">拒绝工具调用</font>
* <font style="color:rgb(51, 51, 51);">强制提示</font>
* <font style="color:rgb(51, 51, 51);">跳过提示让调用继续</font>

**<font style="color:rgb(97, 127, 16);">实例</font>**

*<font style="color:rgb(102, 102, 102);">#!/bin/bash</font>*<font style="color:rgb(51, 51, 51);">\
</font>*<font style="color:rgb(102, 102, 102);"># PreToolUse hook 示例：拦截危险命令</font>*<font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(0, 120, 0);">COMMAND</font><font style="color:rgb(51, 51, 51);">=$</font>**<font style="color:rgb(122, 8, 116);">(</font>\*\*\*\*<font style="color:rgb(194, 12, 185);">cat</font>**<font style="color:rgb(51, 51, 51);"> </font>**<font style="color:rgb(0, 0, 0);">|</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">jq</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(102, 0, 51);">-r</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(170, 17, 0);">'.tool_input.command // empty'</font>**<font style="color:rgb(122, 8, 116);">)</font>**<font style="color:rgb(51, 51, 51);">

</font>**<font style="color:rgb(0, 0, 0);">if</font>**<font style="color:rgb(51, 51, 51);"> </font>**<font style="color:rgb(122, 8, 116);">echo</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(170, 17, 0);">"</font><font style="color:rgb(0, 120, 0);">$COMMAND</font><font style="color:rgb(170, 17, 0);">"</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:rgb(0, 0, 0);">|</font>**<font style="color:rgb(51, 51, 51);"> </font>**<font style="color:rgb(194, 12, 185);">grep</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(102, 0, 51);">-qE</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(170, 17, 0);">'rm\s+(-\[rf]+\s+)\*(/|~|../)'</font><font style="color:rgb(51, 51, 51);">;</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:rgb(0, 0, 0);">then</font>**<font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:rgb(122, 8, 116);">echo</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(170, 17, 0);">"BLOCKED: rm on sensitive path"</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:rgb(122, 8, 116);">exit</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 0, 0);">2</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);"> </font>*<font style="color:rgb(102, 102, 102);"># 退出代码 2 阻止工具调用</font>*<font style="color:rgb(51, 51, 51);">\
</font>**<font style="color:rgb(0, 0, 0);">fi</font>**<font style="color:rgb(51, 51, 51);">\
</font>**<font style="color:rgb(122, 8, 116);">exit</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 0, 0);">0</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);"> </font>*<font style="color:rgb(102, 102, 102);"># 允许继续</font>*

***<font style="color:rgb(44, 58, 94);">重要：</font>**\_\_<font style="color:rgb(44, 58, 94);">跳过提示不会绕过权限规则。Deny 和 ask 规则在 hook 返回 "allow" 后仍会被评估。阻止 hook 以退出代码 2 退出时，在权限规则被评估之前停止工具调用。</font>*

***

## <font style="color:rgb(51, 51, 51);">设置优先级</font>

<font style="color:rgb(51, 51, 51);">Claude Code 的设置按以下优先级生效（从高到低）：</font>

1. **<font style="color:rgb(51, 51, 51);">托管设置</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">- 无法被任何其他级别覆盖（管理员控制）</font>
2. **<font style="color:rgb(51, 51, 51);">命令行参数</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">- 临时会话覆盖</font>
3. **<font style="color:rgb(51, 51, 51);">本地项目设置</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">(</font><code><font style="color:rgb(51, 51, 51);">.claude/settings.local.json</font></code><font style="color:rgb(51, 51, 51);">)</font>
4. **<font style="color:rgb(51, 51, 51);">共享项目设置</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">(</font><code><font style="color:rgb(51, 51, 51);">.claude/settings.json</font></code><font style="color:rgb(51, 51, 51);">)</font>
5. **<font style="color:rgb(51, 51, 51);">用户设置</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">(</font><code><font style="color:rgb(51, 51, 51);">~/.claude/settings.json</font></code><font style="color:rgb(51, 51, 51);">)</font>

***<font style="color:rgb(44, 58, 94);">关键规则：</font>**\_\_<font style="color:rgb(44, 58, 94);">如果工具在任何级别被拒绝，没有其他级别可以允许它。</font>*

***

## <font style="color:rgb(51, 51, 51);">实用配置示例</font>

### <font style="color:rgb(51, 51, 51);">示例一：保守模式（所有操作都需审批）</font>

<font style="color:rgb(51, 51, 51);">适合初次接触 Claude Code 或在重要项目上工作时使用：</font>

**<font style="color:rgb(97, 127, 16);">实例</font>**

<font style="color:rgb(0, 153, 0);">{</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"permissions"</font><font style="color:rgb(51, 153, 51);">:</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">{</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"defaultMode"</font><font style="color:rgb(51, 153, 51);">:</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"default"</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">}</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(0, 153, 0);">}</font>

### <font style="color:rgb(51, 51, 51);">示例二：开发常用配置（读操作放开，命令执行审批）</font>

<font style="color:rgb(51, 51, 51);">适合日常开发：允许 Claude 自由读取和搜索代码，但修改文件和执行命令时需要确认：</font>

**<font style="color:rgb(97, 127, 16);">实例</font>**

<font style="color:rgb(0, 153, 0);">{</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"permissions"</font><font style="color:rgb(51, 153, 51);">:</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">{</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"defaultMode"</font><font style="color:rgb(51, 153, 51);">:</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"acceptEdits"</font><font style="color:rgb(51, 153, 51);">,</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"allow"</font><font style="color:rgb(51, 153, 51);">:</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">\[</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"Bash(git status \*)"</font><font style="color:rgb(51, 153, 51);">,</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">     </font>*<font style="color:rgb(0, 102, 0);">// 查看 git 状态</font>*<font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"Bash(git log \*)"</font><font style="color:rgb(51, 153, 51);">,</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">       </font><font style="color:rgb(51, 51, 51);"> </font>*<font style="color:rgb(0, 102, 0);">// 查看 git 日志</font>*<font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"Bash(git diff \*)"</font><font style="color:rgb(51, 153, 51);">,</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">     </font><font style="color:rgb(51, 51, 51);"> </font>*<font style="color:rgb(0, 102, 0);">// 查看 git 差异</font>*<font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"Bash(npm run \*)"</font><font style="color:rgb(51, 153, 51);">,</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">       </font><font style="color:rgb(51, 51, 51);"> </font>*<font style="color:rgb(0, 102, 0);">// 运行 npm 脚本</font>*<font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"Bash(npm test \*)"</font><font style="color:rgb(51, 153, 51);">,</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">       </font>*<font style="color:rgb(0, 102, 0);">// 运行测试</font>*<font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"Bash(ls \*)"</font><font style="color:rgb(51, 153, 51);">,</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">             </font>*<font style="color:rgb(0, 102, 0);">// 列出目录</font>*<font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"Bash(grep \*)"</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">           </font><font style="color:rgb(51, 51, 51);"> </font>*<font style="color:rgb(0, 102, 0);">// 搜索内容</font>*<font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">]</font><font style="color:rgb(51, 153, 51);">,</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"deny"</font><font style="color:rgb(51, 153, 51);">:</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">\[</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"Bash(rm \*)"</font><font style="color:rgb(51, 153, 51);">,</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">             </font>*<font style="color:rgb(0, 102, 0);">// 删除文件：直接阻止</font>*<font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"Bash(git push \*)"</font><font style="color:rgb(51, 153, 51);">,</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">       </font>*<font style="color:rgb(0, 102, 0);">// 推送代码：直接阻止</font>*<font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"Bash(mkdir / *)"</font><font style="color:rgb(51, 153, 51);">,</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">       </font><font style="color:rgb(51, 51, 51);"> </font>_<font style="color:rgb(0, 102, 0);">// 创建系统目录：直接阻止</font>_<font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"Edit(*.env)"</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">             </font>*<font style="color:rgb(0, 102, 0);">// 阻止编辑 .env 文件</font>*<font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">]</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">}</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(0, 153, 0);">}</font>

### <font style="color:rgb(51, 51, 51);">示例三：锁定环境配置（仅允许预批准操作）</font>

<font style="color:rgb(51, 51, 51);">适合 CI 管道或需要严格控制的环境：</font>

**<font style="color:rgb(97, 127, 16);">实例</font>**

<font style="color:rgb(0, 153, 0);">{</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"permissions"</font><font style="color:rgb(51, 153, 51);">:</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">{</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"defaultMode"</font><font style="color:rgb(51, 153, 51);">:</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"dontAsk"</font><font style="color:rgb(51, 153, 51);">,</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"allow"</font><font style="color:rgb(51, 153, 51);">:</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">\[</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"Read(\*)"</font><font style="color:rgb(51, 153, 51);">,</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">                 </font>*<font style="color:rgb(0, 102, 0);">// 允许读取所有文件</font>*<font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"Bash(npm run build \*)"</font><font style="color:rgb(51, 153, 51);">,</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">   </font>*<font style="color:rgb(0, 102, 0);">// 允许构建命令</font>*<font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"Bash(npm test *)"</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">         </font>_<font style="color:rgb(0, 102, 0);">// 允许运行测试</font>_<font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">]</font><font style="color:rgb(51, 153, 51);">,</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"deny"</font><font style="color:rgb(51, 153, 51);">:</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">\[</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"Edit(*)"</font><font style="color:rgb(51, 153, 51);">,</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">                 </font>*<font style="color:rgb(0, 102, 0);">// 禁止所有文件编辑</font>*<font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"Bash(git \*)"</font><font style="color:rgb(51, 153, 51);">,</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">             </font>*<font style="color:rgb(0, 102, 0);">// 禁止所有 git 操作</font>*<font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"Bash(curl \*)"</font><font style="color:rgb(51, 153, 51);">,</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">           </font><font style="color:rgb(51, 51, 51);"> </font>*<font style="color:rgb(0, 102, 0);">// 禁止网络请求</font>*<font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"Bash(ssh \*)"</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">             </font><font style="color:rgb(51, 51, 51);"> </font>*<font style="color:rgb(0, 102, 0);">// 禁止 SSH 连接</font>*<font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">]</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">}</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(0, 153, 0);">}</font>

### <font style="color:rgb(51, 51, 51);">示例四：允许多项目访问</font>

<font style="color:rgb(51, 51, 51);">当 Claude 需要跨多个项目目录工作时：</font>

**<font style="color:rgb(97, 127, 16);">实例</font>**

<font style="color:rgb(0, 153, 0);">{</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"permissions"</font><font style="color:rgb(51, 153, 51);">:</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">{</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"allow"</font><font style="color:rgb(51, 153, 51);">:</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">\[</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"Edit(/src/**)"</font><font style="color:rgb(51, 153, 51);">,</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">           </font>*<font style="color:rgb(0, 102, 0);">// 允许编辑 src 目录</font>*<font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"Edit(/docs/**)"</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">           </font>*<font style="color:rgb(0, 102, 0);">// 允许编辑文档目录</font>*<font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">]</font><font style="color:rgb(51, 153, 51);">,</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"deny"</font><font style="color:rgb(51, 153, 51);">:</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">\[</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"Edit(/docs/**/\*.md)"</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">     </font><font style="color:rgb(51, 51, 51);"> </font>*<font style="color:rgb(0, 102, 0);">// 禁止编辑文档文件（只读）</font>*<font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">]</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">}</font><font style="color:rgb(51, 153, 51);">,</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"additionalDirectories"</font><font style="color:rgb(51, 153, 51);">:</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">\[</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"~/projects/personal/**"</font><font style="color:rgb(51, 153, 51);">,</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">   </font><font style="color:rgb(51, 51, 51);"> </font>*<font style="color:rgb(0, 102, 0);">// 允许访问个人项目</font>*<font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"~/projects/work/**"</font><font style="color:rgb(51, 153, 51);">,</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">       </font><font style="color:rgb(51, 51, 51);"> </font>*<font style="color:rgb(0, 102, 0);">// 允许访问工作项目</font>*<font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"~/dotfiles/**"</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">             </font><font style="color:rgb(51, 51, 51);"> </font>*<font style="color:rgb(0, 102, 0);">// 允许访问配置文件</font>*<font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">]</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(0, 153, 0);">}</font>

### <font style="color:rgb(51, 51, 51);">示例五：使用沙箱限制 Bash 操作</font>

<font style="color:rgb(51, 51, 51);">启用沙箱提供 OS 级别的额外保护：</font>

**<font style="color:rgb(97, 127, 16);">实例</font>**

<font style="color:rgb(0, 153, 0);">{</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"sandbox"</font><font style="color:rgb(51, 153, 51);">:</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">{</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"enabled"</font><font style="color:rgb(51, 153, 51);">:</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:rgb(0, 51, 102);">true</font>**<font style="color:rgb(51, 153, 51);">,</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"filesystem"</font><font style="color:rgb(51, 153, 51);">:</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">{</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"allowWrite"</font><font style="color:rgb(51, 153, 51);">:</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">\[</font><font style="color:rgb(51, 102, 204);">"/tmp/build"</font><font style="color:rgb(51, 153, 51);">,</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"~/projects/myapp/**"</font><font style="color:rgb(0, 153, 0);">]</font><font style="color:rgb(51, 153, 51);">,</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"denyRead"</font><font style="color:rgb(51, 153, 51);">:</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">\[</font><font style="color:rgb(51, 102, 204);">"~/secrets/**"</font><font style="color:rgb(0, 153, 0);">]</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">}</font><font style="color:rgb(51, 153, 51);">,</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"network"</font><font style="color:rgb(51, 153, 51);">:</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">{</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"httpProxyPort"</font><font style="color:rgb(51, 153, 51);">:</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(204, 0, 0);">8080</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">}</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">}</font><font style="color:rgb(51, 153, 51);">,</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"permissions"</font><font style="color:rgb(51, 153, 51);">:</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">{</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"allow"</font><font style="color:rgb(51, 153, 51);">:</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">\[</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"Bash(\*)"</font><font style="color:rgb(51, 153, 51);">,</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">                 </font>*<font style="color:rgb(0, 102, 0);">// 沙箱内允许所有命令</font>*<font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"WebFetch(domain:api.github.com)"</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">]</font><font style="color:rgb(51, 153, 51);">,</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"deny"</font><font style="color:rgb(51, 153, 51);">:</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">\[</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"WebFetch(domain:untrusted.com)"</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">]</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">}</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(0, 153, 0);">}</font>

***

## <font style="color:rgb(51, 51, 51);">托管设置（管理员配置）</font>

<font style="color:rgb(51, 51, 51);">管理员可以部署无法被用户或项目设置覆盖的托管设置。</font>

| <font style="color:rgb(255, 255, 255);">设置</font> | <font style="color:rgb(255, 255, 255);">描述</font> |
| --- | --- |
| <code><font style="color:rgb(51, 51, 51);">allowManagedHooksOnly</font></code> | <font style="color:rgb(51, 51, 51);">防止加载用户、项目和插件 hooks</font> |
| <code><font style="color:rgb(51, 51, 51);">allowManagedMcpServersOnly</font></code> | <font style="color:rgb(51, 51, 51);">仅尊重托管设置的 MCP 服务器</font> |
| <code><font style="color:rgb(51, 51, 51);">allowManagedPermissionRulesOnly</font></code> | <font style="color:rgb(51, 51, 51);">防止用户和项目设置定义权限规则</font> |
| <code><font style="color:rgb(51, 51, 51);">sandbox.filesystem.allowManagedReadPathsOnly</font></code> | <font style="color:rgb(51, 51, 51);">仅尊重托管设置的读取路径</font> |
| <code><font style="color:rgb(51, 51, 51);">sandbox.network.allowManagedDomainsOnly</font></code> | <font style="color:rgb(51, 51, 51);">仅尊重托管设置的允许域</font> |
| <code><font style="color:rgb(51, 51, 51);">permissions.disableBypassPermissionsMode</font></code> | <font style="color:rgb(51, 51, 51);">设置为 "disable" 可防止使用 bypassPermissions 模式</font> |
| <code><font style="color:rgb(51, 51, 51);">permissions.disableAutoMode</font></code> | <font style="color:rgb(51, 51, 51);">设置为 "disable" 可防止使用自动模式</font> |

***

## <font style="color:rgb(51, 51, 51);">安全最佳实践</font>

1. **<font style="color:rgb(51, 51, 51);">从限制性开始</font>**<font style="color:rgb(51, 51, 51);">：从最小权限开始，根据需要扩展</font>
2. **<font style="color:rgb(51, 51, 51);">使用沙箱</font>**<font style="color:rgb(51, 51, 51);">：沙箱提供 OS 级别的额外保护，应同时启用</font>
3. **<font style="color:rgb(51, 51, 51);">保护敏感文件</font>**<font style="color:rgb(51, 51, 51);">：使用</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">deny</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">规则阻止访问</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">.env</font></code><font style="color:rgb(51, 51, 51);">、密钥文件等</font>
4. **<font style="color:rgb(51, 51, 51);">限制网络访问</font>**<font style="color:rgb(51, 51, 51);">：仅允许访问必要的域名，防止数据泄露</font>
5. **<font style="color:rgb(51, 51, 51);">避免 bypassPermissions</font>**<font style="color:rgb(51, 51, 51);">：仅在隔离环境（容器、VM）中使用</font>
6. **<font style="color:rgb(51, 51, 51);">使用 auto 模式的 soft_deny</font>**<font style="color:rgb(51, 51, 51);">：提供安全指导而不过度限制</font>
7. **<font style="color:rgb(51, 51, 51);">定期审查配置</font>**<font style="color:rgb(51, 51, 51);">：查看沙箱违规尝试和被拒绝的操作</font>

***<font style="color:rgb(44, 58, 94);">安全警告：</font>***<code>_<font style="color:rgb(44, 58, 94);">bypassPermissions</font>_</code>*<font style="color:rgb(44, 58, 94);"> 模式不提供针对提示注入或意外操作的保护。对于仍维护后台安全检查的更安全替代品，应使用 auto 模式。</font>*

# Claude Code MCP 核心协议配置与业务系统无缝对接

## <font style="color:rgb(51, 51, 51);">Claude Code MCP</font>

<font style="color:rgb(51, 51, 51);">如果说 Claude Code 是一个优秀的打字员（代码生成）和测试员（代码校验），那么加上 MCP（Model Context Protocol，模型上下文协议） 则是让 Claude 真正拥有了外部感官和手脚——它不再局限于当前项目的代码文件，而是能主动连接外部世界的资源与工具，成为你的全链路开发协作伙伴。</font>

![1783649363294-b16596b7-de16-42de-b36b-c78a641ba92c.svg](./img/wf9R51v5S5sXlvV1/1783649363294-b16596b7-de16-42de-b36b-c78a641ba92c-663289.svg)

### <font style="color:rgb(51, 51, 51);">什么是 MCP (Model Context Protocol)？</font>

<font style="color:rgb(51, 51, 51);">MCP 是 Anthropic 推出的一套开放的标准化协议，专为解决AI 与外部工具协作的核心痛点而生。</font>

<font style="color:rgb(51, 51, 51);">MCP 的核心逻辑颠覆了传统思路：不要让 AI 去逐一学习所有工具的使用规则，而是让所有工具都提供一个统一的接口给 AI。</font>

<font style="color:rgb(51, 51, 51);">这个逻辑就像现实中的通用插座——不用让电器适配不同的插座，只要插座统一标准，所有电器都能直接使用。</font>

<font style="color:rgb(51, 51, 51);">连接 MCP 服务器后，你可以让 Claude Code：</font>

* <font style="color:rgb(51, 51, 51);">从 JIRA/工单系统获取需求并开发功能、创建 GitHub PR</font>
* <font style="color:rgb(51, 51, 51);">分析 Sentry 监控数据、定位生产环境错误</font>
* <font style="color:rgb(51, 51, 51);">查询 PostgreSQL/MySQL 等数据库数据</font>
* <font style="color:rgb(51, 51, 51);">基于 Figma 设计更新代码、自动化生成邮件草稿等</font>

![1783649363489-b1d8dcc5-4262-47b2-95ae-6554a662aeb7.png](./img/wf9R51v5S5sXlvV1/1783649363489-b1d8dcc5-4262-47b2-95ae-6554a662aeb7-163362.png)

### <font style="color:rgb(51, 51, 51);">为什么 Claude Code 需要 MCP？</font>

<font style="color:rgb(51, 51, 51);">在没有 MCP 之前，Claude Code 的能力被严格限制在你当前打开的项目文件夹内，就像一个坐井观天的助手，只能看到眼前的代码，无法感知项目之外的任何信息。而 MCP 的出现，彻底打破了这个信息孤岛，让 Claude 能深度参与全流程开发：</font>

<font style="color:rgb(51, 51, 51);">举几个直观的场景对比，你就能快速理解 MCP 的价值：</font>

| <font style="color:rgb(255, 255, 255);">场景</font> | <font style="color:rgb(255, 255, 255);">无 MCP 时</font> | <font style="color:rgb(255, 255, 255);">有 MCP 时</font> |
| --- | --- | --- |
| <font style="color:rgb(51, 51, 51);">跨仓库分析</font> | <font style="color:rgb(51, 51, 51);">只能分析当前文件夹内的代码，无法关联其它仓库</font> | <font style="color:rgb(51, 51, 51);">跨仓库协作："帮我分析仓库 A 的接口文档，然后在仓库 B 中编写对应的调用方法"</font> |
| <font style="color:rgb(51, 51, 51);">需求/讨论同步</font> | <font style="color:rgb(51, 51, 51);">需要你手动把需求文档、团队讨论记录复制粘贴到对话框</font> | <font style="color:rgb(51, 51, 51);">实时同步协作信息："查一下 Slack 里 #feature-x 频道的讨论记录，看看大家对该功能的修改建议"</font> |
| <font style="color:rgb(51, 51, 51);">数据库验证</font> | <font style="color:rgb(51, 51, 51);">无法直接验证代码与数据库的适配性，只能手动查表结构</font> | <font style="color:rgb(51, 51, 51);">直接联动数据库："去查一下 MySQL 中 users 表的结构和前 5 条数据，判断我写的用户查询接口是否匹配"</font> |
| <font style="color:rgb(51, 51, 51);">自动化流程</font> | <font style="color:rgb(51, 51, 51);">只能生成代码片段，供你手动复制使用</font> | <font style="color:rgb(51, 51, 51);">自动化执行："帮我写浏览器自动化脚本，并通过 MCP 调用 Puppeteer 执行，验证登录页面的交互逻辑"</font> |

<font style="color:rgb(51, 51, 51);">简单来说，MCP 让 Claude Code 从被动接收信息的助手，变成了主动获取信息、执行操作的协作伙伴。</font>

***

## <font style="color:rgb(51, 51, 51);">Claude Code 中 MCP 的基本使用方式</font>

<font style="color:rgb(51, 51, 51);">Claude Code 内置了完整的 MCP 管理能力，核心命令只有一个：</font>

claude mcp

<font style="color:rgb(51, 51, 51);">常用子命令:</font>

| <font style="color:rgb(255, 255, 255);">命令</font> | <font style="color:rgb(255, 255, 255);">作用</font> |
| --- | --- |
| <code><font style="color:rgb(51, 51, 51);">claude mcp add</font></code> | <font style="color:rgb(51, 51, 51);">添加一个 MCP 服务器</font> |
| <code><font style="color:rgb(51, 51, 51);">claude mcp list</font></code> | <font style="color:rgb(51, 51, 51);">查看所有已配置服务器</font> |
| <code><font style="color:rgb(51, 51, 51);">claude mcp get <name></font></code> | <font style="color:rgb(51, 51, 51);">查看某个服务器详情</font> |
| <code><font style="color:rgb(51, 51, 51);">claude mcp remove <name></font></code> | <font style="color:rgb(51, 51, 51);">删除服务器</font> |
| <code><font style="color:rgb(51, 51, 51);">/mcp</font></code> | <font style="color:rgb(51, 51, 51);">在 Claude Code 中查看状态 / 认证</font> |

***

## <font style="color:rgb(51, 51, 51);">安装 MCP 服务器</font>

<font style="color:rgb(51, 51, 51);">MCP 服务器支持 HTTP/SSE/stdio 三种接入方式，推荐优先使用 HTTP（SSE已弃用）。</font>

### <font style="color:rgb(51, 51, 51);">1. 远程 HTTP 服务器（推荐）</font>

<font style="color:rgb(51, 51, 51);">适用于云服务类工具，是最通用的方式：</font>

```plain
# 基础语法
claude mcp add --transport http <服务器名称> <服务器URL>

# 示例1：连接Notion
claude mcp add --transport http notion https://mcp.notion.com/mcp

# 示例2：带身份验证的HTTP服务器
claude mcp add --transport http secure-api https://api.example.com/mcp \
  --header "Authorization: Bearer 你的令牌"
```

### <font style="color:rgb(51, 51, 51);">2. 远程 SSE 服务器（已弃用）</font>

<font style="color:rgb(51, 51, 51);">仅兼容旧版工具，优先用 HTTP 替代：</font>

```plain
# 基础语法（仅兼容用）
claude mcp add --transport sse <服务器名称> <服务器URL>
# 示例：连接Asana
claude mcp add --transport sse asana https://mcp.asana.com/sse
```

### <font style="color:rgb(51, 51, 51);">3. 本地 stdio 服务器</font>

<font style="color:rgb(51, 51, 51);">适用于需要本地系统访问的工具（如本地数据库、自定义脚本）：</font>

```plain
# 基础语法（注意：--前是Claude参数，--后是服务器命令）
claude mcp add --transport stdio [--env 环境变量] <服务器名称> -- <启动命令>

# 示例：连接Airtable（需替换自己的API密钥）
claude mcp add --transport stdio --env AIRTABLE_API_KEY=你的密钥 airtable \
  -- npx -y airtable-mcp-server
```

*<font style="color:rgb(44, 58, 94);">关键注意：</font>*<code>_<font style="color:rgb(44, 58, 94);">--transport</font>_</code>*<font style="color:rgb(44, 58, 94);">/</font>*<code>_<font style="color:rgb(44, 58, 94);">--env</font>_</code>*<font style="color:rgb(44, 58, 94);"> </font>**<font style="color:rgb(44, 58, 94);">等参数必须放在服务器名称</font>**__<font style="color:rgb(44, 58, 94);">前面</font>__\_\_<font style="color:rgb(44, 58, 94);">，</font>*<code>_<font style="color:rgb(44, 58, 94);">--</font>_</code>*<font style="color:rgb(44, 58, 94);"> </font>\_\_<font style="color:rgb(44, 58, 94);">用于分隔Claude参数和服务器命令，避免参数冲突。</font>*

## <font style="color:rgb(51, 51, 51);">管理 MCP 服务器</font>

<font style="color:rgb(51, 51, 51);">配置完成后，你可以通过以下命令管理服务器：</font>

```plain
# 列出所有已配置的服务器
claude mcp list

# 查看指定服务器详情（如github）
claude mcp get github

# 删除指定服务器
claude mcp remove github

# 在Claude Code中检查服务器状态
/mcp
```

***

## <font style="color:rgb(51, 51, 51);">配置范围（控制服务器可见性）</font>

<font style="color:rgb(51, 51, 51);">你可以指定 MCP 服务器的生效范围，适配个人/团队使用场景：</font>

| <font style="color:rgb(255, 255, 255);">范围</font> | <font style="color:rgb(255, 255, 255);">用途</font> | <font style="color:rgb(255, 255, 255);">配置命令示例</font> |
| --- | --- | --- |
| <font style="color:rgb(51, 51, 51);">local（默认）</font> | <font style="color:rgb(51, 51, 51);">仅当前项目可用，私密配置（如敏感密钥）</font> | <code><font style="color:rgb(51, 51, 51);">claude mcp add --scope local ...</font></code> |
| <font style="color:rgb(51, 51, 51);">project</font> | <font style="color:rgb(51, 51, 51);">团队共享（存储在.mcp.json，可提交版本库）</font> | <code><font style="color:rgb(51, 51, 51);">claude mcp add --scope project ...</font></code> |
| <font style="color:rgb(51, 51, 51);">user</font> | <font style="color:rgb(51, 51, 51);">所有项目可用（个人全局配置）</font> | <code><font style="color:rgb(51, 51, 51);">claude mcp add --scope user ...</font></code> |

*<font style="color:rgb(44, 58, 94);">优先级：local > project > user（同名服务器，本地配置覆盖共享配置）</font>*

## <font style="color:rgb(51, 51, 51);">实用示例</font>

### <font style="color:rgb(51, 51, 51);">示例 1：GitHub 代码审查</font>

claude mcp add --transport http github https://api.githubcopilot.com/mcp/

<font style="color:rgb(51, 51, 51);">在 Claude Code 中：</font>

```plain
> Review PR #456 and suggest improvements
> Show me all open PRs assigned to me
```

### <font style="color:rgb(51, 51, 51);">示例 2：Sentry 生产环境排错</font>

claude mcp add --transport http sentry https://mcp.sentry.dev/mcp

```plain
> /mcp   # 完成 OAuth 登录
> What are the most common errors in the last 24 hours?
```

### <font style="color:rgb(51, 51, 51);">示例 3：直接查 PostgreSQL</font>

```plain
claude mcp add --transport stdio db \
  -- npx -y @bytebase/dbhub \
  --dsn "postgresql://readonly:pass@prod.db.com:5432/analytics"
```

```plain
> Show me the schema for the orders table
> Which users haven't purchased in 90 days?
```

***

## <font style="color:rgb(51, 51, 51);">在对话中使用 MCP 的高级方式</font>

### <font style="color:rgb(51, 51, 51);">1、使用</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:rgb(51, 51, 51);">@</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">引用 MCP 资源</font>

> Analyze @github:issue://123 and suggest a fix

<font style="color:rgb(51, 51, 51);">支持多个资源对比：</font>

> Compare @postgres:schema://users with @docs:file://user-model

### <font style="color:rgb(51, 51, 51);">2、MCP Prompt 作为斜杠命令</font>

<font style="color:rgb(51, 51, 51);">MCP 可以暴露命令：</font>

```plain
/mcp__github__list_prs
/mcp__jira__create_issue "Login bug" high
```

<font style="color:rgb(51, 51, 51);">Claude 会像执行内置命令一样执行它们。</font>

***

## <font style="color:rgb(51, 51, 51);">关键注意事项</font>

1. **<font style="color:rgb(51, 51, 51);">身份验证</font>**<font style="color:rgb(51, 51, 51);">：远程MCP服务器（如GitHub/Sentry）需在Claude Code中执行</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">/mcp</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">完成OAuth 2.0授权；</font>
2. **<font style="color:rgb(51, 51, 51);">Windows兼容</font>**<font style="color:rgb(51, 51, 51);">：本地stdio服务器若用npx，需加</font><code><font style="color:rgb(51, 51, 51);">cmd /c</font></code><font style="color:rgb(51, 51, 51);">包装（如</font><code><font style="color:rgb(51, 51, 51);">-- cmd /c npx -y 包名</font></code><font style="color:rgb(51, 51, 51);">），否则会报"Connection closed"错误；</font>
3. **<font style="color:rgb(51, 51, 51);">第三方风险</font>**<font style="color:rgb(51, 51, 51);">：使用非官方MCP服务器时，需确认来源可信，避免提示注入/安全风险；</font>
4. **<font style="color:rgb(51, 51, 51);">参数顺序</font>**<font style="color:rgb(51, 51, 51);">：stdio服务器配置时，</font><code><font style="color:rgb(51, 51, 51);">--</font></code><font style="color:rgb(51, 51, 51);"> 前后的参数不可颠倒，否则会执行失败。</font>

<font style="color:rgb(51, 51, 51);"></font>

<font style="color:rgb(51, 51, 51);"></font>

# Claude Code SubAgents 多智能体协同与复杂任务分发

<font style="color:rgb(51, 51, 51);">在 Claude Code 中，你可以创建</font>**<font style="color:rgb(51, 51, 51);">专门的 AI 子代理（Subagent）</font>**<font style="color:rgb(51, 51, 51);">，用于处理特定类型的任务，从而获得更好的上下文隔离、更强的约束控制和更高的执行效率。</font>

<font style="color:rgb(51, 51, 51);">子代理运行在</font>**<font style="color:rgb(51, 51, 51);">独立的上下文窗口</font>**<font style="color:rgb(51, 51, 51);">中，每个子代理都可以拥有独立的系统提示、指定的模型、明确的工具访问权限、独立的权限模式，以及跨会话的持久记忆。当 Claude 判断你的请求符合某个子代理的描述时，会自动将任务委托给它，由子代理独立完成后返回结果。</font>

*<font style="color:rgb(44, 58, 94);">子代理只接收自身的系统提示和基础环境信息（如工作目录），</font>**__<font style="color:rgb(44, 58, 94);">不会继承完整的 Claude Code 系统提示</font>__**<font style="color:rgb(44, 58, 94);">，这保证了行为的纯净和可控。</font>*

***

## <font style="color:rgb(51, 51, 51);">为什么要使用子代理</font>

<font style="color:rgb(51, 51, 51);">子代理的核心价值在于</font>**<font style="color:rgb(51, 51, 51);">隔离 + 专业化</font>**<font style="color:rgb(51, 51, 51);">，主要体现在以下几个方面：</font>

**<font style="color:rgb(51, 51, 51);">保留主对话上下文</font>**<font style="color:rgb(51, 51, 51);">：把探索、日志分析等"重任务"放到子代理中，主对话只接收结论摘要，不被大量中间输出淹没。研究表明，并行运行三个子代理分析 5 万行项目约需 45 秒，而串行执行需要 3 分钟。</font>

**<font style="color:rgb(51, 51, 51);">强制执行约束</font>**<font style="color:rgb(51, 51, 51);">：通过工具白名单或黑名单限制子代理的能力，例如只读分析、禁止执行危险命令。</font>

**<font style="color:rgb(51, 51, 51);">行为专业化</font>**<font style="color:rgb(51, 51, 51);">：为特定领域（代码审查、调试、数据分析）设计专用 AI，在系统提示中明确指出代理的能力边界，避免不必要的调用。</font>

**<font style="color:rgb(51, 51, 51);">控制成本</font>**<font style="color:rgb(51, 51, 51);">：将简单任务交给 Haiku，将复杂分析交给 Sonnet，通过环境变量</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">CLAUDE_CODE_SUBAGENT_MODEL</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">统一设置所有子代理使用的模型。</font>

**<font style="color:rgb(51, 51, 51);">跨项目复用</font>**<font style="color:rgb(51, 51, 51);">：用户级子代理一次配置，所有项目可用。</font>

***

## <font style="color:rgb(51, 51, 51);">子代理 vs 多代理</font>

<font style="color:rgb(51, 51, 51);">这两个概念容易混淆，区别在于任务粒度和运行范围：</font>

| <font style="color:rgb(255, 255, 255);">对比项</font> | <font style="color:rgb(255, 255, 255);">子代理（Subagent）</font> | <font style="color:rgb(255, 255, 255);">多代理（Multi-agent）</font> |
| --- | --- | --- |
| <font style="color:rgb(51, 51, 51);">运行范围</font> | <font style="color:rgb(51, 51, 51);">在单个 Claude Code 会话内启动，处理子任务后返回结果</font> | <font style="color:rgb(51, 51, 51);">多个 Claude Code 会话并行或串行运行，通常由编排器管理</font> |
| <font style="color:rgb(51, 51, 51);">上下文</font> | <font style="color:rgb(51, 51, 51);">独立上下文窗口，与主对话隔离</font> | <font style="color:rgb(51, 51, 51);">各会话上下文完全独立</font> |
| <font style="color:rgb(51, 51, 51);">嵌套</font> | <font style="color:rgb(51, 51, 51);">子代理不能再创建子代理（需嵌套时使用 Skills）</font> | <font style="color:rgb(51, 51, 51);">可由编排器协调多层级任务</font> |
| <font style="color:rgb(51, 51, 51);">适用场景</font> | <font style="color:rgb(51, 51, 51);">聚焦子任务、大量输出隔离、专业分析</font> | <font style="color:rgb(51, 51, 51);">全功能开发流水线（设计 → 实现 → 测试 → 发布）</font> |

***

## <font style="color:rgb(51, 51, 51);">内置子代理</font>

<font style="color:rgb(51, 51, 51);">Claude Code 已内置多种子代理，通常会自动使用，无需手动配置。</font>

### <font style="color:rgb(51, 51, 51);">1、Explore（探索代理）</font>

<font style="color:rgb(51, 51, 51);">用于只读搜索与分析代码库。模型默认使用 Haiku（速度快、延迟低），只开放只读工具（不能 Edit / Write）。当 Claude 需要查看代码但不修改代码时，会自动使用 Explore 代理。支持不同探索深度：</font><code><font style="color:rgb(51, 51, 51);">quick</font></code><font style="color:rgb(51, 51, 51);">、</font><code><font style="color:rgb(51, 51, 51);">medium</font></code><font style="color:rgb(51, 51, 51);">、</font><code><font style="color:rgb(51, 51, 51);">very thorough</font></code><font style="color:rgb(51, 51, 51);">。</font>

### <font style="color:rgb(51, 51, 51);">2、Plan（规划代理）</font>

<font style="color:rgb(51, 51, 51);">在计划模式下收集代码库信息，帮助 Claude 理解项目结构，为后续方案制定积累上下文。只开放只读工具，在不产生嵌套代理的前提下安全地收集规划所需信息。</font>

### <font style="color:rgb(51, 51, 51);">3、General-purpose（通用代理）</font>

<font style="color:rgb(51, 51, 51);">用于复杂、多步骤任务，开放全部工具，继承主对话的模型。适合"看 + 改 + 推理"的综合场景，以及需要多步骤代码修改的任务。</font>

### <font style="color:rgb(51, 51, 51);">4、其他内部代理</font>

| <font style="color:rgb(255, 255, 255);">代理名称</font> | <font style="color:rgb(255, 255, 255);">说明</font> |
| --- | --- |
| <font style="color:rgb(51, 51, 51);">Bash</font> | <font style="color:rgb(51, 51, 51);">在独立上下文中运行 Shell 命令</font> |
| <font style="color:rgb(51, 51, 51);">statusline-setup</font> | <font style="color:rgb(51, 51, 51);">配置终端状态栏显示</font> |
| <font style="color:rgb(51, 51, 51);">Claude Code Guide</font> | <font style="color:rgb(51, 51, 51);">解答 Claude Code 使用相关问题</font> |

***

## <font style="color:rgb(51, 51, 51);">创建你的第一个子代理</font>

### <font style="color:rgb(51, 51, 51);">1、打开子代理管理界面</font>

<font style="color:rgb(51, 51, 51);">在 Claude Code 中执行以下命令，打开完整的子代理管理界面：</font>

/agents

<font style="color:rgb(51, 51, 51);">该界面提供所有子代理管理能力：查看全部可用代理（内置 / 用户级 / 项目级 / 插件）、创建新代理、编辑已有代理，以及在同名冲突时查看哪个版本实际生效。</font>

### <font style="color:rgb(51, 51, 51);">2、选择创建用户级子代理</font>

<font style="color:rgb(51, 51, 51);">在界面中选择</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:rgb(51, 51, 51);">Create new agent</font>**<font style="color:rgb(51, 51, 51);">:</font>

![1783649567610-839789c1-8f77-490e-8fe1-86b814adbb54.png](./img/wf9R51v5S5sXlvV1/1783649567610-839789c1-8f77-490e-8fe1-86b814adbb54-297609.png)

<font style="color:rgb(51, 51, 51);">然后选择</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:rgb(51, 51, 51);">Project (.claude/agents/)</font>**<font style="color:rgb(51, 51, 51);">，代理文件会保存到当前目录的 .claude/agents/ 目录下，如果选择</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">~/.claude/agents/</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">目录，则对所有项目生效：</font>

![1783649567615-77eee398-ff87-440b-81ed-86aace2e78c8.png](./img/wf9R51v5S5sXlvV1/1783649567615-77eee398-ff87-440b-81ed-86aace2e78c8-152228.png)

<font style="color:rgb(51, 51, 51);">使用 Claude 推荐的：</font>

![1783649567734-40e5bb7a-e69f-4171-9c7f-e63fec8edced.png](./img/wf9R51v5S5sXlvV1/1783649567734-40e5bb7a-e69f-4171-9c7f-e63fec8edced-393535.png)

### <font style="color:rgb(51, 51, 51);">3、描述代理的职责</font>

<font style="color:rgb(51, 51, 51);">我们可以直接用自然语言告诉 Claude 这个代理要做什么，Claude 会自动生成系统提示和初始配置。例如：</font>

```plain
一个代码改进代理，扫描项目文件，
针对可读性、性能和最佳实践提出建议，
并给出改进示例。
```

![1783649567600-3d214bba-4854-4d46-8e83-f70ac246b626.png](./img/wf9R51v5S5sXlvV1/1783649567600-3d214bba-4854-4d46-8e83-f70ac246b626-364831.png)

<font style="color:rgb(51, 51, 51);">生成完成后，按</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">e</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">键可以手动编辑所有配置内容。</font>

### <font style="color:rgb(51, 51, 51);">4、配置工具权限与模型</font>

* <font style="color:rgb(51, 51, 51);">只做代码审查 → 仅勾选只读工具（Read / Grep / Glob）</font>
* <font style="color:rgb(51, 51, 51);">需要修改代码 → 保留 Edit / Write 工具</font>
* <font style="color:rgb(51, 51, 51);">模型推荐选择</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:rgb(51, 51, 51);">Sonnet</font>**<font style="color:rgb(51, 51, 51);">，分析能力与执行速度较为均衡</font>

<font style="color:rgb(51, 51, 51);">直接选 Contiune 然后回车：</font>

![1783649567412-48eeacc1-3ae2-4dff-ac18-471146c8ca7c.png](./img/wf9R51v5S5sXlvV1/1783649567412-48eeacc1-3ae2-4dff-ac18-471146c8ca7c-229306.png)

<font style="color:rgb(51, 51, 51);">接下来的选默认回车就好。</font>

### <font style="color:rgb(51, 51, 51);">5、选择记忆范围（可选）</font>

* <font style="color:rgb(51, 51, 51);">选择</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:rgb(51, 51, 51);">User</font>**<font style="color:rgb(51, 51, 51);">：在</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">~/.claude/agent-memory/</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">建立持久记忆，跨所有项目积累经验</font>
* <font style="color:rgb(51, 51, 51);">选择</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:rgb(51, 51, 51);">None</font>**<font style="color:rgb(51, 51, 51);">：不保留学习成果，每次任务从零开始</font>

![1783649568281-4edea0d3-aa2d-4038-b0bf-64a8312c6e66.png](./img/wf9R51v5S5sXlvV1/1783649568281-4edea0d3-aa2d-4038-b0bf-64a8312c6e66-982463.png)

### <font style="color:rgb(51, 51, 51);">6、使用刚创建的代理</font>

使用 code-improver 子代理为此项目提出改进建议

![1783649568577-6d71135c-bfa6-41aa-aca5-4fbeabe5e95f.png](./img/wf9R51v5S5sXlvV1/1783649568577-6d71135c-bfa6-41aa-aca5-4fbeabe5e95f-159735.png)

<font style="color:rgb(51, 51, 51);">代理会在独立上下文中运行，完成后将结果摘要返回给主对话。</font>

***

## <font style="color:rgb(51, 51, 51);">子代理的作用范围</font>

<font style="color:rgb(51, 51, 51);">子代理本质上是带 YAML frontmatter 的 Markdown 文件，存放位置决定了它的作用范围和优先级：</font>

| <font style="color:rgb(255, 255, 255);">存放位置</font> | <font style="color:rgb(255, 255, 255);">作用范围</font> | <font style="color:rgb(255, 255, 255);">优先级</font> |
| --- | --- | --- |
| <font style="color:rgb(51, 51, 51);">CLI</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">--agents</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">标志</font> | <font style="color:rgb(51, 51, 51);">仅当前会话</font> | <font style="color:rgb(51, 51, 51);">最高</font> |
| <code><font style="color:rgb(51, 51, 51);">.claude/agents/</font></code> | <font style="color:rgb(51, 51, 51);">当前项目</font> | <font style="color:rgb(51, 51, 51);">高</font> |
| <code><font style="color:rgb(51, 51, 51);">~/.claude/agents/</font></code> | <font style="color:rgb(51, 51, 51);">所有项目（全局）</font> | <font style="color:rgb(51, 51, 51);">中</font> |
| <font style="color:rgb(51, 51, 51);">插件 agents</font> | <font style="color:rgb(51, 51, 51);">插件作用域</font> | <font style="color:rgb(51, 51, 51);">最低</font> |

<font style="color:rgb(51, 51, 51);">当同名子代理在不同位置都存在时，优先级高的会覆盖低的。可通过</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">/agents</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">命令查看当前哪个版本实际生效。</font>

<font style="color:rgb(51, 51, 51);">选择存放位置的建议：项目代理（</font><code><font style="color:rgb(51, 51, 51);">.claude/agents/</font></code><font style="color:rgb(51, 51, 51);">）可以跟随代码一起提交，让团队共享；用户代理（</font><code><font style="color:rgb(51, 51, 51);">~/.claude/agents/</font></code><font style="color:rgb(51, 51, 51);">）存放个人习惯与通用工具，跨项目生效；CLI 代理（</font><code><font style="color:rgb(51, 51, 51);">--agents</font></code><font style="color:rgb(51, 51, 51);">）用于临时测试或自动化脚本，不保留到磁盘。</font>

***

## <font style="color:rgb(51, 51, 51);">配置文件结构</font>

<font style="color:rgb(51, 51, 51);">每个子代理配置文件由两部分组成：YAML frontmatter（元数据与配置）和 Markdown 正文（系统提示）。</font>

**<font style="color:rgb(97, 127, 16);">实例</font>**

<font style="color:cyan;">---</font><font style="color:green;">\
</font><font style="color:green;">name</font>**<font style="color:brown;">:</font>\*\*\*\*<font style="color:brown;"> </font>**<font style="color:rgb(51, 51, 51);">code-reviewer                    </font><font style="color:blue;"># 必填：唯一标识，小写字母 + 连字符</font><font style="color:green;">\
</font><font style="color:green;">description</font>**<font style="color:brown;">:</font>\*\*\*\*<font style="color:brown;"> </font>**<font style="color:rgb(51, 51, 51);">Reviews code for quality, best practices, and security issues.\
</font><font style="color:rgb(51, 51, 51);">Invoke when the user asks to review, audit, or check code quality.\
</font><font style="color:blue;"># 必填：决定 Claude 何时自动调用此代理，建议写成"何时调用 + 能做什么"</font><font style="color:green;">\
</font><font style="color:green;">tools</font>**<font style="color:brown;">:</font>\*\*\*\*<font style="color:brown;"> </font>**<font style="color:rgb(51, 51, 51);">Read, Grep, Glob                </font><font style="color:blue;"># 工具白名单（只能使用这些工具）</font><font style="color:green;">\
</font><font style="color:green;">model</font>**<font style="color:brown;">:</font>\*\*\*\*<font style="color:brown;"> </font>**<font style="color:rgb(51, 51, 51);">sonnet                          </font><font style="color:blue;"># 指定模型：haiku / sonnet / opus / inherit</font><font style="color:green;">\
</font><font style="color:green;">permissionMode</font>**<font style="color:brown;">:</font>\*\*\*\*<font style="color:brown;"> </font>**<font style="color:rgb(51, 51, 51);">default                </font><font style="color:blue;"># 权限模式（见下方权限模式章节）</font><font style="color:green;">\
</font><font style="color:green;">memory</font>**<font style="color:brown;">:</font>\*\*\*\*<font style="color:brown;"> </font>**<font style="color:rgb(51, 51, 51);">project                        </font><font style="color:blue;"># 持久记忆范围（见下方记忆章节）</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:cyan;">---</font><font style="color:rgb(51, 51, 51);">

</font><font style="color:rgb(51, 51, 51);">You are a senior code reviewer.</font><font style="color:green;">\
</font><font style="color:green;">Analyze code and provide actionable feedback organized by severity</font>**<font style="color:brown;">:</font>\*\*\*\*<font style="color:brown;"> </font>**<font style="color:rgb(51, 51, 51);">Critical / Major / Minor.

</font><font style="color:rgb(51, 51, 51);">Update your agent memory with recurring patterns, conventions, and known issues you discover.</font>

### <font style="color:rgb(51, 51, 51);">完整字段说明</font>

| <font style="color:rgb(255, 255, 255);">字段</font> | <font style="color:rgb(255, 255, 255);">是否必填</font> | <font style="color:rgb(255, 255, 255);">说明</font> |
| --- | --- | --- |
| <code><font style="color:rgb(51, 51, 51);">name</font></code> | <font style="color:rgb(51, 51, 51);">必填</font> | <font style="color:rgb(51, 51, 51);">唯一标识，也是显式调用时的名称。格式：小写字母 + 连字符，如</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">code-reviewer</font></code> |
| <code><font style="color:rgb(51, 51, 51);">description</font></code> | <font style="color:rgb(51, 51, 51);">必填</font> | **<font style="color:rgb(51, 51, 51);">最重要的字段</font>**<font style="color:rgb(51, 51, 51);">，Claude 是否以及何时自动调用该代理完全依赖于此，务必写清楚使用场景</font> |
| <code><font style="color:rgb(51, 51, 51);">tools</font></code> | <font style="color:rgb(51, 51, 51);">可选</font> | <font style="color:rgb(51, 51, 51);">工具白名单；设置后只能使用列出的工具，MCP 工具也会被排除</font> |
| <code><font style="color:rgb(51, 51, 51);">disallowedTools</font></code> | <font style="color:rgb(51, 51, 51);">可选</font> | <font style="color:rgb(51, 51, 51);">工具黑名单；继承主对话全部工具，但排除列出的工具（MCP 工具保留）</font> |
| <code><font style="color:rgb(51, 51, 51);">model</font></code> | <font style="color:rgb(51, 51, 51);">可选</font> | <font style="color:rgb(51, 51, 51);">指定模型，可填</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">haiku</font></code><br/><font style="color:rgb(51, 51, 51);">、</font><code><font style="color:rgb(51, 51, 51);">sonnet</font></code><br/><font style="color:rgb(51, 51, 51);">、</font><code><font style="color:rgb(51, 51, 51);">opus</font></code><br/><font style="color:rgb(51, 51, 51);">、完整模型 ID，或</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">inherit</font></code><br/><font style="color:rgb(51, 51, 51);">（默认，继承主对话）</font> |
| <code><font style="color:rgb(51, 51, 51);">permissionMode</font></code> | <font style="color:rgb(51, 51, 51);">可选</font> | <font style="color:rgb(51, 51, 51);">权限行为控制，见下方权限模式章节</font> |
| <code><font style="color:rgb(51, 51, 51);">memory</font></code> | <font style="color:rgb(51, 51, 51);">可选</font> | <font style="color:rgb(51, 51, 51);">持久记忆范围：</font><code><font style="color:rgb(51, 51, 51);">user</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">/</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">project</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">/</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">local</font></code><br/><font style="color:rgb(51, 51, 51);">，见下方记忆章节</font> |
| <code><font style="color:rgb(51, 51, 51);">background</font></code> | <font style="color:rgb(51, 51, 51);">可选</font> | <font style="color:rgb(51, 51, 51);">设为</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">true</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">时，该代理始终以后台方式运行（不阻塞主对话）</font> |
| <code><font style="color:rgb(51, 51, 51);">isolation</font></code> | <font style="color:rgb(51, 51, 51);">可选</font> | <font style="color:rgb(51, 51, 51);">设为</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">worktree</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">时，在临时 git worktree 中运行，与主仓库完全隔离</font> |
| <code><font style="color:rgb(51, 51, 51);">skills</font></code> | <font style="color:rgb(51, 51, 51);">可选</font> | <font style="color:rgb(51, 51, 51);">在此代理启动时自动加载的 Skills 列表</font> |
| <code><font style="color:rgb(51, 51, 51);">hooks</font></code> | <font style="color:rgb(51, 51, 51);">可选</font> | <font style="color:rgb(51, 51, 51);">生命周期钩子：</font><code><font style="color:rgb(51, 51, 51);">SubagentStart</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">/</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">SubagentStop</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">/</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">PreToolUse</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">/</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">PostToolUse</font></code> |

### <font style="color:rgb(51, 51, 51);">tools 与 disallowedTools 的区别</font>

| <font style="color:rgb(255, 255, 255);">配置方式</font> | <font style="color:rgb(255, 255, 255);">行为</font> | <font style="color:rgb(255, 255, 255);">典型场景</font> |
| --- | --- | --- |
| <font style="color:rgb(51, 51, 51);">两者均不设置</font> | <font style="color:rgb(51, 51, 51);">继承主对话全部工具，含 MCP 工具</font> | <font style="color:rgb(51, 51, 51);">通用代理，不需要限制</font> |
| <font style="color:rgb(51, 51, 51);">仅设置</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">tools</font></code> | <font style="color:rgb(51, 51, 51);">只能使用白名单内的工具，MCP 工具被排除</font> | <font style="color:rgb(51, 51, 51);">只读分析代理、严格约束场景</font> |
| <font style="color:rgb(51, 51, 51);">仅设置</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">disallowedTools</font></code> | <font style="color:rgb(51, 51, 51);">继承全部工具，排除黑名单工具，MCP 工具保留</font> | <font style="color:rgb(51, 51, 51);">保留 MCP 能力但禁止写操作</font> |
| <font style="color:rgb(51, 51, 51);">两者同时设置</font> | <font style="color:rgb(51, 51, 51);">先应用</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">disallowedTools</font></code><br/><font style="color:rgb(51, 51, 51);">，再从剩余工具中按</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">tools</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">筛选</font> | <font style="color:rgb(51, 51, 51);">精细控制工具访问</font> |

**<font style="color:rgb(97, 127, 16);">实例</font>**

<font style="color:blue;"># 示例一：只允许只读操作（使用 tools 白名单）</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:cyan;">---</font><font style="color:green;">\
</font><font style="color:green;">name</font>**<font style="color:brown;">:</font>\*\*\*\*<font style="color:brown;"> </font>**<font style="color:rgb(51, 51, 51);">safe-researcher</font><font style="color:green;">\
</font><font style="color:green;">description</font>**<font style="color:brown;">:</font>\*\*\*\*<font style="color:brown;"> </font>**<font style="color:rgb(51, 51, 51);">Research agent with read-only access. Use when analyzing code without making changes.</font><font style="color:green;">\
</font><font style="color:green;">tools</font>**<font style="color:brown;">:</font>\*\*\*\*<font style="color:brown;"> </font>**<font style="color:rgb(51, 51, 51);">Read, Grep, Glob, Bash    </font><font style="color:blue;"># 只开放这四个工具，Write 和 Edit 不在白名单内无法使用</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:cyan;">---</font>

**<font style="color:rgb(97, 127, 16);">实例</font>**

<font style="color:blue;"># 示例二：继承所有工具但禁止写文件（使用 disallowedTools 黑名单）</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:cyan;">---</font><font style="color:green;">\
</font><font style="color:green;">name</font>**<font style="color:brown;">:</font>\*\*\*\*<font style="color:brown;"> </font>**<font style="color:rgb(51, 51, 51);">no-writes</font><font style="color:green;">\
</font><font style="color:green;">description</font>**<font style="color:brown;">:</font>\*\*\*\*<font style="color:brown;"> </font>**<font style="color:rgb(51, 51, 51);">Analysis agent that inherits</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:rgb(51, 51, 51);">all</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">tools except file writes.</font><font style="color:green;">\
</font><font style="color:green;">disallowedTools</font>**<font style="color:brown;">:</font>\*\*\*\*<font style="color:brown;"> </font>**<font style="color:rgb(51, 51, 51);">Write, Edit    </font><font style="color:rgb(51, 51, 51);"> </font><font style="color:blue;"># 保留 MCP 工具，仅排除 Write 和 Edit</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:cyan;">---</font>

***

## <font style="color:rgb(51, 51, 51);">权限模式</font>

<font style="color:rgb(51, 51, 51);">通过</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">permissionMode</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">字段控制子代理执行操作时的权限行为：</font>

| <font style="color:rgb(255, 255, 255);">模式</font> | <font style="color:rgb(255, 255, 255);">行为</font> | <font style="color:rgb(255, 255, 255);">适用场景</font> |
| --- | --- | --- |
| <code><font style="color:rgb(51, 51, 51);">default</font></code> | <font style="color:rgb(51, 51, 51);">正常权限提示，每次操作前询问用户</font> | <font style="color:rgb(51, 51, 51);">通用场景，推荐默认值</font> |
| <code><font style="color:rgb(51, 51, 51);">acceptEdits</font></code> | <font style="color:rgb(51, 51, 51);">自动接受文件编辑，无需每次确认</font> | <font style="color:rgb(51, 51, 51);">频繁改动文件的代理，减少交互中断</font> |
| <code><font style="color:rgb(51, 51, 51);">dontAsk</font></code> | <font style="color:rgb(51, 51, 51);">自动拒绝未授权操作，不中断执行流程</font> | <font style="color:rgb(51, 51, 51);">严格只读场景，操作失败时静默跳过</font> |
| <code><font style="color:rgb(51, 51, 51);">bypassPermissions</font></code> | <font style="color:rgb(51, 51, 51);">跳过所有权限检查，直接执行</font> | <font style="color:rgb(51, 51, 51);">仅限完全可信、受控的自动化环境</font> |
| <code><font style="color:rgb(51, 51, 51);">plan</font></code> | <font style="color:rgb(51, 51, 51);">只读规划模式，不执行任何写操作</font> | <font style="color:rgb(51, 51, 51);">方案制定、架构分析</font> |

<code>_<font style="color:rgb(44, 58, 94);">bypassPermissions</font>_</code>*<font style="color:rgb(44, 58, 94);"> </font>**<font style="color:rgb(44, 58, 94);">只适合完全可信的子代理。另外，子代理会</font>**__<font style="color:rgb(44, 58, 94);">继承父会话的权限模式</font>__\_\_<font style="color:rgb(44, 58, 94);">——如果主会话开启了 bypass，所有子代理也会跟着 bypass，使用时请格外谨慎。</font>*

***

## <font style="color:rgb(51, 51, 51);">持久记忆（Memory）</font>

<font style="color:rgb(51, 51, 51);">通过</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">memory</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">字段，子代理可以在会话之间积累知识，例如代码库规律、调试经验、架构决策等，无需每次重新探索。</font>

| <font style="color:rgb(255, 255, 255);">范围值</font> | <font style="color:rgb(255, 255, 255);">存储位置</font> | <font style="color:rgb(255, 255, 255);">适用场景</font> |
| --- | --- | --- |
| <code><font style="color:rgb(51, 51, 51);">user</font></code> | <code><font style="color:rgb(51, 51, 51);">~/.claude/agent-memory/<name>/</font></code> | <font style="color:rgb(51, 51, 51);">代理的知识适用于所有项目，如通用代码审查规范</font> |
| <code><font style="color:rgb(51, 51, 51);">project</font></code> | <code><font style="color:rgb(51, 51, 51);">.claude/agent-memory/<name>/</font></code> | <font style="color:rgb(51, 51, 51);">知识与项目绑定，可通过 git 在团队间共享（推荐默认值）</font> |
| <code><font style="color:rgb(51, 51, 51);">local</font></code> | <code><font style="color:rgb(51, 51, 51);">.claude/agent-memory-local/<name>/</font></code> | <font style="color:rgb(51, 51, 51);">知识与项目绑定但不提交 git，仅存储个人本地经验</font> |

**<font style="color:rgb(97, 127, 16);">实例</font>**

<font style="color:cyan;">---</font><font style="color:green;">\
</font><font style="color:green;">name</font>**<font style="color:brown;">:</font>\*\*\*\*<font style="color:brown;"> </font>**<font style="color:rgb(51, 51, 51);">code-reviewer</font><font style="color:green;">\
</font><font style="color:green;">description</font>**<font style="color:brown;">:</font>\*\*\*\*<font style="color:brown;"> </font>**<font style="color:rgb(51, 51, 51);">Reviews code for quality and best practices. Invoke when reviewing code changes.</font><font style="color:green;">\
</font><font style="color:green;">memory</font>**<font style="color:brown;">:</font>\*\*\*\*<font style="color:brown;"> </font>**<font style="color:rgb(51, 51, 51);">user    </font><font style="color:blue;"># 用户级记忆：跨项目积累审查经验</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:cyan;">---</font><font style="color:rgb(51, 51, 51);">

</font><font style="color:rgb(51, 51, 51);">You are a code reviewer.\
</font><font style="color:rgb(51, 51, 51);">As you review code, update your agent memory with patterns, conventions,\
</font><font style="color:rgb(51, 51, 51);">and recurring issues you discover in this codebase.</font>

<font style="color:rgb(51, 51, 51);">在对话中控制记忆的使用方式：</font>

* <font style="color:rgb(51, 51, 51);">任务开始前：</font><code><font style="color:rgb(51, 51, 51);">请先查阅你的记忆，再开始审查</font></code><font style="color:rgb(51, 51, 51);">（让代理利用已有经验）</font>
* <font style="color:rgb(51, 51, 51);">任务结束后：</font><code><font style="color:rgb(51, 51, 51);">任务完成后，把你发现的规律保存到记忆中</font></code><font style="color:rgb(51, 51, 51);">（持续积累）</font>
* <font style="color:rgb(51, 51, 51);">也可直接在系统提示中写入"主动维护记忆"的指令，让代理自动执行，无需每次手动提醒</font>

***

## <font style="color:rgb(51, 51, 51);">worktree 隔离模式</font>

<font style="color:rgb(51, 51, 51);">设置</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">isolation: worktree</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">后，子代理会在临时 git worktree 中运行，与主仓库完全隔离。适合以下场景：</font>

* <font style="color:rgb(51, 51, 51);">需要大量文件修改但不确定结果的探索性任务</font>
* <font style="color:rgb(51, 51, 51);">并行跑多个方案对比，互不干扰</font>
* <font style="color:rgb(51, 51, 51);">自动化测试、CI 验证等需要干净环境的操作</font>

<font style="color:rgb(97, 127, 16);">实例</font>

<font style="color:cyan;">---</font><font style="color:green;">\
</font><font style="color:green;">name</font>**<font style="color:brown;">:</font>\*\*\*\*<font style="color:brown;"> </font>**<font style="color:rgb(51, 51, 51);">experimental-refactor</font><font style="color:green;">\
</font><font style="color:green;">description</font>**<font style="color:brown;">:</font>\*\*\*\*<font style="color:brown;"> </font>**<font style="color:rgb(51, 51, 51);">Tries refactoring approaches in an isolated worktree.\
</font><font style="color:rgb(51, 51, 51);">Use when exploring risky refactoring that shouldn't affect main branch.</font><font style="color:green;">\
</font><font style="color:green;">isolation</font>**<font style="color:brown;">:</font>\*\*\*\*<font style="color:brown;"> </font>**<font style="color:rgb(51, 51, 51);">worktree    </font><font style="color:blue;"># 在临时 worktree 中运行，修改不影响主仓库</font><font style="color:green;">\
</font><font style="color:green;">tools</font>**<font style="color:brown;">:</font>\*\*\*\*<font style="color:brown;"> </font>**<font style="color:rgb(51, 51, 51);">Read, Write, Edit, Bash\
</font><font style="color:cyan;">---</font><font style="color:rgb(51, 51, 51);">

</font><font style="color:rgb(51, 51, 51);">You are a refactoring agent working in an isolated environment.\
</font><font style="color:rgb(51, 51, 51);">Feel free to make changes—they won't affect the main branch.\
</font><font style="color:rgb(51, 51, 51);">Summarize what you changed and whether the approach was successful.</font>

***

## <font style="color:rgb(51, 51, 51);">后台运行（Background）</font>

<font style="color:rgb(51, 51, 51);">子代理支持前台和后台两种运行方式，行为不同：</font>

| <font style="color:rgb(255, 255, 255);">运行方式</font> | <font style="color:rgb(255, 255, 255);">行为</font> | <font style="color:rgb(255, 255, 255);">限制</font> |
| --- | --- | --- |
| **<font style="color:rgb(51, 51, 51);">前台（Foreground）</font>** | <font style="color:rgb(51, 51, 51);">阻塞主对话直到完成，权限提示和澄清问题会实时传给用户</font> | <font style="color:rgb(51, 51, 51);">无特殊限制</font> |
| **<font style="color:rgb(51, 51, 51);">后台（Background）</font>** | <font style="color:rgb(51, 51, 51);">并行执行，不打断主对话；启动前会预先确认所需权限</font> | <font style="color:rgb(51, 51, 51);">无法使用 MCP，无法进行交互式澄清；权限不足时任务失败而非暂停等待</font> |

<font style="color:rgb(51, 51, 51);">Claude 会根据任务特性自动判断使用前台还是后台。你也可以手动控制：</font>

* <code><font style="color:rgb(51, 51, 51);">Ctrl + B</font></code><font style="color:rgb(51, 51, 51);">：将当前运行的子代理切换到后台</font>
* <code><font style="color:rgb(51, 51, 51);">Ctrl + F</font></code><font style="color:rgb(51, 51, 51);">（按两次确认）：终止所有后台代理</font>
* <font style="color:rgb(51, 51, 51);">在 frontmatter 中设置</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">background: true</font></code><font style="color:rgb(51, 51, 51);">：该代理始终以后台方式运行</font>
* <font style="color:rgb(51, 51, 51);">消息开头加</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">&</font></code><font style="color:rgb(51, 51, 51);">：将该任务作为后台任务发送给 claude.ai 网页端</font>
* <font style="color:rgb(51, 51, 51);">通过</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">/tasks</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">命令随时查看后台任务进度</font>

<font style="color:rgb(51, 51, 51);">如需彻底禁用后台任务功能，设置以下环境变量：</font>

export CLAUDE_CODE_DISABLE_BACKGROUND_TASKS=1

<font style="color:rgb(51, 51, 51);">如需统一设置所有子代理使用的模型（例如主对话用 Opus 做复杂推理，子代理用 Sonnet 节省成本）：</font>

export CLAUDE_CODE_SUBAGENT_MODEL="claude-sonnet-4-6"

***

## <font style="color:rgb(51, 51, 51);">生命周期钩子（Hooks）</font>

<font style="color:rgb(51, 51, 51);">子代理支持以下钩子事件，可用于日志记录、操作验证、结果通知等自动化场景：</font>

| <font style="color:rgb(255, 255, 255);">钩子事件</font> | <font style="color:rgb(255, 255, 255);">触发时机</font> | <font style="color:rgb(255, 255, 255);">典型用途</font> |
| --- | --- | --- |
| <code><font style="color:rgb(51, 51, 51);">SubagentStart</font></code> | <font style="color:rgb(51, 51, 51);">子代理启动时</font> | <font style="color:rgb(51, 51, 51);">记录启动日志、初始化环境</font> |
| <code><font style="color:rgb(51, 51, 51);">SubagentStop</font></code> | <font style="color:rgb(51, 51, 51);">子代理任务完成时</font> | <font style="color:rgb(51, 51, 51);">记录结果、触发下游任务、发送通知。包含</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">agent_id</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">和</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">agent_transcript_path</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">字段</font> |
| <code><font style="color:rgb(51, 51, 51);">PreToolUse</font></code> | <font style="color:rgb(51, 51, 51);">工具调用前</font> | <font style="color:rgb(51, 51, 51);">校验操作合法性，脚本退出码为 2 时可阻止该工具调用</font> |
| <code><font style="color:rgb(51, 51, 51);">PostToolUse</font></code> | <font style="color:rgb(51, 51, 51);">工具调用后</font> | <font style="color:rgb(51, 51, 51);">格式化输出、生成变更记录</font> |

<font style="color:rgb(51, 51, 51);">高级用法：通过</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">PreToolUse</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">钩子动态控制工具行为。例如，让数据库代理只允许执行只读 SQL 查询，任何写操作都被脚本拦截：</font>

**<font style="color:rgb(97, 127, 16);">实例</font>**

<font style="color:cyan;">---</font><font style="color:green;">\
</font><font style="color:green;">name</font>**<font style="color:brown;">:</font>\*\*\*\*<font style="color:brown;"> </font>**<font style="color:rgb(51, 51, 51);">db-analyst</font><font style="color:green;">\
</font><font style="color:green;">description</font>**<font style="color:brown;">:</font>\*\*\*\*<font style="color:brown;"> </font>**<font style="color:rgb(51, 51, 51);">Read-only database analysis agent. Use for querying and reporting, never for writes.</font><font style="color:green;">\
</font><font style="color:green;">tools</font>**<font style="color:brown;">:</font>\*\*\*\*<font style="color:brown;"> </font>**<font style="color:rgb(51, 51, 51);">Bash\
</font><font style="color:blue;"># 在 .claude/settings.json 中配置钩子：</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:blue;"># PreToolUse on Bash -> validate-readonly-query.sh</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:blue;"># 脚本检测到非 SELECT 操作时以退出码 2 返回，阻止该命令执行</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:cyan;">---</font><font style="color:rgb(51, 51, 51);">

</font><font style="color:rgb(51, 51, 51);">You are a database analyst. Only run SELECT queries.\
</font><font style="color:rgb(51, 51, 51);">Never run INSERT, UPDATE, DELETE, DROP, or</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:rgb(51, 51, 51);">any</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">DDL statements.</font>

***

## <font style="color:rgb(51, 51, 51);">禁用特定子代理</font>

<font style="color:rgb(51, 51, 51);">如果你不希望 Claude 自动调用某个内置子代理，可以在</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">.claude/settings.json</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">中将其加入禁用列表：</font>

<font style="color:rgb(97, 127, 16);">实例</font>

<font style="color:rgb(51, 51, 51);">{\
</font><font style="color:rgb(51, 51, 51);">"subagents": {\
</font><font style="color:rgb(51, 51, 51);">"deny": \["explore", "plan"]    // 禁用 explore 和 plan 内置代理\
</font><font style="color:rgb(51, 51, 51);">// 禁用后 Claude 不会自动调用它们，但你仍可手动显式调用\
</font><font style="color:rgb(51, 51, 51);">}\
</font><font style="color:rgb(51, 51, 51);">}</font>

***

## <font style="color:rgb(51, 51, 51);">如何调用子代理</font>

### <font style="color:rgb(51, 51, 51);">1、自动委托</font>

<font style="color:rgb(51, 51, 51);">Claude 会根据</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">description</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">字段自动判断任务是否适合某个子代理，无需在提示中手动指定：</font>

帮我检查最近的代码改动质量

### <font style="color:rgb(51, 51, 51);">2、显式调用</font>

<font style="color:rgb(51, 51, 51);">在提示中明确指定要使用哪个代理：</font>

让 code-reviewer 子代理检查最近的改动

***

## <font style="color:rgb(51, 51, 51);">典型使用模式</font>

### <font style="color:rgb(51, 51, 51);">1、隔离高输出任务</font>

<font style="color:rgb(51, 51, 51);">将产生大量中间输出的任务（如运行测试、扫描日志）放到子代理中，主对话只接收精简的结论：</font>

使用子代理运行所有测试，只返回失败的测试和根因分析

### <font style="color:rgb(51, 51, 51);">2、并行研究</font>

<font style="color:rgb(51, 51, 51);">同时启动多个子代理处理不同模块，大幅缩短分析时间：</font>

并行使用子代理分别分析认证模块、数据库模块和 API 模块，汇总后给出整体架构建议

### <font style="color:rgb(51, 51, 51);">3、串联子代理流水线</font>

<font style="color:rgb(51, 51, 51);">将复杂工作流拆分为多个专职代理，按顺序传递结果：</font>

先用 code-reviewer 找出问题，再用 optimizer 子代理修复这些问题

<font style="color:rgb(51, 51, 51);">串联工作流的设计原则：每个代理只做一件事，并通过清晰的"输入 → 处理 → 输出 → 交接信号"定义接口。以下是一个生产实践中的三段式流水线示例：</font>

* **<font style="color:rgb(51, 51, 51);">pm-spec</font>**<font style="color:rgb(51, 51, 51);">：读取需求，生成工作规格，确认后标记</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">READY_FOR_ARCH</font></code>
* **<font style="color:rgb(51, 51, 51);">architect-review</font>**<font style="color:rgb(51, 51, 51);">：验证设计约束，产出架构决策记录（ADR），标记</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">READY_FOR_BUILD</font></code>
* **<font style="color:rgb(51, 51, 51);">implementer-tester</font>**<font style="color:rgb(51, 51, 51);">：实现代码和测试，更新文档，标记</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">DONE</font></code>

<font style="color:rgb(51, 51, 51);">通过</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">SubagentStop</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">钩子监听状态文件，自动触发下一个代理，无需手动干预。</font>

### <font style="color:rgb(51, 51, 51);">4、并行代码审查</font>

```plain
同时启动 style-checker、security-scanner、test-coverage 三个子代理并行审查，
将审查时间从数分钟压缩到数十秒
```

***

## <font style="color:rgb(51, 51, 51);">什么时候该用子代理</font>

**<font style="color:rgb(51, 51, 51);">适合用子代理的场景：</font>**

* <font style="color:rgb(51, 51, 51);">任务自包含，可以给出明确的输入和期望输出</font>
* <font style="color:rgb(51, 51, 51);">输出量很大，会显著占用主对话上下文</font>
* <font style="color:rgb(51, 51, 51);">需要强约束（只读、隔离 worktree 等）</font>
* <font style="color:rgb(51, 51, 51);">同类任务会重复出现，值得固化为代理</font>
* <font style="color:rgb(51, 51, 51);">涉及多个独立子域，可以并行处理</font>

**<font style="color:rgb(51, 51, 51);">适合用主对话的场景：</font>**

* <font style="color:rgb(51, 51, 51);">需要频繁来回调整，交互性强</font>
* <font style="color:rgb(51, 51, 51);">多阶段任务有强依赖关系，上下文需要连续</font>
* <font style="color:rgb(51, 51, 51);">快速、小改动，启动代理的开销不值得</font>
* <font style="color:rgb(51, 51, 51);">实际经验：超过 3～4 个子代理后，管理成本可能反而降低整体效率</font>

*<font style="color:rgb(44, 58, 94);">子代理不能再创建子代理（防止无限嵌套）。如需嵌套逻辑，请使用</font>**<font style="color:rgb(44, 58, 94);"> </font>**__<font style="color:rgb(44, 58, 94);">Skills</font>__\_\_<font style="color:rgb(44, 58, 94);">。</font>*

***

## <font style="color:rgb(51, 51, 51);">最佳实践</font>

**<font style="color:rgb(51, 51, 51);">description 怎么写</font>**

* <font style="color:rgb(51, 51, 51);">用动作式描述：</font><code><font style="color:rgb(51, 51, 51);">当用户要求审查 / 分析 / 检查代码质量时调用</font></code>
* <font style="color:rgb(51, 51, 51);">说明前置条件：</font><code><font style="color:rgb(51, 51, 51);">在规格文档确认后使用，产出架构决策记录</font></code>
* <font style="color:rgb(51, 51, 51);">写清楚代理的边界和不擅长的场景，防止被错误调用</font>

**<font style="color:rgb(51, 51, 51);">工具权限设计（最小权限原则）</font>**

* <font style="color:rgb(51, 51, 51);">只读代理（审查、审计）：</font><code><font style="color:rgb(51, 51, 51);">Read, Grep, Glob</font></code>
* <font style="color:rgb(51, 51, 51);">研究代理（信息收集）：</font><code><font style="color:rgb(51, 51, 51);">Read, Grep, Glob, WebFetch, WebSearch</font></code>
* <font style="color:rgb(51, 51, 51);">实现代理（写代码）：</font><code><font style="color:rgb(51, 51, 51);">Read, Write, Edit, Bash, Glob, Grep</font></code>

**<font style="color:rgb(51, 51, 51);">单一职责</font>**

* <font style="color:rgb(51, 51, 51);">每个代理只做一件事，给出清晰的输入 / 输出 / 交接规则</font>
* <font style="color:rgb(51, 51, 51);">不要试图用一个代理包办所有事情</font>

**<font style="color:rgb(51, 51, 51);">系统提示建议</font>**

* <font style="color:rgb(51, 51, 51);">在系统提示中明确代理的性格：</font><code><font style="color:rgb(51, 51, 51);">请保持批判性，不要只说好话</font></code>
* <font style="color:rgb(51, 51, 51);">指出代理的弱点和局限，避免过度自信</font>
* <font style="color:rgb(51, 51, 51);">如果启用了记忆，在系统提示里写入"主动维护记忆"的指令，让代理自动执行</font>

**<font style="color:rgb(51, 51, 51);">并行 vs 串行的选择</font>**

* <font style="color:rgb(51, 51, 51);">各子域之间相互独立 → 优先并行，节省时间</font>
* <font style="color:rgb(51, 51, 51);">下一步依赖上一步的结果 → 必须串行，保证质量</font>
* <font style="color:rgb(51, 51, 51);">避免为了并行而并行：10 个并行代理处理简单任务反而浪费 Token 和协调成本</font>

# Claude Code 插件集成与记忆系统进阶应用

## <font style="color:rgb(51, 51, 51);">Claude Code 插件</font>

<font style="color:rgb(51, 51, 51);">插件（Plugin）是 Claude Code 中</font>**<font style="color:rgb(51, 51, 51);">最高级别的扩展机制</font>**<font style="color:rgb(51, 51, 51);">，用于将命令、代理、Skills、钩子、MCP、LSP 等能力</font>**<font style="color:rgb(51, 51, 51);">打包、版本化、共享和分发</font>**<font style="color:rgb(51, 51, 51);">。</font>

**<font style="color:rgb(51, 51, 51);">插件 = 一组可复用的 Claude Code 扩展能力集合</font>**

<font style="color:rgb(51, 51, 51);">一个插件可以包含：</font>

* <font style="color:rgb(51, 51, 51);">斜杠命令（Slash Commands）</font>
* <font style="color:rgb(51, 51, 51);">子代理（Agents）</font>
* <font style="color:rgb(51, 51, 51);">Skills（能力说明）</font>
* <font style="color:rgb(51, 51, 51);">Hooks（事件钩子）</font>
* <font style="color:rgb(51, 51, 51);">MCP 服务器（外部工具/服务）</font>
* <font style="color:rgb(51, 51, 51);">LSP 服务器（代码智能）</font>

*<font style="color:rgb(44, 58, 94);">插件的核心目标只有一个：</font>*

***<font style="color:rgb(44, 58, 94);">让 Claude Code 的能力像工具箱"一样被复用，而不是每个项目重复配置</font>***

***

## <font style="color:rgb(51, 51, 51);">插件 vs 独立配置（如何选择）</font>

<font style="color:rgb(51, 51, 51);">Claude Code 支持两种扩展方式：</font>

| <font style="color:rgb(255, 255, 255);">方式</font> | <font style="color:rgb(255, 255, 255);">命令形式</font> | <font style="color:rgb(255, 255, 255);">适合场景</font> |
| --- | --- | --- |
| **<font style="color:rgb(51, 51, 51);">独立配置</font>**<font style="color:rgb(51, 51, 51);">（</font><code><font style="color:rgb(51, 51, 51);">.claude/</font></code><br/><font style="color:rgb(51, 51, 51);">）</font> | <code><font style="color:rgb(51, 51, 51);">/hello</font></code> | <font style="color:rgb(51, 51, 51);">个人使用、单项目、快速实验</font> |
| **<font style="color:rgb(51, 51, 51);">插件</font>**<font style="color:rgb(51, 51, 51);">（</font><code><font style="color:rgb(51, 51, 51);">.claude-plugin/</font></code><br/><font style="color:rgb(51, 51, 51);">）</font> | <code><font style="color:rgb(51, 51, 51);">/plugin-name:hello</font></code> | <font style="color:rgb(51, 51, 51);">团队共享、跨项目、版本化</font> |

### <font style="color:rgb(51, 51, 51);">什么时候用独立配置？</font>

* <font style="color:rgb(51, 51, 51);">只在当前项目使用</font>
* <font style="color:rgb(51, 51, 51);">个人工作流</font>
* <font style="color:rgb(51, 51, 51);">尚未稳定的实验性配置</font>
* <font style="color:rgb(51, 51, 51);">想要简短命令名（如</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">/review</font></code><font style="color:rgb(51, 51, 51);">）</font>

### <font style="color:rgb(51, 51, 51);">什么时候用插件？</font>

* <font style="color:rgb(51, 51, 51);">要在</font>**<font style="color:rgb(51, 51, 51);">多个项目复用</font>**
* <font style="color:rgb(51, 51, 51);">要</font>**<font style="color:rgb(51, 51, 51);">分享给团队或社区</font>**
* <font style="color:rgb(51, 51, 51);">需要</font>**<font style="color:rgb(51, 51, 51);">版本控制、升级、回滚</font>**
* <font style="color:rgb(51, 51, 51);">计划通过市场分发</font>
* <font style="color:rgb(51, 51, 51);">可以接受命名空间命令（避免冲突）</font>

***<font style="color:rgb(44, 58, 94);">最佳实践：</font>***

*<font style="color:rgb(44, 58, 94);">先在</font>\_\_<font style="color:rgb(44, 58, 94);"> </font>*<code>_<font style="color:rgb(44, 58, 94);">.claude/</font>_</code>*<font style="color:rgb(44, 58, 94);"> </font>\_\_<font style="color:rgb(44, 58, 94);">中迭代 → 稳定后打包为插件</font>*

***

## <font style="color:rgb(51, 51, 51);">插件的最小结构（必须记住）</font>

```plain
my-plugin/
├── .claude-plugin/
│   └── plugin.json     # 插件清单（必需）
├── commands/           # 斜杠命令
├── agents/             # 子代理
├── skills/             # Skills
├── hooks/              # 钩子
├── .mcp.json           # MCP 配置
└── .lsp.json           # LSP 配置
```

**<font style="color:rgb(51, 51, 51);">重要规则</font>**

* <code><font style="color:rgb(51, 51, 51);">.claude-plugin/</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">目录中</font>**<font style="color:rgb(51, 51, 51);">只能放</font>\*\*\*\*<font style="color:rgb(51, 51, 51);"> </font>**<code>**<font style="color:rgb(51, 51, 51);">plugin.json</font>**</code>
* <font style="color:rgb(51, 51, 51);">其他目录必须在插件根目录</font>

***

## <font style="color:rgb(51, 51, 51);">插件清单（plugin.json）</font>

<font style="color:rgb(51, 51, 51);">插件的"身份证"，决定：</font>

* <font style="color:rgb(51, 51, 51);">插件名称</font>
* <font style="color:rgb(51, 51, 51);">命令命名空间</font>
* <font style="color:rgb(51, 51, 51);">版本</font>
* <font style="color:rgb(51, 51, 51);">作者信息</font>

<font style="color:rgb(51, 51, 51);">示例：</font>

```plain
{
  "name": "my-first-plugin",
  "description": "A greeting plugin to learn the basics",
  "version": "1.0.0",
  "author": { "name": "Your Name" }
}
```

<font style="color:rgb(51, 51, 51);">关键字段说明：</font>

| <font style="color:rgb(255, 255, 255);">字段</font> | <font style="color:rgb(255, 255, 255);">作用</font> |
| --- | --- |
| <font style="color:rgb(51, 51, 51);">name</font> | <font style="color:rgb(51, 51, 51);">唯一标识 + 命令命名空间</font> |
| <font style="color:rgb(51, 51, 51);">description</font> | <font style="color:rgb(51, 51, 51);">插件市场中展示</font> |
| <font style="color:rgb(51, 51, 51);">version</font> | <font style="color:rgb(51, 51, 51);">语义化版本控制</font> |
| <font style="color:rgb(51, 51, 51);">author</font> | <font style="color:rgb(51, 51, 51);">可选，归属说明</font> |

***

## <font style="color:rgb(51, 51, 51);">斜杠命令（最常用插件能力）</font>

### <font style="color:rgb(51, 51, 51);">1、命令定义方式</font>

* <font style="color:rgb(51, 51, 51);">位于</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">commands/</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">目录</font>
* <font style="color:rgb(51, 51, 51);">每个命令 = 一个 Markdown 文件</font>
* <font style="color:rgb(51, 51, 51);">文件名 = 命令名</font>

<font style="color:rgb(51, 51, 51);">示例：</font>

commands/hello.md

<font style="color:rgb(51, 51, 51);">对应命令：</font>

/my-first-plugin:hello

### <font style="color:rgb(51, 51, 51);">2、命令内容示例</font>

```plain
---
description: Greet the user with a friendly message
---

Greet the user warmly and ask how you can help them today.
```

### <font style="color:rgb(51, 51, 51);">3、命令参数</font>

<font style="color:rgb(51, 51, 51);">使用</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">$ARGUMENTS</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">捕获用户输入：</font>

Greet the user named "$ARGUMENTS" warmly.

<font style="color:rgb(51, 51, 51);">调用：</font>

/my-first-plugin:hello Alex

***

## <font style="color:rgb(51, 51, 51);">本地测试插件（开发必会）</font>

<font style="color:rgb(51, 51, 51);">使用</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">--plugin-dir</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">直接加载插件目录：</font>

claude --plugin-dir ./my-plugin

<font style="color:rgb(51, 51, 51);">特点：</font>

* <font style="color:rgb(51, 51, 51);">不需要安装</font>
* <font style="color:rgb(51, 51, 51);">修改后需重启 Claude Code</font>
* <font style="color:rgb(51, 51, 51);">支持同时加载多个插件</font>

claude --plugin-dir ./plugin-a --plugin-dir ./plugin-b

***

## <font style="color:rgb(51, 51, 51);">插件还能做什么</font>

| <font style="color:rgb(255, 255, 255);">能力</font> | <font style="color:rgb(255, 255, 255);">用途</font> |
| --- | --- |
| <font style="color:rgb(51, 51, 51);">Commands</font> | <font style="color:rgb(51, 51, 51);">自定义斜杠命令</font> |
| <font style="color:rgb(51, 51, 51);">Agents</font> | <font style="color:rgb(51, 51, 51);">专用子代理</font> |
| <font style="color:rgb(51, 51, 51);">Skills</font> | <font style="color:rgb(51, 51, 51);">教会 Claude 何时用某种能力</font> |
| <font style="color:rgb(51, 51, 51);">Hooks</font> | <font style="color:rgb(51, 51, 51);">自动化（写完文件后执行命令等）</font> |
| <font style="color:rgb(51, 51, 51);">MCP</font> | <font style="color:rgb(51, 51, 51);">连接外部服务（GitHub、DB、API）</font> |
| <font style="color:rgb(51, 51, 51);">LSP</font> | <font style="color:rgb(51, 51, 51);">代码智能（跳转、类型检查）</font> |

***

## <font style="color:rgb(51, 51, 51);">插件市场（Plugin Marketplace）</font>

<font style="color:rgb(51, 51, 51);">插件通过</font>**<font style="color:rgb(51, 51, 51);">市场</font>**<font style="color:rgb(51, 51, 51);">分发，本质是一个插件目录仓库。</font>

### <font style="color:rgb(51, 51, 51);">官方市场</font>

* <font style="color:rgb(51, 51, 51);">默认已添加</font>
* <font style="color:rgb(51, 51, 51);">运行</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">/plugin</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">→</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:rgb(51, 51, 51);">Discover</font>**

![1783649847436-a1676d4c-880d-4cf0-973e-3b0af04e5a3d.png](./img/wf9R51v5S5sXlvV1/1783649847436-a1676d4c-880d-4cf0-973e-3b0af04e5a3d-283028.png)

<font style="color:rgb(51, 51, 51);">安装插件：</font>

/plugin install plugin-name@claude-plugins-official

***

## <font style="color:rgb(51, 51, 51);">插件安装范围</font>

| <font style="color:rgb(255, 255, 255);">范围</font> | <font style="color:rgb(255, 255, 255);">说明</font> |
| --- | --- |
| <font style="color:rgb(51, 51, 51);">用户范围</font> | <font style="color:rgb(51, 51, 51);">仅你自己，所有项目</font> |
| <font style="color:rgb(51, 51, 51);">项目范围</font> | <font style="color:rgb(51, 51, 51);">当前仓库，团队共享</font> |
| <font style="color:rgb(51, 51, 51);">本地范围</font> | <font style="color:rgb(51, 51, 51);">当前仓库，仅你</font> |

<font style="color:rgb(51, 51, 51);">推荐：</font>

* <font style="color:rgb(51, 51, 51);">团队工具 →</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:rgb(51, 51, 51);">项目范围</font>**
* <font style="color:rgb(51, 51, 51);">个人效率工具 →</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:rgb(51, 51, 51);">用户范围</font>**

***

## <font style="color:rgb(51, 51, 51);">典型插件分类</font>

### <font style="color:rgb(51, 51, 51);">1、代码智能（LSP）</font>

* <font style="color:rgb(51, 51, 51);">TypeScript、Python、Go、Rust 等</font>
* <font style="color:rgb(51, 51, 51);">提供跳转定义、引用、类型错误</font>

<font style="color:rgb(51, 51, 51);">需要本地安装对应语言服务器</font>

### <font style="color:rgb(51, 51, 51);">2、外部集成（MCP）</font>

* <font style="color:rgb(51, 51, 51);">GitHub / GitLab</font>
* <font style="color:rgb(51, 51, 51);">Jira / Notion</font>
* <font style="color:rgb(51, 51, 51);">Slack / Figma</font>
* <font style="color:rgb(51, 51, 51);">Vercel / Supabase</font>

*<font style="color:rgb(44, 58, 94);">本质：</font>\_\_**<font style="color:rgb(44, 58, 94);">插件 = MCP 服务器 + 配置</font>***

### <font style="color:rgb(51, 51, 51);">3、开发工作流</font>

* <font style="color:rgb(51, 51, 51);">Git 提交、PR</font>
* <font style="color:rgb(51, 51, 51);">代码审查代理</font>
* <font style="color:rgb(51, 51, 51);">插件开发工具</font>

***

## <font style="color:rgb(51, 51, 51);">插件管理常用命令</font>

```plain
/plugin                # 打开插件管理器
/plugin install         # 安装插件
/plugin uninstall       # 卸载
/plugin enable/disable  # 启用 / 禁用
/plugin marketplace add # 添加市场
/plugin marketplace rm  # 移除市场
```

***

## <font style="color:rgb(51, 51, 51);">从</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">.claude/</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">迁移到插件（核心思路）</font>

| <font style="color:rgb(255, 255, 255);">原来</font> | <font style="color:rgb(255, 255, 255);">迁移后</font> |
| --- | --- |
| <code><font style="color:rgb(51, 51, 51);">.claude/commands</font></code> | <code><font style="color:rgb(51, 51, 51);">plugin/commands</font></code> |
| <code><font style="color:rgb(51, 51, 51);">.claude/agents</font></code> | <code><font style="color:rgb(51, 51, 51);">plugin/agents</font></code> |
| <code><font style="color:rgb(51, 51, 51);">settings.json hooks</font></code> | <code><font style="color:rgb(51, 51, 51);">plugin/hooks/hooks.json</font></code> |

<font style="color:rgb(51, 51, 51);">迁移后：</font>

* <font style="color:rgb(51, 51, 51);">插件版本优先生效</font>
* <font style="color:rgb(51, 51, 51);">可删除旧</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">.claude/</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">配置避免重复</font>

***

## <font style="color:rgb(51, 51, 51);">什么时候你一定要用插件？</font>

* <font style="color:rgb(51, 51, 51);">你已经有</font>**<font style="color:rgb(51, 51, 51);">稳定的 Claude 工作流</font>**
* <font style="color:rgb(51, 51, 51);">你在</font>**<font style="color:rgb(51, 51, 51);">反复复制</font>\*\*\*\*<font style="color:rgb(51, 51, 51);"> </font>**<code>**<font style="color:rgb(51, 51, 51);">.claude/</font>**</code>
* <font style="color:rgb(51, 51, 51);">团队成员开始问你："这个怎么配置？"</font>
* <font style="color:rgb(51, 51, 51);">你希望 Claude 像 IDE 插件一样可控</font>

***<font style="color:rgb(44, 58, 94);">插件，是 Claude Code 从"个人 AI 助手"走向"工程化工具"的分水岭</font>***

# Agent Skills 从需求到落地开发实战：skill-creator 定制

## <font style="color:rgb(51, 51, 51);">Agent Skills（智能体技能）</font>

<font style="color:rgb(51, 51, 51);">Agent 是智能体，Skills 是技能的意思，Agent Skills（智能体技能）是将专业知识、工作流规范固化为可复用资产的核心工具。</font>

<font style="color:rgb(51, 51, 51);">Agent Skills 本质上是一个模块化的 Markdown 文件，能教会 AI 工具 （如 Claude、GitHub Copilot、Cursor 等） 执行特定任务，且支持自动触发、团队共享与工程化管理，彻底告别重复的提示词输入。</font>

<font style="color:rgb(51, 51, 51);">Agent Skills 的本质不是工具，而是：</font>

***<font style="color:rgb(44, 58, 94);">行为规范 + 专业知识 + 使用时机的组合</font>***

**<font style="color:rgb(51, 51, 51);">核心形式：</font>**

* <font style="color:rgb(51, 51, 51);">一个 Skill 就是一个文件夹，里面必须有一个 SKILL.md 文件（包含说明和元数据），可选其他资源文件（如脚本、示例、参考文档）。</font>
* <font style="color:rgb(51, 51, 51);">Skill 是一个 Markdown 文件（SKILL.md），用于教 Claude 在特定场景下按你的方式做事。</font>
* <font style="color:rgb(51, 51, 51);">本质是其实就是相当于给 AI 代理发放一本专业手册，AI 不会每次都从零学习，而是根据任务自动调用手册中的知识。</font>
* <font style="color:rgb(51, 51, 51);">简单来说，过去我们用提示词（prompt）教 AI 做事，现在用 Agent Skills 可以把提示词 + 资源打包成可复用、可共享的技能包，更高效、更可靠。</font>

![1783649947232-0f979130-73bd-49b5-9ed8-5602bcb9161e.png](./img/wf9R51v5S5sXlvV1/1783649947232-0f979130-73bd-49b5-9ed8-5602bcb9161e-688851.png)

### <font style="color:rgb(51, 51, 51);">Agent Skills 的工作原理</font>

<font style="color:rgb(51, 51, 51);">Agent Skills 的关键是渐进式披露，分三层加载：</font>

* **<font style="color:rgb(51, 51, 51);">层级 1：技能发现</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">-- AI 先读取所有技能的元数据（name 和 description），判断任务是否相关，这些元数据始终在系统提示中。</font>
* **<font style="color:rgb(51, 51, 51);">层级 2：加载核心指令</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">-- 如果相关，AI 自动读取 SKILL.md 的正文内容，获取详细指导。</font>
* **<font style="color:rgb(51, 51, 51);">层级 3：加载资源文件</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">-- 只在需要时读取额外文件（如脚本、示例），或通过工具执行脚本。</font>

### <font style="color:rgb(51, 51, 51);">支持的工具和环境</font>

<font style="color:rgb(51, 51, 51);">目前主要支持：</font>

* <font style="color:rgb(51, 51, 51);">Claude（Anthropic）：Claude.ai、Claude Code、Agent SDK。</font>
* <font style="color:rgb(51, 51, 51);">VS Code + GitHub Copilot：项目级（.github/skills/）或个人级技能。</font>
* <font style="color:rgb(51, 51, 51);">Cursor：项目级（.cursor/skills/）或全局技能，支持从 GitHub 安装。</font>
* <font style="color:rgb(51, 51, 51);">其他：正在扩展中，标准开源在</font><font style="color:rgb(51, 51, 51);"> </font>[<font style="color:rgb(0, 102, 0);">https://github.com/agentskills/agentskills</font>](https://github.com/agentskills/agentskills)<font style="color:rgb(51, 51, 51);">。</font>

### <font style="color:rgb(51, 51, 51);">为什么需要 Skills？它解决了什么问题？</font>

<font style="color:rgb(51, 51, 51);">普通 AI 代理（如 Claude 或 Copilot）很聪明，但缺少特定上下文时容易出错。例如：</font>

* <font style="color:rgb(51, 51, 51);">团队有自己的代码规范，但 AI 每次都要手动提醒。</font>
* <font style="color:rgb(51, 51, 51);">需要处理 PDF 表单、调试 GitHub Actions 等复杂流程，AI 可能不知道最佳实践。</font>

<font style="color:rgb(51, 51, 51);">Agent Skills 解决这些问题：</font>

* **<font style="color:rgb(51, 51, 51);">自动触发</font>**<font style="color:rgb(51, 51, 51);">：AI 根据任务自动加载相关技能，无需手动输入长提示。</font>
* **<font style="color:rgb(51, 51, 51);">可复用 & 可共享</font>**<font style="color:rgb(51, 51, 51);">：一次创建，全团队或社区使用，支持 Git 版本控制。</font>
* **<font style="color:rgb(51, 51, 51);">高效利用上下文</font>**<font style="color:rgb(51, 51, 51);">：采用渐进式披露（progressive disclosure），只加载需要的部分，避免上下文窗口溢出。</font>
* **<font style="color:rgb(51, 51, 51);">跨平台</font>**<font style="color:rgb(51, 51, 51);">：同一个 Skill 可以在 Claude、VS Code Copilot、Cursor 等工具中使用。</font>

### <font style="color:rgb(51, 51, 51);">核心概念快速理解</font>

| <font style="color:rgb(255, 255, 255);">概念</font> | <font style="color:rgb(255, 255, 255);">比喻</font> | <font style="color:rgb(255, 255, 255);">作用</font> |
| --- | --- | --- |
| **<font style="color:rgb(51, 51, 51);">Skill（技能）</font>** | <font style="color:rgb(51, 51, 51);">一个独立的瑞士军刀工具或烹饪食谱</font> | <font style="color:rgb(51, 51, 51);">完成一项特定任务（如写邮件、分析数据）的完整套件。</font> |
| **<font style="color:rgb(51, 51, 51);">Instruction（指令）</font>** | <font style="color:rgb(51, 51, 51);">工具的使用说明书或食谱的步骤</font> | <font style="color:rgb(51, 51, 51);">告诉Claude具体要做什么、如何思考、输出什么格式。</font> |
| **<font style="color:rgb(51, 51, 51);">Knowledge（知识）</font>** | <font style="color:rgb(51, 51, 51);">工具的零件清单或食谱的食材背景资料</font> | <font style="color:rgb(51, 51, 51);">上传文件（如产品手册、API 文档）作为 Skill 的专属知识库。</font> |
| **<font style="color:rgb(51, 51, 51);">Tool（工具）</font>** | <font style="color:rgb(51, 51, 51);">工具上的特殊配件（如开瓶器）</font> | <font style="color:rgb(51, 51, 51);">定义 Skill 可以调用的外部 API 或函数，用于获取数据或执行操作。</font> |

### <font style="color:rgb(51, 51, 51);">Skill 执行流程</font>

* <font style="color:rgb(51, 51, 51);">从用户指令开始，先进行 Skill 意图识别，决定是否进入受控执行路径。</font>
* <font style="color:rgb(51, 51, 51);">命中 Skill 后，系统加载 SKILL.md，建立工具权限与行为边界，再结合上下文进行推理。</font>
* <font style="color:rgb(51, 51, 51);">只有在确实需要时才调用被允许的外部工具，否则在规则内完成逻辑。</font>
* <font style="color:rgb(51, 51, 51);">最终结果经过约束整合后输出，用户的下一次输入触发新一轮完整流程。</font>

![1783649947394-de7b903f-40ca-4cb9-a84e-aaba9ef6b536.png](./img/wf9R51v5S5sXlvV1/1783649947394-de7b903f-40ca-4cb9-a84e-aaba9ef6b536-322988.png)

***

## <font style="color:rgb(51, 51, 51);">Skill 的最小结构</font>

```plain
my-skill/
└── SKILL.md   （唯一必需）
```

<font style="color:rgb(51, 51, 51);">SKILL.md 基本模板:</font>

```plain
---
name: your-skill-name
description: What it does and when Claude should use it
---

# Skill Title

## Instructions
Clear, concrete, actionable rules.

## Examples
- Example usage 1
- Example usage 2

## Guidelines
- Guideline 1
- Guideline 2
```

<font style="color:rgb(51, 51, 51);">元数据字段:</font>

| <font style="color:rgb(255, 255, 255);">字段</font> | <font style="color:rgb(255, 255, 255);">必填</font> | <font style="color:rgb(255, 255, 255);">说明</font> |
| --- | --- | --- |
| <font style="color:rgb(51, 51, 51);">name</font> | <font style="color:rgb(51, 51, 51);">否</font> | <font style="color:rgb(51, 51, 51);">Skill 显示名称，默认使用目录名，仅支持小写字母、数字和短横线（最长 64 字符）</font> |
| <font style="color:rgb(51, 51, 51);">description</font> | <font style="color:rgb(51, 51, 51);">推荐</font> | <font style="color:rgb(51, 51, 51);">技能用途及使用场景，Claude 根据它判断是否自动应用</font> |
| <font style="color:rgb(51, 51, 51);">argument-hint</font> | <font style="color:rgb(51, 51, 51);">否</font> | <font style="color:rgb(51, 51, 51);">自动补全时显示的参数提示，如</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">[issue-number]</font></code><br/><font style="color:rgb(51, 51, 51);">、</font><code><font style="color:rgb(51, 51, 51);">[filename] [format]</font></code> |
| <font style="color:rgb(51, 51, 51);">disable-model-invocation</font> | <font style="color:rgb(51, 51, 51);">否</font> | <font style="color:rgb(51, 51, 51);">设为</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">true</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">禁止 Claude 自动触发，仅能手动</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">/name</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">调用（默认 false）</font> |
| <font style="color:rgb(51, 51, 51);">user-invocable</font> | <font style="color:rgb(51, 51, 51);">否</font> | <font style="color:rgb(51, 51, 51);">设为</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">false</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">从</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">/</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">菜单隐藏，作为后台增强能力使用（默认 true）</font> |
| <font style="color:rgb(51, 51, 51);">allowed-tools</font> | <font style="color:rgb(51, 51, 51);">否</font> | <font style="color:rgb(51, 51, 51);">Skill 激活时 Claude 可无授权使用的工具</font> |
| <font style="color:rgb(51, 51, 51);">model</font> | <font style="color:rgb(51, 51, 51);">否</font> | <font style="color:rgb(51, 51, 51);">Skill 激活时使用的模型</font> |
| <font style="color:rgb(51, 51, 51);">context</font> | <font style="color:rgb(51, 51, 51);">否</font> | <font style="color:rgb(51, 51, 51);">设为</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">fork</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">时在子代理上下文中运行</font> |
| <font style="color:rgb(51, 51, 51);">agent</font> | <font style="color:rgb(51, 51, 51);">否</font> | <font style="color:rgb(51, 51, 51);">子代理类型（配合 context: fork 使用）</font> |
| <font style="color:rgb(51, 51, 51);">hooks</font> | <font style="color:rgb(51, 51, 51);">否</font> | <font style="color:rgb(51, 51, 51);">技能生命周期钩子配置</font> |

<font style="color:rgb(51, 51, 51);">Skills 支持在内容中插入动态变量：</font>

| <font style="color:rgb(255, 255, 255);">变量</font> | <font style="color:rgb(255, 255, 255);">说明</font> |
| --- | --- |
| <code><font style="color:rgb(51, 51, 51);">$ARGUMENTS</font></code> | <font style="color:rgb(51, 51, 51);">调用 Skill 时传入的所有参数</font> |
| <code><font style="color:rgb(51, 51, 51);">$ARGUMENTS[N]</font></code> | <font style="color:rgb(51, 51, 51);">按索引访问参数，如</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">$ARGUMENTS[0]</font></code> |
| <code><font style="color:rgb(51, 51, 51);">$N</font></code> | <font style="color:rgb(51, 51, 51);">简写方式，如</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">$0</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">表示第一个参数</font> |
| <code><font style="color:rgb(51, 51, 51);">${CLAUDE_SESSION_ID}</font></code> | <font style="color:rgb(51, 51, 51);">当前会话 ID，用于日志、临时文件、关联输出</font> |

<font style="color:rgb(51, 51, 51);">例如：</font>

```plain
---
name: session-logger
description: 记录当前会话活动
---

请将以下内容写入日志文件：

logs/${CLAUDE_SESSION_ID}.log

$ARGUMENTS
```

<font style="color:rgb(51, 51, 51);">调用：</font>

/session-logger 用户登录成功

<font style="color:rgb(51, 51, 51);">实际会生成会话专属日志记录。</font>

### <font style="color:rgb(51, 51, 51);">SKILL.md 文件的核心构成</font>

<font style="color:rgb(51, 51, 51);">以 Claude 的 PDF 文档编辑技能为例，Claude 原生可解析 PDF，但无法直接操作（如填写表单），该技能补足了这一短板。</font>

* **<font style="color:rgb(51, 51, 51);">核心形态：</font>**<font style="color:rgb(51, 51, 51);">一个包含 SKILL.md 的目录</font>
* **<font style="color:rgb(51, 51, 51);">必填元数据：</font>**<font style="color:rgb(51, 51, 51);">SKILL.md 开头的 YAML 块，需包含 name（名称）和 description（描述），启动时预加载至系统提示词</font>

![1783649947027-e6940282-cf6d-4320-a4c2-e3aae12070c9.webp](./img/wf9R51v5S5sXlvV1/1783649947027-e6940282-cf6d-4320-a4c2-e3aae12070c9-729320.webp)

### <font style="color:rgb(51, 51, 51);">多文件 Skill（渐进式披露）</font>

**<font style="color:rgb(51, 51, 51);">渐进式披露机制</font>**

* <font style="color:rgb(51, 51, 51);">第一层：元数据 → 让 Claude 判断技能适用场景，不加载全部内容</font>
* <font style="color:rgb(51, 51, 51);">第二层：SKILL.md正文 → 判定相关后，载入完整上下文</font>
* <font style="color:rgb(51, 51, 51);">第三层 +：附属文件（如forms.md）→ 按需引用，精简核心文件体积</font>

![1783649947008-3e9138a6-4c2a-4d5e-8ecd-4590717f7b80.webp](./img/wf9R51v5S5sXlvV1/1783649947008-3e9138a6-4c2a-4d5e-8ecd-4590717f7b80-395657.webp)

<font style="color:rgb(51, 51, 51);">下图显示了当用户消息触发技能时，上下文窗口如何变化:</font>

![1783649947085-6a7ac548-a1c6-49e2-9c94-6e8a8597869b.webp](./img/wf9R51v5S5sXlvV1/1783649947085-6a7ac548-a1c6-49e2-9c94-6e8a8597869b-760103.webp)

* <font style="color:rgb(51, 51, 51);">初始状态：上下文窗口含系统提示词、技能元数据、用户指令</font>
* <font style="color:rgb(51, 51, 51);">调用 Bash 工具读取目标 SKILL.md，触发对应技能</font>
* <font style="color:rgb(51, 51, 51);">按需加载附属文件（如forms.md）</font>
* <font style="color:rgb(51, 51, 51);">加载完成后执行用户任务</font>

### <font style="color:rgb(51, 51, 51);">推荐目录结构</font>

<font style="color:rgb(51, 51, 51);">为避免上下文膨胀：</font>

* <font style="color:rgb(51, 51, 51);">核心规则 →</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">SKILL.md</font></code>
* <font style="color:rgb(51, 51, 51);">详细资料 → 单独文件</font>
* <font style="color:rgb(51, 51, 51);">实用逻辑 → 脚本执行（不加载）</font>

<font style="color:rgb(51, 51, 51);">推荐结构:</font>

```plain
my-skill/
├── SKILL.md
├── reference.md
├── examples.md    # 存放示例文件
└── scripts/
    └── helper.py
```

***

## <font style="color:rgb(51, 51, 51);">第一个 Skill</font>

<font style="color:rgb(51, 51, 51);">让我们暂时忘掉复杂的创建过程，先从</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:rgb(51, 51, 51);">使用一个现成的 Skill</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">开始，感受它带来的便利。</font>

### <font style="color:rgb(51, 51, 51);">创建 Skill 目录</font>

<font style="color:rgb(51, 51, 51);">Skills 存放在</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:rgb(51, 51, 51);">~/.claude/skills/</font>**<font style="color:rgb(51, 51, 51);">（个人全局）或项目目录下的</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:rgb(51, 51, 51);">.claude/skills/</font>**<font style="color:rgb(51, 51, 51);">（项目专用）。</font>

<font style="color:rgb(51, 51, 51);">本章节再项目目录下测试，先创建个目录 claude-test:</font>

mkdir claude-test

<font style="color:rgb(51, 51, 51);">进入该目录，创建 skills 的目录与文件：</font>

mkdir -p .claude/skills/python-naming-standard

### <font style="color:rgb(51, 51, 51);">编写配置文件 SKILL.md</font>

<font style="color:rgb(51, 51, 51);">在目录下创建 SKILL.md，这是 Skill 的大脑 ，告诉 Claude 什么时候用它。</font>

```plain
---
name: Python 内部命名规范技能
description: 当用户要求重构、审查或编写 Python 代码时，请参考此规范。
---

## 指令
1. 所有的内部辅助函数必须以 `_internal_` 前缀命名。
2. 如果发现不符合此规则的代码，请自动提出修改建议。
3. 在执行 `claude commit` 前，必须检查此规范。

## 参考示例
- 正确：`def _internal_calculate_risk():`
- 错误：`def _calculate_risk():`
```

<font style="color:rgb(51, 51, 51);">字段要求：</font>

* **<font style="color:rgb(51, 51, 51);">name</font>**<font style="color:rgb(51, 51, 51);">：必须仅使用小写字母、数字和连字符（最多 64 个字符）</font>
* **<font style="color:rgb(51, 51, 51);">description</font>**<font style="color:rgb(51, 51, 51);">：Skill 的简要描述及其使用时机（最多 1024 个字符）</font>

<font style="color:rgb(51, 51, 51);">创建完后文件结构如下：</font>

![1783649947724-47c5e04a-813e-4f9e-8a88-d79702749930.png](./img/wf9R51v5S5sXlvV1/1783649947724-47c5e04a-813e-4f9e-8a88-d79702749930-300613.png)

<font style="color:rgb(51, 51, 51);">你的项目现在看起来应该是这样的：</font>

```plain
my-project/
├─ src/
│  └─ test.py              # 项目源码
├─ .claude/
│  ├─ skills/
│  │  └─ hello-world/
│  │     ├─ skill.md       # Skill 定义（YAML + Instructions，机器可执行）
│  │     └─ README.md      # Skill 说明（人类阅读，可选）
│  └─ config.yml           # Claude 项目级配置（可选）
├─ .gitignore
└─ README.md               # 项目整体说明
```

<font style="color:rgb(51, 51, 51);">接下来我们再终端执行以下命令启动 Claude Code：</font>

claude

<font style="color:rgb(51, 51, 51);">输入任务：</font>

帮我写一个计算用户折扣的函数

<font style="color:rgb(51, 51, 51);">Claude 就会会扫描已安装的 Skills，发现你的请求涉及 "Python 代码编写"，匹配了 python-naming-standard。</font>

![1783649947911-68a3bd3c-a5da-4ff3-9af3-b47f609f6b56.png](./img/wf9R51v5S5sXlvV1/1783649947911-68a3bd3c-a5da-4ff3-9af3-b47f609f6b56-849161.png)

<font style="color:rgb(51, 51, 51);">它会根据 SKILL.md 中的要求，生成如下代码：</font>

```plain
def _internal_get_discount(user_score):
    # 计算逻辑...
    return discount
```

### <font style="color:rgb(51, 51, 51);">添加资源文件（可选）</font>

<font style="color:rgb(51, 51, 51);">另外我们可以在</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:rgb(51, 51, 51);">.claude/skills/</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">下添加以下目录：</font>

<font style="color:rgb(51, 51, 51);">在同一文件夹添加：</font>

* <code><font style="color:rgb(51, 51, 51);">examples/</font></code><font style="color:rgb(51, 51, 51);">：存放示例文件。</font>
* <code><font style="color:rgb(51, 51, 51);">references/</font></code><font style="color:rgb(51, 51, 51);">：存放参考文档。</font>
* <code><font style="color:rgb(51, 51, 51);">scripts/</font></code><font style="color:rgb(51, 51, 51);">：存放可执行脚本（例如 Python 处理 PDF）。</font>

<font style="color:rgb(51, 51, 51);">然后在 SKILL.md 中引用：</font>

```plain
查看示例 commit：./examples/good-commit.txt
运行脚本：使用工具执行 ./scripts/process.py
```

***

## <font style="color:rgb(51, 51, 51);">官方市场</font>

<font style="color:rgb(51, 51, 51);">除了自己编写，你还可以利用 2025 年末发布的 Agent Skills 开放标准：</font>

* <font style="color:rgb(51, 51, 51);">官方市场：访问</font><font style="color:rgb(51, 51, 51);"> </font>[<font style="color:rgb(0, 102, 0);">https://github.com/anthropics/skills</font>](https://github.com/anthropics/skills)<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">仓库下载预设的技能（如：React 优化器、SQL 调优工具）。</font>
* <font style="color:rgb(51, 51, 51);">Skill Creator：你可以对 Claude 说："帮我把我刚才教你的关于 Docker 的配置逻辑总结成一个 Skill"，它会自动在相应目录为你生成文件。</font>

<font style="color:rgb(51, 51, 51);">我们可以将本仓库注册为 Claude Code 的插件市场，只需在 Claude Code 中执行以下命令：</font>

/plugin marketplace add anthropics/skills

![1783649947872-42960c2d-c16c-41f8-b968-ff5e139a2804.png](./img/wf9R51v5S5sXlvV1/1783649947872-42960c2d-c16c-41f8-b968-ff5e139a2804-692071.png)

<font style="color:rgb(51, 51, 51);">然后就可以使用</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:rgb(51, 51, 51);">/plugin</font>\*\*\*\*<font style="color:rgb(51, 51, 51);"> </font>**<font style="color:rgb(51, 51, 51);">查看：</font>

![1783649948327-34b236c0-55bd-46bb-bbd2-53b2c497088c.png](./img/wf9R51v5S5sXlvV1/1783649948327-34b236c0-55bd-46bb-bbd2-53b2c497088c-003572.png)

**<font style="color:rgb(51, 51, 51);">安装指定技能集的步骤：</font>**

* <font style="color:rgb(51, 51, 51);">浏览并安装插件（Browse and install plugins）</font>
* <font style="color:rgb(51, 51, 51);">选择 anthropic-agent-skills 插件源</font>
* <font style="color:rgb(51, 51, 51);">选择 document-skills（文档技能） 或 example-skills（示例技能）</font>

![1783649948400-b4865912-c7cd-4895-9390-0915ef6afa30.png](./img/wf9R51v5S5sXlvV1/1783649948400-b4865912-c7cd-4895-9390-0915ef6afa30-906376.png)

* <font style="color:rgb(51, 51, 51);">点击立即安装（Install now）</font>

![1783649948483-528ff142-c251-4903-a891-b9a121c8b436.png](./img/wf9R51v5S5sXlvV1/1783649948483-528ff142-c251-4903-a891-b9a121c8b436-714870.png)

<font style="color:rgb(51, 51, 51);">我们也可直接通过命令安装上述两类插件：</font>

```plain
/plugin install document-skills@anthropic-agent-skills
/plugin install example-skills@anthropic-agent-skills
```

**<font style="color:rgb(51, 51, 51);">注意：</font>**<font style="color:rgb(51, 51, 51);">使用插件安装的 skills 目录在</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:rgb(51, 51, 51);">～/claude/plugins/marketplaces/</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">下。</font>

<font style="color:rgb(51, 51, 51);">插件安装完成后，需要重启一下 Claude Code。</font>

<font style="color:rgb(51, 51, 51);">使用的时候只需在指令中提及技能名称即可调用，例如安装 document-skills 插件后，可向 Claude Code 下达指令：</font>

使用 PDF 技能提取 path/to/some-file.pdf 文件中的表单字段

<font style="color:rgb(51, 51, 51);">或者创建一个 PPT：</font>

创建一个 Agent Skill 的演示文稿

<font style="color:rgb(51, 51, 51);">可以看到，调用了</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:rgb(51, 51, 51);">/document-skills:pptx</font>**<font style="color:rgb(51, 51, 51);">：</font>

![1783649948602-8f0ec55d-06aa-42f5-8c66-567f9f898d21.png](./img/wf9R51v5S5sXlvV1/1783649948602-8f0ec55d-06aa-42f5-8c66-567f9f898d21-684366.png)

<font style="color:rgb(51, 51, 51);">开始生成：</font>

![1783649948644-5ff50aaf-f3a7-4e7d-9ec2-a96d5a6ee874.png](./img/wf9R51v5S5sXlvV1/1783649948644-5ff50aaf-f3a7-4e7d-9ec2-a96d5a6ee874-231484.png)

<font style="color:rgb(51, 51, 51);">之后就会告诉你生成的文件位置：</font>

![1783649949282-b9478a1a-85c1-4403-b130-e1369ef4cec8.png](./img/wf9R51v5S5sXlvV1/1783649949282-b9478a1a-85c1-4403-b130-e1369ef4cec8-388041.png)

***

## <font style="color:rgb(51, 51, 51);">Agent Skills 相关资源整理</font>

| <font style="color:rgb(255, 255, 255);">资源说明</font> | <font style="color:rgb(255, 255, 255);">链接</font> |
| --- | --- |
| <font style="color:rgb(51, 51, 51);">Skill 聚合入口</font> | [<font style="color:rgb(0, 102, 0);">https://skills.sh/</font>](https://skills.sh/) |
| <font style="color:rgb(51, 51, 51);">Skills 市场（中文界面）</font> | [<font style="color:rgb(0, 102, 0);">https://skillsmp.com/zh</font>](https://skillsmp.com/zh) |
| <font style="color:rgb(51, 51, 51);">Agent Skills 官方标准站点</font> | [<font style="color:rgb(0, 102, 0);">https://agentskills.io</font>](https://agentskills.io/) |
| <font style="color:rgb(51, 51, 51);">Anthropic 官方工程文章（Agent Skills 实战理念）</font> | [<font style="color:rgb(0, 102, 0);">https://www.anthropic.com/engineering/equipping-agents-for-the-real-world-with-agent-skills</font>](https://www.anthropic.com/engineering/equipping-agents-for-the-real-world-with-agent-skills) |
| <font style="color:rgb(51, 51, 51);">VS Code Copilot Agent Skills 文档</font> | [<font style="color:rgb(0, 102, 0);">https://code.visualstudio.com/docs/copilot/customization/agent-skills</font>](https://code.visualstudio.com/docs/copilot/customization/agent-skills) |
| <font style="color:rgb(51, 51, 51);">Anthropic 官方 Skills GitHub 仓库</font> | [<font style="color:rgb(0, 102, 0);">https://github.com/anthropics/skills</font>](https://github.com/anthropics/skills) |
| <font style="color:rgb(51, 51, 51);">Claude 技能精选列表（Awesome 系列）</font> | [<font style="color:rgb(0, 102, 0);">https://github.com/ComposioHQ/awesome-claude-skills</font>](https://github.com/ComposioHQ/awesome-claude-skills) |
| <font style="color:rgb(51, 51, 51);">软件开发自动化工作流 Skills 集合</font> | [<font style="color:rgb(0, 102, 0);">https://github.com/obra/superpowers</font>](https://github.com/obra/superpowers) |
| <font style="color:rgb(51, 51, 51);">自动生成 Skill 的 Skill（官方示例）</font> | [<font style="color:rgb(0, 102, 0);">https://github.com/anthropics/skills/tree/main/skills/skill-creator</font>](https://github.com/anthropics/skills/tree/main/skills/skill-creator) |

## <font style="color:rgb(51, 51, 51);">Claude Code Skills 使用实例</font>

<font style="color:rgb(51, 51, 51);">在上一章节</font><font style="color:rgb(51, 51, 51);"> </font>[<font style="color:rgb(0, 102, 0);">Agent Skills（智能体技能）</font>](https://www.runoob.com/claude-code/claude-agent-skills.html)<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">中我们已经了解了 Skills 的基本概念，本章节我们将结合一个具体的 Skills 来开发一个项目。</font>

*<font style="color:rgb(44, 58, 94);">现在市面上已经有很多现成的 skills，我么可以直接拿来使用，我们可以在</font>\_\_<font style="color:rgb(44, 58, 94);"> </font>*[*<font style="color:rgb(0, 102, 0);">https://skills.sh/</font>*](https://skills.sh/)*<font style="color:rgb(44, 58, 94);"> </font>\_\_<font style="color:rgb(44, 58, 94);">查找更多的 skill。</font>*

*<font style="color:rgb(44, 58, 94);">安装方式：</font>*

<font style="color:rgb(44, 58, 94);">npx skills add \<owner/repo></font>

*<font style="color:rgb(44, 58, 94);">npx 安装 ui-ux-pro-max 可参考：</font>*[*<font style="color:rgb(0, 102, 0);">OpenCode skills 使用</font>*](https://www.runoob.com/ai-agent/opencode-skills-intro.html)*<font style="color:rgb(44, 58, 94);">。</font>*

**<font style="color:rgb(44, 58, 94);">注：</font>**<font style="color:rgb(44, 58, 94);">如果对 npx 不了解，可以参阅：</font>[<font style="color:rgb(0, 102, 0);">npx 入门教程</font>](https://www.runoob.com/nodejs/npx-intro.html)

<font style="color:rgb(51, 51, 51);">本章节我们将介绍一个支持多平台、多框架的专业级 UI/UX SKILL 插件 - UI UX Pro Max。</font>

<font style="color:rgb(51, 51, 51);">UI UX Pro Max 旨在为跨平台和多框架开发提供专业的 UI/UX 设计智能支持。</font>

<font style="color:rgb(51, 51, 51);">UI UX Pro Max 本质上是一个可检索的设计数据库，包含样式、色板、字体、组件建议及 UX 准则，专门喂给 Cursor、Claude Code、Windsurf等这些 AI 编码助手。</font>

**<font style="color:rgb(51, 51, 51);">核心亮点：</font>**

* <font style="color:rgb(51, 51, 51);">67 种 UI 风格（从 Minimalism 到 Brutalism、Glassmorphism、Bento Grid、AI-Native 等）</font>
* <font style="color:rgb(51, 51, 51);">96 个行业调色盘（SaaS、Fintech、Healthcare、Beauty、EdTech…）</font>
* <font style="color:rgb(51, 51, 51);">57 组字体搭配（Google Fonts 精选组合）</font>
* <font style="color:rgb(51, 51, 51);">25 种常用图表类型（适合 dashboard）</font>
* <font style="color:rgb(51, 51, 51);">99 条 UX 指导原则（包含可访问性、性能、交互规范）</font>
* <font style="color:rgb(51, 51, 51);">100 条行业专项推理规则（包含反面模式 Anti-patterns）</font>
* <font style="color:rgb(51, 51, 51);">支持 13 个技术栈：React / Next.js / Vue / Tailwind / Flutter / SwiftUI / HTML+CSS / Electron 等</font>

**<font style="color:rgb(51, 51, 51);">工作原理：</font>**

* <font style="color:rgb(51, 51, 51);">提出需求：构建、设计、实现、优化或评审 UI / UX</font>
* <font style="color:rgb(51, 51, 51);">技能自动触发：AI 会在内部搜索 UI 风格、配色、字体和 UX 规范数据库</font>
* <font style="color:rgb(51, 51, 51);">智能设计推荐：根据产品类型与使用场景匹配合适的设计体系</font>
* <font style="color:rgb(51, 51, 51);">直接生成代码：按最佳实践输出包含正确配色、字体、间距和结构的 UI 实现</font>

<font style="color:rgb(51, 51, 51);">开源地址：</font>[<font style="color:rgb(0, 102, 0);">https://github.com/nextlevelbuilder/ui-ux-pro-max-skill</font>](https://github.com/nextlevelbuilder/ui-ux-pro-max-skill)

<font style="color:rgb(51, 51, 51);">官方文档：</font>[<font style="color:rgb(0, 102, 0);">https://ui-ux-pro-max-skill.nextlevelbuilder.io/</font>](https://ui-ux-pro-max-skill.nextlevelbuilder.io/)

### <font style="color:rgb(51, 51, 51);">安装方式</font>

<font style="color:rgb(51, 51, 51);">1、通过 Claude Marketplace（Claude Code）安装</font>

<font style="color:rgb(51, 51, 51);">在 Claude Code 中执行以下两条命令即可直接安装。</font>

<font style="color:rgb(51, 51, 51);">注册插件市场源：</font>

<font style="color:rgb(51, 51, 51);">/plugin marketplace add nextlevelbuilder/ui-ux-pro-max-skill</font>

![1783650003964-382db435-c572-4e02-aac1-8116baaac4b9.png](./img/wf9R51v5S5sXlvV1/1783650003964-382db435-c572-4e02-aac1-8116baaac4b9-374711.png)

<font style="color:rgb(51, 51, 51);">安装插件：</font>

<font style="color:rgb(51, 51, 51);">/plugin install ui-ux-pro-max@ui-ux-pro-max-skill</font>

<font style="color:rgb(51, 51, 51);">安装成功后重启 Claude Code 就可以使用了:</font>

![1783650004499-db94e6af-e8a9-4759-87d8-b2cebebd3ee8.png](./img/wf9R51v5S5sXlvV1/1783650004499-db94e6af-e8a9-4759-87d8-b2cebebd3ee8-502490.png)

<font style="color:rgb(51, 51, 51);">2、使用 CLI（推荐）</font>

<font style="color:rgb(51, 51, 51);">全局安装 CLI：</font>

```plain
npm install -g uipro-cli

# 进入你的项目目录
cd /path/to/your/project

# 为对应 AI 助手安装
uipro init --ai claude      # Claude Code
uipro init --ai cursor      # Cursor
uipro init --ai windsurf    # Windsurf
uipro init --ai antigravity # Antigravity (.agent + .shared)
uipro init --ai copilot     # GitHub Copilot
uipro init --ai kiro        # Kiro
uipro init --ai codex       # Codex CLI
uipro init --ai qoder       # Qoder
uipro init --ai roocode     # Roo Code
uipro init --ai gemini      # Gemini CLI
uipro init --ai trae        # Trae
uipro init --ai all         # 所有助手
```

<font style="color:rgb(51, 51, 51);">3、其他 CLI 命令：</font>

```plain
uipro versions              # 查看可用版本
uipro update                # 更新到最新版本
uipro init --version v1.0.0 # 安装指定版本
```

<font style="color:rgb(51, 51, 51);">2、使用 npx</font>

<font style="color:rgb(51, 51, 51);">npx skills add https://github.com/nextlevelbuilder/ui-ux-pro-max-skill --skill ui-ux-pro-max</font>

<font style="color:rgb(51, 51, 51);">5、安装指定版本</font>

<font style="color:rgb(51, 51, 51);">安装完后，假设在 Claude 中使用，执行以下命令：</font>

<font style="color:rgb(51, 51, 51);">uipro init --ai claude</font>

*<font style="color:rgb(44, 58, 94);">搜索脚本需要使用 Python 3.x：</font>*

```plain
# 查看 Python  是否已经安装
python3 --version

# macOS
brew install python3

# Ubuntu/Debian
sudo apt update && sudo apt install python3

# Windows
winget install Python.Python.3.12
```

<font style="color:rgb(51, 51, 51);">安装完成后输出如下：</font>

![1783650004001-62abe437-212d-47ea-b8e8-94ba4642ebc4.webp](./img/wf9R51v5S5sXlvV1/1783650004001-62abe437-212d-47ea-b8e8-94ba4642ebc4-267158.webp)

<font style="color:rgb(51, 51, 51);">然后启用输入命令进入 Claude：</font>

<font style="color:rgb(51, 51, 51);">claude</font>

<font style="color:rgb(51, 51, 51);">我们可以使用</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:rgb(51, 51, 51);">/plugin</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">命令查看已经安装的创建：</font>

![1783650004065-a6338ab9-3ed2-4ca0-8489-33b3ba6cb8fa.png](./img/wf9R51v5S5sXlvV1/1783650004065-a6338ab9-3ed2-4ca0-8489-33b3ba6cb8fa-243879.png)

<font style="color:rgb(51, 51, 51);">按</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:rgb(51, 51, 51);">Esc</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">按键退出。</font>

<font style="color:rgb(51, 51, 51);">注意：通过插件安装的 Skill，目录放在</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:rgb(51, 51, 51);">～/.claude/plugins/marketplaces</font>**<font style="color:rgb(51, 51, 51);">。</font>

***

### <font style="color:rgb(51, 51, 51);">如何使用</font>

<font style="color:rgb(51, 51, 51);">接下来我们就可以直接输入需求：</font>

<font style="color:rgb(51, 51, 51);">为宠物美容服务搭建一个着陆页，风格活泼亲和，并设置预约类行动召唤按钮。</font>

<font style="color:rgb(51, 51, 51);">会提示是否使用我们安装的 skill 来设计，一路回车就好了：</font>

![1783650004183-03b261bf-4e59-4efd-b8da-5a1ab80fc8ba.png](./img/wf9R51v5S5sXlvV1/1783650004183-03b261bf-4e59-4efd-b8da-5a1ab80fc8ba-068579.png)

<font style="color:rgb(51, 51, 51);">一路回车就好了，会提示完成的功能：</font>

![1783650004610-e14645a7-e16f-40a6-ae3e-d759444f02fe.png](./img/wf9R51v5S5sXlvV1/1783650004610-e14645a7-e16f-40a6-ae3e-d759444f02fe-333942.png)

<font style="color:rgb(51, 51, 51);">然后查看最终效果，好看很多：</font>

![1783650004769-675a7101-b011-43a4-bf9f-fca67bd12cea.png](./img/wf9R51v5S5sXlvV1/1783650004769-675a7101-b011-43a4-bf9f-fca67bd12cea-235141.png)

## <font style="color:rgb(51, 51, 51);">skill-creator 使用</font>

<font style="color:rgb(51, 51, 51);">在 Claude Code 生态中，Skill（技能） 是扩展 Agent 能力的重要机制。</font>

<font style="color:rgb(51, 51, 51);">Skill 本质上是一个模块化知识包，可以给 Claude 添加：</font>

* <font style="color:rgb(51, 51, 51);">专业领域知识</font>
* <font style="color:rgb(51, 51, 51);">固定工作流程</font>
* <font style="color:rgb(51, 51, 51);">API / 工具使用方式</font>
* <font style="color:rgb(51, 51, 51);">模板和脚本</font>

<font style="color:rgb(51, 51, 51);">简单理解：</font>

<font style="color:rgb(51, 51, 51);">Skill = 给 AI 写的一份操作说明书。</font>

<font style="color:rgb(51, 51, 51);">而 skill-creator 就是 Anthropic 官方提供的 Skill 开发助手，帮助开发者创建、优化和打包技能。</font>

<font style="color:rgb(51, 51, 51);">GitHub 地址：</font>[<font style="color:rgb(0, 102, 0);">https://github.com/anthropics/skills/tree/main/skills/skill-creator</font>](https://github.com/anthropics/skills/tree/main/skills/skill-creator)

### <font style="color:rgb(51, 51, 51);">Skill 是什么</font>

<font style="color:rgb(51, 51, 51);">在 Claude Code 中，Skill 是一种 可复用的能力扩展包。</font>

<font style="color:rgb(51, 51, 51);">一个 Skill 通常包含：</font>

```plain
skill-name/
├── SKILL.md        # 核心说明（必须）
├── scripts/        # 可执行脚本
├── references/     # 文档或知识
├── assets/         # 附加资源
```

<font style="color:rgb(51, 51, 51);">其中最重要的是 SKILL.md。</font>

<font style="color:rgb(51, 51, 51);">示例：</font>

```plain
---
name: video-tool
description: Video processing CLI for editing and transcribing videos
---

# Video Tool Skill

Use the video-tool CLI to process videos.

## Quick Start

video-tool video download -u URL
video-tool generate transcript -i video.mp4
```

<font style="color:rgb(51, 51, 51);">SKILL.md 的作用就是：教 Claude 如何使用某个工具或完成某个流程。</font>

### <font style="color:rgb(51, 51, 51);">安装 skill-creator</font>

<font style="color:rgb(51, 51, 51);">首先安装 Anthropic 的 skills 集合。</font>

<font style="color:rgb(51, 51, 51);">npx skills add https://github.com/anthropics/skills --skill skill-creator</font>

<font style="color:rgb(51, 51, 51);">或者：</font>

<font style="color:rgb(51, 51, 51);">claude install anthropics/skills/skill-creator</font>

<font style="color:rgb(51, 51, 51);">安装完成后，你就可以在 Claude 中调用：</font>

<font style="color:rgb(51, 51, 51);">/skill-creator</font>

![1783650065866-d4372971-434a-487e-8066-aa6ed20edad1.png](./img/wf9R51v5S5sXlvV1/1783650065866-d4372971-434a-487e-8066-aa6ed20edad1-007286.png)

<font style="color:rgb(51, 51, 51);">skill-creator 提供完整的 Skill 开发流程工具链。</font>

<font style="color:rgb(51, 51, 51);">安装完成后，本地会下载该 Skill，其中包含：</font>

```plain
skills/skill-creator/
├── SKILL.md          ← 核心说明文件
├── agents/           ← 内置的评审助手
├── eval-viewer/      ← 测试结果可视化工具
├── references/       ← 参考文档（数据格式说明等）
└── scripts/          ← 自动化脚本（打包、测评等）
```

<font style="color:rgb(51, 51, 51);">Skill Creator 的工作流程可以概括为一个循环：</font>

```plain
想清楚需求
    ↓
起草 SKILL.md
    ↓
设计测试用例
    ↓
运行测试（有 Skill vs 没有 Skill，对比效果）
    ↓
评估结果（看报告 + 打分）
    ↓
根据反馈修改 SKILL.md
    ↓
重复，直到满意
    ↓
打包成 .skill 文件
```

***

## <font style="color:rgb(51, 51, 51);">用 skill-creator 创建 Skill</font>

### <font style="color:rgb(51, 51, 51);">需求询问</font>

<font style="color:rgb(51, 51, 51);">Claude 会先问你几个问题，帮你把需求想清楚。你不需要一次说完所有细节，像聊天一样回答就行。</font>

**<font style="color:rgb(51, 51, 51);">Claude 通常会问：</font>**

1. <font style="color:rgb(51, 51, 51);">这个 Skill 具体做什么？</font>
2. <font style="color:rgb(51, 51, 51);">什么情况下触发（用户说什么、上传什么文件）？</font>
3. <font style="color:rgb(51, 51, 51);">输出是什么格式？</font>
4. <font style="color:rgb(51, 51, 51);">有没有特殊要求（固定模板、特定格式规范……）？</font>

**<font style="color:rgb(51, 51, 51);">示例对话：</font>**

```plain
你：我想做一个 Skill，把会议录音的文字稿整理成结构化的会议纪要。

Claude：好的，我来问几个问题帮你确认需求：
        1. 纪要里需要包含哪些内容？（比如：时间、参与人、决议、行动事项……）
        2. 输出格式是 Word 文档、Markdown，还是直接在对话里回复？
        3. 有没有固定的纪要模板？

你：需要包含会议主题、时间、参与人、讨论要点、决议事项、
    下一步行动（含负责人和截止日期）。
    输出 Word 文档。
    有模板，我来上传。
```

![1783650065859-daf3c36b-6852-4be6-a40d-35aee054713d.png](./img/wf9R51v5S5sXlvV1/1783650065859-daf3c36b-6852-4be6-a40d-35aee054713d-902451.png)

<font style="color:rgb(51, 51, 51);">可以按 Tab 键或方向按键切换菜单详情，并提交。</font>

<font style="color:rgb(51, 51, 51);">这个阶段你的目标： 把所有细节和边界情况说清楚，不要跳过，后面测试时踩的坑大多源于这里没说清楚。</font>

<font style="color:rgb(51, 51, 51);">也可以直接回车，它也能帮我们创建：</font>

![1783650065835-00d26e87-bec0-4563-a3c7-4f60041e8973.png](./img/wf9R51v5S5sXlvV1/1783650065835-00d26e87-bec0-4563-a3c7-4f60041e8973-294713.png)

<font style="color:rgb(51, 51, 51);">之后 Claude 会写出 SKILL.md 草稿，大致长这样：</font>

![1783650065925-8257039f-010e-4e1a-bb45-3c0ee6773aa4.png](./img/wf9R51v5S5sXlvV1/1783650065925-8257039f-010e-4e1a-bb45-3c0ee6773aa4-783682.png)

<font style="color:rgb(51, 51, 51);">接下来还会创建参考文件：</font>

![1783650065937-e38a38d4-9cdf-485d-aa9e-be2efb2175dd.png](./img/wf9R51v5S5sXlvV1/1783650065937-e38a38d4-9cdf-485d-aa9e-be2efb2175dd-270284.png)

<font style="color:rgb(51, 51, 51);">创建完成后，会验证技能结构是否正确，等待就好了。</font>

<font style="color:rgb(51, 51, 51);">验证通过！就会打包 Skill，并展示目录结构：</font>

![1783650066414-3586a5d4-acd6-47db-9638-3100fbabb694.png](./img/wf9R51v5S5sXlvV1/1783650066414-3586a5d4-acd6-47db-9638-3100fbabb694-297729.png)

<font style="color:rgb(51, 51, 51);">测试下，输入会议内容：</font>

```plain
整理以下会议纪要：一、会议基本信息
  会议主题：学习平台内容优化会议
  参会人员：张三、李四、王五
  会议时间：2025-XX-XX 14:00-15:00
  记录人：张三
  二、会议内容
  讨论当前团队在编程教学中使用的案例素材，一致认为runoob教程简洁易懂，适合作为新手入门参考。
  确定后续内部培训将优先采用 runoob 上的基础语法、实战小案例进行讲解。
  安排李四整理 runoob 中 Python、Java 高频知识点，形成内部速查文档。
  下次会议检查文档完成情况。
  三、待办事项
  李四：整理 runoob 核心知识点文档，下周一前完成。
  全体：提前熟悉 runoob 对应章节，便于下次讨论。
```

![1783650066497-8a3de94b-d885-4cd8-bfc5-b8dc09b32ac5.png](./img/wf9R51v5S5sXlvV1/1783650066497-8a3de94b-d885-4cd8-bfc5-b8dc09b32ac5-862964.png)

# Claude Code 输出样式与 Hooks 钩子：工作流自动化赋能

## <font style="color:rgb(51, 51, 51);">Claude Code 输出样式</font>

<font style="color:rgb(51, 51, 51);">输出样式（Output Style）让你可以定制 Claude Code 的交互风格和响应方式，使其适配软件开发之外的更多使用场景，同时保留运行本地脚本、读写文件、跟踪待办事项等核心功能。</font>

<font style="color:rgb(51, 51, 51);">其本质是通过修改系统提示（System Prompt），改变 Claude Code 的交互逻辑和响应风格。</font>

***

## <font style="color:rgb(51, 51, 51);">内置输出样式</font>

<font style="color:rgb(51, 51, 51);">Claude Code 提供 3 种开箱即用的输出样式：</font>

| <font style="color:rgb(255, 255, 255);">样式名称</font> | <font style="color:rgb(255, 255, 255);">适用场景</font> | <font style="color:rgb(255, 255, 255);">核心特点</font> |
| --- | --- | --- |
| **<font style="color:rgb(51, 51, 51);">默认样式（default）</font>** | <font style="color:rgb(51, 51, 51);">日常软件工程任务</font> | <font style="color:rgb(51, 51, 51);">专注高效完成编码、调试、重构等工作，回复简洁直接</font> |
| **<font style="color:rgb(51, 51, 51);">解释性样式（explanatory）</font>** | <font style="color:rgb(51, 51, 51);">边做边学场景</font> | <font style="color:rgb(51, 51, 51);">在完成任务的同时讲解实现思路、设计模式等知识点，适合想深入理解代码的开发者</font> |
| **<font style="color:rgb(51, 51, 51);">学习样式（learning）</font>** | <font style="color:rgb(51, 51, 51);">主动实践式学习</font> | <font style="color:rgb(51, 51, 51);">与你协作完成任务，会在关键位置添加</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">TODO(human)</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">标记，引导你亲手实现核心代码片段，而不是直接给出答案</font> |

***

## <font style="color:rgb(51, 51, 51);">工作原理</font>

<font style="color:rgb(51, 51, 51);">切换输出样式时，Claude Code 会按以下规则调整系统提示：</font>

1. <font style="color:rgb(51, 51, 51);">所有样式都会移除默认的"简洁回复、高效输出"等约束指令</font>
2. <font style="color:rgb(51, 51, 51);">自定义样式默认会剔除"用测试验证代码"等编码相关指令（如需保留，可在样式文件中开启</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">keep-coding-instructions: true</font></code><font style="color:rgb(51, 51, 51);">）</font>
3. <font style="color:rgb(51, 51, 51);">每种样式会在系统提示末尾追加自定义规则，覆盖默认行为</font>
4. <font style="color:rgb(51, 51, 51);">对话过程中会触发合规检查，确保 Claude 始终遵守当前样式的指令</font>

***

## <font style="color:rgb(51, 51, 51);">切换输出样式</font>

<font style="color:rgb(51, 51, 51);">切换样式有两种方式，配置保存在项目目录的</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">.claude/settings.local.json</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">文件中，</font>**<font style="color:rgb(51, 51, 51);">仅对当前项目生效</font>**<font style="color:rgb(51, 51, 51);">：</font>

**<font style="color:rgb(51, 51, 51);">方式一：菜单选择</font>**<font style="color:rgb(51, 51, 51);">——输入命令后，在交互菜单中选择目标样式：</font>

<font style="color:rgb(51, 51, 51);">/output-style</font>

**<font style="color:rgb(51, 51, 51);">方式二：直接指定</font>**<font style="color:rgb(51, 51, 51);">——在命令后直接加上样式名称，一步到位：</font>

<font style="color:rgb(51, 51, 51);">/output-style explanatory</font><font style="color:rgb(51, 51, 51);">/output-style learning</font><font style="color:rgb(51, 51, 51);">/output-style default</font>

*<font style="color:rgb(44, 58, 94);">除了使用命令切换，也可以直接编辑</font>\_\_<font style="color:rgb(44, 58, 94);"> </font>*<code>_<font style="color:rgb(44, 58, 94);">.claude/settings.local.json</font>_</code>*<font style="color:rgb(44, 58, 94);">（项目级）或</font>\_\_<font style="color:rgb(44, 58, 94);"> </font>*<code>_<font style="color:rgb(44, 58, 94);">~/.claude/settings.json</font>_</code>*<font style="color:rgb(44, 58, 94);">（全局级）文件，修改</font>\_\_<font style="color:rgb(44, 58, 94);"> </font>*<code>_<font style="color:rgb(44, 58, 94);">outputStyle</font>_</code>*<font style="color:rgb(44, 58, 94);"> </font>\_\_<font style="color:rgb(44, 58, 94);">字段的值来切换样式。</font>*

***

## <font style="color:rgb(51, 51, 51);">创建自定义输出样式</font>

<font style="color:rgb(51, 51, 51);">如果内置样式不满足需求，可以通过 Markdown 文件定义专属样式。</font>

### <font style="color:rgb(51, 51, 51);">1、文件保存位置</font>

| <font style="color:rgb(255, 255, 255);">级别</font> | <font style="color:rgb(255, 255, 255);">保存路径</font> | <font style="color:rgb(255, 255, 255);">作用范围</font> |
| --- | --- | --- |
| **<font style="color:rgb(51, 51, 51);">用户级别</font>** | <code><font style="color:rgb(51, 51, 51);">~/.claude/output-styles/</font></code> | <font style="color:rgb(51, 51, 51);">当前用户的所有项目均可使用</font> |
| **<font style="color:rgb(51, 51, 51);">项目级别</font>** | <code><font style="color:rgb(51, 51, 51);">.claude/output-styles/</font></code><br/><font style="color:rgb(51, 51, 51);">（项目根目录下）</font> | <font style="color:rgb(51, 51, 51);">仅当前项目可用，可提交到 git 与团队共享</font> |

### <font style="color:rgb(51, 51, 51);">2、文件格式</font>

<font style="color:rgb(51, 51, 51);">自定义样式文件由两部分组成：顶部的</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:rgb(51, 51, 51);">YAML frontmatter</font>**<font style="color:rgb(51, 51, 51);">（元数据配置）和下方的</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:rgb(51, 51, 51);">Markdown 正文</font>**<font style="color:rgb(51, 51, 51);">（具体指令内容）。</font>

**<font style="color:rgb(97, 127, 16);">实例</font>**

<font style="color:cyan;">---</font><font style="color:green;">\
</font><font style="color:green;">name</font>**<font style="color:brown;">:</font>\*\*\*\*<font style="color:brown;"> </font>**<font style="color:rgb(51, 51, 51);">data-analyst              </font><font style="color:rgb(51, 51, 51);"> </font><font style="color:blue;"># 样式名称，显示在 /output-style 菜单中（未填则使用文件名）</font><font style="color:green;">\
</font><font style="color:green;">description</font>**<font style="color:brown;">:</font>\*\*\*\*<font style="color:brown;"> </font>**<font style="color:rgb(51, 51, 51);">专注将复杂数据转化为可视化报告和分析结论\
</font><font style="color:blue;"># 样式描述，显示在菜单的说明文字中（可选）</font><font style="color:green;">\
</font><font style="color:green;">keep-coding-instructions</font>**<font style="color:brown;">:</font>\*\*\*\*<font style="color:brown;"> </font>**<font style="color:rgb(51, 51, 51);">false  </font><font style="color:blue;"># 是否保留默认编码相关指令</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:blue;"># false（默认）：剔除编码指令，适合非开发场景</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:blue;"># true：保留编码指令，同时叠加自定义规则</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:cyan;">---</font><font style="color:rgb(51, 51, 51);">

</font><font style="color:blue;"># 角色定位</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);">你是一个专业的数据分析助手，擅长使用 Python 处理各类结构化数据，\
</font><font style="color:rgb(51, 51, 51);">并将复杂数据转化为简洁易懂的可视化报告。

</font><font style="color:blue;">## 响应规则</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);">1</font><font style="color:rgb(51, 51, 51);">. 所有分析必须包含「结论 + 数据支撑 + 优化建议」三部分\
</font><font style="color:rgb(51, 51, 51);">2</font><font style="color:rgb(51, 51, 51);">. 生成代码时必须附带详细注释，优先使用 Pandas 和 Matplotlib\
</font><font style="color:rgb(51, 51, 51);">3</font><font style="color:rgb(51, 51, 51);">. 避免专业术语堆砌，用通俗语言解释复杂概念

</font><font style="color:blue;">## 格式要求</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);">1</font><font style="color:rgb(51, 51, 51);">. 结论部分加粗显示\
</font><font style="color:rgb(51, 51, 51);">2</font><font style="color:rgb(51, 51, 51);">. 代码块使用 \`\`\`python 标签包裹\
</font><font style="color:rgb(51, 51, 51);">3</font><font style="color:rgb(51, 51, 51);">. 建议部分使用有序列表呈现

</font><font style="color:blue;">## 特殊场景</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);">1</font><font style="color:rgb(51, 51, 51);">. 遇到缺失数据时，主动提示用户补充关键信息，而非直接报错\
</font><font style="color:rgb(51, 51, 51);">2</font><font style="color:rgb(51, 51, 51);">. 生成可视化图表时，默认使用中文标签和浅色主题</font>

### <font style="color:rgb(51, 51, 51);">3、frontmatter 参数说明</font>

| <font style="color:rgb(255, 255, 255);">参数名</font> | <font style="color:rgb(255, 255, 255);">是否必填</font> | <font style="color:rgb(255, 255, 255);">说明</font> | <font style="color:rgb(255, 255, 255);">默认值</font> |
| --- | --- | --- | --- |
| <code><font style="color:rgb(51, 51, 51);">name</font></code> | <font style="color:rgb(51, 51, 51);">否</font> | <font style="color:rgb(51, 51, 51);">样式名称，显示在</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">/output-style</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">菜单中。未填则使用文件名（不含 .md 后缀）</font> | <font style="color:rgb(51, 51, 51);">文件名</font> |
| <code><font style="color:rgb(51, 51, 51);">description</font></code> | <font style="color:rgb(51, 51, 51);">否</font> | <font style="color:rgb(51, 51, 51);">样式功能的简要描述，显示在菜单的说明文字中，帮助区分多个自定义样式</font> | <font style="color:rgb(51, 51, 51);">无</font> |
| <code><font style="color:rgb(51, 51, 51);">keep-coding-instructions</font></code> | <font style="color:rgb(51, 51, 51);">否</font> | <font style="color:rgb(51, 51, 51);">是否保留默认系统提示中的编码相关指令。设为</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">true</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">时，自定义指令会叠加在默认编码指令之上</font> | <code><font style="color:rgb(51, 51, 51);">false</font></code> |

### <font style="color:rgb(51, 51, 51);">4、使用步骤</font>

1. <font style="color:rgb(51, 51, 51);">按上述格式创建</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">.md</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">文件（例如</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">data-analyst.md</font></code><font style="color:rgb(51, 51, 51);">）</font>
2. <font style="color:rgb(51, 51, 51);">将文件放到对应目录：</font>
   * <font style="color:rgb(51, 51, 51);">所有项目可用：</font><code><font style="color:rgb(51, 51, 51);">~/.claude/output-styles/data-analyst.md</font></code>
   * <font style="color:rgb(51, 51, 51);">仅当前项目可用：</font><code><font style="color:rgb(51, 51, 51);">.claude/output-styles/data-analyst.md</font></code>
3. <font style="color:rgb(51, 51, 51);">在 Claude Code 中执行</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">/output-style</font></code><font style="color:rgb(51, 51, 51);">，即可在菜单中看到并选择新创建的样式</font>

***

## <font style="color:rgb(51, 51, 51);">与相关功能的区别</font>

<font style="color:rgb(51, 51, 51);">输出样式与以下几个功能看起来相似，但作用层面不同：</font>

| <font style="color:rgb(255, 255, 255);">对比对象</font> | <font style="color:rgb(255, 255, 255);">核心差异</font> |
| --- | --- |
| **<font style="color:rgb(51, 51, 51);">输出样式 vs CLAUDE.md</font>** | <font style="color:rgb(51, 51, 51);">输出样式会</font>**<font style="color:rgb(51, 51, 51);">替换</font>**<font style="color:rgb(51, 51, 51);">默认的软件工程系统提示，从根本上改变 Claude 的工作模式；CLAUDE.md 是以用户消息的形式追加项目背景和约定，不修改系统提示本身</font> |
| **<font style="color:rgb(51, 51, 51);">输出样式 vs --append-system-prompt</font>** | <font style="color:rgb(51, 51, 51);">输出样式替换并关闭默认提示；</font><code><font style="color:rgb(51, 51, 51);">--append-system-prompt</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">是在默认提示的末尾追加内容，两者均保留原有提示</font> |
| **<font style="color:rgb(51, 51, 51);">输出样式 vs 子代理（Subagent）</font>** | <font style="color:rgb(51, 51, 51);">输出样式修改的是主代理的系统提示，影响全局交互风格；子代理是独立的任务处理模块，可以自定义模型、工具和触发条件，处理特定子任务后返回结果</font> |
| **<font style="color:rgb(51, 51, 51);">输出样式 vs 自定义斜杠命令</font>** | <font style="color:rgb(51, 51, 51);">输出样式是"存储的系统提示"，决定 Claude 整体的交互风格；自定义斜杠命令是"存储的用户提示"，用于快速执行某个具体的指令或任务</font> |

***

## <font style="color:rgb(51, 51, 51);">自定义样式模板</font>

<font style="color:rgb(51, 51, 51);">以下是一个通用的自定义输出样式模板，将</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">[ ]</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">中的内容替换为你的实际需求，保存为</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">.md</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">文件即可使用：</font>

**<font style="color:rgb(97, 127, 16);">实例</font>**

<font style="color:cyan;">---</font><font style="color:green;">\
</font><font style="color:green;">name</font>**<font style="color:brown;">:</font>\*\*\*\*<font style="color:brown;"> </font>**<font style="color:rgb(51, 51, 51);">\[</font><font style="color:rgb(51, 51, 51);">样式名称，例如：写作助手</font><font style="color:rgb(51, 51, 51);">]</font><font style="color:green;">\
</font><font style="color:green;">description</font>**<font style="color:brown;">:</font>\*\*\*\*<font style="color:brown;"> </font>**<font style="color:rgb(51, 51, 51);">\[</font><font style="color:rgb(51, 51, 51);">一句话说明用途，例如：专注技术文档写作，输出结构清晰、表达准确的内容</font><font style="color:rgb(51, 51, 51);">]</font><font style="color:green;">\
</font><font style="color:green;">keep-coding-instructions</font>**<font style="color:brown;">:</font>\*\*\*\*<font style="color:brown;"> </font>**<font style="color:rgb(51, 51, 51);">\[</font><font style="color:rgb(51, 51, 51);">true 或 false</font><font style="color:rgb(51, 51, 51);">]</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:cyan;">---</font><font style="color:rgb(51, 51, 51);">

</font><font style="color:blue;"># 一、核心定位</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);">\[</font><font style="color:rgb(51, 51, 51);">定义 Claude 的角色和专长，例如：\
</font><font style="color:rgb(51, 51, 51);">你是一个专业的技术文档写作助手，擅长将复杂的技术概念转化为清晰易懂的文字</font><font style="color:rgb(51, 51, 51);">]</font><font style="color:rgb(51, 51, 51);">

</font><font style="color:blue;"># 二、响应规则</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);">\[</font><font style="color:rgb(51, 51, 51);">规定 Claude 的回复逻辑，例如：\
</font><font style="color:rgb(51, 51, 51);">1</font><font style="color:rgb(51, 51, 51);">. 每次回复必须包含「核心观点 + 详细说明 + 示例」三部分\
</font><font style="color:rgb(51, 51, 51);">2</font><font style="color:rgb(51, 51, 51);">. 使用主动语态，避免被动句式\
</font><font style="color:rgb(51, 51, 51);">3</font><font style="color:rgb(51, 51, 51);">. 专业术语首次出现时附带简短解释</font><font style="color:rgb(51, 51, 51);">]</font><font style="color:rgb(51, 51, 51);">

</font><font style="color:blue;"># 三、格式要求</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);">\[</font><font style="color:rgb(51, 51, 51);">指定输出的排版格式，例如：\
</font><font style="color:rgb(51, 51, 51);">1</font><font style="color:rgb(51, 51, 51);">. 标题使用</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:blue;">## 二级标题</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);">2</font><font style="color:rgb(51, 51, 51);">. 代码示例使用代码块，并标注语言类型\
</font><font style="color:rgb(51, 51, 51);">3</font><font style="color:rgb(51, 51, 51);">. 关键信息用粗体标注</font><font style="color:rgb(51, 51, 51);">]</font><font style="color:rgb(51, 51, 51);">

</font><font style="color:blue;"># 四、特殊场景处理</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);">\[</font><font style="color:rgb(51, 51, 51);">针对特定情况的处理规则，例如：\
</font><font style="color:rgb(51, 51, 51);">1</font><font style="color:rgb(51, 51, 51);">. 需要举例时，优先使用真实场景而非抽象示例\
</font><font style="color:rgb(51, 51, 51);">2</font><font style="color:rgb(51, 51, 51);">. 遇到表述不清的需求时，先确认意图再开始写作</font><font style="color:rgb(51, 51, 51);">]</font>

## <font style="color:rgb(51, 51, 51);">Claude Code 钩子</font>

<font style="color:rgb(51, 51, 51);">Claude Code 钩子是</font>**<font style="color:rgb(51, 51, 51);">用户自定义的 Shell 命令</font>**<font style="color:rgb(51, 51, 51);">，会在 Claude Code 生命周期的特定节点自动执行。</font>

<font style="color:rgb(51, 51, 51);">借助钩子，你可以对 Claude Code 的行为实现精准控制，确保某些操作（如代码格式化、日志记录）</font>**<font style="color:rgb(51, 51, 51);">必定触发</font>**<font style="color:rgb(51, 51, 51);">，而非依赖大模型自主选择是否执行。</font>

### <font style="color:rgb(51, 51, 51);">钩子的典型应用场景</font>

<font style="color:rgb(51, 51, 51);">钩子能帮你实现很多实用功能，常见场景包括：</font>

* **<font style="color:rgb(51, 51, 51);">消息通知</font>**<font style="color:rgb(51, 51, 51);">：当 Claude Code 等待输入或需要权限时，自动发送桌面/邮件提醒</font>
* **<font style="color:rgb(51, 51, 51);">自动格式化</font>**<font style="color:rgb(51, 51, 51);">：编辑</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">.ts</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">文件后自动运行</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">prettier</font></code><font style="color:rgb(51, 51, 51);">，修改</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">.go</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">文件后执行</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">gofmt</font></code>
* **<font style="color:rgb(51, 51, 51);">操作日志</font>**<font style="color:rgb(51, 51, 51);">：记录 Claude 执行的所有命令，用于合规审计或调试排障</font>
* **<font style="color:rgb(51, 51, 51);">代码规范校验</font>**<font style="color:rgb(51, 51, 51);">：若 Claude 生成的代码不符合项目规范（如命名规则），自动给出反馈</font>
* **<font style="color:rgb(51, 51, 51);">文件权限管控</font>**<font style="color:rgb(51, 51, 51);">：阻止 Claude 修改生产环境配置文件或敏感目录（如</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">.env</font></code><font style="color:rgb(51, 51, 51);">、</font><code><font style="color:rgb(51, 51, 51);">.git</font></code><font style="color:rgb(51, 51, 51);">）</font>

<font style="color:rgb(51, 51, 51);">相比于通过提示词约束 Claude 的行为，钩子是</font>**<font style="color:rgb(51, 51, 51);">应用级的硬规则</font>**<font style="color:rgb(51, 51, 51);">，只要触发对应事件就会强制执行，稳定性和可靠性更高。</font>

### <font style="color:rgb(51, 51, 51);">重要安全提醒</font>

<font style="color:rgb(51, 51, 51);">钩子运行时会</font>**<font style="color:rgb(51, 51, 51);">直接使用当前系统环境的凭证</font>**<font style="color:rgb(51, 51, 51);">（如环境变量、用户权限），存在一定安全风险：</font>

* <font style="color:rgb(51, 51, 51);">恶意钩子代码可能泄露你的敏感数据（如 API 密钥、项目源码）</font>
* <font style="color:rgb(51, 51, 51);">错误的钩子命令可能导致文件误删、系统异常</font>

**<font style="color:rgb(51, 51, 51);">必做安全操作</font>**<font style="color:rgb(51, 51, 51);">：</font>

1. <font style="color:rgb(51, 51, 51);">注册钩子前，务必逐行审查命令的逻辑和权限</font>
2. <font style="color:rgb(51, 51, 51);">避免在钩子中执行来源不明的脚本</font>
3. <font style="color:rgb(51, 51, 51);">详细安全最佳实践，可参考官方文档的</font><font style="color:rgb(51, 51, 51);"> </font>[<font style="color:rgb(0, 102, 0);">安全注意事项</font>](https://code.claude.com/docs/zh-CN/hooks#security-considerations)

***

## <font style="color:rgb(51, 51, 51);">钩子事件类型说明</font>

<font style="color:rgb(51, 51, 51);">Claude Code 内置了多个生命周期事件，你可以为不同事件绑定钩子命令。每个事件会传递不同的上下文数据，且对 Claude 行为的影响方式不同。</font>

| <font style="color:rgb(255, 255, 255);">事件名称</font> | <font style="color:rgb(255, 255, 255);">触发时机</font> | <font style="color:rgb(255, 255, 255);">核心作用</font> |
| --- | --- | --- |
| <code><font style="color:rgb(51, 51, 51);">PreToolUse</font></code> | <font style="color:rgb(51, 51, 51);">工具调用</font>**<font style="color:rgb(51, 51, 51);">之前</font>** | <font style="color:rgb(51, 51, 51);">可拦截工具执行（如阻止修改敏感文件），并向 Claude 反馈调整建议</font> |
| <code><font style="color:rgb(51, 51, 51);">PermissionRequest</font></code> | <font style="color:rgb(51, 51, 51);">弹出权限请求对话框时</font> | <font style="color:rgb(51, 51, 51);">自动批准或拒绝权限申请</font> |
| <code><font style="color:rgb(51, 51, 51);">PostToolUse</font></code> | <font style="color:rgb(51, 51, 51);">工具调用</font>**<font style="color:rgb(51, 51, 51);">完成后</font>** | <font style="color:rgb(51, 51, 51);">执行后置操作（如格式化代码、记录日志）</font> |
| <code><font style="color:rgb(51, 51, 51);">UserPromptSubmit</font></code> | <font style="color:rgb(51, 51, 51);">用户提交提示词后、Claude 处理前</font> | <font style="color:rgb(51, 51, 51);">预处理用户输入（如补充上下文信息）</font> |
| <code><font style="color:rgb(51, 51, 51);">Notification</font></code> | <font style="color:rgb(51, 51, 51);">Claude 发送通知时</font> | <font style="color:rgb(51, 51, 51);">自定义通知方式（如桌面弹窗、短信提醒）</font> |
| <code><font style="color:rgb(51, 51, 51);">Stop</font></code> | <font style="color:rgb(51, 51, 51);">Claude 完成响应时</font> | <font style="color:rgb(51, 51, 51);">执行收尾工作（如清理临时文件）</font> |
| <code><font style="color:rgb(51, 51, 51);">SubagentStop</font></code> | <font style="color:rgb(51, 51, 51);">子代理任务完成时</font> | <font style="color:rgb(51, 51, 51);">处理子代理的执行结果</font> |
| <code><font style="color:rgb(51, 51, 51);">PreCompact</font></code> | <font style="color:rgb(51, 51, 51);">即将执行上下文压缩操作时</font> | <font style="color:rgb(51, 51, 51);">自定义压缩规则</font> |
| <code><font style="color:rgb(51, 51, 51);">SessionStart</font></code> | <font style="color:rgb(51, 51, 51);">启动新会话或恢复旧会话时</font> | <font style="color:rgb(51, 51, 51);">初始化会话环境（如加载项目配置）</font> |
| <code><font style="color:rgb(51, 51, 51);">SessionEnd</font></code> | <font style="color:rgb(51, 51, 51);">会话结束时</font> | <font style="color:rgb(51, 51, 51);">保存会话数据、清理环境</font> |

***

## <font style="color:rgb(51, 51, 51);">快速入门：实现命令日志记录</font>

<font style="color:rgb(51, 51, 51);">下面以</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:rgb(51, 51, 51);">记录 Claude 执行的所有 Bash 命令</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">为例，带你一步步完成钩子的配置和使用。</font>

### <font style="color:rgb(51, 51, 51);">前置准备</font>

<font style="color:rgb(51, 51, 51);">安装</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">jq</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">工具（用于命令行解析 JSON 数据）：</font>

* **<font style="color:rgb(51, 51, 51);">macOS</font>**<font style="color:rgb(51, 51, 51);">：</font><code><font style="color:rgb(51, 51, 51);">brew install jq</font></code>
* **<font style="color:rgb(51, 51, 51);">Linux</font>**<font style="color:rgb(51, 51, 51);">：</font><code><font style="color:rgb(51, 51, 51);">sudo apt install jq</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">/</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">sudo yum install jq</font></code>
* **<font style="color:rgb(51, 51, 51);">Windows</font>**<font style="color:rgb(51, 51, 51);">：下载</font><font style="color:rgb(51, 51, 51);"> </font>[<font style="color:rgb(0, 102, 0);">jq 官方安装包</font>](https://stedolan.github.io/jq/download/)<font style="color:rgb(51, 51, 51);">，或通过 WSL 安装</font>

### <font style="color:rgb(51, 51, 51);">步骤 1：打开钩子配置界面</font>

<font style="color:rgb(51, 51, 51);">在 Claude Code 的交互界面中，输入斜杠命令</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">/hooks</font></code><font style="color:rgb(51, 51, 51);">，回车后选择要绑定的事件 —— 这里我们选</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">PreToolUse</font></code><font style="color:rgb(51, 51, 51);">（工具调用前触发，适合记录命令）。</font>

### <font style="color:rgb(51, 51, 51);">步骤 2：添加事件匹配器</font>

<font style="color:rgb(51, 51, 51);">匹配器的作用是</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:rgb(51, 51, 51);">限定钩子的触发条件</font>**<font style="color:rgb(51, 51, 51);">，只在指定工具被调用时执行钩子命令。</font>

1. <font style="color:rgb(51, 51, 51);">选择</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">+ Add new matcher…</font></code>
2. <font style="color:rgb(51, 51, 51);">输入匹配关键词</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">Bash</font></code><font style="color:rgb(51, 51, 51);">，表示仅当 Claude 调用 Bash 工具时触发钩子</font>

*<font style="color:rgb(44, 58, 94);">小技巧：输入</font>\_\_<font style="color:rgb(44, 58, 94);"> </font>*<code>_<font style="color:rgb(44, 58, 94);">*</font>_</code>*<font style="color:rgb(44, 58, 94);"> </font>**<font style="color:rgb(44, 58, 94);">可以匹配</font>**__<font style="color:rgb(44, 58, 94);">所有工具</font>__\_\_<font style="color:rgb(44, 58, 94);">，实现全局钩子</font>*

### <font style="color:rgb(51, 51, 51);">步骤 3：添加钩子命令</font>

<font style="color:rgb(51, 51, 51);">选择</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">+ Add new hook…</font></code><font style="color:rgb(51, 51, 51);">，输入以下命令（功能：提取命令内容和描述，写入日志文件）：</font>

jq -r '"(.tool_input.command) - (.tool_input.description // "无描述信息")"' >> ~/.claude/bash-command-log.txt

<font style="color:rgb(51, 51, 51);">命令说明：</font>

* <code><font style="color:rgb(51, 51, 51);">jq -r ...</font></code><font style="color:rgb(51, 51, 51);">：提取 JSON 中的命令（</font><code><font style="color:rgb(51, 51, 51);">command</font></code><font style="color:rgb(51, 51, 51);">）和描述（</font><code><font style="color:rgb(51, 51, 51);">description</font></code><font style="color:rgb(51, 51, 51);">），无描述时显示"无描述信息"</font>
* <code><font style="color:rgb(51, 51, 51);">>> ~/.claude/...</font></code><font style="color:rgb(51, 51, 51);">：将内容追加写入用户主目录下的日志文件</font>

### <font style="color:rgb(51, 51, 51);">步骤 4：选择配置存储位置</font>

<font style="color:rgb(51, 51, 51);">配置保存位置决定钩子的生效范围：</font>

* **<font style="color:rgb(51, 51, 51);">User settings</font>**<font style="color:rgb(51, 51, 51);">：保存到用户级配置（</font><code><font style="color:rgb(51, 51, 51);">~/.claude/settings.json</font></code><font style="color:rgb(51, 51, 51);">），</font>**<font style="color:rgb(51, 51, 51);">所有项目生效</font>**
* **<font style="color:rgb(51, 51, 51);">Project settings</font>**<font style="color:rgb(51, 51, 51);">：保存到当前项目配置（</font><code><font style="color:rgb(51, 51, 51);">.claude/settings.local.json</font></code><font style="color:rgb(51, 51, 51);">），</font>**<font style="color:rgb(51, 51, 51);">仅当前项目生效</font>**

<font style="color:rgb(51, 51, 51);">这里我们选</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">User settings</font></code><font style="color:rgb(51, 51, 51);">，实现全局命令日志记录。选择后按</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">Esc</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">键退出配置界面，钩子即注册完成。</font>

### <font style="color:rgb(51, 51, 51);">步骤 5：验证钩子配置</font>

1. <font style="color:rgb(51, 51, 51);">再次输入</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">/hooks</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">命令，可查看已配置的钩子列表</font>
2. <font style="color:rgb(51, 51, 51);">或直接打开配置文件</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">~/.claude/settings.json</font></code><font style="color:rgb(51, 51, 51);">，会看到如下配置内容：</font>

```plain
{
  "hooks": {
    "PreToolUse": [
      {
        "matcher": "Bash",
        "hooks": [
          {
            "type": "command",
            "command": "jq -r '\"\\(.tool_input.command) - \\(.tool_input.description // \"无描述信息\")\"' >> ~/.claude/bash-command-log.txt"
          }
        ]
      }
    ]
  }
}
```

### <font style="color:rgb(51, 51, 51);">步骤 6：测试钩子效果</font>

1. <font style="color:rgb(51, 51, 51);">在 Claude Code 中输入指令：</font><code><font style="color:rgb(51, 51, 51);">帮我执行 ls 命令</font></code>
2. <font style="color:rgb(51, 51, 51);">执行完成后，在终端中查看日志文件：</font><font style="color:rgb(51, 51, 51);">cat ~/.claude/bash-command-log.txt</font>
3. <font style="color:rgb(51, 51, 51);">若日志中出现如下内容，说明钩子配置成功：</font><font style="color:rgb(51, 51, 51);">ls - Lists files and directories</font>

***

## <font style="color:rgb(51, 51, 51);">实用钩子示例</font>

<font style="color:rgb(51, 51, 51);">下面提供几个常用的钩子配置，你可以直接复制使用或按需修改。</font>

*<font style="color:rgb(44, 58, 94);">📌</font>\_\_<font style="color:rgb(44, 58, 94);"> 完整示例代码可参考官方仓库：</font>*[*<font style="color:rgb(0, 102, 0);">bash 命令验证器示例</font>*](https://github.com/anthropics/claude-code/blob/main/examples/hooks/bash_command_validator_example.py)

### <font style="color:rgb(51, 51, 51);">示例 1：自动格式化 TypeScript 文件</font>

<font style="color:rgb(51, 51, 51);">功能：编辑/写入</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">.ts</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">文件后，自动用</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">prettier</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">格式化代码</font>

```plain
{
  "hooks": {
    "PostToolUse": [
      {
        "matcher": "Edit|Write", // 匹配“编辑”和“写入”工具
        "hooks": [
          {
            "type": "command",
            "command": "jq -r '.tool_input.file_path' | { read file_path; if echo \"$file_path\" | grep -q '\\.ts$'; then npx prettier --write \"$file_path\"; fi; }"
          }
        ]
      }
    ]
  }
}
```

### <font style="color:rgb(51, 51, 51);">示例 2：自动修复 Markdown 文件格式</font>

<font style="color:rgb(51, 51, 51);">功能：为无语言标签的代码块自动补全标签、清理多余空行</font>

#### <font style="color:rgb(51, 51, 51);">第一步：添加钩子配置</font>

```plain
{
  "hooks": {
    "PostToolUse": [
      {
        "matcher": "Edit|Write",
        "hooks": [
          {
            "type": "command",
            "command": "\"$CLAUDE_PROJECT_DIR\"/.claude/hooks/markdown_formatter.py"
          }
        ]
      }
    ]
  }
}
```

#### <font style="color:rgb(51, 51, 51);">第二步：创建格式化脚本</font>

<font style="color:rgb(51, 51, 51);">在项目目录下新建文件</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">.claude/hooks/markdown_formatter.py</font></code><font style="color:rgb(51, 51, 51);">，粘贴以下代码：</font>

**<font style="color:rgb(97, 127, 16);">实例</font>**

<font style="color:rgb(170, 85, 0);">#!/usr/bin/env python3</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(170, 17, 17);">"""\
</font><font style="color:rgb(170, 17, 17);">Markdown 格式化工具：自动补全代码块语言标签、清理多余空行\
</font><font style="color:rgb(170, 17, 17);">"""</font><font style="color:rgb(51, 51, 51);">\
</font>**<font style="color:green;">import</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">json\
</font>**<font style="color:green;">import</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 85, 170);">sys</font><font style="color:rgb(51, 51, 51);">\
</font>**<font style="color:green;">import</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 85, 170);">re</font><font style="color:rgb(51, 51, 51);">\
</font>**<font style="color:green;">import</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 85, 170);">os</font><font style="color:rgb(51, 51, 51);">

</font>**<font style="color:green;">def</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">detect_language</font><font style="color:olive;">(</font><font style="color:rgb(0, 85, 170);">code</font><font style="color:olive;">)</font><font style="color:rgb(51, 51, 51);">:\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(170, 17, 17);">"""根据代码内容自动检测编程语言"""</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 85, 170);">code</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:gray;">=</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 85, 170);">code</font><font style="color:rgb(51, 51, 51);">.</font><font style="color:rgb(0, 85, 170);">strip</font><font style="color:olive;">(</font><font style="color:olive;">)</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(170, 85, 0);"># 检测 JSON</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:green;">if</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 85, 170);">re</font><font style="color:rgb(51, 51, 51);">.</font><font style="color:rgb(0, 85, 170);">search</font><font style="color:olive;">(</font><font style="color:rgb(51, 51, 51);">r</font><font style="color:rgb(170, 17, 17);">'^</font>**<font style="color:rgb(0, 0, 153);">\s</font>**<font style="color:rgb(170, 17, 17);">*\[{</font>**<font style="color:rgb(0, 0, 153);">\[</font>**<font style="color:rgb(170, 17, 17);">]'</font><font style="color:gray;">,</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 85, 170);">code</font><font style="color:olive;">)</font><font style="color:rgb(51, 51, 51);">:\
</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:green;">try</font>**<font style="color:rgb(51, 51, 51);">:\
</font><font style="color:rgb(51, 51, 51);">json.</font><font style="color:rgb(0, 85, 170);">loads</font><font style="color:olive;">(</font><font style="color:rgb(0, 85, 170);">code</font><font style="color:olive;">)</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:green;">return</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(170, 17, 17);">'json'</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:green;">except</font>**<font style="color:rgb(51, 51, 51);">:\
</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:green;">pass</font>**<font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(170, 85, 0);"># 检测 Python</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:green;">if</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 85, 170);">re</font><font style="color:rgb(51, 51, 51);">.</font><font style="color:rgb(0, 85, 170);">search</font><font style="color:olive;">(</font><font style="color:rgb(51, 51, 51);">r</font><font style="color:rgb(170, 17, 17);">'^</font>**<font style="color:rgb(0, 0, 153);">\s</font>**<font style="color:rgb(170, 17, 17);">*def</font>**<font style="color:rgb(0, 0, 153);">\s</font>**<font style="color:rgb(170, 17, 17);">+</font>**<font style="color:rgb(0, 0, 153);">\w</font>**<font style="color:rgb(170, 17, 17);">+</font>**<font style="color:rgb(0, 0, 153);">\s</font>**<font style="color:rgb(170, 17, 17);">*</font>**<font style="color:rgb(0, 0, 153);">(</font>**<font style="color:rgb(170, 17, 17);">'</font><font style="color:gray;">,</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 85, 170);">code</font><font style="color:gray;">,</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 85, 170);">re</font><font style="color:rgb(51, 51, 51);">.</font><font style="color:rgb(0, 85, 170);">M</font><font style="color:olive;">)</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:green;">or</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 85, 170);">re</font><font style="color:rgb(51, 51, 51);">.</font><font style="color:rgb(0, 85, 170);">search</font><font style="color:olive;">(</font><font style="color:rgb(51, 51, 51);">r</font><font style="color:rgb(170, 17, 17);">'^</font>**<font style="color:rgb(0, 0, 153);">\s</font>**<font style="color:rgb(170, 17, 17);">*(import|from)</font>**<font style="color:rgb(0, 0, 153);">\s</font>**<font style="color:rgb(170, 17, 17);">+</font>**<font style="color:rgb(0, 0, 153);">\w</font>**<font style="color:rgb(170, 17, 17);">+'</font><font style="color:gray;">,</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 85, 170);">code</font><font style="color:gray;">,</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 85, 170);">re</font><font style="color:rgb(51, 51, 51);">.</font><font style="color:rgb(0, 85, 170);">M</font><font style="color:olive;">)</font><font style="color:rgb(51, 51, 51);">:\
</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:green;">return</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(170, 17, 17);">'python'</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(170, 85, 0);"># 检测 JavaScript/TypeScript</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:green;">if</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 85, 170);">re</font><font style="color:rgb(51, 51, 51);">.</font><font style="color:rgb(0, 85, 170);">search</font><font style="color:olive;">(</font><font style="color:rgb(51, 51, 51);">r</font><font style="color:rgb(170, 17, 17);">'</font>**<font style="color:rgb(0, 0, 153);">\b</font>**<font style="color:rgb(170, 17, 17);">(function</font>**<font style="color:rgb(0, 0, 153);">\s</font>**<font style="color:rgb(170, 17, 17);">+</font>**<font style="color:rgb(0, 0, 153);">\w</font>**<font style="color:rgb(170, 17, 17);">+</font>**<font style="color:rgb(0, 0, 153);">\s</font>**<font style="color:rgb(170, 17, 17);">*</font>**<font style="color:rgb(0, 0, 153);">(</font>**<font style="color:rgb(170, 17, 17);">|const</font>**<font style="color:rgb(0, 0, 153);">\s</font>**<font style="color:rgb(170, 17, 17);">+</font>**<font style="color:rgb(0, 0, 153);">\w</font>**<font style="color:rgb(170, 17, 17);">+</font>**<font style="color:rgb(0, 0, 153);">\s</font>**<font style="color:rgb(170, 17, 17);">*=)'</font><font style="color:gray;">,</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 85, 170);">code</font><font style="color:olive;">)</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:green;">or</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 85, 170);">re</font><font style="color:rgb(51, 51, 51);">.</font><font style="color:rgb(0, 85, 170);">search</font><font style="color:olive;">(</font><font style="color:rgb(51, 51, 51);">r</font><font style="color:rgb(170, 17, 17);">'=>|console</font>**<font style="color:rgb(0, 0, 153);">.</font>**<font style="color:rgb(170, 17, 17);">(log|error)'</font><font style="color:gray;">,</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 85, 170);">code</font><font style="color:olive;">)</font><font style="color:rgb(51, 51, 51);">:\
</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:green;">return</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(170, 17, 17);">'javascript'</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(170, 85, 0);"># 检测 Bash</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:green;">if</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 85, 170);">re</font><font style="color:rgb(51, 51, 51);">.</font><font style="color:rgb(0, 85, 170);">search</font><font style="color:olive;">(</font><font style="color:rgb(51, 51, 51);">r</font><font style="color:rgb(170, 17, 17);">'^#!.\*</font>**<font style="color:rgb(0, 0, 153);">\b</font>**<font style="color:rgb(170, 17, 17);">(bash|sh)</font>**<font style="color:rgb(0, 0, 153);">\b</font>**<font style="color:rgb(170, 17, 17);">'</font><font style="color:gray;">,</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 85, 170);">code</font><font style="color:gray;">,</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 85, 170);">re</font><font style="color:rgb(51, 51, 51);">.</font><font style="color:rgb(0, 85, 170);">M</font><font style="color:olive;">)</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:green;">or</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 85, 170);">re</font><font style="color:rgb(51, 51, 51);">.</font><font style="color:rgb(0, 85, 170);">search</font><font style="color:olive;">(</font><font style="color:rgb(51, 51, 51);">r</font><font style="color:rgb(170, 17, 17);">'</font>**<font style="color:rgb(0, 0, 153);">\b</font>**<font style="color:rgb(170, 17, 17);">(if|then|fi|for|in|do|done)</font>**<font style="color:rgb(0, 0, 153);">\b</font>**<font style="color:rgb(170, 17, 17);">'</font><font style="color:gray;">,</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 85, 170);">code</font><font style="color:olive;">)</font><font style="color:rgb(51, 51, 51);">:\
</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:green;">return</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(170, 17, 17);">'bash'</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(170, 85, 0);"># 默认文本格式</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:green;">return</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(170, 17, 17);">'text'</font><font style="color:rgb(51, 51, 51);">

</font>**<font style="color:green;">def</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">format_markdown</font><font style="color:olive;">(</font><font style="color:rgb(51, 51, 51);">content</font><font style="color:olive;">)</font><font style="color:rgb(51, 51, 51);">:\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(170, 17, 17);">"""格式化 Markdown 内容"""</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(170, 85, 0);"># 为无标签代码块补全语言</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);">fence_pattern</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:gray;">=</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">r</font><font style="color:rgb(170, 17, 17);">'(?ms)^(\[</font><font style="color:rgb(170, 17, 17);"> </font>**<font style="color:rgb(0, 0, 153);">\t</font>**<font style="color:rgb(170, 17, 17);">]{0,3})<code>([^</font>**<font style="color:rgb(0, 0, 153);">\n</font>**<font style="color:rgb(170, 17, 17);">]*)</font>**<font style="color:rgb(0, 0, 153);">\n</font>**<font style="color:rgb(170, 17, 17);">(.*?)(</font>**<font style="color:rgb(0, 0, 153);">\n</font>****<font style="color:rgb(0, 0, 153);">\1</font>**<font style="color:rgb(170, 17, 17);"></code>)</font>**<font style="color:rgb(0, 0, 153);">\s</font>**<font style="color:rgb(170, 17, 17);">*$'</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:green;">def</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">add_lang</font><font style="color:olive;">(</font><font style="color:rgb(51, 51, 51);">match</font><font style="color:olive;">)</font><font style="color:rgb(51, 51, 51);">:\
</font><font style="color:rgb(51, 51, 51);">indent</font><font style="color:gray;">,</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">info</font><font style="color:gray;">,</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">body</font><font style="color:gray;">,</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">closing</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:gray;">=</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">match.</font><font style="color:rgb(0, 85, 170);">groups</font><font style="color:olive;">(</font><font style="color:olive;">)</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:green;">if</font>**<font style="color:rgb(51, 51, 51);"> </font>**<font style="color:green;">not</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">info.</font><font style="color:rgb(0, 85, 170);">strip</font><font style="color:olive;">(</font><font style="color:olive;">)</font><font style="color:rgb(51, 51, 51);">:\
</font><font style="color:rgb(51, 51, 51);">lang</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:gray;">=</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">detect_language</font><font style="color:olive;">(</font><font style="color:rgb(51, 51, 51);">body</font><font style="color:olive;">)</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:green;">return</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">f</font><font style="color:rgb(170, 17, 17);">"{indent}\`\`\`{lang}</font>**<font style="color:rgb(0, 0, 153);">\n</font>**<font style="color:rgb(170, 17, 17);">{body}{closing}</font>**<font style="color:rgb(0, 0, 153);">\n</font>**<font style="color:rgb(170, 17, 17);">"</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:green;">return</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">match.</font><font style="color:rgb(0, 85, 170);">group</font><font style="color:olive;">(</font><font style="color:maroon;">0</font><font style="color:olive;">)</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);">content</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:gray;">=</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 85, 170);">re</font><font style="color:rgb(51, 51, 51);">.</font><font style="color:rgb(0, 85, 170);">sub</font><font style="color:olive;">(</font><font style="color:rgb(51, 51, 51);">fence_pattern</font><font style="color:gray;">,</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">add_lang</font><font style="color:gray;">,</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">content</font><font style="color:olive;">)</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(170, 85, 0);"># 清理多余空行（仅清理代码块外的内容）</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);">content</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:gray;">=</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 85, 170);">re</font><font style="color:rgb(51, 51, 51);">.</font><font style="color:rgb(0, 85, 170);">sub</font><font style="color:olive;">(</font><font style="color:rgb(51, 51, 51);">r</font><font style="color:rgb(170, 17, 17);">'</font>**<font style="color:rgb(0, 0, 153);">\n</font>**<font style="color:rgb(170, 17, 17);">{3,}'</font><font style="color:gray;">,</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(170, 17, 17);">'</font>\*\*<font style="color:rgb(0, 0, 153);">\n</font>*\***<font style="color:rgb(0, 0, 153);">\n</font>**<font style="color:rgb(170, 17, 17);">'</font><font style="color:gray;">,</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">content</font><font style="color:olive;">)</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:green;">return</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">content.</font><font style="color:rgb(0, 85, 170);">rstrip</font><font style="color:olive;">(</font><font style="color:olive;">)</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">+</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(170, 17, 17);">'</font>**<font style="color:rgb(0, 0, 153);">\n</font>**<font style="color:rgb(170, 17, 17);">'</font><font style="color:rgb(51, 51, 51);">

</font>**<font style="color:green;">if</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">**name**</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:gray;">==</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(170, 17, 17);">"**main**"</font><font style="color:rgb(51, 51, 51);">:\
</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:green;">try</font>**<font style="color:rgb(51, 51, 51);">:\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(170, 85, 0);"># 读取 Claude 传递的 JSON 数据</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);">input_data</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:gray;">=</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">json.</font><font style="color:rgb(0, 85, 170);">load</font><font style="color:olive;">(</font><font style="color:rgb(0, 85, 170);">sys</font><font style="color:rgb(51, 51, 51);">.</font><font style="color:rgb(0, 85, 170);">stdin</font><font style="color:olive;">)</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);">file_path</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:gray;">=</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">input_data.</font><font style="color:rgb(0, 85, 170);">get</font><font style="color:olive;">(</font><font style="color:rgb(170, 17, 17);">'tool_input'</font><font style="color:gray;">,</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:olive;">{</font><font style="color:olive;">}</font><font style="color:olive;">)</font><font style="color:rgb(51, 51, 51);">.</font><font style="color:rgb(0, 85, 170);">get</font><font style="color:olive;">(</font><font style="color:rgb(170, 17, 17);">'file_path'</font><font style="color:gray;">,</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(170, 17, 17);">''</font><font style="color:olive;">)</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(170, 85, 0);"># 仅处理 .md/.mdx 文件</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:green;">if</font>**<font style="color:rgb(51, 51, 51);"> </font>**<font style="color:green;">not</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">file_path.</font><font style="color:rgb(0, 85, 170);">endswith</font><font style="color:olive;">(</font><font style="color:olive;">(</font><font style="color:rgb(170, 17, 17);">'.md'</font><font style="color:gray;">,</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(170, 17, 17);">'.mdx'</font><font style="color:olive;">)</font><font style="color:olive;">)</font><font style="color:rgb(51, 51, 51);">:\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 85, 170);">sys</font><font style="color:rgb(51, 51, 51);">.</font><font style="color:rgb(0, 85, 170);">exit</font><font style="color:olive;">(</font><font style="color:maroon;">0</font><font style="color:olive;">)</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(170, 85, 0);"># 读取并格式化文件</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:green;">if</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 85, 170);">os</font><font style="color:rgb(51, 51, 51);">.</font><font style="color:rgb(0, 85, 170);">path</font><font style="color:rgb(51, 51, 51);">.</font><font style="color:rgb(0, 85, 170);">exists</font><font style="color:olive;">(</font><font style="color:rgb(51, 51, 51);">file_path</font><font style="color:olive;">)</font><font style="color:rgb(51, 51, 51);">:\
</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:green;">with</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:teal;">open</font><font style="color:olive;">(</font><font style="color:rgb(51, 51, 51);">file_path</font><font style="color:gray;">,</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(170, 17, 17);">'r'</font><font style="color:gray;">,</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">encoding</font><font style="color:gray;">=</font><font style="color:rgb(170, 17, 17);">'utf-8'</font><font style="color:olive;">)</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:green;">as</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">f:\
</font><font style="color:rgb(51, 51, 51);">content</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:gray;">=</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">f.</font><font style="color:rgb(0, 85, 170);">read</font><font style="color:olive;">(</font><font style="color:olive;">)</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);">formatted_content</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:gray;">=</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">format_markdown</font><font style="color:olive;">(</font><font style="color:rgb(51, 51, 51);">content</font><font style="color:olive;">)</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(170, 85, 0);"># 仅在内容变化时写入</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:green;">if</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">formatted_content</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:gray;">!=</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">content:\
</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:green;">with</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:teal;">open</font><font style="color:olive;">(</font><font style="color:rgb(51, 51, 51);">file_path</font><font style="color:gray;">,</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(170, 17, 17);">'w'</font><font style="color:gray;">,</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">encoding</font><font style="color:gray;">=</font><font style="color:rgb(170, 17, 17);">'utf-8'</font><font style="color:olive;">)</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:green;">as</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">f:\
</font><font style="color:rgb(51, 51, 51);">f.</font><font style="color:rgb(0, 85, 170);">write</font><font style="color:olive;">(</font><font style="color:rgb(51, 51, 51);">formatted_content</font><font style="color:olive;">)</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:green;">print</font>**<font style="color:olive;">(</font><font style="color:rgb(51, 51, 51);">f</font><font style="color:rgb(170, 17, 17);">"已格式化 Markdown 文件：{file_path}"</font><font style="color:olive;">)</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:green;">except</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:teal;">Exception</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:green;">as</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">e:\
</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:green;">print</font>**<font style="color:olive;">(</font><font style="color:rgb(51, 51, 51);">f</font><font style="color:rgb(170, 17, 17);">"格式化失败：{e}"</font><font style="color:gray;">,</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:teal;">file</font><font style="color:gray;">=</font><font style="color:rgb(0, 85, 170);">sys</font><font style="color:rgb(51, 51, 51);">.</font><font style="color:rgb(0, 85, 170);">stderr</font><font style="color:olive;">)</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 85, 170);">sys</font><font style="color:rgb(51, 51, 51);">.</font><font style="color:rgb(0, 85, 170);">exit</font><font style="color:olive;">(</font><font style="color:maroon;">1</font><font style="color:olive;">)</font>

#### <font style="color:rgb(51, 51, 51);">第三步：赋予脚本执行权限</font>

chmod +x .claude/hooks/markdown_formatter.py

### <font style="color:rgb(51, 51, 51);">示例 3：Claude 等待输入时发送桌面通知</font>

<font style="color:rgb(51, 51, 51);">功能：当 Claude 需要用户输入时，自动弹出桌面提醒（适用于 Linux/macOS）</font>

```plain
{
  "hooks": {
    "Notification": [
      {
        "matcher": "", // 匹配所有通知事件
        "hooks": [
          {
            "type": "command",
            "command": "notify-send 'Claude Code 提示' '请你输入指令或确认权限'"
          }
        ]
      }
    ]
  }
}
```

### <font style="color:rgb(51, 51, 51);">示例 4：禁止修改敏感文件</font>

<font style="color:rgb(51, 51, 51);">功能：阻止 Claude 编辑</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">.env</font></code><font style="color:rgb(51, 51, 51);">、</font><code><font style="color:rgb(51, 51, 51);">package-lock.json</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">等敏感文件</font>

```plain
{
  "hooks": {
    "PreToolUse": [
      {
        "matcher": "Edit|Write",
        "hooks": [
          {
            "type": "command",
            "command": "python3 -c \"import json, sys; data=json.load(sys.stdin); path=data.get('tool_input',{}).get('file_path',''); sys.exit(2 if any(p in path for p in ['.env', 'package-lock.json', '.git/']) else 0)\""
          }
        ]
      }
    ]
  }
}
```

<font style="color:rgb(51, 51, 51);">说明：脚本返回状态码</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">2</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">时，Claude Code 会拦截此次工具调用，从而阻止文件修改。</font>

***

## <font style="color:rgb(51, 51, 51);">Claude Code 钩子参考手册</font>

### <font style="color:rgb(51, 51, 51);">配置文件路径</font>

| <font style="color:rgb(255, 255, 255);">配置级别</font> | <font style="color:rgb(255, 255, 255);">文件路径</font> | <font style="color:rgb(255, 255, 255);">生效范围</font> |
| --- | --- | --- |
| <font style="color:rgb(51, 51, 51);">用户级</font> | <code><font style="color:rgb(51, 51, 51);">~/.claude/settings.json</font></code> | <font style="color:rgb(51, 51, 51);">所有项目</font> |
| <font style="color:rgb(51, 51, 51);">项目级</font> | <code><font style="color:rgb(51, 51, 51);">.claude/settings.json</font></code> | <font style="color:rgb(51, 51, 51);">当前项目</font> |
| <font style="color:rgb(51, 51, 51);">本地项目级（不提交）</font> | <code><font style="color:rgb(51, 51, 51);">.claude/settings.local.json</font></code> | <font style="color:rgb(51, 51, 51);">当前项目，不纳入版本控制</font> |
| <font style="color:rgb(51, 51, 51);">托管策略级</font> | <font style="color:rgb(51, 51, 51);">管理员指定路径</font> | <font style="color:rgb(51, 51, 51);">企业/团队统一管控</font> |

### <font style="color:rgb(51, 51, 51);">核心配置结构</font>

<font style="color:rgb(51, 51, 51);">Hooks 按</font>**<font style="color:rgb(51, 51, 51);">事件+匹配器</font>**<font style="color:rgb(51, 51, 51);">组织，支持</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">command</font></code><font style="color:rgb(51, 51, 51);">（执行 Shell 命令）和</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">prompt</font></code><font style="color:rgb(51, 51, 51);">（调用 LLM 决策）两种类型。</font>

```plain
{
  "hooks": {
    "【钩子事件名】": [
      {
        "matcher": "【工具匹配规则】", // 部分事件可省略
        "hooks": [
          {
            "type": "command/prompt",
            "command": "【Shell 命令】", // type=command 时必填
            "prompt": "【LLM 提示词】",  // type=prompt 时必填
            "timeout": 30 // 可选，超时时间（秒）
          }
        ]
      }
    ]
  }
}
```

### <font style="color:rgb(51, 51, 51);">匹配器规则（仅适用于工具类事件）</font>

| <font style="color:rgb(255, 255, 255);">匹配规则</font> | <font style="color:rgb(255, 255, 255);">示例</font> | <font style="color:rgb(255, 255, 255);">说明</font> |
| --- | --- | --- |
| <font style="color:rgb(51, 51, 51);">精确匹配</font> | <code><font style="color:rgb(51, 51, 51);">Write</font></code> | <font style="color:rgb(51, 51, 51);">仅匹配</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">Write</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">工具</font> |
| <font style="color:rgb(51, 51, 51);">多工具匹配</font> | <font style="color:rgb(51, 51, 51);">Edit | Write</font> | <font style="color:rgb(51, 51, 51);">匹配</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">Edit</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">或</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">Write</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">工具</font> |
| <font style="color:rgb(51, 51, 51);">前缀匹配</font> | <code><font style="color:rgb(51, 51, 51);">Notebook.*</font></code> | <font style="color:rgb(51, 51, 51);">匹配所有以</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">Notebook</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">开头的工具</font> |
| <font style="color:rgb(51, 51, 51);">全匹配</font> | <code><font style="color:rgb(51, 51, 51);">*</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">/ 空字符串</font> | <font style="color:rgb(51, 51, 51);">匹配所有工具</font> |

### <font style="color:rgb(51, 51, 51);">特殊配置技巧</font>

| <font style="color:rgb(255, 255, 255);">场景</font> | <font style="color:rgb(255, 255, 255);">配置方法</font> | <font style="color:rgb(255, 255, 255);">示例</font> |
| --- | --- | --- |
| <font style="color:rgb(51, 51, 51);">引用项目内脚本</font> | <font style="color:rgb(51, 51, 51);">使用环境变量</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">$CLAUDE_PROJECT_DIR</font></code> | <code><font style="color:rgb(51, 51, 51);">"command": "\"$CLAUDE_PROJECT_DIR\"/.claude/hooks/check-style.sh"</font></code> |
| <font style="color:rgb(51, 51, 51);">插件 Hooks</font> | <font style="color:rgb(51, 51, 51);">插件内配置</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">hooks/hooks.json</font></code><br/><font style="color:rgb(51, 51, 51);">，用</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">${CLAUDE_PLUGIN_ROOT}</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">引用插件文件</font> | <code><font style="color:rgb(51, 51, 51);">"command": "${CLAUDE_PLUGIN_ROOT}/scripts/format.sh"</font></code> |
| <font style="color:rgb(51, 51, 51);">组件级 Hooks（Skill/Agent）</font> | <font style="color:rgb(51, 51, 51);">在组件 frontmatter 中定义，作用域仅限组件生命周期</font> | <font style="color:rgb(51, 51, 51);">见下方</font>**<font style="color:rgb(51, 51, 51);">扩展配置</font>**<font style="color:rgb(51, 51, 51);">表格</font> |

### <font style="color:rgb(51, 51, 51);">扩展配置（Skill/Agent/斜杠命令）</font>

<font style="color:rgb(51, 51, 51);">扩展配置允许直接在 Skill、Agent 或自定义斜杠命令的定义中内嵌 Hooks 配置，这类 Hooks 仅在对应组件被激活并运行时生效，组件执行完成后会自动清理，不会影响全局会话。</font>

#### <font style="color:rgb(51, 51, 51);">支持的钩子事件</font>

<font style="color:rgb(51, 51, 51);">仅支持</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">PreToolUse</font></code><font style="color:rgb(51, 51, 51);">、</font><code><font style="color:rgb(51, 51, 51);">PostToolUse</font></code><font style="color:rgb(51, 51, 51);">、</font><code><font style="color:rgb(51, 51, 51);">Stop</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">三类事件，与全局 Hooks 功能一致，但作用域仅限当前 Skill/斜杠命令的生命周期。</font>

#### <font style="color:rgb(51, 51, 51);">特有配置项</font>

* <code><font style="color:rgb(51, 51, 51);">once: true</font></code><font style="color:rgb(51, 51, 51);">（可选）：设置为</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">true</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">时，该 Hooks 在整个会话中仅运行一次，首次成功执行后会自动移除，避免重复触发。</font>

#### <font style="color:rgb(51, 51, 51);">完整配置示例</font>

```plain
---
# Skill/斜杠命令的基础信息
name: secure-operations
description: 执行Shell命令前先做安全校验的工具
# Hooks 配置段
hooks:
  PreToolUse:
    # 匹配器：仅拦截Bash工具调用
    - matcher: "Bash"
      hooks:
        - type: "command"
          # 要执行的安全校验脚本
          command: "./scripts/security-check.sh"
          # 会话内仅执行一次
          once: true
          # 超时时间（秒），避免脚本卡死
          timeout: 15
---
```

### <font style="color:rgb(51, 51, 51);">Agent 中的 Hooks 配置</font>

#### <font style="color:rgb(51, 51, 51);">支持的钩子事件</font>

<font style="color:rgb(51, 51, 51);">同样仅支持</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">PreToolUse</font></code><font style="color:rgb(51, 51, 51);">、</font><code><font style="color:rgb(51, 51, 51);">PostToolUse</font></code><font style="color:rgb(51, 51, 51);">、</font><code><font style="color:rgb(51, 51, 51);">Stop</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">三类事件，作用域仅限该子 Agent 的任务执行周期。</font>

#### <font style="color:rgb(51, 51, 51);">特有配置项</font>

<font style="color:rgb(51, 51, 51);">无额外专属配置项，不支持</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">once: true</font></code><font style="color:rgb(51, 51, 51);">（Agent 每次执行任务时，Hooks 都会触发）。</font>

#### <font style="color:rgb(51, 51, 51);">完整配置示例</font>

```plain
---
# Agent 的基础信息
name: code-reviewer
description: 自动审查代码修改并运行代码检查的子代理
# Hooks 配置段
hooks:
  PostToolUse:
    # 匹配器：拦截Edit（编辑）或Write（写入）工具
    - matcher: "Edit|Write"
      hooks:
        - type: "command"
          # 代码检查脚本，执行lint校验
          command: "./scripts/run-linter.sh"
          # 超时时间（秒）
          timeout: 30
---
```

**<font style="color:rgb(51, 51, 51);">注意事项：</font>**

1. <font style="color:rgb(51, 51, 51);">组件内 Hooks 的匹配器规则与全局 Hooks 完全一致：支持精确匹配（如</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">"Write"</font></code><font style="color:rgb(51, 51, 51);">）、多工具匹配（如</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">"Edit|Write"</font></code><font style="color:rgb(51, 51, 51);">）、通配匹配（</font><code><font style="color:rgb(51, 51, 51);">"*"</font></code><font style="color:rgb(51, 51, 51);">），且区分大小写；</font>
2. <font style="color:rgb(51, 51, 51);">组件内 Hooks 与全局 Hooks 会并行执行：若全局和组件内同时配置了针对同一事件的 Hooks，触发时两类 Hooks 会一起运行，互不冲突；</font>
3. <font style="color:rgb(51, 51, 51);">配置格式要求：组件内 Hooks 需写在 frontmatter（</font><code><font style="color:rgb(51, 51, 51);">---</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">包裹的区域）中，遵循 YAML 语法，缩进错误会导致配置失效；</font>
4. <font style="color:rgb(51, 51, 51);">脚本路径建议：优先使用相对路径（如</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">./scripts/xxx.sh</font></code><font style="color:rgb(51, 51, 51);">），或借助</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">$CLAUDE_PROJECT_DIR</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">环境变量指定绝对路径，确保组件在任意目录下都能找到脚本。</font>

### <font style="color:rgb(51, 51, 51);">钩子事件--工具类事件（支持匹配器）</font>

| <font style="color:rgb(255, 255, 255);">事件名</font> | <font style="color:rgb(255, 255, 255);">触发时机</font> | <font style="color:rgb(255, 255, 255);">常见匹配器</font> | <font style="color:rgb(255, 255, 255);">核心作用</font> |
| --- | --- | --- | --- |
| <code><font style="color:rgb(51, 51, 51);">PreToolUse</font></code> | <font style="color:rgb(51, 51, 51);">工具调用</font>**<font style="color:rgb(51, 51, 51);">前</font>** | <code><font style="color:rgb(51, 51, 51);">Bash</font></code><br/><font style="color:rgb(51, 51, 51);">/</font><code><font style="color:rgb(51, 51, 51);">Edit</font></code><br/><font style="color:rgb(51, 51, 51);">/</font><code><font style="color:rgb(51, 51, 51);">Write</font></code><br/><font style="color:rgb(51, 51, 51);">/</font><code><font style="color:rgb(51, 51, 51);">Read</font></code> | <font style="color:rgb(51, 51, 51);">拦截工具执行、修改入参、自动批准/拒绝权限</font> |
| <code><font style="color:rgb(51, 51, 51);">PermissionRequest</font></code> | <font style="color:rgb(51, 51, 51);">弹出权限请求对话框时</font> | <font style="color:rgb(51, 51, 51);">同</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">PreToolUse</font></code> | <font style="color:rgb(51, 51, 51);">自动处理权限申请，无需用户手动确认</font> |
| <code><font style="color:rgb(51, 51, 51);">PostToolUse</font></code> | <font style="color:rgb(51, 51, 51);">工具调用</font>**<font style="color:rgb(51, 51, 51);">成功后</font>** | <font style="color:rgb(51, 51, 51);">同</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">PreToolUse</font></code> | <font style="color:rgb(51, 51, 51);">执行后置操作（如代码格式化、日志记录）</font> |
| <code><font style="color:rgb(51, 51, 51);">Notification</font></code> | <font style="color:rgb(51, 51, 51);">Claude 发送通知时</font> | <code><font style="color:rgb(51, 51, 51);">permission_prompt</font></code><br/><font style="color:rgb(51, 51, 51);">/</font><code><font style="color:rgb(51, 51, 51);">idle_prompt</font></code><br/><font style="color:rgb(51, 51, 51);">/</font><code><font style="color:rgb(51, 51, 51);">auth_success</font></code> | <font style="color:rgb(51, 51, 51);">自定义通知方式（如桌面弹窗、邮件提醒）</font> |
| <code><font style="color:rgb(51, 51, 51);">PreCompact</font></code> | <font style="color:rgb(51, 51, 51);">执行上下文压缩操作前</font> | <code><font style="color:rgb(51, 51, 51);">manual</font></code><br/><font style="color:rgb(51, 51, 51);">（手动触发）/</font><code><font style="color:rgb(51, 51, 51);">auto</font></code><br/><font style="color:rgb(51, 51, 51);">（自动触发）</font> | <font style="color:rgb(51, 51, 51);">自定义压缩规则、备份重要上下文</font> |

### <font style="color:rgb(51, 51, 51);">钩子事件--会话/任务类事件（无匹配器）</font>

| <font style="color:rgb(255, 255, 255);">事件名</font> | <font style="color:rgb(255, 255, 255);">触发时机</font> | <font style="color:rgb(255, 255, 255);">核心作用</font> |
| --- | --- | --- |
| <code><font style="color:rgb(51, 51, 51);">UserPromptSubmit</font></code> | <font style="color:rgb(51, 51, 51);">用户提交提示后、Claude 处理前</font> | <font style="color:rgb(51, 51, 51);">验证提示合法性、补充上下文信息</font> |
| <code><font style="color:rgb(51, 51, 51);">Stop</font></code> | <font style="color:rgb(51, 51, 51);">主 Agent 完成响应时（用户中断不触发）</font> | <font style="color:rgb(51, 51, 51);">智能判断是否需要继续执行任务</font> |
| <code><font style="color:rgb(51, 51, 51);">SubagentStop</font></code> | <font style="color:rgb(51, 51, 51);">子 Agent 任务完成时</font> | <font style="color:rgb(51, 51, 51);">评估子任务结果，决定是否终止</font> |
| <code><font style="color:rgb(51, 51, 51);">SessionStart</font></code> | <font style="color:rgb(51, 51, 51);">启动/恢复会话时</font> | <font style="color:rgb(51, 51, 51);">初始化环境、加载项目配置、设置持久化环境变量</font> |
| <code><font style="color:rgb(51, 51, 51);">SessionEnd</font></code> | <font style="color:rgb(51, 51, 51);">会话结束时</font> | <font style="color:rgb(51, 51, 51);">清理临时文件、记录会话日志、保存工作状态</font> |

## <font style="color:rgb(51, 51, 51);">钩子类型对比</font>

<font style="color:rgb(51, 51, 51);">Claude Code 支持两种钩子类型，满足不同场景需求。</font>

| <font style="color:rgb(51, 51, 51);">特性</font> | <code><font style="color:rgb(51, 51, 51);">command</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">类型（命令钩子）</font> | <code><font style="color:rgb(51, 51, 51);">prompt</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">类型（提示词钩子）</font> |
| --- | --- | --- |
| <font style="color:rgb(51, 51, 51);">执行方式</font> | <font style="color:rgb(51, 51, 51);">运行 Shell 命令/脚本</font> | <font style="color:rgb(51, 51, 51);">调用 LLM（默认 Haiku 模型）做智能决策</font> |
| <font style="color:rgb(51, 51, 51);">决策逻辑</font> | <font style="color:rgb(51, 51, 51);">基于代码逻辑的</font>**<font style="color:rgb(51, 51, 51);">确定性判断</font>** | <font style="color:rgb(51, 51, 51);">基于上下文的</font>**<font style="color:rgb(51, 51, 51);">灵活语义判断</font>** |
| <font style="color:rgb(51, 51, 51);">配置难度</font> | <font style="color:rgb(51, 51, 51);">需要编写脚本，门槛较高</font> | <font style="color:rgb(51, 51, 51);">只需写提示词，简单易上手</font> |
| <font style="color:rgb(51, 51, 51);">响应速度</font> | <font style="color:rgb(51, 51, 51);">快（本地执行）</font> | <font style="color:rgb(51, 51, 51);">较慢（需 API 调用）</font> |
| <font style="color:rgb(51, 51, 51);">适用场景</font> | <font style="color:rgb(51, 51, 51);">代码格式化、日志记录、权限拦截等固定规则</font> | <font style="color:rgb(51, 51, 51);">任务完成度评估、复杂意图判断等灵活场景</font> |
| <font style="color:rgb(51, 51, 51);">核心配置</font> | <code><font style="color:rgb(51, 51, 51);">command</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">+</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">timeout</font></code> | <code><font style="color:rgb(51, 51, 51);">prompt</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">+</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">timeout</font></code><br/><font style="color:rgb(51, 51, 51);">（可引用</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">$ARGUMENTS</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">占位符）</font> |

### <font style="color:rgb(51, 51, 51);">输入与输出 -- 钩子输入（stdin 传入 JSON）</font>

<font style="color:rgb(51, 51, 51);">所有钩子都会收到通用字段，部分事件附带特定字段。</font>

| <font style="color:rgb(255, 255, 255);">字段类型</font> | <font style="color:rgb(255, 255, 255);">通用字段</font> | <font style="color:rgb(255, 255, 255);">说明</font> |
| --- | --- | --- |
| <font style="color:rgb(51, 51, 51);">基础信息</font> | <code><font style="color:rgb(51, 51, 51);">session_id</font></code> | <font style="color:rgb(51, 51, 51);">会话唯一标识</font> |
|  | <code><font style="color:rgb(51, 51, 51);">transcript_path</font></code> | <font style="color:rgb(51, 51, 51);">对话记录文件路径</font> |
|  | <code><font style="color:rgb(51, 51, 51);">cwd</font></code> | <font style="color:rgb(51, 51, 51);">钩子执行时的当前工作目录</font> |
|  | <code><font style="color:rgb(51, 51, 51);">permission_mode</font></code> | <font style="color:rgb(51, 51, 51);">当前权限模式（default/plan/acceptEdits 等）</font> |
|  | <code><font style="color:rgb(51, 51, 51);">hook_event_name</font></code> | <font style="color:rgb(51, 51, 51);">当前触发的钩子事件名</font> |

**<font style="color:rgb(51, 51, 51);">各事件特有字段示例</font>**

| <font style="color:rgb(255, 255, 255);">事件名</font> | <font style="color:rgb(255, 255, 255);">特有字段</font> | <font style="color:rgb(255, 255, 255);">示例</font> |
| --- | --- | --- |
| <code><font style="color:rgb(51, 51, 51);">PreToolUse</font></code> | <code><font style="color:rgb(51, 51, 51);">tool_name</font></code><br/><font style="color:rgb(51, 51, 51);">/</font><code><font style="color:rgb(51, 51, 51);">tool_input</font></code> | <code><font style="color:rgb(51, 51, 51);">{"tool_name":"Write","tool_input":{"file_path":"/test.txt"}}</font></code> |
| <code><font style="color:rgb(51, 51, 51);">UserPromptSubmit</font></code> | <code><font style="color:rgb(51, 51, 51);">prompt</font></code> | <code><font style="color:rgb(51, 51, 51);">{"prompt":"帮我写一个排序函数"}</font></code> |
| <code><font style="color:rgb(51, 51, 51);">SessionEnd</font></code> | <code><font style="color:rgb(51, 51, 51);">reason</font></code> | <code><font style="color:rgb(51, 51, 51);">{"reason":"clear/logout/other"}</font></code> |

### <font style="color:rgb(51, 51, 51);">钩子输出（两种方式）</font>

#### <font style="color:rgb(51, 51, 51);">方式1：退出代码（简单场景）</font>

<font style="color:rgb(51, 51, 51);">通过退出代码传递执行状态，</font><code><font style="color:rgb(51, 51, 51);">stdout</font></code><font style="color:rgb(51, 51, 51);">/</font><code><font style="color:rgb(51, 51, 51);">stderr</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">用于反馈信息。</font>

| <font style="color:rgb(255, 255, 255);">退出代码</font> | <font style="color:rgb(255, 255, 255);">含义</font> | <font style="color:rgb(255, 255, 255);">行为说明</font> |
| --- | --- | --- |
| <code><font style="color:rgb(51, 51, 51);">0</font></code> | <font style="color:rgb(51, 51, 51);">执行成功</font> | <code><font style="color:rgb(51, 51, 51);">stdout</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">可返回 JSON 做高级控制；部分事件（如</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">UserPromptSubmit</font></code><br/><font style="color:rgb(51, 51, 51);">）会将</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">stdout</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">加入上下文</font> |
| <code><font style="color:rgb(51, 51, 51);">2</font></code> | <font style="color:rgb(51, 51, 51);">阻止操作</font> | <font style="color:rgb(51, 51, 51);">仅使用</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">stderr</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">作为错误消息反馈给 Claude，</font>**<font style="color:rgb(51, 51, 51);">阻止当前事件继续执行</font>** |
| <font style="color:rgb(51, 51, 51);">其他非零值</font> | <font style="color:rgb(51, 51, 51);">非阻塞错误</font> | <code><font style="color:rgb(51, 51, 51);">stderr</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">仅在详细模式（</font><code><font style="color:rgb(51, 51, 51);">ctrl+o</font></code><br/><font style="color:rgb(51, 51, 51);">）显示，不影响事件执行</font> |

**<font style="color:rgb(51, 51, 51);">退出代码 2 在各事件中的行为</font>**

| <font style="color:rgb(255, 255, 255);">事件名</font> | <font style="color:rgb(255, 255, 255);">触发行为</font> |
| --- | --- |
| <code><font style="color:rgb(51, 51, 51);">PreToolUse</font></code> | <font style="color:rgb(51, 51, 51);">阻止工具调用，向 Claude 展示</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">stderr</font></code> |
| <code><font style="color:rgb(51, 51, 51);">UserPromptSubmit</font></code> | <font style="color:rgb(51, 51, 51);">阻止提示处理，擦除用户输入</font> |
| <code><font style="color:rgb(51, 51, 51);">Stop</font></code> | <font style="color:rgb(51, 51, 51);">阻止 Claude 停止，强制继续工作</font> |
| <code><font style="color:rgb(51, 51, 51);">PostToolUse</font></code><br/><font style="color:rgb(51, 51, 51);">/</font><code><font style="color:rgb(51, 51, 51);">Notification</font></code> | <font style="color:rgb(51, 51, 51);">仅展示</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">stderr</font></code><br/><font style="color:rgb(51, 51, 51);">，不影响已完成操作</font> |

#### <font style="color:rgb(51, 51, 51);">方式2：JSON 输出（高级场景）</font>

<font style="color:rgb(51, 51, 51);">退出代码为</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">0</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">时，可通过</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">stdout</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">返回 JSON 实现精细化控制，核心字段如下：</font>

| <font style="color:rgb(255, 255, 255);">通用 JSON 字段</font> | <font style="color:rgb(255, 255, 255);">作用</font> |
| --- | --- |
| <code><font style="color:rgb(51, 51, 51);">continue: true/false</font></code> | <font style="color:rgb(51, 51, 51);">是否允许事件继续执行（</font><code><font style="color:rgb(51, 51, 51);">false</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">优先于其他规则）</font> |
| <code><font style="color:rgb(51, 51, 51);">stopReason</font></code> | <code><font style="color:rgb(51, 51, 51);">continue=false</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">时，展示给用户的原因</font> |
| <code><font style="color:rgb(51, 51, 51);">systemMessage</font></code> | <font style="color:rgb(51, 51, 51);">向用户显示的警告信息</font> |

**<font style="color:rgb(51, 51, 51);">事件特有 JSON 字段示例</font>**

| <font style="color:rgb(255, 255, 255);">事件名</font> | <font style="color:rgb(255, 255, 255);">特有字段</font> | <font style="color:rgb(255, 255, 255);">示例</font> |
| --- | --- | --- |
| <code><font style="color:rgb(51, 51, 51);">PreToolUse</font></code> | <code><font style="color:rgb(51, 51, 51);">permissionDecision</font></code><br/><font style="color:rgb(51, 51, 51);">（allow/deny/ask）</font> | <code><font style="color:rgb(51, 51, 51);">{"hookSpecificOutput":{"permissionDecision":"allow","updatedInput":{"file_path":"/new.txt"}}}</font></code> |
| <code><font style="color:rgb(51, 51, 51);">UserPromptSubmit</font></code> | <code><font style="color:rgb(51, 51, 51);">decision: block/undefined</font></code> | <code><font style="color:rgb(51, 51, 51);">{"decision":"block","reason":"提示包含敏感信息"}</font></code> |
| <code><font style="color:rgb(51, 51, 51);">PostToolUse</font></code> | <code><font style="color:rgb(51, 51, 51);">additionalContext</font></code> | <code><font style="color:rgb(51, 51, 51);">{"hookSpecificOutput":{"additionalContext":"文件已格式化完成"}}</font></code> |

***

## <font style="color:rgb(51, 51, 51);">MCP 工具的 Hooks 配置</font>

<font style="color:rgb(51, 51, 51);">MCP 工具可与 Hooks 无缝集成，通过特定命名规则匹配。</font>

### <font style="color:rgb(51, 51, 51);">MCP 工具命名规则</font>

mcp\_\_<服务器名>\_\_<工具名>

<font style="color:rgb(51, 51, 51);">示例：</font><code><font style="color:rgb(51, 51, 51);">mcp__github__search_repositories</font></code><font style="color:rgb(51, 51, 51);">、</font><code><font style="color:rgb(51, 51, 51);">mcp__filesystem__read_file</font></code>

### <font style="color:rgb(51, 51, 51);">匹配示例</font>

```plain
{
  "hooks": {
    "PreToolUse": [
      {
        "matcher": "mcp__memory__.*", // 匹配 memory 服务器的所有工具
        "hooks": [{"type": "command", "command": "echo '内存操作日志' >> log.txt"}]
      },
      {
        "matcher": "mcp__.*__write.*", // 匹配所有服务器的写操作工具
        "hooks": [{"type": "command", "command": "./validate-write.py"}]
      }
    ]
  }
}
```

***

## <font style="color:rgb(51, 51, 51);">安全与调试</font>

### <font style="color:rgb(51, 51, 51);">安全最佳实践</font>

| <font style="color:rgb(255, 255, 255);">安全要点</font> | <font style="color:rgb(255, 255, 255);">具体操作</font> |
| --- | --- |
| <font style="color:rgb(51, 51, 51);">输入校验</font> | <font style="color:rgb(51, 51, 51);">严格校验</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">tool_input</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">中的文件路径、命令参数，防止路径遍历（如</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">../</font></code><br/><font style="color:rgb(51, 51, 51);">）</font> |
| <font style="color:rgb(51, 51, 51);">变量引用</font> | <font style="color:rgb(51, 51, 51);">Shell 命令中使用</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">"$VAR"</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">而非</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">$VAR</font></code><br/><font style="color:rgb(51, 51, 51);">，避免参数注入</font> |
| <font style="color:rgb(51, 51, 51);">权限最小化</font> | <font style="color:rgb(51, 51, 51);">钩子脚本仅赋予必要权限，避免使用</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">sudo</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">等高危命令</font> |
| <font style="color:rgb(51, 51, 51);">敏感文件排除</font> | <font style="color:rgb(51, 51, 51);">拦截对</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">.env</font></code><br/><font style="color:rgb(51, 51, 51);">、</font><code><font style="color:rgb(51, 51, 51);">.git</font></code><br/><font style="color:rgb(51, 51, 51);">、密钥文件的操作</font> |
| <font style="color:rgb(51, 51, 51);">命令审查</font> | <font style="color:rgb(51, 51, 51);">注册钩子前，手动执行命令验证逻辑，确认无恶意行为</font> |

### <font style="color:rgb(51, 51, 51);">调试技巧</font>

| <font style="color:rgb(255, 255, 255);">问题类型</font> | <font style="color:rgb(255, 255, 255);">排查步骤</font> |
| --- | --- |
| <font style="color:rgb(51, 51, 51);">钩子不生效</font> | <font style="color:rgb(51, 51, 51);">1. 执行</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">/hooks</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">命令检查配置是否注册<br>2. 验证 JSON 语法是否正确<br>3. 检查匹配器规则是否与工具名一致（区分大小写）</font> |
| <font style="color:rgb(51, 51, 51);">命令执行失败</font> | <font style="color:rgb(51, 51, 51);">1. 手动运行钩子命令，确认是否可正常执行<br>2. 检查脚本是否有可执行权限（</font><code><font style="color:rgb(51, 51, 51);">chmod +x script.sh</font></code><br/><font style="color:rgb(51, 51, 51);">）<br>3. 使用绝对路径调用脚本，避免环境变量问题</font> |
| <font style="color:rgb(51, 51, 51);">查看详细日志</font> | <font style="color:rgb(51, 51, 51);">启动 Claude Code 时添加</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">--debug</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">参数，查看钩子执行全过程</font> |

*<font style="color:rgb(44, 58, 94);">参考文档：如需查看钩子的完整功能说明，可查阅官方 </font>*[*<font style="color:rgb(0, 102, 0);">钩子参考文档</font>*](https://code.claude.com/docs/zh-CN/hooks)*<font style="color:rgb(44, 58, 94);">。</font>*

# Claude Code 高阶指令体系：斜杠命令、检查点与插件管理

## <font style="color:rgb(51, 51, 51);">Claude Code 斜杠 / 命令</font>

<font style="color:rgb(51, 51, 51);">斜杠</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:rgb(51, 51, 51);">/</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">命令是 Claude Code 交互式会话的</font>**<font style="color:rgb(51, 51, 51);">快捷控制入口</font>**<font style="color:rgb(51, 51, 51);">，通过输入</font><font style="color:rgb(51, 51, 51);"> </font><code>**<font style="color:rgb(51, 51, 51);">/</font>**</code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">开头的指令，就能快速调用功能、管理会话、自定义工作流。</font>

![1783653949847-60638706-3f68-4ca2-a84b-dc31b45361f3.png](./img/wf9R51v5S5sXlvV1/1783653949847-60638706-3f68-4ca2-a84b-dc31b45361f3-329406.png)

<font style="color:rgb(51, 51, 51);">查看所有可用命令：</font>

/help

<code><font style="color:rgb(51, 51, 51);">/help</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">会列出所有内置命令、当前项目的自定义命令（Skills / Commands），以及已连接 MCP 服务器暴露的命令。</font>

<font style="color:rgb(51, 51, 51);">命令类型：</font>

| <font style="color:rgb(255, 255, 255);">类型</font> | <font style="color:rgb(255, 255, 255);">触发方式</font> | <font style="color:rgb(255, 255, 255);">来源</font> | <font style="color:rgb(255, 255, 255);">存储位置</font> | <font style="color:rgb(255, 255, 255);">适用场景</font> |
| --- | --- | --- | --- | --- |
| **<font style="color:rgb(51, 51, 51);">内置命令</font>** | <code><font style="color:rgb(51, 51, 51);">/command</font></code> | <font style="color:rgb(51, 51, 51);">随 Claude Code 安装</font> | <font style="color:rgb(51, 51, 51);">内部实现</font> | <font style="color:rgb(51, 51, 51);">会话管理、配置、集成等系统操作</font> |
| **<font style="color:rgb(51, 51, 51);">内置 Skills</font>** | <code><font style="color:rgb(51, 51, 51);">/skill-name</font></code> | <font style="color:rgb(51, 51, 51);">随 Claude Code 附带</font> | <font style="color:rgb(51, 51, 51);">内部实现</font> | <font style="color:rgb(51, 51, 51);">代码审查、调试、批处理等预置 AI 工作流</font> |
| **<font style="color:rgb(51, 51, 51);">项目自定义 Skills</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(255, 255, 255);">推荐</font> | <code><font style="color:rgb(51, 51, 51);">/skill-name</font></code> | <font style="color:rgb(51, 51, 51);">用户创建目录 + SKILL.md</font> | <code><font style="color:rgb(51, 51, 51);">.claude/skills/<名称>/SKILL.md</font></code> | <font style="color:rgb(51, 51, 51);">团队共享的可复用工作流，纳入 git；支持 Claude 自动触发</font> |
| **<font style="color:rgb(51, 51, 51);">项目自定义命令</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(255, 255, 255);">旧格式</font> | <code><font style="color:rgb(51, 51, 51);">/command</font></code> | <font style="color:rgb(51, 51, 51);">用户创建</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">.md</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">文件</font> | <code><font style="color:rgb(51, 51, 51);">.claude/commands/</font></code> | <font style="color:rgb(51, 51, 51);">团队共享的重复工作流，纳入 git</font> |
| **<font style="color:rgb(51, 51, 51);">个人自定义 Skills</font>** | <code><font style="color:rgb(51, 51, 51);">/skill-name</font></code> | <font style="color:rgb(51, 51, 51);">用户创建目录 + SKILL.md</font> | <code><font style="color:rgb(51, 51, 51);">~/.claude/skills/<名称>/SKILL.md</font></code> | <font style="color:rgb(51, 51, 51);">跨项目通用的个人工作流</font> |
| **<font style="color:rgb(51, 51, 51);">个人自定义命令</font>** | <code><font style="color:rgb(51, 51, 51);">/command</font></code> | <font style="color:rgb(51, 51, 51);">用户创建</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">.md</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">文件</font> | <code><font style="color:rgb(51, 51, 51);">~/.claude/commands/</font></code> | <font style="color:rgb(51, 51, 51);">跨项目通用的个人工作流（旧格式）</font> |
| **<font style="color:rgb(51, 51, 51);">MCP 命令</font>** | <code><font style="color:rgb(51, 51, 51);">/mcp__服务器__命令</font></code> | <font style="color:rgb(51, 51, 51);">MCP 服务器自动暴露</font> | <font style="color:rgb(51, 51, 51);">由 MCP 服务器提供</font> | <font style="color:rgb(51, 51, 51);">调用 GitHub、Slack、数据库等外部工具</font> |
| <code>**<font style="color:rgb(51, 51, 51);">!</font>**</code><br/>**<font style="color:rgb(51, 51, 51);"> </font>\*\*\*\*<font style="color:rgb(51, 51, 51);">Shell 命令</font>** | <code><font style="color:rgb(51, 51, 51);">!bash命令</font></code> | <font style="color:rgb(51, 51, 51);">直接执行</font> | <font style="color:rgb(51, 51, 51);">—</font> | <font style="color:rgb(51, 51, 51);">绕过 AI 处理，直接运行终端命令</font> |

**<font style="color:rgb(51, 51, 51);">命令优先级（同名时）</font>**<font style="color:rgb(51, 51, 51);">：企业级 > 个人级 > 项目级 > 内置</font>

<font style="color:rgb(51, 51, 51);"> </font>**<font style="color:rgb(51, 51, 51);">Skills vs Commands</font>**<font style="color:rgb(51, 51, 51);">：两者均用</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">/</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">触发，但 Skills（</font><code><font style="color:rgb(51, 51, 51);">.claude/skills/</font></code><font style="color:rgb(51, 51, 51);">）是新一代格式，支持多文件组织、Claude 自动触发、更丰富的 frontmatter 控制；Commands（</font><code><font style="color:rgb(51, 51, 51);">.claude/commands/</font></code><font style="color:rgb(51, 51, 51);">）为旧格式，仍完全兼容，新项目推荐直接使用 Skills。</font>

***

## <font style="color:rgb(51, 51, 51);">一、常用内置斜杠命令</font>

<font style="color:rgb(51, 51, 51);">内置命令是 Claude Code 自带的核心功能，直接输入就能用。新手优先掌握这几类高频命令：</font>

### <font style="color:rgb(51, 51, 51);">基础操作命令</font>

| <font style="color:rgb(255, 255, 255);">命令</font> | <font style="color:rgb(255, 255, 255);">用途</font> | <font style="color:rgb(255, 255, 255);">新手示例</font> |
| --- | --- | --- |
| <code><font style="color:rgb(51, 51, 51);">/help</font></code> | <font style="color:rgb(51, 51, 51);">查看所有可用命令及说明（含 MCP 命令）</font> | <font style="color:rgb(51, 51, 51);">输入</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">/help</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">快速查命令清单</font> |
| <code><font style="color:rgb(51, 51, 51);">/exit</font></code> | <font style="color:rgb(51, 51, 51);">退出当前交互式会话</font> | <font style="color:rgb(51, 51, 51);">不想继续聊了，输</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">/exit</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">直接走</font> |
| <code><font style="color:rgb(51, 51, 51);">/clear</font></code> | <font style="color:rgb(51, 51, 51);">清除当前对话历史</font> | <font style="color:rgb(51, 51, 51);">会话太乱？</font><code><font style="color:rgb(51, 51, 51);">/clear</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">一键清空</font> |

<font style="color:rgb(51, 51, 51);">例如我们使用</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:rgb(51, 51, 51);">/help</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">命令查看帮助信息，</font>**<font style="color:rgb(51, 51, 51);">Tab</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">键可以切换菜单，</font>**<font style="color:rgb(51, 51, 51);">Esc</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">退出：</font>

![1783653949948-59c32850-ac2e-4967-b6fb-4f3bf92b2562.png](./img/wf9R51v5S5sXlvV1/1783653949948-59c32850-ac2e-4967-b6fb-4f3bf92b2562-178369.png)

### <font style="color:rgb(51, 51, 51);">会话管理命令</font>

| <font style="color:rgb(255, 255, 255);">命令</font> | <font style="color:rgb(255, 255, 255);">语法</font> | <font style="color:rgb(255, 255, 255);">功能说明</font> | <font style="color:rgb(255, 255, 255);">使用示例</font> | <font style="color:rgb(255, 255, 255);">注意事项</font> |
| --- | --- | --- | --- | --- |
| <code><font style="color:rgb(51, 51, 51);">/clear</font></code> | <code><font style="color:rgb(51, 51, 51);">/clear</font></code> | <font style="color:rgb(51, 51, 51);">清除全部对话历史，开始全新会话</font> | <code><font style="color:rgb(51, 51, 51);">/clear</font></code> | <font style="color:rgb(51, 51, 51);">不可恢复，建议先</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">/export</font></code> |
| <code><font style="color:rgb(51, 51, 51);">/compact</font></code> | <code><font style="color:rgb(51, 51, 51);">/compact [侧重点]</font></code> | <font style="color:rgb(51, 51, 51);">智能压缩历史对话，保留语义，缩小 Token 占用</font> | <code><font style="color:rgb(51, 51, 51);">/compact 保留数据库设计部分</font></code> | <font style="color:rgb(51, 51, 51);">与</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">/clear</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">区别：保留语义摘要而非完全清空</font> |
| <code><font style="color:rgb(51, 51, 51);">/resume</font></code> | <code><font style="color:rgb(51, 51, 51);">/resume [id或名称]</font></code> | <font style="color:rgb(51, 51, 51);">恢复历史会话；不带参数列出所有可恢复会话</font> | <code><font style="color:rgb(51, 51, 51);">/resume task-hub-backend</font></code> | <font style="color:rgb(51, 51, 51);">配合</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">/rename</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">效果更佳</font> |
| <code><font style="color:rgb(51, 51, 51);">/rewind</font></code> | <code><font style="color:rgb(51, 51, 51);">/rewind</font></code> | <font style="color:rgb(51, 51, 51);">撤销最近操作，含文件修改和对话内容，恢复到上一检查点；新版新增"仅回退代码"选项，可保留对话历史</font> | <font style="color:rgb(51, 51, 51);">按</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">Esc</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">两次呼出回退菜单</font> | <font style="color:rgb(51, 51, 51);">适合 Agent 执行结果不满意时回退</font> |
| <code><font style="color:rgb(51, 51, 51);">/rename</font></code> | <code><font style="color:rgb(51, 51, 51);">/rename <名称></font></code> | <font style="color:rgb(51, 51, 51);">为当前会话命名，便于后续</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">/resume</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">找回</font> | <code><font style="color:rgb(51, 51, 51);">/rename auth-module-refactor</font></code> | <font style="color:rgb(51, 51, 51);">建议命名规范：</font><code><font style="color:rgb(51, 51, 51);">功能-操作</font></code> |
| <code><font style="color:rgb(51, 51, 51);">/export</font></code> | <code><font style="color:rgb(51, 51, 51);">/export [文件名]</font></code> | <font style="color:rgb(51, 51, 51);">导出对话为文件；不指定文件名则复制到剪贴板</font> | <code><font style="color:rgb(51, 51, 51);">/export debug-session.md</font></code> | <font style="color:rgb(51, 51, 51);">支持 Markdown 格式</font> |
| <code><font style="color:rgb(51, 51, 51);">/copy</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(255, 255, 255);">NEW</font> | <code><font style="color:rgb(51, 51, 51);">/copy</font></code> | <font style="color:rgb(51, 51, 51);">将 Claude 最近一次回复复制到剪贴板；若含多个代码块，会弹出交互式选择器</font> | <code><font style="color:rgb(51, 51, 51);">/copy</font></code> | <font style="color:rgb(51, 51, 51);">比手动框选文本快得多</font> |
| <code><font style="color:rgb(51, 51, 51);">/btw</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(255, 255, 255);">NEW</font> | <code><font style="color:rgb(51, 51, 51);">/btw <问题></font></code> | <font style="color:rgb(51, 51, 51);">在不影响主任务上下文的情况下，快速插问一个临时问题，回答不会污染主对话流</font> | <code><font style="color:rgb(51, 51, 51);">/btw Redis 的默认端口是多少？</font></code> | <font style="color:rgb(51, 51, 51);">适合临时查阅而不想干扰当前任务</font> |
| <code><font style="color:rgb(51, 51, 51);">/exit</font></code> | <code><font style="color:rgb(51, 51, 51);">/exit</font></code> | <font style="color:rgb(51, 51, 51);">安全退出 Claude Code REPL</font> | <code><font style="color:rgb(51, 51, 51);">/exit</font></code> | <font style="color:rgb(51, 51, 51);">—</font> |

### <font style="color:rgb(51, 51, 51);">上下文与记忆</font>

| <font style="color:rgb(255, 255, 255);">命令</font> | <font style="color:rgb(255, 255, 255);">语法</font> | <font style="color:rgb(255, 255, 255);">功能说明</font> | <font style="color:rgb(255, 255, 255);">使用示例</font> | <font style="color:rgb(255, 255, 255);">注意事项</font> |
| --- | --- | --- | --- | --- |
| <code><font style="color:rgb(51, 51, 51);">/context</font></code> | <code><font style="color:rgb(51, 51, 51);">/context</font></code> | <font style="color:rgb(51, 51, 51);">可视化上下文窗口使用量，显示各部分（历史/文件/系统提示/Skills）占比</font> | <code><font style="color:rgb(51, 51, 51);">/context</font></code> | <font style="color:rgb(51, 51, 51);">接近上限时应执行</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">/compact</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">或</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">/clear</font></code> |
| <code><font style="color:rgb(51, 51, 51);">/memory</font></code> | <code><font style="color:rgb(51, 51, 51);">/memory</font></code> | <font style="color:rgb(51, 51, 51);">打开编辑器修改</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">CLAUDE.md</font></code><br/><font style="color:rgb(51, 51, 51);">（项目级与全局级），跨会话持久化项目约定</font> | <code><font style="color:rgb(51, 51, 51);">/memory</font></code> | <font style="color:rgb(51, 51, 51);">修改后对后续所有会话生效</font> |
| <code><font style="color:rgb(51, 51, 51);">/add-dir</font></code> | <code><font style="color:rgb(51, 51, 51);">/add-dir <路径></font></code> | <font style="color:rgb(51, 51, 51);">将额外目录纳入工作范围，适合 monorepo 或跨目录操作</font> | <code><font style="color:rgb(51, 51, 51);">/add-dir ../packages/shared</font></code> | <font style="color:rgb(51, 51, 51);">可多次调用添加多个目录</font> |
| <code><font style="color:rgb(51, 51, 51);">/todos</font></code> | <code><font style="color:rgb(51, 51, 51);">/todos</font></code> | <font style="color:rgb(51, 51, 51);">列出当前会话中 Claude 记录的 TODO 事项</font> | <code><font style="color:rgb(51, 51, 51);">/todos</font></code> | <font style="color:rgb(51, 51, 51);">—</font> |
| <code><font style="color:rgb(51, 51, 51);">/diff</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(255, 255, 255);">NEW</font> | <code><font style="color:rgb(51, 51, 51);">/diff</font></code> | <font style="color:rgb(51, 51, 51);">查看本次会话中所有文件变更的 diff 摘要，便于回顾 Claude 做了哪些修改</font> | <code><font style="color:rgb(51, 51, 51);">/diff</font></code> | <font style="color:rgb(51, 51, 51);">与</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">/rewind</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">配合：先</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">/diff</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">确认变更，再决定是否回滚</font> |

### <font style="color:rgb(51, 51, 51);">项目与配置</font>

| <font style="color:rgb(255, 255, 255);">命令</font> | <font style="color:rgb(255, 255, 255);">语法</font> | <font style="color:rgb(255, 255, 255);">功能说明</font> | <font style="color:rgb(255, 255, 255);">使用示例</font> | <font style="color:rgb(255, 255, 255);">注意事项</font> |
| --- | --- | --- | --- | --- |
| <code><font style="color:rgb(51, 51, 51);">/init</font></code> | <code><font style="color:rgb(51, 51, 51);">/init</font></code> | <font style="color:rgb(51, 51, 51);">分析项目结构，自动生成</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">CLAUDE.md</font></code><br/><font style="color:rgb(51, 51, 51);">，写入技术栈/构建命令/代码规范</font> | <code><font style="color:rgb(51, 51, 51);">/init</font></code> | <font style="color:rgb(51, 51, 51);">新项目必备第一步</font> |
| <code><font style="color:rgb(51, 51, 51);">/config</font></code> | <code><font style="color:rgb(51, 51, 51);">/config</font></code> | <font style="color:rgb(51, 51, 51);">以交互式界面管理 Claude Code 全局配置</font> | <code><font style="color:rgb(51, 51, 51);">/config</font></code> | <font style="color:rgb(51, 51, 51);">—</font> |
| <code><font style="color:rgb(51, 51, 51);">/status</font></code> | <code><font style="color:rgb(51, 51, 51);">/status</font></code> | <font style="color:rgb(51, 51, 51);">打开设置状态页，查看当前配置概览</font> | <code><font style="color:rgb(51, 51, 51);">/status</font></code> | <font style="color:rgb(51, 51, 51);">—</font> |
| <code><font style="color:rgb(51, 51, 51);">/hooks</font></code> | <code><font style="color:rgb(51, 51, 51);">/hooks</font></code> | <font style="color:rgb(51, 51, 51);">交互式配置生命周期 Hook（如提交前 lint、保存后格式化）</font> | <code><font style="color:rgb(51, 51, 51);">/hooks</font></code> | <font style="color:rgb(51, 51, 51);">支持 PreToolUse / PostToolUse / Notification / Stop</font> |
| <code><font style="color:rgb(51, 51, 51);">/permissions</font></code> | <code><font style="color:rgb(51, 51, 51);">/permissions</font></code> | <font style="color:rgb(51, 51, 51);">查看或更新工具权限（读文件/写文件/执行命令等）</font> | <code><font style="color:rgb(51, 51, 51);">/permissions</font></code> | <font style="color:rgb(51, 51, 51);">限制权限可提升操作安全性</font> |
| <code><font style="color:rgb(51, 51, 51);">/sandbox</font></code> | <code><font style="color:rgb(51, 51, 51);">/sandbox</font></code> | <font style="color:rgb(51, 51, 51);">启用隔离沙盒环境执行 Bash 命令，防止影响宿主系统</font> | <code><font style="color:rgb(51, 51, 51);">/sandbox</font></code> | <font style="color:rgb(51, 51, 51);">适合测试不确定的脚本</font> |
| <code><font style="color:rgb(51, 51, 51);">/doctor</font></code> | <code><font style="color:rgb(51, 51, 51);">/doctor</font></code> | <font style="color:rgb(51, 51, 51);">诊断安装状态，检查依赖/配置/网络连接是否正常</font> | <code><font style="color:rgb(51, 51, 51);">/doctor</font></code> | <font style="color:rgb(51, 51, 51);">遇到异常时首先执行</font> |

### <font style="color:rgb(51, 51, 51);">模型与输出</font>

| <font style="color:rgb(255, 255, 255);">命令</font> | <font style="color:rgb(255, 255, 255);">语法</font> | <font style="color:rgb(255, 255, 255);">功能说明</font> | <font style="color:rgb(255, 255, 255);">使用示例</font> | <font style="color:rgb(255, 255, 255);">注意事项</font> |
| --- | --- | --- | --- | --- |
| <code><font style="color:rgb(51, 51, 51);">/model</font></code> | <code><font style="color:rgb(51, 51, 51);">/model [模型名]</font></code> | <font style="color:rgb(51, 51, 51);">切换底层 AI 模型；不带参数显示交互式选择菜单</font> | <code><font style="color:rgb(51, 51, 51);">/model claude-haiku-4-5-20251001</font></code> | <font style="color:rgb(51, 51, 51);">见下方模型对照表</font> |
| <code><font style="color:rgb(51, 51, 51);">/plan</font></code> | <code><font style="color:rgb(51, 51, 51);">/plan [任务描述]</font></code> | <font style="color:rgb(51, 51, 51);">进入计划模式，Claude 先输出执行计划供确认再行动</font> | <code><font style="color:rgb(51, 51, 51);">/plan 重构认证模块并补充测试</font></code> | <font style="color:rgb(51, 51, 51);">适合复杂多步骤任务，避免走偏</font> |
| <code><font style="color:rgb(51, 51, 51);">/output-style</font></code> | <code><font style="color:rgb(51, 51, 51);">/output-style</font></code> | <font style="color:rgb(51, 51, 51);">设置响应格式（代码优先/说明优先/简洁模式等）</font> | <code><font style="color:rgb(51, 51, 51);">/output-style</font></code> | <font style="color:rgb(51, 51, 51);">—</font> |
| <code><font style="color:rgb(51, 51, 51);">/theme</font></code> | <code><font style="color:rgb(51, 51, 51);">/theme</font></code> | <font style="color:rgb(51, 51, 51);">切换终端界面颜色方案</font> | <code><font style="color:rgb(51, 51, 51);">/theme</font></code> | <font style="color:rgb(51, 51, 51);">—</font> |
| <code><font style="color:rgb(51, 51, 51);">/statusline</font></code> | <code><font style="color:rgb(51, 51, 51);">/statusline</font></code> | <font style="color:rgb(51, 51, 51);">定制终端底部状态栏显示内容</font> | <code><font style="color:rgb(51, 51, 51);">/statusline</font></code> | <font style="color:rgb(51, 51, 51);">—</font> |
| <code><font style="color:rgb(51, 51, 51);">/vim</font></code> | <code><font style="color:rgb(51, 51, 51);">/vim</font></code> | <font style="color:rgb(51, 51, 51);">启用 Vim 键位绑定</font> | <code><font style="color:rgb(51, 51, 51);">/vim</font></code> | <font style="color:rgb(51, 51, 51);">适合 Vim 用户</font> |
| <code><font style="color:rgb(51, 51, 51);">/terminal-setup</font></code> | <code><font style="color:rgb(51, 51, 51);">/terminal-setup</font></code> | <font style="color:rgb(51, 51, 51);">安装</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">Shift+Enter</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">换行绑定，方便输入多行 Prompt</font> | <code><font style="color:rgb(51, 51, 51);">/terminal-setup</font></code> | <font style="color:rgb(51, 51, 51);">首次使用建议配置</font> |

**<font style="color:rgb(51, 51, 51);">可用模型对照表（2026）：</font>**

| <font style="color:rgb(255, 255, 255);">模型标识</font> | <font style="color:rgb(255, 255, 255);">定位</font> | <font style="color:rgb(255, 255, 255);">适用场景</font> |
| --- | --- | --- |
| <code><font style="color:rgb(51, 51, 51);">claude-sonnet-4-6</font></code> | <font style="color:rgb(51, 51, 51);">均衡型（默认）</font> | <font style="color:rgb(51, 51, 51);">日常开发任务，Pro/Max5 用户首选</font> |
| <code><font style="color:rgb(51, 51, 51);">claude-haiku-4-5-20251001</font></code> | <font style="color:rgb(51, 51, 51);">快速轻量</font> | <font style="color:rgb(51, 51, 51);">简单查询、自定义命令中节省 Token</font> |
| <code><font style="color:rgb(51, 51, 51);">claude-opus-4-6</font></code> | <font style="color:rgb(51, 51, 51);">高能力旗舰</font> | <font style="color:rgb(51, 51, 51);">复杂架构规划、高难度代码推理，Max20 用户可作默认</font> |

### <font style="color:rgb(51, 51, 51);">代码与工具</font>

| <font style="color:rgb(255, 255, 255);">命令</font> | <font style="color:rgb(255, 255, 255);">语法</font> | <font style="color:rgb(255, 255, 255);">功能说明</font> | <font style="color:rgb(255, 255, 255);">使用示例</font> | <font style="color:rgb(255, 255, 255);">注意事项</font> |
| --- | --- | --- | --- | --- |
| <code><font style="color:rgb(51, 51, 51);">/review</font></code> | <code><font style="color:rgb(51, 51, 51);">/review</font></code> | <font style="color:rgb(51, 51, 51);">对最近修改的代码进行结构化 Code Review，按优先级输出改进建议</font> | <code><font style="color:rgb(51, 51, 51);">/review</font></code> | <font style="color:rgb(51, 51, 51);">—</font> |
| <code><font style="color:rgb(51, 51, 51);">/security-review</font></code> | <code><font style="color:rgb(51, 51, 51);">/security-review</font></code> | <font style="color:rgb(51, 51, 51);">针对当前改动进行安全专项审查（SQL 注入/XSS/敏感信息泄露等）</font> | <code><font style="color:rgb(51, 51, 51);">/security-review</font></code> | <font style="color:rgb(51, 51, 51);">上线前必执行</font> |
| <code><font style="color:rgb(51, 51, 51);">/pr-comments</font></code> | <code><font style="color:rgb(51, 51, 51);">/pr-comments</font></code> | <font style="color:rgb(51, 51, 51);">拉取当前分支关联 PR 的审查意见，在终端中直接处理</font> | <code><font style="color:rgb(51, 51, 51);">/pr-comments</font></code> | <font style="color:rgb(51, 51, 51);">需配置 GitHub 集成</font> |
| <code><font style="color:rgb(51, 51, 51);">/install-github-app</font></code> | <code><font style="color:rgb(51, 51, 51);">/install-github-app</font></code> | <font style="color:rgb(51, 51, 51);">配置 GitHub Actions 集成，Claude 自动 Review 新 PR</font> | <code><font style="color:rgb(51, 51, 51);">/install-github-app</font></code> | <font style="color:rgb(51, 51, 51);">生成</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">.github/workflows/claude-code-review.yml</font></code> |
| <code><font style="color:rgb(51, 51, 51);">/agents</font></code> | <code><font style="color:rgb(51, 51, 51);">/agents</font></code> | <font style="color:rgb(51, 51, 51);">查看、创建和管理专项子代理（DB 专家/安全专家/测试专家等）</font> | <code><font style="color:rgb(51, 51, 51);">/agents</font></code> | <font style="color:rgb(51, 51, 51);">—</font> |
| <code><font style="color:rgb(51, 51, 51);">/bashes</font></code> | <code><font style="color:rgb(51, 51, 51);">/bashes</font></code> | <font style="color:rgb(51, 51, 51);">查看当前后台运行的 Bash 进程，可中断或查看输出</font> | <code><font style="color:rgb(51, 51, 51);">/bashes</font></code> | <font style="color:rgb(51, 51, 51);">—</font> |
| <code><font style="color:rgb(51, 51, 51);">/skills</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(255, 255, 255);">NEW</font> | <code><font style="color:rgb(51, 51, 51);">/skills</font></code> | <font style="color:rgb(51, 51, 51);">列出所有可用的 Skills（内置 + 项目级 + 个人级），含描述和触发方式</font> | <code><font style="color:rgb(51, 51, 51);">/skills</font></code> | <font style="color:rgb(51, 51, 51);">上下文预算不足时部分 Skills 会被排除，通过此命令可确认加载状态</font> |

### <font style="color:rgb(51, 51, 51);">集成与扩展</font>

| <font style="color:rgb(255, 255, 255);">命令</font> | <font style="color:rgb(255, 255, 255);">语法</font> | <font style="color:rgb(255, 255, 255);">功能说明</font> | <font style="color:rgb(255, 255, 255);">使用示例</font> | <font style="color:rgb(255, 255, 255);">注意事项</font> |
| --- | --- | --- | --- | --- |
| <code><font style="color:rgb(51, 51, 51);">/mcp</font></code> | <code><font style="color:rgb(51, 51, 51);">/mcp</font></code> | <font style="color:rgb(51, 51, 51);">管理 MCP 服务器连接（连接/断开/查看可用工具）</font> | <code><font style="color:rgb(51, 51, 51);">/mcp</font></code> | <font style="color:rgb(51, 51, 51);">见第七节 MCP 命令详解</font> |
| <code><font style="color:rgb(51, 51, 51);">/ide</font></code> | <code><font style="color:rgb(51, 51, 51);">/ide</font></code> | <font style="color:rgb(51, 51, 51);">配置与 VSCode / JetBrains 等 IDE 的联动集成</font> | <code><font style="color:rgb(51, 51, 51);">/ide</font></code> | <font style="color:rgb(51, 51, 51);">—</font> |
| <code><font style="color:rgb(51, 51, 51);">/plugin</font></code> | <code><font style="color:rgb(51, 51, 51);">/plugin [子命令]</font></code> | <font style="color:rgb(51, 51, 51);">管理 Claude Code 插件：安装、卸载、更新、浏览市场</font> | <code><font style="color:rgb(51, 51, 51);">/plugin install typescript-lsp</font></code> | <font style="color:rgb(51, 51, 51);">官方插件市场含 36 款精选插件</font> |
| <code><font style="color:rgb(51, 51, 51);">/teleport</font></code> | <code><font style="color:rgb(51, 51, 51);">/teleport</font></code> | <font style="color:rgb(51, 51, 51);">将 claude.ai 网页端发起的会话迁移到本地终端继续（云端 → 本地方向）</font> | <code><font style="color:rgb(51, 51, 51);">/teleport</font></code> | <font style="color:rgb(51, 51, 51);">需安装 GitHub App，仅支持 GitHub 托管仓库</font> |

<code>**<font style="color:rgb(51, 51, 51);">/plugin</font>**</code>**<font style="color:rgb(51, 51, 51);"> </font>\*\*\*\*<font style="color:rgb(51, 51, 51);">子命令详情：</font>**

| <font style="color:rgb(255, 255, 255);">子命令</font> | <font style="color:rgb(255, 255, 255);">功能</font> |
| --- | --- |
| <code><font style="color:rgb(51, 51, 51);">/plugin install <名称></font></code> | <font style="color:rgb(51, 51, 51);">安装指定插件</font> |
| <code><font style="color:rgb(51, 51, 51);">/plugin list</font></code> | <font style="color:rgb(51, 51, 51);">列出所有已安装插件</font> |
| <code><font style="color:rgb(51, 51, 51);">/plugin update</font></code> | <font style="color:rgb(51, 51, 51);">更新所有已安装插件</font> |
| <code><font style="color:rgb(51, 51, 51);">/plugin marketplace</font></code> | <font style="color:rgb(51, 51, 51);">浏览官方插件市场</font> |
| <code><font style="color:rgb(51, 51, 51);">/plugin uninstall <名称></font></code> | <font style="color:rgb(51, 51, 51);">卸载指定插件</font> |

### <font style="color:rgb(51, 51, 51);">统计与账户</font>

| <font style="color:rgb(255, 255, 255);">命令</font> | <font style="color:rgb(255, 255, 255);">语法</font> | <font style="color:rgb(255, 255, 255);">功能说明</font> | <font style="color:rgb(255, 255, 255);">使用示例</font> | <font style="color:rgb(255, 255, 255);">注意事项</font> |
| --- | --- | --- | --- | --- |
| <code><font style="color:rgb(51, 51, 51);">/cost</font></code> | <code><font style="color:rgb(51, 51, 51);">/cost</font></code> | <font style="color:rgb(51, 51, 51);">显示当前会话的 Token 消耗量与预估费用</font> | <code><font style="color:rgb(51, 51, 51);">/cost</font></code> | <font style="color:rgb(51, 51, 51);">API 计费用户可见；订阅制用户 Token 已含在套餐内</font> |
| <code><font style="color:rgb(51, 51, 51);">/usage</font></code> | <code><font style="color:rgb(51, 51, 51);">/usage</font></code> | <font style="color:rgb(51, 51, 51);">查看当前套餐用量、剩余配额和速率限制状态</font> | <code><font style="color:rgb(51, 51, 51);">/usage</font></code> | <font style="color:rgb(51, 51, 51);">—</font> |
| <code><font style="color:rgb(51, 51, 51);">/stats</font></code> | <code><font style="color:rgb(51, 51, 51);">/stats</font></code> | <font style="color:rgb(51, 51, 51);">图表形式展示历史使用数据（每日 Token / 会话数量）</font> | <code><font style="color:rgb(51, 51, 51);">/stats</font></code> | <font style="color:rgb(51, 51, 51);">—</font> |
| <code><font style="color:rgb(51, 51, 51);">/release-notes</font></code> | <code><font style="color:rgb(51, 51, 51);">/release-notes</font></code> | <font style="color:rgb(51, 51, 51);">查看 Claude Code 最新版本变更记录</font> | <code><font style="color:rgb(51, 51, 51);">/release-notes</font></code> | <font style="color:rgb(51, 51, 51);">—</font> |
| <code><font style="color:rgb(51, 51, 51);">/bug</font></code> | <code><font style="color:rgb(51, 51, 51);">/bug</font></code> | <font style="color:rgb(51, 51, 51);">将当前会话上下文打包，向 Anthropic 提交 Bug 报告</font> | <code><font style="color:rgb(51, 51, 51);">/bug</font></code> | <font style="color:rgb(51, 51, 51);">—</font> |
| <code><font style="color:rgb(51, 51, 51);">/login</font></code> | <code><font style="color:rgb(51, 51, 51);">/login</font></code> | <font style="color:rgb(51, 51, 51);">登录或切换 Anthropic 账户</font> | <code><font style="color:rgb(51, 51, 51);">/login</font></code> | <font style="color:rgb(51, 51, 51);">适合多账号开发者</font> |
| <code><font style="color:rgb(51, 51, 51);">/logout</font></code> | <code><font style="color:rgb(51, 51, 51);">/logout</font></code> | <font style="color:rgb(51, 51, 51);">注销当前账户</font> | <code><font style="color:rgb(51, 51, 51);">/logout</font></code> | <font style="color:rgb(51, 51, 51);">—</font> |
| <code><font style="color:rgb(51, 51, 51);">/privacy-settings</font></code> | <code><font style="color:rgb(51, 51, 51);">/privacy-settings</font></code> | <font style="color:rgb(51, 51, 51);">管理数据使用偏好（是否允许对话用于模型训练等）</font> | <code><font style="color:rgb(51, 51, 51);">/privacy-settings</font></code> | <font style="color:rgb(51, 51, 51);">—</font> |
| <code><font style="color:rgb(51, 51, 51);">/remote-env</font></code> | <code><font style="color:rgb(51, 51, 51);">/remote-env</font></code> | <font style="color:rgb(51, 51, 51);">配置远程会话的环境变量</font> | <code><font style="color:rgb(51, 51, 51);">/remote-env</font></code> | <font style="color:rgb(51, 51, 51);">—</font> |

***

## <font style="color:rgb(51, 51, 51);">二、内置 Skills</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(255, 255, 255);">NEW</font>

<font style="color:rgb(51, 51, 51);">内置 Skills 是随 Claude Code 附带的预置 AI 工作流，与内置命令不同——它们加载详细提示词后由 Claude 推理执行，可产出更丰富的分析和操作结果，同样用</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">/</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">触发。</font>

<font style="color:rgb(51, 51, 51);"> </font>**<font style="color:rgb(51, 51, 51);">区别：内置命令 vs 内置 Skills</font>**<font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);">内置命令（如</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">/clear</font></code><font style="color:rgb(51, 51, 51);">、</font><code><font style="color:rgb(51, 51, 51);">/compact</font></code><font style="color:rgb(51, 51, 51);">）执行固定逻辑，不涉及 AI 推理，速度极快。\
</font><font style="color:rgb(51, 51, 51);">内置 Skills（如</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">/debug</font></code><font style="color:rgb(51, 51, 51);">、</font><code><font style="color:rgb(51, 51, 51);">/simplify</font></code><font style="color:rgb(51, 51, 51);">）加载提示词后由 Claude 推理执行，结果更丰富，适合复杂分析任务。</font>

| <font style="color:rgb(255, 255, 255);">命令</font> | <font style="color:rgb(255, 255, 255);">功能说明</font> | <font style="color:rgb(255, 255, 255);">适用场景</font> |
| --- | --- | --- |
| <code><font style="color:rgb(51, 51, 51);">/simplify</font></code> | <font style="color:rgb(51, 51, 51);">将指定代码或文本简化，提升可读性，消除不必要的复杂度</font> | <font style="color:rgb(51, 51, 51);">重构冗长函数、简化过度工程化的代码</font> |
| <code><font style="color:rgb(51, 51, 51);">/debug</font></code> | <font style="color:rgb(51, 51, 51);">对报错信息或异常行为进行系统化根因分析，给出修复思路</font> | <font style="color:rgb(51, 51, 51);">定位难以复现的 bug</font> |
| <code><font style="color:rgb(51, 51, 51);">/batch</font></code> | <font style="color:rgb(51, 51, 51);">对多个文件或目标并行执行相同任务（如批量重命名、批量添加类型注解）</font> | <font style="color:rgb(51, 51, 51);">大批量重复性代码改动</font> |
| <code><font style="color:rgb(51, 51, 51);">/loop</font></code> | <font style="color:rgb(51, 51, 51);">在循环中反复执行某个操作直到满足退出条件（如不断重试测试直至通过）</font> | <font style="color:rgb(51, 51, 51);">自动化 CI 修复循环</font> |
| <code><font style="color:rgb(51, 51, 51);">/claude-api</font></code> | <font style="color:rgb(51, 51, 51);">快速生成调用 Anthropic API 的示例代码，支持指定模型和任务类型</font> | <font style="color:rgb(51, 51, 51);">搭建 Claude API 集成原型</font> |

***

## <font style="color:rgb(51, 51, 51);">三、命令前缀语法</font>

| <font style="color:rgb(255, 255, 255);">前缀</font> | <font style="color:rgb(255, 255, 255);">语法</font> | <font style="color:rgb(255, 255, 255);">功能说明</font> | <font style="color:rgb(255, 255, 255);">示例</font> | <font style="color:rgb(255, 255, 255);">对比</font> |
| --- | --- | --- | --- | --- |
| <code><font style="color:rgb(51, 51, 51);">/</font></code> | <code><font style="color:rgb(51, 51, 51);">/command</font></code> | <font style="color:rgb(51, 51, 51);">触发内置命令、内置 Skills 或自定义 Skills/Commands</font> | <code><font style="color:rgb(51, 51, 51);">/review</font></code> | <font style="color:rgb(51, 51, 51);">—</font> |
| <code><font style="color:rgb(51, 51, 51);">!</font></code> | <code><font style="color:rgb(51, 51, 51);">!<bash命令></font></code> | <font style="color:rgb(51, 51, 51);">直接执行 Shell 命令，绕过 AI 处理，节省 Token</font> | <code><font style="color:rgb(51, 51, 51);">!git status</font></code> | <font style="color:rgb(51, 51, 51);">等价于在终端直接运行，但比「帮我查看 git 状态」省 Token</font> |
| <code><font style="color:rgb(51, 51, 51);">@</font></code> | <code><font style="color:rgb(51, 51, 51);">@<文件路径></font></code> | <font style="color:rgb(51, 51, 51);">将文件内容注入当前上下文</font> | <code><font style="color:rgb(51, 51, 51);">@src/api/users.ts</font></code> | <font style="color:rgb(51, 51, 51);">比手动粘贴代码更精准，支持多文件</font> |

<code>**<font style="color:rgb(51, 51, 51);">!</font>**</code>**<font style="color:rgb(51, 51, 51);"> </font>\*\*\*\*<font style="color:rgb(51, 51, 51);">前缀使用示例：</font>**

![1783653949864-47c65797-2675-4a47-926b-3a3621bb6af1.png](./img/wf9R51v5S5sXlvV1/1783653949864-47c65797-2675-4a47-926b-3a3621bb6af1-631005.png)

```plain
> ! ls
> !git log --oneline -10
> !npm test -- --coverage
> !cat logs/error.log | tail -50
```

**<font style="color:rgb(51, 51, 51);">@</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">前缀使用示例：</font>

![1783653949837-ea74f551-3ff0-4002-8711-61f6163d30e7.png](./img/wf9R51v5S5sXlvV1/1783653949837-ea74f551-3ff0-4002-8711-61f6163d30e7-956651.png)

```plain
> 对比 @src/auth/v1.ts 和 @src/auth/v2.ts 的实现差异
> 审查 @src/api/users.ts 中的错误处理逻辑是否完善
```

***

## <font style="color:rgb(51, 51, 51);">四、自定义 Skills（新推荐格式）</font>

<font style="color:rgb(51, 51, 51);">Skills 是自定义命令的新一代格式，取代旧版</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">.claude/commands/</font></code><font style="color:rgb(51, 51, 51);">。两种格式均可正常使用，但新项目建议直接使用 Skills。</font>

### <font style="color:rgb(51, 51, 51);">Skills vs Commands 对比</font>

| <font style="color:rgb(255, 255, 255);">特性</font> | <font style="color:rgb(255, 255, 255);">Skills（推荐）</font> | <font style="color:rgb(255, 255, 255);">Commands（旧格式）</font> |
| --- | --- | --- |
| <font style="color:rgb(51, 51, 51);">存储路径</font> | <code><font style="color:rgb(51, 51, 51);">.claude/skills/<名称>/SKILL.md</font></code> | <code><font style="color:rgb(51, 51, 51);">.claude/commands/<名称>.md</font></code> |
| <font style="color:rgb(51, 51, 51);">触发方式</font> | <code><font style="color:rgb(51, 51, 51);">/名称</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">手动触发，或 Claude 根据描述自动触发</font> | <code><font style="color:rgb(51, 51, 51);">/名称</font></code><br/><font style="color:rgb(51, 51, 51);">（仅手动触发）</font> |
| <font style="color:rgb(51, 51, 51);">多文件支持</font> | <font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">支持附带模板、示例、辅助脚本</font> | <font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">单文件</font> |
| <font style="color:rgb(51, 51, 51);">Claude 自动触发</font> | <font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">Claude 根据 description 智能判断调用</font> |  |
| <font style="color:rgb(51, 51, 51);">Agent Skills 标准</font> | <font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">符合开放标准，可跨工具共享</font> |  |

### <font style="color:rgb(51, 51, 51);">创建 Skill 步骤</font>

#### <font style="color:rgb(51, 51, 51);">步骤 1：创建目录结构</font>

<font style="color:rgb(51, 51, 51);">自定义 Skills 分两种，存储位置不同：</font>

* **<font style="color:rgb(51, 51, 51);">项目 Skill</font>**<font style="color:rgb(51, 51, 51);">：只在当前项目生效，团队共享 → 目录：</font><code><font style="color:rgb(51, 51, 51);">.claude/skills/<名称>/</font></code>
* **<font style="color:rgb(51, 51, 51);">个人 Skill</font>**<font style="color:rgb(51, 51, 51);">：所有项目通用，自己用 → 目录：</font><code><font style="color:rgb(51, 51, 51);">~/.claude/skills/<名称>/</font></code>

```plain
# 创建项目级 Skill（团队共享，纳入 git）
mkdir -p .claude/skills/optimize

# 创建个人级 Skill（跨项目通用，本地私有）
mkdir -p ~/.claude/skills/fix-bug
```

#### <font style="color:rgb(51, 51, 51);">步骤 2：编写 SKILL.md</font>

<font style="color:rgb(51, 51, 51);">新建</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">SKILL.md</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">文件，YAML frontmatter 写配置，下方 Markdown 正文写提示词。</font><code><font style="color:rgb(51, 51, 51);">name</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">字段定义触发命令名。</font>

**<font style="color:rgb(51, 51, 51);">示例：创建代码性能优化 Skill</font>**

```plain
---
name: optimize
description: 分析代码性能瓶颈，给出优化建议。当用户提到性能问题时自动触发。
allowed-tools: Read, Grep, Glob
argument-hint: [目标文件或目录]
model: claude-sonnet-4-6
---

分析以下代码的性能瓶颈，给出具体的优化建议，优先考虑时间复杂度和内存占用：
$ARGUMENTS
```

<font style="color:rgb(51, 51, 51);">使用时输入：</font>

/optimize src/utils/data-processor.ts

### <font style="color:rgb(51, 51, 51);">子目录命名空间组织</font>

<font style="color:rgb(51, 51, 51);">可在</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">.claude/skills/</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">下用子目录按职能分类管理，目录名即命令名：</font>

```plain
.claude/skills/
├── optimize/            → /optimize
│   ├── SKILL.md
│   └── examples/        # 可选：示例文件辅助 Claude 理解
├── debug/               → /debug
│   ├── SKILL.md
│   └── scripts/         # 可选：辅助脚本
└── commit/              → /commit
    └── SKILL.md
```

***

## <font style="color:rgb(51, 51, 51);">五、自定义斜杠命令（旧格式，兼容）</font>

<font style="color:rgb(51, 51, 51);">如果有</font>**<font style="color:rgb(51, 51, 51);">重复使用的提示词</font>**<font style="color:rgb(51, 51, 51);">（比如固定的代码审查要求、重复的指令模板），可以把它做成自定义命令，一键调用。</font>

**<font style="color:rgb(51, 51, 51);">命令文件存储位置：</font>**

| <font style="color:rgb(255, 255, 255);">作用域</font> | <font style="color:rgb(255, 255, 255);">存储路径</font> | <font style="color:rgb(255, 255, 255);">共享方式</font> | <font style="color:rgb(255, 255, 255);">适用场景</font> |
| --- | --- | --- | --- |
| <font style="color:rgb(51, 51, 51);">项目级</font> | <code><font style="color:rgb(51, 51, 51);">.claude/commands/<命令名>.md</font></code> | <font style="color:rgb(51, 51, 51);">纳入 git，团队共享</font> | <font style="color:rgb(51, 51, 51);">项目专属工作流（如特定框架的代码生成）</font> |
| <font style="color:rgb(51, 51, 51);">个人级</font> | <code><font style="color:rgb(51, 51, 51);">~/.claude/commands/<命令名>.md</font></code> | <font style="color:rgb(51, 51, 51);">本地私有</font> | <font style="color:rgb(51, 51, 51);">通用开发习惯（如个人代码风格检查）</font> |

**<font style="color:rgb(51, 51, 51);">参数语法：</font>**

| <font style="color:rgb(255, 255, 255);">语法</font> | <font style="color:rgb(255, 255, 255);">说明</font> | <font style="color:rgb(255, 255, 255);">命令文件示例</font> | <font style="color:rgb(255, 255, 255);">调用示例</font> |
| --- | --- | --- | --- |
| <code><font style="color:rgb(51, 51, 51);">$ARGUMENTS</font></code> | <font style="color:rgb(51, 51, 51);">捕获命令名之后的所有内容</font> | <code><font style="color:rgb(51, 51, 51);">分析并修复：$ARGUMENTS</font></code> | <code><font style="color:rgb(51, 51, 51);">/fix 登录接口返回 500，见 logs/error.log</font></code> |
| <code><font style="color:rgb(51, 51, 51);">$1</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">$2</font></code> | <font style="color:rgb(51, 51, 51);">按空格分割的位置参数</font> | <code><font style="color:rgb(51, 51, 51);">修复 Issue #$1，优先级 $2</font></code> | <code><font style="color:rgb(51, 51, 51);">/fix-issue 42 high</font></code> |
| <code><font style="color:rgb(51, 51, 51);">!</code>cmd`</font>` | <font style="color:rgb(51, 51, 51);">执行 Shell 命令并将输出嵌入 Prompt</font> | <code><font style="color:rgb(51, 51, 51);">!</code>git diff HEAD`</font>` | <font style="color:rgb(51, 51, 51);">自动展开为命令执行结果</font> |
| <code><font style="color:rgb(51, 51, 51);">@文件路径</font></code> | <font style="color:rgb(51, 51, 51);">将文件内容注入 Prompt</font> | <code><font style="color:rgb(51, 51, 51);">审查 @src/utils/helpers.ts</font></code> | <font style="color:rgb(51, 51, 51);">自动读取文件内容</font> |

### <font style="color:rgb(51, 51, 51);">核心原理</font>

<font style="color:rgb(51, 51, 51);">自定义命令本质是</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:rgb(51, 51, 51);">Markdown 文本文件</font>**<font style="color:rgb(51, 51, 51);">——文件名就是命令名，文件内容就是要执行的提示词，支持传参数、调用 Bash 命令。</font>

### <font style="color:rgb(51, 51, 51);">步骤创建自定义命令</font>

#### <font style="color:rgb(51, 51, 51);">步骤 1：创建命令存储目录</font>

<font style="color:rgb(51, 51, 51);">自定义命令分两种，存储位置不同：</font>

* **<font style="color:rgb(51, 51, 51);">项目命令</font>**<font style="color:rgb(51, 51, 51);">：只在当前项目生效，团队共享 → 目录：</font><code><font style="color:rgb(51, 51, 51);">.claude/commands/</font></code>
* **<font style="color:rgb(51, 51, 51);">个人命令</font>**<font style="color:rgb(51, 51, 51);">：所有项目通用，自己用 → 目录：</font><code><font style="color:rgb(51, 51, 51);">~/.claude/commands/</font></code>

<font style="color:rgb(51, 51, 51);">以创建项目命令为例，先建目录：</font>

```plain
# 在项目根目录执行
mkdir -p .claude/commands
```

#### <font style="color:rgb(51, 51, 51);">步骤 2：写 Markdown 命令文件</font>

<font style="color:rgb(51, 51, 51);">新建一个</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">.md</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">文件，文件名就是命令名（比如</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">optimize.md</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">→ 命令</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">/optimize</font></code><font style="color:rgb(51, 51, 51);">），文件内容写提示词。</font>

**<font style="color:rgb(51, 51, 51);">示例：创建代码性能优化命令</font>**

```plain
# 写入提示词到文件
echo "分析这段代码的性能瓶颈，给出具体的优化建议，优先考虑时间复杂度和内存占用：" > .claude/commands/optimize.md
```

<font style="color:rgb(51, 51, 51);">现在，在会话里输入</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">/optimize</font></code><font style="color:rgb(51, 51, 51);">，再粘贴代码，Claude 就会按你的要求做性能分析！</font>

### <font style="color:rgb(51, 51, 51);">高级技巧：给命令加参数</font>

<font style="color:rgb(51, 51, 51);">命令可以带参数，用</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">$ARGUMENTS</font></code><font style="color:rgb(51, 51, 51);">（捕获所有参数）或</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">$1</font></code><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">$2</font></code><font style="color:rgb(51, 51, 51);">（按位置取参数）。</font>

**<font style="color:rgb(51, 51, 51);">示例：带参数的 Bug 修复命令</font>**

<font style="color:rgb(51, 51, 51);">创建命令文件</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">.claude/commands/fix-issue.md</font></code><font style="color:rgb(51, 51, 51);">：</font>

```plain
修复 Issue #$ARGUMENTS，要求：
1. 符合项目编码规范
2. 附上测试用例
3. 说明修复思路
```

<font style="color:rgb(51, 51, 51);">使用命令：</font>

/fix-issue 123  # $ARGUMENTS 会被替换成 "123"

***

## <font style="color:rgb(51, 51, 51);">六、Frontmatter 字段参考</font>

<font style="color:rgb(51, 51, 51);">自定义命令文件（</font><code><font style="color:rgb(51, 51, 51);">commands/*.md</font></code><font style="color:rgb(51, 51, 51);">）和 Skills（</font><code><font style="color:rgb(51, 51, 51);">skills/*/SKILL.md</font></code><font style="color:rgb(51, 51, 51);">）顶部均可添加 YAML Frontmatter 进行精细配置：</font>

```plain
---
name: commit                          # Skills 中必填；命令文件中可选（默认取文件名）
allowed-tools: Bash(git add:*), Bash(git commit:*), Read, Edit
argument-hint: [commit-message]
description: 检查代码质量后提交
model: claude-haiku-4-5-20251001
context: fork
agent: general-purpose
disable-model-invocation: false
user-invocable: true
hooks:
  PreToolUse:
    - matcher: "Bash"
      hooks:
        - type: command
          command: "./scripts/validate.sh"
          once: true
---
```

### <font style="color:rgb(51, 51, 51);">字段说明</font>

| <font style="color:rgb(255, 255, 255);">字段</font> | <font style="color:rgb(255, 255, 255);">类型</font> | <font style="color:rgb(255, 255, 255);">必填</font> | <font style="color:rgb(255, 255, 255);">说明</font> |
| --- | --- | --- | --- |
| <code><font style="color:rgb(51, 51, 51);">name</font></code> | <font style="color:rgb(51, 51, 51);">string</font> | <font style="color:rgb(51, 51, 51);">Skills 必填</font> | <font style="color:rgb(51, 51, 51);">定义触发命令名（</font><code><font style="color:rgb(51, 51, 51);">/name</font></code><br/><font style="color:rgb(51, 51, 51);">）；命令文件默认取文件名</font> |
| <code><font style="color:rgb(51, 51, 51);">allowed-tools</font></code> | <font style="color:rgb(51, 51, 51);">string</font> | <font style="color:rgb(51, 51, 51);">否</font> | <font style="color:rgb(51, 51, 51);">命令可使用的工具，匹配的工具无需每次人工确认</font> |
| <code><font style="color:rgb(51, 51, 51);">argument-hint</font></code> | <font style="color:rgb(51, 51, 51);">string</font> | <font style="color:rgb(51, 51, 51);">否</font> | <font style="color:rgb(51, 51, 51);">在</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">/help</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">列表中显示的参数格式提示，如</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">[message]</font></code> |
| <code><font style="color:rgb(51, 51, 51);">description</font></code> | <font style="color:rgb(51, 51, 51);">string</font> | <font style="color:rgb(51, 51, 51);">否</font> | <font style="color:rgb(51, 51, 51);">命令功能描述，展示在</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">/help</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">和</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">/skills</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">列表中；Skills 中还用于让 Claude 判断是否自动触发</font> |
| <code><font style="color:rgb(51, 51, 51);">model</font></code> | <font style="color:rgb(51, 51, 51);">string</font> | <font style="color:rgb(51, 51, 51);">否</font> | <font style="color:rgb(51, 51, 51);">强制指定模型；简单任务用 Haiku 可降低成本</font> |
| <code><font style="color:rgb(51, 51, 51);">context</font></code> | <font style="color:rgb(51, 51, 51);">enum</font> | <font style="color:rgb(51, 51, 51);">否</font> | <code><font style="color:rgb(51, 51, 51);">fork</font></code><br/><font style="color:rgb(51, 51, 51);">：以独立子代理运行；</font><code><font style="color:rgb(51, 51, 51);">inline</font></code><br/><font style="color:rgb(51, 51, 51);">：在当前会话内运行</font> |
| <code><font style="color:rgb(51, 51, 51);">agent</font></code> | <font style="color:rgb(51, 51, 51);">string</font> | <font style="color:rgb(51, 51, 51);">否</font> | <code><font style="color:rgb(51, 51, 51);">context: fork</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">时指定代理类型</font> |
| <code><font style="color:rgb(51, 51, 51);">disable-model-invocation</font></code> | <font style="color:rgb(51, 51, 51);">bool</font> | <font style="color:rgb(51, 51, 51);">否</font> | <font style="color:rgb(51, 51, 51);">为</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">true</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">时禁止通过 Skill 工具编程调用此命令</font> |
| <code><font style="color:rgb(51, 51, 51);">user-invocable</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(255, 255, 255);">NEW</font> | <font style="color:rgb(51, 51, 51);">bool</font> | <font style="color:rgb(51, 51, 51);">否</font> | <font style="color:rgb(51, 51, 51);">为</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">false</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">时只允许 Claude 自动触发，用户无法手动</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">/调用</font></code> |
| <code><font style="color:rgb(51, 51, 51);">hooks</font></code> | <font style="color:rgb(51, 51, 51);">object</font> | <font style="color:rgb(51, 51, 51);">否</font> | <font style="color:rgb(51, 51, 51);">命令执行过程中的生命周期 Hook</font> |

### <code><font style="color:rgb(51, 51, 51);">allowed-tools</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">写法示例</font>

| <font style="color:rgb(255, 255, 255);">写法</font> | <font style="color:rgb(255, 255, 255);">含义</font> |
| --- | --- |
| <code><font style="color:rgb(51, 51, 51);">Read</font></code> | <font style="color:rgb(51, 51, 51);">允许读取任意文件</font> |
| <code><font style="color:rgb(51, 51, 51);">Read(src/*)</font></code> | <font style="color:rgb(51, 51, 51);">只允许读取</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">src/</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">目录</font> |
| <code><font style="color:rgb(51, 51, 51);">Bash(git *:*)</font></code> | <font style="color:rgb(51, 51, 51);">允许所有 git 子命令</font> |
| <code><font style="color:rgb(51, 51, 51);">Bash(npm test:*)</font></code> | <font style="color:rgb(51, 51, 51);">只允许运行</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">npm test</font></code> |
| <code><font style="color:rgb(51, 51, 51);">Read, Grep, Glob</font></code> | <font style="color:rgb(51, 51, 51);">组合多个工具</font> |

### <font style="color:rgb(51, 51, 51);">Hook 触发时机</font>

| <font style="color:rgb(255, 255, 255);">时机</font> | <font style="color:rgb(255, 255, 255);">说明</font> | <font style="color:rgb(255, 255, 255);">典型用途</font> |
| --- | --- | --- |
| <code><font style="color:rgb(51, 51, 51);">PreToolUse</font></code> | <font style="color:rgb(51, 51, 51);">工具调用前</font> | <font style="color:rgb(51, 51, 51);">提交前运行 lint、写文件前备份</font> |
| <code><font style="color:rgb(51, 51, 51);">PostToolUse</font></code> | <font style="color:rgb(51, 51, 51);">工具调用后</font> | <font style="color:rgb(51, 51, 51);">修改后自动格式化、生成变更日志</font> |
| <code><font style="color:rgb(51, 51, 51);">Notification</font></code> | <font style="color:rgb(51, 51, 51);">Claude 发出通知时</font> | <font style="color:rgb(51, 51, 51);">发送 Slack 消息、桌面通知</font> |
| <code><font style="color:rgb(51, 51, 51);">Stop</font></code> | <font style="color:rgb(51, 51, 51);">Claude 完成响应时</font> | <font style="color:rgb(51, 51, 51);">记录日志、触发下游任务</font> |

***

## <font style="color:rgb(51, 51, 51);">七、插件与 MCP 命令</font>

<font style="color:rgb(51, 51, 51);">除了自己写，还能通过</font>**<font style="color:rgb(51, 51, 51);">插件</font>**<font style="color:rgb(51, 51, 51);">和</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:rgb(51, 51, 51);">MCP 服务器</font>**<font style="color:rgb(51, 51, 51);">获取更多扩展命令。</font>

<font style="color:rgb(51, 51, 51);">命名格式：</font>

/mcp\_\_<服务器名>\_\_<命令名> \[参数]

### <font style="color:rgb(51, 51, 51);">常用 MCP 命令示例</font>

| <font style="color:rgb(255, 255, 255);">MCP 服务器</font> | <font style="color:rgb(255, 255, 255);">命令示例</font> | <font style="color:rgb(255, 255, 255);">功能</font> |
| --- | --- | --- |
| <font style="color:rgb(51, 51, 51);">GitHub</font> | <code><font style="color:rgb(51, 51, 51);">/mcp__github__list_prs</font></code> | <font style="color:rgb(51, 51, 51);">列出当前仓库的 PR</font> |
| <font style="color:rgb(51, 51, 51);">GitHub</font> | <code><font style="color:rgb(51, 51, 51);">/mcp__github__create_issue "Bug标题" high</font></code> | <font style="color:rgb(51, 51, 51);">创建 Issue</font> |
| <font style="color:rgb(51, 51, 51);">PostgreSQL</font> | <code><font style="color:rgb(51, 51, 51);">/mcp__postgres__query "SELECT * FROM users LIMIT 10"</font></code> | <font style="color:rgb(51, 51, 51);">执行 SQL 查询</font> |
| <font style="color:rgb(51, 51, 51);">Slack</font> | <code><font style="color:rgb(51, 51, 51);">/mcp__slack__send_message "#dev" "部署完成"</font></code> | <font style="color:rgb(51, 51, 51);">发送 Slack 消息</font> |
| <font style="color:rgb(51, 51, 51);">Jira</font> | <code><font style="color:rgb(51, 51, 51);">/mcp__jira__create_issue "修复登录Bug" high</font></code> | <font style="color:rgb(51, 51, 51);">创建 Jira 工单</font> |
| <font style="color:rgb(51, 51, 51);">Figma</font> | <code><font style="color:rgb(51, 51, 51);">/mcp__figma__get_component "Button"</font></code> | <font style="color:rgb(51, 51, 51);">获取 Figma 组件信息</font> |

<font style="color:rgb(51, 51, 51);">查看所有可用 MCP 命令：</font><code><font style="color:rgb(51, 51, 51);">/help</font></code><font style="color:rgb(51, 51, 51);">（MCP 命令在帮助列表底部单独分组展示）</font>

### <font style="color:rgb(51, 51, 51);">1. 插件命令</font>

<font style="color:rgb(51, 51, 51);">安装 Claude Code 插件后，会自动新增插件专属命令，格式通常是：</font>

/plugin-name:command-name  # 避免命令名冲突

<font style="color:rgb(51, 51, 51);">比如安装 Git 插件后，可能会有</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">/git:commit</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">命令，一键生成规范的 commit 信息。</font>

### <font style="color:rgb(51, 51, 51);">2. MCP 命令</font>

<font style="color:rgb(51, 51, 51);">MCP（模型上下文协议）服务器可以把外部工具（比如 GitHub、Jira）的功能变成斜杠命令，格式：</font>

/mcp\_\_<服务器名>\_\_<功能名> \[参数]

<font style="color:rgb(51, 51, 51);">示例：</font>

```plain
/mcp__github__list_prs  # 列出 GitHub 仓库的 PR
/mcp__jira__create_issue "登录按钮失效" high  # 在 Jira 创建高优先级问题
```

***

## <font style="color:rgb(51, 51, 51);">八、实用命令模板库</font>

### <font style="color:rgb(51, 51, 51);">模板概览</font>

| <font style="color:rgb(255, 255, 255);">模板名</font> | <font style="color:rgb(255, 255, 255);">文件路径</font> | <font style="color:rgb(255, 255, 255);">推荐模型</font> | <font style="color:rgb(255, 255, 255);">功能</font> |
| --- | --- | --- | --- |
| <font style="color:rgb(51, 51, 51);">智能 Git 提交</font> | <code><font style="color:rgb(51, 51, 51);">.claude/commands/commit.md</font></code> | <font style="color:rgb(51, 51, 51);">Haiku</font> | <font style="color:rgb(51, 51, 51);">检查调试残留后提交</font> |
| <font style="color:rgb(51, 51, 51);">PR 代码审查</font> | <code><font style="color:rgb(51, 51, 51);">.claude/commands/pr-review.md</font></code> | <font style="color:rgb(51, 51, 51);">Sonnet</font> | <font style="color:rgb(51, 51, 51);">全面分级审查</font> |
| <font style="color:rgb(51, 51, 51);">智能测试运行</font> | <code><font style="color:rgb(51, 51, 51);">.claude/commands/test.md</font></code> | <font style="color:rgb(51, 51, 51);">Sonnet</font> | <font style="color:rgb(51, 51, 51);">运行并自动修复失败用例</font> |
| <font style="color:rgb(51, 51, 51);">安全漏洞扫描</font> | <code><font style="color:rgb(51, 51, 51);">.claude/commands/security-scan.md</font></code> | <font style="color:rgb(51, 51, 51);">Opus</font> | <font style="color:rgb(51, 51, 51);">OWASP Top 10 扫描</font> |
| <font style="color:rgb(51, 51, 51);">API 文档生成</font> | <code><font style="color:rgb(51, 51, 51);">.claude/commands/api-docs.md</font></code> | <font style="color:rgb(51, 51, 51);">Sonnet</font> | <font style="color:rgb(51, 51, 51);">自动生成 REST API 文档</font> |
| <font style="color:rgb(51, 51, 51);">代码重构</font> | <code><font style="color:rgb(51, 51, 51);">.claude/commands/refactor.md</font></code> | <font style="color:rgb(51, 51, 51);">Sonnet</font> | <font style="color:rgb(51, 51, 51);">可读性 / DRY / 类型安全重构</font> |
| <font style="color:rgb(51, 51, 51);">文档链接检查</font> | <code><font style="color:rgb(51, 51, 51);">.claude/commands/check-links.md</font></code> | <font style="color:rgb(51, 51, 51);">Haiku</font> | <font style="color:rgb(51, 51, 51);">批量验证文档中的超链接有效性</font> |

<font style="color:rgb(51, 51, 51);">智能 Git 提交：</font>

```plain
<!-- .claude/commands/commit.md -->
---
allowed-tools: Bash(git add:*), Bash(git status:*), Bash(git diff:*), Bash(git commit:*)
argument-hint: [commit-message]
description: 检查代码质量后提交
model: claude-haiku-4-5-20251001
---

## 暂存区内容
!`git diff --cached`

提交前检查以下问题，发现问题则报告并询问是否继续：
1. 遗留的 `console.log` / `print` 调试语句
2. 未处理的 `TODO` / `FIXME` 注释
3. 大段被注释掉的代码
4. 测试文件中的 `.only` / `.skip` 标记

若无问题，使用以下信息提交：$ARGUMENTS
```

<font style="color:rgb(51, 51, 51);">PR 代码审查：</font>

```plain
<!-- .claude/commands/pr-review.md -->
---
allowed-tools: Read, Grep, Glob, Bash(git diff:*), Bash(git log:*)
description: 全面的 PR 代码审查
---

## 变更文件
!`git diff --name-only HEAD~1`

## 详细差异
!`git diff HEAD~1`

## 近期提交
!`git log --oneline -5`

按 Critical / Major / Minor 三级优先级输出审查结果，涵盖：
代码逻辑与可读性、安全漏洞、性能隐患（N+1 查询）、测试覆盖率、文档完整性
```

<font style="color:rgb(51, 51, 51);">智能测试运行：</font>

```plain
<!-- .claude/commands/test.md -->
---
allowed-tools: Bash, Read, Edit
argument-hint: [test-pattern]
description: 运行测试并自动修复失败用例
---

运行匹配 "$ARGUMENTS" 的测试：
1. 自动检测测试框架（Jest / pytest / Go test）
2. 运行指定模式的测试
3. 若有失败，分析根因并修复代码
4. 重新运行验证修复

不提供参数则运行全量测试并输出覆盖率报告。
```

<font style="color:rgb(51, 51, 51);">安全漏洞扫描：</font>

```plain
<!-- .claude/commands/security-scan.md -->
---
allowed-tools: Read, Grep, Glob
description: OWASP Top 10 安全漏洞扫描
model: claude-opus-4-6
---

以安全工程师视角审查代码库：

高危：SQL 注入、XSS、命令注入、硬编码密钥
中危：不安全的反序列化、过时依赖、敏感信息写入日志、CORS 配置过宽
低危：缺失安全响应头、错误信息暴露内部细节

输出格式：漏洞位置 + 危险级别 + 修复建议代码示例
```

<font style="color:rgb(51, 51, 51);">API 文档生成：</font>

```plain
<!-- .claude/commands/api-docs.md -->
---
allowed-tools: Read, Glob, Edit
argument-hint: [输出文件路径]
description: 自动生成 REST API 文档
---

扫描 @src/routes/ 和 @src/controllers/，为所有端点生成 Markdown 文档：
- 端点路径与 HTTP 方法
- 请求参数（Query / Body / Path）及类型
- 响应结构（成功与错误）
- 认证要求
- curl 调用示例

保存到：$ARGUMENTS（默认：docs/api.md）
```

<font style="color:rgb(51, 51, 51);">代码重构：</font>

```plain
<!-- .claude/commands/refactor.md -->
---
allowed-tools: Read, Edit, Glob
argument-hint: [目标文件或目录]
description: 代码质量重构
---

对 $ARGUMENTS 进行重构，遵循原则：
- 可读性：变量/函数命名语义化，消除魔法数字
- DRY 原则：提取重复逻辑为复用函数
- 单一职责：拆分超过 50 行的函数
- 错误处理：完善异常捕获和错误边界
- TypeScript：消除 `any` 类型，补全类型注解

重构前先输出变更计划，确认后再执行。
```

<font style="color:rgb(51, 51, 51);">文档链接检查：</font>

```plain
<!-- .claude/commands/check-links.md -->
---
allowed-tools: Read, Bash, WebFetch
argument-hint: [文档文件路径]
description: 检查文档中的链接是否全部有效
model: claude-haiku-4-5-20251001
---

读取 $ARGUMENTS 文件，提取所有超链接（http/https），逐一请求并检查响应状态码。

输出格式：
- 有效链接（200）
- 重定向链接（3xx）及目标地址
- 失效链接（4xx/5xx）及建议替代链接

最后输出汇总：共 N 个链接，M 个失效。
```

***

## <font style="color:rgb(51, 51, 51);">附：配置文件说明</font>

<font style="color:rgb(51, 51, 51);"> </font>**<font style="color:rgb(51, 51, 51);">建议：</font>**<font style="color:rgb(51, 51, 51);">将</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">CLAUDE.local.md</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">和</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">.claude/settings.local.json</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">加入</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">.gitignore</font></code><font style="color:rgb(51, 51, 51);">，避免个人偏好影响团队成员。</font>

| <font style="color:rgb(255, 255, 255);">文件 / 目录</font> | <font style="color:rgb(255, 255, 255);">作用</font> | <font style="color:rgb(255, 255, 255);">版本控制</font> |
| --- | --- | --- |
| <code><font style="color:rgb(51, 51, 51);">CLAUDE.md</font></code> | <font style="color:rgb(51, 51, 51);">项目级共享指令（技术栈、构建命令、编码规范等）</font> | <font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">纳入 git</font> |
| <code><font style="color:rgb(51, 51, 51);">CLAUDE.local.md</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(255, 255, 255);">NEW</font> | <font style="color:rgb(51, 51, 51);">个人私有指令（个人偏好，不共享给团队）</font> | <font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">加入 .gitignore</font> |
| <code><font style="color:rgb(51, 51, 51);">~/.claude/CLAUDE.md</font></code> | <font style="color:rgb(51, 51, 51);">全局指令，所有项目通用</font> | <font style="color:rgb(51, 51, 51);">—</font> |
| <code><font style="color:rgb(51, 51, 51);">.claude/settings.json</font></code> | <font style="color:rgb(51, 51, 51);">项目共享配置（工具权限、hooks 等）</font> | <font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">纳入 git</font> |
| <code><font style="color:rgb(51, 51, 51);">.claude/settings.local.json</font></code> | <font style="color:rgb(51, 51, 51);">项目个人配置（覆盖 settings.json，不共享）</font> | <font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">加入 .gitignore</font> |
| <code><font style="color:rgb(51, 51, 51);">.claude/skills/</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(255, 255, 255);">推荐</font> | <font style="color:rgb(51, 51, 51);">项目级自定义 Skills（新推荐格式）</font> | <font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">纳入 git</font> |
| <code><font style="color:rgb(51, 51, 51);">.claude/commands/</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(255, 255, 255);">旧格式</font> | <font style="color:rgb(51, 51, 51);">项目级自定义命令（旧格式，仍完全兼容）</font> | <font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">纳入 git</font> |
| <code><font style="color:rgb(51, 51, 51);">~/.claude/skills/</font></code> | <font style="color:rgb(51, 51, 51);">个人全局 Skills（跨项目通用，本地私有）</font> | <font style="color:rgb(51, 51, 51);">—</font> |

## <font style="color:rgb(51, 51, 51);">Claude Code 检查点</font>

<font style="color:rgb(51, 51, 51);">检查点是 Claude Code 的</font>**<font style="color:rgb(51, 51, 51);">代码安全回退工具</font>**<font style="color:rgb(51, 51, 51);">，能自动跟踪 Claude 对文件的编辑操作，帮你快速撤销不需要的更改，避免代码改坏后难以恢复。</font>

## <font style="color:rgb(51, 51, 51);">检查点的工作原理</font>

<font style="color:rgb(51, 51, 51);">检查点会在你使用 Claude Code 时</font>**<font style="color:rgb(51, 51, 51);">自动后台运行</font>**<font style="color:rgb(51, 51, 51);">，全程无需手动配置：</font>

1. **<font style="color:rgb(51, 51, 51);">自动创建</font>**<font style="color:rgb(51, 51, 51);">：每次发送用户提示后，都会自动创建一个检查点，记录当前的代码状态</font>
2. **<font style="color:rgb(51, 51, 51);">持久保存</font>**<font style="color:rgb(51, 51, 51);">：检查点会在会话之间保留，即使关闭会话，下次恢复后仍能访问历史检查点</font>
3. **<font style="color:rgb(51, 51, 51);">自动清理</font>**<font style="color:rgb(51, 51, 51);">：超过 30 天的检查点会自动删除（清理时间可配置）</font>

*<font style="color:rgb(44, 58, 94);">注意：仅跟踪 Claude</font>**<font style="color:rgb(44, 58, 94);"> </font>**__<font style="color:rgb(44, 58, 94);">通过文件编辑工具</font>__**<font style="color:rgb(44, 58, 94);"> </font>**<font style="color:rgb(44, 58, 94);">做出的直接修改，其他方式的更改不会被记录。</font>*

***

## <font style="color:rgb(51, 51, 51);">如何使用检查点回退更改</font>

### <font style="color:rgb(51, 51, 51);">1. 打开回退菜单</font>

<font style="color:rgb(51, 51, 51);">有两种触发方式，任选其一：</font>

* <font style="color:rgb(51, 51, 51);">快捷键：按两次</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">Esc</font></code><font style="color:rgb(51, 51, 51);">（</font><code><font style="color:rgb(51, 51, 51);">Esc</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">+</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">Esc</font></code><font style="color:rgb(51, 51, 51);">）</font>
* <font style="color:rgb(51, 51, 51);">斜杠命令：输入</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">/rewind</font></code>

### <font style="color:rgb(51, 51, 51);">2. 选择回退类型</font>

<font style="color:rgb(51, 51, 51);">打开菜单后，可根据需求选择三种回退模式：</font>

| <font style="color:rgb(255, 255, 255);">回退类型</font> | <font style="color:rgb(255, 255, 255);">效果</font> | <font style="color:rgb(255, 255, 255);">适用场景</font> |
| --- | --- | --- |
| <font style="color:rgb(51, 51, 51);">仅对话</font> | <font style="color:rgb(51, 51, 51);">回退到历史对话内容，保留当前代码更改</font> | <font style="color:rgb(51, 51, 51);">觉得对话方向跑偏，想重新提问，但代码改得没问题</font> |
| <font style="color:rgb(51, 51, 51);">仅代码</font> | <font style="color:rgb(51, 51, 51);">恢复文件到历史状态，保留当前对话</font> | <font style="color:rgb(51, 51, 51);">代码改坏了，但想继续基于当前对话调整</font> |
| <font style="color:rgb(51, 51, 51);">代码和对话</font> | <font style="color:rgb(51, 51, 51);">同时回退代码和对话到之前的状态</font> | <font style="color:rgb(51, 51, 51);">想彻底推倒重来，回到某个满意的节点</font> |

***

## <font style="color:rgb(51, 51, 51);">常见用例</font>

<font style="color:rgb(51, 51, 51);">检查点特别适合以下开发场景：</font>

1. **<font style="color:rgb(51, 51, 51);">探索多种方案</font>**<font style="color:rgb(51, 51, 51);">：尝试不同的代码实现思路，不满意就一键回退到起点，再换另一种方案</font>
2. **<font style="color:rgb(51, 51, 51);">快速修复失误</font>**<font style="color:rgb(51, 51, 51);">：当 Claude 的修改引入 bug 或破坏功能时，快速回退到修改前的可用状态</font>
3. **<font style="color:rgb(51, 51, 51);">迭代功能开发</font>**<font style="color:rgb(51, 51, 51);">：对功能做多次变体实验，随时恢复到某个稳定的中间版本</font>

***

## <font style="color:rgb(51, 51, 51);">重要限制</font>

<font style="color:rgb(51, 51, 51);">检查点是</font>**<font style="color:rgb(51, 51, 51);">临时安全网</font>**<font style="color:rgb(51, 51, 51);">，不是万能的，要注意它的边界：</font>

**<font style="color:rgb(51, 51, 51);">不跟踪 Bash 命令的更改</font>**<font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);">像</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">rm</font></code><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">mv</font></code><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">cp</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">这类通过 Bash 工具执行的文件操作，不会被检查点记录，无法回退。</font>

**<font style="color:rgb(51, 51, 51);">不跟踪外部更改</font>**<font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);">只有当前会话内 Claude 编辑过的文件才会被跟踪。你在 VS Code、终端等外部工具里手动改的文件，或者其他会话的修改，都不会被捕获。</font>

**<font style="color:rgb(51, 51, 51);">不能替代版本控制工具</font>**<font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);">检查点仅用于</font>**<font style="color:rgb(51, 51, 51);">会话级的临时回退</font>**<font style="color:rgb(51, 51, 51);">，不适合长期项目管理和团队协作。</font>

* <font style="color:rgb(51, 51, 51);">长期历史记录、分支管理 → 用 Git 等版本控制工具</font>
* <font style="color:rgb(51, 51, 51);">检查点 = 本地临时撤销，Git = 永久项目历史</font>

<font style="color:rgb(51, 51, 51);"></font>

<font style="color:rgb(51, 51, 51);"></font>

## <font style="color:rgb(51, 51, 51);">Claude Code 插件</font>

<font style="color:rgb(51, 51, 51);">插件（Plugin）是 Claude Code 中</font>**<font style="color:rgb(51, 51, 51);">最高级别的扩展机制</font>**<font style="color:rgb(51, 51, 51);">，用于将命令、代理、Skills、钩子、MCP、LSP 等能力</font>**<font style="color:rgb(51, 51, 51);">打包、版本化、共享和分发</font>**<font style="color:rgb(51, 51, 51);">。</font>

**<font style="color:rgb(51, 51, 51);">插件 = 一组可复用的 Claude Code 扩展能力集合</font>**

<font style="color:rgb(51, 51, 51);">一个插件可以包含：</font>

* <font style="color:rgb(51, 51, 51);">斜杠命令（Slash Commands）</font>
* <font style="color:rgb(51, 51, 51);">子代理（Agents）</font>
* <font style="color:rgb(51, 51, 51);">Skills（能力说明）</font>
* <font style="color:rgb(51, 51, 51);">Hooks（事件钩子）</font>
* <font style="color:rgb(51, 51, 51);">MCP 服务器（外部工具/服务）</font>
* <font style="color:rgb(51, 51, 51);">LSP 服务器（代码智能）</font>

*<font style="color:rgb(44, 58, 94);">插件的核心目标只有一个：</font>*

***<font style="color:rgb(44, 58, 94);">让 Claude Code 的能力像工具箱"一样被复用，而不是每个项目重复配置</font>***

***

## <font style="color:rgb(51, 51, 51);">插件 vs 独立配置（如何选择）</font>

<font style="color:rgb(51, 51, 51);">Claude Code 支持两种扩展方式：</font>

| <font style="color:rgb(255, 255, 255);">方式</font> | <font style="color:rgb(255, 255, 255);">命令形式</font> | <font style="color:rgb(255, 255, 255);">适合场景</font> |
| --- | --- | --- |
| **<font style="color:rgb(51, 51, 51);">独立配置</font>**<font style="color:rgb(51, 51, 51);">（</font><code><font style="color:rgb(51, 51, 51);">.claude/</font></code><br/><font style="color:rgb(51, 51, 51);">）</font> | <code><font style="color:rgb(51, 51, 51);">/hello</font></code> | <font style="color:rgb(51, 51, 51);">个人使用、单项目、快速实验</font> |
| **<font style="color:rgb(51, 51, 51);">插件</font>**<font style="color:rgb(51, 51, 51);">（</font><code><font style="color:rgb(51, 51, 51);">.claude-plugin/</font></code><br/><font style="color:rgb(51, 51, 51);">）</font> | <code><font style="color:rgb(51, 51, 51);">/plugin-name:hello</font></code> | <font style="color:rgb(51, 51, 51);">团队共享、跨项目、版本化</font> |

### <font style="color:rgb(51, 51, 51);">什么时候用独立配置？</font>

* <font style="color:rgb(51, 51, 51);">只在当前项目使用</font>
* <font style="color:rgb(51, 51, 51);">个人工作流</font>
* <font style="color:rgb(51, 51, 51);">尚未稳定的实验性配置</font>
* <font style="color:rgb(51, 51, 51);">想要简短命令名（如</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">/review</font></code><font style="color:rgb(51, 51, 51);">）</font>

### <font style="color:rgb(51, 51, 51);">什么时候用插件？</font>

* <font style="color:rgb(51, 51, 51);">要在</font>**<font style="color:rgb(51, 51, 51);">多个项目复用</font>**
* <font style="color:rgb(51, 51, 51);">要</font>**<font style="color:rgb(51, 51, 51);">分享给团队或社区</font>**
* <font style="color:rgb(51, 51, 51);">需要</font>**<font style="color:rgb(51, 51, 51);">版本控制、升级、回滚</font>**
* <font style="color:rgb(51, 51, 51);">计划通过市场分发</font>
* <font style="color:rgb(51, 51, 51);">可以接受命名空间命令（避免冲突）</font>

***<font style="color:rgb(44, 58, 94);">最佳实践：</font>***

*<font style="color:rgb(44, 58, 94);">先在</font>\_\_<font style="color:rgb(44, 58, 94);"> </font>*<code>_<font style="color:rgb(44, 58, 94);">.claude/</font>_</code>*<font style="color:rgb(44, 58, 94);"> </font>\_\_<font style="color:rgb(44, 58, 94);">中迭代 → 稳定后打包为插件</font>*

***

## <font style="color:rgb(51, 51, 51);">插件的最小结构（必须记住）</font>

```plain
my-plugin/
├── .claude-plugin/
│   └── plugin.json     # 插件清单（必需）
├── commands/           # 斜杠命令
├── agents/             # 子代理
├── skills/             # Skills
├── hooks/              # 钩子
├── .mcp.json           # MCP 配置
└── .lsp.json           # LSP 配置
```

**<font style="color:rgb(51, 51, 51);">重要规则</font>**

* <code><font style="color:rgb(51, 51, 51);">.claude-plugin/</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">目录中</font>**<font style="color:rgb(51, 51, 51);">只能放</font>\*\*\*\*<font style="color:rgb(51, 51, 51);"> </font>**<code>**<font style="color:rgb(51, 51, 51);">plugin.json</font>**</code>
* <font style="color:rgb(51, 51, 51);">其他目录必须在插件根目录</font>

***

## <font style="color:rgb(51, 51, 51);">插件清单（plugin.json）</font>

<font style="color:rgb(51, 51, 51);">插件的"身份证"，决定：</font>

* <font style="color:rgb(51, 51, 51);">插件名称</font>
* <font style="color:rgb(51, 51, 51);">命令命名空间</font>
* <font style="color:rgb(51, 51, 51);">版本</font>
* <font style="color:rgb(51, 51, 51);">作者信息</font>

<font style="color:rgb(51, 51, 51);">示例：</font>

```plain
{
  "name": "my-first-plugin",
  "description": "A greeting plugin to learn the basics",
  "version": "1.0.0",
  "author": { "name": "Your Name" }
}
```

<font style="color:rgb(51, 51, 51);">关键字段说明：</font>

| <font style="color:rgb(255, 255, 255);">字段</font> | <font style="color:rgb(255, 255, 255);">作用</font> |
| --- | --- |
| <font style="color:rgb(51, 51, 51);">name</font> | <font style="color:rgb(51, 51, 51);">唯一标识 + 命令命名空间</font> |
| <font style="color:rgb(51, 51, 51);">description</font> | <font style="color:rgb(51, 51, 51);">插件市场中展示</font> |
| <font style="color:rgb(51, 51, 51);">version</font> | <font style="color:rgb(51, 51, 51);">语义化版本控制</font> |
| <font style="color:rgb(51, 51, 51);">author</font> | <font style="color:rgb(51, 51, 51);">可选，归属说明</font> |

***

## <font style="color:rgb(51, 51, 51);">斜杠命令（最常用插件能力）</font>

### <font style="color:rgb(51, 51, 51);">1、命令定义方式</font>

* <font style="color:rgb(51, 51, 51);">位于</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">commands/</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">目录</font>
* <font style="color:rgb(51, 51, 51);">每个命令 = 一个 Markdown 文件</font>
* <font style="color:rgb(51, 51, 51);">文件名 = 命令名</font>

<font style="color:rgb(51, 51, 51);">示例：</font>

<font style="color:rgb(51, 51, 51);">commands/hello.md</font>

<font style="color:rgb(51, 51, 51);">对应命令：</font>

<font style="color:rgb(51, 51, 51);">/my-first-plugin:hello</font>

### <font style="color:rgb(51, 51, 51);">2、命令内容示例</font>

```plain
---
description: Greet the user with a friendly message
---

Greet the user warmly and ask how you can help them today.
```

### <font style="color:rgb(51, 51, 51);">3、命令参数</font>

<font style="color:rgb(51, 51, 51);">使用</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">$ARGUMENTS</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">捕获用户输入：</font>

<font style="color:rgb(51, 51, 51);">Greet the user named "$ARGUMENTS" warmly.</font>

<font style="color:rgb(51, 51, 51);">调用：</font>

<font style="color:rgb(51, 51, 51);">/my-first-plugin:hello Alex</font>

***

## <font style="color:rgb(51, 51, 51);">本地测试插件（开发必会）</font>

<font style="color:rgb(51, 51, 51);">使用</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">--plugin-dir</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">直接加载插件目录：</font>

<font style="color:rgb(51, 51, 51);">claude --plugin-dir ./my-plugin</font>

<font style="color:rgb(51, 51, 51);">特点：</font>

* <font style="color:rgb(51, 51, 51);">不需要安装</font>
* <font style="color:rgb(51, 51, 51);">修改后需重启 Claude Code</font>
* <font style="color:rgb(51, 51, 51);">支持同时加载多个插件</font>

<font style="color:rgb(51, 51, 51);">claude --plugin-dir ./plugin-a --plugin-dir ./plugin-b</font>

***

## <font style="color:rgb(51, 51, 51);">插件还能做什么</font>

| <font style="color:rgb(255, 255, 255);">能力</font> | <font style="color:rgb(255, 255, 255);">用途</font> |
| --- | --- |
| <font style="color:rgb(51, 51, 51);">Commands</font> | <font style="color:rgb(51, 51, 51);">自定义斜杠命令</font> |
| <font style="color:rgb(51, 51, 51);">Agents</font> | <font style="color:rgb(51, 51, 51);">专用子代理</font> |
| <font style="color:rgb(51, 51, 51);">Skills</font> | <font style="color:rgb(51, 51, 51);">教会 Claude 何时用某种能力</font> |
| <font style="color:rgb(51, 51, 51);">Hooks</font> | <font style="color:rgb(51, 51, 51);">自动化（写完文件后执行命令等）</font> |
| <font style="color:rgb(51, 51, 51);">MCP</font> | <font style="color:rgb(51, 51, 51);">连接外部服务（GitHub、DB、API）</font> |
| <font style="color:rgb(51, 51, 51);">LSP</font> | <font style="color:rgb(51, 51, 51);">代码智能（跳转、类型检查）</font> |

***

## <font style="color:rgb(51, 51, 51);">插件市场（Plugin Marketplace）</font>

<font style="color:rgb(51, 51, 51);">插件通过</font>**<font style="color:rgb(51, 51, 51);">市场</font>**<font style="color:rgb(51, 51, 51);">分发，本质是一个插件目录仓库。</font>

### <font style="color:rgb(51, 51, 51);">官方市场</font>

* <font style="color:rgb(51, 51, 51);">默认已添加</font>
* <font style="color:rgb(51, 51, 51);">运行</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">/plugin</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">→</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:rgb(51, 51, 51);">Discover</font>**

![1783654095835-9934117a-090b-415a-aabd-740779f4c662.png](./img/wf9R51v5S5sXlvV1/1783654095835-9934117a-090b-415a-aabd-740779f4c662-372117.png)

<font style="color:rgb(51, 51, 51);">安装插件：</font>

<font style="color:rgb(51, 51, 51);">/plugin install plugin-name@claude-plugins-official</font>

***

## <font style="color:rgb(51, 51, 51);">插件安装范围</font>

| <font style="color:rgb(255, 255, 255);">范围</font> | <font style="color:rgb(255, 255, 255);">说明</font> |
| --- | --- |
| <font style="color:rgb(51, 51, 51);">用户范围</font> | <font style="color:rgb(51, 51, 51);">仅你自己，所有项目</font> |
| <font style="color:rgb(51, 51, 51);">项目范围</font> | <font style="color:rgb(51, 51, 51);">当前仓库，团队共享</font> |
| <font style="color:rgb(51, 51, 51);">本地范围</font> | <font style="color:rgb(51, 51, 51);">当前仓库，仅你</font> |

<font style="color:rgb(51, 51, 51);">推荐：</font>

* <font style="color:rgb(51, 51, 51);">团队工具 →</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:rgb(51, 51, 51);">项目范围</font>**
* <font style="color:rgb(51, 51, 51);">个人效率工具 →</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:rgb(51, 51, 51);">用户范围</font>**

***

## <font style="color:rgb(51, 51, 51);">典型插件分类</font>

### <font style="color:rgb(51, 51, 51);">1、代码智能（LSP）</font>

* <font style="color:rgb(51, 51, 51);">TypeScript、Python、Go、Rust 等</font>
* <font style="color:rgb(51, 51, 51);">提供跳转定义、引用、类型错误</font>

<font style="color:rgb(51, 51, 51);">需要本地安装对应语言服务器</font>

### <font style="color:rgb(51, 51, 51);">2、外部集成（MCP）</font>

* <font style="color:rgb(51, 51, 51);">GitHub / GitLab</font>
* <font style="color:rgb(51, 51, 51);">Jira / Notion</font>
* <font style="color:rgb(51, 51, 51);">Slack / Figma</font>
* <font style="color:rgb(51, 51, 51);">Vercel / Supabase</font>

*<font style="color:rgb(44, 58, 94);">本质：</font>\_\_**<font style="color:rgb(44, 58, 94);">插件 = MCP 服务器 + 配置</font>***

### <font style="color:rgb(51, 51, 51);">3、开发工作流</font>

* <font style="color:rgb(51, 51, 51);">Git 提交、PR</font>
* <font style="color:rgb(51, 51, 51);">代码审查代理</font>
* <font style="color:rgb(51, 51, 51);">插件开发工具</font>

***

## <font style="color:rgb(51, 51, 51);">插件管理常用命令</font>

```plain
/plugin                # 打开插件管理器
/plugin install         # 安装插件
/plugin uninstall       # 卸载
/plugin enable/disable  # 启用 / 禁用
/plugin marketplace add # 添加市场
/plugin marketplace rm  # 移除市场
```

***

## <font style="color:rgb(51, 51, 51);">从</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">.claude/</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">迁移到插件（核心思路）</font>

| <font style="color:rgb(255, 255, 255);">原来</font> | <font style="color:rgb(255, 255, 255);">迁移后</font> |
| --- | --- |
| <code><font style="color:rgb(51, 51, 51);">.claude/commands</font></code> | <code><font style="color:rgb(51, 51, 51);">plugin/commands</font></code> |
| <code><font style="color:rgb(51, 51, 51);">.claude/agents</font></code> | <code><font style="color:rgb(51, 51, 51);">plugin/agents</font></code> |
| <code><font style="color:rgb(51, 51, 51);">settings.json hooks</font></code> | <code><font style="color:rgb(51, 51, 51);">plugin/hooks/hooks.json</font></code> |

<font style="color:rgb(51, 51, 51);">迁移后：</font>

* <font style="color:rgb(51, 51, 51);">插件版本优先生效</font>
* <font style="color:rgb(51, 51, 51);">可删除旧</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">.claude/</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">配置避免重复</font>

***

## <font style="color:rgb(51, 51, 51);">什么时候你一定要用插件？</font>

* <font style="color:rgb(51, 51, 51);">你已经有</font>**<font style="color:rgb(51, 51, 51);">稳定的 Claude 工作流</font>**
* <font style="color:rgb(51, 51, 51);">你在</font>**<font style="color:rgb(51, 51, 51);">反复复制</font>\*\*\*\*<font style="color:rgb(51, 51, 51);"> </font>**<code>**<font style="color:rgb(51, 51, 51);">.claude/</font>**</code>
* <font style="color:rgb(51, 51, 51);">团队成员开始问你："这个怎么配置？"</font>
* <font style="color:rgb(51, 51, 51);">你希望 Claude 像 IDE 插件一样可控</font>

***<font style="color:rgb(44, 58, 94);">插件，是 Claude Code 从"个人 AI 助手"走向"工程化工具"的分水岭</font>***

# Claude Code 并行任务与 Git 工作流工程化实战

## <font style="color:rgb(51, 51, 51);">Claude Code 并行任务</font>

<font style="color:rgb(51, 51, 51);">Claude Code 提供了多种并行执行任务的机制，让你可以同时处理多个工作项，显著提升开发效率。本章将介绍三种主要的并行化方案：Subagents（子代理）、Agent Teams（代理团队）和 Git Worktree（Git 工作树），帮助你根据不同的使用场景选择最合适的方式。</font>

***

## <font style="color:rgb(51, 51, 51);">并行任务概述</font>

<font style="color:rgb(51, 51, 51);">当面对复杂任务时，单个 Claude 实例可能会力不从心——上下文过长、响应变慢、任务交织。Claude Code 提供了三层并行化机制，满足不同复杂度和协作需求：</font>

| <font style="color:rgb(255, 255, 255);">机制</font> | <font style="color:rgb(255, 255, 255);">适用场景</font> | <font style="color:rgb(255, 255, 255);">协作方式</font> | <font style="color:rgb(255, 255, 255);">复杂度</font> |
| --- | --- | --- | --- |
| **<font style="color:rgb(51, 51, 51);">Subagents</font>** | <font style="color:rgb(51, 51, 51);">专注型任务，只需关注结果</font> | <font style="color:rgb(51, 51, 51);">单向汇报（结果返回主代理）</font> | <font style="color:rgb(51, 51, 51);">低</font> |
| **<font style="color:rgb(51, 51, 51);">Agent Teams</font>** | <font style="color:rgb(51, 51, 51);">需要讨论与协作的复杂工作</font> | <font style="color:rgb(51, 51, 51);">多向通信（队友直接互发消息）</font> | <font style="color:rgb(51, 51, 51);">中</font> |
| **<font style="color:rgb(51, 51, 51);">Git Worktree</font>** | <font style="color:rgb(51, 51, 51);">多个任务需要隔离的代码环境</font> | <font style="color:rgb(51, 51, 51);">完全独立（各自的工作目录）</font> | <font style="color:rgb(51, 51, 51);">中</font> |

***<font style="color:rgb(44, 58, 94);">选择建议：</font>***

* <font style="color:rgb(44, 58, 94);">只需并行处理、相互独立的子任务 → 使用</font><font style="color:rgb(44, 58, 94);"> </font>**<font style="color:rgb(44, 58, 94);">Subagents</font>**
* <font style="color:rgb(44, 58, 94);">需要多个 Agent 相互讨论、协调工作 → 使用</font><font style="color:rgb(44, 58, 94);"> </font>**<font style="color:rgb(44, 58, 94);">Agent Teams</font>**
* <font style="color:rgb(44, 58, 94);">多个任务需要操作同一仓库的不同分支 → 使用</font><font style="color:rgb(44, 58, 94);"> </font>**<font style="color:rgb(44, 58, 94);">Git Worktree</font>**

***

## <font style="color:rgb(51, 51, 51);">Subagents（子代理）</font>

### <font style="color:rgb(51, 51, 51);">什么是 Subagents</font>

<font style="color:rgb(51, 51, 51);">Subagent 是一个独立运行的 Claude 实例，它有自己的上下文和任务焦点。主 Claude 可以创建多个 Subagent，每个 Subagent 负责一个特定的子任务：</font>

```plain
┌─────────────────────────────────────────────────────────┐
│                    主 Claude                            │
│                    (协调者)                              │
└─────────────────────────────────────────────────────────┘
                        │
                        ▼
        ┌───────────────┼───────────────┐
        ▼               ▼               ▼
┌──────────┐    ┌──────────┐    ┌──────────┐
│ Agent A  │    │ Agent B  │    │ Agent C  │
│ 代码审查  │    │ 测试生成  │    │ 文档编写  │
└──────────┘    └──────────┘    └──────────┘
        │               │               │
        └───────────────┴───────────────┘
                        │
                        ▼
                 返回结果给主代理
```

<font style="color:rgb(51, 51, 51);">Subagent 最多可并行运行 49 个，完全满足大多数并行处理需求。</font>

### <font style="color:rgb(51, 51, 51);">内置 Subagents</font>

<font style="color:rgb(51, 51, 51);">Claude Code 预置了以下内置 Subagent：</font>

| <font style="color:rgb(255, 255, 255);">Agent</font> | <font style="color:rgb(255, 255, 255);">模型</font> | <font style="color:rgb(255, 255, 255);">工具</font> | <font style="color:rgb(255, 255, 255);">用途</font> |
| --- | --- | --- | --- |
| <code><font style="color:rgb(51, 51, 51);">Explore</font></code> | <font style="color:rgb(51, 51, 51);">Haiku（快速、低延迟）</font> | <font style="color:rgb(51, 51, 51);">只读工具</font> | <font style="color:rgb(51, 51, 51);">文件发现、代码搜索、代码库探索</font> |
| <code><font style="color:rgb(51, 51, 51);">Plan</font></code> | <font style="color:rgb(51, 51, 51);">继承主对话</font> | <font style="color:rgb(51, 51, 51);">只读工具</font> | <font style="color:rgb(51, 51, 51);">规划模式下的代码库研究</font> |
| <code><font style="color:rgb(51, 51, 51);">General-purpose</font></code> | <font style="color:rgb(51, 51, 51);">继承主对话</font> | <font style="color:rgb(51, 51, 51);">所有工具</font> | <font style="color:rgb(51, 51, 51);">复杂研究、多步骤操作、代码修改</font> |
| <code><font style="color:rgb(51, 51, 51);">statusline-setup</font></code> | <font style="color:rgb(51, 51, 51);">Sonnet</font> | <font style="color:rgb(51, 51, 51);">—</font> | <font style="color:rgb(51, 51, 51);">运行</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">/statusline</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">配置状态行</font> |
| <code><font style="color:rgb(51, 51, 51);">Claude Code Guide</font></code> | <font style="color:rgb(51, 51, 51);">Haiku</font> | <font style="color:rgb(51, 51, 51);">—</font> | <font style="color:rgb(51, 51, 51);">回答 Claude Code 功能问题</font> |

### <font style="color:rgb(51, 51, 51);">创建 Subagent</font>

#### <font style="color:rgb(51, 51, 51);">方式一：使用 /agents 命令</font>

<font style="color:rgb(51, 51, 51);">运行</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">/agents</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">命令，按提示创建新的 Subagent：</font>

/agents

<font style="color:rgb(51, 51, 51);">选择</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:rgb(51, 51, 51);">Create new agent</font>**<font style="color:rgb(51, 51, 51);">，然后选择保存位置，描述功能后让 Claude 生成配置。</font>

#### <font style="color:rgb(51, 51, 51);">方式二：手动创建 Subagent 文件</font>

<font style="color:rgb(51, 51, 51);">Subagent 文件使用 YAML frontmatter 进行配置，然后是 Markdown 中的系统提示：</font>

**<font style="color:rgb(97, 127, 16);">实例</font>**

<font style="color:cyan;">---</font><font style="color:green;">\
</font><font style="color:green;">name</font>**<font style="color:brown;">:</font>\*\*\*\*<font style="color:brown;"> </font>**<font style="color:rgb(51, 51, 51);">code-reviewer</font><font style="color:green;">\
</font><font style="color:green;">description</font>**<font style="color:brown;">:</font>\*\*\*\*<font style="color:brown;"> </font>**<font style="color:rgb(51, 51, 51);">Reviews code for quality and best practices</font><font style="color:green;">\
</font><font style="color:green;">tools</font>**<font style="color:brown;">:</font>\*\*\*\*<font style="color:brown;"> </font>**<font style="color:rgb(51, 51, 51);">Read, Glob, Grep</font><font style="color:green;">\
</font><font style="color:green;">model</font>**<font style="color:brown;">:</font>\*\*\*\*<font style="color:brown;"> </font>**<font style="color:rgb(51, 51, 51);">sonnet\
</font><font style="color:cyan;">---</font><font style="color:rgb(51, 51, 51);">

</font><font style="color:rgb(51, 51, 51);">You are a code reviewer. When invoked, analyze the code and provide\
</font><font style="color:rgb(51, 51, 51);">specific, actionable feedback on quality, security, and best practices.</font>

### <font style="color:rgb(51, 51, 51);">Subagent 配置字段</font>

| <font style="color:rgb(255, 255, 255);">字段</font> | <font style="color:rgb(255, 255, 255);">必需</font> | <font style="color:rgb(255, 255, 255);">描述</font> |
| --- | --- | --- |
| <code><font style="color:rgb(51, 51, 51);">name</font></code> | <font style="color:rgb(51, 51, 51);">是</font> | <font style="color:rgb(51, 51, 51);">唯一标识符，使用小写字母和连字符</font> |
| <code><font style="color:rgb(51, 51, 51);">description</font></code> | <font style="color:rgb(51, 51, 51);">是</font> | <font style="color:rgb(51, 51, 51);">描述 Claude 何时应该委托给此 Subagent</font> |
| <code><font style="color:rgb(51, 51, 51);">tools</font></code> | <font style="color:rgb(51, 51, 51);">否</font> | <font style="color:rgb(51, 51, 51);">Subagent 可以使用的工具列表</font> |
| <code><font style="color:rgb(51, 51, 51);">disallowedTools</font></code> | <font style="color:rgb(51, 51, 51);">否</font> | <font style="color:rgb(51, 51, 51);">要拒绝的工具</font> |
| <code><font style="color:rgb(51, 51, 51);">model</font></code> | <font style="color:rgb(51, 51, 51);">否</font> | <font style="color:rgb(51, 51, 51);">使用的模型：sonnet、opus、haiku 或 inherit</font> |
| <code><font style="color:rgb(51, 51, 51);">permissionMode</font></code> | <font style="color:rgb(51, 51, 51);">否</font> | <font style="color:rgb(51, 51, 51);">权限模式：default、acceptEdits、auto、dontAsk、bypassPermissions、plan</font> |
| <code><font style="color:rgb(51, 51, 51);">maxTurns</font></code> | <font style="color:rgb(51, 51, 51);">否</font> | <font style="color:rgb(51, 51, 51);">Subagent 停止前的最大代理轮数</font> |
| <code><font style="color:rgb(51, 51, 51);">skills</font></code> | <font style="color:rgb(51, 51, 51);">否</font> | <font style="color:rgb(51, 51, 51);">启动时加载的 skills</font> |
| <code><font style="color:rgb(51, 51, 51);">mcpServers</font></code> | <font style="color:rgb(51, 51, 51);">否</font> | <font style="color:rgb(51, 51, 51);">对此 Subagent 可用的 MCP 服务器</font> |
| <code><font style="color:rgb(51, 51, 51);">memory</font></code> | <font style="color:rgb(51, 51, 51);">否</font> | <font style="color:rgb(51, 51, 51);">持久内存范围：user、project 或 local</font> |
| <code><font style="color:rgb(51, 51, 51);">background</font></code> | <font style="color:rgb(51, 51, 51);">否</font> | <font style="color:rgb(51, 51, 51);">是否始终作为后台任务运行</font> |
| <code><font style="color:rgb(51, 51, 51);">isolation</font></code> | <font style="color:rgb(51, 51, 51);">否</font> | <font style="color:rgb(51, 51, 51);">设置为 worktree 在临时 git worktree 中运行</font> |

### <font style="color:rgb(51, 51, 51);">控制 Subagent 能力</font>

#### <font style="color:rgb(51, 51, 51);">工具限制</font>

**<font style="color:rgb(97, 127, 16);">实例</font>**

<font style="color:blue;"># 只允许特定工具</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:cyan;">---</font><font style="color:green;">\
</font><font style="color:green;">name</font>**<font style="color:brown;">:</font>\*\*\*\*<font style="color:brown;"> </font>**<font style="color:rgb(51, 51, 51);">safe-researcher</font><font style="color:green;">\
</font><font style="color:green;">description</font>**<font style="color:brown;">:</font>\*\*\*\*<font style="color:brown;"> </font>**<font style="color:rgb(51, 51, 51);">Research agent with restricted capabilities</font><font style="color:green;">\
</font><font style="color:green;">tools</font>**<font style="color:brown;">:</font>\*\*\*\*<font style="color:brown;"> </font>**<font style="color:rgb(51, 51, 51);">Read, Grep, Glob, Bash\
</font><font style="color:cyan;">---</font><font style="color:rgb(51, 51, 51);">

</font><font style="color:blue;"># 排除特定工具</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:cyan;">---</font><font style="color:green;">\
</font><font style="color:green;">name</font>**<font style="color:brown;">:</font>\*\*\*\*<font style="color:brown;"> </font>**<font style="color:rgb(51, 51, 51);">no-writes</font><font style="color:green;">\
</font><font style="color:green;">description</font>**<font style="color:brown;">:</font>\*\*\*\*<font style="color:brown;"> </font>**<font style="color:rgb(51, 51, 51);">Inherits every tool except file writes</font><font style="color:green;">\
</font><font style="color:green;">disallowedTools</font>**<font style="color:brown;">:</font>\*\*\*\*<font style="color:brown;"> </font>**<font style="color:rgb(51, 51, 51);">Write, Edit\
</font><font style="color:cyan;">---</font>

#### <font style="color:rgb(51, 51, 51);">模型选择</font>

**<font style="color:rgb(97, 127, 16);">实例</font>**

<font style="color:blue;"># 使用 Haiku（快速、便宜）</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:cyan;">---</font><font style="color:green;">\
</font><font style="color:green;">name</font>**<font style="color:brown;">:</font>\*\*\*\*<font style="color:brown;"> </font>**<font style="color:rgb(51, 51, 51);">quick-searcher</font><font style="color:green;">\
</font><font style="color:green;">description</font>**<font style="color:brown;">:</font>\*\*\*\*<font style="color:brown;"> </font>**<font style="color:rgb(51, 51, 51);">Quick file search</font><font style="color:green;">\
</font><font style="color:green;">model</font>**<font style="color:brown;">:</font>\*\*\*\*<font style="color:brown;"> </font>**<font style="color:rgb(51, 51, 51);">haiku\
</font><font style="color:cyan;">---</font><font style="color:rgb(51, 51, 51);">

</font><font style="color:blue;"># 使用 Opus（强大、昂贵）</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:cyan;">---</font><font style="color:green;">\
</font><font style="color:green;">name</font>**<font style="color:brown;">:</font>\*\*\*\*<font style="color:brown;"> </font>**<font style="color:rgb(51, 51, 51);">deep-analyst</font><font style="color:green;">\
</font><font style="color:green;">description</font>**<font style="color:brown;">:</font>\*\*\*\*<font style="color:brown;"> </font>**<font style="color:rgb(51, 51, 51);">Deep code analysis</font><font style="color:green;">\
</font><font style="color:green;">model</font>**<font style="color:brown;">:</font>\*\*\*\*<font style="color:brown;"> </font>**<font style="color:rgb(51, 51, 51);">opus\
</font><font style="color:cyan;">---</font><font style="color:rgb(51, 51, 51);">

</font><font style="color:blue;"># 继承主对话模型</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:cyan;">---</font><font style="color:green;">\
</font><font style="color:green;">name</font>**<font style="color:brown;">:</font>\*\*\*\*<font style="color:brown;"> </font>**<font style="color:rgb(51, 51, 51);">general-purpose</font><font style="color:green;">\
</font><font style="color:green;">model</font>**<font style="color:brown;">:</font>\*\*\*\*<font style="color:brown;"> </font>**<font style="color:rgb(51, 51, 51);">inherit\
</font><font style="color:cyan;">---</font>

### <font style="color:rgb(51, 51, 51);">调用 Subagent</font>

#### <font style="color:rgb(51, 51, 51);">方式一：自然语言</font>

Use the test-runner subagent to fix failing tests

#### <font style="color:rgb(51, 51, 51);">方式二：@-mention</font>

@"code-reviewer (agent)" look at the auth changes

#### <font style="color:rgb(51, 51, 51);">方式三：命令行启动</font>

claude --agent code-reviewer

### <font style="color:rgb(51, 51, 51);">前台与后台运行</font>

* **<font style="color:rgb(51, 51, 51);">前台 Subagent</font>**<font style="color:rgb(51, 51, 51);">：阻塞主对话直到完成</font>
* **<font style="color:rgb(51, 51, 51);">后台 Subagent</font>**<font style="color:rgb(51, 51, 51);">：并发运行，可按</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">Ctrl+B</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">切换</font>

***

## <font style="color:rgb(51, 51, 51);">Agent Teams（代理团队）</font>

### <font style="color:rgb(51, 51, 51);">什么是 Agent Teams</font>

<font style="color:rgb(51, 51, 51);">Agent Teams 可以让你协调多个 Claude Code 实例一起工作。想象一下，你同时开启 4 个 Claude 会话（ABCD），其中一个充当团队负责人（Leader），负责协调工作、分配任务并整合结果。其他三个成员各自独立工作，拥有各自的上下文窗口，同时还能直接相互沟通。</font>

### <font style="color:rgb(51, 51, 51);">Subagents vs Agent Teams</font>

| <font style="color:rgb(255, 255, 255);">特性</font> | <font style="color:rgb(255, 255, 255);">Subagents</font> | <font style="color:rgb(255, 255, 255);">Agent Teams</font> |
| --- | --- | --- |
| **<font style="color:rgb(51, 51, 51);">上下文</font>** | <font style="color:rgb(51, 51, 51);">自己的上下文窗口；结果返回给调用者</font> | <font style="color:rgb(51, 51, 51);">自己的上下文窗口；完全独立</font> |
| **<font style="color:rgb(51, 51, 51);">通信</font>** | <font style="color:rgb(51, 51, 51);">仅将结果汇报给主代理</font> | <font style="color:rgb(51, 51, 51);">队友之间直接互发消息</font> |
| **<font style="color:rgb(51, 51, 51);">协调</font>** | <font style="color:rgb(51, 51, 51);">主代理负责管理所有工作</font> | <font style="color:rgb(51, 51, 51);">共享任务列表，支持自我协调</font> |
| **<font style="color:rgb(51, 51, 51);">最适合</font>** | <font style="color:rgb(51, 51, 51);">只需关注结果的专注型任务</font> | <font style="color:rgb(51, 51, 51);">需要讨论与协作的复杂工作</font> |
| **<font style="color:rgb(51, 51, 51);">Token 成本</font>** | <font style="color:rgb(51, 51, 51);">较低：结果汇总回主上下文</font> | <font style="color:rgb(51, 51, 51);">较高：每位队友都是独立的 Claude 实例</font> |

<font style="color:rgb(51, 51, 51);">简单来说：</font>**<font style="color:rgb(51, 51, 51);">Subagent 是打工人向老板汇报，Agent Teams 是平等协作的项目组</font>**<font style="color:rgb(51, 51, 51);">。</font>

### <font style="color:rgb(51, 51, 51);">启用 Agent Teams</font>

<font style="color:rgb(51, 51, 51);">Agent Teams 默认禁用。需要在</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">settings.json</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">中添加：</font>

**<font style="color:rgb(97, 127, 16);">实例</font>**

<font style="color:rgb(0, 153, 0);">{</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"env"</font><font style="color:rgb(51, 153, 51);">:</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">{</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"CLAUDE_CODE_EXPERIMENTAL_AGENT_TEAMS"</font><font style="color:rgb(51, 153, 51);">:</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"1"</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">}</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(0, 153, 0);">}</font>

<font style="color:rgb(51, 51, 51);">或设置环境变量：</font>

export CLAUDE_CODE_EXPERIMENTAL_AGENT_TEAMS=1

***<font style="color:rgb(44, 58, 94);">要求</font>**\_\_<font style="color:rgb(44, 58, 94);">：Claude Code v2.1.32 或更高版本</font>*

### <font style="color:rgb(51, 51, 51);">启动 Agent Team</font>

<font style="color:rgb(51, 51, 51);">启用后，用自然语言描述任务和团队结构：</font>

**<font style="color:rgb(97, 127, 16);">实例</font>**

<font style="color:rgb(51, 51, 51);">I'm designing a CLI tool that helps developers track TODO comments across\
</font><font style="color:rgb(51, 51, 51);">their codebase. Create an agent team to explore this from different angles: one\
</font><font style="color:rgb(51, 51, 51);">teammate on UX, one on technical architecture, one playing devil's advocate.</font>

### <font style="color:rgb(51, 51, 51);">控制 Agent Team</font>

#### <font style="color:rgb(51, 51, 51);">显示模式</font>

* **<font style="color:rgb(51, 51, 51);">In-process</font>**<font style="color:rgb(51, 51, 51);">：所有队友在主终端内运行，使用</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">Shift+Down</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">循环浏览队友</font>
* **<font style="color:rgb(51, 51, 51);">Split panes</font>**<font style="color:rgb(51, 51, 51);">：每个队友获得自己的 tmux/iTerm2 窗格</font>

**<font style="color:rgb(97, 127, 16);">实例</font>**

<font style="color:rgb(0, 153, 0);">{</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"teammateMode"</font><font style="color:rgb(51, 153, 51);">:</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"in-process"</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(0, 153, 0);">}</font>

#### <font style="color:rgb(51, 51, 51);">指定队友数量和模型</font>

```plain
Create a team with 4 teammates to refactor these modules in parallel.
Use Sonnet for each teammate.
```

#### <font style="color:rgb(51, 51, 51);">任务分配</font>

* <font style="color:rgb(51, 51, 51);">负责人可显式分配任务</font>
* <font style="color:rgb(51, 51, 51);">队友可自我认领未分配、未阻止的任务</font>
* <font style="color:rgb(51, 51, 51);">任务有三种状态：待处理、进行中、已完成</font>

#### <font style="color:rgb(51, 51, 51);">与队友交互</font>

* **<font style="color:rgb(51, 51, 51);">In-process</font>**<font style="color:rgb(51, 51, 51);">：</font><code><font style="color:rgb(51, 51, 51);">Shift+Down</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">循环浏览 → 输入消息 →</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">Enter</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">查看 →</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">Escape</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">中断</font>
* **<font style="color:rgb(51, 51, 51);">Split-pane</font>**<font style="color:rgb(51, 51, 51);">：点击队友窗格直接交互</font>

#### <font style="color:rgb(51, 51, 51);">关闭队友</font>

Ask the researcher teammate to shut down

### <font style="color:rgb(51, 51, 51);">Agent Teams 架构</font>

| <font style="color:rgb(255, 255, 255);">组件</font> | <font style="color:rgb(255, 255, 255);">角色</font> |
| --- | --- |
| **<font style="color:rgb(51, 51, 51);">Team Lead</font>** | <font style="color:rgb(51, 51, 51);">创建团队、生成队友并协调工作的主 Claude Code 会话</font> |
| **<font style="color:rgb(51, 51, 51);">Teammates</font>** | <font style="color:rgb(51, 51, 51);">各自处理分配任务的独立 Claude Code 实例</font> |
| **<font style="color:rgb(51, 51, 51);">Task List</font>** | <font style="color:rgb(51, 51, 51);">队友认领和完成的共享工作项列表</font> |
| **<font style="color:rgb(51, 51, 51);">Mailbox</font>** | <font style="color:rgb(51, 51, 51);">代理之间通信的消息系统</font> |

**<font style="color:rgb(51, 51, 51);">存储位置：</font>**

* <font style="color:rgb(51, 51, 51);">Team config:</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">~/.claude/teams/{team-name}/config.json</font></code>
* <font style="color:rgb(51, 51, 51);">Task list:</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">~/.claude/tasks/{team-name}/</font></code>

***

## <font style="color:rgb(51, 51, 51);">Git Worktree 支持</font>

### <font style="color:rgb(51, 51, 51);">问题背景</font>

<font style="color:rgb(51, 51, 51);">多个 Agent 同时干活时，可能会"打架"。想象一下这个场景：你让 Agent A 去重构数据库模块，让 Agent B 去修复登录页面的 bug。两个任务看起来互不相关，但它们都在同一个代码仓库、同一分支上工作。Agent A 正在修改</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">utils.py</font></code><font style="color:rgb(51, 51, 51);">，Agent B 也在修改</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">utils.py</font></code><font style="color:rgb(51, 51, 51);">。一个保存了一个版本，另一个覆盖了不同的版本，最终导致冲突、报错，甚至数据丢失。</font>

<font style="color:rgb(51, 51, 51);">这不是 AI 的问题，这是底层 Git 仓库结构的限制。</font>

### <font style="color:rgb(51, 51, 51);">什么是 Git Worktree</font>

<font style="color:rgb(51, 51, 51);">Git Worktree 是 Git 的一个功能，允许你在同一个仓库上挂载多个独立的工作目录。每个工作目录有自己的分支、自己的 HEAD、自己的暂存区，但共用同一个</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">.git</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">数据库（历史记录、对象存储）。</font>

**<font style="color:rgb(97, 127, 16);">类比</font>**

<font style="color:rgb(51, 51, 51);">日常生活比喻："同一家公司（主仓库）有多个办公室（worktree），\
</font><font style="color:rgb(51, 51, 51);">每个办公室有不同的团队（Agent），各自处理不同的项目（分支），\
</font><font style="color:rgb(51, 51, 51);">但都共享公司的数据库（.git）和历史记录。"</font>

### <font style="color:rgb(51, 51, 51);">使用 Git Worktree</font>

#### <font style="color:rgb(51, 51, 51);">命令行启动</font>

```plain
# 创建 feature-auth 分支的工作树
claude -w feature-auth

# 同时创建 tmux 会话
claude -w feature-auth --tmux

# 使用传统 tmux
claude -w feature-auth --tmux=classic
```

#### <font style="color:rgb(51, 51, 51);">CLI 参数</font>

| <font style="color:rgb(255, 255, 255);">参数</font> | <font style="color:rgb(255, 255, 255);">描述</font> | <font style="color:rgb(255, 255, 255);">示例</font> |
| --- | --- | --- |
| <code><font style="color:rgb(51, 51, 51);">--worktree</font></code><br/><font style="color:rgb(51, 51, 51);">,</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">-w</font></code> | <font style="color:rgb(51, 51, 51);">在隔离的 git worktree 中启动 Claude</font> | <code><font style="color:rgb(51, 51, 51);">claude -w feature-auth</font></code> |
| <code><font style="color:rgb(51, 51, 51);">--tmux</font></code> | <font style="color:rgb(51, 51, 51);">为 worktree 创建 tmux 会话</font> | <code><font style="color:rgb(51, 51, 51);">claude -w feature-auth --tmux</font></code> |

<font style="color:rgb(51, 51, 51);">Worktree 创建位置：</font><code><font style="color:rgb(51, 51, 51);"><repo>/.claude/worktrees/<name></font></code>

#### <font style="color:rgb(51, 51, 51);">桌面端支持</font>

<font style="color:rgb(51, 51, 51);">在 Claude 桌面端应用中，进入 Code 选项卡，直接勾选 worktree mode 即可开启工作区模式。</font>

### <font style="color:rgb(51, 51, 51);">Subagent + Worktree 隔离</font>

<font style="color:rgb(51, 51, 51);">可以让自定义 Subagent 始终在自己的 worktree 中运行：</font>

**<font style="color:rgb(97, 127, 16);">实例</font>**

<font style="color:cyan;">---</font><font style="color:green;">\
</font><font style="color:green;">name</font>**<font style="color:brown;">:</font>\*\*\*\*<font style="color:brown;"> </font>**<font style="color:rgb(51, 51, 51);">background-refactorer</font><font style="color:green;">\
</font><font style="color:green;">description</font>**<font style="color:brown;">:</font>\*\*\*\*<font style="color:brown;"> </font>**<font style="color:rgb(51, 51, 51);">Background refactoring agent</font><font style="color:green;">\
</font><font style="color:green;">isolation</font>**<font style="color:brown;">:</font>\*\*\*\*<font style="color:brown;"> </font>**<font style="color:rgb(51, 51, 51);">worktree\
</font><font style="color:cyan;">---</font>

***

## <font style="color:rgb(51, 51, 51);">使用示例</font>

### <font style="color:rgb(51, 51, 51);">示例一：并行代码审查</font>

## <font style="color:rgb(97, 127, 16);">使用 Subagent</font>

<font style="color:rgb(51, 51, 51);"># 让多个 Subagent 同时审查代码的不同方面\
</font><font style="color:rgb(51, 51, 51);">Use the security-reviewer subagent to check for security issues\
</font><font style="color:rgb(51, 51, 51);">Use the performance-reviewer subagent to analyze performance impact\
</font><font style="color:rgb(51, 51, 51);">Use the test-coverage subagent to validate test coverage</font>

## <font style="color:rgb(97, 127, 16);">使用 Agent Teams</font>

<font style="color:rgb(51, 51, 51);">Create an agent team to review PR #142. Spawn three reviewers:\
</font><font style="color:rgb(51, 51, 51);">- One focused on security implications\
</font><font style="color:rgb(51, 51, 51);">- One checking performance impact\
</font><font style="color:rgb(51, 51, 51);">- One validating test coverage\
</font><font style="color:rgb(51, 51, 51);">Have them each review and report findings.</font>

### <font style="color:rgb(51, 51, 51);">示例二：并行研究</font>

Research the authentication, database, and API modules in parallel using separate subagents

### <font style="color:rgb(51, 51, 51);">示例三：使用竞争假设进行调查</font>

**<font style="color:rgb(97, 127, 16);">实例</font>**

<font style="color:rgb(51, 51, 51);">Users report the app exits after one message instead of staying connected.\
</font><font style="color:rgb(51, 51, 51);">Spawn 5 agent teammates to investigate different hypotheses. Have them talk to\
</font><font style="color:rgb(51, 51, 51);">each other to try to disprove each other's theories, like a scientific\
</font><font style="color:rgb(51, 51, 51);">debate. Update the findings doc with whatever consensus emerges.</font>

### <font style="color:rgb(51, 51, 51);">示例四：多分支开发</font>

```plain
# 终端 1：重构用户模块
claude -w feature/user-refactor

# 终端 2：修复登录 bug
claude -w bugfix/login-issue

# 终端 3：开发新功能
claude -w feature/new-dashboard
```

### <font style="color:rgb(51, 51, 51);">示例五：链接 Subagent</font>

Use the code-reviewer subagent to find performance issues, then use the optimizer subagent to fix them

***

## <font style="color:rgb(51, 51, 51);">最佳实践</font>

### <font style="color:rgb(51, 51, 51);">Subagent 最佳实践</font>

1. **<font style="color:rgb(51, 51, 51);">保持专注</font>**<font style="color:rgb(51, 51, 51);">：每个 Subagent 应有明确、单一的任务</font>
2. **<font style="color:rgb(51, 51, 51);">限制工具</font>**<font style="color:rgb(51, 51, 51);">：根据任务需要限制 Subagent 的工具访问权限</font>
3. **<font style="color:rgb(51, 51, 51);">选择合适模型</font>**<font style="color:rgb(51, 51, 51);">：简单任务使用 Haiku，复杂任务使用 Sonnet 或 Opus</font>
4. **<font style="color:rgb(51, 51, 51);">使用后台运行</font>**<font style="color:rgb(51, 51, 51);">：长时间任务使用后台 Subagent，避免阻塞主对话</font>
5. **<font style="color:rgb(51, 51, 51);">恢复 Subagent</font>**<font style="color:rgb(51, 51, 51);">：需要继续工作时，要求 Claude 恢复 Subagent</font>

### <font style="color:rgb(51, 51, 51);">Agent Teams 最佳实践</font>

1. **<font style="color:rgb(51, 51, 51);">给队友足够的上下文</font>**<font style="color:rgb(51, 51, 51);">：在生成提示中包含特定于任务的详细信息</font>
2. **<font style="color:rgb(51, 51, 51);">选择适当的团队规模</font>**<font style="color:rgb(51, 51, 51);">：大多数工作流从 3-5 个队友开始</font>
3. **<font style="color:rgb(51, 51, 51);">适当调整任务大小</font>**<font style="color:rgb(51, 51, 51);">：每个队友 5-6 个任务，保持生产力</font>
4. **<font style="color:rgb(51, 51, 51);">等待队友完成</font>**<font style="color:rgb(51, 51, 51);">：告诉负责人等待队友完成任务后再进行</font>
5. **<font style="color:rgb(51, 51, 51);">从研究和审查开始</font>**<font style="color:rgb(51, 51, 51);">：从不需要编写代码的任务开始</font>
6. **<font style="color:rgb(51, 51, 51);">避免文件冲突</font>**<font style="color:rgb(51, 51, 51);">：分解工作使每个队友拥有不同的文件集</font>
7. **<font style="color:rgb(51, 51, 51);">监控和指导</font>**<font style="color:rgb(51, 51, 51);">：检查进度，重定向不起作用的方法</font>

### <font style="color:rgb(51, 51, 51);">Git Worktree 最佳实践</font>

1. **<font style="color:rgb(51, 51, 51);">每个任务一个 Worktree</font>**<font style="color:rgb(51, 51, 51);">：避免在同一个 worktree 中处理多个不相关的任务</font>
2. **<font style="color:rgb(51, 51, 51);">使用 tmux 管理</font>**<font style="color:rgb(51, 51, 51);">：同时运行多个 Claude 会话时，使用 tmux 便于切换</font>
3. **<font style="color:rgb(51, 51, 51);">清理不需要的 Worktree</font>**<font style="color:rgb(51, 51, 51);">：任务完成后及时删除 worktree</font>

***

## <font style="color:rgb(51, 51, 51);">故障排除</font>

### <font style="color:rgb(51, 51, 51);">Agent Teams 常见问题</font>

| <font style="color:rgb(255, 255, 255);">问题</font> | <font style="color:rgb(255, 255, 255);">解决方案</font> |
| --- | --- |
| <font style="color:rgb(51, 51, 51);">队友未出现</font> | <font style="color:rgb(51, 51, 51);">检查任务是否足够复杂、tmux 是否安装</font> |
| <font style="color:rgb(51, 51, 51);">过多权限提示</font> | <font style="color:rgb(51, 51, 51);">在权限设置中预批准常见操作</font> |
| <font style="color:rgb(51, 51, 51);">队友在错误后停止</font> | <font style="color:rgb(51, 51, 51);">检查输出并给予额外指示或生成替代队友</font> |
| <font style="color:rgb(51, 51, 51);">负责人提前关闭</font> | <font style="color:rgb(51, 51, 51);">告诉负责人继续或等待队友完成</font> |
| <font style="color:rgb(51, 51, 51);">孤立的 tmux 会话</font> | <font style="color:rgb(51, 51, 51);">使用</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">tmux ls</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">和</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">tmux kill-session -t <session-name></font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">清理</font> |

***

## <font style="color:rgb(51, 51, 51);">实用 Subagent 示例</font>

### <font style="color:rgb(51, 51, 51);">代码审查者</font>

**<font style="color:rgb(97, 127, 16);">实例</font>**

<font style="color:cyan;">---</font><font style="color:green;">\
</font><font style="color:green;">name</font>**<font style="color:brown;">:</font>\*\*\*\*<font style="color:brown;"> </font>**<font style="color:rgb(51, 51, 51);">code-reviewer</font><font style="color:green;">\
</font><font style="color:green;">description</font>**<font style="color:brown;">:</font>\*\*\*\*<font style="color:brown;"> </font>**<font style="color:rgb(51, 51, 51);">Expert code review specialist. Proactively reviews code for quality, security, and maintainability.</font><font style="color:green;">\
</font><font style="color:green;">tools</font>**<font style="color:brown;">:</font>\*\*\*\*<font style="color:brown;"> </font>**<font style="color:rgb(51, 51, 51);">Read, Grep, Glob, Bash</font><font style="color:green;">\
</font><font style="color:green;">model</font>**<font style="color:brown;">:</font>\*\*\*\*<font style="color:brown;"> </font>**<font style="color:rgb(51, 51, 51);">inherit\
</font><font style="color:cyan;">---</font><font style="color:rgb(51, 51, 51);">

</font><font style="color:rgb(51, 51, 51);">You are a senior code reviewer ensuring high standards of code quality and security.\
</font><font style="color:rgb(0, 127, 69);">\
</font><font style="color:rgb(0, 127, 69);">When invoked</font>**<font style="color:brown;">:\
</font>**<font style="color:rgb(51, 51, 51);">1</font><font style="color:rgb(51, 51, 51);">. Run git diff to see recent changes\
</font><font style="color:rgb(51, 51, 51);">2</font><font style="color:rgb(51, 51, 51);">. Focus on modified files\
</font><font style="color:rgb(51, 51, 51);">3</font><font style="color:rgb(51, 51, 51);">. Begin review immediately\
</font><font style="color:rgb(0, 127, 69);">\
</font><font style="color:rgb(0, 127, 69);">Review checklist</font>**<font style="color:brown;">:\
</font>**<font style="color:rgb(51, 51, 51);">- Code is clear and readable\
</font><font style="color:rgb(51, 51, 51);">- Functions and variables are well-named\
</font><font style="color:rgb(51, 51, 51);">-</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:rgb(51, 51, 51);">No</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">duplicated code\
</font><font style="color:rgb(51, 51, 51);">- Proper error handling\
</font><font style="color:rgb(51, 51, 51);">-</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:rgb(51, 51, 51);">No</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">exposed secrets or API keys\
</font><font style="color:rgb(51, 51, 51);">- Input validation implemented\
</font><font style="color:rgb(51, 51, 51);">- Good test coverage\
</font><font style="color:rgb(51, 51, 51);">- Performance considerations addressed\
</font><font style="color:rgb(0, 127, 69);">\
</font><font style="color:rgb(0, 127, 69);">Provide feedback organized by priority</font>**<font style="color:brown;">:\
</font>**<font style="color:rgb(51, 51, 51);">- Critical issues</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">(</font><font style="color:rgb(51, 51, 51);">must fix</font><font style="color:rgb(51, 51, 51);">)</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);">- Warnings</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">(</font><font style="color:rgb(51, 51, 51);">should fix</font><font style="color:rgb(51, 51, 51);">)</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);">- Suggestions</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">(</font><font style="color:rgb(51, 51, 51);">consider improving</font><font style="color:rgb(51, 51, 51);">)</font>

### <font style="color:rgb(51, 51, 51);">调试器</font>

**<font style="color:rgb(97, 127, 16);">实例</font>**

<font style="color:cyan;">---</font><font style="color:green;">\
</font><font style="color:green;">name</font>**<font style="color:brown;">:</font>\*\*\*\*<font style="color:brown;"> </font>**<font style="color:rgb(51, 51, 51);">debugger</font><font style="color:green;">\
</font><font style="color:green;">description</font>**<font style="color:brown;">:</font>\*\*\*\*<font style="color:brown;"> </font>**<font style="color:rgb(51, 51, 51);">Debugging specialist for errors, test failures, and unexpected behavior.</font><font style="color:green;">\
</font><font style="color:green;">tools</font>**<font style="color:brown;">:</font>\*\*\*\*<font style="color:brown;"> </font>**<font style="color:rgb(51, 51, 51);">Read, Edit, Bash, Grep, Glob\
</font><font style="color:cyan;">---</font><font style="color:rgb(51, 51, 51);">

</font><font style="color:rgb(51, 51, 51);">You are an expert debugger specializing in root cause analysis.\
</font><font style="color:rgb(0, 127, 69);">\
</font><font style="color:rgb(0, 127, 69);">When invoked</font>**<font style="color:brown;">:\
</font>**<font style="color:rgb(51, 51, 51);">1</font><font style="color:rgb(51, 51, 51);">. Capture error message and stack trace\
</font><font style="color:rgb(51, 51, 51);">2</font><font style="color:rgb(51, 51, 51);">. Identify reproduction steps\
</font><font style="color:rgb(51, 51, 51);">3</font><font style="color:rgb(51, 51, 51);">. Isolate the failure location\
</font><font style="color:rgb(51, 51, 51);">4</font><font style="color:rgb(51, 51, 51);">. Implement minimal fix\
</font><font style="color:rgb(51, 51, 51);">5</font><font style="color:rgb(51, 51, 51);">. Verify solution works\
</font><font style="color:rgb(0, 127, 69);">\
</font><font style="color:rgb(0, 127, 69);">Debugging process</font>**<font style="color:brown;">:\
</font>**<font style="color:rgb(51, 51, 51);">- Analyze error messages and logs\
</font><font style="color:rgb(51, 51, 51);">- Check recent code changes\
</font><font style="color:rgb(51, 51, 51);">- Form and test hypotheses\
</font><font style="color:rgb(51, 51, 51);">- Add strategic debug logging\
</font><font style="color:rgb(51, 51, 51);">- Inspect variable states</font>

### <font style="color:rgb(51, 51, 51);">只读数据库查询器</font>

**<font style="color:rgb(97, 127, 16);">实例</font>**

<font style="color:cyan;">---</font><font style="color:green;">\
</font><font style="color:green;">name</font>**<font style="color:brown;">: </font>**<font style="color:rgb(51, 51, 51);">db-reader</font><font style="color:green;">\
</font><font style="color:green;">description</font>**<font style="color:brown;">: </font>**<font style="color:rgb(51, 51, 51);">Execute read-only database queries. Use when analyzing data or generating reports.</font><font style="color:green;">\
</font><font style="color:green;">tools</font>**<font style="color:brown;">: </font>**<font style="color:rgb(51, 51, 51);">Bash</font><font style="color:rgb(0, 127, 69);">\
</font><font style="color:rgb(0, 127, 69);">hooks</font><font style="color:rgb(51, 51, 51);">:</font><font style="color:rgb(0, 127, 69);">\
</font><font style="color:rgb(0, 127, 69);">PreToolUse</font><font style="color:rgb(51, 51, 51);">:</font><font style="color:green;">\
</font><font style="color:green;">- matcher</font>**<font style="color:brown;">: </font>**<font style="color:rgb(207, 0, 207);">"Bash"</font><font style="color:rgb(0, 127, 69);">\
</font><font style="color:rgb(0, 127, 69);">hooks</font><font style="color:rgb(51, 51, 51);">:</font><font style="color:green;">\
</font><font style="color:green;">- type</font>**<font style="color:brown;">: </font>**<font style="color:rgb(51, 51, 51);">command</font><font style="color:green;">\
</font><font style="color:green;">command</font>**<font style="color:brown;">: </font>**<font style="color:rgb(207, 0, 207);">"./scripts/validate-readonly-query.sh"</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:cyan;">---</font><font style="color:rgb(51, 51, 51);">

</font><font style="color:rgb(51, 51, 51);">You are a database analyst with read-only access. Execute SELECT queries to answer questions about the data.</font>

# Claude Agent SDK 开发配置与智能体应用构建

## <font style="color:rgb(51, 51, 51);">Claude Agent SDK 使用说明</font>

<font style="color:rgb(51, 51, 51);">Claude Agent SDK 让你能够构建可以自主读取文件、运行命令、搜索网络、编辑代码等的 AI Agent。</font>

<font style="color:rgb(51, 51, 51);">Claude Agent SDK 将驱动 Claude Code 的工具、Agent 循环和上下文管理能力开放为可编程的 Python 和 TypeScript 库。</font>

<font style="color:rgb(51, 51, 51);">简单来说，这是一个把 Claude Code 作为库来使用的 SDK，你可以把它嵌入到自己的应用、CI 流水线或自动化脚本中，构建能自主完成复杂任务的 AI Agent。</font>

***

## <font style="color:rgb(51, 51, 51);">核心能力</font>

<font style="color:rgb(51, 51, 51);">SDK 内置了读取文件、运行命令和编辑代码的工具，你的 Agent 无需自己实现工具执行逻辑，可以立即开始工作。主要能力包括：</font>

| <font style="color:rgb(255, 255, 255);">能力</font> | <font style="color:rgb(255, 255, 255);">说明</font> |
| --- | --- |
| **<font style="color:rgb(51, 51, 51);">内置工具</font>** | <font style="color:rgb(51, 51, 51);">文件读写、终端命令、代码编辑、Web 搜索等</font> |
| **<font style="color:rgb(51, 51, 51);">Hooks</font>** | <font style="color:rgb(51, 51, 51);">在工具调用前后执行自定义逻辑</font> |
| **<font style="color:rgb(51, 51, 51);">子 Agent（Subagents）</font>** | <font style="color:rgb(51, 51, 51);">将大任务分解，并行交给独立的子 Agent 执行</font> |
| **<font style="color:rgb(51, 51, 51);">MCP 服务器</font>** | <font style="color:rgb(51, 51, 51);">连接数据库、浏览器、外部 API 等</font> |
| **<font style="color:rgb(51, 51, 51);">权限控制</font>** | <font style="color:rgb(51, 51, 51);">精细控制 Agent 能做什么、何时需要用户审批</font> |
| **<font style="color:rgb(51, 51, 51);">会话管理（Sessions）</font>** | <font style="color:rgb(51, 51, 51);">构建保持上下文的多轮对话 Agent</font> |

***

## <font style="color:rgb(51, 51, 51);">前提条件</font>

* **<font style="color:rgb(51, 51, 51);">Node.js 18+</font>**<font style="color:rgb(51, 51, 51);">（TypeScript）或</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:rgb(51, 51, 51);">Python 3.10+</font>**
* <font style="color:rgb(51, 51, 51);">一个</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:rgb(51, 51, 51);">Anthropic 账号</font>**<font style="color:rgb(51, 51, 51);">，并获取 API Key（</font>[<font style="color:rgb(0, 102, 0);">在此注册</font>](https://platform.claude.com/)<font style="color:rgb(51, 51, 51);">）</font>

***

## <font style="color:rgb(51, 51, 51);">第一步：安装 SDK</font>

### <font style="color:rgb(51, 51, 51);">TypeScript</font>

npm install @anthropic-ai/claude-agent-sdk

*<font style="color:rgb(44, 58, 94);">TypeScript SDK 会将适用于你当前平台的 Claude Code 二进制文件作为可选依赖一起打包，无需单独安装 Claude Code。</font>*

### <font style="color:rgb(51, 51, 51);">Python</font>

```plain
# 使用 pip
pip install claude-agent-sdk

# 或使用 uv（推荐）
uv add claude-agent-sdk
```

*<font style="color:rgb(44, 58, 94);">注意：Claude Code CLI 会自动随包一起安装，无需单独安装！SDK 默认使用打包的 CLI。</font>*

*<font style="color:rgb(44, 58, 94);">如果你希望使用系统级安装或指定版本，可以通过</font>\_\_<font style="color:rgb(44, 58, 94);"> </font>*<code>_<font style="color:rgb(44, 58, 94);">ClaudeAgentOptions(cli_path="/path/to/claude")</font>_</code>*<font style="color:rgb(44, 58, 94);"> </font>\_\_<font style="color:rgb(44, 58, 94);">指定路径。</font>*

***

## <font style="color:rgb(51, 51, 51);">第二步：配置 API Key</font>

<font style="color:rgb(51, 51, 51);">从</font><font style="color:rgb(51, 51, 51);"> </font>[<font style="color:rgb(0, 102, 0);">Claude Console</font>](https://platform.claude.com/)<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">获取 API Key，然后在项目目录创建</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">.env</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">文件：</font>

ANTHROPIC_API_KEY=your-api-key-here

<font style="color:rgb(51, 51, 51);">或直接设置为环境变量：</font>

export ANTHROPIC_API_KEY=your-api-key-here

### <font style="color:rgb(51, 51, 51);">支持第三方云平台</font>

<font style="color:rgb(51, 51, 51);">SDK 也支持通过第三方 API 提供商进行认证：Amazon Bedrock（设置</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">CLAUDE_CODE_USE_BEDROCK=1</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">环境变量并配置 AWS 凭证）、Google Vertex AI（设置</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">CLAUDE_CODE_USE_VERTEX=1</font></code><font style="color:rgb(51, 51, 51);">）以及 Microsoft Azure（设置</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">CLAUDE_CODE_USE_FOUNDRY=1</font></code><font style="color:rgb(51, 51, 51);">）。</font>

*<font style="color:rgb(44, 58, 94);">⚠️</font>**<font style="color:rgb(44, 58, 94);"> </font>**__<font style="color:rgb(44, 58, 94);">重要</font>__\_\_<font style="color:rgb(44, 58, 94);">：除非事先获得 Anthropic 批准，否则不允许第三方开发者在基于 Claude Agent SDK 构建的产品中提供 claude.ai 登录或速率限制。请使用文档中描述的 API Key 认证方式。</font>*

***

## <font style="color:rgb(51, 51, 51);">第三步：运行你的第一个 Agent</font>

<font style="color:rgb(51, 51, 51);">以下示例创建一个 Agent，列出当前目录中的文件：</font>

### <font style="color:rgb(51, 51, 51);">Python</font>

**<font style="color:rgb(97, 127, 16);">实例</font>**

**<font style="color:green;">import</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">asyncio\
</font>**<font style="color:green;">from</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">claude_agent_sdk</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:green;">import</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">query</font><font style="color:gray;">,</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">ClaudeAgentOptions

</font><font style="color:rgb(51, 51, 51);">async</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:green;">def</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">main</font><font style="color:olive;">(</font><font style="color:olive;">)</font><font style="color:rgb(51, 51, 51);">:\
</font><font style="color:rgb(51, 51, 51);">async</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:green;">for</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">message</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:green;">in</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">query</font><font style="color:olive;">(</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);">prompt</font><font style="color:gray;">=</font><font style="color:rgb(170, 17, 17);">"What files are in this directory?"</font><font style="color:gray;">,</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);">options</font><font style="color:gray;">=</font><font style="color:rgb(51, 51, 51);">ClaudeAgentOptions</font><font style="color:olive;">(</font><font style="color:rgb(51, 51, 51);">allowed_tools</font><font style="color:gray;">=</font><font style="color:olive;">\[</font><font style="color:rgb(170, 17, 17);">"Bash"</font><font style="color:gray;">,</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(170, 17, 17);">"Glob"</font><font style="color:olive;">]</font><font style="color:olive;">)</font><font style="color:gray;">,</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:olive;">)</font><font style="color:rgb(51, 51, 51);">:\
</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:green;">if</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:teal;">hasattr</font><font style="color:olive;">(</font><font style="color:rgb(51, 51, 51);">message</font><font style="color:gray;">,</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(170, 17, 17);">"result"</font><font style="color:olive;">)</font><font style="color:rgb(51, 51, 51);">:\
</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:green;">print</font>**<font style="color:olive;">(</font><font style="color:rgb(51, 51, 51);">message.</font><font style="color:rgb(0, 85, 170);">result</font><font style="color:olive;">)</font><font style="color:rgb(51, 51, 51);">

</font><font style="color:rgb(51, 51, 51);">asyncio.</font><font style="color:rgb(0, 85, 170);">run</font><font style="color:olive;">(</font><font style="color:rgb(51, 51, 51);">main</font><font style="color:olive;">(</font><font style="color:olive;">)</font><font style="color:olive;">)</font>

### <font style="color:rgb(51, 51, 51);">TypeScript</font>

**<font style="color:rgb(97, 127, 16);">实例</font>**

<font style="color:rgb(255, 0, 0);">import</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">{</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">query</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">}</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">from</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"@anthropic-ai/claude-agent-sdk"</font><font style="color:rgb(51, 153, 51);">;</font><font style="color:rgb(51, 51, 51);">

</font><font style="color:rgb(51, 51, 51);">async</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:rgb(0, 0, 102);">function</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">main</font><font style="color:rgb(0, 153, 0);">(</font><font style="color:rgb(0, 153, 0);">)</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">{</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:rgb(0, 0, 102);">for</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">await</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">(</font>**<font style="color:rgb(0, 0, 102);">const</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">message of query</font><font style="color:rgb(0, 153, 0);">(</font><font style="color:rgb(0, 153, 0);">{</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);">prompt</font><font style="color:rgb(51, 153, 51);">:</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"What files are in this directory?"</font><font style="color:rgb(51, 153, 51);">,</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);">options</font><font style="color:rgb(51, 153, 51);">:</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">{</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">allowedTools</font><font style="color:rgb(51, 153, 51);">:</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">\[</font><font style="color:rgb(51, 102, 204);">"Bash"</font><font style="color:rgb(51, 153, 51);">,</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 102, 204);">"Glob"</font><font style="color:rgb(0, 153, 0);">]</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">}</font><font style="color:rgb(51, 153, 51);">,</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">}</font><font style="color:rgb(0, 153, 0);">)</font><font style="color:rgb(0, 153, 0);">)</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">{</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:rgb(0, 0, 102);">if</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">(</font><font style="color:rgb(51, 102, 204);">"result"</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:rgb(0, 0, 102);">in</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">message</font><font style="color:rgb(0, 153, 0);">)</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">{</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);">console.</font><font style="color:rgb(102, 0, 102);">log</font><font style="color:rgb(0, 153, 0);">(</font><font style="color:rgb(51, 51, 51);">message.</font><font style="color:rgb(102, 0, 102);">result</font><font style="color:rgb(0, 153, 0);">)</font><font style="color:rgb(51, 153, 51);">;</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">}</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 153, 0);">}</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(0, 153, 0);">}</font><font style="color:rgb(51, 51, 51);">

</font><font style="color:rgb(51, 51, 51);">main</font><font style="color:rgb(0, 153, 0);">(</font><font style="color:rgb(0, 153, 0);">)</font><font style="color:rgb(51, 153, 51);">;</font>

***

## <font style="color:rgb(51, 51, 51);">实战：构建一个自动修复 Bug 的 Agent</font>

<font style="color:rgb(51, 51, 51);">下面通过一个完整示例，演示 Agent SDK 的核心用法。</font>

### <font style="color:rgb(51, 51, 51);">准备一个有 Bug 的文件</font>

<font style="color:rgb(51, 51, 51);">创建</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">utils.py</font></code><font style="color:rgb(51, 51, 51);">，包含两处有意为之的 Bug：</font>

**<font style="color:rgb(97, 127, 16);">实例</font>**

**<font style="color:green;">def</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">calculate_average</font><font style="color:olive;">(</font><font style="color:rgb(51, 51, 51);">numbers</font><font style="color:olive;">)</font><font style="color:rgb(51, 51, 51);">:\
</font><font style="color:rgb(51, 51, 51);">total</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:gray;">=</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:maroon;">0</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:green;">for</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">num</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:green;">in</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">numbers:\
</font><font style="color:rgb(51, 51, 51);">total +</font><font style="color:gray;">=</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">num\
</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:green;">return</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">total /</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:teal;">len</font><font style="color:olive;">(</font><font style="color:rgb(51, 51, 51);">numbers</font><font style="color:olive;">)</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(170, 85, 0);"># Bug: 空列表时除以 0</font><font style="color:rgb(51, 51, 51);">

</font>**<font style="color:green;">def</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">get_user_name</font><font style="color:olive;">(</font><font style="color:rgb(0, 85, 170);">user</font><font style="color:olive;">)</font><font style="color:rgb(51, 51, 51);">:\
</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:green;">return</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(0, 85, 170);">user</font><font style="color:olive;">\[</font><font style="color:rgb(170, 17, 17);">"name"</font><font style="color:olive;">]</font><font style="color:rgb(51, 51, 51);">.</font><font style="color:rgb(0, 85, 170);">upper</font><font style="color:olive;">(</font><font style="color:olive;">)</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(170, 85, 0);"># Bug: user 为 None 时报 TypeError</font>

### <font style="color:rgb(51, 51, 51);">编写 Agent</font>

<font style="color:rgb(51, 51, 51);">创建</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">agent.py</font></code><font style="color:rgb(51, 51, 51);">：</font>

**<font style="color:rgb(97, 127, 16);">实例</font>**

**<font style="color:green;">import</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">asyncio\
</font>**<font style="color:green;">from</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">claude_agent_sdk</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:green;">import</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">query</font><font style="color:gray;">,</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">ClaudeAgentOptions</font><font style="color:gray;">,</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">AssistantMessage</font><font style="color:gray;">,</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">ResultMessage

</font><font style="color:rgb(51, 51, 51);">async</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:green;">def</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">main</font><font style="color:olive;">(</font><font style="color:olive;">)</font><font style="color:rgb(51, 51, 51);">:\
</font><font style="color:rgb(51, 51, 51);">async</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:green;">for</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">message</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:green;">in</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">query</font><font style="color:olive;">(</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);">prompt</font><font style="color:gray;">=</font><font style="color:rgb(170, 17, 17);">"Review utils.py for bugs that would cause crashes. Fix any issues you find."</font><font style="color:gray;">,</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);">options</font><font style="color:gray;">=</font><font style="color:rgb(51, 51, 51);">ClaudeAgentOptions</font><font style="color:olive;">(</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);">allowed_tools</font><font style="color:gray;">=</font><font style="color:olive;">\[</font><font style="color:rgb(170, 17, 17);">"Read"</font><font style="color:gray;">,</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(170, 17, 17);">"Edit"</font><font style="color:gray;">,</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(170, 17, 17);">"Glob"</font><font style="color:olive;">]</font><font style="color:gray;">,</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(170, 85, 0);"># 允许使用的工具</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);">permission_mode</font><font style="color:gray;">=</font><font style="color:rgb(170, 17, 17);">"acceptEdits"</font><font style="color:gray;">,</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">           </font><font style="color:rgb(170, 85, 0);"># 自动批准文件编辑</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:olive;">)</font><font style="color:gray;">,</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:olive;">)</font><font style="color:rgb(51, 51, 51);">:\
</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:green;">if</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:teal;">isinstance</font><font style="color:olive;">(</font><font style="color:rgb(51, 51, 51);">message</font><font style="color:gray;">,</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">AssistantMessage</font><font style="color:olive;">)</font><font style="color:rgb(51, 51, 51);">:\
</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:green;">for</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">block</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:green;">in</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">message.</font><font style="color:rgb(0, 85, 170);">content</font><font style="color:rgb(51, 51, 51);">:\
</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:green;">if</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:teal;">hasattr</font><font style="color:olive;">(</font><font style="color:rgb(51, 51, 51);">block</font><font style="color:gray;">,</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(170, 17, 17);">"text"</font><font style="color:olive;">)</font><font style="color:rgb(51, 51, 51);">:\
</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:green;">print</font>**<font style="color:olive;">(</font><font style="color:rgb(51, 51, 51);">block.</font><font style="color:rgb(0, 85, 170);">text</font><font style="color:olive;">)</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">         </font><font style="color:rgb(170, 85, 0);"># Claude 的推理过程</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:green;">elif</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:teal;">hasattr</font><font style="color:olive;">(</font><font style="color:rgb(51, 51, 51);">block</font><font style="color:gray;">,</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(170, 17, 17);">"name"</font><font style="color:olive;">)</font><font style="color:rgb(51, 51, 51);">:\
</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:green;">print</font>**<font style="color:olive;">(</font><font style="color:rgb(51, 51, 51);">f</font><font style="color:rgb(170, 17, 17);">"Tool: {block.name}"</font><font style="color:olive;">)</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(170, 85, 0);"># 正在调用的工具</font><font style="color:rgb(51, 51, 51);">\
</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:green;">elif</font>**<font style="color:rgb(51, 51, 51);"> </font><font style="color:teal;">isinstance</font><font style="color:olive;">(</font><font style="color:rgb(51, 51, 51);">message</font><font style="color:gray;">,</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">ResultMessage</font><font style="color:olive;">)</font><font style="color:rgb(51, 51, 51);">:\
</font><font style="color:rgb(51, 51, 51);"> </font>**<font style="color:green;">print</font>**<font style="color:olive;">(</font><font style="color:rgb(51, 51, 51);">f</font><font style="color:rgb(170, 17, 17);">"Done: {message.subtype}"</font><font style="color:olive;">)</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(170, 85, 0);"># 最终结果</font><font style="color:rgb(51, 51, 51);">

</font><font style="color:rgb(51, 51, 51);">asyncio.</font><font style="color:rgb(0, 85, 170);">run</font><font style="color:olive;">(</font><font style="color:rgb(51, 51, 51);">main</font><font style="color:olive;">(</font><font style="color:olive;">)</font><font style="color:olive;">)</font>

### <font style="color:rgb(51, 51, 51);">运行</font>

python agent.py

<font style="color:rgb(51, 51, 51);">运行后查看</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">utils.py</font></code><font style="color:rgb(51, 51, 51);">，你会看到 Agent 自主完成了以下操作：</font>

1. **<font style="color:rgb(51, 51, 51);">读取</font>**<font style="color:rgb(51, 51, 51);">了</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">utils.py</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">文件</font>
2. **<font style="color:rgb(51, 51, 51);">分析</font>**<font style="color:rgb(51, 51, 51);">了代码逻辑，识别出可能导致崩溃的边界情况</font>
3. **<font style="color:rgb(51, 51, 51);">编辑</font>**<font style="color:rgb(51, 51, 51);">了文件，添加了完善的错误处理</font>

***

## <font style="color:rgb(51, 51, 51);">核心概念解析</font>

### <font style="color:rgb(51, 51, 51);">函数 —— Agent 循环的入口</font>

<code><font style="color:rgb(51, 51, 51);">query</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">是创建 Agent 循环的主要入口点，返回一个异步迭代器，因此你使用</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">async for</font></code><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">来实时流式获取 Claude 工作时产生的消息。循环在 Claude 完成任务或遇到错误时结束。SDK 负责编排（工具执行、上下文管理、重试），你只需消费这个消息流。</font>

<font style="color:rgb(51, 51, 51);">每次迭代会产生一条消息，可能是：</font>

* <font style="color:rgb(51, 51, 51);">Claude 的推理过程</font>
* <font style="color:rgb(51, 51, 51);">一次工具调用</font>
* <font style="color:rgb(51, 51, 51);">工具调用结果</font>
* <font style="color:rgb(51, 51, 51);">最终结果</font>

### <font style="color:rgb(51, 51, 51);">工具（Tools）—— 控制 Agent 能做什么</font>

| <font style="color:rgb(255, 255, 255);">工具组合</font> | <font style="color:rgb(255, 255, 255);">Agent 能力</font> |
| --- | --- |
| <code><font style="color:rgb(51, 51, 51);">Read</font></code><br/><font style="color:rgb(51, 51, 51);">,</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">Glob</font></code><br/><font style="color:rgb(51, 51, 51);">,</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">Grep</font></code> | <font style="color:rgb(51, 51, 51);">只读分析</font> |
| <code><font style="color:rgb(51, 51, 51);">Read</font></code><br/><font style="color:rgb(51, 51, 51);">,</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">Edit</font></code><br/><font style="color:rgb(51, 51, 51);">,</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">Glob</font></code> | <font style="color:rgb(51, 51, 51);">分析并修改代码</font> |
| <code><font style="color:rgb(51, 51, 51);">Read</font></code><br/><font style="color:rgb(51, 51, 51);">,</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">Edit</font></code><br/><font style="color:rgb(51, 51, 51);">,</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">Bash</font></code><br/><font style="color:rgb(51, 51, 51);">,</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">Glob</font></code><br/><font style="color:rgb(51, 51, 51);">,</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">Grep</font></code> | <font style="color:rgb(51, 51, 51);">完整自动化</font> |
| <font style="color:rgb(51, 51, 51);">加上</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">WebSearch</font></code> | <font style="color:rgb(51, 51, 51);">加入网络搜索能力</font> |

### <font style="color:rgb(51, 51, 51);">权限模式（Permission Modes）—— 控制人工监督程度</font>

| <font style="color:rgb(255, 255, 255);">模式</font> | <font style="color:rgb(255, 255, 255);">行为</font> | <font style="color:rgb(255, 255, 255);">适用场景</font> |
| --- | --- | --- |
| <code><font style="color:rgb(51, 51, 51);">acceptEdits</font></code> | <font style="color:rgb(51, 51, 51);">自动批准文件编辑，其他操作仍需确认</font> | <font style="color:rgb(51, 51, 51);">受信任的开发工作流</font> |
| <code><font style="color:rgb(51, 51, 51);">dontAsk</font></code> | <font style="color:rgb(51, 51, 51);">拒绝</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">allowedTools</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">之外的所有操作</font> | <font style="color:rgb(51, 51, 51);">锁定的无人值守 Agent</font> |
| <code><font style="color:rgb(51, 51, 51);">auto</font></code><br/><font style="color:rgb(51, 51, 51);">（仅 TypeScript）</font> | <font style="color:rgb(51, 51, 51);">模型分类器自动审批/拒绝每个工具调用</font> | <font style="color:rgb(51, 51, 51);">带安全护栏的自主 Agent</font> |
| <code><font style="color:rgb(51, 51, 51);">bypassPermissions</font></code> | <font style="color:rgb(51, 51, 51);">无需提示直接运行所有工具</font> | <font style="color:rgb(51, 51, 51);">沙箱化 CI 环境</font> |
| <code><font style="color:rgb(51, 51, 51);">default</font></code> | <font style="color:rgb(51, 51, 51);">需提供</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">canUseTool</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">回调处理审批</font> | <font style="color:rgb(51, 51, 51);">自定义审批流程</font> |

***

## <font style="color:rgb(51, 51, 51);">自定义 Agent 行为</font>

### <font style="color:rgb(51, 51, 51);">添加 Web 搜索</font>

```plain
options = ClaudeAgentOptions(
    allowed_tools=["Read", "Edit", "Glob", "WebSearch"],
    permission_mode="acceptEdits"
)
```

### <font style="color:rgb(51, 51, 51);">添加自定义系统提示</font>

```plain
options = ClaudeAgentOptions(
    allowed_tools=["Read", "Edit", "Glob"],
    permission_mode="acceptEdits",
    system_prompt="You are a senior Python developer. Always follow PEP 8 style guidelines.",
)
```

### <font style="color:rgb(51, 51, 51);">允许执行终端命令</font>

```plain
options = ClaudeAgentOptions(
    allowed_tools=["Read", "Edit", "Glob", "Bash"],
    permission_mode="acceptEdits"
)
# 可以尝试：
# prompt="Write unit tests for utils.py, run them, and fix any failures"
```

### <font style="color:rgb(51, 51, 51);">加载项目配置（CLAUDE.md 等）</font>

<font style="color:rgb(51, 51, 51);">SDK 构建于与 Claude Code 相同的基础之上，SDK Agent 可以访问相同的基于文件系统的功能：项目说明（CLAUDE.md 和 rules）、技能、Hooks 等。默认情况下 SDK 不加载任何文件系统设置。</font>

```plain
options = ClaudeAgentOptions(
    allowed_tools=["Read", "Edit"],
    # "user" 从 ~/.claude/ 加载，"project" 从 ./.claude/ 加载
    setting_sources=["user", "project"],
)
```

***

## <font style="color:rgb(51, 51, 51);">错误处理</font>

```plain
from claude_agent_sdk import (
    ClaudeSDKError,      # 基础错误
    CLINotFoundError,    # Claude Code 未安装
    CLIConnectionError,  # 连接问题
    ProcessError,        # 进程失败
    CLIJSONDecodeError,  # JSON 解析失败
)

try:
    async for message in query(prompt="Hello"):
        pass
except CLINotFoundError:
    print("请先安装 Claude Code")
except ProcessError as e:
    print(f"进程失败，退出码：{e.exit_code}")
except CLIJSONDecodeError as e:
    print(f"响应解析失败：{e}")
```

***

## <font style="color:rgb(51, 51, 51);">Agent SDK vs. 其他 Claude 工具</font>

|  | <font style="color:rgb(255, 255, 255);">Agent SDK</font> | <font style="color:rgb(255, 255, 255);">Client SDK（Messages API）</font> | <font style="color:rgb(255, 255, 255);">Claude Code CLI</font> |
| --- | --- | --- | --- |
| **<font style="color:rgb(51, 51, 51);">使用方式</font>** | <font style="color:rgb(51, 51, 51);">Python/TypeScript 库</font> | <font style="color:rgb(51, 51, 51);">HTTP API 调用</font> | <font style="color:rgb(51, 51, 51);">终端命令行工具</font> |
| **<font style="color:rgb(51, 51, 51);">工具执行</font>** | <font style="color:rgb(51, 51, 51);">内置，自动执行</font> | <font style="color:rgb(51, 51, 51);">需手动实现</font> | <font style="color:rgb(51, 51, 51);">内置，交互式</font> |
| **<font style="color:rgb(51, 51, 51);">适用场景</font>** | <font style="color:rgb(51, 51, 51);">构建自主 Agent、应用集成</font> | <font style="color:rgb(51, 51, 51);">一般 LLM 调用</font> | <font style="color:rgb(51, 51, 51);">直接编码辅助</font> |
| **<font style="color:rgb(51, 51, 51);">状态管理</font>** | <font style="color:rgb(51, 51, 51);">有状态，支持会话</font> | <font style="color:rgb(51, 51, 51);">无状态</font> | <font style="color:rgb(51, 51, 51);">有状态，交互式</font> |

***

## <font style="color:rgb(51, 51, 51);">SDK 功能对照表</font>

<font style="color:rgb(51, 51, 51);">SDK 还支持 Claude Code 的基于文件系统的配置。若要使用这些功能，需在选项中设置</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">setting_sources=["project"]</font></code><font style="color:rgb(51, 51, 51);">（Python）或</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">settingSources: ['project']</font></code><font style="color:rgb(51, 51, 51);">（TypeScript）。</font>

| <font style="color:rgb(255, 255, 255);">功能</font> | <font style="color:rgb(255, 255, 255);">说明</font> | <font style="color:rgb(255, 255, 255);">位置</font> |
| --- | --- | --- |
| **<font style="color:rgb(51, 51, 51);">Skills（技能）</font>** | <font style="color:rgb(51, 51, 51);">用 Markdown 定义的专项能力</font> | <code><font style="color:rgb(51, 51, 51);">.claude/skills/*/SKILL.md</font></code> |
| **<font style="color:rgb(51, 51, 51);">Slash Commands</font>** | <font style="color:rgb(51, 51, 51);">常用任务的自定义命令</font> | <code><font style="color:rgb(51, 51, 51);">.claude/commands/*.md</font></code> |
| **<font style="color:rgb(51, 51, 51);">Memory（记忆）</font>** | <font style="color:rgb(51, 51, 51);">项目上下文和指令</font> | <code><font style="color:rgb(51, 51, 51);">CLAUDE.md</font></code> |
| **<font style="color:rgb(51, 51, 51);">Plugins（插件）</font>** | <font style="color:rgb(51, 51, 51);">通过</font><font style="color:rgb(51, 51, 51);"> </font><code><font style="color:rgb(51, 51, 51);">plugins</font></code><br/><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">选项扩展</font> | <font style="color:rgb(51, 51, 51);">通过代码配置</font> |

# 企业级项目 Harness AI 工程化编程快速实战

**Harness Engineering（驾驭工程）**是围绕 AI 智能体设计和构建**约束机制、反馈回路、工作流控制和持续改进循环**的系统工程实践。

它不优化模型本身，而是优化模型运行的环境。核心哲学八个字：**人类掌舵，智能体执行（Human Steer, Agent Execute）**。

Harness一词来自马具——缰绳、马鞍、嚼子——这是一套引导强大但不可预测的动物的完整装备。**驾驭工程不是去削弱 AI 的能力，而是为它打造一套黄金缰绳，让它跑得又快又稳。**

![1783672356308-8a4e1937-2897-4f50-86e1-3f8594bd1999.png](./img/wf9R51v5S5sXlvV1/1783672356308-8a4e1937-2897-4f50-86e1-3f8594bd1999-731850.png)

<font style="color:rgb(85, 86, 102);">将 Claude Code 集成到企业软件开发全流程的系统性方法论，通过标准化配置、工作流编排、权限管理和效率度量，实现可复制、可度量、可管控的 AI 辅助开发体系。</font>

**<font style="color:rgb(77, 77, 77);">核心目标：</font>**

1. **<font style="color:rgba(0, 0, 0, 0.75);">可复制</font>**<font style="color:rgba(0, 0, 0, 0.75);">：通过 CLAUDE.md、Skills、Memory 固化最佳实践</font>
2. **<font style="color:rgba(0, 0, 0, 0.75);">可度量</font>**<font style="color:rgba(0, 0, 0, 0.75);">：量化效率提升、质量改善、成本节约</font>
3. **<font style="color:rgba(0, 0, 0, 0.75);">可管控</font>**<font style="color:rgba(0, 0, 0, 0.75);">：权限管理、审计追踪、安全合规</font>

**<font style="color:rgba(0, 0, 0, 0.75);">落地路线图：三步走</font>**

在动手之前，先画清楚路线。Harness Engineering 的落地不是 "一把梭"，而是渐进式的：

```plain
阶段1: 信息层        					阶段2: 约束层         阶段3: 自动化层 
┌───────────────────┐       ┌───────────────────┐       ┌───────────────────┐
│ CLAUDE.md 地图模式  │  →    │ 分层架构 + Linter   │  →    │ Agent 自验证闭环    │
│ docs/ 结构化文档    │       │ CI 约束检查         │       │ 后台清理 Agent      │
│ 编码规范文档化      │       │ 错误信息含修复指令   │       │ JaCoCo/截图自动验证 │
└───────────────────┘       └───────────────────┘       └───────────────────┘
  适合：所有项目               适合：中期项目                适合：长期维护项目
  收益：Agent 输出一致性 ↑     收益：代码质量可控            收益：人工审查量 ↓↓↓
```

**不要一步到位。** 很多人失败就在于想一次性搭完所有基础设施。阶段1 已经能带来显著提升，阶段2 是质变点，阶段3 是锦上添花。

# 基于 Claude Code 和 Harness 开发 Java 电商后台管理系统

### 落地路线图：三步走

在动手之前，先画清楚路线。Harness Engineering 的落地不是 "一把梭"，而是渐进式的：

```plain
阶段1: 信息层（1-2天）         阶段2: 约束层（3-5天）         阶段3: 自动化层（1-2周）
┌───────────────────┐       ┌───────────────────┐       ┌───────────────────┐
│ CLAUDE.md 地图模式  │  →    │ 分层架构 + Linter   │  →    │ Hooks 自验证闭环    │
│ docs/ 结构化文档    │       │ CI 约束检查         │       │ 无头模式清理 Agent  │
│ 编码规范文档化      │       │ 错误信息含修复指令   │       │ JaCoCo/健康检查自动化│
└───────────────────┘       └───────────────────┘       └───────────────────┘
  适合：所有项目               适合：中期项目                适合：长期维护项目
  收益：Agent 输出一致性 ↑     收益：代码质量可控            收益：人工审查量 ↓↓↓
```

**不要一步到位。** 很多人失败就在于想一次性搭完所有基础设施。阶段1 已经能带来显著提升，阶段2 是质变点，阶段3 是锦上添花。

### 阶段1：信息层——让 Claude Code "看得懂" 你的项目

#### CLAUDE.md：写地图，不写百科全书

Claude Code 在每次会话启动时会自动加载项目根目录的 `CLAUDE.md`（以及父目录、`~/.claude/CLAUDE.md` 中的全局记忆）。Anthropic 官方推荐用 "地图模式" 替代超长指令文件——`CLAUDE.md` 只放导航和硬性规则，细节放到 `docs/` 里按需加载。这里给出可以直接拷贝使用的模板。

> 提示：新项目可以先在 Claude Code 中运行 `/init`，让它扫描代码库自动生成一份初始 CLAUDE.md，再按下面的模板裁剪。

**反面教材**（别这么写）：

```plain
# ❌ 错误示范：把所有内容塞进一个文件
我们使用 Spring Boot 2.7.18 + Java 1.8 + Maven 3.6.3 + MySQL 5.7...
类命名使用 PascalCase，方法用 camelCase，常量用 UPPER_SNAKE_CASE...
ORM 用 MyBatis-Plus，迁移用 Flyway，缓存用 Caffeine...
（后面还有 500 行）
```

问题：挤占上下文窗口、难以维护、Agent 很难定位需要的信息。

**正确做法**（直接用）：

```plain
# CLAUDE.md

mkdir -p docs/{architecture,conventions,design,plans,reference}
mkdir -p .claude/hooks .claude/commands .claude/agents

cat > CLAUDE.md << 'EOF'
# CLAUDE.md

## 项目简介
[一句话] 这是一个电商后台管理系统，基于 Spring Boot 2.7 + Java 1.8 + MySQL 5.7。

## 技术栈基线（不允许擅自升级）
- JDK: 1.8，不可使用 Java 9+ 语法（record/var/text blocks）
- Spring Boot: 2.7.x，不可升 3.x（Spring 6 要求 JDK 17）
- Maven: 3.6.3，由 enforcer 强制
- 数据库: MySQL 5.7（utf8mb4），不可升 8.x（生产环境为 5.7）
- 持久化: MyBatis-Plus 3.5.x（基于 MyBatis 3.5）+ Flyway（含 flyway-mysql 子模块），不引入 JPA / Hibernate

## 快速导航
| 你想做什么 | 去哪里看 |
|-----------|---------|
| 了解系统架构 | docs/architecture/overview.md |
| 了解模块边界和依赖规则 | docs/architecture/boundaries.md |
| 了解编码规范 | docs/conventions/README.md |
| 了解当前迭代任务 | docs/plans/current-sprint.md |
| 了解 API 规范 | docs/reference/api-spec.yaml |
| 了解错误码 | docs/reference/error-codes.md |
| 了解测试规范 | docs/conventions/testing.md |

## 硬性规则（必须遵守，CI 会验证）
1. 依赖方向：domain → config → mapper → service → controller
2. 横切关注点（auth/log/telemetry）只能通过 Spring 注入，禁止 `new` 实例化
3. 单文件（.java） ≤ 300 行；单方法 ≤ 50 行
4. 禁止 `System.out.println` / `e.printStackTrace()`，统一使用 SLF4J `Logger`
5. 禁止裸 `RestTemplate` / `HttpURLConnection`，统一通过 `ApiClient` 抽象
6. 禁止字段级 `@Autowired`，必须构造器注入（推荐 Lombok `@RequiredArgsConstructor`）
7. 新增代码必须有对应 JUnit 5 测试，行覆盖率 ≥ 80%

## 常用命令
- 全量校验（编译 + 单测 + Checkstyle + SpotBugs + ArchUnit + JaCoCo）：`mvn -B clean verify`
- 只跑架构测试：`mvn -B test -Dtest=LayerDependencyTest`

## 提交规范
- feat: 新功能
- fix: 修复
- refactor: 重构
- docs: 文档
- test: 测试
```

**关键设计原则**：

* **CLAUDE.md 控制在 50-100 行**。超过就说明你在写百科全书了
* **"你想做什么 → 去哪里看"** 比 "这是什么" 更有效——面向任务而非面向知识
* **硬性规则单独列出**，这些是 CI 会强制验证的，不是 "建议"
* 需要每次会话强制加载的细则，可以用 `@` 导入语法内联进来（如 `@docs/conventions/README.md`）——但要克制，导入的内容同样占上下文
* 会话中发现 Claude 反复犯同一个错误时，直接以 `#` 开头输入一条指令，Claude Code 会把它追加进 CLAUDE.md，实现规则的持续沉淀

#### docs/ 目录：结构化知识库

```plain
# harness环境文档

docs/
├── architecture/
│   ├── overview.md
│   ├── boundaries.md
│   └── data-flow.md
│
├── conventions/
│   ├── README.md
│   ├── naming.md
│   ├── error-handling.md
│   ├── testing.md
│   └── logging.md
│
├── design/
│   ├── feature-auth.md
│   ├── feature-search.md
│   └── feature-billing.md
│
├── plans/
│   ├── current-sprint.md
│   └── backlog.md
│
└── reference/
    ├── api-spec.yaml
    └── error-codes.md
```

**每个文档的头部都加上元信息**：

```plain
---
last_updated: 2026-03-28
status: active          # active | deprecated | draft
owner: @zhangsan
---
```

这样 doc-gardening Agent 可以自动扫描过期文档。

#### 设计文档模板

Agent 执行复杂功能前，先写设计文档。在 Claude Code 中推荐配合 **Plan Mode**（`Shift+Tab` 切换，或 `claude --permission-mode plan` 启动）：先让 Claude 在只读模式下产出方案，人工审批后再退出 Plan Mode 动手写代码。以下是模板：

````plain
# Feature: [功能名称]

## Status: 📝 Draft | 📋 Approved | 🚧 In Progress | ✅ Implemented

## 目标
一句话描述这个功能要解决什么问题。

## 非目标
明确列出这次不做什么（防止 Agent 扩大范围）。

## 技术方案

### 涉及的模块
- domain/      : 新增 XXX 实体（@TableName）与 DTO
- mapper/      : 新增 XXXMapper extends BaseMapper<XXX>
- service/     : 新增 XXXService 业务逻辑
- controller/  : 新增 /api/xxx 端点

### 数据模型变更
```sql
-- 如有数据库变更，写在这里（Flyway 迁移脚本路径：src/main/resources/db/migration/V__xxx.sql）
````

### API 变更

```http
POST /api/xxx
  Request:  { ... }
  Response: { ... }
```

## 验收标准

* 标准 1：具体的、可验证的
* 标准 2：具体的、可验证的
* 测试覆盖率 ≥ 80%

## 依赖

* 依赖 feature-auth（已实现 ✅）

````

**为什么要这么做**：Agent 拿到一个功能需求后，先在 Plan Mode 下填写这个模板（或人工填写），审批通过后再动手写代码。这就是"明确意图"的工程化实现。

### 阶段2：约束层——让 Agent "不能犯错"
Spring Boot 2.7 工程上的标准包结构：

```plain
src/main/java/com/example/app/
├── domain/         # 领域模型与 DTO（不依赖任何业务包；纯 POJO + MyBatis-Plus Entity）
│   ├── model/      # MyBatis-Plus Entity（@TableName / @TableId / @TableField）/ Value Object
│   └── dto/        # Request/Response/Command/Query（Java 8 用 Lombok @Value 模拟 record）
├── config/         # Spring 配置类、@ConfigurationProperties、@MapperScan、MybatisPlusInterceptor（只依赖 domain）
├── mapper/         # MyBatis-Plus Mapper 接口（extends BaseMapper<T>；只依赖 domain、config）
├── service/        # 业务逻辑（依赖 domain、config、mapper）
├── controller/     # REST Controller、@ControllerAdvice 全局异常处理
└── infrastructure/ # 横切关注点：ApiClient、日志、指标、安全
````

下面给出具体的 Linter 配置。

#### 分层依赖检查

##### Java 1.8 + Spring Boot 项目：用 ArchUnit

新增依赖（`pom.xml`）：

```xml
<dependency>
    <groupId>com.tngtech.archunit</groupId>
    <artifactId>archunit-junit5</artifactId>
    <version>1.3.0</version>
    <scope>test</scope>
</dependency>

```

新增架构测试（`src/test/java/com/example/app/architecture/LayerDependencyTest.java`）：

```java
package com.example.app.architecture;

import com.tngtech.archunit.core.importer.ImportOption;
import com.tngtech.archunit.junit.AnalyzeClasses;
import com.tngtech.archunit.junit.ArchTest;
import com.tngtech.archunit.lang.ArchRule;

import static com.tngtech.archunit.library.Architectures.layeredArchitecture;
import static com.tngtech.archunit.lang.syntax.ArchRuleDefinition.noClasses;

@AnalyzeClasses(
    packages = "com.example.app",
    importOptions = ImportOption.DoNotIncludeTests.class
)
public class LayerDependencyTest {

    @ArchTest
    public static final ArchRule layered = layeredArchitecture()
        .consideringAllDependencies()
        .layer("Domain").definedBy("..domain..")
        .layer("Config").definedBy("..config..")
        .layer("Mapper").definedBy("..mapper..")
        .layer("Service").definedBy("..service..")
        .layer("Controller").definedBy("..controller..")
        .layer("Infrastructure").definedBy("..infrastructure..")

        .whereLayer("Controller").mayNotBeAccessedByAnyLayer()
        .whereLayer("Service").mayOnlyBeAccessedByLayers("Controller")
        .whereLayer("Mapper").mayOnlyBeAccessedByLayers("Service")
        .as(
            "❌ 层级依赖违规。\n" +
            "✅ FIX: Controller 必须经 Service，Service 通过 MyBatis-Plus Mapper 访问数据。\n" +
            "📖 See: docs/architecture/boundaries.md"
        );

    @ArchTest
    public static final ArchRule controllerMustNotUseMapper = noClasses()
        .that().resideInAPackage("..controller..")
        .should().dependOnClassesThat().resideInAPackage("..mapper..")
        .as(
            "❌ Controller 不得直接依赖 Mapper。\n" +
            "✅ FIX: 在 Service 中编排数据访问，Controller 仅持有 Service 引用。\n" +
            "📖 See: docs/architecture/boundaries.md"
        );

    @ArchTest
    public static final ArchRule noFieldInjection = noClasses()
        .should().beAnnotatedWith("org.springframework.beans.factory.annotation.Autowired")
        .as(
            "❌ 禁止字段级 @Autowired。\n" +
            "✅ FIX: 构造器注入：\n" +
            "   @RequiredArgsConstructor\n" +
            "   public class UserService {\n" +
            "       private final UserMapper userMapper;\n" +
            "   }\n" +
            "📖 See: docs/conventions/di.md"
        );
}
```

注意：示例中字段一律用 `public static final`（而不是包私有），是因为 Java 8 + JUnit 5 的字段访问要求；Spring Boot 2.7 + ArchUnit 1.3 在 Java 8 上完全可用。

#### 自定义 Linter 规则：错误信息即 Prompt

这是 Harness Engineering 最有杠杆的实践之一。核心思路：**每条 Linter 报错都必须包含三要素——问题是什么、怎么修、去哪看文档。**

以 ArchUnit 自定义规则为例，禁止直接使用 `RestTemplate` / `HttpURLConnection`（要求统一通过 `ApiClient`）：

```java
@ArchTest
public static final ArchRule noRawHttpClient = noClasses()
    .should().dependOnClassesThat()
        .haveFullyQualifiedName("org.springframework.web.client.RestTemplate")
    .orShould().dependOnClassesThat()
        .haveFullyQualifiedName("java.net.HttpURLConnection")
    .orShould().dependOnClassesThat()
        .haveFullyQualifiedName("org.apache.http.client.HttpClient")
    .as(
        "❌ 禁止直接使用 RestTemplate / HttpURLConnection / Apache HttpClient。\n" +
        "✅ FIX: 注入统一的 API Client：\n" +
        "   private final ApiClient apiClient;  // 构造器注入\n" +
        "   Foo foo = apiClient.get(\"/endpoint\", Foo.class);\n" +
        "📖 See: docs/conventions/api-calls.md"
    );
```

或用 Checkstyle 的正则规则，禁止 `System.out.println` / `e.printStackTrace()`（注意 Java 8 兼容须用 Checkstyle 9.3）：

```xml
<module name="RegexpSinglelineJava">
    <property name="format" value="System\.out\.println"/>
    <property name="message"
              value="❌ 禁止 System.out.println。
✅ FIX: private static final Logger log = LoggerFactory.getLogger(X.class);
       log.info(&quot;message {}&quot;, arg);
📖 See: docs/conventions/logging.md"/>
</module>
<module name="RegexpSinglelineJava">
    <property name="format" value="\.printStackTrace\(\)"/>
    <property name="message"
              value="❌ 禁止 e.printStackTrace()。
✅ FIX: log.error(&quot;context message&quot;, e);
📖 See: docs/conventions/logging.md"/>
</module>

```

**一个万能公式**：

```plain
❌ [什么错了]
✅ FIX: [怎么改，给出代码片段]
📖 See: [哪个文档有详细说明]
```

Agent 看到这种报错，不需要任何额外提示就能自动修复。**你写的每一条 Linter 规则，本质上都是一个自动触发的 Prompt。** 配合下文阶段3 的 Hooks，这些报错会在 Claude Code 每次改完文件后自动喂回给它。

#### 完整 pom.xml 关键片段

```xml
<?xml version="1.0" encoding="UTF-8"?>
<project xmlns="http://maven.apache.org/POM/4.0.0">
    <modelVersion>4.0.0</modelVersion>
    <parent>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-parent</artifactId>
        <version>2.7.18</version>
        <relativePath/>
    </parent>
    <groupId>com.example</groupId>
    <artifactId>taskapp</artifactId>
    <version>0.0.1-SNAPSHOT</version>
    <properties>
        <java.version>1.8</java.version>
        <maven.compiler.source>1.8</maven.compiler.source>
        <maven.compiler.target>1.8</maven.compiler.target>
        <project.build.sourceEncoding>UTF-8</project.build.sourceEncoding>
        <!-- 工具版本（均锁定为 Java 8 兼容版本） -->
        <archunit.version>1.3.0</archunit.version>
        <checkstyle.version>9.3</checkstyle.version>
        <maven-checkstyle-plugin.version>3.3.1</maven-checkstyle-plugin.version>
        <spotbugs-maven-plugin.version>4.7.3.6</spotbugs-maven-plugin.version>
        <jacoco.version>0.8.11</jacoco.version>
        <maven-enforcer-plugin.version>3.4.1</maven-enforcer-plugin.version>
        <lombok.version>1.18.30</lombok.version>
        <mybatis-plus.version>3.5.3.2</mybatis-plus.version>
    </properties>
    <dependencies>
        <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-web</artifactId>
        </dependency>
        <!-- 持久化：MyBatis-Plus（替代 Spring Data JPA + Hibernate） -->
        <dependency>
            <groupId>com.baomidou</groupId>
            <artifactId>mybatis-plus-boot-starter</artifactId>
            <version>${mybatis-plus.version}</version>
        </dependency>
        <dependency>
            <groupId>mysql</groupId>
            <artifactId>mysql-connector-java</artifactId>
            <scope>runtime</scope>
        </dependency>
        <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-validation</artifactId>
        </dependency>
        <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-actuator</artifactId>
        </dependency>
        <dependency>
            <groupId>org.projectlombok</groupId>
            <artifactId>lombok</artifactId>
            <version>${lombok.version}</version>
            <scope>provided</scope>
        </dependency>
        <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-test</artifactId>
            <scope>test</scope>
        </dependency>
        <dependency>
            <groupId>com.tngtech.archunit</groupId>
            <artifactId>archunit-junit5</artifactId>
            <version>${archunit.version}</version>
            <scope>test</scope>
        </dependency>
    </dependencies>
    <build>
        <plugins>
            <!-- 锁定 Maven 与 JDK 版本：不达标直接构建失败 -->
            <plugin>
                <groupId>org.apache.maven.plugins</groupId>
                <artifactId>maven-enforcer-plugin</artifactId>
                <version>${maven-enforcer-plugin.version}</version>
                <executions>
                    <execution>
                        <id>enforce-tooling</id>
                        <goals><goal>enforce</goal></goals>
                        <configuration>
                            <rules>
                                <requireMavenVersion>
                                    <version>[3.6.3,)</version>
                                    <message>
                                        ❌ Maven 版本过低。
                                        ✅ FIX: 使用 Maven 3.6.3 及以上（项目基线）。
                                        📖 See: docs/conventions/build.md
                                    </message>
                                </requireMavenVersion>
                                <requireJavaVersion>
                                    <version>[1.8,9)</version>
                                    <message>
                                        ❌ JDK 版本不符。
                                        ✅ FIX: 使用 JDK 1.8 编译；不要升级到 9+。
                                        📖 See: docs/conventions/build.md
                                    </message>
                                </requireJavaVersion>
                            </rules>
                        </configuration>
                    </execution>
                </executions>
            </plugin>
            <!-- Checkstyle：必须显式指定 9.3，否则 maven-checkstyle-plugin 会拉取 Java 11+ 版本 -->
            <plugin>
                <groupId>org.apache.maven.plugins</groupId>
                <artifactId>maven-checkstyle-plugin</artifactId>
                <version>${maven-checkstyle-plugin.version}</version>
                <dependencies>
                    <dependency>
                        <groupId>com.puppycrawl.tools</groupId>
                        <artifactId>checkstyle</artifactId>
                        <version>${checkstyle.version}</version>
                    </dependency>
                </dependencies>
                <configuration>
                    <configLocation>config/checkstyle/checkstyle.xml</configLocation>
                    <consoleOutput>true</consoleOutput>
                    <failsOnError>true</failsOnError>
                    <violationSeverity>warning</violationSeverity>
                </configuration>
                <executions>
                    <execution>
                        <phase>verify</phase>
                        <goals><goal>check</goal></goals>
                    </execution>
                </executions>
            </plugin>
            <!-- SpotBugs -->
            <plugin>
                <groupId>com.github.spotbugs</groupId>
                <artifactId>spotbugs-maven-plugin</artifactId>
                <version>${spotbugs-maven-plugin.version}</version>
                <configuration>
                    <effort>Max</effort>
                    <threshold>Low</threshold>
                    <failOnError>true</failOnError>
                </configuration>
                <executions>
                    <execution>
                        <phase>verify</phase>
                        <goals><goal>check</goal></goals>
                    </execution>
                </executions>
            </plugin>
            <!-- JaCoCo 覆盖率 ≥ 80% -->
            <plugin>
                <groupId>org.jacoco</groupId>
                <artifactId>jacoco-maven-plugin</artifactId>
                <version>${jacoco.version}</version>
                <executions>
                    <execution><goals><goal>prepare-agent</goal></goals></execution>
                    <execution>
                        <id>jacoco-check</id>
                        <phase>verify</phase>
                        <goals><goal>check</goal></goals>
                        <configuration>
                            <rules>
                                <rule>
                                    <element>BUNDLE</element>
                                    <limits>
                                        <limit>
                                            <counter>LINE</counter>
                                            <value>COVEREDRATIO</value>
                                            <minimum>0.80</minimum>
                                        </limit>
                                    </limits>
                                </rule>
                            </rules>
                        </configuration>
                    </execution>
                </executions>
            </plugin>
        </plugins>
    </build>
</project>

```

#### Checkstyle 配置（`config/checkstyle/checkstyle.xml`）

```xml
<?xml version="1.0"?>
<!DOCTYPE module PUBLIC
        "-//Checkstyle//DTD Checkstyle Configuration 1.3//EN"
        "https://checkstyle.org/dtds/configuration_1_3.dtd">
<module name="Checker">
    <property name="severity" value="error"/>

    <module name="FileLength">
        <property name="max" value="300"/>
        <message key="maxLen.file"
                 value="❌ 文件超过 300 行。
✅ FIX: 拆分为更小的类，把辅助方法移至 *Helper 或 infrastructure。
📖 See: docs/conventions/file-size.md"/>
    </module>
    <module name="TreeWalker">
        <module name="MethodLength">
            <property name="max" value="50"/>
            <property name="countEmpty" value="false"/>
            <message key="maxLen.method"
                     value="❌ 方法超过 50 行。
✅ FIX: 抽取私有方法或将职责下沉到 Service / Domain。
📖 See: docs/conventions/method-size.md"/>
        </module>
        <module name="RegexpSinglelineJava">
            <property name="format" value="System\.out\.println"/>
            <property name="message"
                      value="❌ 禁止 System.out.println。
✅ FIX: private static final Logger log = LoggerFactory.getLogger(X.class);
📖 See: docs/conventions/logging.md"/>
        </module>
        <module name="RegexpSinglelineJava">
            <property name="format" value="\.printStackTrace\(\)"/>
            <property name="message"
                      value="❌ 禁止 e.printStackTrace()。
✅ FIX: log.error(&quot;context message&quot;, e);
📖 See: docs/conventions/logging.md"/>
        </module>
    </module>
</module>

```

#### CI 管线配置：完整的 Agent 护栏

```yaml
name: Agent Guardrails

on: [pull_request]

jobs:
  quality-gates:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4

      - name: Set up JDK 1.8
        uses: actions/setup-java@v4
        with:
          distribution: 'temurin'
          java-version: '8'
          cache: maven

      # GitHub Actions runner 默认 Maven 版本可能与基线不一致，强制对齐 3.6.3
      - name: Set up Maven 3.6.3
        uses: stCarolas/setup-maven@v5
        with:
          maven-version: 3.6.3

      - name: Verify tooling
        run: |
          java -version
          mvn -v

      # 编译 + 单测 + Checkstyle + SpotBugs + JaCoCo (>= 80%) + ArchUnit
      # 全部绑定到 verify 阶段，一次执行；enforcer 会顺带验证 Maven/JDK 版本
      - name: Build & Verify
        run: mvn -B clean verify

      - name: Architecture Check (ArchUnit, 单独打日志)
        run: mvn -B test -Dtest='*ArchTest,LayerDependencyTest'

      - name: File Size Check
        shell: bash
        run: |
          find src/main/java -name '*.java' | while read f; do
            lines=$(wc -l < "$f")
            if [ "$lines" -gt 300 ]; then
              echo "❌ $f 有 $lines 行（上限 300）"
              echo "✅ FIX: 拆分为更小的类，将辅助方法移至 *Helper 或 infrastructure。"
              echo "📖 See: docs/conventions/file-size.md"
              exit 1
            fi
          done

      - name: Doc Freshness
        shell: bash
        run: |
          find docs/design/ -name '*.md' | while read f; do
            last_mod=$(git log -1 --format=%ct "$f")
            now=$(date +%s)
            days_old=$(( (now - last_mod) / 86400 ))
            if [ "$days_old" -gt 60 ]; then
              echo "⚠️ $f 已 ${days_old} 天未更新，可能已过期"
            fi
          done
```

CI 是最后一道防线。但对 Claude Code 来说，更高杠杆的做法是把同样的检查前移到本地会话内——见阶段3 的 Hooks。

#### 把主观品味翻译成机械规则

| **团队口头约定** | **机械化规则** | **实现方式** |
| :--- | :--- | :--- |
| "方法要短" | 单方法 ≤ 50 行 | Checkstyle `MethodLength` |
| "文件要短" | 单文件 ≤ 300 行 | Checkstyle `FileLength` |
| "日志要规范" | 禁止 `System.out` / `printStackTrace` | Checkstyle 正则规则 |
| "HTTP 调用要统一" | 禁止裸 `RestTemplate` / `HttpURLConnection` | ArchUnit 自定义规则 |
| "Controller 要纯" | Controller 不得直接调 Mapper | ArchUnit 分层规则 |
| "依赖要构造器注入" | 禁止字段级 `@Autowired` | ArchUnit 注解检查 |
| "不要污染全局" | 禁止 `public static` 非 final 字段 | SpotBugs `MS_*` 规则族 |
| "测试要充分" | 行覆盖率 ≥ 80% | JaCoCo `coverage check` |
| "锁定构建工具版本" | Maven ≥ 3.6.3，JDK = 1.8 | maven-enforcer-plugin |
| "危险命令不能跑" | 禁止 `git push -f` / 删库脚本 | Claude Code `settings.json` deny 规则 |

**经验法则**：如果一条规则在 Code Review 中被提过 3 次以上，就应该写成 Linter 规则。

### 阶段3：自动化层——让 Claude Code 自我验证和自我修复

#### Hooks：改完即验证的闭环

Hooks 是 Claude Code 的确定性护栏：在指定生命周期（如 `PostToolUse`、`Stop`）自动执行 shell 命令，**退出码 2 时 stderr 会直接喂回给 Claude**，触发它自动修复。这正好和阶段2 "错误信息即 Prompt" 的 Linter 规则形成闭环。

项目级配置 `.claude/settings.json`（提交进 git，全团队共享）：

```json
{
  "permissions": {
    "allow": [
      "Bash(mvn -B *)",
      "Bash(mvn clean verify)",
      "Bash(git diff *)",
      "Bash(git log *)"
    ],
    "deny": [
      "Bash(git push --force*)",
      "Bash(rm -rf *)",
      "Read(./.env*)"
    ]
  },
  "hooks": {
    "PostToolUse": [
      {
        "matcher": "Edit|Write",
        "hooks": [
          {
            "type": "command",
            "command": "bash .claude/hooks/check-java.sh"
          }
        ]
      }
    ],
    "Stop": [
      {
        "hooks": [
          {
            "type": "command",
            "command": "bash .claude/hooks/verify-before-stop.sh",
            "timeout": 600
          }
        ]
      }
    ]
  }
}
```

`.claude/hooks/check-java.sh`——每次 Claude 编辑 `.java` 文件后立即做轻量检查（重活留给 Stop 钩子和 CI）：

```bash
#!/bin/bash
# stdin 是 hook 的 JSON 输入，取出刚被编辑的文件路径
file=$(jq -r '.tool_input.file_path // empty')
[[ "$file" != *.java ]] && exit 0

# 单文件行数检查（对应 CLAUDE.md 硬性规则 3）
lines=$(wc -l < "$file")
if [ "$lines" -gt 300 ]; then
  echo "❌ $file 有 $lines 行（上限 300）。" >&2
  echo "✅ FIX: 拆分为更小的类，将辅助方法移至 *Helper 或 infrastructure。" >&2
  echo "📖 See: docs/conventions/file-size.md" >&2
  exit 2   # 退出码 2：stderr 反馈给 Claude，让它立即修复
fi

# 禁止 System.out.println / printStackTrace（对应硬性规则 4）
if grep -nE 'System\.out\.println|\.printStackTrace\(\)' "$file"; then
  echo "❌ 检测到 System.out.println 或 e.printStackTrace()。" >&2
  echo "✅ FIX: 使用 SLF4J：log.error(\"context message\", e);" >&2
  echo "📖 See: docs/conventions/logging.md" >&2
  exit 2
fi
exit 0
```

`.claude/hooks/verify-before-stop.sh`——Claude 声称 "做完了" 之前，强制跑一次全量校验：

```bash
#!/bin/bash
# 无 Java 改动就放行，避免每次对话结束都跑 Maven
git diff --name-only HEAD | grep -q '\.java$' || exit 0

if ! mvn -B clean verify > /tmp/verify.log 2>&1; then
  echo "❌ mvn -B clean verify 失败，不能结束任务。最近报错：" >&2
  tail -n 40 /tmp/verify.log >&2
  echo "✅ FIX: 根据上面的 Checkstyle/ArchUnit/JaCoCo 报错逐条修复后重试。" >&2
  exit 2   # 阻止 Claude 停下来，带着报错继续修
fi
exit 0
```

有了这两个钩子，"约束 → 告知 → 验证 → 纠正" 的闭环就完全自动化了：Claude 每次改完代码立即被检查，想结束任务必须先让 `mvn verify` 通过。

#### 后台清理 Agent：自定义斜杠命令 + 无头模式

把清理任务写成 Claude Code 自定义斜杠命令 `.claude/commands/cleanup.md`（提交进 git，团队共用）：

```markdown
---
description: 代码库卫生清理，每个问题生成独立修复 PR
allowed-tools: Bash(mvn *), Bash(git *), Bash(gh *)
---

# 任务：代码库卫生清理

请执行以下检查，对每个发现的问题生成独立的修复 PR：

## 检查清单
1. **超长文件**：找出 src/main/java/ 下超过 300 行的 .java 文件，拆分为更小的类
2. **缺失测试**：找出 src/main/java/ 下没有对应 *Test.java 的类，补充基础测试
3. **未使用的 import**：清理所有未使用的 import 语句
4. **TODO/FIXME**：列出所有 TODO 和 FIXME，超过 30 天未处理则生成清理 PR
5. **重复代码**：找出高度相似的代码段（>10行），提取为共享工具类（infrastructure/）
6. **过时文档**：检查 docs/design/ 中状态为 Draft 但已超过 30 天的文档
7. **Checkstyle/SpotBugs 历史告警**：清理 mvn verify 中累积的非阻塞告警

## 约束
- 每个修复作为独立 PR，不要混在一起
- 每个 PR 修改后必须确保 `mvn -B clean verify` 通过
- PR 标题格式：`chore(cleanup): [具体描述]`
- 不允许使用 Java 9+ 语法（record/var/text blocks），保持 JDK 1.8 兼容
- 不允许升级 Spring Boot 主版本（保持 2.7.x）
- 如果不确定某个修改是否安全，跳过并在 PR 中标注原因
```

交互式会话里输入 `/cleanup` 即可触发；定时任务用**无头模式**（`claude -p`）跑，配合 cron / Windows 计划任务 / GitHub Actions schedule：

```bash
# 每周一凌晨 2 点自动清理（crontab）
0 2 * * 1  cd /path/to/project && claude -p "/cleanup" \
    --permission-mode acceptEdits \
    --allowedTools "Bash(mvn *)" "Bash(git *)" "Bash(gh pr create*)" \
    --output-format json > /var/log/claude-cleanup.log 2>&1
```

复杂检查项还可以拆成**子代理**（`.claude/agents/doc-gardener.md`），让文档巡检与代码清理各用独立上下文并行执行：

```markdown
---
name: doc-gardener
description: 扫描 docs/ 下的过期文档并标记 deprecated。检查文档新鲜度时主动使用。
tools: Read, Grep, Glob, Edit, Bash(git log *)
---

你是文档园丁。职责：
1. 扫描 docs/**/*.md 头部的 last_updated 与 status 元信息
2. 超过 60 天未更新且 status 为 active 的，核对代码后改为 deprecated 或更新内容
3. status 为 draft 且超过 30 天的，汇总清单输出
禁止修改 docs/ 以外的任何文件。
```

#### Git Worktree：并行会话隔离验证

Claude Code 官方推荐用 git worktree 跑并行任务——每个 worktree 一个独立的 Claude 会话，互不污染。验证脚本模板：

```bash
#!/bin/bash

BRANCH=$1
WORKTREE_DIR="/tmp/agent-verify-$(date +%s)"

echo "🔧 创建 worktree: $WORKTREE_DIR"
git worktree add "$WORKTREE_DIR" "$BRANCH"

cd "$WORKTREE_DIR"

echo "🔍 校验工具链版本..."
java -version 2>&1 | grep '"1.8' || { echo "❌ 必须使用 JDK 1.8"; exit 1; }
mvn -v | grep 'Apache Maven 3.6.3' || { echo "❌ 必须使用 Maven 3.6.3"; exit 1; }

echo "📦 编译并跑全量校验（enforcer + Checkstyle + SpotBugs + ArchUnit + 单测 + JaCoCo）..."
mvn -B clean verify || { echo "❌ mvn verify 失败"; exit 1; }

echo "🚀 启动 Spring Boot 应用做健康检查..."
mvn -B spring-boot:run > /tmp/app.log 2>&1 &
APP_PID=$!

# 等待应用启动（默认 8080，actuator 健康检查）
for i in {1..30}; do
  sleep 2
  if curl -sf http://localhost:8080/actuator/health | grep -q '"status":"UP"'; then
    echo "✅ 健康检查通过"
    kill $APP_PID 2>/dev/null
    cd -
    git worktree remove "$WORKTREE_DIR"
    echo "✅ 所有验证通过"
    exit 0
  fi
done

echo "❌ 应用启动失败或健康检查未通过，最近日志："
tail -n 50 /tmp/app.log
kill $APP_PID 2>/dev/null
exit 1
```

也可以在 worktree 里直接开无头验证会话，让 Claude 自己解读失败日志：

```bash
git worktree add /tmp/verify-feat feat/xxx
cd /tmp/verify-feat && claude -p "运行 mvn -B clean verify，如失败请分析根因并输出修复建议（不要改代码）"
```

#### 可观测性接入：让 Claude Code 能 "看日志"

在本地开发环境部署一个轻量级的可观测性堆栈：

```yaml
version: '3.8'

services:
  loki:
    image: grafana/loki:2.9.0
    ports: ["3100:3100"]

  promtail:
    image: grafana/promtail:2.9.0
    volumes:
      - ./logs:/var/log/app
      - ./promtail-config.yml:/etc/promtail/config.yml

  prometheus:
    image: prom/prometheus:latest
    ports: ["9090:9090"]
    volumes:
      - ./prometheus.yml:/etc/prometheus/prometheus.yml

  grafana:
    image: grafana/grafana:latest
    ports: ["3001:3000"]
    depends_on: [loki, prometheus]
```

Spring Boot 2.7 侧只需开启 Actuator + Micrometer Prometheus（已包含在 actuator starter 中）：

```yaml
# application.yml
management:
  endpoints:
    web:
      exposure:
        include: health,info,metrics,prometheus
  metrics:
    tags:
      application: ${spring.application.name}
```

同时在 `application.yml` 中给出 MyBatis-Plus 与数据源的最小可工作配置（与 Hibernate `MySQL57Dialect` 无关；不再使用 `spring.jpa.*`）：

```yaml
spring:
  datasource:
    url: jdbc:mysql://localhost:3306/taskapp?useSSL=false&serverTimezone=Asia/Shanghai&characterEncoding=utf8mb4&allowPublicKeyRetrieval=true
    username: app
    password: ${DB_PASSWORD}
    driver-class-name: com.mysql.cj.jdbc.Driver
  flyway:
    enabled: true
    locations: classpath:db/migration
    baseline-on-migrate: true

mybatis-plus:
  mapper-locations: classpath*:/mapper/**/*.xml
  type-aliases-package: com.example.app.domain.model
  global-config:
    db-config:
      id-type: auto
      logic-delete-field: deleted
      logic-not-delete-value: 0
      logic-delete-value: 1
  configuration:
    map-underscore-to-camel-case: true
    cache-enabled: false
```

`@MapperScan` 与分页插件单独放在 `config/MybatisPlusConfig.java`，以便 ArchUnit 仅在 `..config..` 这一层看到它：

```java
@Configuration
@MapperScan("com.example.app.mapper")
public class MybatisPlusConfig {

    @Bean
    public MybatisPlusInterceptor mybatisPlusInterceptor() {
        MybatisPlusInterceptor interceptor = new MybatisPlusInterceptor();
        interceptor.addInnerInterceptor(new PaginationInnerInterceptor(DbType.MYSQL));
        return interceptor;
    }
}
```

并在 `logback-spring.xml` 中启用 JSON 结构化日志（`logstash-logback-encoder`），落盘到 `./logs/` 供 Promtail 抓取。日志接口（Loki/Prometheus）还可以通过 MCP Server 挂进 Claude Code（`claude mcp add`），让它直接查询而不是靠 curl。

排错时可以在 Claude Code 里用这样的 Prompt：

```plain
应用在 /api/users 端点返回 500 错误。
请用 curl 查询 Loki（http://localhost:3100）最近 5 分钟的错误日志，
对照 Spring Boot 的 traceId 找到完整调用链，
定位根因并修复。修复后重新跑 `mvn -B clean verify` 与对应的 *Test 验证。
```

### Claude Code 安装配置与工具选型

#### 工具全景图

```plain
                        ┌─────────────────────────────────┐
                        │  你的项目代码仓库（Spring Boot 2.7 / JDK8） │
                        └─────────────┬───────────────────┘
                                      │
              ┌───────────────────────┼───────────────────────┐
              │                       │                       │
    ┌─────────▼─────────┐  ┌─────────▼─────────┐  ┌─────────▼─────────┐
    │  阶段1: 信息层   │  │  阶段2: 约束层   │  │ 阶段3: 自动化层  │
    │                    │  │                    │  │                    │
    │ • CLAUDE.md        │  │ • ArchUnit         │  │ • Hooks            │
    │ • docs/ 结构       │  │ • Checkstyle 9.3   │  │ • 斜杠命令/子代理  │
    │ • 设计文档模板     │  │ • SpotBugs/JaCoCo  │  │ • claude -p 无头   │
    │                    │  │ • maven-enforcer   │  │ • Worktree + Loki  │
    └────────────────────┘  └────────────────────┘  └────────────────────┘
              │                       │                       │
              └───────────────────────┼───────────────────────┘
                                      │
                        ┌─────────────▼───────────────────┐
                        │        Claude Code（CLI Agent）    │
                        │  CLAUDE.md / settings.json /      │
                        │  Hooks / Commands / Subagents /   │
                        │  MCP / Headless (-p)              │
                        └───────────────────────────────────┘
```

#### 安装与启动

```bash
# 通过 npm 全局安装
npm install -g @anthropic-ai/claude-code

# 验证安装
claude --version

# 进入项目目录，启动交互式会话（首次会引导登录 / 配置 API Key）
cd your-spring-project
claude

# 首次使用：让 Claude 扫描代码库生成初始 CLAUDE.md
> /init
```

#### 权限模式（Permission Mode）

Claude Code 通过权限模式控制自主程度，`Shift+Tab` 在会话中随时切换：

| **模式** | **说明** | **适用场景** |
| :--- | :--- | :--- |
| **Default（默认）** | 每次写文件/执行命令都需确认 | 教学演示、初学者，安全可控 |
| **Plan Mode（计划）** | 只读分析，先出方案再动手 | 复杂功能的设计评审阶段 |
| **Accept Edits（自动编辑）** | 自动改文件，敏感命令仍需确认 | 熟练后提速 |
| **Bypass Permissions（全自动）** | 不再询问，全自动执行 | 沙箱/容器内的批量任务 |

更细粒度的控制放在 `.claude/settings.json` 的 `permissions.allow / deny`（见阶段3），把 "哪些命令可以自动跑" 一次性写成团队共享的规则，而不是每次会话手动确认。

#### 同类工具对比

| **工具** | **类型** | **最适合的场景** | **Harness 友好度** |
| :--- | :--- | :--- | :--- |
| [**Claude Code**](https://claude.com/claude-code) | CLI / IDE Agent | 深度自主任务、Hooks/子代理/无头模式全套 harness 能力 | ⭐⭐⭐⭐⭐ |
| [**Aider**](https://github.com/Aider-AI/aider) | CLI 结对编程 | 个人开发者，终端党 | ⭐⭐⭐⭐ |
| [**Cline**](https://github.com/cline/cline) | VS Code Agent | 小团队，需要 Plan/Act 模式 | ⭐⭐⭐⭐ |
| [**OpenHands**](https://github.com/All-Hands-AI/OpenHands) | 平台 | 团队级部署，需要沙箱隔离 | ⭐⭐⭐⭐⭐ |
| [**SWE-agent**](https://github.com/princeton-nlp/SWE-agent) | CLI Agent | 自动修复 GitHub Issue | ⭐⭐⭐ |

**怎么选**：

* **个人/团队项目，想要完整 harness 能力** → Claude Code。CLAUDE.md 天然实现 "地图模式"，Hooks 实现改完即验证，`-p` 无头模式接 cron/CI：

```bash
npm install -g @anthropic-ai/claude-code
cd your-spring-project && claude
```

* **需要流程强控制** → Claude Code 的 Plan Mode + Default 权限模式：先审批计划，再逐步确认每个改动。
* **生产级，需要完全隔离** → Devcontainer/Docker 沙箱内跑 `claude --dangerously-skip-permissions`，或用 OpenHands 平台化部署。

### Harness 落地实战：开发电商后台订单管理模块

以本仓库（RuoYi-Vue：Spring Boot + MyBatis + Vue2/Element-UI 前后端分离）为例，演示用 Claude Code 从需求到验证完整交付一个**订单管理模块**。这个案例覆盖了 harness 闭环的每一环：设计文档先行（Plan Mode）→ 遵循既有架构约定实现 → 编译/语法自动验证。

#### 第 0 步：给 Claude Code 的任务 Prompt

```plain
分析当前项目和 sql/ry_20260417.sql，设计电商管理后台订单管理模块的 SQL 表和初始化脚本，
然后实现前端和后端代码，验证通过后交付。
约束：
- 遵循 RuoYi 既有分层：domain/mapper/service 放 ruoyi-system，controller 放 ruoyi-admin
- Mapper 用 MyBatis XML（不是注解），前端遵循 Vue2 + element-ui + dicts 字典模式
- 菜单/字典 ID 不得与 ry_20260417.sql 已有数据冲突
- 权限标识遵循 模块:实体:动作 规范（shop:order:list 等）
```

**关键点**：Prompt 里不需要教 Claude 怎么写 RuoYi 代码——它会先读现有模块（`SysNotice*` 全链路）提炼模式再动手。这正是 "信息层" 的价值：项目本身的一致性就是最好的 CLAUDE.md。

#### 第 1 步：设计文档（Plan Mode 产出，人工审批）

```plain
# Feature: 订单管理模块

## Status: ✅ Implemented

## 目标
电商后台的订单查询、发货、取消、删除、导出全流程管理。

## 非目标
- 不做订单创建/支付（属于商城前台域）
- 不做物流轨迹对接

## 技术方案
### 涉及的模块
- sql/                 : shop_order + shop_order_item 建表与字典/菜单初始化
- ruoyi-system/shop    : domain（ShopOrder/ShopOrderItem）、mapper、service
- ruoyi-admin          : ShopOrderController（/shop/order）
- ruoyi-ui             : api/shop/order.js + views/shop/order/index.vue

### 状态机（核心业务规则，Service 层强校验）
0待付款 → 1待发货 → 2待收货 → 3已完成
   ↓          ↓
 4已取消   4已取消          （5已退款为终态）
- 发货：仅 1 → 2，记录 delivery_time
- 取消：仅 0/1 → 4
- 删除：仅终态（3/4/5）可删，逻辑删除（del_flag='2'）

## 验收标准
- mvn -B compile 通过；Mapper XML 与接口方法一一对应
- 菜单/字典 ID 与存量数据无冲突（menu_id 从 2000 起，dict_id 从 11 起）
- 前端 JS 语法校验通过，字典渲染用 dict-tag 组件
```

#### 第 2 步：SQL 设计（`sql/shop_order_20260710.sql`）

表结构遵循 RuoYi 约定（del_flag 逻辑删除、create_by/create_time 四件套、状态用 char(1) + 字典）：

```sql
create table shop_order (
  order_id          bigint(20)      not null auto_increment    comment '订单ID',
  order_no          varchar(32)     not null                   comment '订单编号',
  user_name         varchar(30)     not null                   comment '下单用户',
  receiver_name     varchar(30)     not null                   comment '收货人姓名',
  receiver_phone    varchar(11)     not null                   comment '收货人电话',
  receiver_address  varchar(200)    not null                   comment '收货地址',
  total_amount      decimal(12,2)   not null default 0.00      comment '订单总金额',
  pay_amount        decimal(12,2)   not null default 0.00      comment '实付金额',
  pay_type          char(1)         default null               comment '支付方式（1微信 2支付宝 3银行卡）',
  status            char(1)         not null default '0'       comment '订单状态（0待付款 1待发货 2待收货 3已完成 4已取消 5已退款）',
  pay_time          datetime        default null               comment '支付时间',
  delivery_time     datetime        default null               comment '发货时间',
  finish_time       datetime        default null               comment '完成时间',
  del_flag          char(1)         default '0'                comment '删除标志（0代表存在 2代表删除）',
  create_by         varchar(64)     default ''                 comment '创建者',
  create_time       datetime                                   comment '创建时间',
  update_by         varchar(64)     default ''                 comment '更新者',
  update_time       datetime                                   comment '更新时间',
  remark            varchar(500)    default null               comment '备注',
  primary key (order_id),
  unique key uk_order_no (order_no),
  key idx_status (status),
  key idx_create_time (create_time)
) engine=innodb auto_increment=100 comment = '订单主表';

create table shop_order_item (
  item_id           bigint(20)      not null auto_increment    comment '明细ID',
  order_id          bigint(20)      not null                   comment '订单ID',
  goods_name        varchar(100)    not null                   comment '商品名称',
  goods_sku         varchar(50)     default ''                 comment '商品SKU',
  goods_price       decimal(10,2)   not null default 0.00      comment '商品单价',
  quantity          int(4)          not null default 1         comment '购买数量',
  total_price       decimal(12,2)   not null default 0.00      comment '小计金额',
  primary key (item_id),
  key idx_order_id (order_id)
) engine=innodb auto_increment=100 comment = '订单明细表';
```

字典与菜单初始化（**ID 避让是 Agent 最容易踩的坑**——先 grep 存量脚本确定 max ID，再从安全区间起号）：

```sql
-- 字典：ry_20260417.sql 中 dict_id 最大为 10、dict_code 最大为 29，故从 11/30 起
insert into sys_dict_type values(11, '订单状态', 'shop_order_status', '0', 'admin', sysdate(), '', null, '商城订单状态列表');
insert into sys_dict_data values(30, 1, '待付款', '0', 'shop_order_status', '', 'warning', 'Y', '0', 'admin', sysdate(), '', null, '订单待付款');
-- ...（31-38：待发货/待收货/已完成/已取消/已退款 + 微信/支付宝/银行卡）

-- 菜单：存量 menu_id 最大 1060，业务菜单从 2000 起
insert into sys_menu values('2000', '商城管理', '0',    '5', 'shop',  null,               '', '', 1, 0, 'M', '0', '0', '',                'shopping', 'admin', sysdate(), '', null, '商城管理目录');
insert into sys_menu values('2001', '订单管理', '2000', '1', 'order', 'shop/order/index', '', '', 1, 0, 'C', '0', '0', 'shop:order:list', 'list',     'admin', sysdate(), '', null, '订单管理菜单');
-- 按钮权限 2002-2006：shop:order:query / deliver / cancel / remove / export
```

#### 第 3 步：后端实现（分层 + 状态机校验）

包结构（`@MapperScan("com.ruoyi.**.mapper")` 与 `typeAliasesPackage: com.ruoyi.**.domain` 使新包零配置生效）：

```plain
ruoyi-system/src/main/java/com/ruoyi/shop/
├── domain/ShopOrder.java, ShopOrderItem.java
├── mapper/ShopOrderMapper.java, ShopOrderItemMapper.java
└── service/IShopOrderService.java, impl/ShopOrderServiceImpl.java
ruoyi-system/src/main/resources/mapper/shop/
├── ShopOrderMapper.xml, ShopOrderItemMapper.xml
ruoyi-admin/src/main/java/com/ruoyi/web/controller/shop/
└── ShopOrderController.java
```

Service 层把设计文档里的状态机翻译成强校验——**业务规则收敛在 Service，Controller 保持纯净**（对应硬性规则"Controller 要纯"）：

```java
@Service
public class ShopOrderServiceImpl implements IShopOrderService
{
    /** 订单状态：0待付款 1待发货 2待收货 3已完成 4已取消 5已退款 */
    public static final String STATUS_UNDELIVERED = "1";
    public static final String STATUS_DELIVERED = "2";

    @Override
    public int deliverOrder(Long orderId, String updateBy)
    {
        ShopOrder order = checkOrderExists(orderId);
        if (!STATUS_UNDELIVERED.equals(order.getStatus()))
        {
            throw new ServiceException("订单当前状态不允许发货，仅待发货订单可执行发货");
        }
        ShopOrder update = new ShopOrder();
        update.setOrderId(orderId);
        update.setStatus(STATUS_DELIVERED);
        update.setDeliveryTime(new Date());
        update.setUpdateBy(updateBy);
        return orderMapper.updateOrder(update);
    }

    @Override
    @Transactional
    public int deleteOrderByIds(Long[] orderIds)
    {
        for (Long orderId : orderIds)
        {
            ShopOrder order = checkOrderExists(orderId);
            if (!STATUS_FINISHED.equals(order.getStatus())
                && !STATUS_CANCELED.equals(order.getStatus())
                && !STATUS_REFUNDED.equals(order.getStatus()))
            {
                throw new ServiceException(String.format("订单 %s 尚在流转中，不允许删除", order.getOrderNo()));
            }
        }
        return orderMapper.deleteOrderByIds(orderIds);  // XML 中为 update del_flag='2' 逻辑删除
    }
}
```

Controller 只做权限、审计日志与参数编排（`@PreAuthorize` 权限标识与 sys_menu 的 perms 一一对应）：

```java
@RestController
@RequestMapping("/shop/order")
public class ShopOrderController extends BaseController
{
    @Autowired
    private IShopOrderService orderService;

    @PreAuthorize("@ss.hasPermi('shop:order:deliver')")
    @Log(title = "订单管理", businessType = BusinessType.UPDATE)
    @PutMapping("/deliver/{orderId}")
    public AjaxResult deliver(@PathVariable Long orderId)
    {
        return toAjax(orderService.deliverOrder(orderId, getUsername()));
    }

    @PreAuthorize("@ss.hasPermi('shop:order:export')")
    @Log(title = "订单管理", businessType = BusinessType.EXPORT)
    @PostMapping("/export")
    public void export(HttpServletResponse response, ShopOrder order)
    {
        List<ShopOrder> list = orderService.selectOrderList(order);
        ExcelUtil<ShopOrder> util = new ExcelUtil<ShopOrder>(ShopOrder.class);
        util.exportExcel(response, list, "订单数据");
    }
}
```

Mapper XML 关键点：逻辑删除全链路生效 + 日期范围检索复用 BaseEntity 的 params 约定：

```xml
<select id="selectOrderList" parameterType="ShopOrder" resultMap="ShopOrderResult">
    <include refid="selectOrderVo"/>
    <where>
        del_flag = '0'
        <if test="orderNo != null and orderNo != ''">
            AND order_no like concat('%', #{orderNo}, '%')
        </if>
        <if test="status != null and status != ''">
            AND status = #{status}
        </if>
        <if test="params.beginTime != null and params.beginTime != ''">
            AND date_format(create_time,'%Y%m%d') &gt;= date_format(#{params.beginTime},'%Y%m%d')
        </if>
        <if test="params.endTime != null and params.endTime != ''">
            AND date_format(create_time,'%Y%m%d') &lt;= date_format(#{params.endTime},'%Y%m%d')
        </if>
    </where>
    order by order_id desc
</select>
<update id="deleteOrderByIds" parameterType="Long">
    update shop_order set del_flag = '2' where order_id in
    <foreach item="orderId" collection="array" open="(" separator="," close=")">
        #{orderId}
    </foreach>
</update>

```

#### 第 4 步：前端实现（字典驱动 + 按状态渲染操作按钮）

`ruoyi-ui/src/api/shop/order.js` 封装 REST 调用；`ruoyi-ui/src/views/shop/order/index.vue` 关键片段——状态列用字典组件渲染，操作按钮按状态机条件显示，权限用 `v-hasPermi` 指令与后端 `@PreAuthorize` 同源：

```vue
<el-table-column label="订单状态" align="center" prop="status" width="100">
  <template slot-scope="scope">
    <dict-tag :options="dict.type.shop_order_status" :value="scope.row.status"/>
  </template>
</el-table-column>
<el-table-column label="操作" align="center">
  <template slot-scope="scope">
    <el-button v-if="scope.row.status === '1'" size="mini" type="text"
      icon="el-icon-truck" @click="handleDeliver(scope.row)"
      v-hasPermi="['shop:order:deliver']">发货</el-button>
    <el-button v-if="scope.row.status === '0' || scope.row.status === '1'"
      size="mini" type="text" icon="el-icon-circle-close"
      @click="handleCancel(scope.row)"
      v-hasPermi="['shop:order:cancel']">取消</el-button>
  </template>
</el-table-column>

```

```javascript
export default {
  name: "Order",
  dicts: ['shop_order_status', 'shop_pay_type'],   // 声明式加载字典
  methods: {
    getList() {
      this.loading = true
      listOrder(this.addDateRange(this.queryParams, this.dateRange)).then(response => {
        this.orderList = response.rows
        this.total = response.total
        this.loading = false
      })
    },
    handleDeliver(row) {
      this.$modal.confirm('是否确认对订单"' + row.orderNo + '"执行发货？').then(() => {
        return deliverOrder(row.orderId)
      }).then(() => {
        this.getList()
        this.$modal.msgSuccess("发货成功")
      }).catch(() => {})
    }
  }
}
```

#### 第 5 步：验证闭环

```bash
# 后端：编译 + Mapper XML 随 classpath 打包确认
mvn -B compile -pl ruoyi-system,ruoyi-admin -am -DskipTests
ls ruoyi-system/target/classes/mapper/shop/   # ShopOrderMapper.xml 已进 classpath

# 前端：JS/脚本块语法校验（完整构建走 npm run build:prod）
node --check ruoyi-ui/src/api/shop/order.js
```

配合阶段3 的 Hooks，这些验证在 Claude Code 会话内自动发生：PostToolUse 钩子拦截规范违规，Stop 钩子保证 `mvn verify` 通过才允许交付。

#### 这个案例说明了什么

| **Harness 原则** | **在本案例中的体现** |
| :--- | :--- |
| 信息层：项目即文档 | Claude 先读 SysNotice 全链路，零额外提示对齐 RuoYi 编码风格 |
| 明确意图：设计先行 | 状态机、非目标、验收标准写进设计文档再动代码 |
| 约束层：规则机械化 | 权限标识 `模块:实体:动作`、del_flag 逻辑删除、ID 避让区间 |
| 业务规则收敛 | 状态流转校验全部在 Service 层，Controller/前端只做展示与编排 |
| 验证闭环 | 编译 + classpath 检查 + JS 语法校验，全部命令化、可进 Hooks/CI |

### 踩坑指南：容易犯的一些错误

#### CLAUDE.md 写太长

**症状**：Claude 的输出质量反而下降了，经常忽略部分规则。

**原因**：CLAUDE.md 每次会话都会整体注入上下文，写太长会挤占 "正事" 的空间。

**解法**：砍到 50-100 行。如果超过，把内容移到 docs/ 并在 CLAUDE.md 中只留导航表；确需强制加载的细则再用 `@docs/xxx.md` 导入。

#### Linter 规则太多，Agent 陷入死循环

**症状**：Claude 修了一个 Checkstyle 错误，又触发了另一个 ArchUnit 错误，反复循环。

**解法**：

* 逐条添加 Linter 规则，每加一条都让 Claude 试跑一遍
* 确保每条规则的 FIX 信息**给出具体代码片段**
* 互相冲突的规则只保留一条

#### Hook 太重，拖慢每一次编辑

**症状**：PostToolUse 钩子里跑 `mvn clean verify`，Claude 每改一个文件都要等几分钟。

**解法**：分层放检查——`PostToolUse` 只做秒级的轻量检查（行数、正则、单文件 checkstyle），全量 `mvn verify` 放到 `Stop` 钩子（并给足 `timeout`），最重的留给 CI。

#### Java 版本与依赖版本踩坑（Java 8 专属）

**症状**：升级了 Checkstyle 或某个依赖后，本地 `mvn verify` 抛 `UnsupportedClassVersionError`。

**原因**：很多工具的最新版已不再支持 Java 8 运行时（Checkstyle 10+、Spring 6+、Maven 4+ 等）。

**解法**：

* `pom.xml` 中显式锁定 Java 8 兼容版本（参考 pom.xml 一节的版本表）
* `dependabot.yml` 配置 `ignore` 阻止误升级：

```yaml
version: 2
updates:
  - package-ecosystem: maven
    directory: "/"
    schedule:
      interval: weekly
    ignore:
      - dependency-name: "com.puppycrawl.tools:checkstyle"
        update-types: ["version-update:semver-major"]
      - dependency-name: "org.springframework.boot:*"
        update-types: ["version-update:semver-major"]
```

#### 架构约束太严，阻碍合理的跨层调用

**症状**：某些合理的代码模式被 ArchUnit 拦截，团队开始绕过规则。

**解法**：设置 "豁免白名单" 机制：

```java
@ArchTest
public static final ArchRule controllerMustNotUseMapperExceptLegacy = noClasses()
    .that().resideInAPackage("..controller..")
    .and().resideOutsideOfPackage("..controller.legacy..")
    .should().dependOnClassesThat().resideInAPackage("..mapper..");
```

#### Doc-gardening 没人管，文档比不写还误导

**症状**：Claude 参考了过时文档，写出的代码基于错误的假设。

**解法**：

* 在 CI 中加文档新鲜度检查（见 CI 管线一节）
* 每两周跑一次 doc-gardener 子代理（或 `claude -p "@doc-gardener 巡检 docs/"`）
* 设计文档加 `status` 字段，过期的标记为 `deprecated`

#### 过度依赖 Agent，忘了 "审查环境"

**解法**：每周花 30 分钟做一次 "环境审查"：

* 最近一周的 CI 失败率是否上升？
* Checkstyle / ArchUnit 规则和 Hooks 是否覆盖了新出现的 bad pattern？
* CLAUDE.md、`.claude/settings.json` 和 docs/ 是否跟代码库一致？
* 是否有人尝试升级 SB 3.x / Java 11+？

### Harness Engineering 落地清单

```plain
□ 阶段1: 信息层
  □ 创建 CLAUDE.md（/init 生成后裁剪到 50-100 行，含 JDK/SB/Maven 版本基线）
  □ 建立 docs/ 结构化目录
  □ 编写架构文档 + 编码规范文档
  □ 设计文档模板（含 Status 标记，配合 Plan Mode 审批）

□ 阶段2: 约束层
  □ 配置 maven-enforcer-plugin（锁定 JDK 1.8 + Maven 3.6.3）
  □ 配置 ArchUnit（分层依赖 + 禁字段注入 + 禁裸 HTTP 客户端）
  □ 配置 Checkstyle 9.3 + 自定义错误信息（必须显式声明版本）
  □ 配置 SpotBugs + JaCoCo（行覆盖率 ≥ 80%）
  □ 配置 .claude/settings.json（permissions allow/deny 提交进 git）
  □ CI: setup-java@8 + setup-maven@3.6.3 + mvn -B clean verify
  □ 把团队口头约定翻译成机械规则

□ 阶段3: 自动化层（可选，长期项目推荐）
  □ PostToolUse 钩子（编辑后轻量检查）+ Stop 钩子（结束前 mvn verify）
  □ .claude/commands/cleanup.md 斜杠命令 + claude -p 定时无头执行
  □ .claude/agents/ 子代理（doc-gardener 等）
  □ Git Worktree 隔离验证脚本（含 spring-boot:run + actuator/health）
  □ 可观测性堆栈（Actuator + Micrometer + Loki + Prometheus，可经 MCP 接入）
  □ 文档新鲜度自动检查
  □ Dependabot 配置（防止误升级到 Java 11+ 工具版本）

□ 持续维护
  □ 每周 30 分钟"环境审查"
  □ 每月回顾并更新 ArchUnit / Checkstyle / Hooks 规则
  □ 每两周运行 doc-gardener 子代理
```

**记住**：Harness Engineering 的核心不是搭建复杂的基础设施，而是一个简单的闭环——**约束 → 告知 → 验证 → 纠正**。在 Claude Code 里，这个闭环有一一对应的原生机制：CLAUDE.md 负责约束与告知，Hooks 与 Linter 负责验证，退出码 2 的 stderr 反馈负责纠正。从一份 CLAUDE.md 和一条 ArchUnit 规则开始，比什么都不做强一百倍。

# 基于 Claude Code 和 Harness 开发 Python 智能客服应用

## Harness 三阶段落地

首先我们要解决的是"让 Claude Code 在这个项目里**长期、稳定、可控地**工作"。Harness Engineering 的落地不是"一把梭"，而是渐进式的三步走：

```plain
阶段1: 信息层（1-2天）         阶段2: 约束层（3-5天）         阶段3: 自动化层（1-2周）
┌───────────────────┐       ┌───────────────────┐       ┌───────────────────┐
│ CLAUDE.md 地图模式  │  →    │ 分层架构 + Linter   │  →    │ Hooks 自验证闭环    │
│ docs/ 结构化文档    │       │ CI 约束检查         │       │ 无头模式清理 Agent  │
│ 编码规范文档化      │       │ 错误信息含修复指令   │       │ 导入检查/健康检查自动化│
└───────────────────┘       └───────────────────┘       └───────────────────┘
  适合：所有项目               适合：中期项目                适合：长期维护项目
  收益：Agent 输出一致性 ↑     收益：代码质量可控            收益：人工审查量 ↓↓↓
```

**不要一步到位。** 阶段1 已经能带来显著提升，阶段2 是质变点，阶段3 是锦上添花。

### 阶段1：信息层——让 Claude Code "看得懂" 这个 RAG 项目

#### CLAUDE.md：写地图，不写百科全书

Claude Code 在每次会话启动时会自动加载项目根目录的 `CLAUDE.md`。推荐用"地图模式"——`CLAUDE.md` 只放导航和硬性规则，细节放到 `docs/` 里按需加载。先用 `/init` 生成初稿，再按下面的模板裁剪：

```plain
# CLAUDE.md

## 项目简介
银行 RAG 智能客服系统：Streamlit 多页面 Web 应用 + LangGraph Agent + Chroma 向量库。

## 技术栈基线（不允许擅自升级）
- Python: 3.10（conda 环境 agent）
- LangChain 生态：严格按 requirements.txt 锁定版本（langchain 0.3.12 / langgraph 0.2.59 等），
  不可升级任何 langchain-* 包——生态 API 变动频繁，升级必须人工评审
- Streamlit: 1.41.1，多页面用 st.navigation + st.Page（不用 pages/ 目录）
- 向量库: Chroma 0.5.23，持久化目录固定为 kb/<知识库名>/vectorstore

## 快速导航
| 你想做什么 | 去哪里看 |
|-----------|---------|
| 了解系统架构 | docs/architecture/overview.md |
| 了解模块边界和依赖规则 | docs/architecture/boundaries.md |
| 了解编码规范 | docs/conventions/README.md |
| 了解当前迭代任务 | docs/plans/current-sprint.md |
| 了解检索工具约定 | docs/conventions/rag-tools.md |

## 硬性规则（必须遵守，CI 会验证）
1. 依赖方向：utils → tools → webui → rag.py，禁止反向导入（utils 不得 import tools/webui）
2. 可选依赖（langchain_ollama / xinference 等）必须函数内延迟导入（lazy import）
3. 检索工具命名必须为 <知识库名>_knowledge_base_tool，页面靠该后缀反推知识库名
4. 外部服务连接失败用 st.toast 提示并返回空列表，禁止向页面抛异常
5. 禁止 print() 调试输出，页面反馈用 st.*，脚本日志用 logging
6. 单文件 ≤ 300 行；新增公共函数必须写中文注释
7. 创建 Chroma 实例前必须先 clear_system_cache()（Streamlit rerun 缓存冲突）

## 常用命令
- 启动应用：streamlit run rag.py
- 模块自检：python -c "import utils, tools, webui"
- 模型层自测：python utils.py
- 代码检查：ruff check . 与 lint-imports

## 提交规范
- feat / fix / refactor / docs / test
```

**关键设计原则**：

* **CLAUDE.md 控制在 50-100 行**，超过就把内容移到 `docs/` 只留导航
* **"你想做什么 → 去哪里看"** 比"这是什么"更有效——面向任务而非面向知识
* **硬性规则单独列出**，这些是 CI 和 Hooks 会强制验证的，不是"建议"
* 会话中发现 Claude 反复犯同一个错误时，直接以 `#` 开头输入一条指令，Claude Code 会把它追加进 CLAUDE.md，实现规则的持续沉淀

#### docs/ 目录：结构化知识库

```plain
docs/
├── architecture/
│   ├── overview.md         # 本文开头的架构图 + 模块职责
│   └── boundaries.md       # utils → tools → webui 依赖规则
├── conventions/
│   ├── README.md
│   ├── rag-tools.md        # 工具命名、score_threshold、source 前缀约定
│   └── streamlit.md        # session_state、st.status、rerun 使用规范
├── design/
│   ├── feature-kb-manage.md
│   └── feature-rag-chat.md
├── plans/
│   └── current-sprint.md
└── reference/
    └── error-codes.md
```

每个文档头部加元信息（`last_updated` / `status` / `owner`），供后文的 doc-gardener 子代理自动扫描过期文档。

#### 设计文档模板（配合 Plan Mode）

新功能（如课后作业的"网络搜索工具"）动手前，先在 Plan Mode 下让 Claude 填写设计文档，人工审批后再实现：

```plain
# Feature: 网络搜索兜底工具

## Status: 📝 Draft | 📋 Approved | 🚧 In Progress | ✅ Implemented

## 目标
知识库检索无结果时，Agent 自动调用 DuckDuckGo 搜索联网兜底。

## 非目标
不做搜索结果缓存；不改动现有知识库检索逻辑。

## 技术方案
- tools/：新增 web_search_tool.py，工具名 web_search_tool
- webui/rag_chat_page.py：把该工具并入 bind_tools 列表，前端标注"联网结果"

## 验收标准
* 知识库命中时不触发联网搜索
* 联网结果在 st.status 中明确标注来源
```

### 阶段2：约束层——让 Agent "不能犯错"

把 CLAUDE.md 里的硬性规则翻译成机器可执行的检查。Python 项目的对应工具链：

| **团队口头约定** | **机械化规则** | **实现方式** |
| :--- | :--- | :--- |
| "不要乱升级依赖" | requirements.txt 全量锁版本 | `pip install` + CI 中 `pip check` |
| "模块边界要清晰" | utils 不得 import tools/webui | import-linter 分层契约 |
| "不要 print 调试" | 禁止 print() | Ruff `T201`（flake8-print） |
| "文件要短" | 单文件 ≤ 300 行 | 自定义检查脚本（见阶段3 Hook） |
| "可选依赖延迟导入" | 顶层不得 import langchain_ollama 等 | 自定义检查脚本 / Code Review |
| "改完必须能跑" | 所有模块可导入 | CI 中 `python -c "import utils, tools, webui"` |
| "危险命令不能跑" | 禁止 rm -rf / 读 .env | Claude Code `settings.json` deny 规则 |

**经验法则**：如果一条规则在 Code Review 中被提过 3 次以上，就应该写成 Linter 规则。

#### 分层依赖检查：import-linter

新增开发依赖并创建 `.importlinter`：

```properties
[importlinter]
root_packages =
    webui
    tools
    utils

[importlinter:contract:layers]
name = 分层依赖：webui → tools → utils，禁止反向导入
type = layers
layers =
    webui
    tools
    utils
```

运行 `lint-imports`，一旦 `utils.py` 里出现 `import webui` 这类反向依赖，构建直接失败。

#### Ruff 配置（`pyproject.toml`）

```toml
[tool.ruff]
target-version = "py310"
line-length = 120

[tool.ruff.lint]
# E/F: 基础错误; I: import 排序; T20: 禁止 print; B: 常见 bug 模式
select = ["E", "F", "I", "T20", "B"]

[tool.ruff.lint.per-file-ignores]
# utils.py 末尾的 __main__ 自测允许 print
"utils.py" = ["T201"]
```

#### 错误信息即 Prompt

这是 Harness Engineering 最有杠杆的实践之一：**每条检查报错都必须包含三要素——问题是什么、怎么修、去哪看文档**。万能公式：

```plain
❌ [什么错了]
✅ FIX: [怎么改，给出代码片段]
📖 See: [哪个文档有详细说明]
```

Ruff 的报错信息不可自定义，但可以用轻量检查脚本补充项目私有规则。`scripts/check_conventions.py`：

```python
"""项目私有约定检查：报错信息本身就是给 Claude 的修复提示。"""
import sys
from pathlib import Path

FORBIDDEN_TOP_IMPORTS = ["langchain_ollama", "xinference_client", "langchain_chroma"]

def main() -> int:
    errors = []
    for py in Path(".").glob("**/*.py"):
        if "kb" in py.parts or ".venv" in py.parts:
            continue
        lines = py.read_text(encoding="utf-8").splitlines()

        # 规则：单文件 ≤ 300 行
        if len(lines) > 300:
            errors.append(
                f"❌ {py} 有 {len(lines)} 行（上限 300）。\n"
                f"✅ FIX: 按页面/工具职责拆分模块。\n"
                f"📖 See: docs/conventions/README.md"
            )

        # 规则：可选依赖必须延迟导入（只检查模块顶层）
        for n, line in enumerate(lines, 1):
            if line.startswith(("import ", "from ")) and any(m in line for m in FORBIDDEN_TOP_IMPORTS):
                errors.append(
                    f"❌ {py}:{n} 顶层导入了可选依赖：{line.strip()}\n"
                    f"✅ FIX: 移到使用它的函数内部（lazy import），避免未安装时模块加载失败。\n"
                    f"📖 See: docs/conventions/README.md"
                )

    print("\n\n".join(errors) or "✅ 约定检查通过")
    return 1 if errors else 0

if __name__ == "__main__":
    sys.exit(main())
```

Agent 看到这种报错，不需要任何额外提示就能自动修复。**你写的每一条检查规则，本质上都是一个自动触发的 Prompt。**

#### CI 管线（`.github/workflows/harness-checks.yml`）

```yaml
name: Harness Checks
on: [pull_request]

jobs:
  quality-gates:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - uses: actions/setup-python@v5
        with:
          python-version: '3.10'
          cache: pip

      - name: Install（锁定版本安装）
        run: |
          pip install -r requirements.txt
          pip install ruff import-linter
          pip check   # 依赖冲突直接失败

      - name: Lint
        run: |
          ruff check .
          lint-imports
          python scripts/check_conventions.py

      - name: Import Smoke Test（所有模块可导入）
        run: python -c "import utils, tools, webui"
        env:
          OPENAI_API_KEY: dummy   # 导入自检不真正调用 API
```

CI 是最后一道防线。但对 Claude Code 来说，更高杠杆的做法是把同样的检查前移到本地会话内——见阶段3 的 Hooks。

### 阶段3：自动化层——让 Claude Code 自我验证和自我修复

#### Hooks：改完即验证的闭环

Hooks 是 Claude Code 的确定性护栏：在指定生命周期（如 `PostToolUse`、`Stop`）自动执行 shell 命令，**退出码 2 时 stderr 会直接喂回给 Claude**，触发它自动修复——正好和阶段2 "错误信息即 Prompt" 形成闭环。

项目级配置 `.claude/settings.json`（提交进 git，全团队共享）：

```json
{
  "permissions": {
    "allow": [
      "Bash(streamlit run *)",
      "Bash(python -c *)",
      "Bash(python utils.py)",
      "Bash(ruff check *)",
      "Bash(lint-imports)",
      "Bash(git diff *)",
      "Bash(git log *)"
    ],
    "deny": [
      "Bash(git push --force*)",
      "Bash(rm -rf *)",
      "Read(./.env*)"
    ]
  },
  "hooks": {
    "PostToolUse": [
      {
        "matcher": "Edit|Write",
        "hooks": [
          { "type": "command", "command": "bash .claude/hooks/check-python.sh" }
        ]
      }
    ],
    "Stop": [
      {
        "hooks": [
          { "type": "command", "command": "bash .claude/hooks/verify-before-stop.sh", "timeout": 300 }
        ]
      }
    ]
  }
}
```

`.claude/hooks/check-python.sh`——每次 Claude 编辑 `.py` 文件后立即做秒级轻量检查：

```bash
#!/bin/bash
# stdin 是 hook 的 JSON 输入，取出刚被编辑的文件路径
file=$(jq -r '.tool_input.file_path // empty')
[[ "$file" != *.py ]] && exit 0

# Ruff 单文件检查（含 T201 禁 print）
if ! ruff check "$file" >&2; then
  echo "✅ FIX: 按上方 Ruff 报错逐条修复；print() 换成 st.* 或 logging。" >&2
  echo "📖 See: docs/conventions/README.md" >&2
  exit 2   # 退出码 2：stderr 反馈给 Claude，让它立即修复
fi

# 项目私有约定（行数上限、可选依赖延迟导入）
if ! python scripts/check_conventions.py >&2; then
  exit 2
fi
exit 0
```

`.claude/hooks/verify-before-stop.sh`——Claude 声称"做完了"之前，强制跑一次全量校验：

```bash
#!/bin/bash
# 无 Python 改动就放行，避免每次对话结束都全量校验
git diff --name-only HEAD | grep -q '\.py$' || exit 0

{
  ruff check . &&
  lint-imports &&
  python scripts/check_conventions.py &&
  OPENAI_API_KEY=dummy python -c "import utils, tools, webui"
} > /tmp/verify.log 2>&1

if [ $? -ne 0 ]; then
  echo "❌ 全量校验失败，不能结束任务。最近报错：" >&2
  tail -n 40 /tmp/verify.log >&2
  echo "✅ FIX: 根据上面的 Ruff / import-linter / 导入自检报错逐条修复后重试。" >&2
  exit 2   # 阻止 Claude 停下来，带着报错继续修
fi
exit 0
```

有了这两个钩子，"约束 → 告知 → 验证 → 纠正"的闭环就完全自动化了：Step 7 里"贴报错让 Claude Code 修"的动作，现在由 Hooks 自动完成。

#### 后台清理 Agent：自定义斜杠命令 + 无头模式

把清理任务写成自定义斜杠命令 `.claude/commands/cleanup.md`（提交进 git，团队共用）：

```markdown
---
description: RAG 项目卫生清理，每个问题生成独立修复 PR
allowed-tools: Bash(ruff *), Bash(python *), Bash(git *), Bash(gh *)
---

# 任务：代码库卫生清理

请执行以下检查，对每个发现的问题生成独立的修复 PR：

## 检查清单
1. **超长文件**：找出超过 300 行的 .py 文件，按职责拆分
2. **未使用的 import**：ruff check --select F401 清理
3. **顶层导入可选依赖**：langchain_ollama 等必须函数内延迟导入
4. **TODO/FIXME**：列出所有 TODO，超过 30 天未处理则生成清理 PR
5. **过时文档**：检查 docs/design/ 中 status 为 Draft 且超过 30 天的文档
6. **孤儿知识库**：kb/ 下存在 vectorstore 但 files/ 为空的目录，汇总清单

## 约束
- 每个修复作为独立 PR，不要混在一起
- 每个 PR 修改后必须确保 ruff check . 和 python -c "import utils, tools, webui" 通过
- 不允许升级 requirements.txt 中任何 langchain-* 版本
- 如果不确定某个修改是否安全，跳过并在 PR 中标注原因
```

交互式会话里输入 `/cleanup` 即可触发；定时任务用**无头模式**（`claude -p`）配合 cron / Windows 计划任务：

```bash
# 每周一凌晨 2 点自动清理（crontab）
0 2 * * 1  cd /path/to/rag-customer && claude -p "/cleanup" \
    --permission-mode acceptEdits \
    --allowedTools "Bash(ruff *)" "Bash(git *)" "Bash(gh pr create*)" \
    --output-format json > /var/log/claude-cleanup.log 2>&1
```

文档巡检拆成**子代理**（`.claude/agents/doc-gardener.md`），与代码清理各用独立上下文并行执行：

```markdown
---
name: doc-gardener
description: 扫描 docs/ 下的过期文档并标记 deprecated。检查文档新鲜度时主动使用。
tools: Read, Grep, Glob, Edit, Bash(git log *)
---

你是文档园丁。职责：
1. 扫描 docs/**/*.md 头部的 last_updated 与 status 元信息
2. 超过 60 天未更新且 status 为 active 的，核对代码后改为 deprecated 或更新内容
3. status 为 draft 且超过 30 天的，汇总清单输出
禁止修改 docs/ 以外的任何文件。
```

#### Git Worktree：并行会话隔离验证

每个 worktree 一个独立的 Claude 会话，互不污染。针对 Streamlit 应用的端到端验证脚本：

```bash
#!/bin/bash
BRANCH=$1
WORKTREE_DIR="/tmp/agent-verify-$(date +%s)"

echo "🔧 创建 worktree: $WORKTREE_DIR"
git worktree add "$WORKTREE_DIR" "$BRANCH"
cd "$WORKTREE_DIR"

echo "📦 安装依赖并跑静态校验..."
pip install -r requirements.txt -q
ruff check . || { echo "❌ ruff 失败"; exit 1; }
lint-imports || { echo "❌ 分层依赖违规"; exit 1; }
OPENAI_API_KEY=dummy python -c "import utils, tools, webui" || { echo "❌ 模块导入失败"; exit 1; }

echo "🚀 启动 Streamlit 应用做健康检查..."
streamlit run rag.py --server.headless true --server.port 8599 > /tmp/app.log 2>&1 &
APP_PID=$!

for i in {1..30}; do
  sleep 2
  if curl -sf http://localhost:8599/_stcore/health | grep -q 'ok'; then
    echo "✅ 健康检查通过"
    kill $APP_PID 2>/dev/null
    cd - && git worktree remove "$WORKTREE_DIR"
    echo "✅ 所有验证通过"
    exit 0
  fi
done

echo "❌ 应用启动失败，最近日志："
tail -n 50 /tmp/app.log
kill $APP_PID 2>/dev/null
exit 1
```

也可以在 worktree 里直接开无头验证会话，让 Claude 自己解读失败日志：

```bash
git worktree add /tmp/verify-feat feat/web-search
cd /tmp/verify-feat && claude -p "运行上面的验证脚本，如失败请分析根因并输出修复建议（不要改代码）"
```

### Harness 落地清单

```plain
□ 阶段1: 信息层
  □ 创建 CLAUDE.md（/init 生成后裁剪到 50-100 行，含依赖锁版本基线）
  □ 建立 docs/ 结构化目录（architecture / conventions / design / plans）
  □ 沉淀 RAG 项目约定：工具命名、score_threshold、source 前缀、lazy import
  □ 设计文档模板（含 Status 标记，配合 Plan Mode 审批）

□ 阶段2: 约束层
  □ requirements.txt 全量锁版本 + CI 中 pip check
  □ 配置 import-linter（webui → tools → utils 分层契约）
  □ 配置 Ruff（T201 禁 print 等）+ scripts/check_conventions.py 私有规则
  □ 配置 .claude/settings.json（permissions allow/deny 提交进 git）
  □ CI: setup-python@3.10 + Lint + 模块导入冒烟测试
  □ 把团队口头约定翻译成机械规则

□ 阶段3: 自动化层（可选，长期项目推荐）
  □ PostToolUse 钩子（编辑后 ruff + 约定检查）+ Stop 钩子（结束前全量校验）
  □ .claude/commands/cleanup.md 斜杠命令 + claude -p 定时无头执行
  □ .claude/agents/doc-gardener.md 子代理
  □ Git Worktree 隔离验证脚本（含 streamlit headless 启动 + /_stcore/health）
  □ 文档新鲜度自动检查

□ 持续维护
  □ 每周 30 分钟"环境审查"（CI 失败率 / 规则覆盖 / CLAUDE.md 与代码一致性）
  □ 每月回顾并更新 Ruff / import-linter / Hooks 规则
  □ 每两周运行 doc-gardener 子代理
```

**记住**：Harness Engineering 的核心不是搭建复杂的基础设施，而是一个简单的闭环——**约束 → 告知 → 验证 → 纠正**。在 Claude Code 里，这个闭环有一一对应的原生机制：CLAUDE.md 负责约束与告知，Hooks 与 Linter 负责验证，退出码 2 的 stderr 反馈负责纠正。从一份 CLAUDE.md 和一条 import-linter 契约开始，比什么都不做强一百倍。

## 基于 Claude Code (Harness) 全流程开发 RAG 智能客服系统

需求：我们要做一个**银行智能客服系统**。用户在网页里提问（如"如何查询账户余额？"），系统会：

1. 从**行业知识库**中检索最相关的内容；
2. 让大模型基于检索到的内容生成**有依据的回答**；
3. 在界面上**流式**展示回答，并把"调用了哪个知识库、检索到什么"过程透明地展示给用户。

### 系统最终架构图

```plain
┌───────────────────────────────────────────────────────────┐
│                     rag.py  (Streamlit 入口)                │
│              侧边栏 Logo + 多页面导航（对话 / 设置）         │
└───────────────┬───────────────────────────┬───────────────┘
                │                           │
        ┌───────▼────────┐         ┌────────▼─────────────┐
        │ rag_chat_page  │         │ knowledge_base_page  │
        │  智能客服对话   │         │   行业知识库管理      │
        │ (LangGraph)    │         │ (上传/切分/向量化)    │
        └───────┬────────┘         └────────┬─────────────┘
                │                           │
        ┌───────▼────────┐                  │
        │ naive_rag_tool │◄─────────────────┘
        │  检索工具(Tool) │     共用向量库 kb/<name>/vectorstore
        └───────┬────────┘
                │
        ┌───────▼─────────────────────────────────────────┐
        │ utils.py  模型接入层                              │
        │ OpenAI / Ollama / Xinference 的 LLM & Embedding  │
        └───────┬─────────────────────────────────────────┘
                │
        ┌───────▼────────┐     ┌──────────────────────────┐
        │ Chroma 向量库   │     │ OpenAI Embedding / Chat   │
        └────────────────┘     └──────────────────────────┘
```

### 核心技术栈

| **技术** | **作用** |
| :--- | :--- |
| **Streamlit** | 快速构建 Web 交互界面 |
| **LangChain** | 模型接入、文档加载与切分、检索工具封装 |
| **LangGraph** | 构建 Agent 状态机（`StateGraph`），实现"模型 ↔ 工具"循环 |
| **Chroma** | 本地向量数据库，持久化存储知识库 |
| **OpenAI / Ollama / Xinference** | 多平台 LLM 与 Embedding 模型 |

### 为什么用 Claude Code 开发

* Claude Code 是 Anthropic 官方的**智能体编程工具（Agentic Coding Harness）**，不仅生成代码，还能**读项目、改文件、跑命令、修 Bug**——所有操作都在你的终端里、在你的授权下完成。
* 它自带完整的工具体系（文件读写、代码搜索、Shell 执行、子代理等），并通过 `CLAUDE.md` 沉淀项目记忆，天然适合工程化协作。
* 我们采用**分步交付**：每一步给一个清晰的提示词（Prompt），产出一个模块，验证后再进入下一步——这正是工程化使用 AI 编程的正确姿势。

## Claude Code 与环境准备

### 安装 Claude Code

```plain
# 通过 npm 全局安装
npm install -g @anthropic-ai/claude-code

# 验证安装
claude --version
```

### 配置认证

```plain
# 方式一：首次启动时按引导登录（推荐，使用 Claude 订阅或 Console 账号）
claude
# 首次运行会自动打开浏览器完成 OAuth 登录

# 方式二：环境变量（适合 CI / API 计费方式）
export ANTHROPIC_API_KEY="sk-ant-xxxxxxxxxxxxxxxxxxxx"
```

Windows PowerShell 下设置环境变量：

```plain
setx ANTHROPIC_API_KEY "sk-ant-xxxxxxxxxxxxxxxxxxxx"
```

注意：`setx` 设置后需重启终端/IDE 才能生效。

另外，本项目**应用本身**调用 OpenAI 的 Chat / Embedding 模型，因此还需要为应用配置：

```plain
setx OPENAI_API_KEY "sk-xxxxxxxxxxxxxxxxxxxx"
setx OPENAI_BASE_URL "https://api.openai.com/v1"
```

这两组密钥职责不同：`ANTHROPIC_API_KEY` 给 Claude Code（开发工具）用，`OPENAI_API_KEY` 给 RAG 应用运行时用，不要混淆。

### 启动 Claude Code 并理解权限模式

```plain
# 进入你的项目目录
cd rag-customer

# 启动交互式会话
claude
```

进入会话后，建议先执行 `/init`，让 Claude Code 扫描项目并生成 `CLAUDE.md`（项目记忆文件，记录技术栈、目录约定、常用命令）。

Claude Code 常用的几种权限模式（按 Shift+Tab 循环切换，按需选择）：

| **模式** | **说明** | **适用场景** |
| :--- | :--- | :--- |
| **默认模式（Default）** | 每次改文件、跑命令都需你确认 | 教学演示、初学者，安全可控 |
| **自动接受编辑（Auto-Accept Edits）** | 自动改文件，但执行命令仍需确认 | 熟练后提速 |
| **计划模式（Plan Mode）** | 只读分析、先产出方案，不改任何文件 | 架构设计、代码审查 |
| **跳过权限（**`--dangerously-skip-permissions`**）** | 自动改文件 + 自动跑命令 | 隔离环境中信任度高的批量任务 |

## 需求拆解与架构设计（用 Claude Code 做技术方案）

不要一上来就让 Claude Code"写一个智能客服系统"。要先让它和你一起**做技术方案**，把大需求拆成小步骤。这是 AI 协作开发的第一步——**对齐认知**。这一步推荐使用**计划模式（Plan Mode）**，让它只读分析、只出方案不动代码。

### 提示词：让 Claude Code 输出技术方案

**🔹**\*\* Prompt（架构设计，建议在 Plan Mode 下执行）\*\*

```plain
我要开发一个 RAG 智能客服系统，技术栈限定为：
- Web 界面：Streamlit
- Agent 编排：LangGraph
- 向量库：Chroma
- 模型：支持 OpenAI / Ollama / Xinference 三个平台，Embedding 默认用 OpenAI

功能需求：
1. 一个"知识库管理"页面：可以新建知识库、上传 Markdown 文档、自动切分并向量化入库。
2. 一个"智能客服对话"页面：用户提问后，Agent 自动调用知识库检索工具，
   基于检索结果生成回答，支持流式输出，并展示工具调用过程。
3. 多知识库可选，对话时可以勾选启用哪些知识库。

请先不要写代码。请你输出：
(1) 推荐的项目目录结构；
(2) 每个模块的职责划分；
(3) 建议的开发步骤顺序（从底层到上层）。
```

### Claude Code 给出的方案（预期产出）

Claude Code 会建议如下**目录结构**，这也是我们后续要逐步实现的蓝图：

```plain
rag-customer/
├── rag.py                      # Streamlit 主入口，页面导航
├── requirements.txt            # 依赖清单
├── CLAUDE.md                   # Claude Code 项目记忆（/init 生成）
├── utils.py                    # 模型接入层（LLM / Embedding）+ 通用工具
├── tools/
│   ├── __init__.py
│   └── naive_rag_tool.py       # 基于 Chroma 的 RAG 检索工具
├── webui/
│   ├── __init__.py
│   ├── knowledge_base_page.py  # 知识库管理页面
│   └── rag_chat_page.py        # 智能客服对话页面
├── kb/                         # 知识库根目录（运行时生成）
│   └── <知识库名>/
│       ├── files/              # 原始文档
│       └── vectorstore/        # Chroma 持久化向量库
└── img/                        # Logo 等静态资源
```

**开发步骤顺序（自底向上）：**

1. 初始化项目 + 依赖 → 2. 模型接入层 `utils.py` → 3. RAG 检索工具 → 4. 知识库管理页面 → 5. 对话页面 + Agent → 6. 主入口导航 → 7. 运行调试。

**要点：** 自底向上开发的好处是——每一层都可以**独立验证**（如 `utils.py` 写完就能 `python utils.py` 测试），不会等到最后才发现问题。在 Plan Mode 下确认方案后，退出计划模式再开始动手写代码。

***

## Step 1：项目初始化与依赖管理

### 本步目标

创建项目骨架和 `requirements.txt`，把环境跑起来。

### 提示词

**🔹**\*\* Prompt（初始化项目骨架）\*\*

```plain
请在当前目录创建上面方案确定的项目骨架：
- 创建 tools/、webui/、img/ 目录，并为 tools/ 和 webui/ 添加空的 __init__.py
- 创建一个 requirements.txt，包含以下依赖及锁定版本：
  langchain-openai==0.2.9, langchain-community==0.3.12, ollama==0.4.4,
  xinference-client==1.1.0, streamlit==1.41.1, langgraph==0.2.59,
  tiktoken==0.8.0, chromadb==0.5.23, langchain==0.3.12,
  langchain-text-splitters==0.3.3, langchain-ollama==0.2.2,
  langchain-chroma==0.1.4, langchain-core==0.3.27, openai==1.55.0,
  chardet==5.2.0, onnxruntime
- 创建一个 README.md，写明环境创建、依赖安装、运行命令、配置 OpenAI 环境变量的方法。
```

### 产出：`requirements.txt`（核心依赖）

```plain
langchain-openai==0.2.9
langchain-community==0.3.12
ollama==0.4.4
xinference-client==1.1.0
streamlit==1.41.1
langgraph==0.2.59
tiktoken==0.8.0
chromadb==0.5.23
langchain==0.3.12
langchain-text-splitters==0.3.3
langchain-ollama==0.2.2
langchain-chroma==0.1.4
langchain-core==0.3.27
openai==1.55.0
chardet==5.2.0
onnxruntime
```

### 验证

```plain
conda create -n agent python=3.10 -y
conda activate agent
pip install -r requirements.txt
```

**要点：** 强调**锁定版本号**的重要性。LangChain 生态版本迭代快，不锁版本极易出现 API 不兼容。让 Claude Code 生成依赖时一定要带上版本号。

***

## Step 2：模型接入层 utils.py

这是整个系统的"地基"——把对 OpenAI / Ollama / Xinference 的差异封装起来，上层只管调用统一接口。

### 本步目标

实现以下函数：

* `get_llm_models(platform)`：列出某平台可用的对话模型
* `get_embedding_models(platform)`：列出某平台可用的 Embedding 模型
* `get_chatllm(platform, model, ...)`：返回一个 LangChain Chat 模型对象
* `get_embedding_model(platform, model, ...)`：返回一个 Embedding 模型对象
* `get_kb_names()`：列出 `kb/` 目录下的所有知识库
* `get_img_base64(file_name)`：把图片转成 base64（供 Streamlit Logo 用）
* `show_graph(graph)`：在页面上可视化 LangGraph 流程图

### 提示词

**🔹**\*\* Prompt（模型接入层）\*\*

```plain
请创建 utils.py，实现一个多平台模型接入层。要求：

1. 定义常量 PLATFORMS = ["OpenAI", "Ollama", "Xinference"]。

2. get_chatllm(platform_type, model, base_url="", api_key="", temperature=0.1)：
   - OpenAI：用 langchain_openai.ChatOpenAI，base_url 默认 https://api.openai.com/v1，
     api_key 默认从环境变量 OPENAI_API_KEY 读取，开启 streaming=True。
   - Ollama：用 langchain_ollama.ChatOllama，base_url 默认 http://127.0.0.1:11434。
   - Xinference：base_url 默认 http://127.0.0.1:9997/v1，用 OpenAI 兼容接口。

3. get_embedding_model(platform_type="Ollama", model="text-embedding-ada-002", base_url, api_key)：
   - OpenAI：用 langchain_openai.OpenAIEmbeddings。
   - Ollama：用 langchain_ollama.OllamaEmbeddings。
   - Xinference：用 langchain_community 的 XinferenceEmbeddings。

4. get_llm_models / get_embedding_models：
   - Ollama：用 ollama.Client(host=base_url).list() 列出模型，
     对话模型排除 families 含 "bert" 的，Embedding 模型只保留含 "bert" 的。
   - Xinference：用 xinference_client.RESTfulClient，按 model_type 过滤。
   - OpenAI：直接返回 ['gpt-4o', 'gpt-3.5-turbo']。
   - 连接失败要用 st.toast 提示错误并返回空列表，不要抛异常。

5. get_kb_names()：返回当前文件同级 kb/ 目录下的所有子目录名；目录不存在则创建。

6. get_img_base64(file_name)：读取同级 img/ 目录下的图片，返回
   "data:image/png;base64,<编码>" 字符串（注意 Windows 路径兼容）。

7. show_graph(graph)：用 streamlit_flow 把 LangGraph 的节点和边渲染成树状流程图。

每个函数都要写中文注释，方便教学讲解。
```

### 产出：核心代码片段

**统一的对话模型工厂 **`get_chatllm`**：**

```python
def get_chatllm(
        platform_type: Literal[tuple(PLATFORMS)],
        model: str,
        base_url: str = "",
        api_key: str = "",
        temperature: float = 0.1
):
    if platform_type == "Ollama":
        if not base_url:
            base_url = "http://127.0.0.1:11434"
        return ChatOllama(temperature=temperature, model=model, base_url=base_url)
    elif platform_type == "Xinference":
        if not base_url:
            base_url = "http://127.0.0.1:9997/v1"
        if not api_key:
            api_key = "EMPTY"
    elif platform_type == "OpenAI":
        if not base_url:
            base_url = "https://api.openai.com/v1"
        if not api_key:
            api_key = os.getenv('OPENAI_API_KEY')

    # OpenAI / Xinference 都走 OpenAI 兼容接口
    return ChatOpenAI(
        temperature=temperature,
        model_name=model,
        streaming=True,
        base_url=base_url,
        api_key=api_key,
    )
```

**Embedding 模型工厂 **`get_embedding_model`**：**

```python
def get_embedding_model(
        platform_type: Literal[tuple(PLATFORMS)] = "Ollama",
        model: str = "text-embedding-ada-002",
        base_url: str = os.getenv('OPENAI_BASE_URL'),
        api_key: str = os.getenv('OPENAI_API_KEY'),
):
    if platform_type == "Ollama":
        from langchain_ollama import OllamaEmbeddings
        return OllamaEmbeddings(base_url=base_url or "http://127.0.0.1:11434/", model=model)
    elif platform_type == "Xinference":
        from langchain_community.embeddings.xinference import XinferenceEmbeddings
        return XinferenceEmbeddings(server_url=base_url or "http://127.0.0.1:9997/v1", model_uid=model)
    else:  # OpenAI
        from langchain_openai import OpenAIEmbeddings
        return OpenAIEmbeddings(base_url=base_url, api_key=api_key, model=model)
```

**知识库目录扫描 **`get_kb_names`**：**

```python
def get_kb_names():
    kb_root = os.path.join(os.path.dirname(__file__), "kb")
    if not os.path.exists(kb_root):
        os.mkdir(kb_root)
    return [f for f in os.listdir(kb_root) if os.path.isdir(os.path.join(kb_root, f))]
```

### 验证

```plain
python utils.py   # 文件末尾的 __main__ 会打印 Ollama 的 Embedding 模型列表
```

**要点：**

1. **"适配器模式"思想**——`get_chatllm` 用一组 `if/elif` 屏蔽了不同平台的差异，这是接入多模型的经典做法。
2. **OpenAI 兼容接口的威力**——Xinference 也走 `ChatOpenAI`，因为它提供 OpenAI 兼容的 API，只是 `base_url` 不同。
3. **延迟导入（lazy import）**——`OllamaEmbeddings` 等在函数内部 `import`，避免没装某个库时整个模块加载失败。

***

## Step 3：RAG 检索工具 naive_rag_tool.py

这一步把"向量检索"封装成 LangGraph Agent 能直接调用的**工具（Tool）**。这是 RAG 的核心。

### 本步目标

实现 `get_naive_rag_tool(vectorstore_name)`：传入知识库名，返回一个可被 Agent 调用的检索工具。

### 提示词

**🔹**\*\* Prompt（RAG 检索工具）\*\*

```plain
请创建 tools/naive_rag_tool.py，实现 get_naive_rag_tool(vectorstore_name) 函数：

1. 用 langchain_chroma.Chroma 连接已有向量库：
   - collection_name = vectorstore_name
   - embedding_function 用 utils.get_embedding_model(platform_type="OpenAI")
   - persist_directory 指向 项目根目录/kb/<vectorstore_name>/vectorstore

2. 把向量库转成 retriever：
   - search_type = "similarity_score_threshold"
   - search_kwargs = {"k": 3, "score_threshold": 0.15}

3. 用 langchain.tools.retriever.create_retriever_tool 创建工具：
   - 工具名为 "<vectorstore_name>_knowledge_base_tool"
   - 描述为 "search and return information about <vectorstore_name>"

4. 自定义工具的返回格式：把检索到的若干文档整理成
   {"已知内容 1": "...", "已知内容 2": "..."} 这样的字典，
   并去掉每段开头注入的 source 路径前缀。

在 __init__.py 里导出 get_naive_rag_tool。
```

### 产出：核心代码

```python
from langchain.tools.retriever import create_retriever_tool
import os
from utils import get_embedding_model

def get_naive_rag_tool(vectorstore_name):
    from langchain_chroma import Chroma

    # 1. 连接持久化的 Chroma 向量库
    vectorstore = Chroma(
        collection_name=vectorstore_name,
        embedding_function=get_embedding_model(platform_type="OpenAI"),
        persist_directory=os.path.join(
            os.path.dirname(os.path.dirname(__file__)),
            "kb", vectorstore_name, "vectorstore"
        ),
    )

    # 2. 转成带相似度阈值的检索器
    retriever = vectorstore.as_retriever(
        search_type="similarity_score_threshold",
        search_kwargs={"k": 3, "score_threshold": 0.15},
    )

    # 3. 封装为 Agent 可调用的工具
    retriever_tool = create_retriever_tool(
        retriever,
        f"{vectorstore_name}_knowledge_base_tool",
        f"search and return information about {vectorstore_name}",
    )
    retriever_tool.response_format = "content"

    # 4. 自定义返回结构：编号 + 去掉 source 前缀
    retriever_tool.func = lambda query: {
        f"已知内容 {inum + 1}": doc.page_content.replace(doc.metadata["source"] + "\n\n", "")
        for inum, doc in enumerate(retriever.invoke(query))
    }
    return retriever_tool
```

`tools/__init__.py`：

```python
from tools.naive_rag_tool import get_naive_rag_tool
```

**要点：**

1. `score_threshold`\*\* 的作用\*\*——只返回相似度高于 0.15 的结果，过滤掉不相关内容，避免"幻觉素材"。
2. **工具名约定**——`<kb>_knowledge_base_tool` 这个后缀很关键，后面对话页面会用它来反推知识库名展示给用户。
3. `create_retriever_tool`\*\* 是 LangChain 的语法糖\*\*——它把一个检索器自动包装成符合 Agent `bind_tools` 规范的工具，省去手写 schema。

***

## Step 4：知识库管理页面

让用户能"喂数据"给系统：新建知识库 → 上传 Markdown → 切分 → 向量化入库。

### 本步目标

实现 `knowledge_base_page()`：包含"新建知识库"和"向已有知识库上传文件"两个分支。

### 提示词

**🔹**\*\* Prompt（知识库管理页面）\*\*

```plain
请创建 webui/knowledge_base_page.py，实现 knowledge_base_page() Streamlit 页面：

【知识库选择】
- 用 utils.get_kb_names() 获取已有知识库，下拉框选项为 ["新建知识库"] + 已有列表。

【新建知识库分支】
- 表单：知识库名称(英文)、向量库类型(Chroma)、知识库描述、
  Embedding 平台(PLATFORMS)、Embedding 模型(get_embedding_models 动态获取)。
- 点击"创建知识库"后，在 kb/<name>/ 下创建 files/ 和 vectorstore/ 子目录；
  已存在则报错；成功后写入 session_state 并 st.rerun() 刷新。

【上传文件分支（选中已有知识库时）】
- 文件上传控件，只允许 md 格式，支持多文件。
- 点击"上传"后：
  1. 把文件保存到 kb/<name>/files/。
  2. 用 DirectoryLoader + TextLoader(autodetect_encoding=True) 加载文档。
  3. 用 MarkdownTextSplitter(chunk_size=500, chunk_overlap=100) 切分。
  4. 给每个分块的 page_content 前面拼上它的 source 路径（用于溯源）。
  5. 清理 Chroma 系统缓存后，用 Chroma 向量库 add_documents 入库，
     embedding 用 get_embedding_model(platform_type="OpenAI")。
  6. 成功后 st.success 提示。

用 st.status 包裹配置/上传过程，体验更好。所有逻辑写中文注释。
```

### 产出：核心代码（文件入库逻辑）

```python
if upload:
    # 1. 保存上传的文件到 files/ 目录
    for file in files:
        with open(os.path.join(file_storage_path, file.name), "wb") as f:
            f.write(file.getvalue())

    # 2. 加载文档（自动检测编码，兼容中文）
    from langchain_community.document_loaders import DirectoryLoader, TextLoader
    loader = DirectoryLoader(
        file_storage_path,
        glob=[f"**/{file.name}" for file in files],
        show_progress=True,
        use_multithreading=True,
        loader_cls=TextLoader,
        loader_kwargs={"autodetect_encoding": True},
    )
    docs_list = loader.load()

    # 3. Markdown 感知切分
    text_splitter = MarkdownTextSplitter(chunk_size=500, chunk_overlap=100)
    doc_splits = text_splitter.split_documents(docs_list)

    # 4. 把 source 路径注入正文开头，便于检索结果溯源
    for doc in doc_splits:
        doc.page_content = doc.metadata["source"] + "\n\n" + doc.page_content

    # 5. 清缓存 + 入库
    import chromadb.api
    chromadb.api.client.SharedSystemClient.clear_system_cache()
    vectorstore = Chroma(
        collection_name=selected_kb,
        embedding_function=get_embedding_model(platform_type="OpenAI"),
        persist_directory=vs_path,
    )
    vectorstore.add_documents(doc_splits)
    st.success("上传文件成功")
```

**要点：**

1. \*\*为什么用 \*\*`MarkdownTextSplitter`——它能感知 Markdown 的标题层级，比纯字符切分更"语义完整"。`chunk_overlap=100` 保证上下文不被切断。
2. **source 前缀注入 + 检索时还原**——这是一个巧妙设计：入库时把来源拼进正文（让 Embedding 也"看到"来源），检索返回时再用 `replace` 去掉（参见 Step 3）。
3. `clear_system_cache()`\*\* 的坑\*\*——Chroma 在 Streamlit 多次 rerun 时容易出现客户端缓存冲突，清缓存可避免报错。**这是个典型的"踩坑后让 Claude Code 修"的点**，运行调试章节会讲。

***

## Step 5：RAG 对话页面与 LangGraph Agent

全系统最核心的一章：用 LangGraph 搭建"模型 ↔ 工具"的 Agent 循环，实现自动检索 + 流式回答。

### LangGraph Agent 工作原理

```plain
用户提问
      │
      ▼
  ┌────────┐  需要检索？(tools_condition)
  │ agent  │──────── yes ────────►┌───────┐
  │(调模型) │                      │ tools │ 调用知识库检索工具
  └────────┘◄─────────────────────└───────┘
      │ no（已能回答）
      ▼
   生成最终回答（流式）
```

* `agent` 节点：调用绑定了工具的大模型，模型自己决定"要不要检索、检索什么"。
* `tools` 节点：执行检索工具，把结果塞回消息历史。
* `tools_condition`：LangGraph 内置的条件判断——模型若发起 tool_call 就去 `tools`，否则结束。
* `tools → agent` 形成循环：检索完再回到模型，让它基于检索结果作答。

### 提示词

**🔹**\*\* Prompt（构建 LangGraph Agent）\*\*

```plain
请先阅读 utils.py 和 tools/naive_rag_tool.py，理解现有接口，
然后创建 webui/rag_chat_page.py。先实现 get_rag_graph(platform, model, temperature, selected_kbs, KBS)：

1. 根据 selected_kbs 从 KBS 字典取出对应的检索工具列表 tools，创建 ToolNode。
2. 定义 call_model(state)：用 utils.get_chatllm 取得模型，bind_tools(tools)，
   对 state["messages"] 调用并返回 {"messages": [响应]}。
3. 用 langgraph 的 StateGraph(MessagesState) 构建图：
   - 添加 "agent" 节点(call_model) 和 "tools" 节点(tool_node)。
   - add_conditional_edges("agent", tools_condition)。
   - add_edge("tools", "agent")。
   - set_entry_point("agent")。
4. 用 MemorySaver 作为 checkpointer 编译并返回 app。
```

**🔹**\*\* Prompt（流式响应 + 工具调用过程展示）\*\*

```plain
继续在 rag_chat_page.py 中实现 graph_response(graph, input)：
用 graph.invoke(..., stream_mode="messages") 流式遍历事件：
- 遇到 AIMessageChunk：若包含 tool_calls，往 session_state["rag_tool_calls"]
  记录一条"正在查询..."状态（知识库名 = 工具名去掉 _knowledge_base_tool 后缀）；
  然后 yield 这段内容。
- 遇到 ToolMessage：用 st.status 展示"已调用 X 知识库 + 检索结果"，
  并把结果存进 session_state。

再实现 rag_chat_page() 页面：
- 用 get_kb_names() + get_naive_rag_tool() 构建 KBS 字典。
- 侧边栏可多选启用的知识库；底部有模型配置弹窗(平台/模型/temperature/历史长度)、
  输入框、清空按钮。
- 用户提问后调用 get_rag_chat_response，用 st.write_stream 流式展示助手回答，
  并维护带工具调用记录的对话历史。
```

### 产出：Agent 图构建（核心）

```python
def get_rag_graph(platform, model, temperature, selected_kbs, KBS):
    tools = [KBS[k] for k in selected_kbs]
    tool_node = ToolNode(tools)

    def call_model(state):
        llm = get_chatllm(platform, model, temperature=temperature)
        llm_with_tools = llm.bind_tools(tools)        # 关键：把检索工具绑定给模型
        return {"messages": [llm_with_tools.invoke(state["messages"])]}

    workflow = StateGraph(MessagesState)
    workflow.add_node("agent", call_model)
    workflow.add_node("tools", tool_node)
    workflow.add_conditional_edges("agent", tools_condition)  # 模型决定是否检索
    workflow.add_edge("tools", "agent")                       # 检索完回到模型
    workflow.set_entry_point("agent")

    checkpointer = MemorySaver()                              # 记忆多轮对话
    return workflow.compile(checkpointer=checkpointer)
```

### 产出：流式响应处理（节选）

```python
def graph_response(graph, input):
    for event in graph.invoke(
            {"messages": input},
            config={"configurable": {"thread_id": 42}},
            stream_mode="messages",
    ):
        if type(event[0]) == AIMessageChunk:
            if len(event[0].tool_calls):
                st.session_state["rag_tool_calls"].append({
                    "status": "正在查询...",
                    "knowledge_base": event[0].tool_calls[0]["name"].replace("_knowledge_base_tool", ""),
                    "query": ""
                })
            yield event[0].content                    # 流式吐字
        elif type(event[0]) == ToolMessage:
            with st.status("正在查询...", expanded=True) as s:
                st.write("已调用 `", event[0].name.replace("_knowledge_base_tool", ""), "` 知识库进行查询")
                st.write("知识库检索结果：")
                st.code(event[0].content, wrap_lines=True)
                s.update(label="已完成知识库检索！", expanded=False)
```

**要点：**

1. `bind_tools`\*\* 是工具调用的开关\*\*——只有绑定后，模型才"知道"自己有哪些工具可用，并能输出结构化的 `tool_calls`。
2. `stream_mode="messages"`——这是实现"打字机效果"的关键，逐 token 返回。
3. `thread_id`\*\* + \*\*`MemorySaver`——配合实现多轮记忆，相同 `thread_id` 的对话共享上下文。
4. **过程透明化**——把工具调用过程用 `st.status` 展示出来，是企业级客服系统建立用户信任的重要设计。

***

## Step 6：主入口与多页面导航

### 提示词

**🔹**\*\* Prompt（主入口）\*\*

```plain
请创建 rag.py 作为 Streamlit 主入口：
- 侧边栏用 st.logo 显示 Logo（用 utils.get_img_base64 读取 img/ 下的图片）。
- 用 st.navigation 组织两个分组：
  "对话" 分组 → rag_chat_page（标题"智能客服"，chat 图标）；
  "设置" 分组 → knowledge_base_page（标题"行业知识库"，library_books 图标）。
- 调用 pg.run() 启动。
```

### 产出

```python
import streamlit as st
from webui import rag_chat_page, knowledge_base_page
from utils import get_img_base64

if __name__ == "__main__":
    with st.sidebar:
        st.logo(
            get_img_base64("chatchat_lite_logo.png"),
            size="large",
            icon_image=get_img_base64("chatchat_lite_small_logo.png"),
        )

    pg = st.navigation({
        "对话": [
            st.Page(rag_chat_page, title="智能客服", icon=":material/chat:"),
        ],
        "设置": [
            st.Page(knowledge_base_page, title="行业知识库", icon=":material/library_books:"),
        ]
    })
    pg.run()
```

`webui/__init__.py`：

```python
from webui.rag_chat_page import rag_chat_page
from webui.knowledge_base_page import knowledge_base_page
```

**要点：**`st.navigation` + `st.Page` 是 Streamlit 1.36+ 的多页面 API，比传统 `pages/` 目录更灵活，可以用代码动态组织页面分组。

***

## Step 7：运行、调试与排错（让 Claude Code 修 Bug）

这一章是 Claude Code 真正的价值所在——**它不仅能写代码，更能帮你修代码**：它可以自己跑命令、读报错、定位到具体文件行号并直接修复。

### 启动项目

```plain
# 先配置好 OpenAI 环境变量
streamlit run rag.py
```

浏览器自动打开后：

1. 进入"行业知识库" → 新建知识库 `bank` → 上传 `bank.md` → 等待向量化完成；
2. 回到"智能客服" → 勾选 `bank` 知识库 → 输入"如何查询账户余额？"。

### 常见报错与"修 Bug 提示词"

**要点：** 真实开发中报错是常态。下面演示如何把报错原文丢给 Claude Code 让它定位修复。

**🔹**\*\* Prompt（修复 Chroma 缓存报错）\*\*

```plain
我在上传文件第二次入库时报错：
"An instance of Chroma already exists for ... with different settings"。
请定位 webui/knowledge_base_page.py 中的问题并修复，
要求在创建 Chroma 实例前清理系统缓存。
```

Claude Code 会在 `add_documents` 前补上：

```python
import chromadb.api
chromadb.api.client.SharedSystemClient.clear_system_cache()
```

**🔹**\*\* Prompt（检索为空 / 阈值问题）\*\*

```plain
对话时模型总是说"没有查到相关内容"。我怀疑是检索阈值太高。
请检查 tools/naive_rag_tool.py 的 search_kwargs，
把 score_threshold 调低到 0.15、k 调成 3，并解释这两个参数的含义。
```

**🔹**\*\* Prompt（让 Claude Code 自己跑起来排查）\*\*

```plain
请帮我运行 `streamlit run rag.py` 之前，先用 `python -c "import utils"` 和
`python -c "import webui"` 检查所有模块能否正常导入，
如果有 ImportError 或版本不兼容，请定位并修复。
```

### 调试技巧：让 Claude Code 解释代码

**🔹**\*\* Prompt（理解既有代码）\*\*

```plain
请逐行解释 webui/rag_chat_page.py 中 graph_response 函数的执行流程，
特别是它如何区分 AIMessageChunk 和 ToolMessage，
以及 session_state["rag_tool_calls"] 是怎么积累工具调用记录的。
```

**要点：** Claude Code 是很好的"代码讲解员"。接手别人的项目、或忘了自己几天前写的逻辑时，让它解释一遍效率极高。

***

## Claude Code Harness 三阶段落地（工程化进阶）

## Claude Code 体系实战复盘总结

把这一章作为课程的"方法论升华"，让学员带走可复用的经验。

### 黄金法则：分步交付，单步验证

❌ 反面教材：

帮我写一个完整的 RAG 智能客服系统。

→ 产出庞大、难以验证、出错难定位。

✅ 正确姿势：把大需求拆成 7 个 Step，**每步只交付一个模块，验证通过再继续**（正是本课程的结构）。

### 好提示词的四要素

| **要素** | **说明** | **示例** |
| :--- | :--- | :--- |
| **目标明确** | 说清要"做什么文件、什么函数" | "创建 utils.py，实现 get_chatllm 函数" |
| **约束清晰** | 指定库、版本、参数、默认值 | "用 langchain_openai.ChatOpenAI，streaming=True" |
| **输入输出** | 描述函数签名和返回结构 | "返回 {'已知内容 1': '...'} 字典" |
| **附加要求** | 注释、风格、错误处理 | "写中文注释；连接失败用 st.toast 提示不要抛异常" |

### 善用 Claude Code 的"智能体"能力

* **让它读项目**："先阅读 utils.py 和 tools/，理解现有接口后再写对话页面。"
* **让它跑命令**："安装依赖后运行 `python utils.py` 验证模型列表能正常返回。"
* **让它修 Bug**：把**完整报错堆栈**贴给它，比只说"报错了"有效得多。
* **让它做重构**："把 utils.py 里重复的 base_url 默认值逻辑抽成一个辅助函数。"
* **让它先做计划**：复杂改动前切到 Plan Mode，先评审方案再放行实现。

### 上下文管理

* 用 `/init` 生成并持续维护 `CLAUDE.md`，沉淀项目规范（技术栈、目录约定、代码风格、常用命令），Claude Code 每次会话都会自动加载它。
* 会话中用 `#` 开头的消息可以把新约定随手写入 `CLAUDE.md`；上下文太长时用 `/compact` 压缩会话，避免"上下文漂移"。
* 项目进入长期维护后，按上一章"Harness 三阶段落地"逐步补齐信息层（CLAUDE.md + docs/）、约束层（Ruff / import-linter / CI）和自动化层（Hooks / 斜杠命令 / 子代理）。

### 安全与审查

* **代码审查不可省**：AI 生成的代码必须人工 review，尤其是涉及文件写入、密钥、删除操作的部分。
* 课堂演示用**默认模式**，让每一处文件改动和命令执行都可见可控；`--dangerously-skip-permissions` 只在隔离环境中使用。

***

**结语**：本课程的核心不是"让 AI 替你写代码"，而是教会你**像架构师一样思考、像工程师一样验证、像产品经理一样拆解需求**，再用 Claude Code 把这套工程化方法落地。掌握"分步交付 + 单步验证 + 精准提示"，你就能用 Claude Code 高效开发任何复杂应用。


> 更新: 2026-07-22 20:17:29  
> 原文: <https://www.yuque.com/aaron-wecc3/dhluml/fhowrdl9sccuglho>