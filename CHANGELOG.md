# 更新日志

## v2.0.1 (2026-05-11)

审计修复补丁，6个改动：

- PRIOR声明修正：authority:system → authority:developer，补齐dimension/default/scope canonical写法，新增clarification和output两条PRIOR
- 新增conformance:L1-advisory声明（project-rules.md和README）
- deai重命名为style-polish：描述从"AI fingerprint removal / zero residual"改为"提升自然表达，减少模板腔"
- 安装说明补两种方式：方式A独立项目，方式B复制到已有项目
- 新增执行边界规则：低风险直接推进，高风险（部署/删除/API Key/服务器）先确认
- DEFAULT:build改为默认进入build规划模式（解释方案/给建议），不直接执行建站/部署/改文件
- 安全说明补充：技能可能指导AI生成命令，执行前用户应确认影响和回滚方式


## v2.0.0 (2026-05-11)

架构级重构：单文件→模块化技能。

- 核心行为和领域技能分离：project-rules.md只管"怎么说话"（50行），14个SKILL.md管"怎么做事"
- 新增CLAUDE.md：同时支持Trae和Claude Code，一个仓库两个入口
- 新增DeepSeek配置技能：模型选择（4 Pro vs Chat）、API Key管理、TUI安装、省钱策略
- 新增Google AdSense完整技能：申请、广告位、RPM优化、封号防护、多站运营、收益诊断（基于400+实战案例提炼）
- 联盟营销独立技能：从变现里拆出，覆盖选品、Cookie周期、转化率
- 三步法→四步法：新增验证步骤
- SEO基础+实战合并为一个完整SEO技能
- 教学模式+提智去障合并
- 质量检查/压缩/进度汇报/意图识别并入核心行为
- ads.txt并入AdSense技能
- I-Lang v4.0：PRIOR声明、四步法验证
- OpenClaw对接：电报→飞书

## v1.1 (2026-05-11)

- I-Lang v3.0→v4.0
- 三步法→四步法
- PRIOR声明
- 飞书替代电报
- 安全说明、卸载方法

## v1.0 (2026-05-10)

- 初始发布，20个技能，单文件结构
