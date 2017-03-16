---
layout: post
title:  安装windows包管理工具
date:   2017-03-15 10:00:00 +0800
categories: 工具 wintool
---    
## 起因  

因为本网站是在linux(centos 7) 里面安装的，[jekyll官方](http://jekyll.com.cn/)称最好的环境是*nix系统，不适合windows,所以部署了很不熟悉的环境（原win+c#开发），  
好吧，配置好了，但linux确实用不太习惯，加上喜欢用vscode，在win来写blog,如果想本地预览，就要安装jekyll,jekyll
这种程序又是命令行的，跟nodejs类似吧，服务形式，无GUI，在网上找（我不会告诉你我是在找jekyll模版）了发现一个win下的包管理工具 [chocolaty](https://chocolatey.org/)   

所以我的目的是使用chocolatey安装jekyll


## 行动  
### 1.下载        

(window下启动powershell)

```diff
+ win + R 
+ 运行 `powershell` 

```   
<!--```diff
+ this will be highlighted in green
- this will be highlighted in red 
```-->

在powershell下启动（远程脚本运行）具体[参照](http://www.cnblogs.com/zhaozhan/archive/2012/06/01/2529384.html),  
```diff

+ 若要在本地计算机上运行您编写的未签名脚本和来自其他用户的签名脚本，请使用以下命令将计算机上的 
+ 执行策略更改为 RemoteSigned： 
  set-executionpolicy remotesigned
```

### 2. 安装 （[Help](https://chocolatey.org/install)）   

    

```
2.1. 安装chocolatey  

iwr https://chocolatey.org/install.ps1 -UseBasicParsing | iex

``` 

```
2.2. 安装Ruby(通过上面的安装的chocolatey)  

    choco install ruby -y

``` 
```
2.3. 安装Jekyll/Sass(通过上面的安装的Ruby)  

    gem install github-pages

``` 

### 3. 运行   
这里运行建议使用其他人的模板开始，自己可以重新开始做一个，但是呢，现在还是流行脚手架，推荐一个[Jekyll-Mono](https://github.com/AkshayAgarwal007/Jekyll-Mono),别问为什么是这个，我就是抄他的（~0。0~）。具体git的操作这里就不做多备注了，我这里是git clone在D:/workspace  

 
```js
git clone  https://github.com/AkshayAgarwal007/Jekyll-Mono.git
 
```  
然后，  
```
cd D:/workspace/Jekyll-Mono  
jekyll start  

```  
这时候可以在本地 http://localhost:4000 查看安装的jekyll网站了
## 结语  
**其实写这个东西也不知道谁会看，或者只是给自己做一个记录，写得漏洞百出的，没有什么逻辑可言，希望自己不要因此而停止吧，虽然很是乱，但毕竟才开始，跟我的小肉肉一样**
![](http://image18.poco.cn/mypoco/myphoto/20170315/11/6645508220170315115602090.jpg)


