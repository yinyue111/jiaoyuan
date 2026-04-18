<div align="center">

# jiaoyuan

**一个基于公开材料整理的毛泽东式战略分析 skill。**  
**A Mao-style strategic analysis skill distilled from public sources.**

不是人物 cosplay。  
不是语录拼盘。  
是一套能被 agent 直接调用的判断框架。

Not a character cosplay.  
Not a quote collection.  
A working framework an agent can actually use.

[效果示例 / Examples](#效果示例--examples) · [快速调用 / Quick Start](#快速调用--quick-start) · [安装 / Installation](#安装--installation) · [项目结构 / Project Structure](#项目结构--project-structure) · [边界 / Boundaries](#边界--boundaries)

</div>

---

## 这是什么 / What This Is

`jiaoyuan` 把毛泽东在主要矛盾、对象划分、阶段判断、统一战线、群众动员这些问题上的判断方法，整理成一个可运行的 skill。

`jiaoyuan` turns Mao-style strategic reasoning on contradiction, actor classification, phase judgment, united front, and mass mobilization into a runnable skill.

它的重点不是模仿腔调。
它的重点是让回答先有骨架，再有力度。

It is not mainly about mimicking a voice.
It is about giving answers a stable structure before giving them force.

仓库里的运行真身是 `SKILL.md`。
README 负责让人快速看懂它能做什么、怎么装、怎么用。

The runtime source of truth is `SKILL.md`.
This README is the front door.

---

## 它能做什么 / What It Does

- 把复杂问题先拆成主要矛盾、对象、阶段、动作  
  Breaks a messy problem into contradiction, actors, phase, and action
- 遇到具体人物、公司、政策、历史事件时，先研究再判断  
  Researches concrete cases before making strategic claims
- 保留历史张力，不把人物写成一条平滑直线  
  Keeps historical tension instead of flattening the figure into a mascot
- 为 agent 提供 6 个核心模型、8 条决策启发式和 14 份研究底稿  
  Gives the agent 6 core models, 8 decision heuristics, and 14 research packs

---

## 效果示例 / Examples

### 示例一 / Example 1

**输入 / Prompt**

```text
用毛泽东的视角分析一家创业公司里，创始人与职业经理人的冲突。
```

**输出风格示例 / Sample Output Style**

```text
先定性。
这不是一般的人事摩擦，是路线和领导权的冲突。

主要矛盾不在两个人谁更委屈，
在公司下一阶段到底由谁定义目标，谁来组织资源。

这时候不能把人混成一锅。
创始人、经理层、核心骨干、摇摆中层，不是一类对象。
对象不分清，动作就会乱。

如果创始人还想掌握方向，就不能只靠资格压人。
要把真正能打的人重新组织起来，把摇摆者稳住，把公开对撞的战场缩到最小。
```

### 示例二 / Example 2

**输入 / Prompt**

```text
If a small AI product is being squeezed by platform giants, where should it break through?
```

**输出风格示例 / Sample Output Style**

```text
Do not crash into the center.
If the giants own distribution, they want you to fight on their terrain.

Your first task is to identify the contradiction that actually decides survival.
Usually it is not model quality. It is access, switching cost, or speed of iteration.

Then classify the actors.
Who is a direct enemy, who is a temporary ally, who is a neutral force you can pull over.

If the center is hard, hit the flank.
Find the narrow workflow, the ignored user group, or the ugly edge case the big system does not want to touch.
```

### 示例三 / Example 3

**输入 / Prompt**

```text
用毛式方法看 OpenAI 和 Anthropic 的竞争，先别急着下结论。
```

**这个 skill 会怎么干 / How The Skill Handles It**

- 先认定这是事实题，不直接摆观点  
  First treats it as a fact-grounded question
- 先回到 `references/research/` 和外部可核材料  
  Then checks internal research packs and verifiable external material
- 先写事实底稿，再进角色化判断  
  Builds a factual brief before switching into voice

这点很关键。
这玩意儿不是一上来就喊口号。

That matters.
The skill is designed not to jump straight into slogans.

---

## 快速调用 / Quick Start

你可以直接这样叫它。
You can invoke it with prompts like these.

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

```text
Switch into jiaoyuan mode and give me contradiction, actors, phase, and next action.
```

---

## 方法骨架 / Core Method

这个 skill 的主轴很清楚。
The spine of the skill is intentionally narrow and sharp.

- 主要矛盾先行  
  Find the principal contradiction first
- 调查先于判断  
  Investigation before judgment
- 中心太硬就打边缘  
  If the center is too hard, break through the flank
- 联合与斗争并行  
  Alliance and struggle can coexist
- 群众经验必须经过组织加工  
  Raw mass experience must be turned into organized line
- 战略上藐视，战术上重视  
  Strategic confidence, tactical seriousness
- 利用对手之间的矛盾打开空间  
  Use contradictions among opponents to create room

它不是把毛泽东写成永远正确。
相反，它明确保留了不同时期的断裂、代价和争议。

It does not present Mao as uniformly correct.
It explicitly preserves rupture, cost, and controversy across periods.

---

## 安装 / Installation

### 方式一 / Option 1

把仓库直接放进共享技能目录。
Clone the repository into the shared skills directory.

```bash
git clone https://github.com/yinyue111/jiaoyuan.git ~/.openclaw/skills/jiaoyuan
```

### 方式二 / Option 2

直接克隆到当前工作区的 `skills/` 目录。
Clone it straight into the active workspace `skills/` directory.

```bash
git clone https://github.com/yinyue111/jiaoyuan.git ./skills/jiaoyuan
```

OpenClaw 会自动从工作区 `skills/` 或共享目录 `~/.openclaw/skills/` 加载技能。
新开一个 session 后就能看到它。

OpenClaw loads skills from the workspace `skills/` directory and from `~/.openclaw/skills/`.
Start a new session and the skill becomes available.

### 包文件 / Packaged File

仓库根目录已经附带 `jiaoyuan.skill`。
它适合做归档、传输或分发。

The repository root also includes `jiaoyuan.skill` for packaging, transfer, or distribution workflows.

### 校验与重打包 / Validate and Repackage

在 skill 根目录做快速体检。
Run a quick health check in the skill root.

```bash
python3 scripts/quality_check.py SKILL.md
```

如果你是在 OpenClaw 工作区里维护它，可以这样重新打包。
If you maintain it inside an OpenClaw workspace, repackage it like this.

```bash
python3 skills/skill-creator/scripts/package_skill.py skills/jiaoyuan
```

---

## 项目结构 / Project Structure

```text
.
├── README.md
├── SKILL.md
├── jiaoyuan.skill
├── references/
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

### 关键文件 / Key Files

- `SKILL.md`  定义触发条件、边界、工作流和表达约束  
  Defines triggers, boundaries, workflow, and output constraints
- `references/research/`  放研究底稿和补料包  
  Holds the research base and source packs
- `references/review-a.md` 与 `references/review-b.md`  放结构复核和真实性复核  
  Hold structure review and historical-fidelity review
- `scripts/quality_check.py`  做交付前检查  
  Runs a pre-delivery check
- `scripts/merge_research.py`  看研究覆盖面和缺口  
  Summarizes coverage and gaps across the research set

---

## 什么时候该用 / When To Use It

适合这些问题。
Good fit for prompts like these.

- 组织冲突、路线分歧、联盟博弈  
  Organizational conflict, line struggle, coalition dynamics
- 弱势方如何破局  
  How a weaker side should break through
- 一个局面现在处在哪个阶段  
  Which phase a situation is in
- 如何区分敌人、朋友和中间力量  
  How to distinguish enemies, allies, and swing actors

不适合这些问题。
Not a fit for prompts like these.

- 只想要中立历史总结  
  Plain neutral history summaries
- 要求伪造原话、史实或会谈  
  Fabricated quotes, events, or meetings
- 想把高争议历史后果洗成漂亮口号  
  Sanitizing contested historical consequences into slogans
- 不需要角色框架，只要普通商务分析  
  Plain business analysis with no role-based frame

---

## 边界 / Boundaries

这部分不是装样子。
This part is not decorative.

- 不伪造毛泽东没有说过的话  
  Do not fabricate quotes Mao never said
- 不把视角化推演伪装成已证实事实  
  Do not present role-based inference as established fact
- 遇到争议历史后果，必须保留代价、断裂和外部批评  
  Preserve cost, rupture, and external criticism on disputed historical outcomes
- 涉及具体现实对象时，先研究，再判断  
  Research concrete real-world subjects before judging them

这也是这个 skill 和低配角色扮演的分水岭。
That is the line between this skill and cheap roleplay.

---

## 给维护者的话 / Notes For Maintainers

如果你继续扩这套 skill，最该守住的不是语气，是方法。
If you extend this skill, protect the method before the tone.

先看问题是不是事实题。
先补事实底稿。
再决定能不能进入角色化输出。

Classify the question first.
Build the factual brief second.
Only then move into voice.

如果顺序反了，写出来的东西就容易变成有气势、没根的废话。
If you reverse that order, the output starts sounding forceful but hollow.

---

## 当前状态 / Current Status

- 已完成完整版研究稿收口  
  Full research pass completed
- 已完成从 `mao-zedong-perspective` 到 `jiaoyuan` 的命名迁移  
  Renamed from `mao-zedong-perspective` to `jiaoyuan`
- 仓库根目录已附带 `jiaoyuan.skill`  
  `jiaoyuan.skill` is included in the repository root
- 当前仓库地址  
  Repository URL

```text
https://github.com/yinyue111/jiaoyuan
```
