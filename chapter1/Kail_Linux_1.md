# GitBook.com

[Gitbook.com](www.github.com)是一个围绕gitbook发行书籍的社区, 于2014年初创, GitBook.com提供免费和付费的服务, 而且免费账户就可以享受诸多服务, 包括:

- 一本私有书籍
- 托管不限数量的公开书籍
- 售卖不限数量的书籍, 并分享80%的书籍收入
- 不限数量的协作者
- 免费的在线书籍编辑器

对于普通用户来说，免费账号就已经足够用了, 因为虽然限制为1本私有书籍, 但没有限制书籍的大小, 所以对于个人的学习来说非常适合, 用户甚至可以将所有知识归类放入一本私有书籍中! 当然, **GitBook.com** 限制私有书籍数量但不限制公开书籍数量的政策, 显然是鼓励用户能够共享知识!

# New Books
----
要使用**GitBook.com**来托管你的书籍, 首先需要注册一个账号, 免费注册后, 用户也可以选择升级为付费用户, 享受更多的服务.

登录[**GitBook.com**](www.gitbook.com)后, 在用户界面, 可以管理现有书籍, 如下图:
![GitBook书籍管理界面](http://7xp79m.com1.z0.glb.clouddn.com/%60%25O%7DW%7BKFC%25BEC$NK_%5BL6~@X.png)

目前有4种书籍主题可以选择, 这里以默认的 `Basic` 主题为例，输入书籍名字后, 点击"Create book", 完成书籍的创建.

创建完成后, 就会进入书籍属性界面, 如图所示:
![书籍属性管理界面](http://7xp79m.com1.z0.glb.clouddn.com/test.png)

这里可以进行对书籍的各项属性进行配置, 例如:

- 编辑书籍(Edit Book)
- 书籍主题(Theme)
- 绑定 GitHub(GitHub)
- 绑定域名(Domain Names)

等.

以上几个配置将在后面介绍, 其它的配置比较简单,请自行探索！


# Edit Book
******
在创建了书籍后，可以使用免费的在线编辑器进行编辑, 也可以使用[gitbook editor](https://github.com/GitbookIO/editor)编辑, 甚至使用任何喜欢的文本编辑器来编辑, 例如: `Vim`.

## 在线编辑
----
进入书籍的属性页面后, 点击"Edit Book"按钮即可打开在线编辑器.

GitBook 的在线编辑器对于国内用户来说, 很可能不能访问, 所以还是做好下载gitbook editor到本地, 安装后使用, 或者使用自己喜欢的文本编辑器进行编辑.

## GitBook Editor
-----
gitbook editor 实际上就是一个本地应用版的在线编辑器, 使用方式和在线编辑器类似, 所见即所得, 这里不再介绍, 读者可以参考[gitbook 使用](http://www.chengweiyang.cn/basic-usage/README.html)中的内容.

## Git & Markdown
----
另一种方式, 就是直接使用文本编辑器, 编写Markdown文档, 然后使用Git提交到书籍的远程项目, 当然, 提交前, 最好在本地使用gitbook 预览下过, 提交后, Gitbook.com会自动生成新书籍的内容.

### Colen source of book
----
GitBook.com 上的每本书都使用Git项目来管理, 所以, 这里首先需要克隆需要编辑书籍的Git项目, 登录GitBook.com后, 跳转到书籍的属性页面, 如下图所示:
![](http://7xp79m.com1.z0.glb.clouddn.com/%60%25O%7DW%7BKFC%25BEC$NK_%5BL6~@X.png)

下面是在线编辑器的截图:
![gitbook在线编辑器](http://7xp79m.com1.z0.glb.clouddn.com/%E4%B8%AAitbook_editor.png)

使用如下命令, 克隆书籍的源代码:

```
$ git clone https://git.gitbook.com/chengweiv5/test.git
Cloning into 'test'...
remote: Counting objects: 28, done.
remote: Compressing objects: 100% (17/17), done.
remote: Total 28 (delta 6), reused 28 (delta 6)
Unpacking objects: 100% (28/28), done.
Checking connectivity... done.

$ cd test/

$ ls
README.md  SUMMARY.md

$ git log --oneline 
07bde6c Cleanup example
6d368db Add _book to gitignore
20779f5 Add explanation in README.md
1b5b1a6 Create chapter-1/ARTICLE1.md
77b1858 Add help message in SUMMARY.md
210e3fe Create chapter-1/README.md
5570112 Create SUMMARY.md
2a8a0c3 Initial commit
```

可以看到, 创建好的书籍默认已经创建了一些内容, 但是这些内容是还没有发布的, 所以其他人不能阅读!

### Edit content
----
现在, 可以参考 [gitbook 使用](http://www.chengweiyang.cn/basic-usage/README.html)中的内容来编辑书籍内容, 使用 gitbook init, gitbook serve 来预览, 完成后, 可以提交修改:

`$ git commit -asm "init book"`

### Publiction
-----
最后, 提交到远程的Git项目:

```
$ git push 
Counting objects: 3, done.
Delta compression using up to 4 threads.
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 362 bytes | 0 bytes/s, done.
Total 3 (delta 1), reused 0 (delta 0)
To https://git.gitbook.com/chengweiv5/test.git
   07bde6c..b6a8b3f  master -> master
```

### Read Book
----
提交到GitBook.com后, 书籍就自动发布了, 用户就可以通过书籍的地址访问了.



