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




###################����ssh key�C��ȫ����
ʹ��git bash/git cmd ����(git bash Ϊ�� )

����git��user.name��user.email
$ git config --global user.name "yxzhong"
$ git config --global user.email "your email"


�鿴�Ƿ��Ѿ�����ssh key�Ƿ����
$ cd ~/.ssh
1
�C> ���û������ʾ�� No such file or directory 
�C> ����������~/.ssh·���£�ls�鿴��ǰ·���ļ���rm * ɾ�������ļ��������µ�ssh key

����ssh key
cd ~ //������"~"Ŀ¼��
$ ssh-keygen -t rsa -C "xxxxxx@yy.com"//��д��ʵ������
Generating public/private rsa key pair.
Enter file in which to save the key (/c/Users/xxxx_000/.ssh/id_rsa):   #����ֱ�ӻس�
Enter passphrase (empty for no passphrase):   #�������루����Ϊ�գ�
Enter same passphrase again:   #�ٴ�ȷ�����루����Ϊ�գ�
Your identification has been saved in /c/Users/xxxx_000/.ssh/id_rsa.   #���ɵ���Կ
Your public key has been saved in /c/Users/xxxx_000/.ssh/id_rsa.pub.  #���ɵĹ�Կ


���ssh key��github
��>��github��Settings��SSH kyes��Add SSH key

�C>1. ����c:/Users/xxxx_000/.ssh/Ŀ¼�£���id_rsa.pub�ļ���ȫѡ���ƹ�Կ���� 
�C>2. Title�Զ��壬����Կճ����GitHub��Add an SSH key��key��������Add Key��

����ssh key�Ƿ����óɹ�
$ ssh -T git@github.com
The authenticity of host 'github.com (192.30.252.129)' can't be established.
RSA key fingerprint is 16:27:xx:xx:xx:xx:xx:4d:eb:df:a6:48.
Are you sure you want to continue connecting (yes/no)? yes #ȷ�����Ƿ������ϵ������yes
Warning: Permanently added 'github.com,192.30.252.129' (RSA) to the list of known hosts.
Enter passphrase for key '/c/Users/xxxx_000/.ssh/id_rsa':  #����ssh kye������Ϊ�����޴�����������������д����ң���������ssh keyʱ���õ����뼴�ɡ�
Hi xxx! You've successfully authenticated, but GitHub does not provide shell access. #���ִʾ仰��˵�����óɹ�


#################��������Ŀpush��github(git cmdΪ��)

��git cmd ��·�����õ���Ŀ·��
��ʼ����Ŀ
git init

���Զ�ֿ̲�
git remote add origin git@github.com:michaelliao/learngit.git //���Լ��ĵ�ַ

###########push������Ŀ��Զ�ֿ̲�
git add . //������б��ش��뵽������
git commit -m "describe message"
git push -u origin master//originҲ�����Լ�����Զ�ֿ̲�����











































