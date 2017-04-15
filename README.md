# Yaku Han JP

## Demo

- [Demo Page](https://qrac.github.io/yakuhanjp)

## About

"Yaku Han JP"は、Web上の日本語テキストに含まれる約物を半角にする「約物半角専用Webフォント」です。Googleの"Noto Sans CJK JP（源ノ角ゴシック）"と"Noto Serif CJK JP（源ノ明朝）"をベースにしており、ゴシック体と明朝体でそれぞれ7ウェイト対応できます。

## Detail

仕組みは、文字幅を調整した「約物だけのフォント」をデバイスフォントよりも前に優先的適応することです。font-family（CSS）のフォールバック機能を利用しています。旧ブラウザ対応に優れ、動的コンテンツへの利用に最適。1つのフォントが4〜5KBと軽量なので、表示速度やパフォーマンスを重視するサイトへの使用も安心です。

## Valuation

4種類のフォントを用意しています。ゴシック体と明朝体を使い分けられる他、カッコだけを半角にするSmall Amount（少量版）が使えます。

- YakuHanJP : ゴシック体 All Include（全部入り版）
- YakuHanJPs : ゴシック体 Small Amount（少量版）
- YakuHanMP : 明朝体 All Include（全部入り版）
- YakuHanMPs : 明朝体 Small Amount（少量版）

内包する文字はそれぞれ以下の通りです。

### All Include（全部入り版） : 約物すべて

> 、。！？〈〉《》「」『』【】〔〕・（）：；［］｛｝…

### Small Amount（少量版） : カッコのみ

> 〈〉《》「」『』【】〔〕（）［］｛｝…

ウェイトは7段階。付属のCSSでは以下のfont-weightで指定できます。※Noto Sans CJK JPとNoto Serif CJK JPでウエイト・ファイル名が若干異なるため、当ライブラリ内のファイル名もそれに準じています。

- font-weight: 100;
- font-weight: 200;
- font-weight: 300;
- font-weight: 400;
- font-weight: 500;
- font-weight: 700;
- font-weight: 900;

## How To Use

### CDN （ [jsDelivr](https://www.jsdelivr.com/projects/yakuhanjp) ）

```
// YakuHanJP
<link rel="stylesheet" href="https://cdn.jsdelivr.net/yakuhanjp/2.0.0/css/yakuhanjp.min.css">

// YakuHanJPs
<link rel="stylesheet" href="https://cdn.jsdelivr.net/yakuhanjp/2.0.0/css/yakuhanjp_s.min.css">

// YakuHanMP
<link rel="stylesheet" href="https://cdn.jsdelivr.net/yakuhanjp/2.0.0/css/yakuhanmp.min.css">

// YakuHanMPs
<link rel="stylesheet" href="https://cdn.jsdelivr.net/yakuhanjp/2.0.0/css/yakuhanmp_s.min.css">
```

### npm

```
npm install yakuhanjp
```

### Download

1. データを[ダウンロード](https://github.com/qrac/yakuhanjp/archive/master.zip)
2. distフォルダ内の「css」「fonts」を制作サイトに配置
3. headでCSSを読み込む
  - ゴシック体
    - 約物すべてを使う場合は「yakuhanjp.min.css」
    - カッコだけを使う場合は「yakuhanjp_s.min.css」
  - 明朝体
    - 約物すべてを使う場合は「yakuhanmp.min.css」
    - カッコだけを使う場合は「yakuhanmp_s.min.css」
4. CSSでフォントを適応
  - ゴシック体
    - 約物すべてを使う場合は「YakuHanJP」
    - カッコだけを使う場合は「YakuHanJPs」
  - 明朝体
    - 約物すべてを使う場合は「YakuHanMP」
    - カッコだけを使う場合は「YakuHanMPs」

```
// YakuHanJP
<link rel="stylesheet" href="dist/css/yakuhanjp.min.css">

// YakuHanJPs
<link rel="stylesheet" href="dist/css/yakuhanjp_s.min.css">

// YakuHanMP
<link rel="stylesheet" href="dist/css/yakuhanmp.min.css">

// YakuHanMPs
<link rel="stylesheet" href="dist/css/yakuhanmp_s.min.css">
```

```
// YakuHanJP
.yakuhanjp {
  font-family: YakuHanJP, "Hiragino Sans", "Yu Gothic", YuGothic, Meiryo, sans-serif;
}

// YakuHanJPs
.yakuhanjps {
  font-family: YakuHanJPs, "Hiragino Sans", "Yu Gothic", YuGothic, Meiryo, sans-serif;
}

// YakuHanMP
.yakuhanmp {
  font-family: YakuHanMP, "Hiragino Mincho ProN", "Yu Mincho", YuMincho, serif;
}

// YakuHanMPs
.yakuhanmps {
  font-family: YakuHanMPs, "Hiragino Mincho ProN", "Yu Mincho", YuMincho, serif;
}
```

## Support

| Chrome | Firefox | IE | Ege | Opera | Safari(Mac) |
|:------:|:------:|:------:|:------:|:------:|:------:|
| 5~ | 3.6~ | 6~ | 12~ | 11.5~ | 5.1~ |

| Safari(iOS) | Chrome(Android) | Browser(Android) |
|:------------:|:------------:|:------------:|
| 5.1~ | 56~ | 4.4~ |

## Media

- [HTML5 Conference 2016 LT "Yaku Han JP" by Qrac // Speaker Deck](https://speakerdeck.com/qrac/html5-conference-2016-lt-yaku-han-jp-by-qrac)

## License

- Yaku Han JP : SIL OFL 1.1
- Author : [Qrac](https://twitter.com/Qrac_JP)
- Gothic fonts : Based on ["Noto Sans CJK JP"](https://www.google.com/get/noto/#sans-jpan) licensed under the SIL OFL 1.1
- Mincho fonts : Based on ["Noto Serif CJK JP"](https://www.google.com/get/noto/#serif-jpan) licensed under the SIL OFL 1.1
