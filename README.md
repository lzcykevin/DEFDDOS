# DEFDDOS

## INSTALL
``` bash
wget https://raw.githubusercontent.com/lzcykevin/DEFDDOS/master/install.sh
chmod +x install.sh
./install.sh
``` 
## UNINSTALL
``` bash
wget https://raw.githubusercontent.com/lzcykevin/DEFDDOS/master/uninstall.sh
chmod +x uninstall.sh
./uninstall.sh
``` 
## CONFIG
``` bash
/usr/local/ddos/ddos.conf
##### Paths of the script and other files
PROGDIR="/usr/local/ddos"
PROG="/usr/local/ddos/ddos.sh"
IGNORE_IP_LIST="/usr/local/ddos/ignore.ip.list"
CRON="/etc/cron.d/ddos.cron"
APF="/etc/apf/apf"
IPT="/sbin/iptables"

##### frequency in minutes for running the script
##### Caution: Every time this setting is changed, run the script with --cron 多少分钟执行一次统计
#####          option so that the new frequency takes effect
FREQ=1

##### How many connections define a bad IP? Indicate that below. 当一个IP的最大连接是多少的时候阻止它
NO_OF_CONNECTIONS=150

##### APF_BAN=1 (Make sure your APF version is atleast 0.96，确定安装APF并且版本大雨0.96)
##### APF_BAN=0 (Uses iptables for banning ips instead of APF，用iptables代理APF)
APF_BAN=1

##### KILL=0 (Bad IPs are'nt banned, good for interactive execution of script)
##### KILL=1 (Recommended setting，推荐设置)
KILL=1

##### An email is sent to the following address when an IP is banned.阻止一个IP后通知谁
##### Blank would suppress sending of mails
EMAIL_TO="root"

##### Number of seconds the banned
```
