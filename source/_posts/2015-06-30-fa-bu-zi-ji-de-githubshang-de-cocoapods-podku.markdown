---
layout: post
title: "发布自己的github上的cocoaPods pod库"
date: 2015-06-30 21:01:40 +0800
comments: true
categories: 
---


今天第一次在github上publish一个ILEditLabel控件，同时支持了cocoapods查找该pod库。

这里简单说下几个小坑。

提交前注意给你的github的代码打tag，比如这里的0.0.1，然后编写podspec文件，对应好里面的source的tag，其实可以将pod的tag和你的库的tag一致，这样方便记忆。

然后你需要执行pod spec lint specFile测试下是否spec文件编写正确。

如果发现远程tag打错了，你可以通过命令```git push origin refs/tags/yourtag```来删除远程tag。

通过podspec文件的检测后，就到了发布该spec文件了。

那就是需要通过```pod trunk push specFile```的方式来提交spec文件到cocoapods上。

但是由于我是第一次提交，执行命令后提示：

```
You need to register a session first.
```

所以需要参照cocoapods上的这篇文章[Getting setup with Trunk][1]先注册自己的session。

注册需要执行如下命令：

```
pod trunk register orta@cocoapods.org 'Orta Therox' --description='macbook air'
```

然后你就会在你输入的orta@cocoapods.org邮箱里收到一个email，点击里面的连接完成认证，之后你就可以完成提交。至此自己故障庆祝吧~~~


[1]: http://guides.cocoapods.org/making/getting-setup-with-trunk.html