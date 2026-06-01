# トラブルシューティング

このページでは、日本語LaTeX実験レポートを書くときによくある問題と対処法をまとめます。

## 日本語が表示されない

### 原因

pdfLaTeXでコンパイルしている可能性があります。

### 対処

LuaLaTeXまたはupLaTeXを使ってください。

Overleafの場合は、`Menu` から Compiler を `LuaLaTeX` に変更します。

ローカル環境の場合は、以下を実行します。

```bash
latexmk -lualatex main.tex
```

## `ltjsarticle.cls not found` と表示される

### 原因

LuaLaTeX用の日本語クラスがインストールされていない可能性があります。

### 対処

TeX Liveを利用している場合は、TeX Liveの日本語関連パッケージが入っているか確認してください。

Overleafでは通常利用できますが、CompilerがLuaLaTeXになっているか確認してください。

## 図が表示されない

### 原因

画像ファイルのパスが間違っている可能性があります。

例えば、次のように書いた場合：

```latex
\includegraphics[width=0.75\linewidth]{figures/example.png}
```

`figures/example.png` が存在している必要があります。

### 対処

- ファイル名を確認する
- 拡張子を確認する
- 空白や日本語を含むファイル名を避ける
- `figures/` フォルダ内に画像を置く

## `siunitx` でエラーが出る

### 原因

`siunitx` パッケージが読み込まれていない、または記法が間違っている可能性があります。

### 対処

プリアンブルに以下があるか確認してください。

```latex
\usepackage{siunitx}
```

使用例：

```latex
\SI{9.81}{\meter\per\second\squared}
```

## 参考文献が表示されない

### 原因

BibTeXやbiberの実行が必要な場合があります。

### 対処

まずはテンプレート内の `thebibliography` 環境を使うと簡単です。

```latex
\begin{thebibliography}{9}
  \bibitem{example}
  著者名，『書籍名』，出版社，出版年．
\end{thebibliography}
```

## GitHub Actionsでビルドが失敗する

### 確認すること

- `template/main.tex` が存在しているか
- LaTeXの文法エラーがないか
- 必要なパッケージが読み込まれているか
- 画像ファイルのパスが正しいか

Actionsのログを開くと、エラーの原因が表示されます。

## 授業レポートに使ってよいか

このテンプレートは、汎用的な文書作成を補助するためのものです。

実際の授業レポートに利用する場合は、所属する大学・授業・教員のルールに従ってください。
