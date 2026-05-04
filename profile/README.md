# Agentic-CliniAI
> 致力于创建安全、透明、可溯源的AI诊疗工具，辅助医疗专业人员提升诊疗效率与准确性。

[![Website](https://img.shields.io/badge/website-agentic--cliniai.github.io-blue)](https://agentic-cliniai.github.io)

## DermAgent — 皮肤科诊断智能体

> 基于多Agent协作的皮肤科诊断系统：迭代追问 + 多模态感知 + 468疾病知识库

468 皮肤病种 · 35+ ICD-10 类别 · 11 检索工具 · 4 感知模态

**Demo 演示（面部红斑3周 → SLE 诊断）：**

```
╭──────────────────────────────────────────────────╮
│ DermAgent — 皮肤科诊断Agent系统                    │
│ Multi-agent diagnostic system for dermatology     │
╰──────────────────────────────────────────────────╯

主诉：面部红斑3周
年龄：20
性别：女

  ✔ 主诉分析  — 初始印象: 接触性皮炎, 脂溢性皮炎, 玫瑰痤疮, SLE
    ▪ 接触性皮炎
    ▪ 脂溢性皮炎
    ▪ 玫瑰痤疮
    ▪ 系统性红斑狼疮
    ? 需确认分布区域、光敏感、接触史、全身症状

  ✔ 追问与检查规划  迭代#1  — 4 个追问 · 4 项检查
    Q1: 红斑分布在面部哪些区域？  →  两边脸颊和鼻梁，对称，边界不清
    Q2: 有无瘙痒灼热？是否日晒后加重？  →  发烫发痒，晒太阳后明显加重
    Q3: 发病前是否换过护肤品？  →  最近换了新防晒霜和洗面奶
    Q4: 有无口腔溃疡、脱发、关节痛、发热？  →  没有溃疡和关节痛，但感觉累，有时低烧
    检查: 皮肤镜, ANA+dsDNA抗体, 皮肤病理, 斑贴试验

  ✔ 多模态证据采集  — 体格检查完成
    [physical] 皮肤散在皮疹; 未见特征性分布模式 (置信度: 0.4)

  ✔ 知识检索  — 本地知识库 + Web Search + DermNet
    LLM诊断: 系统性红斑狼疮, 光变应性接触性皮炎, 玫瑰痤疮

  ✔ Memory 1 · 知识融合  — 融合完成

  ✔ Check_Agent · 疾病验证  — 验证 5 个诊断
    ✘ 光变应性接触性皮炎  核心皮损停用后仍持续
    ✘ 系统性红斑狼疮  毛细血管扩张更符合玫瑰痤疮，缺少血清学证据

  ✔ 信息充分性评估  — 路由: → 追加追问

  ✔ 追问与检查规划  迭代#2  — 5 个追问 · 3 项检查
    Q5: 停用新护肤品后有无减轻？  →  灼热稍减轻，红斑没完全消
    Q6: 头皮眉毛鼻唇沟是否油腻发红？  →  没有
    Q7: 能否看到扩张的红血丝？  →  能看到，一热就更明显
    检查: 皮肤镜, ANA+dsDNA+ENA抗体谱, 补体C3/C4+血常规+尿常规

  ✔ 知识检索  搜索深度:2  — + DermNet + Orphanet + OMIM

  ✔ Memory 1 · 知识融合  — 融合完成 (迭代#2)

  ✔ Check_Agent · 疾病验证  — 验证 5 个诊断
    ✘ 光变应性接触性皮炎  持续皮损+系统症状无法解释
    ✘ 系统性红斑狼疮  毛细血管扩张+丘疹更似玫瑰痤疮，缺少血清学证据

  ✔ 信息充分性评估  — 路由: → 生成最终诊断

  ✔ Memory 2 · 最终诊断  — 生成 5 个鉴别诊断
    #1 系统性红斑狼疮 (SLE)  █████████░ 90%
           青年女性+蝶形红斑+光敏感+乏力低热 → 符合ACR标准
    #2 SLE  ███████░░░ 75%
    #3 玫瑰痤疮  ██████░░░░ 60%
    #4 亚急性皮肤型红斑狼疮  ████░░░░░░ 45%
    #5 SCLE  ███░░░░░░░ 30%

  ✔ 报告生成  — 报告已生成
    ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
    【主要诊断】系统性红斑狼疮 (SLE)  置信度: 80%
    依据: 青年女性蝶形红斑+光敏感+毛细血管扩张+乏力低热
    建议: 严格防晒 + 转诊风湿免疫科 → ANA+dsDNA+补体+皮肤活检
    迭代次数: 2, 搜索深度: 2
```

**更多案例：** 银屑病 · 天疱疮 → [在线体验 Demo](https://agentic-cliniai.github.io/dermagent.html)

## 核心项目

- **DermAgent** — 皮肤科多Agent诊断系统 [`dermagent`](https://github.com/agentic-cliniai/dermagent)
- **Evidence Tracking Agent** — 循证医学决策支持代理系统 [`meddecision`](https://github.com/agentic-cliniai/meddecision)
- **SafeGuard Toolkit** — 医疗AI安全框架 [`safeguard`](https://github.com/agentic-cliniai/safeguard)

## 知识与工具

| 项目 | 描述 | 仓库 |
|------|------|------|
| **Awesome Clinical Agents** | 临床Agent领域论文、数据集的系统性调研整理 | [`awesome-clinical-agents`](https://github.com/Agentic-CliniAI/Awesome-Clinical-Agents) |
| **Knowledge Base** | 结构化医学知识库：疾病-症状-治疗关系图谱与临床指南编码 | [`knowledge-base`](https://github.com/Agentic-CliniAI/KnowledgeBase) |
| **Clinical Toolkit** | 多模态诊疗工具集：影像/文本/时序数据的预处理与特征提取 | [`clinical-toolkit`](https://github.com/Agentic-CliniAI/Clinical-Toolkit) |
| **SafeGuard Toolkit** | 医疗AI安全框架：幻觉检测、不确定性量化、偏差校验与反馈机制 | [`safeguard-toolkit`](https://github.com/Agentic-CliniAI/Safeguard-Toolkit) |

---
