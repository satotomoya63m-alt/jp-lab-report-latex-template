# VS Codeで使う方法

このページでは、`jp-lab-report-latex-template` を Visual Studio Code（VS Code）で編集・コンパイルする方法を説明します。

## 前提

VS CodeはLaTeXを書くためのエディタです。

VS CodeだけではLaTeX文書をPDFに変換できないため、別途LaTeX環境が必要です。

主に以下の環境を想定しています。

- VS Code
- LaTeX Workshop
- TeX Live
- LuaLaTeX
- latexmk
- Git

## 1. 必要なもの

### VS Code

VS Codeをインストールします。

### LaTeX環境

PCにTeX LiveなどのLaTeX環境をインストールします。

このテンプレートでは、主にLuaLaTeXを想定しています。

### VS Code拡張機能

VS Codeで以下の拡張機能をインストールします。

- LaTeX Workshop

## 2. リポジトリを取得する

Gitが使える場合は、ターミナルで以下を実行します。

```bash
git clone https://github.com/satotomoya63m-alt/jp-lab-report-latex-template.git
cd jp-lab-report-latex-template
```

Gitを使わない場合は、GitHubの `Code` → `Download ZIP` からダウンロードして展開してください。

## 3. VS Codeでフォルダを開く

VS Codeを起動し、以下のフォルダを開きます。

```text
jp-lab-report-latex-template
```

VS Codeでは、ファイル単体ではなく、リポジトリ全体のフォルダを開くことをおすすめします。

## 4. テンプレートを編集する

主に編集するファイルは以下です。

```text
template/main.tex
```

LaTeXの共通設定は以下に分離しています。

```text
template/preamble.tex
```

通常は `main.tex` を編集すれば十分です。

パッケージや表示設定を変更したい場合のみ、`preamble.tex` を編集してください。

## 5. ターミナルからコンパイルする

VS Codeのターミナルを開き、以下を実行します。

```bash
cd template
latexmk -lualatex main.tex
```

ビルドに成功すると、以下のPDFが生成されます。

```text
template/main.pdf
```

## 6. LaTeX Workshopでコンパイルする

LaTeX Workshopを使うと、VS Code上からLaTeXをコンパイルできます。

基本的には、`template/main.tex` を開いた状態でコンパイルを実行します。

うまく動かない場合は、まずターミナルから以下が通るか確認してください。

```bash
latexmk -lualatex main.tex
```

ターミナルでコンパイルできない場合、VS Code側ではなくLaTeX環境の設定に問題がある可能性があります。

## 7. よくある問題

### `latexmk` が見つからない

LaTeX環境が正しくインストールされていない、またはPATHが通っていない可能性があります。

### 日本語が表示されない

pdfLaTeXではなく、LuaLaTeXを使ってください。

このテンプレートはLuaLaTeXを想定しています。

### `ltjsarticle.cls not found` と表示される

LuaLaTeX用の日本語クラスが見つかっていない可能性があります。

TeX Liveの日本語関連パッケージがインストールされているか確認してください。

### 画像が表示されない

画像ファイルのパスを確認してください。

例：

```latex
\includegraphics[width=0.75\linewidth]{figures/example.png}
```

この場合、`figures/example.png` が存在している必要があります。

## 8. 環境構築が難しい場合

LaTeX環境の構築が難しい場合は、Overleafの利用をおすすめします。

Overleafでの使い方は以下を参照してください。

```text
docs/overleaf.md
```

## 注意

このテンプレートは、特定の授業・実験課題の解答例ではありません。

授業で利用する場合は、所属する大学・授業・教員のルールに従ってください。
