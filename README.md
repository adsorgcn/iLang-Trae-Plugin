# iLang 提智插件

**一句话：装上这个，AI就变聪明了。你说中文，它帮你做网站赚钱。**

## 这东西干什么用的

你知道ChatGPT、DeepSeek这些AI吗？它们很聪明，但有时候回答废话多、不敢给建议、说了半天没结论。

这个插件就是给AI装一套"工作规范"。装上之后AI会：

- 你问它哪个好，它直接告诉你哪个好，不说"取决于你的需求"
- 数据对比自动画表格，一目了然
- 教你东西的时候一步一步来，不会一次倒一堆把你搞晕
- 你说"帮我做个网站"，它真的从零开始帮你做出来
- 你不知道做什么方向，它帮你看赚钱的赛道，搜出标杆网站给你参考

你不需要懂任何技术。装上就生效。

## 我需要准备什么

一台电脑（Windows 或 Mac），能上网就行。

## 第一步：装 Trae

Trae 是一个免费的AI编程工具，字节跳动（抖音的公司）做的。你不需要懂编程，你说中文，它替你写代码。

**Windows用户：**

1. 打开浏览器（Edge、Chrome都行）
2. 在地址栏输入 **trae.cn** 按回车
3. 点页面上的"下载"按钮
4. 下载完双击安装，一路点"下一步"就行
5. 如果弹出"Windows已保护你的电脑"蓝色弹窗，点左边小字"更多信息"，再点"仍要运行"。这不是病毒，是因为软件比较新

**Mac用户：**

1. 打开浏览器，输入 **trae.cn**
2. 点"下载"
3. 下载完打开，把Trae图标拖到"应用程序"文件夹
4. 第一次打开如果提示"无法打开"：点左上角苹果图标 → 系统设置 → 隐私与安全性 → 点"仍要打开"

打开Trae，看到欢迎界面 = 成功了。

## 第二步：装提智插件

### Windows用户（推荐方式：直接下载）

1. 打开浏览器，在地址栏输入下面这个地址，按回车：

```
https://gitee.com/palmmedia/iLang-Trae-Plugin/repository/archive/main.zip
```

2. 浏览器会自动下载一个压缩包（ZIP文件）
3. 找到下载的文件（通常在"下载"文件夹里），右键 → "全部解压缩"
4. 解压后会得到一个文件夹，名字类似 **iLang-Trae-Plugin-main**
5. 打开 Trae，点左上角"文件" → "打开文件夹"，选中刚才解压的那个文件夹，点"选择"

### Mac用户

1. 打开 Trae
2. 按 **Cmd+J**，屏幕下方会弹出一个黑色的框（终端）
3. 复制下面这行，粘贴进去，按回车：

```
git clone https://gitee.com/palmmedia/iLang-Trae-Plugin.git
```

4. 如果弹出"需要安装命令行开发者工具"，点"安装"，装完再试一次
5. 等几秒下载完后，点"文件" → "打开文件夹"，找到 **iLang-Trae-Plugin** 文件夹打开

### 海外用户

把上面地址里的 `gitee.com/palmmedia` 换成 `github.com/adsorgcn`。

Windows直接下载地址：

```
https://github.com/adsorgcn/iLang-Trae-Plugin/archive/refs/heads/main.zip
```

## 第三步：开始用

打开文件夹后，在 Trae 的对话框里直接说中文就行：

- "帮我做一个卖咖啡的网站"
- "我不知道做什么方向，帮我看看什么赚钱"
- "这个网站怎么让Google搜到"
- "帮我接广告赚钱"

AI 会按照提智规则回答你，比普通AI聪明很多。

## 装了之后AI多了什么能力

| 能力 | 说明 |
|------|------|
| 帮你选赚钱方向 | 不知道做什么？它列出几十个赚钱赛道给你选，搜出标杆网站给你看真实数据 |
| 帮你做网站 | 你说想做什么站，它从零搭出来，手机电脑都能看 |
| 帮你做SEO | 让Google能搜到你的网站，自动配置好各种搜索引擎需要的东西 |
| 帮你做7种语言 | 一个中文网站自动变成8种语言，搜索量翻8倍 |
| 帮你接广告赚钱 | Google AdSense广告怎么申请、怎么放、怎么提高收入 |
| 帮你推产品赚佣金 | 联盟营销怎么选品、怎么放链接、怎么赚佣金 |
| 帮你上线 | 网站做好后一行命令发布到网上，全世界都能访问 |
| 帮你配AI员工 | 做一个24小时在线的AI助手，手机随时管 |

## 不想用了怎么办

在 Trae 的终端（Ctrl+J打开）里输入：

```
rm -rf .trae
```

按回车，插件就删掉了，AI恢复默认。

## 看图文教程

不想看文字？这里有图文版，每一步都有截图：

[ilang.cn/tpinstall.html](https://ilang.cn/tpinstall.html)

## 安全说明

这个插件本身只是一堆文字规则，不是程序，不会在你电脑上运行任何东西。

但AI在帮你做网站的过程中，可能会建议你执行一些命令（比如上传文件到服务器）。遇到这种情况，AI会先告诉你这个命令要做什么，你确认了再执行。不确定的时候就问AI"这个命令具体会改什么，能撤销吗"。

## 技术信息

<details>
<summary>展开看技术细节（普通用户不需要看）</summary>

### I-Lang v4.0 兼容等级

本仓库是 I-Lang v4.0 L1 advisory skill pack。提供规则和技能文本，不提供 L2 runtime enforcement 或 L3 external grader。

### 结构

```
.trae/
  rules/project-rules.md       ← 核心行为规则
  skills/                       ← 15个领域技能
    niche-select/  deepseek/  think/  build/  seo/
    multilang/  content/  style-polish/  affiliate/
    adsense/  research/  deploy/  openclaw/  techstack/  teaching/
CLAUDE.md                       ← Claude Code 入口
```

### Claude Code 用户

```
git clone https://github.com/adsorgcn/iLang-Trae-Plugin.git
cd iLang-Trae-Plugin
claude
```

### 安装到已有项目

```
git clone --depth 1 https://gitee.com/palmmedia/iLang-Trae-Plugin.git .ilang-tmp
cp -R .ilang-tmp/.trae ./
rm -rf .ilang-tmp
```

### 更新日志

见 [CHANGELOG.md](CHANGELOG.md)

</details>

## 相关项目

- [I-Lang 协议](https://ilang.cn)
- [Trae 下载](https://trae.cn)
- [DeepSeek 终端客户端](https://gitee.com/palmmedia/DeepSeek-TUI-Enhanced)

## 协议

MIT · 免费 · 永久

## 关于

[掌媒科技](https://zhangmei.com) · [I-Lang Research](https://ilang.cn) · Eastsoft Inc.
