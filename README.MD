# 河北工程大学大学英语(4)课本题目合订本

本项目是《大学英语(4)》课本题目的 LaTeX 汇编文档，整理了 1-6 单元的 Listening、Banked Cloze 和 Translation 部分，并已生成可直接阅读的 PDF 文件。

> 公益整理项目，仅供学习交流使用，请勿用于商业售卖。

## 项目内容

- `main.tex`：主 LaTeX 文件，负责组织封面、目录和各章节内容。
- `config.sty`：统一的版式、字体、题目框、选项列表、超链接等样式配置。
- `chapter/`：正文内容目录。
  - `index.tex`：封面、说明页和目录。
  - `listening.tex`：Listening 题目与答案。
  - `bankedcloze.tex`：Banked Cloze 题目与答案。
  - `translation.tex`：Translation 题目与参考译文。
- `figure/`：封面及文档中使用的图片资源。
- `refpdf/`：按单元整理的参考文本。
- `main.pdf`：由 LaTeX 源码编译生成的 PDF。
- `河北工程大学-大学英语(4)-课本题目合订本.pdf`：便于分发和阅读的成品 PDF。
- `clean.bat`：Windows 下清理 LaTeX 编译中间文件的脚本。

## 环境要求

建议使用支持中文排版的 LaTeX 发行版，例如：

- TeX Live
- MiKTeX

由于项目使用 `ctexart` 文档类，推荐使用 `XeLaTeX` 编译。

## 编译方式

在项目根目录执行：

```powershell
xelatex main.tex
```

如果目录、书签或交叉引用没有完全更新，可以连续编译两次：

```powershell
xelatex main.tex
xelatex main.tex
```

编译完成后会生成或更新 `main.pdf`。

## 清理中间文件

Windows 用户可以运行：

```powershell
.\clean.bat
```

该脚本会删除 `.aux`、`.log`、`.toc`、`.out`、`.synctex.gz` 等 LaTeX 编译中间文件。

## 维护说明

- 修改题目内容时，优先编辑 `chapter/` 目录下对应的 `.tex` 文件。
- 修改整体版式、题目框、选项列表、行距、页边距等样式时，编辑 `config.sty`。
- 新增图片请放入 `figure/` 目录，并在 LaTeX 中使用相对路径引用。
- 若调整章节结构，请同步检查 `main.tex` 中的 `\input{...}` 顺序。

## 开源地址

项目仓库：

```text
https://github.com/nsyhfxc/gongwai4.git
```

如需同步后续更新，可使用：

```powershell
git pull
```

## 免责声明

本项目内容来源于课程学习整理，仅用于个人复习、学习交流和资料备份。若内容存在错误或需要更新，欢迎通过仓库提交 Issue 或 Pull Request。
