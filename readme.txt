 Git 学习总结
 1.安装git之后，通过git config --global user.name "my name"
                    git config --global user.email "email@example.com"
 初始配置git
 2.mkdir cd pwd 等命令与unix类似
 3.cd newfile 之后，通过 git init 来初始化仓库（空的）
 4.通过 git add filename 来把改动添加到缓存区
 5.通过 git commit filename -m "what you changed" 把改动提交到仓库
 6.通过 git status 查看当前缓存区状态
 7.通过 git diff filename 查看改动内容
 8.通过 git log 查看历史版本记录 （加 --pretty=oneline 参数单行显示）
 9.通过 git reset --hard HEAD^ 回退到上一版本 （HEAD~n）
 10.通过 cat filename 查看内容
 11.通过 git reset --hard (commit id) 回到指定id版本
 12.通过 git reflog 查看命令历史
 13.工作区：本地；缓存区：stage；版本库：repo；
 14.通过 git checkout -- filename 回撤到最近一次 add 或 commit 的版本（丢弃工作区的修改）
 15.通过 git reset HEAD filename 撤销缓存区的修改（即回到add前的状态，HEAD表示最新版本）
 16.通过 rm filename 移除本地文件
 17.通过 git rm filename　移除版本库文件
 18.通过 git checkout -- filename 用版本库里的版本替换工作区的版本
 19.通过 ssh-keygen -t rsa -C "youremail@example.com" 创建SSH key
 20.通过 git remote add origin git@github.com:username/reponame.git 关联远程库
 21.通过 git push -u origin master 推送master分支所有内容（第一次）
 22.通过 git push origin master 推送（第二次及以后）
 23.通过 git remove rm origin 删除远程的orgin
 24.通过 git clone git@github.com:username/reponame.git 克隆一个仓库到本地
 25.master 为主分支，head 为当前分支
 26.分支改动，未提交之前，master不变；合并之后，master指向分支末端
 27.通过 git checkout -b dev (-b 表示创建并切换到新分支）
 28.通过 git branch dev 创建；通过 git checkout dev 切换
 29.通过 git branch 查看所有分支，当前分支前面会有*号
 30.通过 git merge dev 合并分支到 master 上
 31.通过 git branch -d dev 删除 dev 分支
 32.通过 git log --graph 看到分支合并图
 33.通过 git merge --no-ff -m "***" dev 进行普通模式合并
 34.如果正在 dev 分支上进行操作，而要修改 master 分支上的内容，而 dev 上的又不能 add ，可以用 git stash 保存工作现场；
    用 git stash list 查看保存目录，用 git stash pop 恢复工作区
 35.通过 git branch -D <name> 强行删除未合并过的分支
 36.通过 git remote 查看远程库信息
 37.通过 git push origin dev 推送 dev 分支到 origin
 38.其他人克隆分支到本地后，通过 git branch -b dev dev/origin 创建origin的dev分支到本地
 39.通过 git pull 抓取远程的分支
 40.多人协作的工作模式通常是这样：
    首先，可以试图用git push origin branch-name推送自己的修改；
    如果推送失败，则因为远程分支比你的本地更新，需要先用git pull试图合并；
    如果合并有冲突，则解决冲突，并在本地提交；
    没有冲突或者解决掉冲突后，再用git push origin branch-name推送就能成功！
    如果git pull提示“no tracking information”，则说明本地分支和远程分支的链接关系没有创建，用命令git branch --set-upstream branch-name origin/branch-name。
 41.通过 git tag <name> 打标签，git tag 查看标签， git tag <name> <commit id> 在对应修改id上打标签
 42.通过 git show <tagname> 获取标签信息
 43.通过 git tag -d <tagname> 删除本地标签
 44.通过 git push origin <tagname> 推送一个标签
 45.通过 git push origin --tags 推送全部标签
 46.通过 git push origin :refs/tags/<tagname> 删除远程标签
 
 从 http://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000/ 中总结
