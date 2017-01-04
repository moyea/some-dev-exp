#NPM一些常用命令
##npm查看全局安装过的包:

    $ npm list -g --depth 0

##清空npm缓存:

    $ npm cache clean
##查看npm源:

    $ npm config get registry
##临时切换npm源

    $ npm config set registry https://registry.npm.taobao.org
##设置可以查看npm进度:

    $ npm config set loglevel=http
