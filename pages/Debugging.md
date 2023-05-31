- > 调试代码。分为日志、debug、特殊工具、静态分析。
- Printf debugging and Logging
	- 日志输出要素
		- log to files, sockets or even reomte servers
		- support serverity levels
		- what msg and format to log
	- 语言自带实现
		- JavaScript: console.log, console.error，原理是输出不同。log 是 stdout，error 是 stderr。
	- Third party logs
		- 系统自带 shell
			- Linux: [journalctl命令 – 查看指定的日志信息](https://www.linuxcool.com/journalctl#:~:text=journalctl%E5%91%BD%E4%BB%A4%E6%9D%A5%E8%87%AA%E4%BA%8E%E8%8B%B1%E6%96%87,%E5%85%A8%E9%83%A8%E7%9A%84%E6%97%A5%E5%BF%97%E4%BF%A1%E6%81%AF%E4%BA%86%E3%80%82)，但 linux 上守护程序使用 systemd,则服务输出日志统一被重定向到`/var/log/journal`，使用 journalctl 则可查看他们
			- MacOS: /var/log/system.log，使用 log show 查看
		- 第三方平台
			- 使用 PM2 启动并统一收集单一服务日志。
			- 使用 Docker 自带的能力收集日志。
			- 使用 Kibana 收集一整个链路服务的日志。
			- 使用 Cat 收集服务日志。
- Debuggers
- Sepcialized Tools
	- NodeJS 的调试器
	- Golang 的调试器
- Static Analysis
	- JS = eslint+ts
	- Golang = go 工具集