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

```

test周りが特に雑な状態なので直したい
(というかtestできないのが現状。以下のエラーが`npm run lint`で出てしまう)
.eslintrc.js`'prettier/@typescript-eslint'`で無効化すると、noundefが出るのでどうしたものか

``` bash
$ npm run lint                                                                                                                                                                                                  [13:35:01]

> ts-sample@1.0.0 lint
> eslint --ext .js,.ts --ignore-path .gitignore .


Oops! Something went wrong! :(

ESLint: 7.21.0

Error: Cannot read config file: /home/user/ts-sample/node_modules/eslint-config-prettier/@typescript-eslint.js
Error: "prettier/@typescript-eslint" has been merged into "prettier" in eslint-config-prettier 8.0.0. See: https://github.com/prettier/eslint-config-prettier/blob/main/CHANGELOG.md#version-800-2021-02-21
Referenced from: /home/user/ts-sample/.eslintrc.js
    at Object.<anonymous> (/home/user/ts-sample/node_modules/eslint-config-prettier/@typescript-eslint.js:1:69)
    at Module._compile (/home/user/ts-sample/node_modules/v8-compile-cache/v8-compile-cache.js:192:30)
    at Object.Module._extensions..js (internal/modules/cjs/loader.js:1138:10)
    at Module.load (internal/modules/cjs/loader.js:982:32)
    at Function.Module._load (internal/modules/cjs/loader.js:875:14)
    at Module.require (internal/modules/cjs/loader.js:1022:19)
    at module.exports (/home/user/ts-sample/node_modules/import-fresh/index.js:32:59)
    at loadJSConfigFile (/home/user/ts-sample/node_modules/@eslint/eslintrc/lib/config-array-factory.js:225:16)
    at loadConfigFile (/home/user/ts-sample/node_modules/@eslint/eslintrc/lib/config-array-factory.js:309:20)
    at ConfigArrayFactory._loadConfigData (/home/user/ts-sample/node_modules/@eslint/eslintrc/lib/config-array-factory.js:609:42)
npm ERR! code 2
npm ERR! path /home/user/ts-sample
npm ERR! command failed
npm ERR! command sh -c eslint --ext .js,.ts --ignore-path .gitignore .

npm ERR! A complete log of this run can be found in:
npm ERR!     /home/user/.npm/_logs/2021-03-09T04_35_03_465Z-debug.log
```

## 参考

<https://qiita.com/suzuki_sh/items/f3349efbfe1bdfc0c634>#
