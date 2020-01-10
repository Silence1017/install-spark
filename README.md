# 简介
My name is bighead.
下面是我安装spark遇到的问题，大家可以借鉴借鉴。

# 问题及解决方法
1.Linux系统登陆新建用户时，shell开头为$，不显示用户名和路径的解决方法
    https://blog.csdn.net/Du_wood/article/details/84914759
    原因：未给该用户指定shell

2.Scala安装过程中环境变量配置问题
    Linux系统配置用户环境变量：
    https://blog.csdn.net/flw8840488/article/details/90513873
    配置scala环境变量代码行：
    #scala environment
    export SCALA_HOME=/usr/local/scala
    export PATH=${SCALA_HOME}/bin:$PATH
    对于scala来说，单独修改适用于全局用户的/etc/profile或/etc/bash_bashrc是没用的，只能起到暂时有效的效果。
    所以我们应该对每个用户的~/.bashrc文件进行修改，才能保证每个用户正常执行scala -version命令。
    修改后执行source ~/.bashrc 命令，成功生效。

3.安装Spark非常完整的教程链接：
    https://blog.csdn.net/weixin_42001089/article/details/82346367
