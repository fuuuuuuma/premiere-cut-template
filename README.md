# premiere-cut-template

Premiere Pro XML 無音カットワークフローのテンプレートリポジトリです。

## 使い方

1. このリポジトリをクローンする
2. `scripts/silence_cut.py` を配置する
3. `input/` にカット対象の XML を置く
4. Claude Code に `/cut` で実行を依頼する

出力は `output/cut/` に書き出されます。
