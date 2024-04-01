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

## 参考資料
- [ユニットテストを記述する · JavaScript Primer #jsprimer](https://jsprimer.net/use-case/nodecli/refactor-and-unittest/)
- [Mocha - the fun, simple, flexible JavaScript test framework](https://mochajs.org)
- [Test runner | Node.js v20.11.1 Documentation](https://nodejs.org/docs/latest-v20.x/api/test.html)
