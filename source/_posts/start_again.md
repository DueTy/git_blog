---
title: start again
---
## 起因
我又双叒叕起了个个博，最终还是倒腾不动了，选择了hexo，调了个自适应皮肤，那，我们重新开始吧...
## hexo配置

#### 全局脚手架依赖

``` bash
npm install -g hexo-cli
```
安装完成后看一下版本号，新版本的hexo是跟npm版本挂钩的

``` bash
hexo -v
```
#### 初始化项目

``` bash
hexo init xxx(项目名)
# 完成后进入
cd xxx(项目名)
# 安装依赖
npm / cnpm / yarn i
```
然后开始为所欲为，中间的一些诸如编写文章的指令，官方文档都有提供，而由于hexo是直接编译md文件，生成页面，所以我是直接修改source/_posts目录下的文章进行本地修改，完成之后，来到发布
#### 发布GitHub Page
此处涉及的++GitHub Page++，是每个git仓库提供的页面化功能，我这里是将master作为代码分支，再切了一个gh-pages分支作为页面分支，部署涉及一个工具

``` bash
hexo-deployer-git
```
安装至本地后，修改项目的配置文件，根目录下的_config.yml，找到如下，按需配置

``` bash
# Deployment
## Docs: https://hexo.io/docs/deployment.html
deploy:
  type: 部署类型
  repo: 部署仓库
  branch: 部署到对应分支

```
然后我们执行以下命令

``` bash
hexo clean & hexo deploy
```
此步骤需要填写git账号和密码，跟着走就行，提示完成，如果不知道页面地址，按照如下步骤可找到
```
个人git -> 对应仓库 -> settings -> 拉到最下面找到github pages这一项，找到Your site is published at xxxxx，便是你的页面地址
```
当然如果有自己的域名，也可以做映射，具体操作请搜github pages域名绑定（手动狗头，不要打我）
##### ps
如果绑定域名之后，每次部署会导致域名被重置，此时可在项目根目录下的source文件夹中添加名为CNAME的文件，文件中写入你的域名即可，因为在项目部署后，source中的文件会被copy至编译后的根目录下，而git提供的可访问页面会解析该文件配置的域名，进行映射。
#### 结语
不管是说给看的人，还是说给自己：做一件事一定要坚持，从大学的时候，jQuery版本，到工作一年的react版本，再到现在的hexo，每次搭起来基本就吃灰，之前写的也全部丢了，而且都是见证自己成长的宝贵的记忆，现在想想懊悔不已。所以还在学习的同学，不要丢掉自己成长的一点一滴，一定要保持激情，敬畏技术，不要浪费时间，明确自己想要什么。
##### 莫惧前路不平，且惜过往不易




