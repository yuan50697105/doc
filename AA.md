# git 使用

1. 初始化本地仓库 git init
2. 关联远程仓库 git remote add xxx（本地映射别名） xxxx(远程地址，git 支持 http 和 ssh两种方式，建议使用ssh)
3. 添加文件到版本控制 git add . (git 会自动遍历子目录)
4. 提交文件 git commit -m 提交信息
5. 推送到远程仓库 git push 远程仓库别名 本地分支名称:远程分支名称
6. ignore 文件（自动忽略文件）.gitignore
7. git 多远程仓库（git本身是分布式储存 可以一个本地关联多个远程）
8. 分支相关
   1. 检出分支 git checkout -b 分支别名  远程仓库别名/远程分支
   2. 推送新分支，在检出分支基础上 使用 git push -u 远程仓库别名 分支名称