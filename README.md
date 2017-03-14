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

