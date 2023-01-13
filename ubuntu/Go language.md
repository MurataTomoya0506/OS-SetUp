# ubuntuにgo言語を導入する


### 1.標準リポジトリで go のインストール

~~~sh
apt  install -y golang-go
~~~

<span style="color: red; ">ーー実行結果ーー</span>

~~~sh
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
The following additional packages will be installed:
 golang-1.18-go golang-1.18-src golang-src
Suggested packages:
 bzr | brz git mercurial subversion
The following NEW packages will be installed:
 golang-1.18-go golang-1.18-src golang-go golang-src
0 upgraded, 4 newly installed, 0 to remove and 9 not upgraded.
Need to get 82.2 MB of archives.
After this operation, 436 MB of additional disk space will be used.
Get:1 http://archive.ubuntu.com/ubuntu jammy/main amd64 golang-1.18-src all 1.18.1-1ubuntu1 [16.2 MB]
Get:2 http://archive.ubuntu.com/ubuntu jammy/main amd64 golang-1.18-go amd64 1.18.1-1ubuntu1 [66.0 MB]
Get:3 http://archive.ubuntu.com/ubuntu jammy/main amd64 golang-src all 2:1.18~0ubuntu2 [4438 B]
Get:4 http://archive.ubuntu.com/ubuntu jammy/main amd64 golang-go amd64 2:1.18~0ubuntu2 [41.8 kB]
Fetched 82.2 MB in 14s (5981 kB/s)
debconf: delaying package configuration, since apt-utils is not installed
Selecting previously unselected package golang-1.18-src.
(Reading database ... 18262 files and directories currently installed.)
Preparing to unpack .../golang-1.18-src_1.18.1-1ubuntu1_all.deb ...
Unpacking golang-1.18-src (1.18.1-1ubuntu1) ...
Selecting previously unselected package golang-1.18-go.
Preparing to unpack .../golang-1.18-go_1.18.1-1ubuntu1_amd64.deb ...
Unpacking golang-1.18-go (1.18.1-1ubuntu1) ...
Selecting previously unselected package golang-src.
Preparing to unpack .../golang-src_2%3a1.18~0ubuntu2_all.deb ...
Unpacking golang-src (2:1.18~0ubuntu2) ...
Selecting previously unselected package golang-go:amd64.
Preparing to unpack .../golang-go_2%3a1.18~0ubuntu2_amd64.deb ...
Unpacking golang-go:amd64 (2:1.18~0ubuntu2) ...
Setting up golang-1.18-src (1.18.1-1ubuntu1) ...
Setting up golang-src (2:1.18~0ubuntu2) ...
Setting up golang-1.18-go (1.18.1-1ubuntu1) ...
Setting up golang-go:amd64 (2:1.18~0ubuntu2) ...

~~~

この画面が出たらインストールされているはず。

<br>

### 2.正常にインストールされたか確認をする　

~~~sh
$ go version
~~~


<span style="color: red; ">ーー実行結果ーー</span>


~~~sh
go version go1.10.4 linux/amd64
~~~

きちんとGo言語がインストールできたことが確認できた