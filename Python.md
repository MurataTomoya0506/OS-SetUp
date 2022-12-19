 # ubuntuにパイソンをインストールする
 
 
### 0-1.wgetコマンドをインストール

>#apt install wget

 ### 0-2.sudoをインストール

>#apt-get install sudo
 
 
 <br>
 
### 1.ビルド環境の準備する（必要なツールをインストール）


>$ apt audate

>$ sudo apt install build-essential libbz2-dev libdb-dev \
  libreadline-dev libffi-dev libgdbm-dev liblzma-dev \
  libncursesw5-dev libsqlite3-dev libssl-dev \
  zlib1g-dev uuid-dev tk-dev

### 2.ソースコードをダウンロードする


2-1.ターミナルからインストールする
>/# wget https://www.python.org/ftp/python/3.9.2/Python-3.9.13.tar.xz

2-2ダウンロードしたファイルを解凍する
>tar xJf Python-3.9.2.tar.xz

### 3.ビルドする

>$ cd Python-3.9.2

>$ ./configure

>$ make

>$  make install

<br>


#### インストールが完了したら下記のような表示が出る

>（省略）
Looking in links: /tmp/tmptq6lx706
Requirement already up-to-date: setuptools in /usr/local/lib/python3.9/site-packages (49.2.1)
Requirement already up-to-date: pip in /usr/local/lib/python3.9/site-packages (20.2.3)


<br>

### 4.正常にインストールされたか確認する

~~~sh
$ python3 -V <br>
~~~

<span style="color: red; ">ーー実行結果ーー</span>

~~~sh
root@6c715f176372:/Python-3.9.2#
~~~
<br>
<br
<br>


~~~sh
$ which python3<br>
~~~
<span style="color: red; ">ーー実行結果ーー</span>

~~~sh
/usr/local/bin/python3
~~~
<br>
<br>

### 5.Pythonを起動する
ターミナルに　***python3***　と入力する

<span style="color: red; ">ーー実行結果ーー</span>
~~~sh
Python 3.9.2 (default, Nov 26 2022, 19:28:32) 
[GCC 7.5.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
~~~
6.試しに「Hello World」を表示させる

~~~sh
print("Hello World")
実行結果：
Hello World
~~~
7.Pythonを停止させる

~~~sh
exit()
~~~
<span style="color: red; ">ーー実行結果ーー</span>

~~~sh
root@267e441941fa:/Python-3.9.2# 
~~~