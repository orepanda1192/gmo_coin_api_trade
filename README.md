# GMO Coin API Trade

簡単なサンプルプロジェクトです。主にGMOコインのAPIを使ったマーケットデータ取得とトレード管理用のスクリプトを含みます。

## 構成

- `main.py` - エントリポイント
- `market_data.py` - マーケットデータ取得ロジック
- `trade_manager.py` - 注文・トレード管理ロジック
- `debug_main.py` - 開発用のデバッグエントリポイント

## 必要条件

- Python 3.8+（ローカルの好みのバージョンを使用してください）

推奨: 仮想環境を作成して依存を分離してください。

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt  # あれば
```

## 使い方

簡単にスクリプトを実行する例:

```bash
python main.py
```

## 設定 (config.json)

このプロジェクトは `config.json` を使って設定を読み込むことができます（`config.json` をルートに置いてください）。
`config.json` には API キーやエンドポイント、取引パラメータなどを記載します。機密情報はコミットしないでください。

例（値はプレースホルダです — 実際のキーは必ず安全に管理してください）:

```json
{
  "API_KEY": "abcd12345",
  "SECRET_KEY": "abcd12345",
  "ORDER_SIZE": "2000"
}
```

代替として、`.env` や環境変数を使うこともできます（`os.environ` から読み込む実装がある場合）。

セキュリティ上の注意: 実際の API キーやシークレットはバージョン管理に含めないでください。開発時は環境変数か、暗号化されたシークレットストアを利用してください。

## .gitignore
このリポジトリは `__pycache__/` 等のPythonキャッシュを追跡しないように設定されています。

## 注意
実際の取引を行う場合は、十分なテストとリスク管理（実資金でのテストを避ける等）を行ってください。

# gmo_coin_api_trade
