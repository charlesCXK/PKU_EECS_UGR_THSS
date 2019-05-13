# LaTeX Template for Undergraduate Thesis at School of EECS, Peking University

The initial author of the repository is Bochen Tan. [SceneryInMirror](https://github.com/SceneryInMirror/) has made invaluable contributions.

I made this Latex template as 'green' as possible, meaning that it does not depend on other things than Latex.

There are mainly two branches: 'master' which follows the .doc file quite rigidly and depend on ctex package 'non-ctex' which is free from ctex. 'non-ctex' contains some variations from the .doc file, but definitely no direct violations. (There are some details that is not explicitly regulated in the .doc file, so we can make up our own minds.)

Beware to change the font names (songti, heiti, kaiti, and Times New Roman) according to your operating system. The font names in 'non-ctex' is tailored to my Mac OS.

## 'overleaf' branch is for overleaf building

To use the template in Overleaf, just download all the files in this branch and upload it to Overleaf. Set the main tex file to template.tex and it should be ready to compile. This branch still bases on ctex. Only font names are changed comparing to master branch.

An older but stable version has been made available on Overleaf. Please search for [PKU EECS UGR THSS ctex](https://www.overleaf.com/latex/templates/pku-eecs-ugr-thss-ctex/mzhftgdsbgnw).

## 'cover' has been merged to 'master'

The project's author is TBC. Based on TBC's code, SceneryInMirror added the cover and reviewtable in branch 'cover'.

There are five .tex files:

* Template.tex
* Cover.tex
* ReviewTable.tex
* CoverHead.tex
* ReviewTableHead.tex

'Template.tex' is the main body of the project. You can write your thesis here.

'Cover.tex' designs the cover of this template.

'ReviewTable.tex' designs the reviewtable of this template.

'CoverHead.tex' and 'ReviewTableHead.tex' are head files for cover and reviewtable. They contain all packages needed for these two parts. **please change the name of kaiti to the name of kaiti in your operating system**

**There is no need to edit the last four .tex files. Everything you want to write is in 'Template.tex', including the words in the cover.**

'Template.pdf' is the output of this project.

## 

## 原版本基础上的修改

1. ##### 按照教务word模板更换了“版权声明”的字体。（黑体 -> 宋体）

2. ##### 增加了文件夹结构，只需修改 `chap/` 文件夹下的文件以及在 `Template.tex` 中对应的 `include` 语句即可加入新的章节

3. ##### 增加了封面word版。由于现在的模板存在这样一个问题：标题过长的话会出现格式错误。所以有这种情况的话，建议在word文件中写好封面，然后打印成PDF，放到模板生成的PDF的第一页，构成完整的毕业论文。
4. ##### 关于图片编号问题
默认图片编号是 `图1`，`图2` 之类。若想实现类似于 `图 1.1` 这样章节号+章节内图片号的编号，只需在每一章节最前面加入如下几行命令
```
\renewcommand {\thetable} {\thechapter{}.\arabic{table}}
\renewcommand {\thefigure} {\thechapter{}.\arabic{figure}}
\setcounter{table}{0}
\setcounter{figure}{0}
```
5. ##### subfigure 导入失败
如果在导入 subfigure 时遇到 `LaTeX Error: Command \c@lofdepth already defined.`，请这样导入：
```
\usepackage{subfigure}
\usepackage[subfigure]{tocloft}
```
## Tip
需要选择 `XeLaTex` 作为编译语言，因为模板中引入了 `ctex` 中文包。
