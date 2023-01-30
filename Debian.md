# Debianをインストールする

##  1. DebianのイメージをDocker hubから取得する

https://hub.docker.com/_/debian

上記ホームページの右上にある
~~~sh
$ docker pull debian
~~~
をコピーする。

## 2. Debianのコンテナを構築する


先ほどコピーした"pull"コマンドを実行し、Debian7のイメージを取得する
~~~sh
$ latest: Pulling from library/debian
Digest: sha256:534da5794e770279c889daa891f46f5a530b0c5de8bfbc5e40394a0164d9fa87
Status: Image is up to date for debian:latest
docker.io/library/debian:latest
~~~

debianのイメージを取得することができたか確認する
~~~sh
$ docker images
~~~


|REPOSITORY|TAG|IMAGE ID|CREATED|SIZE|
|--------------|-----------|---|---|---|
|debian |  latest |5c8936e57a38 | 12 days ago | 124MB

無事Debianのイメージを取得することができた。

## 3. コンテナの作成、起動、ログイン、停止



|操作名|コマンド|
|-----|-----|
|コンテナ作成| docker create --name status-test -it debian_test/bin/sh|
|コンテナの起動|docker start debian_test|
|コンテナへのログイン | docker exec -it debian_test bash|
|コンテナの停止|docker stop debian_test|
