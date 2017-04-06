-----------------------------   
#\#  serverSpeeder Install  \#    
-----------------------------      
----------------------------- 
#For Linux (simple)   
Usage    
```
Usage:     
      bash appex.sh [install |uninstall |install '{serverSpeeder of Kernel Version}']     
```
Install
```
wget --no-check-certificate -O appex.sh https://raw.githubusercontent.com/0oVicero0/serverSpeeder_Install/master/appex.sh && chmod +x appex.sh && bash appex.sh install

```    
Uninstall    
```
wget --no-check-certificate -O appex.sh https://raw.githubusercontent.com/0oVicero0/serverSpeeder_Install/master/appex.sh && chmod +x appex.sh && bash appex.sh uninstall

```  
-----------------------------     
使用此脚本安装时如遇许可证错误，可尝试使用此命令更新许可证。
```    
bash /appex/bin/serverSpeeder.sh renewLic
```

-----------------------------
-----------------------------    
部分用法说明(制作一键脚本或手动安装,仅供学习测试使用)
-----------------------------
具体用哪个加速模块检索这个文件,选择最合适的.         
```
https://github.com/0oVicero0/serverSpeeder_kernel/blob/master/serverSpeeder.txt
```
改加速模块文件名字.       
下载链接如下(变量$1,$2,$3,$4,$5,$6)   
```
https://raw.githubusercontent.com/0oVicero0/serverSpeeder_kernel/master/$1/$2/$3/$4/$5/$6
```
下载后的加速模块文件名改成这样  ```acce-$5-[$1_$2_$3]```            
如果不改名字,可能会触发某个BUG(Debian下会触发,别的系统没用过,不清楚.)           
许可证在这里生成: ```http://serverspeeder.azurewebsites.net/```             
(用Azure免费版搭建的,不支持```HTTPS```.)          
需要填写你机器网卡的MAC,点击OK就可以生成.                 
也可以直接在服务器上运行下面这句(一般情况下可用):      
```
wget -O apx.lic http://serverspeeder.azurewebsites.net/lic?mac=$(ifconfig |grep -B1 "$(wget -qO- ipv4.icanhazip.com)" |awk '/HWaddr/{ print $5 }')

```     
-----------------------------    
#仅供学习测试使用,严禁用于商业用途.
-----------------------------   
[萌咖 - MoeClub.org](https://MoeClub.org)    
-----------------------------      
-----------------------------   
For Linux.
—–
*.从根本原因上解决断流问题,断流的根本原因是没有完整破解验证机制.
*.锐速启动脚本不规范,修正Debian/Ubuntu不能正常自启动.
—–
1.支持自动检测公网网卡,采用官方检测网卡的方式.
2.支持自动匹配内核(可强制安装指定内核版本的锐速,此项专为CentOS设置,仅需查看锐速支持状况).
3.添加询问是否开启accppp功能.(实测并开启后没有效果.)
4.默认设置为G口宽带.(听说设置大点可以提高速度)
5.支持一键完全卸载(此脚本安装的无残留).
6.完美支持官方renewLic命令.
7.所需文件均来自GitHub,完全公开.
8.不支持自动更换内核,请自行更换.(网上教程非常多)
9.不支持OpenVZ,不需要尝试,会告诉你找不到网卡.
#.吐槽:CentOS居然连which都要自己安装,内核那么多!
心好累.脚本将就着看吧.
—–
##.除此脚本外,所有内容均来自互联网.本人不负任何法律责任,仅供学习使用.
#1.使用前请日常update.
#2.如果您是最小化安装系统,请确认您的系统能够执行ifconfig等命令.
#3.关于配置,请查看文章最后手册调教手册,调教后效果更好.
#4.如遇许可证错误,请用/appex/bin/serverSpeeder.sh renewLic命令更新许可证.


GitHub项目地址:
https://github.com/0oVicero0/serverSpeeder_Install
serverSpeeder support:
https://github.com/0oVicero0/serverSpeeder_kernel/blob/master/SystemList.md
serverSpeeder Install:

wget --no-check-certificate -qO /tmp/appex.sh "https://raw.githubusercontent.com/0oVicero0/serverSpeeder_Install/master/appex.sh" && bash /tmp/appex.sh 'install'
serverSpeeder Unstall:

wget --no-check-certificate -qO /tmp/appex.sh "https://raw.githubusercontent.com/0oVicero0/serverSpeeder_Install/master/appex.sh" && bash /tmp/appex.sh 'unstall'
serverSpeeder Advance Install:

wget --no-check-certificate -qO /tmp/appex.sh "https://raw.githubusercontent.com/0oVicero0/serverSpeeder_Install/master/appex.sh" && bash /tmp/appex.sh '${Kernel Version}'
使用方法:
启动命令 /appex/bin/serverSpeeder.sh start
停止加速 /appex/bin/serverSpeeder.sh stop
状态查询 /appex/bin/serverSpeeder.sh status
更新许可 /appex/bin/serverSpeeder.sh renewLic
重新启动 /appex/bin/serverSpeeder.sh restart
调教手册:
https://github.com/0oVicero0/serverSpeeder_Install/blob/master/lotServer.pdf
