一、提交人员信息设置

1、设置提交人员信息
git config --global user.name "guocaifeng"

git config --global user.email "guocaifeng@email.com"

2、查看设置信息
git config user.name

git config user.email


二、git init
创建.git文件(隐藏文件夹)，该文件为管理库文件


git  status    ==>查看状态

三、git add main.cpp   ==》添加文件（git add . === 添加多个文件）

    git commit -m "日志"

四、git diff

五、 git diff --cached

六、 git diff HEAD

查看日志  
   git log --oneline


将当前的日志与上次合并为同一条
git commit --amend --no-edit

如果add后，通过reset则回滚到modify状态
git reset main.cpp


如果commit后，回滚到之前某个版本
git reset --hard HEAD~2
git reset --hard 版本id


查看所有操作日志
git reflog


返回到新版本
git reset --hard  版本id
git reset --hard  HARD@{0}


针对单个文件回到过去的操作
git  checkout 版本id --文件名

git  checkout  分支名    ====切换分支


查看所有分支图形
git log --oneline  --graph



#########分支
//创建分支
git branch dev

//查看分支
git branch

切换到分支
git checkout dev

删除分支
git checkout -d dev

创建分支同时移动到分支
git  checkout -b dev


添加同时提交版本
git commit -am ""



######将分支推到master
1、处于master上
2、git merge --no--ff -m “” dev
    git merg dev





*******出现冲突需要手动进行处理
######分支冲突
git rebase
git rebase --continue
git rebase --skip
git rebase --abort



###临时文件处理
//暂存文件
git stash 
//将暂存文件恢复
git stash pop



//git     =====>本地管理库
//github  =====>在线管理库



#####向远程仓库提交版本
1、设置Git的user name和email

git config --global user.name "yourname"
git config --global user.email "youremail"


2、生成SSH密钥
  ssh-keygen -t rsa -C “haiyan.xu.vip@gmail.com”

  最后得到了两个文件：id_rsa和id_rsa.pub

3、在github上添加ssh密钥，这要添加的是“id_rsa.pub”里面的公钥。
   打开https://github.com/,在设置中添加密钥

4、可以提交代码




###################创建ssh key–安全传输
使用git bash/git cmd 创建(git bash 为例 )

设置git的user.name和user.email
$ git config --global user.name "yxzhong"
$ git config --global user.email "your email"


查看是否已经存在ssh key是否存在
$ cd ~/.ssh
1
–> 如果没有则提示： No such file or directory 
–> 如果有则进入~/.ssh路径下（ls查看当前路径文件，rm * 删除所有文件）生成新的ssh key

生成ssh key
cd ~ //保持在"~"目录下
$ ssh-keygen -t rsa -C "xxxxxx@yy.com"//填写真实的邮箱
Generating public/private rsa key pair.
Enter file in which to save the key (/c/Users/xxxx_000/.ssh/id_rsa):   #不填直接回车
Enter passphrase (empty for no passphrase):   #输入密码（可以为空）
Enter same passphrase again:   #再次确认密码（可以为空）
Your identification has been saved in /c/Users/xxxx_000/.ssh/id_rsa.   #生成的密钥
Your public key has been saved in /c/Users/xxxx_000/.ssh/id_rsa.pub.  #生成的公钥


添加ssh key到github
—>打开github→Settings→SSH kyes→Add SSH key

–>1. 进入c:/Users/xxxx_000/.ssh/目录下，打开id_rsa.pub文件，全选复制公钥内容 
–>2. Title自定义，将公钥粘贴到GitHub中Add an SSH key的key输入框，最后”Add Key”

测试ssh key是否设置成功
$ ssh -T git@github.com
The authenticity of host 'github.com (192.30.252.129)' can't be established.
RSA key fingerprint is 16:27:xx:xx:xx:xx:xx:4d:eb:df:a6:48.
Are you sure you want to continue connecting (yes/no)? yes #确认你是否继续联系，输入yes
Warning: Permanently added 'github.com,192.30.252.129' (RSA) to the list of known hosts.
Enter passphrase for key '/c/Users/xxxx_000/.ssh/id_rsa':  #生成ssh kye是密码为空则无此项，若设置有密码则有此项且，输入生成ssh key时设置的密码即可。
Hi xxx! You've successfully authenticated, but GitHub does not provide shell access. #出现词句话，说明设置成功


#################将本地项目push到github(git cmd为例)

打开git cmd 将路径设置到项目路径
初始化项目
git init

添加远程仓库
git remote add origin git@github.com:michaelliao/learngit.git //你自己的地址

###########push本地项目到远程仓库
git add . //添加所有本地代码到缓冲区
git commit -m "describe message"
git push -u origin master//origin也可以自己命名远程仓库名称











































