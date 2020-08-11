---
title: youkeda0811
date: 2020-08-11 18:06:56
tags:
---
绑定本地仓库到Github
1.初始化为git仓库：git init
2.查看绑定仓库情况：git remote -v（只有这个命令显示空白，我们才可以继续绑定）
3.绑定远程仓库的命令：git remote add origin 仓库地址（GitHub上面的SSH）
4.查看绑定仓库情况：git remote -v（确定绑定成功）
5.删除绑定仓库：git remote remove origin


Ctrl+c可以退出输入


创建博客文件夹：hexo init blog（其中blog是博客文件夹的名字）
安装发布工具：进入blog目录（cd blog）：npm install hexo-deployer-git --save
修改配置文件：找到_config.yml文件：
theme: landscape
deploy:
  type: git
  repository: 你的GitHub仓库地址
  branch: master


Hexo提交：
1.hexo clean：hexo clean
2.Hexo generate：hexo g
3.Hexo deploy：hexo d

1.创建博客文件：hexo new 博客名（例如hexo new hello，则会生成hello.md的文件）文件的位置：source/_post
2.更换主题next：默认主题是landspace
①下载新的主题：git clone https://gitee.com/xiaoyebing/hexo-theme-next.git themes/next
②打开_config.yml文件，将配置中的theme: landscape改成theme: next
③执行上面的hexo提交命令（注意：一定要在blog里面执行）


Branch的简单命令
1.创建分支：git branch 分支名（例如git branch dev）
2.切换到新的分支：git checkout dev（dev是分支的名字）
***1+2合起来一起用的命令：git checkout -b dev