# Learn `node:test`

## 本リポジトリの目的
JavaScript Primerの編集作業にあたって、Mochaを`node:test`に置き換える作業の検証を行ないたいため

## 本リポジトリの達成目標
無事にJavaScript Primerの編集作業を終える

## 実行コマンド
### GFMなしMarkdown→HTML
``` bash
$ node main.js sample.md
```

### GFMありMarkdown→HTML
``` bash
$ node main.js --gfm sample.md
```

### テスト実行
``` bash
$ npm test
```

## メモ
### `node --test`は`node --test test/`は書かずにフォルダ指定をしない
フォルダ指定をすると、WSLでは問題なくてもmacOSで以下のエラーが出るので、デフォルトの指定を使うようにする
```bash
% npm test

> test
> node --test test/

node:internal/modules/cjs/loader:1145
  throw err;
  ^

Error: Cannot find module '/Users/windchime-yk/Documents/web/org/whyk-pg/learn-node-test/test'
    at Module._resolveFilename (node:internal/modules/cjs/loader:1142:15)
    at Module._load (node:internal/modules/cjs/loader:983:27)
    at Function.executeUserEntryPoint [as runMain] (node:internal/modules/run_main:142:12)
    at node:internal/main/run_main_module:28:49 {
  code: 'MODULE_NOT_FOUND',
  requireStack: []
}

Node.js v21.7.1
✖ test (61.092688ms)
  'test failed'

ℹ tests 1
ℹ suites 0
ℹ pass 0
ℹ fail 1
ℹ cancelled 0
ℹ skipped 0
ℹ todo 0
ℹ duration_ms 69.542789

✖ failing tests:

test at test:1:1
✖ test (61.092688ms)
  'test failed'
```
なお`node --test test/**/*.js`と書けばエラーは出ないが、それだったら`node --test`のほうがシンプルで良い

## 参考資料
- [ユニットテストを記述する · JavaScript Primer #jsprimer](https://jsprimer.net/use-case/nodecli/refactor-and-unittest/)
- [Mocha - the fun, simple, flexible JavaScript test framework](https://mochajs.org)
- [Test runner | Node.js v20.11.1 Documentation](https://nodejs.org/docs/latest-v20.x/api/test.html)
