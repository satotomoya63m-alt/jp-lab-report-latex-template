# ローカル環境で使う方法

このページでは、`jp-lab-report-latex-template` を自分のPC上で使う方法を説明します。

## 前提

この方法では、PCにLaTeX環境を用意して、ターミナルからPDFを生成します。

主に以下の環境を想定しています。

- LuaLaTeX
- latexmk
- TeX Live
- 日本語LaTeX環境
- Git

## ターミナルについて

このページに出てくるコマンドは、PCのターミナルで実行します。

使用するアプリの例：

- macOS: ターミナル
- Windows: PowerShell または コマンドプロンプト
- Linux: Terminal

## リポジトリを取得する

Gitが使える場合は、以下をターミナルで実行します。

```bash
git clone https://github.com/satotomoya63m-alt/jp-lab-report-latex-template.git
cd jp-lab-report-latex-template
```

`git clone` は、GitHub上のリポジトリを自分のPCにコピーするためのコマンドです。

Gitを使わない場合は、GitHubのリポジトリページから `Code` → `Download ZIP` を選び、ZIPファイルをダウンロードして展開してください。

## テンプレートをビルドする

以下をターミナルで実行します。

```bash
cd template
latexmk -lualatex main.tex
```

ビルドに成功すると、`template` フォルダ内に `main.pdf` が生成されます。

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

まずはターミナルから以下のコマンドが通ることを確認してください。

```bash
latexmk -lualatex main.tex
```

## 環境構築が難しい場合

PCにLaTeX環境を入れるのが難しい場合は、Overleafの利用をおすすめします。

Overleafを使う場合は、以下を参照してください。

```text
docs/overleaf.md
```

## 注意

このテンプレートは、特定の授業・実験課題の解答例ではありません。

授業で利用する場合は、所属する大学・授業・教員のルールに従ってください。
