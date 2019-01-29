### Linux常见操作命令

关机 ： shutdown -h now   &  half   &  poweroff

重启 ： reboot

图形界面： init 5  &  startx

复制： cp

移动： mv

删除： rm  //加-rf参数表示强制删除

创建文件夹： mkdir

创建文件： touch

显示文件内容： cat

分页显示文件内容： more   //空格键下一页，b键上一页

显示内容并在前面加行号： nl

显示第n行内容： head -n filename

显示后n行内容： tail -n filename

显示分区空间大小占用情况：df -h

显示文件或文件夹大小：du

分区设置：fdisk

硬连接及软连接：ln [-s] 源文件 连接文件，加参数-s是软连接，不加则为硬链接。

***

改变权限

- chown 改变所属人 chown root:root install.log 	//第一个参数是拥有者，第二个参数是可使用人群
- chmod 改变权限 
  - 1）chmod 777 test    //第一个数字表示拥有者权限，第二个数字表示使用者组人群权限，第三个数字表示其他用户权限
  - 2）chmod [ugoa...][[+-=][rwxX]...][,...]    //u表示拥有者，g表组，o表其他	+表增加权限，=表示唯一权限	r读，w写，x 可执行

五大查找命令

- find：*find <指定目录> <指定条件> <指定动作>*，如果什么参数也不加，find默认搜索当前目录及其子目录，并且不过滤任何结果，将它们全都显示在屏幕上。

  find的使用实例：``$ find . -name "my*"``：搜索当前目录（含子目录）中，所有文件名以my开头的文件。

  ``$ find . -name "my\*" -ls``：同上并显示他们的详细信息。

- locate、whereis、which、type：五大查找详细讲解见[查找](https://www.cnblogs.com/kex1n/p/5233821.html)。 

***

查看内核版本：gcc -v

查看当前用户：whoami

对文件及文件夹属性的快速修改：chattr +i filename。

- +i：锁定，不允许对此文件或文件夹内进行任何操作
- -i：解锁；
- +a：只能加文件，不能删除；
- -d：不可删除

***

列出系统有所分区：mount

挂载U盘：fdisk之后找到U盘，``mount U盘 要挂载的文件夹``

卸载U盘：umount  u盘

显示或设置网络设备：ifconfig

观看后台暂停程序：jobs -l

前台/后台运行：fg/bg

查看后台程序：ps aux

显示开机到现在时间：uptime

