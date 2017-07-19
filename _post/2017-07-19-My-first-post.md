#这是文章的标题

文章的段落内容

获取Git的帮助信息

```
git help

```

配置用户信息

```
git config --global user.name   "WZL"
git config --global user.emall  "123456789@qq.com"

```

初始化仓库

```

git init 

```

这个命令会帮我们在目录下创建一个隐藏的`.git`文件夹

创建一个`MyFile.txt`文件

```
echo Hello Git! > MyFile.txt

```

将文件放到**暂存区**中

```
git add MyFile.txt

```

将暂存区中的内容提交到仓库

```
git commit MyFile.txt --message "This is my first commit"

```

将文件从暂存区移除

```
git rm --cached MyFile.txt

```


将文件
#Git本地操作

##文件状态

我们在工作目录中创建的文件或从其他地方拷贝过来的文佳，这些文件的初始状态是**untracked**,这意味着Git知道我们新添加了一些文件，但是Git不会跟踪这些文件的改变。如果你想让Git跟踪记录这些文件的变化，必须使用`add`命令添加他们。这些文件一旦被添加，他们的状态就变成了**unmodified**，这表示这些文件准备着被提交，或者说已经被放倒暂存区里面了。如果说这个时候我们修改了已经被添加到暂存区中的文件，那么他的状态将会变成**modified**。

##暂存区

暂存区中放的都是等待被提交的文件。如果想把新创建的文件或修改过的文件添加到暂存区，必须使用`git add` 命令。如果我们不小心讲一个文件放到了暂存区中，那么我们怎样将它从暂存区中移除呢？

###从暂存区中移除文件

使用`git reset HEAD<file>`命令可以将文件从暂存区移除，被移除的文件将变成未被跟踪的状态**untracked**。

>注意：在使用`git reset`命令时一定要小心，如果使用不当的话，会破坏现在所做的工作，因此不要随意使用。

从暂存区中移除文件的另一种方式是使用`git rm --cached<file>`命令。`--cached`选项只是将文件从暂存区中移除，并不会删除文件本身。

如果被移除的文件已经提交到仓库中，`git rm`命令只会将改文件标记为删除，


#分支                            
```
git branch  secondbranch

```
 
切换分支
```
git checkout secondbranch

```
