# jp-lab-report-latex-template

[![Build LaTeX document](https://github.com/satotomoya63m-alt/jp-lab-report-latex-template/actions/workflows/latex.yml/badge.svg)](https://github.com/satotomoya63m-alt/jp-lab-report-latex-template/actions/workflows/latex.yml)

A Japanese LaTeX template and snippet collection for science and engineering students writing laboratory reports.

理系大学生が日本語で実験レポートを書くための LaTeX テンプレートとコードスニペット集です。

## 概要

このリポジトリは、日本語で実験レポートを書く理系大学生向けに、再利用しやすい LaTeX テンプレートとスニペットを提供します。

図、表、数式、SI単位、参考文献、コード掲載など、実験レポートでよく使う要素をまとめています。

## 特徴

- 日本語の実験レポート向け LaTeX テンプレート
- 図・表・数式・SI単位・参考文献のサンプル
- Python などのコード掲載用スニペット
- Overleaf とローカル TeX 環境の両方で使いやすい構成
- 授業固有の解答や実験データを含まない汎用テンプレート

## 含まれないもの

このリポジトリには以下を含みません。

- 特定の授業・実験課題の解答
- 実験データ
- レポート本文の完成例
- 大学・教員・TAが配布した資料のコピー
- 個人情報

## PDFの確認

このリポジトリでは、GitHub Actionsによって `template/main.tex` のビルド確認を行っています。

Actionsの実行結果から、生成されたPDFをArtifactsとしてダウンロードできます。

1. リポジトリ上部の `Actions` タブを開く
2. 最新の `Build LaTeX document` を開く
3. `Artifacts` から `lab-report-template-pdf` をダウンロードする

## ドキュメント

- [Overleafで使う方法](docs/overleaf.md)
- [ローカル環境で使う方法](docs/local-setup.md)
- [トラブルシューティング](docs/troubleshooting.md)

## ディレクトリ構成

```text
jp-lab-report-latex-template/
├── README.md
├── README.en.md
├── LICENSE
├── CONTRIBUTING.md
├── template/
│   ├── main.tex
│   └── preamble.tex
├── snippets/
│   ├── figures.tex
│   ├── tables.tex
│   ├── equations.tex
│   └── si-units.tex
├── examples/
│   └── minimal/
│       └── main.tex
├── docs/
│   ├── overleaf.md
│   ├── local-setup.md
│   └── troubleshooting.md
└── .github/
    └── workflows/
        └── latex.yml
``
