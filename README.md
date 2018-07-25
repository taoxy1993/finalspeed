### 一键安装代码：
```
wget -N --no-check-certificate https://raw.githubusercontent.com/taoxy1992/finalspeed/master/install_fs.sh && bash install_fs.sh
```
###一键卸载代码
```
wget -N --no-check-certificate https://raw.githubusercontent.com/taoxy1992/finalspeed/master/install_fs.sh && bash install_fs.sh uninstall
```
### finalspeed操作命令

启动： /etc/init.d/finalspeed start

停止命令：/etc/init.d/finalspeed stop

状态命令（查看日志）：/etc/init.d/finalspeed status

开机启动：vim /etc/rc.local 加入
/etc/init.d/finalspeed start

每天5点定时重启,6点清理log,7点清理内存：crontab -e 加入
0 7 * * *  echo 1 > /proc/sys/vm/drop_caches
0 6 * * * true > /fs/server.log
0 5 * * * /etc/init.d/finalspeed restart

### finalspeed安装路径

安装路径： /fs/

日志路径：/fs/server.log

