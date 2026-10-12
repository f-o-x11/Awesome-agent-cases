# AI 日报：Agent 安全危机与编码 Agent 军备竞赛白热化

日期：2026-06-07

**今日结论：** 本周 AI 行业的核心矛盾集中在 **Agent 安全**与 **编码 Agent 能力**两大主题。微软披露的 Claude Code 凭证泄露漏洞和针对 AI 编码 Agent 的供应链攻击（Miasma 蠕虫）引发行业震动，安全厂商与 OWASP 迅速推出应对框架。与此同时，编码 Agent 领域竞争白热化：月之暗面开源 Kimi Code CLI，阿里发布多模态 Agent 模型 Qwen3.7-Plus，Anthropic 被曝雇佣千名工程师培训 Claude Code。华为云则另辟蹊径，提出“Agentic Infra”新范式，押注国产算力。开源社区方面，字节跳动的 DeerFlow 与 Warp 终端开源项目均获得极高关注。

## 新闻与产业动态

1. **微软披露 Claude Code 凭证泄露漏洞，Miasma 蠕虫攻击 73 个 GitHub 仓库**
   - **来源网站：** Microsoft, The Hacker News, Decrypt
   - **原链接：** [Securing CI/CD in an agentic world: Claude Code Github action case](https://news.google.com/rss/articles/CBMivAFBVV95cUxNREJ4Wm45a0lId2d5MUxEOHdRWldESTBfVUZWNFdzMWozbGpLVFVNaEVIV0JlZUFBU0ZjMmFCeWNMazVuM1BsNUx2Z3VlajhHQURuR3cyNDd0LTY5YVJsVGpOU0E1RmtsZmVyb1JyOEgyQmNCeFJZT3U5bTBPSlZuNmdtdm10bzNwSmhyMmNLNkRrUU5EYVRxVG1McjVJSmNqZTBTb0dmRk15UlJtOWFubl9TTFRMUnJmQm5MTg?oc=5) | [Miasma Worm Hits 73 Microsoft GitHub Repositories](https://news.google.com/rss/articles/CBMigAFBVV95cUxNbFdZOWxXR0YwLTVNR2ZUbkdXTzF0M0FzQnR4QWtCX0hhVFNVTTRmNlNmS3FLdThWRWJWZjlsbWdpWmdaSWVGZEtRemVYSHllZUZSWTV0NjVUN0c0eWNZUktRbC1MYUNJbS1mTDlEWjVONTVnNlVBUExETXlNTWJlbA?oc=5) | [Claude Code Vulnerability Could Let Attackers Steal Credentials From GitHub](https://news.google.com/rss/articles/CBMinAFBVV95cUxOTjdvUnZKWEtSZUlURlNPakxCYW9qRDl1a09fcWdBRXczdWtsZVFFR09oLUtWOTRWTDQzdUoyZjZxdGYzajAtck5rQ3BRcDhwT2w3SUVSc2VWWjNBdDI1U2tpUEhoZFlfOUlWWGwwdkxGVXBwWHlQXzcwNjNEWGdIOHlmZ1V5UWtLQXFkdk5qVDhsRExaNExhS1pQUUnSAaQBQVVfeXFMTVhmbmlNdzNVSVg0cHdzVk5McnpxUWNaTncwUVlfZDVNVEhCcXRmU0tYakwzUi1YalJmZXpQX0dXb1R3Y0I2Tm1hZXE4SWEzR3o0b25lRWdkLUJrWVBzdTRzZDJ6MWczbUJJY21yZERiX056RFlEUm4wWUM4M1NOdEpIajA0Wm1FME0xR3Z6dzZfLWxJZDh1RC11LWp6NzZyMTRMOEc?oc=5)
   - **摘要：** 微软安全团队披露，Anthropic 的 Claude Code 在 GitHub Actions 中存在凭证泄露漏洞，攻击者可利用该漏洞窃取 GitHub 凭据。与此同时，名为“Miasma”的蠕虫病毒发动供应链攻击，导致微软 73 个 GitHub 仓库（包括 Azure Functions Action）被禁用。报道称，该攻击专门针对 AI 编码 Agent。
   - **为什么重要：** 这是首次由顶级云厂商公开披露主流 AI 编码 Agent 的严重安全漏洞，标志着 Agent 安全从理论风险进入实际攻击阶段。微软的官方报告为整个行业敲响警钟。
   - **值得继续跟踪：** Anthropic 的修复进展、其他编码 Agent（如 Codex、Gemini CLI）是否存在类似漏洞、以及 CI/CD 安全最佳实践的更新。

2. **Agentic AI 红队测试发现零点击“人在回路”绕过攻击链**
   - **来源网站：** CyberSecurityNews
   - **原链接：** [Agentic AI Red Teaming Reveals Zero-Click Human-in-the-Loop Bypass Attack Chains](https://news.google.com/rss/articles/CBMiggFBVV95cUxQMWlSVzBLU29MWG1HQkJhNFgzZ3luVkFNOHc2bjI4QnN0UjdPQXotV2JSdGtZekg5a0VUcVQxTmpDVmcxS1p5MkpXUm9mdlZNSHlhb2F1TTRiUC1rUVFJb0dDM0VCQ25SQ3ZVNTg1bVJNVlRDTkdwd1YwdklrZTdueDd30gGCAUFVX3lxTFAxaVJXMEtTb0xYbUdCQmE0WDNneW5WQU04dzZuMjhCc3RSN09Bei1XYlJ0a1l6SDlrRVRxVDFOakNWZzFLWnkySldSb2Z2Vk1IeWFvYXVNNGJQLWtRUUlvR0MzRUJDblJDdlU1ODVtUk1WVENOR3B3VjB2SWtlN254N3c?oc=5)
   - **摘要：** 安全研究人员发现了一种针对 Agentic AI 系统的零点击攻击链，能够绕过“人在回路”（Human-in-the-Loop）安全机制。攻击者无需用户交互即可操纵 AI Agent 执行恶意操作。
   - **为什么重要：** “人在回路”被视为 Agent 安全的核心防线，该攻击链的发现意味着现有安全设计存在根本性缺陷，可能影响所有依赖用户确认的 Agent 应用。
   - **值得继续跟踪：** 具体攻击技术细节的披露、各 Agent 平台的修复方案、以及 OWASP 等组织是否会更新安全指南。

3. **月之暗面发布 Kimi Code CLI：开源终端 AI 编码 Agent**
   - **来源网站：** MarkTechPost
   - **原链接：** [Moonshot AI Releases Kimi Code CLI: A Terminal AI Coding Agent Built in TypeScript for Next-Gen Agents](https://www.marktechpost.com/2026/06/06/moonshot-ai-releases-kimi-code-cli-a-terminal-ai-coding-agent-built-in-typescript-for-next-gen-agents/)
   - **摘要：** 月之暗面（Moonshot AI）开源了 Kimi Code CLI，一个基于 TypeScript 构建的终端 AI 编码 Agent。该工具支持子 Agent 和 MCP 配置，旨在为下一代 Agent 提供编码能力。
   - **为什么重要：** 这是中国 AI 公司首次推出对标 Claude Code 和 Codex 的开源终端编码 Agent，标志着编码 Agent 领域的竞争从美国扩展到中国。开源策略有助于快速建立开发者生态。
   - **值得继续跟踪：** Kimi Code CLI 的实际编码能力评测、与 Claude Code 的对比、以及社区贡献情况。

4. **阿里发布 Qwen3.7-Plus：将多模态 AI 转变为全自主 Agent**
   - **来源网站：** The Decoder
   - **原链接：** [Qwen3.7-Plus is Alibaba's bid to turn multimodal AI into a full-blown autonomous agent](https://the-decoder.com/qwen3.7-plus-is-alibabas-bid-to-turn-multimodal-ai-into-a-full-blown-autonomous-agent/)
   - **摘要：** 阿里 Qwen 团队发布 Qwen3.7-Plus，一个多模态 Agent 模型，将视觉感知、GUI 操作和编码整合到单一 Agent 循环中。演示中，基于该模型的 Agent 自主开发了一款词汇学习应用，在 11 小时内生成了超过 10,000 行代码，进行了 1,000 次 Agent 调用。
   - **为什么重要：** 该模型展示了从“看屏幕”到“操作屏幕”再到“写代码”的端到端自主能力，是 Agent 从辅助工具向自主生产力工具演进的重要里程碑。
   - **值得继续跟踪：** 该模型的商业化定价、实际应用场景（如自动化测试、UI 开发）、以及与其他多模态 Agent 的对比。

5. **Anthropic 被曝雇佣 1000 名人类工程师“培训”Claude Code，时薪 280 美元**
   - **来源网站：** 53AI
   - **原链接：** [Anthropic 被曝雇1000名人类工程师“培训”Claude Code，时薪280美元](https://news.google.com/rss/articles/CBMicEFVX3lxTE9xUEJMUnRXYTBJYnhETTJxYUkwM1VGYzFGUXdxNDhJdmt2WjlGQTNIOUFCRk10QnEzam55MDY3RzRSdlNyXzluX2xfSU9kWFdNN3Z4QVFCMnBqMVd5X1pGeGRiR25saHVmU3lNTk9DV3c?oc=5)
   - **摘要：** 报道称，Anthropic 雇佣了约 1000 名人类软件工程师，以时薪 280 美元的高薪来“培训”Claude Code。这些工程师通过编写代码、审查 AI 输出、提供反馈等方式，帮助改进 Claude Code 的编码能力。
   - **为什么重要：** 这一消息揭示了当前 AI 编码 Agent 发展的一个悖论：越追求自动化，越需要大量人类专家进行高质量数据标注和反馈。这既说明了高质量训练数据的稀缺性，也暗示了 AI 编码 Agent 短期内难以完全替代人类工程师。
   - **值得继续跟踪：** 这种“人类在环”培训模式的效果、成本效益分析、以及是否会被其他公司效仿。

6. **华为云发布 Agentic Infra 新范式，不拼 Token 单价赌国产算力**
   - **来源网站：** 36氪
   - **原链接：** [Token大战中，华为云选择了第三条路｜最前线](https://36kr.com/p/3840016255126016?f=rss)
   - **摘要：** 在 2026 华为云 INSPIRE 创想者大会上，华为云 CEO 周跃峰提出“Agentic Infra”新范式，强调不追求 Token 总量和单价，而是关注国产算力系统生产出的 Token 的“健康度”和生产力提升。华为云选择不参与价格战，转而押注国产算力生态。
   - **为什么重要：** 在云厂商普遍陷入 Token 价格战的背景下，华为云的战略转向具有风向标意义。它反映了中国 AI 产业从“拼价格”向“拼生态、拼算力自主”的转变，尤其对国产芯片和基础设施厂商是重大利好。
   - **值得继续跟踪：** Agentic Infra 的具体技术架构、合作伙伴生态建设、以及国产算力在 Agent 场景下的实际性能表现。

7. **微信 AI 对手机厂商打开一道窄门：采用 A2A 机制**
   - **来源网站：** 36氪
   - **原链接：** [微信AI对手机厂商打开一道窄门｜焦点分析](https://36kr.com/p/3839575253993985?f=rss)
   - **摘要：** 腾讯客服确认，微信正在与华为、小米、荣耀、OPPO、vivo 等手机厂商合作推出 A2A（Agent-to-Agent）助手能力。与字节跳动豆包采用的 GUI Agent 路线不同，微信采用 A2A 机制，让手机系统智能体通过加密协议直接与微信内部 Agent 对话，实现“双授权”安全机制。
   - **为什么重要：** 这是国内首次大规模实现应用级 Agent 与系统级 Agent 的协作，为超级 App 的 Agent 化提供了新范式。A2A 机制相比 GUI Agent 更安全、更高效，可能成为行业标准。
   - **值得继续跟踪：** 具体接入进度、用户体验反馈、以及字节跳动等竞争对手的应对策略。

8. **SpaceX 与谷歌签署 9.2 亿美元/月 AI 芯片租赁协议**
   - **来源网站：** The Decoder
   - **原链接：** [SpaceX signs $920 million per month deal with Google for 110,000 Nvidia AI chips ahead of IPO](https://the-decoder.com/spacex-signs-920-million-per-month-deal-with-google-for-110000-nvidia-ai-chips-ahead-of-ipo/)
   - **摘要：** 根据 SEC 文件，SpaceX 以每月 9.2 亿美元的价格向谷歌租赁 AI 计算能力，涉及约 11 万块 Nvidia 芯片。谷歌将利用这些算力满足其 Gemini Enterprise 平台的需求。
   - **为什么重要：** 这一交易凸显了 AI 基础设施的极度稀缺性，即使是全球最大的云提供商之一也需要从外部租赁算力。同时，SpaceX 在 IPO 前签署如此巨额协议，也反映了 AI 算力市场的金融化趋势。
   - **值得继续跟踪：** 该交易对 Nvidia 芯片供需的影响、其他云厂商的算力租赁策略、以及 SpaceX IPO 的进展。

9. **xAI 被曝长期使用 Claude 输出训练编码模型**
   - **来源网站：** The Decoder
   - **原链接：** [Elon Musk's xAI reportedly trained its coding models on Claude outputs for months before getting cut off](https://the-decoder.com/elon-musks-xai-reportedly-trained-its-coding-models-on-claude-outputs-for-months-before-getting-cut-off/)
   - **摘要：** 报道称，马斯克的 xAI 使用 Anthropic 的 Claude 来训练自己的编码模型，持续数月。即使在 Anthropic 切断访问后，xAI 仍通过私人账户和 Blackbox AI 服务继续使用。与此同时，xAI 的预训练团队已缩减至不足 5 人，多位负责人离职。
   - **为什么重要：** 这一事件揭示了 AI 行业激烈的竞争态势和潜在的“数据污染”问题。如果报道属实，xAI 的行为可能涉及违反服务条款和知识产权问题，同时也反映了其内部研发能力的困境。
   - **值得继续跟踪：** Anthropic 的回应、xAI 的官方声明、以及该事件对 AI 训练数据伦理讨论的影响。

10. **OWASP 发布 Agentic AI 安全成熟度框架**
    - **来源网站：** Infosecurity Magazine
    - **原链接：** [Infosecurity Europe: OWASP Introduces Agentic AI Security Maturity Framework](https://news.google.com/rss/articles/CBMihAFBVV95cUxOSHk2d09zVDN2U192aXdwTjA4dnVKUkFOUUh2dFBUTS0xUjJ4c1MtaE5rejRmMjhPTTRmd1lNS3ZMaVIwRUNJRkNxY1VUNFk5QXdHME5FeVlaVTAtN1RYeU81UUZOSDlPTzFuN05vdFNMcjhUTHowMGE1cl9jVEY1QUtDS1o?oc=5)
    - **摘要：** 在 Infosecurity Europe 大会上，OWASP 发布了 Agentic AI 安全成熟度框架，为组织评估和提升其 AI Agent 系统的安全性提供了结构化指南。
    - **为什么重要：** 在 Agent 安全事件频发的背景下，OWASP 作为权威安全组织推出该框架，为行业提供了急需的安全评估标准和最佳实践，有助于推动 Agent 安全的规范化。
    - **值得继续跟踪：** 框架的具体内容、企业采纳情况、以及后续的更新迭代。

11. **93% 的组织正在使用或计划使用 AI Agent 处理敏感安全任务**
    - **来源网站：** Security Magazine
    - **原链接：** [93% of Organizations Use or Plan to Use AI Agents for Sensitive Security Tasks](https://news.google.com/rss/articles/CBMixAFBVV95cUxQLTJaSkJDNVpFX3JZbjdhRkVDUjdZQXdVSFpOZkM1UjMtNXVadjRtOTIwS1d3M1VzY095Mjc3NS1pOXd2WkRvOHlsNUw2dVNhaUVfdWQxbmU4SlVnS2QxemFWN0dyMm5SajR5Z0VFLVYzcnJpV1FMc0lXQVZWVXJVSWVmSlhaeVU3RnJJY2gzLVNURGVwSUhvUVhJdVVNeWg1ZHNvMzc2cDNCWEIxcVN1VU51T29RSUNmZHNxVVlkR1hSU19I?oc=5)
    - **摘要：** 一项调查显示，高达 93% 的组织正在使用或计划使用 AI Agent 来处理敏感的安全任务。这一数据与近期频发的 Agent 安全事件形成鲜明对比，凸显了安全与效率之间的紧张关系。
    - **为什么重要：** 该数据表明，尽管存在安全风险，企业仍对 AI Agent 在安全领域的应用抱有极高期望。这为 Agent 安全解决方案提供商创造了巨大市场机会。
    - **值得继续跟踪：** 具体的安全任务类型、企业面临的主要安全挑战、以及安全 Agent 产品的市场增长。

12. **腾讯任命前 OpenAI 研究员姚顺雨为首席 AI 科学家**
    - **来源网站：** Yellow.com
    - **原链接：** [Tencent Hires Former OpenAI Researcher Yao Shunyu As Chief AI Scientist In AGI Push](https://news.google.com/rss/articles/CBMiiwFBVV95cUxQcS14QVR5UWxhZi1lZmc2a0ZnV1NNOTNjQXN5U2tqdWNYcjFpSzBLbTZuNHJEQTBsZk5aZ0JWMG1hNjYyWWJsRG5pRzE4Vkppa1lIN21qMmVaWm1TQVZmRTV3SVlIeG9oX1QzMWFranNpTTVPWG5TV2NrSzhibkVJdDVmbnpvUTJXNVp3?oc=5)
    - **摘要：** 腾讯任命前 OpenAI 研究员姚顺雨为首席 AI 科学家，以推动其 AGI 战略。姚顺雨此前在 OpenAI 从事前沿 AI 研究。
    - **为什么重要：** 这是中国科技巨头从海外顶级 AI 实验室引进顶尖人才的最新案例，反映了中国公司在 AGI 领域的雄心。姚顺雨的加入可能加速腾讯在 Agent 和基础模型方面的研发。
    - **值得继续跟踪：** 姚顺雨在腾讯的具体研究方向、腾讯 AGI 战略的调整、以及可能发布的新产品。

13. **美国 AI 立法草案曝光：年收入 5 亿美元以上公司每半年审计一次**
    - **来源网站：** cnBeta.COM
    - **原链接：** [美国AI立法草案曝光：年入5亿美元以上的大模型公司 每半年审计一次](https://www.cnbeta.com.tw/articles/tech/1564726.htm)
    - **摘要：** 美国众议院两党议员公布了一份 269 页的 AI 立法讨论稿，要求年收入 5 亿美元以上的前沿 AI 模型公司每半年进行一次安全审计，并包含员工举报保护条款。最具争议的是三年内限制各州自行监管 AI 模型开发。
    - **为什么重要：** 这是美国联邦层面最全面的 AI 监管提案之一，若通过将对 OpenAI、Anthropic、Google 等头部公司产生重大影响。审计要求将直接增加合规成本，并可能影响模型发布节奏。
    - **值得继续跟踪：** 立法进展、行业反馈、以及各州监管权的博弈。

14. **Anthropic 呼吁全球放缓 AI 开发，警告“自我改进”风险**
    - **来源网站：** 36氪
    - **原链接：** [9点1氪｜豆包推出付费后月活减少610万；Anthropic呼吁全球放缓AI开发，警告AI“自我改进”风险](https://36kr.com/p/3840996342073604?f=rss)
    - **摘要：** Anthropic 在博客文章中呼吁全球顶尖 AI 实验室考虑放缓研发步伐，理由是 AI 系统进步太快，可能很快就能在无需人类干预的情况下自我改进，带来重大社会风险。文章同时披露了其内部模型能力提升速度的数据。
    - **为什么重要：** 作为领先的 AI 安全公司，Anthropic 的呼吁具有特殊分量。这反映了行业内部对 AI 发展速度的担忧，可能影响政策制定者和投资者的态度。
    - **值得继续跟踪：** 其他 AI 公司的回应、Anthropic 是否会在自身产品中放缓迭代、以及监管机构的反应。

15. **DeepSeek 登顶美国企业新增采购榜，企业付费意愿回升**
    - **来源网站：** cnBeta.COM
    - **原链接：** [美国企业重新给DeepSeek打钱 登顶美国企业新增采购榜](https://www.cnbeta.com.tw/articles/tech/1564844.htm)
    - **摘要：** 企业支出管理平台 Ramp 发布的 6 月软件供应商榜单显示，DeepSeek 位居美国企业首次付费采购增长最猛的基础大模型厂商榜首。报道称，企业这次是直接向 DeepSeek 付费传输和接收数据，而非仅部署其开源模型。
    - **为什么重要：** 这表明美国企业对 DeepSeek 的信任度正在回升，从“尝鲜”转向“真实付费使用”。DeepSeek 的低价策略和开源生态正在赢得企业客户，对 OpenAI 和 Anthropic 构成竞争压力。
    - **值得继续跟踪：** DeepSeek 的企业客户增长数据、与 OpenAI/Anthropic 的竞争态势、以及数据安全合规方面的进展。

## 论文与开源项目

1. **字节跳动开源 DeerFlow：长周期超级 Agent 框架**
   - **来源网站：** GitHub
   - **原链接：** [bytedance/deer-flow](https://github.com/bytedance/deer-flow)
   - **摘要：** 字节跳动开源了 DeerFlow，一个长周期超级 Agent 框架，支持研究、编码和创作。它利用沙箱、记忆、工具、技能、子 Agent 和消息网关，处理从几分钟到数小时不等的复杂任务。项目已获得 70,617 颗星。
   - **为什么重要：** 这是字节跳动在 Agent 框架领域的重要布局，其“长周期”特性解决了当前 Agent 难以处理长时间任务的核心痛点。高星数反映了社区对其的高度认可。
   - **值得继续跟踪：** 框架的实际应用案例、与其他 Agent 框架（如 LangChain、AutoGPT）的对比、以及字节跳动后续的生态建设。

2. **claude-skills：跨平台编码 Agent 技能库（17,354 星）**
   - **来源网站：** GitHub
   - **原链接：** [alirezarezvani/claude-skills](https://github.com/alirezarezvani/claude-skills)
   - **摘要：** 一个包含 337 个 Claude Code 技能和 Agent 插件的开源项目，支持 Claude Code、Codex、Gemini CLI、Cursor 等 8 种编码 Agent。涵盖工程、营销、产品、合规、研究、商业运营等领域的技能。
   - **为什么重要：** 该项目极大地扩展了编码 Agent 的应用场景，从单纯的编码扩展到企业全职能领域。其跨平台兼容性降低了用户切换成本，是 Agent 生态建设的重要基础设施。
   - **值得继续跟踪：** 技能库的更新频率、社区贡献模式、以及是否会出现商业化的技能市场。

3. **IBM 开源 AssetOpsBench：工业 4.0 Agent 基准与框架**
   - **来源网站：** GitHub
   - **原链接：** [IBM/AssetOpsBench](https://github.com/IBM/AssetOpsBench)
   - **摘要：** IBM 开源了 AssetOpsBench，一个面向工业 4.0 资产运营与维护的 Agent 基准和框架。包含 460+ 场景、4 个专业 Agent（IoT、FMSR、TSFM、工单），以及基于 MCP 的多 Agent 编排蓝图。
   - **为什么重要：** 这是首个针对工业领域的标准化 Agent 基准，填补了 Agent 在制造业、能源等传统行业评估的空白。IBM 的参与有望推动 Agent 在工业场景的落地。
   - **值得继续跟踪：** 基准的评测结果、工业企业的采用情况、以及与其他工业 AI 平台的整合。

4. **Raptor：将 Claude Code 转变为通用安全 Agent（2,883 星）**
   - **来源网站：** GitHub
   - **原链接：** [gadievron/raptor](https://github.com/gadievron/raptor)
   - **摘要：** Raptor 通过配置 Claude.md、规则、子 Agent 和技能，将 Claude Code 转变为通用 AI 攻防安全 Agent。它编排安全工具的使用，支持对抗性思维、研究或攻防操作。
   - **为什么重要：** 在 Agent 安全事件频发的背景下，该项目展示了如何利用 Agent 本身进行安全防御。其“以子之矛攻子之盾”的思路具有创新性。
   - **值得继续跟踪：** 实际安全测试效果、与专业安全工具的整合、以及是否会被用于恶意目的。

5. **PDEAgentBench：科学 PDE 求解器优化 Agent 基准**
   - **来源网站：** GitHub
   - **原链接：** [YusanX/pde-agent-bench](https://github.com/YusanX/pde-agent-bench)
   - **摘要：** PDEAgentBench 是一个自动化基准框架，用于评估编码 Agent 在优化科学 PDE（偏微分方程）求解器方面的能力。
   - **为什么重要：** 这是首个针对科学计算领域的 Agent 基准，将 Agent 评估从通用编码扩展到专业科学计算。对于关注科研 Agent 和科学计算自动化的研究人员具有重要参考价值。
   - **值得继续跟踪：** 基准的评测结果、Agent 在 PDE 优化上的表现、以及后续是否扩展到其他科学计算领域。

6. **Open Mercato：AI 工程基础框架（1,370 星）**
   - **来源网站：** GitHub
   - **原链接：** [open-mercato/open-mercato](https://github.com/open-mercato/open-mercato)
   - **摘要：** 一个由 AI 构建、为 AI 设计的工程基础框架。预置了数百个架构和领域决策（多租户、RBAC、事件流、定价、销售管道等），使 Agent（Cursor、Claude Code、Codex）无需重新发明即可做出架构决策。
   - **为什么重要：** 该项目解决了 Agent 在复杂工程场景中“从零开始”的低效问题，通过预置最佳实践和约定，大幅提升 Agent 的开发效率。是 Agent 辅助工程开发的重要基础设施。
   - **值得继续跟踪：** 框架的适用场景、社区贡献情况、以及是否会出现行业特定版本。

7. **cmux：面向 AI 编码 Agent 的 macOS 终端（21,299 星）**
   - **来源网站：** GitHub
   - **原链接：** [manaflow-ai/cmux](https://github.com/manaflow-ai/cmux)
   - **摘要：** 一个基于 Ghostty 的 macOS 终端，专为 AI 编码 Agent 设计，提供垂直标签页和通知功能。
   - **为什么重要：** 高星数反映了开发者对 Agent 专用工具的需求。该终端优化了 Agent 的工作流，是 Agent 开发环境生态的重要组成部分。
   - **值得继续跟踪：** 与其他终端（如 Warp）的对比、Agent 集成深度、以及跨平台支持计划。

8. **osaurus：原生 macOS AI Agent 框架（5,606 星）**
   - **来源网站：** GitHub
   - **原链接：** [osaurus-ai/osaurus](https://github.com/osaurus-ai/osaurus)
   - **摘要：** 一个原生 macOS AI Agent 框架，支持任意模型、持久记忆、自主执行和加密身份。完全离线、开源。
   - **为什么重要：** 该项目强调“拥有你的 AI”，通过离线运行和加密身份解决 Agent 的隐私和自主权问题。对于关注数据安全和 Agent 自主性的用户具有吸引力。
   - **值得继续跟踪：** 离线性能表现、与 macOS 生态的整合、以及企业级功能扩展。

9. **AssemblyZero：参数化多 Agent 编排框架**
   - **来源网站：** GitHub
   - **原链接：** [martymcenroe/AssemblyZero](https://github.com/martymcenroe/AssemblyZero)
   - **摘要：** 一个针对 Claude Code 和 Gemini 的参数化多 Agent 编排框架，使用 Python 构建。
   - **为什么重要：** 多 Agent 编排是 Agent 系统走向复杂应用的关键。该框架提供了参数化配置，降低了多 Agent 系统的搭建门槛。
   - **值得继续跟踪：** 框架的扩展性、与其他 Agent 的兼容性、以及实际应用案例。

10. **claudectl：用本地 LLM 大脑编排 Claude Code Agent 集群**
    - **来源网站：** GitHub
    - **原链接：** [mercurialsolo/claudectl](https://github.com/mercurialsolo/claudectl)
    - **摘要：** 一个用 Rust 编写的工具，使用本地 LLM 作为“大脑”来编排 Claude Code Agent 集群，并具备从用户行为中学习的能力。
    - **为什么重要：** 该项目引入了“本地 LLM 大脑”的概念，实现了 Agent 集群的智能调度和学习能力。Rust 语言的选择也体现了对性能的追求。
    - **值得继续跟踪：** 本地 LLM 的调度效果、学习机制的实现细节、以及集群规模扩展能力。

## 今日优先阅读排序

1. **微软披露 Claude Code 凭证泄露漏洞，Miasma 蠕虫攻击 73 个 GitHub 仓库**（安全危机，影响面最广）
2. **Agentic AI 红队测试发现零点击“人在回路”绕过攻击链**（安全机制的根本性缺陷）
3. **月之暗面发布 Kimi Code CLI：开源终端 AI 编码 Agent**（中国公司重要开源项目）
4. **阿里发布 Qwen3.7-Plus：将多模态 AI 转变为全自主 Agent**（模型能力重大进展）
5. **Anthropic 被曝雇佣 1000 名人类工程师“培训”Claude Code**（行业悖论与成本揭秘）
6. **华为云发布 Agentic Infra 新范式，不拼 Token 单价赌国产算力**（产业战略转向）
7. **字节跳动开源 DeerFlow：长周期超级 Agent 框架**（高星数开源项目）
8. **SpaceX 与谷歌签署 9.2 亿美元/月 AI 芯片租赁协议**（算力稀缺性标志性事件）
9. **xAI 被曝长期使用 Claude 输出训练编码模型**（行业竞争与伦理争议）
10. **OWASP 发布 Agentic AI 安全成熟度框架**（安全规范化里程碑）
