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
 20.通过 git remove add origin git@github.com:username/reponame.git 关联远程库
 21.通过 git push -u origin master 推送master分支所有内容（第一次）
 22.通过 git push origin master 推送（第二次及以后）
 23.通过 git remote rm origin 删除远程的orgin
 24.
 
