# General

#### Multi-line string to file

```Bash
kernel="2.6.39"
distro="xyz"
cat >/etc/myconfig.conf <<EOL
line 1, ${kernel}
line 2, 
line 3, ${distro}
line 4 line
... 
EOL

cat /etc/myconfig.conf
```
