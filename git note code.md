# git常用命令代码

1. cd切换当前命令目录

2. ls (linux) 或 dir (windows) : 查看当前目录所包含的内容

3. mkdir : 创建新文件夹

4. touch : 创建新文件

5. cat : 查看文件内容

6. clear : 清屏

7. history: 列出历史命令

8. 当记不太清文件名是,按Tab进行文件名提示

9. 按上下箭头查看历史命令

10. git clone [HTTPS/SSH] : 将远程仓库克隆到本地文件夹中

11. git pull origin 分支 : 拉取远程仓库进行更新

# 远程推送到github仓库上

1. git status : 先查看本地代码的状态

2. git conifg --global user.name "github上面的名称"(告诉github你的名字)

3. git conifg --global user.email "github上面的电子邮箱地址"(github你的电子邮箱)

4. git add . : 把文件夹所有文件放到暂存区中(也可以不写"."直接写文件名)

5. git commit -m "提交注释信息" : 把暂存区的文件放到历史区(打个版本)

6. git push origin 分支 [-u] : 把本地历史区推送到github仓库里面

## 把本地文件夹推送到github仓库上面

1. git init : 把本地文件夹变成git仓库

2. 然后同上1~5步(2和3步可以省略)

3. git remote add origin 远程仓库的链接(https)

4. git push origin 分支 [-u] : 把本地历史区推送到github仓库里面

# 版本回退和前进

1. git log : 查看版本日志 q退出

2. git log --pretty=oneline : 版本号完整且在一行显示

3. git log --oneline : 版本号简写在一行显示

4. git reflog : 显示每一次版本改变操作记录和索引

5. git reset [--hard|--mixed|--soft] [HEAD^|HEAD~n|版本号]

>以下是参数解释

6. 参数:--hard 强制移动版本库中的HEAD指针,并且改变暂存区和工作区内容(严格的版本改变)

7. 	    --mixed 只移动版本库中的HEAD指针,并且改变暂存区内容,工作区不变
 	    
9. 	    --soft 只移动版本库中的HEAD指针,暂存区和工作区内容不变

10. git reset --hard HEAD^ : 版本库HEAD指针回退一次(有几个^回退几次)

11. git reset --hard HEAD~n : 版本库HEAD指针回退n次(以上只用与版本回退)

12. git reset --hard 版本号 : 版本库HEAD指针指向特定版本号的版本(可用于版本的回退与前进)

# 当远程仓库改变时,push推送失败怎么解决

1. git pull origin master : 先获取最新的仓库版本

2. :q退出vim编辑

3. git push origin master : 向远程仓库推送即可

4. 如果上一步推送失败可能是合并的问题,git status 检查检查是不是有文件还没有添加的版本库中,添加了在重服第3步