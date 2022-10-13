# valgrind_src

backup valgrind tool source

link: https://valgrind.org/downloads/

######################################################################################################################################
关于高版本的valgrind不可运行问题

valgrind: failed to start tool 'memcheck' for platform 'amd64-linux': No such file or directory

这里的解决方案是：

确定你的valgrind安装路径，如果安装时默认在解压缩包后直接执行./configure，那么这里默认将每个模块安装到/usr/local下

/usr/local/bin valgrind相关可执行程序
/usr/local/include/valgrind
/usr/local/lib/valgrind
/usr/local/libexec/valgrind
1
2
3
4
在~/.bashrc中添加：

export VALGRIND_LIB=/usr/local/libexec/valgrind
1
然后执行source ~/.bashrc即可

执行valgrind --version可以查看到valgrind版本即成功！

原文链接：https://blog.csdn.net/weixin_43900869/article/details/124015870

###########################################################################################################################################
