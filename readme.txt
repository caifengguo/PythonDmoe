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












































