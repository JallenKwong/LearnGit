# 回答一 #

	$ git push origin

上面命令表示，将当前分支推送到origin主机的对应分支。

	$ git push

如果当前分支与多个主机存在追踪关系，那么这个时候**-u选项会**指定一个默认主机，这样后面就可以不加任何参数使用git push。

	$ git push -u origin master

上面命令将本地的master分支推送到origin主机，同时指定origin为默认主机，后面就可以不加任何参数使用git push了。

不带任何参数的git push，默认只推送当前分支，这叫做simple方式。此外，还有一种matching方式，会推送所有有对应的远程分支的本地分支。Git 2.0版本之前，默认采用matching方法，现在改为默认采用simple方式。


# 回答二 #

The -u tells Git to remember the parameters, so that next time we can simply run git push and Git will know what to do.

相当于第一次串门的时候你登了个记办了个vip。。以后再来就知道是你来了。不用脱裤子搜身了

