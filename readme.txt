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
第七步：查看提交历史
	git log

