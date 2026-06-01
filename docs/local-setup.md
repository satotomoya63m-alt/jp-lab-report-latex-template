# ローカル環境で使う方法

このページでは、`jp-lab-report-latex-template` を自分のPC上で使う方法を説明します。

## 前提

このテンプレートは、主に以下の環境を想定しています。

- LuaLaTeX
- latexmk
- TeX Live
- 日本語LaTeX環境

## リポジトリを取得する

```bash
git clone https://github.com/satotomoya63m-alt/jp-lab-report-latex-template.git
cd jp-lab-report-latex-template
```

## テンプレートをビルドする

```bash
cd template
latexmk -lualatex main.tex
```

ビルドに成功すると、`main.pdf` が生成されます。

## 生成ファイルを削除する

LaTeXの一時ファイルを削除したい場合は、以下を実行します。

```bash
latexmk -c
```

PDFを含めて削除したい場合は、以下を実行します。

```bash
latexmk -C
```

## VS Codeで使う場合

VS CodeでLaTeXを書く場合は、以下の拡張機能が便利です。

- LaTeX Workshop

設定例は環境によって異なるため、まずはターミナルから `latexmk -lualatex main.tex` が通ることを確認してください。

## 注意

このテンプレートは、特定の授業・実験課題の解答例ではありません。

授業で利用する場合は、所属する大学・授業・教員のルールに従ってください。
