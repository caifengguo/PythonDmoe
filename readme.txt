һ���ύ��Ա��Ϣ����

1�������ύ��Ա��Ϣ
git config --global user.name "guocaifeng"

git config --global user.email "guocaifeng@email.com"

2���鿴������Ϣ
git config user.name

git config user.email


����git init
����.git�ļ�(�����ļ���)�����ļ�Ϊ������ļ�


git  status    ==>�鿴״̬

����git add main.cpp   ==������ļ���git add . === ��Ӷ���ļ���

    git commit -m "��־"

�ġ�git diff

�塢 git diff --cached

���� git diff HEAD

�鿴��־  
   git log --oneline


����ǰ����־���ϴκϲ�Ϊͬһ��
git commit --amend --no-edit

���add��ͨ��reset��ع���modify״̬
git reset main.cpp


���commit�󣬻ع���֮ǰĳ���汾
git reset --hard HEAD~2
git reset --hard �汾id


�鿴���в�����־
git reflog


���ص��°汾
git reset --hard  �汾id
git reset --hard  HARD@{0}


��Ե����ļ��ص���ȥ�Ĳ���
git  checkout �汾id --�ļ���

git  checkout  ��֧��    ====�л���֧


�鿴���з�֧ͼ��
git log --oneline  --graph



#########��֧
//������֧
git branch dev

//�鿴��֧
git branch

�л�����֧
git checkout dev

ɾ����֧
git checkout -d dev

������֧ͬʱ�ƶ�����֧
git  checkout -b dev


���ͬʱ�ύ�汾
git commit -am ""



######����֧�Ƶ�master
1������master��
2��git merge --no--ff -m ���� dev
    git merg dev





*******���ֳ�ͻ��Ҫ�ֶ����д���
######��֧��ͻ
git rebase
git rebase --continue
git rebase --skip
git rebase --abort



###��ʱ�ļ�����
//�ݴ��ļ�
git stash 
//���ݴ��ļ��ָ�
git stash pop



//git     =====>���ع����
//github  =====>���߹����



#####��Զ�ֿ̲��ύ�汾
1������Git��user name��email

git config --global user.name "yourname"
git config --global user.email "youremail"


2������SSH��Կ
  ssh-keygen -t rsa -C ��haiyan.xu.vip@gmail.com��

  ���õ��������ļ���id_rsa��id_rsa.pub

3����github�����ssh��Կ����Ҫ��ӵ��ǡ�id_rsa.pub������Ĺ�Կ��
   ��https://github.com/,�������������Կ

4�������ύ����












































