# RHEL7をインストールする

##  1. RHEL7のイメージを公式サイトからサイトから取得する

https://catalog.redhat.com/software/containers/rhel7/57ea8cee9c624c035f96f3af?container-tabs=gti&gti-tabs=unauthenticated

上記ホームページの下の方にある
~~~sh
$ docker pull registry.access.redhat.com/rhel7:7.9-887
~~~
をコピーする。

## 2. RHEL7のコンテナを構築する


先ほどコピーした"pull"コマンドを実行し、RHEL7のイメージを取得する
~~~sh
$ business11@2020business11noMacBook-Air ~ % docker pull registry.access.redhat.com/rhel7:7.9-887
7.9-887: Pulling from rhel7
:
Status: Image is up to date for registry.access.redhat.com/rhel7:7.9-887
registry.access.redhat.com/rhel7:7.9-887
~~~

REEL7のイメージを取得することができたか確認する
~~~sh
$ docker images
~~~


|REPOSITORY|TAG|IMAGE ID|CREATED|SIZE|
|--------------|-----------|---|---|---|
|registry.access.redhat.com/rhel7| 7.9-887|71f49ae778de | 5 weeks ago | 208MB

無事RHEL7のイメージを取得することができた。

## 3. コンテナの作成、起動、ログイン、停止



|操作名|コマンド|
|-----|-----|
|コンテナ作成| docker create --name status-test -it rhel_test/bin/sh|
|コンテナの起動|docker start rhel_test|
|コンテナへのログイン | docker exec -it rhel_test bash|
|コンテナの停止|docker stop rhel_test|
