# 符号

## i.e. e.g.
英文排版时 TeX 通常默认句号 . 表示一句话的结束，因此在处理句号时会留出稍宽一点的水平间距。但是有些情况下，句号并不代表句子的结尾，比如「i.e. a word」和「e.g. a word」。按照 TeX 默认规则，这里的宽度会比正常句中单词之间的间隔稍大一些，因此我们需要使用 \ （即一个反斜杠 + 一个空格）来消除这个过大的间距：i.e.\ a word 以及 e.g.\ a word。

然而还有一种特殊情况下，TeX 并不会认为句号表示句子的结尾，那就是句号跟在一个大写字母的后面。此时 TeX 会认为这个句号表示人名缩写的间隔符，因此仍然按照正常间距来排版，比如 「A. Einstein」。然而这个看似贴心的规则在一些情况下会适得其反，比如一句话明明以缩略语结尾，TeX 反而认为这并不是一句话的结尾：「…… in NBA. He…」。此时，排版出的「He」之前的空格会小于正常的句间间距。这种情况下，需要使用 \@. （反斜杠 + @ + 句号 + 空格）来取代原先的句号，即 ... in NBA\@. He...。\@ 用来强制告诉 TeX 这里的的确确是一个句子的结尾。

* i.e. 可以与 in essence, namely 一起记

### 参考
[• 正确处理单词间距](https://ridiqulous.com/latex-notes-details/)
[Correct way to define macros \etc \ie in latex](https://stackoverflow.com/questions/3282319/correct-way-to-define-macros-etc-ie-in-latex)
[论文常用词汇i.e.，e.g.，etc.，viz.，et al.的前世今生
](https://zhuanlan.zhihu.com/p/63640148)
