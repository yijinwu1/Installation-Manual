新增Box。[Box市集](https://www.vagrantup.com/)。
> $ vagrant box add --name {box name} {box url}

已下載Box
> $ vagrant box list

打包Box。(預設package.box)
> $ vagrant package --output package.box

產生vagrantfile
> $ vagrant init bento/ubunto-16.04

啟動虛擬機
> $ vagrant up

登入虛擬機
> $ vagrant ssh

關閉虛擬機
> $ vagrant halt

重新啟動虛擬機(等同於vagrant halt + vagrant up 指令一起執行。)
> $ vagrant reload

虛擬機狀態
> $ vagrant status

刪除虛擬機
> $ vagrant destroy

vagrant指令說明
> $ vagrant help
