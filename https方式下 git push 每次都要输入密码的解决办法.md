# https方式下 git push 每次都要输入密码的解决办法 #

https方式每次都要输入密码，按照如下设置即可输入一次就不用再手输入密码的困扰而且又享受https带来的极速

设置记住密码（默认15分钟）：

	git config --global credential.helper cache

如果想自己设置时间，可以这样做：

	git config credential.helper 'cache --timeout=3600'

这样就设置一个小时之后失效

长期存储密码：

	git config --global credential.helper store
增加远程地址的时候带上密码也是可以的。(推荐)

	http://yourname:password@git.oschina.net/name/project.git
补充：使用客户端也可以存储密码的。

如果你正在使用ssh而且想体验https带来的高速，那么你可以这样做： 切换到项目目录下 ：

	cd projectfile/
移除远程ssh方式的仓库地址

	git remote rm origin
增加https远程仓库地址

	git remote add origin http://yourname:password@git.oschina.net/name/project.git