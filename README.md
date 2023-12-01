# 无root进行搞机       
> 若您已安装Magisk但不会使用或不会安装请跳转到[Magisk文档](https://chouge1huao.github.io/MagiskDocument/)        
    
大家都知道搞机肯定需要权限然而没有root怎么办呢这里我列出几种能够获取并管理权限的应用      
## Shizuku 这个想必大多数人都知道它是用来提供adb接口给其他应用使用缺点是每次重启要重新激活有三种激活方式      
1.root这个激活方式就不多提了毕竟是无root         
![](images/sroot.png)
2.adb通过电脑连接用adb权限执行一个sh进行激活            
![](images/sadb.png)          
3.无线调试这种激活方式是无root电脑的首选需要安卓11及以上自带缺点是需要网络但是安卓10及以下其实也可以他会借用usb调试的接口在电脑上执行这样一串adb指令 adb tcpip 5555最后就可以使用无线调试了  
![](images/s.png)

   
## Dhizuku 这个是仿照Shizuku的提供设备管理员的接口也就是说激活了他你可以给多个应用授权设备管理员(需支持Dhizuku强制接入教程后面会说)          
目前有两种激活方式(将dhizuku设为设备管理员)
1.shizuku用shizuku授权自动执行命令激活        
2.使用shll执行命令        
电脑:adb shell dpm set-device-owner com.rosan.dhizuku/.server.DhizukuDAReceiver          
手机终端:dpm set-device-owner com.rosan.dhizuku/.server.DhizukuDAReceiver         
强制接入:     
准备好以下软件       
Dhiziku       
DAX模块     
任意XP框架      
只要把DAX模块作用到要接入的应用即可

## 免rootXP框架     
太极     
LSPatch     
使用教程      
1.激活   
LSPatch管理器需要Shizuku激活进入软件后点击上方卡片即可授权          
2.使用       
进入管理界面我可以看到尚无已修补的应用几个大字点击+号会弹出这样一个界面(如上图)点击确定随便选一个文件夹或创建一个以后这个生成的新apk就会在这个文件夹里了接下来选择你要使用xp模块的应用如果已经安装了就选择选择已安装的apk没有安装选择从存储目录里选择apk接下来会进入修补页面这是重点       
可以看到有本地模式和集成模式两种       
1.本地       
本地模式的模块作用域可以更换但需要软件保活还只在本机上有用      
2.集成           
可以内嵌模块但作用域不可更改不需要保活分享出apk可以在别的设备上使用      
可以根据自己的使用习惯进行选择接下来只要选择开始修补等待修补完成安装即可      
这样我们就可以进行愉快的玩耍了      

