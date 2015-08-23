---
layout: post
title: "bitbucket"
date: 2015-08-18 11:07:27 +0800
comments: true
categories: git, bitbucket
---

# 完美的私人仓库
一直想弄个私人仓库，最好无限制创建私人仓库。最好还能有个team可以共享访问私人仓库。本来差点就要去自己搭建一个gitlab了，然后突然看到bitbucket，发现原来完美的私人仓库就是他了。

果断申请账号（必须是免费的5人组team形势的），然后折腾一番将自己的一些小代码放上去。
中间碰到了一些问题，以为类似github上的ssh key的添加，结果添加ssh key到repo里的一个deployment key去了（这个应该是用来专门部署的时候用的key，只读性质的）。
查了下，发现overflow上有人说明了原因，果断尝试了OK解决问题，看客们自己也试试吧，值得推荐！

[http://stackoverflow.com/questions/13306435/repository-access-denied-access-via-a-deployment-key-is-read-only/13309843#13309843](http://stackoverflow.com/questions/13306435/repository-access-denied-access-via-a-deployment-key-is-read-only/13309843#13309843)

```
First confusion on my side was about where exactly to set SSH Keys in BitBucket.

I am new to BitBucket and I was setting a Deployment Key which gives read-access only.

So make sure you are setting your rsa pub key in your BitBucket Account Settings.

Click your BitBucket avatar and select Manage account. There you'll be able to set SSH Keys.

I simply deleted the Deployment Key, I don't need any for now. And it worked
```