### git管理文件夹——版本控制

#### 第一天

- 进入文件夹

- ```
  cd /d/github/bbkz
  ```

- 初始化 提名——变成Master
  
  ```
  git init
  ```
  
- 管理 
  - git status
  - git add .
  
- 个人信息配置
  
  - 用户名、邮箱
  
- 生成版本
  
  ```git commit -m "版本名" ```

- 拓展新功能

- 回滚功能

  - ```
    git log
    git reset --hard 版本号
    ```

  - ```
    git reflog
    git reset --hard 版本号
    ```

#### 命令总结

```
git init 
git status
git add .
git commit -m "版本名"
git log
git reset --hard "版本号"
git reset

```

修复bug

#### 第二天

商城开发了50%

继续开发完成100%
```
命令总结：
git branch
git branch '分支名'
git checkout '分支名'
git merge 要合并的分支（注意切换），可能产生冲突
git branch -d '分支名'
```

工作流

```
master
dev
bug
```

GitHub学习

```
1.第一次在家写完代码上传
    git remote add origin '仓库地址'——给远程仓库起别名
    git push -u origin '分支名称'
2.到公司后新电脑第一次获取代码
    git clone '远程地址'(内部已实现起别名)
    git checkout '分支名'
3.在公司进行开发
    切换到dev分支进行开发
    	git checkout dev
    合并master分支到dev做更新
    	git  merge master——更新(一次)
	修改代码
	提交代码
		git add .
		git commit -m 'xxx'
		git push origin dev
4.回到家后继续写代码
	切换到dev分支进行开发
		git checkout dev
	拉代码
		git pull origin dev == 
		git fetch origin dev
		git merge origin/dev
			
	继续开发
	提交代码
		git add .
		git commit -m 'xxx'
		git push origin dev
	
```

rebase命令把多个连续本地版本仓库记录合并成一个

```
git rebase -i HEAD~2 当前版本和前一个版本合并成一个版本
```

#### 第三天

beyond compare工具解决冲突问题

```
两个工具配置在一起
git config --local merge.tool bc4
git config --local mergetool.path 'D:/Program Files/Beyond Compare 4'
git config --local mergetool.keepBackup false
```

记录图形展示

```
git log --graph --pretty=format:"%h %s"
```

##### 协同开发

```
1.创建新项目 mkdir person/dibhot
touch app.py
git init 
git add .
git commit -m '东北热基本功能'


```

