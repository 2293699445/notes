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

     

     

     