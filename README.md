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

## 安装

**看图文教程（推荐）：** [ilang.cn/tpinstall.html](https://ilang.cn/tpinstall.html)

**文字版：**

1. 打开 Trae（还没装？去 trae.cn 下载，免费）
2. 按 Ctrl+J（Mac按Cmd+J）打开终端
3. 复制下面这行，粘贴到终端里，按回车：

**国内用户（推荐）：**

```
git clone https://gitee.com/palmmedia/iLang-Trae-Plugin.git
```

**海外用户：**

```
git clone https://github.com/adsorgcn/iLang-Trae-Plugin.git
```

4. 等几秒钟下载完，Trae 会自动读取规则和技能
5. 开始说中文，AI 会按照提智规则回答

**Claude Code 用户：**

```
git clone https://github.com/adsorgcn/iLang-Trae-Plugin.git
cd iLang-Trae-Plugin
claude
```

Claude Code 会自动读取 CLAUDE.md 并加载所有技能。

## 卸载 / 恢复默认

删掉 `.trae` 文件夹即可恢复默认行为：

```
rm -rf .trae
```

## 结构

```
.trae/
  rules/
    project-rules.md          ← 核心行为（结论先行/不废话/四步法）
  skills/
    deepseek/SKILL.md         ← DeepSeek配置、模型选择、省钱
    think/SKILL.md            ← 四步法思维升级
    build/SKILL.md            ← 从零建站
    seo/SKILL.md              ← SEO全链路
    multilang/SKILL.md        ← 7种语言扩展
    content/SKILL.md          ← AI内容生成
    deai/SKILL.md             ← 去AI指纹
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

- 本插件不包含可执行代码，仅为 AI 行为定义文件
- 安装方式为标准 Git 克隆，无需下载二进制或执行脚本
- 所有外部链接仅作文档引用，不影响插件功能

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
