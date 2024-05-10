# codespace-node-red-starter-simple

これはシンプルに Node-RED を起動する GitHub Codespaces 用のリポジトリです。

## 環境を起動

- このリポジトリを Code ボタン > Codespaces タブをクリック > Create codespaces on main をクリック。
- このリポジトリの内容で Codespace がブラウザが開く
- 初回起動時に Node-RED インストールは自動で行われるので待ちます

## 使い方

ターミナルで以下のコマンドを実行します。

```
npm start
```

また `npm start` を使わず以下のコマンドでも実行可能です。

```
npx node-red -u ./.node-red
```

## 中の仕組み

- `sudo npm install -g --unsafe-perm node-red` でグローバルインストールしてしまうと設定フォルダが分かりにくい場所（/home/codespace/.node-red）で動作してしまうので、`npm i node-red` でプロジェクトフォルダ内にインストールした後、`node-red -u ./.node-red` で、プロジェクトフォルダ内の `.node-red` フォルダで設定フォルダが動作するようにしています。
- 起動コマンドは `npm start` で起動すれば、内部で `node-red -u ./.node-red` が実行されるので、通常はそれを使ってください。
