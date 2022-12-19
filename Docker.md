
# Dockerのイメージ作成とコンテナの作成を行う


## ubuntu コンテナ作成、起動、停止

### １.イメージの確認をする  
~~~sh
$ docker images　
~~~


<span style="color: red; ">ーー実行結果ーー</span>

|REPOSITORY|TAG|IMAGE ID|CREATED|SIZE|
|-----|-----|---|---|---|
|ubuntu| latest |3c2df5585507 | 2 weeks ago | 69.2MB
|ubuntu|18.4|2d07c6c16e27|3 weeks ago|56.7MB
|nginx |latest|df36ec2d82e6 |4 weeks ago| 135MB
（以下省略）


### 2.イメージを取得する
~~~sh
$ docker pull ubuntu<br>
~~~

取得が終わったらもう一度１のコマンドを入力して無事イメージを作ることができたかを確認する。

### 3.コンテナを作成する


 ~~~sh
 $ docker ps
~~~
 <br>


<span style="color: red; ">ーー実行結果ーー</span>

|CONTAINER ID|IMAGE|COMMAND|CREATED|STATUS|PORTS|NAMES|
|-----|-----|---|---|---|---|---|
|70ddbaae8d12| 2edf9c994f19  |"/kube-vpnkit-forwar…" | 16 minutes ago | Up 16 minutes||k8s_vpnkit-controller_vpnkit-controller_kube-system_b6a39451-0bda-4da0-9893-ff1dc883d1c1_173
|cbbfe2bf2d54|c027a58fa0bb|"/storage-provisione…"|2 hours ago|56.7MB
|



※取得したイメージからコンテナを作成する<br>
~~~sh
$ docker run -it ubuntu<br>
~~~
root@0b5aad08487b:/# 


### 4.コンテナの起動、ログイン、停止<br>

コンテナの起動<br>
~~~sh
$docker start ubuntu
~~~

コンテナへのログイン<br>
~~~sh
$docker exec -it ubuntu bash
~~~
コンテナの停止<br>
~~~sh
$docker stop ubuntu
~~~