#MacOs下Homebrew的使用
##安装Homebrew

    /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
##查看Homebrew安装过的包

    brew list 
##查看安装包中的内容

    brew list mysql
##使用Homebrew安装mysql
    
    brew install mysql
默认安装的没有密码，可以使用

    mysql_secure_installation
来设置root用户的密码，之后可以通过

    mysql -u root
来链接数据库
##开启mysql

    [sudo] mysql.server start
##关闭mysql

    mysql.server stop
##将mysql添加为自启动的服务

    brew services start mysql
##停止mysql服务
    
    [sudo] brew services stop mysql
##查看brew添加过的服务

    brew services list
##查看brew services命令的帮助

    brew services
