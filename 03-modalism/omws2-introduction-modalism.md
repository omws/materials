---
title-meta: 様相主義 (イントロダクション)
from: markdown+yaml_metadata_block+citations
pdf-engine: lualatex
documentclass: bxjsarticle
classoption: 'pandoc,jafont=hiragino-pron'
papersize: a4
citeproc: true
csl: ./chicago-author-date.csl
references:
- type: book
  id: Forbes1989
  author:
    family: Forbes
    given: Graeme
  issued: 1989
  title: Languages of Possibility
  publisher: Basil Blackwell
- type: book
  id: Borghini2016
  author:
    family: Borghini
    given: Andrea
  issued: 2016
  title: A Critical Introduction to the Metaphysics of Modality
  publisher: Bloomsbury
  annote: '[第3章が様相主義に充てられている (おすすめ)]'
- type: chapter
  id: Sider2003
  author:
    family: Sider
    given: Theodore
  issued: 2021
  title: Reductive Theories of Modality
  container-title: The Oxford Handbook of Metaphysics
  editor:
    - Michael J. Loux
    - Dean W. Zimmerman
  page: 180-208
  publisher: Oxford University Press
- type: chapter
  id: Reinach1911
  author:
    family: Reinach
    given: Adolf
  issued: 1911
  title: Zur Theorie des negativen Urteils
  container-title: Gesammelte Schriften \textnormal{(1921)}
  publisher: Max Niemeyer
  language: de-DE
- type: chapter
  id: Fine1977
  author:
    family: Fine
    given: Kit
  issued: 1977
  title: Postscript
  container-title: Worlds, Times and Selves
  container-author: Arthur Prior
  publisher: Duckworth
  note: 'Reprinted in Kit Fine, \textit{Modality and Tense} (2005)'
- type: entry
  id: Shalkowski2020
  author:
    family: Shalkowski
    given: Scott A.
  issued: 2020
  title: Modalism
  container-title: The Routledge Handbook of Modality
  chapter-number: 10
  editor:
    - Otávio Bueno
    - Shalkowski, Scott A.
  publisher: Routledge
- type: entry
  id: Shalkowski2006
  author:
    family: Shalkowski
    given: Scott A.
  issued: 2006
  title: Modality, Philosophy and Metaphysics of
  container-title: Encyclopedia of Philosophy
  edition: 2
  volume: 9
  page: 280-289
  publisher: Thomson Gale
  annote: '[様相主義について積極的な立場から後半で紙幅が割かれている (おすすめ). 次のページでも閲覧可能: \url{https://www.encyclopedia.com/humanities/encyclopedias-almanacs-transcripts-and-maps/modality-philosophy-and-metaphysics}]'
- type: entry
  id: Textor2020
  author:
    family: Textor
    given: Mark
  issued: 2020
  title: States of Affairs
  container-title: The Stanford Encyclopedia of Philosophy
  edition: Summer 2020
  editor: Edward N. Zalta
  publisher: Metaphysics Research Lab, Stanford University
  URL: https://plato.stanford.edu/archives/sum2020/entries/states-of-affairs/
- type: article-journal
  id: 小関2021
  author:
    family: 小関
    given: 健太郎
  issued: 2021
  title: マイノングの事態論における可能性と存在
  container-title: 哲学の門
  volume: 3
  page: 44-55
  language: ja-JP
- type: article-journal
  id: Warmke2016
  author:
    family: Warmke
    given: Craig
  issued: 2016
  title: Modal Semantics without Worlds
  container-title: Philosophy Compass
  volume: 11
  page: 702-715
- type: article-journal
  id: Richard1994
  author:
    family: Richard
    given: Mark
  issued: 1994
  title: Review of Graeme Forbes, 'Languages of Possibility'
  container-title: The Philosophical Review
  volume: 1
  page: 139-142
- type: article-journal
  id: Wang2021
  author:
    family: Wang
    given: Jennifer
  issued: 2021
  title: The epistemological objection to modal primitivism
  container-title: Synthese
  volume: 198 (Suppl 8)
  page: S1887-S1898
nocite: '@*'
# https://github.com/jgm/pandoc/issues/7534
header-includes: |
  \makeatletter
  \newcommand{\origvadjust}{\ltj@@orig@vadjust}
  \newcommand{\citeemph}[1]{\textit{#1}}
  \makeatother
  \renewenvironment{CSLReferences}[2] % #1 hanging-ident, #2 entry spacing
  {% prevent redefinition by luatexja
  \renewcommand{\vadjust}{\origvadjust}
  \let\emph\citeemph
  % don't indent paragraphs
  \setlength{\parindent}{0pt}
  % turn on hanging indent if param 1 is 1
  \ifodd #1
  \let\oldpar\par
  \def\par{\hangindent=\cslhangindent\oldpar}
  \fi
  % set entry spacing
  \setlength{\parskip}{#2\cslentryspacingunit}
  }%
  {}
---

# 様相主義 (イントロダクション)

小関 健太郎 (慶應義塾大学)\
(初出) 2021-09-17 · 第2回 存在論・形而上学WS\
CC-BY-NC 4.0\
<https://github.com/omws/materials/tree/master/03-modalism>

## 様相主義の概要

### 様相的真理と可能世界理論

#### 可能世界理論における様相的真理の説明.

可能世界理論は可能性や必然性のような様相概念に，直観的な説得力があり，形式的にも有用な説明 (e.g., 様相論理の可能世界意味論 (Kripke 意味論)) を与える．
つまり，最も単純な形では次のようなものである:

- Aが可能的に真 ($\Diamond A$) $\Longleftrightarrow$ ある可能世界においてAが真
- Aが必然的に真 ($\Box A$) $\Longleftrightarrow$ すべての可能世界においてAが真

#### 問題提起.

可能世界理論が様相的真理を説明する唯一可能な理論なのか？

いくつかのモチベーションの候補:

- 可能世界の形而上学の問題 (様相実在論，代替主義，虚構主義，...) を避けることができる
- 可能世界理論よりも，あるいは可能世界理論とは別の形で，直観的な説得力があり，形式的にも有用な説明が得られる可能性がある
  - 少なくとも哲学史的には，可能世界による様相概念の説明が常に主流であったわけでも，全面的に受け入れられてきたわけでもない

## 様相主義とその周辺

#### 様相主義の整理.

様相概念に関するいくつかの主張として，さしあたり次のような主張を挙げることができる:

- (P1) 様相概念は非様相的な概念に還元可能である
- (P2) 様相概念は別の様相的な概念に還元可能である
- (P3) 様相概念は還元不可能である

可能世界理論は通常 (P1) を肯定する見解のひとつとみなされる [cf., e.g., @Sider2003]．
これに対して，(P1) を否定して (P3) を認める見解が様相主義 (modalism) と呼ばれる (本質に関する様相主義 (本質概念は様相概念によって説明されるという見方) は別の概念である)．
つまり，最も一般的な形では，様相的真理は何らかのXによって字義通り次のように説明される:

- Aが可能的に真 ($\Diamond A$) $\Longleftrightarrow$ Xが可能的
- Aが必然的に真 ($\Box A$) $\Longleftrightarrow$ Xが必然的

また，より不定的な意味で様相原始主義 (modal primitivism) という用語が用いられる場合もある．@Wang2021 は (P1) を否定する見解のうち，(P2) を認める見解を様相原始主義と呼んでいる．

実際のところ，(P1) -- (P3) の差は「様相的な概念」をどう理解するかにも依存する．
まず (P1) と (P2) については，Sider が (様相的命題に関して) 論じているように，様相概念を還元することができるような別の概念があるのであれば，そのような概念こそがまさに様相的な概念であると言うことも可能なのであり，Sider はむしろ還元の結果が認容可能 (acceptable) かどうかが問題であるとしている  [@Sider2003, p. 185]．
また，様相概念を別の様相概念に還元することを還元として認めるかどうかによって，(P2) と (P3) の差は曖昧である．

その上で，(P1) や (P2) を認める見解としては，様相概念についての本質による説明，傾向性 (disposition) や力能 (power, potentiality) といった特定のカテゴリーの性質による説明などが挙げられる [cf. @Borghini2016, §3; @Warmke2016]．

#### 可能世界理論から様相主義への翻訳.

様相主義はさらに，次の主張を含む見解である，あるいはそのようにみなされる場合がある:

- (WT) 可能世界への言及を含む言明は，様相主義の語彙のみを用いた言明に翻訳可能である

現代的な様相主義の嚆矢とみなされる @Fine1977 は (WT) の形式的な実現に焦点を当てている．
しかしながら，(WT) の手続きは自明なものではなく，(むしろ相当程度に複雑であり，) 完全に実現可能かどうかについては論争がある．
他方で，様相主義が同時に可能世界理論を全面的に認める理由はないという意味では，(WT) へのコミットメントは様相主義にとって必須のものではない [@Shalkowski2006]．

## 様相主義の形而上学

#### Forbesの理論.

- @Forbes1989 の理論は真正の意味での様相主義 (であるとともに，おそらく最初の体系的な様相主義の現代的擁護) の理論であり，様相そのものをそれ以上還元できない形而上学的に原始的な [=プリミティブな] ものとみなしている
- 原始的な様相の担い手として，Forbes は**事態** (states of affairs) を挙げている

#### 事態とは?

- ここでは事態を，それが**成り立ったり (obtain)，成り立たなかったりする**ものであるということによって大まかに特徴づける
  - (例) 事態の例として，〈東京タワーが赤色であること〉や〈土星が輪を持つこと〉を考えることができる (以下では〈...〉で事態を表す)．
    東京タワーや土星それ自体は事態ではないという点で区別される (東京タワーや土星が成り立ったり成り立たなかったりはしない)
- 事態は他にも様々な仕方で特徴づけられ，それぞれの間で共通性や差異がある (個別者と性質の複合，可能世界の部分，...)

## 可能的事態と存在

### 背景

#### Forbesの理論の課題.

- @Forbes1989 で素描されている理論には，否定的事態や可能的事態に関しての問題がある [@小関2021; cf. @Richard1994, 140f.]

#### 可能的成立の問題.

Forbes の理論は (原子命題に関して) 次の主張を受け入れているように思われる:

- (1) 命題Aが真 iff 事態〈Aということ〉が成り立っている iff 〈Aということ〉が存在する
- (2) 命題Aが偽 iff 〈Aということ〉が否定的に成り立っている iff 〈Aということ〉が存在しない

Forbes の理論によれば，事態が可能性の担い手であるということは，事態が「可能的な」成立の様態 (mode of obtaining) で成立しているということになる [@Forbes1989, 139]. したがって少なくとも次のように言うことができる:

- (3) 命題Aが可能的に真 iff 〈Aということ〉が可能的に成り立っている

しかしながらここで，(3) において〈Aということ〉の存在のあり方がどのようなものかが問題になる

- もし事態が存在しないなら，何によって (可能性あるいは可能的成立という) 否定的成立以上のことがもたらされているのか明らかではない
- もし事態が存在するなら，少なくとも (2) は満たさないので偽であることはできず，(1) から，ある命題が可能的に真であることが単に真であることを伴うことになる
- それ以外であるなら，それ以外の説明が必要になる

### 可能的事態の存在論

#### 理論的系譜.

- Forbes は上記の見解に関してライナッハの議論を参照しており，ライナッハの議論はマイノングとフッサールのそれぞれの議論に基づいている [@Reinach1911; cf. @Textor2020, §2.2]
- Forbes の理論の問題点は，フッサール-ライナッハやマイノングの形而上学的枠組みではさしあたり回避されている [@小関2021]

#### ライナッハの理論.

 ライナッハの理論では，存在する事態がそれ自体に肯定性や否定性のような規定性を持ち，可能性についても同様であると考えられる

- (1$'$) 命題Aが真 iff 事態〈Aということ〉が肯定性を持ち存在する
- (2$'$) 命題Aが偽 iff 事態〈Aということ〉が否定性を持ち存在する
- (3$'$) 命題Aが可能的に真 iff 事態〈Aということ〉が肯定的な可能性を持ち存在する

#### マイノングの理論.

マイノングの理論では，可能的成立に対応する可能的存在として「存在未確定性」が位置づけられる (さらに，冗長かどうかという点を措けば，ライナッハの理論と同様の説明も実質的に認めている)

- (1$''$) 命題Aが真 iff 事態〈Aということ〉が存在対象である
- (2$''$) 命題Aが偽 iff 事態〈Aということ〉が非存在対象である
- (3$''$) 命題Aが可能的に真 iff 事態〈Aということ〉が存在未確定 (seinsunbestimmt) な対象である

## 文献表
