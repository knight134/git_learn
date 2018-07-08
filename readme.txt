创建一个空的目录用来学习git使用
第一步：建立空仓库repository ，初始化一个目录，在该目录下会自动创建.git目录
	git init
第二步：将文件加入版本库。  所有的版本控制系统都只能跟踪文本文件的改动。很适合代码的版本控制。
	git add readme.txt
	告诉git把文件添加到仓库
第三步：执行所有提交改动
	git commit -m "add readme.txt file,添加第一个文件"
第四步：查看文件的改动
	git diff readme.txt
第五步：提交修改后的文件（提交文件的改动和添加新文件是一样的命令）
	git add readme.txt
	git commit -m "add new info"
第六步：版本回退，每次执行commit操作之后形成一个新的版本。
			此操作是commit的撤销操作么？
			git log        查看提交历史，里面查找存在的版本
			git reflog			查看命令历史，查看所有的版本号
			git reset --hard HEAD^     回退到上一个版本
			git reset --hard 8eb3f8b   回退到一个指定版本
第七步：查看提交历史
	git log
	git reflog
第八步：撤销修改
	git checkout -- readme.txt        将当前文件撤销到最近一次commit 或 add
	git reset HEAD readme.txt					如果文件已经add，此操作撤销add操作，配上上一个命令可以
	将当前文件与主版本一致。
第九步：删除文件
	git rm test.txt 			删除某个文件
	git commit -m ""
	如果某个文件被删除，需要撤销
	git checkout -- test.txt

第十步：远程仓库，创建SSH Key
	ssh-keygen -t rsa -C "knight134@163.com"
	id_rsa 和 id_rsa.pub 两个相关文件
第十一步：将本地仓库与github上的远程仓库关联。
	git remote add origin https://github.com/knight134/git_learn.git
	使用ssh
	git remote add origin git@github.com:knight134/git_learn.git
	origin 是对远程仓库的重命名

