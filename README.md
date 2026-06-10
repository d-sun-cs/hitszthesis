# 哈尔滨工业大学（深圳）硕士学位论文中期报告（midterm 分支）

本分支为**硕士学位论文中期报告**模板，整合自 [ruicx/HITSZ-Mid-Term-LaTex-Template](https://github.com/ruicx/HITSZ-Mid-Term-LaTex-Template)（由 [hithesis v3](https://github.com/dustincys/hithesis) 改进），使用 `hithesisart` 文档类。

> 注意：开题报告位于本仓库 `proposal` 分支，使用的是 `hitszthesis` 文档类，与中期报告的文档类不同。两者共享了选题信息（封面、`reference.bib`、`figures/`）。

## 目录结构

```text
.
├── report.tex                 # 主文件（已设为 type=master, stage=midterm, campus=shenzhen）
├── hithesisart.cls            # 文档类（核心，需纳入版本管理）
├── hithesisart.cfg            # 配置（核心）
├── hithesis.bst              # 参考文献样式（核心）
├── latexmkrc                  # latexmk 编译配置，输出到 build/
├── front/coverart.tex         # 封面信息（已填入本人选题信息）
├── body/report_midterm.tex    # 中期报告正文
├── figures/                   # 插图（含 hitlogo.eps，来自 proposal 分支）
└── reference.bib              # 参考文献（来自 proposal 分支）
```

## 编译方法

编译前需建立与 `.tex` 目录对应的 `build/` 子目录：

```bash
mkdir -p build/front build/body
latexmk report.tex
```

输出 PDF 位于 `build/report.pdf`。

- Linux / CI 环境请使用 `fontset=fandol`（开源字体，已默认）。
- Windows/Mac 本地有方正/系统字体时，可在 `report.tex` 中改为 `fontset=windows|mac`。
