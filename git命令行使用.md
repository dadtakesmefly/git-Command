

### git安装

### git帮助提示
	- git add --help     出现一个网页，git的使用提示
	


### git初始化一个仓库
  - 其实就是创建了一个.git隐藏目录
  - 命令:` git init `;
    + 想在哪个目录创建.git目录，就是哪个目录打开工具然后写命令.
    + 一般是在项目的根目录执行这个命令.


### 自报家门
  - 配置用户名 : `git config user.name "testName"`
  - 全局模式：`git config global user.name "testName"`
  - 配置邮箱   : `git config user.email "test@sina.com"`
  - 查看配置信息: `git config --list`


### 把代码提交到仓库中
  - 1.先把代码添加到暂存区(就相当于放到仓库门口)
    + 命令:`git add 文件路径`
    + 示例:`git add ./reademe.md`
    + 可以使用`git add .`这个命令，批量把当前目录下所有修改过的文件添加到暂存区。

  - 2.把暂存区的文件提交仓库里
    + 命令: `git commit -m "注释" `
    + 示例: `git commit -m "我们添加了一个新的功能"`
    + -m 表示指定一个字符串，作为提交的说明(相当于注释);

  - 合并add 与commit 命令
    + `git commit -a -m "这是使用合并添加与提交的操作"`;
    + 这里-a参数表明把所有修改后的文件一起添加到暂存区.(只是对修改后的文件有效，对于新添加的文件没有作用)


## github
### github与git
  - git 版本管理工具
  - github 就是一个网站，只是这个网站提供git服务器的功能


### 上传代码到git服务器(push)
  - 命令:`git push [远程服务器地址] [远程服务器的分支]`
     + 示例:`git push https://github.com/huoqishi/test002.git master`

  - 上传时可以使用一些简化的命令
    + 将远程服务器地址写成变量的形式
      * `git remote add [变量名]  [远程服务器地址]`
      * 示例:`git remote add origin https://github.com/huoqishi/test002.git`
      * 这样之后就可以直接使用origin来代替git push 后面写的地址了
        `git push origin master`
  - 还可以尽一步简化
    + 在push时加上-u参数，就会默认建立本地当前分支与远程指定分支的关联,下一次push时就不需要输入分支名了`git push origin`;

### 如果提交不了 先拉取在上传
![img](http://oibl5dyji.bkt.clouddn.com/TIM%E6%88%AA%E5%9B%BE20171011104323.png)


