*   前置作業(以下請自行安裝)
    > Widows10。
    
    > VirtualBox(Windows)。[下載VirtualBox](https://www.virtualbox.org/wiki/Downloads)
    
    > 對外網路可通。
    
    > 已安裝完成Ubuntu Linux-Desktop的vdi檔。
    
*   複製多台Ubuntu Linux-Desktop VM

    > 新增 → 建立虛擬機器
    
    > ![ubuntu1](../../master/Ubuntu/images/cpvm1.PNG)
    
    > 配置記憶體大小(實體8G → 2048MB)
    
    > ![ubuntu1](../../master/Ubuntu/images/cpvm2.PNG)
    
    > 硬碟(請選擇「不加入虛擬硬碟」，因為複製vdi檔。)
    
    > ![ubuntu1](../../master/Ubuntu/images/cpvm3.PNG)
    
     > 建立完成，虛擬機即產生。
    
    > ![ubuntu1](../../master/Ubuntu/images/cpvm4.PNG)
    
    > 將已安裝完成Ubuntu Linux-Desktop的vdi檔，複製到新建立的虛擬機資料夾中。並更名為虛擬機名稱。
    
    > ![ubuntu1](../../master/Ubuntu/images/cpvm5.PNG)
    
     > VirtuBox → 設定值 → 一般
     
     > ![ubuntu1](../../master/Ubuntu/images/cpvm6.PNG)
     
     > VirtuBox → 設定值 → 系統(開機順序勾選「光碟機、硬碟」)
     
     > ![ubuntu1](../../master/Ubuntu/images/cpvm7.PNG)
     
     > VirtuBox → 設定值 → 顯示(視訊記憶體拉到最大。加速勾選「啟用3D加速」，若顯示卡不強，此選項勿勾。)
     
     > ![ubuntu1](../../master/Ubuntu/images/cpvm8.PNG)
     
     > VirtuBox → 設定值 → 存放裝置 → 控制器:SATA → 加入硬碟
     
     > ![ubuntu1](../../master/Ubuntu/images/cpvm9.PNG)
     
     > 選擇現有的磁碟
     
     > ![ubuntu1](../../master/Ubuntu/images/cpvm10.PNG)
     
     > 選擇目前虛擬機中的vid檔(請先將準備好的vdi檔，複製到目前虛擬機的資料夾中)
     
     > ![ubuntu1](../../master/Ubuntu/images/cpvm11.PNG)
     
     > 出現此錯誤，請先修改vdi檔的UUID(Universally Unique IDentifier 通用唯一識別碼) 
     
     > ![ubuntu1](../../master/Ubuntu/images/cpvm12.PNG)
     
     > 開啟命令提示字元 → 切換到新建虛擬機vdi檔，所在目錄 → 輸入指令「"C:\Program Files\Oracle\VirtualBox\VBoxManage.exe" internalcommands sethduuid XXX.vdi」 
     
     > ![ubuntu1](../../master/Ubuntu/images/cpvm13.PNG)
     
     > 存放裝置選擇完成
     
     > ![ubuntu1](../../master/Ubuntu/images/cpvm14.PNG)
     
     > VirtuBox → 設定值 → 網路 → 介面卡1(勾選啟用網路卡，附加到NAT。NAT網路：各自獨立，可在任何地方使用，當Client。)
     
     > ![ubuntu1](../../master/Ubuntu/images/cpvm15.PNG)
     
     > 選擇虛擬機 → 啟動(確認完成，即掛載成功)
     
     > ![ubuntu1](../../master/Ubuntu/images/cpvm16.PNG)
     
     > 登入帳號、密碼(第一次登入的帳號、密碼會與來源的vid檔相同。之後再進行帳號創建與密碼修改。)
     
     > ![ubuntu1](../../master/Ubuntu/images/cpvm17.PNG)
