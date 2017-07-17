虽然在CentOS操作系统中具有多语言包，但其man手册是英文的，对于新手来说能够使用中文man手册将加快学习速度。

工具/原料
Linux操作系统：CentOS 6.6
软件：manpages-zh-1.5.1.tar.gz
方法/步骤
1
将安装包下载到本地
http://pkgs.fedoraproject.org/repo/pkgs/man-pages-zh-CN/manpages-zh-1.5.1.tar.gz/13275fd039de8788b15151c896150bc4/
CentOS系统安装中文man手册
2
打开系统终端,输入：tar xf manpages-zh-1.5.1.tar.gz进行解压缩
CentOS系统安装中文man手册
CentOS系统安装中文man手册
3
cd manpages-zh-1.5.1
进入安装目录
CentOS系统安装中文man手册
4
./configure --disable-zhtw
安装配置
CentOS系统安装中文man手册
CentOS系统安装中文man手册
5
make && make install
安装
CentOS系统安装中文man手册
CentOS系统安装中文man手册
6
设置环境变量：vim /etc/profile.d/cman.sh
输入内容：
alias cman='man -M /usr/local/share/man/zh_CN'
保存退出
CentOS系统安装中文man手册
CentOS系统安装中文man手册
7
source /etc/profile.d/cman.sh
重新执行别名文件
CentOS系统安装中文man手册
8
测试，输入命令：cman ls
CentOS系统安装中文man手册
END
注意事项
中文帮助手册的使用命令是cman,目前只翻译部分不是所有的帮助都是中文
如果想使用英文帮助，可以使用命令man
