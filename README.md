# graduation-proposal-rewriter

本科毕业设计开题报告改写 Skill（WorkBuddy）。

基于学校提供的开题报告 Word 模板（含范文）和参考文献，把范文改写为指定新题目的开题报告；在原 Word 文件副本上定点修改，严格保留模板全部格式，章节结构与字数贴近范文，引用规范且不编造文献，无关图表改为文字占位符，完成后直接交付可编辑的 Word 文件。

## 安装

把本仓库目录复制为 WorkBuddy 用户级 Skill 目录：

```
~/.workbuddy/skills/graduation-proposal-rewriter/
```

即确保该目录下有 `SKILL.md` 和 `references/` 两个条目。重启 WorkBuddy 会话后 Skill 即可被自动识别。

## 文件结构

```
graduation-proposal-rewriter/
├── SKILL.md                                   # Skill 元信息与 7 步工作流
└── references/
    └── requirements-and-checklist.md          # 原始要求逐字稿 + 10 条验收清单
```

## 用法

新开一个会话，提供以下材料：

1. 学校开题报告 Word 模板（含范文）
2. 参考文献
3. 新毕业设计题目

然后说“按学校模板写开题报告”即可触发。

## 关键约束

- 必须在原 Word 文件副本上修改，不能重新创建文档
- 字体、字号、行距、缩进、页边距、表格、边框、页眉页脚、学校 Logo、封面及整体排版全部保留
- 章节结构、写作风格、段落层次、大致字数与范文一致，不做关键词替换
- 国内外研究现状结合所给文献撰写，正确标注引用编号，不编造文献或成果
- 无关图片和功能图改为文字占位符，保留原位置与图题格式
- 无格式错乱、异常空白、表格变形，篇幅尽量与范文接近
- 不反复询问，直接交付可下载、可编辑的 Word 文件

## 依赖

执行时经 `workbuddy-office-routing` 路由，主编辑通道为 `workbuddy-local-office-edit`；长段正文起草可借助 `workbuddy-docx`，但产物必须写回模板副本。
