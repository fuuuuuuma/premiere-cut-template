# Premiere Pro 無音カット テンプレート

このリポジトリは Premiere Pro XML の無音カットワークフロー用テンプレートです。

## フォルダ構成

```
.
├── scripts/          # silence_cut.py を配置する
├── input/            # カット対象の XML を置く
└── output/
    └── cut/          # カット済み XML の出力先
```

## セットアップ手順（Claude Code 向け）

1. `scripts/silence_cut.py` を配置する
2. `input/` に Premiere Pro からエクスポートした XML を置く
3. 以下のコマンドで実行する

```bash
python3 scripts/silence_cut.py input/<ファイル名>.xml --output-dir output/cut
```

## オプション

| オプション | 説明 | デフォルト |
|---|---|---|
| `--threshold` | 無音判定閾値（dB） | -50 |
| `--min-silence` | 最小無音長（秒） | 0.2 |
| `--padding` | 余白フレーム数 | 2 |
