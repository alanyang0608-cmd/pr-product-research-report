# pr-product-research-report

An evidence-based Agent Skill for product capability research, communications strategy analysis, and combined research reports.

一个面向业务读者的产品与传播调研 Skill。先讲清产品是什么，再用可追溯材料分析能力、场景、传播节奏和用户反馈。

## 三种研究模式

| 模式 | 适合的问题 | 主要交付 |
| --- | --- | --- |
| 产品能力调研 | 产品是什么、怎么用、能做多深、与竞品有何区别 | 定义、界面与操作、反馈、限制及比较 |
| 传播策略研究 | 最近如何传播、各平台在说什么、哪些内容值得借鉴 | 公开内容证据库、节奏与叙事、平台分析和高互动链接 |
| 综合调研 | 产品价值如何变成传播表达 | 结合能力与传播的完整分析 |

需求明确时直接进入对应模式；方向不明确时，先提供三种选项。只问局部问题时保持简洁，不强制输出完整长报告。

## 安装

将本仓库放入支持 Agent Skills 的客户端所使用的技能目录，目录名保持 `pr-product-research-report`。技能目录内应直接包含 `SKILL.md`、`agents/` 和 `references/`。

Codex 的默认目录可使用以下命令安装；目标目录已经存在时，先查看并备份自己的修改，不覆盖旧目录：

```sh
git clone https://github.com/alanyang0608-cmd/pr-product-research-report.git "${CODEX_HOME:-$HOME/.codex}/skills/pr-product-research-report"
```

也可以在 [Releases](https://github.com/alanyang0608-cmd/pr-product-research-report/releases) 下载版本对应的 Source code (zip)，解压后将顶层目录重命名为 `pr-product-research-report`，放入客户端的技能目录，并重新打开会话。

如果已安装本技能的旧标识版本，请先将旧目录移出客户端扫描的技能目录，再安装新版，避免同时加载两个副本。其他客户端的安装位置按其文档配置。

## 使用示例

以下产品名称均为占位示例，使用时替换成实际研究对象与范围。

```text
请使用 $pr-product-research-report，调研产品 A 和产品 B 的能力。
先让我知道它们是什么、怎么用，再结合真实界面、用户反馈和来源比较差异。
```

```text
请使用 $pr-product-research-report，研究产品 A 最近三个月的公开传播。
分析传播节奏、叙事、主要平台和高互动内容，交付 Markdown 报告与单文件 HTML 看板。
```

```text
请使用 $pr-product-research-report，综合分析产品 A 的实际价值与传播方法，
说明哪些结论有证据、哪些仍需验证。
```

支持文字、Markdown 和 HTML。用户指定 React + Recharts 或离线单文件时，按要求制作；未指定技术栈时选择适合任务的实现。

## 方法与边界

- 区分官方事实、宣传演示、使用反馈与研究判断。
- 传播分析分别记录刊发日、事件日、采集日和指标口径。
- 热门内容按同平台、同指标比较；公开样本不冒充全网普查。
- 标明未读原文、访问受限和未公开指标，不补造数据或评价。
- 报告、图表和证据详情使用同一数据源，并实际检查关键交互。

本仓库只包含通用研究方法和虚构示例，不包含真实项目报告、业务材料、原始素材、私有数据或账号凭据。执行研究时仍需由使用者提供可用且已授权的检索、浏览器或平台工具；本技能不提供访问授权，也不保证能获取所有平台数据。

## 文件结构

```text
SKILL.md                              入口与模式选择
agents/openai.yaml                    客户端展示信息
references/report-structure.md        产品报告结构
references/evidence-and-experience.md  界面、反馈与证据
references/html-delivery.md            HTML 呈现与检查
references/communications-research.md  传播采集与深度分析
references/communications-dashboard.md 传播看板
```

## 许可证

[MIT](LICENSE)。仓库许可证适用于本仓库的技能文本，不授予任何第三方网页、图片、视频或用户数据的使用权。
