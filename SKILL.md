---
name: persona-style-writer
description: >
  人物气质转译写作 skill，用于中文长文、公众号文章、产品测评、评论文章和观点随笔。
  当用户要求用某个人物的风格、气质、口吻、表达方式、访谈方式或论证方式写作时使用。
  适用对象包括名人、企业家、访谈者、评论者、创作者、学者、高管、媒体人物和历史人物，
  前提是该人物的公开表达气质能从公开资料中归纳出来。例如 "用马斯克的风格写",
  "用易立竞的风格写", "像某某那样写", "某某口吻"。本 skill 会产出安全的气质转译稿，
  而不是直接冒充或一比一模仿，并把指定人物转译为高层次、
  非侵权的表达特征，用用户自己的账号片尾写作，并执行四层质检和公众号合规风险检查，
  包括侵权、虚假宣传、隐私、诱导关注和敏感表达。
---

# 人物气质转译写作

根据指定人物的公开可观察表达气质，写中文公众号长文、产品测评和评论文章。目标是“气质转译”，不是冒充本人，也不是复制其独特表达。

## 适用范围

适用于任何能从公开材料中合理总结出表达气质的人物，包括：

- entrepreneurs and executives
- interviewers and hosts
- writers and columnists
- reviewers and critics
- creators and influencers
- academics and public intellectuals
- investors and product commentators
- historical figures

“网上能搜到名字”本身不够。必须有足够公开材料能推断宽泛表达特征，不能凭空发明一个人格。

如果人物冷门、不熟悉、存在重名，或其表达方式可能近期发生变化，先查公开资料再写。若无法浏览或公开材料太少，要求用户提供 2-5 个参考链接、访谈、文章、视频、转录稿，或直接描述想要的气质特征。

不要用私人信息、八卦、人肉资料、泄露聊天记录或未经证实的传闻来推断人物风格。

## 核心规则

不要直接模仿在世人物的独特个人风格、标志性措辞、高频口头禅、私人形象或身份。不要声称文章由该人物写作、背书、受访、授权或认可。

Instead, transform the requested figure into broad, reusable traits:

- reasoning mode
- rhythm
- stance
- question style
- argument structure
- level of sharpness
- emotional temperature
- audience relationship

Use those traits to create an original article under the user's account identity.

If the user asks for exact imitation, respond by reframing:

> 我不能一比一模仿在世名人的个人风格，但可以把它转译成高层次表达特征来写，比如冷静追问、工程化判断、第一性原理、商业拷问、克制讽刺等。

Then write the transformed version.

## Required Inputs

Extract these from the user's prompt:

1. **指定人物**: 用户点名的人物或气质参考。
2. **Topic**: the article subject, product, company, event, or concept.
3. **文章类型**: 产品测评、评论、随笔、访谈式批评、解释型文章或公众号长文。
4. **User account identity**: account name, author name, contact, slogan, or footer text if provided.

If account identity is missing, use placeholders rather than inventing:

```text
> / 作者：[你的账号名]
> / 联系或投稿：[你的联系方式]
```

## 气质转译

Before writing, silently map the requested figure to high-level traits. Do not output this mapping unless the user asks.

Examples:

- **马斯克-like request**: first-principles reasoning, engineering judgment, compressed sentences, future-facing bets, direct tradeoff framing, tolerance for risk, product-system thinking.
- **易立竞-like request**: calm pressure, short and sharp questions, interview-like progression, refusal to flatter, continuous boundary probing, silence and tension, precise moral discomfort.
- **罗永浩-like request**: conversational confidence, product-manager perspective, self-aware humor, consumer-rights sensitivity, sharp but performative judgment.
- **吴军-like request**: historical framing, technological lineage, sober explanation, system-level causal chain, patient but opinionated analysis.

These examples are trait translations, not exact imitation templates.

## 写作流程

### 1. Judge the Task

Decide whether the request is a writing task. Use this skill for:

- public-account longform
- Chinese product review
- product or company commentary
- AI product analysis
- interview-style critical essay
- essay based on supplied material

Do not use this skill for:

- short social posts
- pure title generation
- legal, medical, or financial advice
- 直接冒充指定人物
- fake interviews or fabricated quotes
- 假装由指定人物本人写作的内容

### 2. Gather Facts

Use only facts supplied by the user or facts you have verified. If the topic depends on recent information, search or ask the user for source material.

对于指定人物：

- 如果人物知名，且高层次表达特征相对稳定，可以使用通用公开认知，但必须保持宽泛转译。
- 如果人物不熟、冷门、地域性强、近期变化大，或可能存在信息更新，先查公开材料。
- 如果存在重名，先问清楚是哪一位。
- If the user only gives a vague label like "某个网红那种感觉", ask for a name or examples.
- If no reliable public material exists, do not invent a style. Offer a generic style direction instead, such as "冷静追问型", "第一性原理型", "产品经理吐槽型", or "商业媒体分析型".

Never fabricate:

- personal experience
- screenshots
- test results
- private conversations
- product access
- quotes from the named figure
- official endorsement

If first-hand testing is missing, write:

- "基于公开信息"
- "从目前可见信息看"
- "如果后续实测成立"
- "这里还需要真实截图或灰测体验补充"

### 3. 写文章

Write in Chinese unless the user asks otherwise.

Use public-account longform structure:

1. concrete opening scene or tension
2. topic hook
3. product / event explanation
4. sharp core question
5. layered analysis
6. counterargument or user-side concern
7. risk and boundary discussion
8. closing judgment
9. user's account footer

Avoid excessive Markdown headings unless the user asks for a structured report. Public-account articles should read like prose, not a slide deck.

### 4. 片尾

Do not use another person's byline, email, signature, or fixed tail.

Use the user's account footer if provided.

If not provided, use this neutral footer:

```text
以上，如果这篇文章对你有帮助，欢迎点个赞、在看，也可以转发给需要的人。

谢谢你看到这里，我们下篇再见。

> / 作者：[你的账号名]
> / 联系或投稿：[你的联系方式]
```

Avoid strong engagement inducement. Do not write "必须转发", "不转不是朋友", "转发后领取", "点赞抽奖", or similar inducement.

## 四层质检

Run this before final output. The check may be internal unless the user asks to see it.

### L1 Hard Rules

Check and fix:

- 不直接冒充指定人物
- no "我是某某" unless the user is that person and asks to write autobiographically
- no fake endorsement
- no fabricated quotes
- no fabricated screenshots or tests
- no exact signature phrasing from the named figure
- no copied fixed footer from another creator
- no excessive headings if writing public-account prose

### L2 Style Consistency

Check:

- the transformed traits match the requested figure at a high level
- the article does not drift into generic AI prose
- tone, rhythm, and question style are consistent
- the piece has a clear stance rather than only summary
- the reader can tell why this voice was requested without seeing direct imitation

### L3 Content Quality

Check:

- every important claim has support
- analysis is not just feature listing
- product review covers actual user value, usage scenario, cost, risk, and trust
- opposing view is treated fairly
- limitations are named clearly
- missing facts are marked as missing rather than invented

### L4 Human Feel

Check:

- article feels written for a real reader, not a prompt demo
- sentences have rhythm and tension
- examples are concrete
- judgment feels earned
- ending lands on a clear insight, not generic summary

## 公众号合规风险检查

After the writing quality check, run a compliance risk check. This does not guarantee platform approval, but it reduces obvious risk.

### Infringement

Check:

- no unauthorized byline or identity use
- no copied article structure from a living creator
- no long unlicensed quote
- no claim that the named figure wrote, reviewed, authorized, or endorsed the article
- no unlicensed use of screenshots, logos, or images unless the user provided rights or it is clearly fair commentary

### False Claims

Check:

- no invented product capability
- no fake test result
- no fake internal source
- no "官方确认" unless source confirms it
- no exaggerated certainty for rumors, leaks, or gray-test information

Use cautious phrasing:

- "公开信息显示"
- "灰测信息显示"
- "目前还不能确认"
- "需要等正式上线后验证"

### Privacy

Check:

- no personal phone numbers, private chat records, addresses, ID numbers, or private account details
- blur or omit private screenshots
- do not expose non-public group-chat content
- for examples involving users, anonymize and generalize

### Engagement Inducement

Check:

- avoid forced or conditional engagement
- avoid "转发领取", "点赞解锁", "不转会错过" style pressure
- mild footer requests such as "欢迎点赞、在看、转发" are acceptable, but keep them restrained

### Sensitive Expression

Check:

- avoid political rumor, discriminatory expression, hate, harassment, pornographic, violent, gambling, fraud, and illegal content
- avoid high-risk medical, legal, financial, or investment conclusions unless framed as non-professional discussion
- for public companies or products, distinguish opinion from fact

## 输出规则

Default output:

1. article title options
2. article body
3. footer using the user's account information or placeholders
4. short "发布前风险提示" only if meaningful risks remain

Do not output the full four-layer check unless the user asks. If the user asks for the check, summarize it concisely.

If the user says "只给正文", output only title options and article body, no check report.

If the user says "不要片尾", omit the footer.

If the user says "按我的账号片尾", use their supplied footer exactly unless it creates compliance risk.
