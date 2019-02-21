*   在初始化 Vagrant 時，系統會自動產生 Vagrantfile 
*   Vagrantfile 就是每一台的虛擬機的規格表。每次我們啟動或部署 Vagrant 虛擬機時就是依據這一份設置文件 (configuration file) 來進行定義的
*   打開Vagrantfile檔案，真正有用到的配置其實只有短短幾行。告訴 Vagrant 我們想要用 hashicorp/precise64 當作我們這台虛擬機的 box。
    > ![Install](../../master/Vagrant/images/vf1.png)
*   Vagrantfile 中加入下列設置來替我們的虛擬機命名    
    > ![Install](../../master/Vagrant/images/vf2.png)
*   如果想讓虛擬機啟動時，自動執行一些初始化腳本，可透過 Vagrant 的 provisioning 功能，把初始化的 script 寫在 Vagrantfile 裡面的 provision 區塊。
*   此範本為依次安裝多台虛擬機[Vagrantfile範本](https://github.com/yijinwu1/Installation-Manual/blob/master/Vagrant/Vagrantfile)    
    > ![Install](../../master/Vagrant/images/vf3.png)
    > 要做幾台，就複製幾段    
    > config.vm.define "master1"：為虛擬機命名
    > node.vm.hostname = "master1"：設定hostname
    > node.vm.network :public_network, ip: "192.168.33.90"：設定網路橋接方式
    > v.cpus = 1：cpu
    > v.memory = 1024：ram大小 
    > node.vm.provision "shell", path: "scripts/sethosts.sh", run: "always：shell檔路徑
