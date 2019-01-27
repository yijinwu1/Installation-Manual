*   前置環境(以下請自行安裝並確認版本)

    > Widows10(PowerShell3.0以上)。
    
    > VirtualBoxb5.1.30以上。[下載VirtualBoxb](https://www.virtualbox.org/)
    
    > Git。[下載Git](https://git-scm.com/download/win)
    
    > 可對外網路。

*   安裝Vagrant2.0.1  [下載Vagrant](https://www.vagrantup.com/downloads.html)

    > 進入Vagrant快樂安裝畫面。

    > ![SetupWizard](../../master/Vagrant/images/vagrant1.PNG)

    > 下一步-->License Agreement

    > ![License Agreement](../../master/Vagrant/images/vagrant2.PNG)

    > 下一步-->安裝路徑，不變更

    > ![Install](../../master/Vagrant/images/vagrant3.PNG)

    > 下一步-->Install

    > ![Install](../../master/Vagrant/images/vagrant4.PNG)

    > 下一步-->Finish。(重新啟動電腦)

    > ![Install](../../master/Vagrant/images/vagrant6.PNG)
    
*   進入Vagrant。

    > 開啟GitBatch
    
    > ![GitBatch](../../master/Vagrant/images/vagrant6_1.PNG)

    > 建立專案目錄。指令「mkdir vagbento」

    > 切換至專案目錄。指令「cd vagbento」

    > ![Terminal](../../master/Vagrant/images/vagrant7.PNG)

    > 安裝ubuntu作業系統。指令「vagrant init bento/ubuntu-16.04」。(vagrant init 為專案第一次建立才需要執行指令，目的是要產生vagrantfile檔案[vagrantfile說明](https://www.vagrantup.com/docs/vagrantfile/))。若專案資料夾已有vagrantfile檔案，此指令不用執行。

    > ![Terminal](../../master/Vagrant/images/vagrant9.PNG)

    > 觀看vagrantfile檔。指令「cat -n vagrantfile | less」(確認vagrantfile檔設定)

    > ![Terminal](../../master/Vagrant/images/vagrant10.PNG)
    
    > vagrantfile檔設定。Box.vm.box = "bento/ubuntu-16.04"（user/base image 虛擬機要用的母機)

    > ![Terminal](../../master/Vagrant/images/vagrant11.PNG)
    
    > 建立並啟動虛擬機。指令「vagrant up」

    > ![Terminal](../../master/Vagrant/images/vagrant12.PNG)  

    > 關閉虛擬機。指令「vagrant halt」

    > ![Terminal](../../master/Vagrant/images/vagrant14.PNG)
