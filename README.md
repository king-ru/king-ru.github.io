# king-ru.github.io
## king-ru's blog
### title: 第一次采用hexo+github搭建博客笔记



## hexo介绍：
hexo是一个非常好用的搭建博客的框架，里面有许多主题可供选择。

## hexo搭建博客基础大致流程为：

安装Node.js →安装Git → 安装Hexo → 本地测试运行 → 注册给github与coding并创建pages仓库 → 设置主题 → 修改两个配置文件


### 1.安装node/js和git
在node.js官网上下载，完了之后设置环境变量.
在git官网上下载，完了之后设置环境变量.

### 2.安装hexo
    ####初始化
随便建一个文件夹，名字随便取，我取其名为blog，cd 到文件夹里，先安装必要的文件，执行以下命令：
1.hexo init  # hexo会在目标文件夹建立网站所需要的所有文件
2.npm install  # 安装依赖包

### 3.本地运行
1.hexo g # 等同于hexo generate，生成静态文件
2.hexo s # 等同于hexo server，在本地服务器运行
！[](https://raw.githubusercontent.com/king-ru/king-ru.github.io/master/img/1.png)
之后打开浏览器并输入IP地址 http://localhost:4000/ 查看，效果如下
![](https://raw.githubusercontent.com/king-ru/king-ru.github.io/master/img/2.png)

### 4.注册给github
在github上建立一个仓库，存放该项目。

### 5.改变主题
（我安装的是yilia主题，下载最多的是next主题，但自己那个主题配置起来有问题，最终 选择了它的另一个主题版本yilia）

#### 使用默认主题
（landscape是hexo的默认主题）在站点配置文件下改一些东西。
branch和type这两行需要自己加。

```
  url: http://king-ru.github.io

deploy:
branch: master
type: git
repo: https://github.com/king-ru/king-ru.github.io.git
```
#### 自定义主题

以下提到的站点配置文件指的是博客文件根目录下的 _config.yml，主题配置文件是主题文件夹下的 _config.yml，
1.clone主题
到作者的github[Litten](https://github.com/litten/hexo-theme-yilia)上clone到本地。（theme文件夹下）该文件夹的名字应该和主题相同。
2.配置主题
具体配置参考[yilia](https://github.com/litten/BlogBackup/blob/master/_config.yml)
将作者的_config.yml文件clone到站点配置文件下，替换原来的_config.yml文件。
将站点配置文件下以及主题配置文件的_config.yml文件根据自己的要求调整。必要的调整以下会谈到。一定要注意冒号和后面内容之间的空格，不能省去。

打开站点配置文件（URL要改成自己的）

  ```
  url: http://king-ru.github.io

  theme: yilia
  exclude_generator:
  ```

  ```
  Deployment
  Docs: http://hexo.io/docs/deployment.html
  deploy:
    type: git
    repository: https://github.com/king-ru/king-ru.github.io.git
    branch: master

  deploy:
    branch: master
    type: git
    repo: https://github.com/king-ru/king-ru.github.io.git
  ```
打开主题配置文件里面根据自己的需求改就可以。

### 总结一下简单命令
hexo init [folder] # 初始化一个网站。如果没有设置 folder ，Hexo 默认在目前的文件夹建立网站

hexo new title # 新建一篇文章。title为文章名字

hexo version # 查看版本

hexo clean # 清除缓存文件 (db.json) 和已生成的静态文件 (public)

hexo g # 等于hexo generate # 生成静态文件

hexo s # 等于hexo server # 本地预览

hexo d # 等于hexo deploy # 部署，可与hexo g合并为 hexo d -g

hexo g -d #每次修改之后都要运行，提交到远程仓库。

#### 第一次搭建网站，大家有建议可以邮箱留言给我！

---
