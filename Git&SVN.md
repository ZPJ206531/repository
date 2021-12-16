# Git

在工作中使用Git和SVN两种版本控制工具，因此做个记录。

**Git官方文档：https://git-scm.com/book/en/v2**

## Git初始化

在文件夹中执行如下命令，即可创建本地git仓库。文件夹中生成“.git“隐藏目录。

```
git init
```

## Git配置

"git config"，则是git进行基础配置，包括Git外观和基础行为

```
git config --list --show-origin
```

Git包含三个层级的配置文件。

1. 针对系统中每个用户及仓库的通用配置，文件目录为“/etc/gitconfig”
2. 针对当前用户，目录为下载路径/.gitconfig或~/.config/gitconfig文件
3. 针对当前仓库，目录为.gitconfig。

以上三个级别，每个级别都会覆盖上一个级别的设置，可通过如下命令查看所有的配置和文件路径

```
git config --list --show-origin
```

### 用户信息

初始化设置之后，需要设置用户名和邮件地址

```
git config --global user.name "***"
git config --global user.email ***@**.com
```

### 获取帮助

```
git help <verb>
git <verb> --help
man git-<verb>
git help config
```

## GIt基础操作

```
git clone url
git clone url abc
git add "文件名"
git commit -m "添加信息" //提交更新，并添加“信息"
git commit -a //跳过暂存区域，直接提交代码
git status //显示仓库的状态信息
git status -s //逐行显示状态信息
git diff //查看全部修改内容，比较当前文件和暂存区域的差异
rm filename //从工作目录中移除某文件
git rm 文件名 //记录移除操作
rm -f filename // 强制移除某文件


```

## Git机制

![lifecycle](C:\Users\user\Desktop\lifecycle.png)

### git忽略文件

在本地git仓库中建立一个.gitignore的文件，于其中写入需要忽略的文件类型，如下：

```
$ cat .gitignore
*.[oa]  //忽略oa类型的文件
*~ //忽略~文件
```

.gitignore文件格式如下：

- 所有空行或者以 `#` 开头的行都会被 Git 忽略。
- 可以使用标准的 glob 模式匹配，它会递归地应用在整个工作区中。
- 匹配模式可以以（`/`）开头防止递归。
- 匹配模式可以以（`/`）结尾指定目录。
- 要忽略指定模式以外的文件或目录，可以在模式前加上叹号（`!`）取反。



































# SVN