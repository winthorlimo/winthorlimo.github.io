---
title: Hexo日志
tags: hexo
categories: Note
top: 80
abbrlink: 1c91193
date: 2019-06-02 12:18:55
---
#### 2019.6.1 

Git 远程遇到了问题:
>Please make sure you have the correct access rights and the repository exists.

发现是ssh key有问题，连接不上服务器

1. 首先是重新在git设置一下身份的名字和邮箱：

    - `git config --global user.name "yourname"`
    - `git config --global user.email“your@email.com"`
    
    注：要添加具体的yourname，your@email
2. 删除.ssh文件夹（直接搜索该文件夹）下的known_hosts
3. 在 git输入命令：

    `$ ssh-keygen -t rsa -C "your@email.com"`

    然后会出现：
    >Generating public/private rsa key pair. Enter file in which to save the key (/Users/your_user_directory/.ssh/id_rsa):

    回车后系统自动在 .ssh 文件夹下生成两个文件，id_rsa和id_rsa.pub，用记事本打开id_rsa.pub，把全部内容复制
4. 登陆GitHub 账户，进入设置中的“SSH and GPG keys”新建 SSH      keys 在 Key中把刚刚复制的粘贴进去，点击 add ssh key
5. 在 git 中输入命令
    
    `ssh -T git@github.com`

    然后输入Yes回车，就会提示成功

之后就可以正常 hexo d -g 啦