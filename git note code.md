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

11. git pull origin 分支  : 拉取远程仓库进行更新

# 远程推送到github仓库上

1. git status : 先查看本地代码的状态

2. git conifg --global user.name "github上面的名称"(告诉github你的名字)

3. git conifg --global user.email "github上面的电子邮箱地址"(github你的电子邮箱)

4. git add . : 把文件夹所有文件放到暂存区中(也可以不写"."直接写文件名)

5. git commit -m "提交注释信息" : 把暂存区的文件放到历史区(打个版本)

6. git push origin 分支 : 把本地历史区推送到github仓库里面

## 把本地文件夹推送到github仓库上面

1. git init : 把本地文件夹变成git仓库

2. 然后同上1~5步(2和3步可以省略)

3. git remote add 别名 远程仓库的链接(https)

4. git push origin 分支 [-u] : 把本地历史区推送到github仓库里面