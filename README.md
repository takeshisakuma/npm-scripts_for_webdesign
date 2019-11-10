# npm-scripts_for_webdesign

pug(ejs)、scss(stylus)、typescriptのコンパイル、browserSync、画像の圧縮、コードの整形、公開時の不要ファイルの削除、圧縮ができます。

## 準備
1. git cloneして、フォルダの中に入ります。
2. ターミナルでnpm ciを実行して必要なパッケージをダウンロードしてください。
3. srcフォルダの中にコンパイルしたいファイルを格納します。

## 使用
- コンパイル：ターミナルでnpm run watch:allと打ってください
- 整形：ターミナルでnpm run format:allと打ってください
- 公開用の不要ファイル削除、圧縮：ターミナルでprepare:allと打ってください

## 変更
各種設定ファイルは必要に応じて変更してください。

ejs、stylusのコンパイルをする、TypeScriptではなくJavaScriptを直接書く場合は、package.jsonを書き換えてください。

```
"watch:all": "run-p watch:pug2html watch:scss2cssprefix watch:ts watch:img start:server"
//↓
"watch:all": "run-p watch:ejs2html watch:stylus2cssprefix watch:js watch:img start:server"

"format:all": "run-p format:scss format:ts"
//↓
"format:all": "run-p format:stylus format:js"
```

## その他
詳しい説明は[こちらで確認できます。](https://qiita.com/takeshisakuma/items/dbbb1c465099e6e4dd2e)
