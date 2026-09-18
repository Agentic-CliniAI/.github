# Agentic-CliniAI

> 致力于创建安全、透明、可溯源的AI诊疗工具，辅助医疗专业人员提升诊疗效率与准确性。

[![Website](https://img.shields.io/badge/website-agentic--cliniai.github.io-blue)](https://agentic-cliniai.github.io)

* **Clinical Agentic Engine** - 主诊智能体代理系统

* **Evidence Tracking Agentic Engine** - 循证医学决策支持代理系统

* **SafeGuard Toolkit**- 医疗AI安全框架：幻觉检测、不确定性量化、偏差校验与反馈机制

## 📚 知识与工具

| 项目                          | 描述                                    | 仓库                                                                                                                           |
| --------------------------- | ------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------- |
| **Awesome Clinical Agents** | 临床Agent领域论文、数据集的系统性调研整理               | [`awesome-clinical-agents`](https://github.com/Agentic-CliniAI/Awesome-Clinical-Agents)                                      |
| **Derm Knowledge Base**     | 医学知识库（源自DeepRare）：疾病-症状-治疗关系图谱与临床指南编码 | [`knowledge-base`](https://github.com/Agentic-CliniAI/KnowledgeBase)                                                         |
| **MedTextbooks**            | 医学教材                                  | [`人卫第十版`](https://www.douban.com/note/873222443/?_i=7982968PUBNBNr) [`其他`](https://github.com/Agentic-CliniAI/medical-books) |
| **Clinical Toolkit**        | 多模态诊疗工具集：影像/文本/时序数据的预处理与特征提取          | [`clinical-toolkit`](https://github.com/Agentic-CliniAI/Clinical-Toolkit)                                                    |
| **SafeGuard Toolkit**       | 医疗AI安全框架：幻觉检测、不确定性量化、偏差校验与反馈机制        | [`safeguard-toolkit`](https://github.com/Agentic-CliniAI/Safeguard-Toolkit)                                                  |

## 🧩 核心项目分组

 🔍 **跨模态对齐** — 医疗模型视觉-语言跨模态对齐 
* [`Mobuis`](https://github.com/agentic-cliniai/mobius) ： 对齐SAM 的视觉理解能力与 LVLM 的语义推理能力。

🔍 **LVLM幻觉检测** — 检测 LVLM 的临床幻觉
* [EMNLP 2026 Main] [`MedF2Route`](https://github.com/Agentic-CliniAI/MedF2Route): 将黑盒幻觉检测任务定义成证据路由问题，再结合临床推理文本特点进行语义图谱构建、划分、证据路由、幻觉检测。
* [MICCAI 2026] [`CounterVHD`](https://github.com/Agentic-CliniAI/Counterfactual-Hallucination-Detect): 基于反事实视觉定位不确定性，检测 LVLM 的临床幻觉
* [`MedFH`](https://github.com/Agentic-CliniAI/MedFH): 将临床推理文本拆分成语义树，再根据其逻辑关系构建逻辑线索树，重点检测生成内容的忠实性问题。再根据语言的自回归和错误传播特性，校准首个幻觉发生节点并重新生成后续文本。


🔍 **Agent研究** 
* [应用开发赛][`silicon-power`](https://www.modelscope.cn/events/254/%E7%A1%85%E5%9F%BA%E8%B5%9B%E9%81%93%EF%BC%88%E6%99%BA%E8%83%BD%E4%BD%93%E8%B5%9B%E9%81%93%EF%BC%89%E5%A4%8D%E8%B5%9B%E6%99%8B%E7%BA%A7%E7%BB%93%E6%9E%9C%E5%85%AC%E7%A4%BA): 面向问诊、诊断、检查、治疗、token消耗的综合性虚拟医生Agent竞赛（初赛第二名）。

🔍 **知识图谱与因果推理** 
* [ACM BCB 2024]  [`Rethinking RRG`](https://dl.acm.org/doi/abs/10.1145/3698587.3701353): 重新思考被广泛应用的疾病共线关系在放射科报告生成任务中的因果效应，发现其混杂性。
***

