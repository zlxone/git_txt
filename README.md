# git_txt 简述

-----git操作-----
第一次提交 :
方案一 : 本地创建项目根目录, 然后与远程GitHub关联, 之后的操作一样;
-- 初始化Git仓库 :Git init ;
-- 提交改变到缓存 :git commit -m 'description' ;
-- 本地git仓库关联GitHub仓库 : git remote add origin git@github.com:han1202012/TabHost_Test.git ;
-- 提交到GitHub中 : git push -u origin master ;


方案二 : 方案二就是不用关联GitHub仓库, 直接从GitHub冲克隆源码到本地, 项目根目录也不用创建;
-- 从GitHub上克隆项目到本地 :git clone git@github.com:han1202012/NDKHelloworld.git , 注意克隆的时候直接在仓库根目录即可, 不用再创建项目根目录 ;
-- 添加文件 :git add ./* ;

-- 提交缓存 :git commit -m '提交';
-- 提交到远程GitHub仓库 : git push -u origin master ;
之后修改提交 :
-- 与GitHub远程仓库同步 :git pull ;
-- 查看文件变更 : git status ;
-- 提交代码到本地缓存 : git commit -m 'description';
--提交代码到远程GitHub仓库 :git push ;


参考：http://blog.csdn.net/free_wind22/article/details/50967723

1、git init 把这个目录变成git可以管理的仓库

2、git add readme.txt添加到暂存区里面去

3、用命令 git commit告诉Git，把文件提交到仓库

3.1、git remote add origin https://github.com/tugenhua0707/testgit.git 关联仓库

3.2、git push -u origin master 把本地库的内容推送到远程，由于远程库是空的，第一次推送master分支时，加上了 –u参数

4、通过命令git status来查看是否还有文件未提交

5、git diff readme.txt 查看改了什么内容

6、查看下历史记录信息
git log 

7、回退版本
第一种是：git reset  --hard HEAD^ 那么如果要回退到上上个版本只需把HEAD^ 改成 HEAD^^
如果要回退到前100个版本的话：git reset  --hard HEAD~100

8、命令 git checkout --readme.txt 意思就是，把readme.txt文件在工作区做的修改全部撤销，
这里有2种情况，如下：readme.txt自动修改后，还没有放到暂存区，使用 撤销修改就回到和版本库一模一样的状态。另外一种是readme.txt已经放入暂存区了，接着又作了修改，撤销修改就回到添加暂存区后的状态。


9、多人协作工作模式一般是这样的：
首先，可以试图用git push origin branch-name推送自己的修改.
如果推送失败，则因为远程分支比你的本地更新早，需要先用git pull试图合并。
如果合并有冲突，则需要解决冲突，并在本地提交。再用git push origin branch-name推送。

