# WebPack + Sass + url-loader + file-loader のサンプル

url-loaderとfile-loaderを使うと、CSS内の画像等を埋め込んだり、外部参照とできます。

- `src`フォルダーに画像を配置しておく
- 容量の小さい画像はurl-loaderによって`main.js`にバンドルされる
- 容量の大きい画像はfile-loaderによってビルドするとfile-loaderによって`dist`フォルダーにコピーされる


## ゼロから環境構築する場合の手順

### インストールコマンド

まずはpackage.jsonを作る。

```bash
npm init -y
```

その上で、必要なモジュールをインストールする。

```bash
npm i -D webpack webpack-cli node-sass css-loader url-loader file-loader sass-loader style-loader
```

### webpack.config.js の書き方

[webpack.config.js](webpack.config.js)のコードを参照ください。

webpackのデフォルト構成としているので、`src`フォルダーにソースファイルを格納すること。デフォルトではエントリーポイントは`src/index.js`である。

### ビルドコマンド

```bash
npx webpack
```

`dist`フォルダーに成果物が出力されます。


## このフォルダーをダウンロードしてきてから構築する手順

### インストールコマンド

```bash
npm i
```

### ビルドコマンド

`package.json`にビルドを書いているので、これを使うのがオススメ。

```bash
npm run build
```

もしくは、npxコマンドを使ってもOK。

```bash
npx webpack
```

`dist`フォルダーに成果物が出力されます。

