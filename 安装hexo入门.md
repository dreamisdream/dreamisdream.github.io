
##  安装 nodejs npm 

sudo apt-get install nodejs
sudo apt-get install npm

##  安装 hexo-cli

sudo npm install hexo-cli -g

hexo init 博客名称

hexo g 编译
hexo s 部署
hexo d 上传


## 修改git仓库地址并上传 

deploy:
  type: git
  repository: https://github.com/dreamisdream/dreamisdream.github.io.git
  branch: master



## 替换主题
下载主题到themes下
修改 theme 的值

## 开发分支初始化操作
npm install
npm install hexo-deployer-git --save


## 常见问题

error：spawn failed...

### 解决办法

删除.deploy_git文件夹;
输入git config --global core.autocrlf false
然后，依次执行：
hexo clean
hexo g
hexo d



## 其它
npm install hexo -g #安装Hexo
npm update hexo -g #升级
hexo init #初始化博客

命令简写
hexo n "我的博客" == hexo new "我的博客" #新建文章
hexo g == hexo generate #生成
hexo s == hexo server #启动服务预览
hexo d == hexo deploy #部署

hexo server #Hexo会监视文件变动并自动更新，无须重启服务器
hexo server -s #静态模式
hexo server -p 5000 #更改端口
hexo server -i 192.168.1.1 #自定义 IP
hexo clean #清除缓存，若是网页正常情况下可以忽略这条命令

