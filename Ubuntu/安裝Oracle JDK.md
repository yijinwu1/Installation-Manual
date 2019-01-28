*   前置作業(以下請自行安裝)
    > Widows10。
    
    > VirtualBox虛擬機已安裝Ubuntu。[下載VirtualBox](https://www.virtualbox.org/wiki/Downloads)
    
*   安裝Oracle JDK
    > 指令「sudo –i」→指令「add-apt-repository ppa:webupd8team/java」。
	>> 1.切換身分為管理員(root)。<br>
	>> 2.因為Oracle JDK 非open source，所以要先新增一個ppa。，ppa為Debin派的third-party倉庫。
    
    > ![ubuntu1](../../master/Ubuntu/images/OracleJDK1.PNG)
    
    > 指令「cd /etc」→指令「ls –l /etc/apt/sources.list.d」→指令「apt update」。
	>> 1.切換到 /etc 目錄下。<br>
	>> 2.確認是否有目錄 /etc/apt/sources.list.d。<br>
	>> 3.確認完成，更新。
	
    > ![ubuntu1](../../master/Ubuntu/images/OracleJDK2.PNG)
	
    > 指令「apt install oracle-java8-set-default」。
	>> 1.以安裝日期當下穩定的Oracle JDK版本為主。安裝Oracle JDK8 ->因安裝日期2017/11/12，故用Oracle JDK8版本。<br>
	>> 2.Configuring oracle-java8-installer，請選擇<Yes>。因為Oracle JDK屬於Oracle公司所有，需<Yes>同意授權條款才能安裝Oracle JDK。
    
    > ![ubuntu1](../../master/Ubuntu/images/OracleJDK3.PNG)
	> ![ubuntu1](../../master/Ubuntu/images/OracleJDK4.PNG)
	
	> 指令「java -version」→指令「javac -version」。(確認java的版本。)
    > ![ubuntu1](../../master/Ubuntu/images/OracleJDK5.PNG)	
	
	> 指令「update-alternatives --list java」。(查詢有幾套java的版本。)
    > ![ubuntu1](../../master/Ubuntu/images/OracleJDK6.PNG)	
	
	> 指令「update-alternatives --config java」。
	>> 1.Selection編號前面有「*」，為系統選擇。
	>> 2.可輸入自己想要的Java版本編號。
    > ![ubuntu1](../../master/Ubuntu/images/OracleJDK7.PNG)
