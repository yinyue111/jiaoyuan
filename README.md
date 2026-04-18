# jiaoyuan

一个基于公开材料整理的毛泽东式战略分析 skill。

它不做低配角色扮演，也不拿历史人物当噱头。
它做的事更具体一点：把毛泽东在主要矛盾、对象划分、阶段判断、统一战线、群众动员这些问题上的判断方法，整理成一套可被 agent 稳定调用的分析框架。

## 这个 skill 能干什么

- 用毛泽东式视角分析复杂局势、组织斗争、阶段转换和冲突博弈
- 处理现实议题时，先做事实核对，再进入视角化判断
- 在回答里稳定给出主要矛盾、对象划分、阶段位置和动作建议
- 为 agent 提供成体系的研究材料、复核稿和质量检查脚本

## 适用场景

适合这类问题：

- 用毛泽东的视角看这件事
- 如果按毛式方法分析一家公司的组织冲突，该怎么拆
- 这场舆论战、路线争论、联盟博弈，主要矛盾是什么
- 一个弱势方怎么找突破口、怎么联合、怎么定阶段

不适合这类问题：

- 单纯问历史知识，且只要客观中立总结
- 要求伪造毛泽东原话、会谈、引语或立场
- 想把高争议历史后果洗成口号式正当化
- 不需要角色化表达，只要普通分析

## 工作方式

这个 skill 的核心流程不是先摆态度，而是先做判断准备。

如果问题是纯框架题，可以直接进入毛式分析。
如果问题涉及具体人物、公司、国家、历史事件、政策或现实争议，就先研究，再回答。
研究时优先从 `references/research/` 里找对应材料，先写事实底稿，再进入正式判断。

正式回答默认围绕五步展开：

- 我的判断
- 主要矛盾
- 对象划分
- 阶段位置
- 动作建议

## 核心方法

这个 skill 的骨架来自几条稳定主轴：

- 主要矛盾先行
- 调查先于判断
- 从边缘找突破口
- 联合与斗争并行
- 群众路线要经过组织加工
- 战略上藐视，战术上重视
- 利用对手之间的矛盾打开空间

它不是把毛泽东写成一个永远正确的万能战略家。
相反，skill 明确保留了分期意识和历史张力，尤其强调不把革命时期的方法机械套到晚年政治运动，不把强势表达误当成事实本身。

## 仓库结构

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

## 关键文件说明

- `SKILL.md` 是主入口，定义触发条件、边界、工作流、核心模型和表达规则
- `references/research/` 是研究底稿，按主题和时期拆开
- `references/review-a.md` 与 `references/review-b.md` 是结构和真实性复核稿
- `scripts/quality_check.py` 用来做交付前体检
- `scripts/merge_research.py` 用来快速看研究覆盖面和缺口

## 使用建议

如果你是直接调用这个 skill 的 agent，最稳的用法不是一上来学语气，而是先按 `SKILL.md` 的流程走。

先判断问题属于纯框架题、事实题还是混合题。
如果需要事实支撑，先读相关 research 文件。
材料不够就停，不要硬凹结论。

## 本项目的边界

- 基于公开材料整理，不声称还原历史人物真实在场发言
- 不伪造史实，不伪造引语，不拿角色化输出冒充史料
- 面对高争议问题，必须保留代价、断裂和外部批评
- 强调方法论，不鼓励口号化模仿

## 校验与打包

在仓库根目录可直接运行：

```bash
python3 scripts/quality_check.py SKILL.md
```

如果你在 OpenClaw 工作区里维护这个 skill，可用打包脚本重新生成 `.skill` 文件：

```bash
python3 skills/skill-creator/scripts/package_skill.py skills/jiaoyuan
```

## 当前状态

这个版本已经完成完整研究稿收口、命名改造和仓库上传。
当前 GitHub 仓库名为 `jiaoyuan`，导出包名为 `jiaoyuan.skill`。
