#git
##1.Git 介绍
###1.1 版本控制 version control
主流版本控制器：

- Git
- SVN
- VSS
- CVS

版本控制：

- 本地版本控制
- 集中式版本控制
  <small>所有版本放在服务器上，用户本地只有自己以前所同步的版本，SVN。</small>
- 分布式版本控制  
   <small>每个人拥有全部代码，可在本地查看所有版本历史，可以离线在线提交。Git</small>

###1.2 Git History
Linus Benedic Torvalds

##Git 环境配置
跟视频
（环境变量只是为了全局使用，默认会配上） ##基本 Linux 命令

rm-rf 删库跑路

所有配置文件都保存在本地
##Git 必要配置

###1.配置用户和邮箱
git config --global user.name "yusiquweierwang\*\*\*\*"
git config --global user.email "fefefe@qq.com"

git/etc/gitconfig 文件

```git
[diff "astextplain"]
	textconv = astextplain
[filter "lfs"]
	clean = git-lfs clean -- %f
	smudge = git-lfs smudge -- %f
	process = git-lfs filter-process
	required = true
[http]
	sslBackend = openssl
	sslCAInfo = D:/environment/Git/mingw64/ssl/certs/ca-bundle.crt
[core]
	autocrlf = true
	fscache = true
	symlinks = false
	editor = \"D:\\\\Microsoft VS Code\\\\bin\\\\code\" --wait
[pull]
	rebase = false
[credential]
	helper = manager-core
[credential "https://dev.azure.com"]
	useHttpPath = true
[init]
	defaultBranch = master
```

C 盘用户下.config 也有用户配置

##Git 核心 ###工作区域
三个工作区域：

- 工作目录（working directory），平时存放代码的地方。
- 暂存区（stage/index),临时文件，保存即将提交到文件列表信息。
- 资源库（repository or git directory).安全存放数据的位置，里面有提交到所有版本的数据，HEAD 指向最新放入仓库的版本。
- remote 远程仓库

ref:/cefs/heads/master <-主分支

###git 工作流程： 1.在工作目录中添加，修改文件 2.将需要进行版本管理的文件放入暂存区域（git add.) 3.将暂存区文件提交到 git 仓库（git commit).

##Git 项目搭建
（搞张图）

项目创建
1）本地仓库搭建：git init 2) 克隆远程目录，将远程服务器上的仓库完全镜像一份到本地。

##Git 文件操作
文本 4 状态

- untracked:未跟踪
- unmodify:文件已入库

查看文件状态

```
查看指定文件状态
git status [filename]

查看所有文件状态
git status

##git add 添加文件到暂存区
##git commit -m 提交暂存区文件到本地仓库 -m 提交信息


```

##使用码云 1.设置本机绑定 SSH 密钥，实现免密登录

2.将公钥信息 public key 添加到码云账户 3.用码云创造自己的仓库。

克隆到本地

##IDEA 中集成 git
