node有一个模块叫n，是专门用来管理node.js的版本的。  
首先安装n模块： 

    npm install -g n
第二步：
升级node.js到最新稳定版

    sudo n stable
n后面也可以跟随版本号比如  

    n v0.10.26
或  

    n 0.10.26
几个npm的常用命令:

    npm -v                  #显示版本，检查npm 是否正确安装。
    npm install express     #安装express模块
    npm install -g express  #全局安装express模块 
    npm list                #列出已安装模块 
    npm list -depth=0       #显示当前目录下安装过的模块，不显示依赖 
    npm show express        #显示模块详情 
    npm update              #升级当前目录下的项目的所有模块 
    npm update -g           #升级全局所有安装过的模块 
    npm update express      #升级当前目录下的项目的指定模块 
    npm update -g express   #升级全局安装的express模块 
    npm uninstall express   #删除指定的模块 
