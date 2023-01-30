# CentOSをインストールする

##  1. CentOSの取得する


~~~sh
$ docker pull centos:centos7
~~~
をコピーする。

## 2. CentOSのコンテナを構築する


先ほどコピーした"pull"コマンドを実行し、CentOSのイメージを取得する
~~~sh
$ centos7: Pulling from library/centos
Digest: sha256:be65f488b7764ad3638f236b7b515b3678369a5124c47b8d32916d6487418ea4
Status: Image is up to date for centos:centos7
docker.io/library/centos:centos
~~~

CentOSのイメージを取得することができたか確認する
~~~sh
$ docker images
~~~


|REPOSITORY|TAG|IMAGE ID|CREATED|SIZE|
|--------------|-----------|---|---|---|
|centos |  centos7|eeb6ee3f44bd |16 months ago| 204MB

無事CentOSのイメージを取得することができた。

## 3. コンテナの作成
コンテナの作成を行う
コdocker createコマンドを使ってコンテナの作成を行う。
~~~sh
docker create --name status-test -it centos_test/bin/sh
~~~

コンテナが作られたか確認する
~~~sh
$ docker ps
~~~
|CONTAINERID|IMAGE|COMMAND|CREATED|STATUS|NAMES|
|--------------|-----------|---|---|---|----|
f755be539893| centos:centos7 |  "/bin/bash" |10 days ago | Up 4 seconds|centos_test|


## 4.起動、ログイン、停止

|操作名|コマンド|
|-----|-----|
|コンテナの起動|docker start centos_test|
|コンテナへのログイン | docker exec -it centos_test bash|
|コンテナの停止|docker stop centos_test|


以上でCentOS が使えるようになった。