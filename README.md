# @Slime-hatena/twsv : twsv

## Fork元との変更点

特定ユーザーの画像を取得する際、リツイートを取得しません。  
パラメーターのみを差し替えたため、不具合等のサポートはできません。

GitHub Packagesのみで公開されます。

See also: [Slime-hatena/twsv #1](https://github.com/Slime-hatena/twsv/issues/1)

## Original readme

Twitter の画像・動画をダウンロードする CLI ツール。

[![NPM Version](https://img.shields.io/npm/v/@neos21/twsv.svg)](https://www.npmjs.com/package/@neos21/twsv) [![GPR Version](https://img.shields.io/github/package-json/v/neos21/twsv?label=github)](https://github.com/Neos21/twsv/packages/328039)


## Installation

```sh
$ npm install -g @neos21/twsv

# クレデンシャル情報を設定する
export TWITTER_CONSUMER_KEY='Your Consumer Key'
export TWITTER_CONSUMER_SECRET='Your Consumer Secret'
export TWITTER_ACCESS_TOKEN_KEY='Your Access Token Key'
export TWITTER_ACCESS_TOKEN_SECRET='Your Access Token Secret'
```


## How To Use

```sh
# 指定ユーザのタイムラインより直近200件のツイートを取得し、それらに紐付く画像・動画を取得する
$ twsv https://twitter.com/USERNAME

# 指定のユーザのいいね一覧より直近200件のツイートを取得し、それらに紐付く画像・動画を取得する
$ twsv https://twitter.com/USERNAME/likes

# 指定のツイートから画像・動画を取得する
$ twsv https://twitter.com/USERNAME/status/0000000000000000000
```

デフォルトの保存先は、コマンドを実行した時のカレントディレクトリに `twsv-downloads/` ディレクトリを作り、その下にファイルを保存する。

保存先ディレクトリを変更する場合は、環境変数か第2引数で指定できる (両方指定されている場合は第2引数が優先)。

```sh
# 環境変数で指定して実行
$ export TWSV_SAVE_DIRECTORY='/home/downloads'
$ twsv https://twitter.com/USERNAME/status/0000000000000000000

# 第2引数で指定して実行
$ twsv https://twitter.com/USERNAME/status/0000000000000000000 '/home/downloads'
```


## Links

- [Neo's World](https://neos21.net/)
- [GitHub - Neos21](https://github.com/Neos21/)
- [GitHub - twsv](https://github.com/Neos21/twsv)
- [npm - @neos21/twsv](https://www.npmjs.com/package/@neos21/twsv)
