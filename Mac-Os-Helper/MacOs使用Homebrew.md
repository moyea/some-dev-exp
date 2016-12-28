#MacOs使用Homebrew
##Homebrew介绍
官方网站:[http://brew.sh](http://brew.sh)  
Homebrew是Mac系统的包管理器，类似yum、rpm等工具
##安装Homebrew

    $ /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

##Homebrew安装组件的位置
Homebrew会将组件安装到独立目录(/usr/local/Cellar),并将文件软链接至 /usr/local 
