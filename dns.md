# windows 下使用批处理设置dns服务器的办法：
http://stackoverflow.com/questions/18620173/how-can-i-set-change-dns-using-the-command-prompt-at-windows-8

```
netsh interface show interface

Which will show the name under the "Interface Name" column (shown here in bold):

Admin State    State          Type             Interface Name
-------------------------------------------------------------------------
Enabled        Connected      Dedicated        Ethernet
```

Now you can change the primary dns (index=1), assuming that your interface is static (not using dhcp):
```
netsh interface ipv4 add dnsserver "Ethernet" address=192.168.x.x index=1
```
