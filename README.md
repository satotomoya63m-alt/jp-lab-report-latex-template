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

## 開発状況

このプロジェクトは初期公開版です。

現在は以下に対応しています。

- 日本語実験レポート用の基本テンプレート
- 図・表・数式・SI単位のスニペット
- Overleafでの利用ガイド
- GitHub ActionsによるLaTeXビルド確認

## ディレクトリ構成

```text
jp-lab-report-latex-template/
├── template/
│   ├── main.tex
│   ├── preamble.tex
│   ├── references.bib
│   └── sections/
├── snippets/
│   ├── figures.tex
│   ├── tables.tex
│   ├── equations.tex
│   ├── si-units.tex
│   ├── uncertainty.tex
│   └── code-listing.tex
├── examples/
│   └── minimal/
├── docs/
│   ├── overleaf.md
│   └── local-setup.md
└── README.md
