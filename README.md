# iLang 提智插件

跨境电商 AI 编程课专用技能集，安装即生效，说中文出产品。

## 这是什么

一套 AI 行为定义和技能集，兼容 Trae 和 Claude Code。装上之后 AI 会变得更聪明：

- 回答结论先行，不废话，敢判断
- 数据对比自动用表格
- 教你的时候一步一步来，不会一次倒一堆
- 建站、SEO、多语言、AdSense、联盟营销、部署上线，全链路覆盖
- 基于 I-Lang v4.0 协议，内置四步法（观察、推理、输出、验证）

不需要学 I-Lang 协议。装上就生效，AI 自动按照规则工作。效果因模型能力而异。

## I-Lang v4.0 兼容等级

本仓库是 I-Lang v4.0 L1 advisory skill pack。

它提供规则和技能文本，帮助 AI 按 v4 风格工作：
- PRIOR 默认倾向（完成前自检、安全时推进、不确定时澄清）
- 四步法：观察、推理、输出、验证
- 证据优先，不用努力程度冒充完成

它不提供：
- L2 runtime enforcement（运行时强隔离）
- L3 external grader（外部评分器）

## 安装

**看图文教程（推荐）：** [ilang.cn/tpinstall.html](https://ilang.cn/tpinstall.html)

### 方式 A：作为独立项目使用（推荐新手）

1. 打开 Trae（还没装？去 trae.cn 下载，免费）
2. 按 Ctrl+J（Mac按Cmd+J）打开终端
3. 复制粘贴以下命令，按回车：

**国内用户：**

```
git clone https://gitee.com/palmmedia/iLang-Trae-Plugin.git
```

**海外用户：**

```
git clone https://github.com/adsorgcn/iLang-Trae-Plugin.git
```

4. 在 Trae 中打开克隆下来的 `iLang-Trae-Plugin` 文件夹
5. 开始说中文，AI 会按照提智规则回答

### 方式 B：安装到已有项目

```
git clone --depth 1 https://gitee.com/palmmedia/iLang-Trae-Plugin.git .ilang-tmp
cp -R .ilang-tmp/.trae ./
rm -rf .ilang-tmp
```

海外用户把 gitee.com/palmmedia 换成 github.com/adsorgcn。

### Claude Code 用户

```
git clone https://github.com/adsorgcn/iLang-Trae-Plugin.git
cd iLang-Trae-Plugin
claude
```

Claude Code 会自动读取 CLAUDE.md 并加载所有技能。

**如果报错 "git: command not found"：**
在终端里先跑 `sudo apt install git -y`（Ubuntu）或去 git-scm.com 下载安装。

## 卸载 / 恢复默认

删掉 `.trae` 文件夹即可恢复默认行为：

```
rm -rf .trae
```

## 结构

```
.trae/
  rules/
    project-rules.md          ← 核心行为（结论先行/不废话/四步法/执行边界）
  skills/
    niche-select/SKILL.md     ← 赛道选择、标杆站分析、数据验证
    deepseek/SKILL.md         ← DeepSeek配置、模型选择、省钱
    think/SKILL.md            ← 四步法思维升级
    build/SKILL.md            ← 从零建站
    seo/SKILL.md              ← SEO全链路
    multilang/SKILL.md        ← 7种语言扩展
    content/SKILL.md          ← AI内容生成
    style-polish/SKILL.md     ← 提升自然表达，减少模板腔
    affiliate/SKILL.md        ← 联盟营销变现
    adsense/SKILL.md          ← Google AdSense运营
    research/SKILL.md         ← 信息搜集、竞品分析
    deploy/SKILL.md           ← 一键部署
    openclaw/SKILL.md         ← AI员工对接
    techstack/SKILL.md        ← 技术选型
    teaching/SKILL.md         ← 教学模式
CLAUDE.md                     ← Claude Code 入口
```

## 适合谁

- AI 编程课学员
- 跨境电商从业者
- 想用 AI 做网站赚钱的人
- 不懂编程但想让 AI 帮你写代码的人

## 不适合谁

- 专业程序员（用 AutoCode 更合适：github.com/ilang-ai/autocode）
- 英文环境用户（用 AutoCode）

## 安全说明

本仓库本身不包含可执行代码，仅包含 AI 行为规则和技能文本。
但技能可能指导 AI 生成 shell 命令、安装命令、部署命令或配置命令。

执行任何命令前，请确认：
1. 命令要改什么
2. 是否涉及服务器、DNS、账号、支付、API Key
3. 是否可回滚
4. 是否真的需要现在执行

## 更新日志

见 [CHANGELOG.md](CHANGELOG.md)

## 相关项目

- [I-Lang 协议中文站](https://ilang.cn)
- [I-Lang v4.0 规范](https://github.com/ilang-ai/ilang-spec/blob/main/SPEC-v4.0-FINAL.md)
- [Trae AI 编程工具](https://trae.cn)
- [DeepSeek-TUI 终端客户端](https://gitee.com/palmmedia/DeepSeek-TUI-Enhanced)
- [AutoCode 英文技能集](https://github.com/ilang-ai/autocode)

## 协议

MIT · 免费 · 永久

## 关于

[掌媒科技](https://zhangmei.com) · [I-Lang Research](https://ilang.cn) · Eastsoft Inc.
