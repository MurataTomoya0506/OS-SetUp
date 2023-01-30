# R言語をubuntuにインストールする

### 1. ubuntuのバージョン確認をする

~~~sh
 $ cat /etc/lsb-release
~~~


---実行結果---
~~~sh
DISTRIB_ID=Ubuntu
DISTRIB_RELEASE=18.04
DISTRIB_CODENAME=bionic
DISTRIB_DESCRIPTION="Ubuntu 18.04.6 LTS"
~~~


### 2. Rをインストールする
~~~sh
$ apt install --no-install-recommends r-base
~~~

---実行結果---
~~~sh
Reading package lists... Done
Building dependency tree       
Reading state information... Done
r-base is already the newest version (3.4.4-1ubuntu1).
0 upgraded, 0 newly installed, 0 to remove and 23 not upgraded.
~~~

これでubuntuにR言語をインストールすることができました

### 3. Rの起動確認をする
R言語をインストールして、「R」と入力すると、バージョンが表示され、起動する
~~~sh
＄ R

R version 3.4.4 (2018-03-15) -- "Someone to Lean On"
Copyright (C) 2018 The R Foundation for Statistical Computing
Platform: x86_64-pc-linux-gnu (64-bit)

R is free software and comes with ABSOLUTELY NO WARRANTY.
You are welcome to redistribute it under certain conditions.
Type 'license()' or 'licence()' for distribution details.

R is a collaborative project with many contributors.
Type 'contributors()' for more information and
'citation()' on how to cite R or R packages in publications.

Type 'demo()' for some demos, 'help()' for on-line help, or
'help.start()' for an HTML browser interface to help.
Type 'q()' to quit R.

> 
~~~
　
### 4. Rを終了する
~~~sh
> q()
~~~
---実行結果---

~~~sh
Save workspace image? [y/n/c]: 
~~~
ワークスペースを保存するかと出てくるので任意の英字を入力すると、正常に終了する。
~~~sh
root@35dc0118458c:/# 
~~~