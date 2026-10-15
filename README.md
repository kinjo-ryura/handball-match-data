# handball-match-data

アプリ「ハンド記録」が読むサンプル試合の配信データ。JSON の形は [SCHEMA.md](SCHEMA.md)。

| 一覧 | 本体 |
|---|---|
| `matches/index.json`（注目の試合） | `matches/{slug}.json` |
| `highlights/index.json`（ハイライト） | `highlights/{slug}.json` |
| `competitions/index.json`（大会の名簿） | `competitions/{id}.json`（大会ごとの試合の一覧。試合の本体は `matches/`） |

アプリは `https://raw.githubusercontent.com/kinjo-ryura/handball-match-data/main/` から取る。

push と PR のたびに、[handball-toolkit](https://github.com/kinjo-ryura/handball-toolkit) の検証 CLI が全体を検証する（`.github/workflows/validate.yml`）。
