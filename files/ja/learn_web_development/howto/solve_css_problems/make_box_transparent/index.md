---
title: ボックスを半透明にするには
slug: Learn_web_development/Howto/Solve_CSS_problems/Make_box_transparent
original_slug: Learn/CSS/Howto/Make_box_transparent
l10n:
  sourceCommit: 289d6314f3368aa3e28524e7d090f6e9c704e3b1
---

{{LearnSidebar}}

このガイドでは、CSS を使用してボックスを半透明にする方法についてお手伝いします。

## ボックスとコンテンツの不透明度の変更

ボックスとそのボックスのすべてのコンテンツの不透明度を変更したい場合は、CSS の {{cssxref("opacity")}} プロパティを使用します。不透明度 (opacity) は透明度 (transparency) の逆です。したがって、`opacity: 1` は完全に不透明であり、ボックスはまったく透けて見えません。

`0` の値を使用すると、ボックスは完全に透明になり、2 つの値の間では不透明度が変化し、高い値になるほど透明度が低くなります。

## 背景色の不透明度のみを変更する場合

多くの場合、背景色を部分的に透過させるだけで、テキストや他の要素は完全に不透明なままにしておきたいでしょう。これを実現するには、 `rgb()` のようなアルファチャンネルを持つ [`<color>`](/ja/docs/Web/CSS/color_value) の値を使用してください。`opacity` と同様に、アルファチャンネルの値を `1` にすると、その色は完全に不透明になります。したがって、`background-color: rgb(0 0 0 / 50%);` は、背景色を 50% の不透明度に設定します。

下記の例で、不透明度とアルファチャンネルの値を変えてみて、ボックスの後ろの背景画像が見える割合を上下させてみてください。

{{EmbedGHLiveSample("css-examples/howto/opacity.html", '100%', 770)}}

> [!NOTE]
> 画像を重ねる場合は、テキストと背景のコントラストが十分に保たれるように注意してください。そうしないと、コンテンツが読みづらくなる可能性があります。

## 関連情報

- [CSS を使った HTML の要素への色の適用](/ja/docs/Web/CSS/CSS_colors/Applying_color)
