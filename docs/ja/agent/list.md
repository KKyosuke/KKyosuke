# AIエージェント 手順書一覧

このディレクトリ（`docs/ja/agent/`）は、AIエージェント（GitHub Copilotなど）に対する手順書（プロンプト）と出力テンプレートを管理しています。

## 1. 手順書 (`instruction/`)

- [**`instruction/pull-request.md`**](./instruction/pull-request.md)
  - **用途**: Pull RequestのコードレビューをAIに自動実行させるためのプロンプトです。
  - **概要**: `docs/ja/code/pull-request.md` に記載されたPR作成方針を観点とし、適切に実装・ドキュメント作成が行われているかを診断・レビューします。

## 2. テンプレート (`template/`)

- [**`template/pull-request.md`**](./template/pull-request.md)
  - **用途**: 上記のPRレビュー結果を出力する際のフォーマットです。
  - **概要**: 総合得点、全体サマリ、及び具体的な指摘点一覧（テーブル形式：指摘理由 / 対応度 / 概要）を含みます。
