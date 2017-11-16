# Capstrano
テンプレート作成(productionとstaging環境用が作成される)
```
cap install
```

テンプレート作成(test環境用が作成される)
```
cap install STAGES=test
```

1. config/deploy.rbに処理内容(タスク)を書く
2. config/deploy/[環境名].rbに環境設定を書く
3. `cap [環境名] [タスク名]`で実行  

基本は`cap [環境名] deploy`で  
指定したデプロイディレクトリ/currentに最新がデプロイされる

ロールバックは`cap [環境名] deploy:rollback`

