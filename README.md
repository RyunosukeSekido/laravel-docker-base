# laravel-docker-base

## 概要

Laravel+Docker環境（nginx, MySQL）でwebアプリケーションを構築する際のベースとして使用できます。

## 使い方
1. リポジトリのクローン
```
git clone https://github.com/RyunosukeSekido/laravel-docker-base.git
```

2. Makefileを使って環境を構築
```
make install
```

上記コマンドを実行後、[http://localhost:8080/](http://localhost:8080/)にアクセスすると、
Laravelのウェルカムページが表示されます。  
※Laravelのソースはsrc配下に配置されています。

## 補足
``` make install ```を実行後に以下のようなメッセージが表示される場合
```
You have not agreed to the Xcode and Apple SDKs license. You must agree to the license below in order to use Xcode.
Press enter to display the license:

Xcode and Apple SDKs Agreement
```
下記コマンド（Xcodeのライセンスに同意するためのコマンド）を実行して再度```make install```を実行してください。
```
sudo xcodebuild -license accept
```
