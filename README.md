# git-study
初学git用到的一些比较常用的命令

git全局配置 <br/>
git config -global git config -global user.name "yourname" <br/>
git config -global user.email "youremail"<br/>
cd G: cd www mkdir gitTest pwd(该命令用于显示当前目录) =>表示G盘www目录下新建一个gitTest版本库<br/>
git init 通过git init把这个目录变成git可以管理的仓库<br/>
第一步、git add 文件名 使用命令 git add 添加到暂存区里面去<br/>
第二步、git commit -m "这里填写注释" 用命令 git commit 告诉Git，把文件提交到仓库<br/>
git status 通过命令git status来查看是否还有文件未提交<br/>
git diff 文件名 通过git diff命令来查看文件到底改了什么内容<br/>
版本回退 <br/>
git log <br/>
通过git log命令查看下历史记录 q可以退出 <br/>
git log命令显示从最近到最远的显示日志 如果嫌上面显示的信息太多的话，我们可以使用命令 <br/>
git log –pretty=oneline<br/>
现在我想使用版本回退操作，我想把当前的版本回退到上一个版本，要使用什么命令呢？可以使用如下2种命令， <br/>
第一种是： git reset –hard HEAD^ 那么如果要回退到上上个版本只需把HEAD^ 改成 HEAD^^ 以此类推。<br/>
那如果要回退到前100个版本的话，使用上面的方法肯定不方便，我们可以使用下面的简便命令操作：<br/>
git reset –hard HEAD~100 即可。<br/>
cat 文件名 通过命令cat命令查看文件内容<br/>
git reflog git reflog命令获取到版本号 git reset –hard 版本号=>回复到该版本号<br/>
我们前面说过使用Git提交文件到版本库有两步：<br/>
第一步：是使用 git add 把文件添加进去，实际上就是把文件添加到暂存区。<br/>
第二步：使用git commit提交更改，实际上就是把暂存区的所有内容提交到当前分支上。<br/>
撤销修改 命令 git checkout –- 文件名 删除文件 rm 文件名<br/>
git push origin master 把本地master分支的最新修改推送到github上了<br/>
git clone 地址<br/>
git checkout -b dev 创建并切换分支<br/>
git branch 查看当前分支<br/>
git merge dev 在master分支上合并dev分支内容<br/>
git branch -d dev 删除dev分支<br/>
git branch 查看分支的命令<br/>
总结创建与合并分支命令如下：<br/>
查看分支：git branch<br/>
创建分支：git branch name<br/>
切换分支：git checkout name<br/>
创建+切换分支：git checkout –b name<br/>
合并某分支到当前分支：git merge name<br/>
删除分支：git branch –d name<br/>
