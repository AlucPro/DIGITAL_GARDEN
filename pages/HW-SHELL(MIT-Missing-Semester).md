- Q
	- [Exercises1](https://missing.csail.mit.edu/2020/course-shell/)
	- [Exercises2](https://missing.csail.mit.edu/2020/shell-tools/)
- A
	- 1、对于没有权限的 script.sh，可以这样执行 `sh ./script.sh`
	- 2、将所有启动任务，改写成快捷的`alias`
	- 3、自定义全局脚本
	- 4、ls 命令最佳展示
		- ```
		  $ l # zsh 别名，等同于下边这个
		  或
		  $ ls -alh # a全部，包括.开头的文件，l=list，h=human_read
		  ```
- HW: 设置你的 shell 为 oh my zsh ==@action==
  id:: 62a2941a-5feb-421d-a6c7-d89e118be328
	- REPO [ohmyzsh](https://github.com/ohmyzsh/ohmyzsh)
	- update `omz update` or `zsh`
	- features
		- 1、alias fo git and tmux → view all alias`alias | grep git`
		- 2、omz plugins
			- **[zsh-syntax-highlighting](https://github.com/zsh-users/zsh-syntax-highlighting)**
			- **[zsh-autosuggestions](https://github.com/zsh-users/zsh-autosuggestions)**
			- autojump
		-