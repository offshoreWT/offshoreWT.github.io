---
title: Hello World
---
Welcome to [Hexo](https://hexo.io/)! This is your very first post. Check [documentation](https://hexo.io/docs/) for more info. If you get any problems when using Hexo, you can find the answer in [troubleshooting](https://hexo.io/docs/troubleshooting.html) or you can ask me on [GitHub](https://github.com/hexojs/hexo/issues).

## Quick Start

### Create a new post

``` bash
$ hexo new "My New Post"
```

More info: [Writing](https://hexo.io/docs/writing.html)

### Run server

``` bash
$ hexo server
```

More info: [Server](https://hexo.io/docs/server.html)

### Generate static files

``` bash
$ hexo generate
```

More info: [Generating](https://hexo.io/docs/generating.html)

### Deploy to remote sites

``` bash
$ hexo deploy
```

### 插入图片

[如何插入图片][2]

[ 我的第一个hexo博客参考教程 ][3]

本地预览
```
    hexo g
    hexo server
```

部署
```
    hexo clean
    hexo generate
    hexo deploy
```


部署简化
```
    hexo clean
    hexo generate
    hexo deploy
```

修改config.yml中的deploy参数，分支应为master, 这样就可以新建其他分支保存源码了，master存折deploy信息
于是我新建了一个分支
```

git init

git checkout -b source0

git commit -am "ff"

git remote add origin https://github.com/offshoreWT/offshoreWT.github.io/ 

git push origin source0


```

source0或者sourceN以后用来存储各个版本的源文件信息


不要忘了，每次写完最好都把源文件上传一下

```

git add .
git commit –m "xxxx"
git push 

```

这样以后只要`git pull`即可更新了。

### hexo拓展教程

有时间多看看[Hexo指南][1]
More info: [Deployment](https://hexo.io/docs/deployment.html)

[hexo多人协作：coding pages分流国内][4]

### Coding 分流配置，great

```
# Deployment
## Docs: https://hexo.io/docs/deployment.html
deploy:
  type: git
  repo: 
    github: https://github.com/offshoreWT/offshoreWT.github.io,master
    coding: https://git.coding.net/yezhaoliang/offshoreWT.git,master

```

测试结果如下，的确发往两个备份库

``` sh

Everything up-to-date
Branch master set up to track remote branch master from https://github.com/offshoreWT/offshoreWT.github.io.
On branch master
nothing to commit, working tree clean
Counting objects: 30, done.
Delta compression using up to 4 threads.
Compressing objects: 100% (17/17), done.
Writing objects: 100% (30/30), 3.03 KiB | 0 bytes/s, done.
Total 30 (delta 11), reused 0 (delta 0)
To https://git.coding.net/yezhaoliang/offshoreWT.git
   f034f2e..488eca9  HEAD -> master
Branch master set up to track remote branch master from https://git.coding.net/yezhaoliang/offshoreWT.git.
[32mINFO [39m Deploy done: [35mgit[39m

```
### Gulp性能优化

[ npm gulp ][6]压缩css和html等

1. 全局安装gulp
```
npm install --global gulp

```

执行gulp -v ,然后 建立一个gulpfile.js文件，布置gulp任务

以后只要

```
hexo g  ## 简易生成
gulp   ## 压缩
hexo d  ## 发布

```

gulp使用[terser][7]替换掉老早之前的uglify,否则编译js不通过

``` js

var uglify = require('gulp-terser'); //不要用uglify了

```
### Next主题
[only deploy][5]

[1]: https://hexo-guide.readthedocs.io/zh_CN/latest/index.html 
[2]: https://fuhailin.github.io/%E5%9C%A8Hexo%E5%8D%9A%E5%AE%A2%E4%B8%AD%E6%8F%92%E5%85%A5%E5%9B%BE%E7%89%87%E7%9A%84%E5%90%84%E7%A7%8D%E6%96%B9%E5%BC%8F/
[3]: https://blog.csdn.net/sinat_37781304/article/details/82729029 
[4]:https://www.v2ex.com/t/264283 
[5]:https://spacejmmy.github.io/2017/08/20/2017-08-20-first-post/ 
[6]:https://hexo-guide.readthedocs.io/zh_CN/latest/advanced/[gulp]%E6%80%A7%E8%83%BD%E4%BC%98%E5%8C%96.html 
[7]:https://stackoverflow.com/questions/38886840/how-to-solve-this-minification-error-on-gulp/38886965 
