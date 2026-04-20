# [WIP] Salesforce CLI 早見表

> コピペして `<>` の中を書き換えて使用する。

---

## 認証系

### ログイン済みOrg一覧を表示
```bash
sf org list
```

### Orgの詳細情報を表示
```bash
sf org display --target-org <org-alias>
```

### ブラウザでログイン（本番 / Developer Edition）
```bash
sf org login web --alias <org-alias>
```

### ブラウザでログイン（Sandbox）
```bash
sf org login web --alias <org-alias> --instance-url https://test.salesforce.com
```

### ログアウト
```bash
sf org logout --target-org <org-alias>
```

## クエリ

### SOQLクエリを実行
```bash
sf data query \
  --query "SELECT Id, Name FROM <Account> LIMIT 10" \
  --target-org <org-alias>
```

### 結果をCSVで出力
```bash
sf data query \
  --query "SELECT Id, Name FROM <Account> LIMIT 10" \
  --result-format csv \
  --target-org <org-alias> > output.csv
```

---作成中🚧---