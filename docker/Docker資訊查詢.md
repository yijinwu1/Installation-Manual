Docker指令
-------------
*   啟動Docker-->開啟「Docker Quickstart Terminal」。VirtaulBox-->顯示 default(Docker Server)。

![Start Docker](../../master/images/docker8.PNG)

![Start Docker](../../master/images/docker9.PNG)

![Start Docker](../../master/images/docker10.PNG)

*   查詢虛擬機default資訊   
>核心版本：uname -a 

>OS版本：cat /etc/os-release

>帳號：cat /etc/passwd | wc -l

>CPU：cat /proc/cpuinfo

>Memory：free -h

>HD：df -h

>網路：lsof -nPi

>IP：ip a s | less

>程序相關性：pstree -p

>服務：cd /etc/init.d (Enert鍵) ls -l

>執行程序：ps -ef | grep 'docker'

*   Docker Quickstart Terminal查詢

>環境訊息：docker info 

>啟動Container：docker run 

>查image：docker images

>Container背景執行：docker run -d username/image name

>啟動Container：docker run --name XXX -i -t username/image name 

>查Container：docker ps -a 

>查執行中Container：docker ps

>：docker start xxx

>：docker attach xxx

>：docker stop

>：docker rm $(docker ps -a -q)

>：docker logs

>：docker history

>：exit
