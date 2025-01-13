# git相关

1. git配置
   - 查看全局配置信息：git config --global --list
   - 设置全局配置信息：git config --global user.name "Your Name"；git config --global user.email "your@email.com"

2. git初始化和基本操作

   - 初始化：git init

   - 工作区---》暂存区：git add .

   - 暂存区---》本地仓库：git commit -m 'commit message'

   - 本地仓库---》远程仓库：push origin 

   - git 报红：

     - untracked files：没有被git识别管理的新增加的文件 
     - Changes not staged for commit：做修改了的没有被提交到暂存区的文件

   - 分支相关

     - git branch：查看分支
     - git branch new-branch：创建一个名为new-branch的分支 
     - git checkout branch-name：切换到branch-name分支
     - git checkout -b new-branch：新建并且切换到这个新分支上

   - 远程仓库操作 

     - 本地与远程仓库建立连接： git remote add origin_name  http://www.baidu.com
     - 推送本地仓库内容到远程仓库上 git push
     - 从远程仓库拉取内容 git pull

3. git处理冲突

   - 场景1：A从github远程仓库上拉了一个项目下来，B对项目进行了修改，并且重新推送到了远程仓库，同时A也对项目进行了一些修改，如何将A、B二者的代码合并？ 

     -  step1：从远程仓库拉取最新的项目下来

       git fetch origin

     - step2：查看冲突与差异

       git diff origin/远程分支 本地分支

     - step3：合并远程更新到本地&解决冲突

       git merge origin/远程分支

     - step4：提交解决冲突后的修改

       git add .

     - step5：提交修改

       git commit -m "remark"

     - step6：推送到远程仓库 

       git push origin 本地分支名 