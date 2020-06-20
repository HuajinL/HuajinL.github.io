---

title: Hexo 博客
date: 2019.09.05
updated: 2020.05.20
tags: 博客,Hexo
categories: 博客

---

在此感谢up主https://www.bilibili.com/video/av44544186 视屏的教学



# 基于hexo框架搭建自己的博客(windows10)

<!--more-->

+ 前期软件准备  

1、安装git[https://git-scm.com/download/win]

2、安装node.js(因为hexo框架基于node),地址在这[https://nodejs.org/en/]

+ 安装hexo

1、首先查看git与node是否安装好，采用命令(git -v    node -v)查看有无版本号

2、接下来安装cnpm(npm install -g cnpm –registry=https://registry.npm.taobao.org/) (选择镜像到淘宝因为cnpm在国内的下载速度很慢,安好后用 cnpm -v查看)

3、用安装好的cnpm安装hexo(cnpm install -g hexo-cli),同样采用(hexo -v)查看

4、现在需要本地搭建，首先用pwd命令查看当前文件夹，可以用cd命令到你想要放置的文件夹采用mkdir命令创建一个新的文件夹(我用的是blog)，用命令pwd查看当前文件夹，如果已经在blog文件夹下则不需要任何操作，如不在，用cd命令定位到blog文件夹下

5、采用hexo init命令，在输入命令之后等待一会，最后一行出现(INFO Start blogging with Hex)则表明成功，此时在文件夹blog就可以看到八到九个文件夹了，此时基于hexo框架的博客就已经在本地搭好了(只是在本地搭建好了哦)

6、输入hexo s命令显示

INFO  Start processing
INFO  Hexo is running at http://localhost:4000 . Press Ctrl+C to stop.则表明成功

7、在浏览器中输入http://localhost:4000   则可以看到自己在本地搭建好的博客



部署到GitHub下期再见

“愿你我仍在平凡的世界里还是那个不被人理解和不循规蹈矩的创造者”



