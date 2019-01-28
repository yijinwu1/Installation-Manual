*   前置作業(以下請自行安裝)
    > Widows10。
    
    > VirtualBox虛擬機已安裝Ubuntu。[下載VirtualBox](https://www.virtualbox.org/wiki/Downloads)
    
*   安裝Hadoop
    > 指令「sudo –i」→指令「cd /opt/」→指令「wget http://apache.stu.edu.tw/hadoop/common/hadoop-2.8.2/hadoop-2.8.2.tar.gz」。
	>> 1.切換身分為管理員(root)。<br>
	>> 2.切換到opt目錄。(opt為third-party應用程式置放區)<br>
	>> 3.使用 wget [參數][URL]，下載Hadoop版本。Hadoop版本以安裝日期當下穩定的版本為主。安裝Hadoop-2.8.2 ->因安裝日期2017/11/12，故用Hadoop-2.8.2。<br>
	>> 4.wget指令使用URL，請確認可連外網。[詳見安裝SSH套件遠端操作](https://github.com/yijinwu1/Installation-Manual/blob/master/Ubuntu/%E5%AE%89%E8%A3%9DSSH%E5%A5%97%E4%BB%B6%E9%81%A0%E7%AB%AF%E6%93%8D%E4%BD%9C.md)。<br>
	>> 5.[下載Hadoop版本](http://hadoop.apache.org/releases.html)。

    > ![ubuntu1](../../master/Ubuntu/images/Hadoop1.PNG)
    
    > 指令「tar -xvf hadoop-2.8.2.tar.gz -C /opt」。
	>> 使用打包指令tar。參數 - x:解壓縮、v:Verbose mode顯示詳細過程、f: -f filename。-C /opt 解壓縮到opt目錄下
	
    > ![ubuntu1](../../master/Ubuntu/images/Hadoop2.PNG)
	
    > 指令「ls -l」→指令「du –S hadoop-2.8.2 | wc」→指令「find hadoop-2.8.2/ | wc」。
	>> 1.確認解壓縮檔案，hadoop-2.8.2解壓縮完成。<br>
	>> 2.du:列出所有檔案大小。–S:不含子目錄，列出每個目錄占用容量。|:輸出command|輸入command。pipe運算元，pipleliness管線。wc:列出行、字、字元。
	>> 3.「du –S hadoop-2.8.2 | wc」:列出hadoop-2.8.2目錄下有多少檔案。<br>
	>> 4.find:搜尋。「find hadoop-2.8.2/ | wc」:搜尋含hadoop-2.8.2有多少。

    > ![ubuntu1](../../master/Ubuntu/images/Hadoop3.PNG)
	
	> 指令「adduser hadoop」。(建立hadoop帳號，並設定密碼。)
    > ![ubuntu1](../../master/Ubuntu/images/Hadoop4.PNG)	
	
	> 指令「chown -R hadoop:hadoop hadoop-2.8.2」。
	>> chown [參數] [owner][:[group]] 文件:變更目錄或文件的擁有者與群組。
	>> -R:包含所有子目錄。
	>>「chown -R hadoop:hadoop hadoop-2.8.2」:將hadoop-2.8.2目錄由502:dialout變更給hadoop:hadoop)
    > ![ubuntu1](../../master/Ubuntu/images/Hadoop5.PNG)	
	
	> 指令「cd hadoop/bin」→指令「ls -l」→指令「hadoop」顯示hadoop: command not found) →指令「./hadoop version」(告知在目錄下執行hadoop 版本。
    > ![ubuntu1](../../master/Ubuntu/images/Hadoop6.PNG)	
	
	> 指令「ln -s hadoop-2.8.2 hadoop」→指令「ls -la」。
	>> 1.ln [參數][原檔名][新檔名]:建立捷徑。「ln -s hadoop-2.8.2 hadoop」:將hadoop-2.8.2建立捷徑為hadoop。<br>
	>> 2.查詢建立的捷徑檔，新檔名 -> 原檔名。
    > ![ubuntu1](../../master/Ubuntu/images/Hadoop7.PNG)

	> 指令「cd ~hadoop」→指令「ls -la」。
	>> 尋找個人偏好的設定檔
    >> 1.切換至hadoop的家-使用者的個人目錄。
    >> 2.讀取使用者的個人設定檔依序如下~/.bash_profile → ~/.bash_login → ~/.profile。
    >> hadoop只找到 .profile檔，故改此設定檔。
    > ![ubuntu1](../../master/Ubuntu/images/Hadoop8.PNG)

	> 指令「nano .profile」。
	>> 使用nano編輯 .profile檔，設定hadoop的path環境變數。
    > ![ubuntu1](../../master/Ubuntu/images/Hadoop9.PNG)	
	
	> 「HADOOP_HOME=”/opt/hadoop”」 →「PTAH=”$ HADOOP_HOME/bin: …”」。
	>> 1. .profile檔，PATH上一行加入變數，HADOOP_HOME=”/opt/hadoop”。<br>
	>> 2. .profile檔，PATH路徑最前面加入，hadoop執行檔路徑。PATH=”$ HADOOP_HOME/bin: ”。<br>
	>> 3.nano編輯完成，ctrl+o存檔 → ctrl+x離開。<br>
	>> 4.修改環境變數PATH，登出再登入，PATH設定才可生效。<br>
    > ![ubuntu1](../../master/Ubuntu/images/Hadoop10.PNG)
	
	> 指令「su - hadoop」→指令「echo $PATH」→指令「hadoop version」。
	>> 1.切換到使用者hadoop。因為使用者hadoop，才有執行hadoop指令權限。<br>
	>> 2.印出環境變數 echo $PATH。確認設定的環境變數(PTAH: /opt/hadoop/bin)，是否設定成功。<br>
	>> 3.查詢hadoop指令設定成功。
    > ![ubuntu1](../../master/Ubuntu/images/Hadoop11.PNG)
