# premiere-cut-template

Premiere Pro XML 無音カットワークフローの **セットアップウィザード** テンプレートです。

## 使い方

このリポジトリの URL を Claude Code に渡すと、セットアップウィザードが起動します。
11項目の質問に答えるだけで、自分の環境に合わせた `/cut` スキルとフォルダ構成が自動生成されます。

## 生成されるもの

- `~/.claude/commands/<コマンド名>.md` — Claude Code スキルファイル
- プロジェクトの `CLAUDE.md` — 設定値の記録
- `scripts/` `input/` `output/cut/` — フォルダ構成

## 必要な環境

- Claude Code CLI
- Python 3.9 以降
- ffmpeg（未インストールの場合はセットアップ手順を生成）
- `silence_cut.py`（別途配置）
