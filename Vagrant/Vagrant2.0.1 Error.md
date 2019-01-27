Fix Vagrant2.0.1 Git-Bash no shell prompt error
------------------------------------
1. Windows檔案總管，開啟檔案(C:\Program Files\Git\etc\profile.d\bash_profile.sh)

2. bash_profile.sh檔案，最後一行加入「export VAGRANT_PREFER_SYSTEM_BIN=1」

![LicenseAgreement](../../master/Vagrant/images/vagrant15.PNG) 

3.開啟Git Bash，切換到虛擬機所在目錄，啟動虛擬機(指令「vagrant up」)。出現命令提示字元。

![LicenseAgreement](../../master/Vagrant/images/vagrant16.PNG) 
