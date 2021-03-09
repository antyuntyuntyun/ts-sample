# ts-sample

typescriptでのcli開発練習用

## usage

``` bash
# gitigoreはまとめて設定
curl https://raw.githubusercontent.com/github/gitignore/master/Node.gitignore > .gitignore

# 開発用に監視
npm run build
# VScode開発であればtask設定しているので、コマンドパレットからTasks: Run taskで実行可能#
# Ctrl + shift  + B でビルドタスクが立ち上がる

# プロジェクトに対してシンボリックリンクが貼られ、ローカルでglobal install した状態になり
# binに指定したキーコマンドでコマンド実行可能に
npm link
ts-sample 15

# lint
# .eslintignoreで設定用のjsを除外
# ビルド対象ではないがlint対象にはしたいので、lintようにtsconfig.eslint.jsonが存在する
npm run lint

# test
npm run test

```

## 参考

<https://qiita.com/suzuki_sh/items/f3349efbfe1bdfc0c634>#
