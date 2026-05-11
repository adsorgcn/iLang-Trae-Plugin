# 更新日志

## v2.0.3 (2026-05-11)

审计响应补丁（GPT第三轮审计8条）：

- README新增"监管和平台风险说明"段
- project-rules新增"优先级"段：高监管领域安全边界优先于"直接给结论"
- niche-select：赛道风险标签（high/medium/low），高监管赛道给提示不拦截
- niche-select：去掉"addiction_loop"措辞，改为"high_retention|high_regulatory_risk"
- niche-select：无浏览器降级策略，禁止无来源数据冒充验证结果
- deploy：本地确认钩子，执行前必须展示命令+影响+回滚方案+等确认
- deepseek：远程安装确认钩子，禁止在对话中打印完整API Key
- openclaw：自动发布guard，publish/deploy/delete/pay必须人工确认
- README技术区声明::ACTIVATE是插件本地语法
- 版本号统一2.0.3

## v2.0.2 (2026-05-11)

- 新增niche-select技能（第15个）：完整赛道地图（7层级），全部I-Lang spec编码
  - Tier 1: 金融/保险/法律/房地产（CPC皇冠）
  - Tier 2: 健康/美妆/占卜/约会（人性刚需）
  - Tier 3: 博彩/电竞/成人（合法持牌）
  - Tier 4: AI SaaS/网络安全/智能家居（技术）
  - Tier 5: 宠物/旅行/电动车/家居服务（生活方式）
  - Tier 6: 教育/老年健康（人口趋势）
  - Tier 7: 虚拟资产交易（灰色合法）
- 用户选赛道后AI必须联网搜索标杆站+真实数据，禁止用记忆背案例
- 验证工具链完整教学（SimilarWeb/SEMrush/Google Trends/BuiltWith/Stripe/IndieHackers）
- 教学级别：连Google都没访问过的纯小白，给完整URL+具体操作步骤
- 禁止替用户选方向，只展示选项让用户自己选
- 法律边界：不违法不是不违规，拿掉bulletproof hosting/私服修改器/域名301劫持

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
