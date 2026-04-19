<div align="center">

# jiaoyuan

**一个给 agent 用的毛式战略分析 skill。**  
**A Mao-style strategic analysis skill built for agents.**

不是人物 cosplay。  
不是语录拼盘。  
不是管理学鸡汤。  
是一套先分矛盾、再分对象、再分阶段、最后落动作的分析框架。

Not a character cosplay.  
Not a quote scrapbook.  
Not generic strategy fluff.  
It is a structured frame for contradiction, actors, phase, and action.

[效果示例 / Examples](#效果示例--examples) · [快速上手 / Quick Start](#快速上手--quick-start) · [安装 / Installation](#安装--installation) · [研究方法 / Research Method](#研究方法--research-method) · [项目结构 / Project Structure](#项目结构--project-structure)

</div>

---

## 这玩意儿到底干嘛的 / What This Skill Actually Does

`jiaoyuan` 把毛泽东在主要矛盾、对象划分、阶段判断、统一战线、群众动员这些问题上的判断方法，整理成一个可运行的 skill。

`jiaoyuan` turns Mao-style reasoning on contradiction, actor classification, phase judgment, united front, and mass politics into a runnable skill.

重点不是学口音。
重点是把回答从一堆情绪和口号里拽出来，先立骨架，再给力度。

It is not mainly about voice mimicry.
It is about forcing answers to get the structure right before sounding powerful.

运行真身在 `SKILL.md`。
`README.md` 负责给人看门面。
`references/` 负责给 agent 找证据、找例子、找路由。

---

## 它适合什么问题 / Good Fit

- 组织冲突和路线分歧  
  Organizational conflict and line struggle
- 弱势方怎么破局  
  How a weaker side breaks through
- 一个局面现在处在哪个阶段  
  What phase a situation is in
- 敌人、朋友、中间力量怎么分  
  How to classify enemies, allies, and swing actors
- 现实议题怎么先做事实底稿，再进角色化判断  
  How to build a factual brief before switching into voice

它不适合这些事。

- 只想要中立历史概述  
  Plain neutral history summaries
- 想伪造原话、会谈、史实  
  Fabricated quotes, meetings, or events
- 想把高争议历史后果洗成漂亮口号  
  Sanitizing catastrophic outcomes into slogans
- 想拿毛式框架当内部肃反、封口、造反式治理手册  
  Using it as a playbook for purges, silencing, or destructive mobilization

---

## 效果示例 / Examples

### 示例一 / Example 1

**输入 / Prompt**

```text
用毛泽东的视角分析一家创业公司里，创始人与职业经理人的冲突。
```

**输出风格示例 / Sample Output**

```text
先定性。
这不是一般的人事摩擦，是路线和领导权的冲突。

主要矛盾不在两个人谁更委屈，
在公司下一阶段到底由谁定义目标，谁来组织资源。

对象不能混成一锅。
创始人、经理层、核心骨干、摇摆中层，不是一类力量。
对象不分清，动作就会乱。

如果创始人还想掌握方向，就不能只靠资格压人。
要把真正能打的人重新组织起来，把摇摆者稳住，把公开对撞的战场缩到最小。
```

### 示例二 / Example 2

**输入 / Prompt**

```text
If a small AI product is being squeezed by platform giants, where should it break through?
```

**输出风格示例 / Sample Output**

```text
Do not crash into the center.
If the giants own distribution, they want you to fight on their terrain.

The principal contradiction is usually not model quality.
It is access, switching cost, or speed of iteration.

Then classify the actors.
Who is the direct enemy, who is a temporary ally, who is neutral but movable.

If the center is hard, hit the flank.
Find the ugly workflow or ignored user group the big system does not want to touch.
```

### 示例三 / Example 3

**输入 / Prompt**

```text
用毛式方法拆一场公共舆论危机，先别急着道德表态。
```

**这个 skill 会怎么干 / How The Skill Handles It**

- 先定性这是叙事权和动员能力的争夺  
  First frames it as a struggle over narrative control and mobilization
- 先补事实底稿，不顺着情绪跑  
  Builds a factual brief before chasing public emotion
- 先分对象，再看动作  
  Classifies actors before suggesting action

这点很关键。
这玩意儿不是一上来就喊口号。

---

## 快速上手 / Quick Start

### 直接触发 / Trigger It Directly

```text
用毛泽东的视角看这场组织斗争
```

```text
如果按毛式方法拆这个竞争格局，主要矛盾是什么
```

```text
切到毛式视角，帮我判断这家公司现在处在哪个阶段
```

```text
Use a Mao-style strategic frame to analyze this coalition and tell me where the real contradiction is.
```

### 最小使用路径 / Minimum Path After Install

装完以后，新开一个 session。
直接扔一个带现实对象的问题进去。
如果题目涉及具体公司、政策、人物、历史事件，skill 会先走事实底稿，再进毛式判断。

如果你是维护者，最短路径是这样。

- 先看 `SKILL.md`
- 再看 `references/INDEX.md`
- 要校准输出骨架就看 `references/casebook.md`
- 要补资料再进 `references/research/`

---

## 方法骨架 / Core Method

这套 skill 的主轴很窄。
但够硬。

- 主要矛盾先行  
  Find the principal contradiction first
- 调查先于判断  
  Investigation before judgment
- 中心太硬就打边缘  
  If the center is too hard, hit the flank
- 联合与斗争并行  
  Alliance and struggle can coexist
- 群众经验必须经过组织加工  
  Raw mass experience must be turned into organized line
- 战略上藐视，战术上重视  
  Strategic confidence, tactical seriousness
- 利用敌人之间的矛盾打开空间  
  Use contradictions among opponents to create room

这套 skill 还额外补了青年形成期那条线。
不是只盯成熟期文本。

- 先锻人，再成事
- 先结社，再扩张
- 先小联合，后大联合
- 从个案打穿结构
- 路线必须落到组织载体和权力形态

它不是把毛泽东写成永远正确。
相反，它明确保留了不同时期的断裂、代价和争议。

---

## 安装 / Installation

### 方式一 / Option 1

把仓库直接放进共享技能目录。

```bash
git clone https://github.com/yinyue111/jiaoyuan.git ~/.openclaw/skills/jiaoyuan
```

### 方式二 / Option 2

直接克隆到当前工作区的 `skills/` 目录。

```bash
git clone https://github.com/yinyue111/jiaoyuan.git ./skills/jiaoyuan
```

OpenClaw 会从工作区 `skills/` 或共享目录 `~/.openclaw/skills/` 自动加载 skill。
新开一个 session 就能看到它。

### 包文件 / Packaged File

仓库根目录带了 `jiaoyuan.skill`。
适合归档、传输和分发。

### 校验与重打包 / Validate and Repackage

```bash
python3 skills/jiaoyuan/scripts/quality_check.py skills/jiaoyuan/SKILL.md
```

```bash
python3 skills/skill-creator/scripts/package_skill.py skills/jiaoyuan
```

---

## 研究方法 / Research Method

这套 skill 不是靠几句语录凑出来的。
它有几条硬约束。

- 先分时期，不把 `1927` 到 `1976` 写成一条平滑直线  
  It keeps Mao periodized instead of flattening him into one stable character
- 先分事实题和框架题  
  It separates fact-grounded questions from pure framework questions
- 事实题先写事实底稿，再进角色化判断  
  Fact-grounded questions require a factual brief first
- 保留高张力节点和灾难性后果  
  It preserves rupture, tension, and catastrophic consequences
- 引具体原话时，优先对照正式中文版本和权威编定本  
  It prefers formal Chinese editions and authoritative compilations for direct quotations

### 路由文件 / Navigation Files

- `references/INDEX.md`  资料入口和读法路由  
  Start here when you do not know which research pack to read
- `references/casebook.md`  输出骨架判例集  
  Start here when you want to calibrate output shape
- `references/review-a.md`  结构与流程复核  
  Structural review notes
- `references/review-b.md`  历史真实性与辨识度复核  
  Historical-fidelity review notes

---

## 项目结构 / Project Structure

```text
.
├── README.md
├── SKILL.md
├── jiaoyuan.skill
├── references/
│   ├── INDEX.md
│   ├── casebook.md
│   ├── extraction-framework.md
│   ├── review-a.md
│   ├── review-b.md
│   └── research/
│       ├── 01-writings.md
│       ├── 02-conversations.md
│       ├── 03-expression-dna.md
│       ├── 04-external-views.md
│       ├── 05-decisions.md
│       ├── 06-timeline.md
│       ├── 07-primary-source-map.md
│       ├── 08-high-tension-nodes.md
│       ├── 09-gap-fill-source-pack.md
│       ├── 10-cpc-party-history-pack.md
│       ├── 11-selected-works-full-pass.md
│       ├── 12-selected-works-vol6-9-and-late-theory.md
│       ├── 13-current-round-verified-gap-pack.md
│       └── 14-current-round-merged-gap-map.md
└── scripts/
    ├── download_subtitles.sh
    ├── merge_research.py
    ├── quality_check.py
    └── srt_to_transcript.py
```

---

## 边界 / Boundaries

这部分不是装样子。
是真的分水岭。

- 不伪造毛泽东没说过的话  
  Do not fabricate quotes Mao never said
- 不把视角化推演伪装成已证实事实  
  Do not present role-based inference as established fact
- 碰到高争议历史后果，必须保留代价、断裂和外部批评  
  Preserve cost, rupture, and external criticism
- 碰到现实对象，先研究，再判断  
  Research concrete subjects before judging them
- 不能拿这套框架替人设计肃反、封口、造反式治理  
  Do not turn this skill into a purge or silencing playbook

---

## 给维护者的话 / Notes For Maintainers

如果你继续扩这套 skill，最该守住的不是语气。
是方法。

先看问题是不是事实题。
先补事实底稿。
再决定能不能进入角色化输出。

如果顺序反了，写出来的东西就会变成有气势、没根的废话。

仓库地址在这。

```text
https://github.com/yinyue111/jiaoyuan
```