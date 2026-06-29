# フォルダ構成テンプレート

壁打ちの回答をもとに以下の構成を作成してください。

```
{{PROJECT_NAME}}/
├── CLAUDE.md          # プロジェクト運用ルール（設定値を記載）
├── scripts/
│   └── silence_cut.py # または symlink（Q8 の回答に従う）
├── input/             # Q6 の書き出し場所からXMLをここにコピーして使う
└── output/
    └── cut/           # Q7 の保存先（カット済みXMLの出力先）
```

## 生成する CLAUDE.md の内容

プロジェクトの CLAUDE.md には以下の設定値を記載すること:

```markdown
# {{PROJECT_NAME}} — 運用設定

## /{{COMMAND_NAME}} 設定

| 項目 | 値 |
|---|---|
| スクリプトパス | {{SCRIPT_PATH}} |
| メイン音声トラック | {{MAIN_TRACK}} |
| 出力先 | {{OUTPUT_DIR}} |
| 無音判定閾値 | {{THRESHOLD}}dB |
| 最小無音長 | {{MIN_SILENCE}}秒 |
| パディング | {{PADDING}}フレーム |
| 出力サフィックス | {{OUTPUT_SUFFIX}} |
```

## ffmpeg 未インストールの場合（Q11 が「いいえ」）

以下のセットアップ手順も出力すること:

```bash
# Homebrew でインストール
brew install ffmpeg

# インストール確認
ffmpeg -version
```
